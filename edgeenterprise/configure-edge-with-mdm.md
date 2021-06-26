---
title: Configurar Microsoft Edge con Administración de dispositivos móviles
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 04/06/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar Microsoft Edge con Administración de dispositivos móviles.
ms.openlocfilehash: a24e6d171707cdc02b6dbecb573e1238f1273426
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617610"
---
# <a name="configure-microsoft-edge-using-mobile-device-management"></a><span data-ttu-id="ac3f1-103">Configurar Microsoft Edge con Administración de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="ac3f1-103">Configure Microsoft Edge using Mobile Device Management</span></span>

<span data-ttu-id="ac3f1-104">En este artículo se explica cómo configurar Microsoft Edge en Windows 10 con [Administración de dispositivos móviles (MDM)](/windows/client-management/mdm/), mediante [Ingesta ADMX](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-104">This article explains how to configure Microsoft Edge on Windows 10 using [Mobile Device Management (MDM)](/windows/client-management/mdm/) by means of [ADMX Ingestion](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span> <span data-ttu-id="ac3f1-105">Este artículo describe también:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-105">This article also describes:</span></span>

- <span data-ttu-id="ac3f1-106">Cómo [crear un identificador uniforme de recursos Open Mobile Alliance (OMA-URI) para directivas de Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-106">How to [create Open Mobile Alliance Uniform Resource Identifier (OMA-URI) for Microsoft Edge policies](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>
- <span data-ttu-id="ac3f1-107">Cómo [configurar Microsoft Edge en Intune usando la ingesta ADMX y OMA-URI personalizado](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-107">How to [configure Microsoft Edge in Intune using ADMX ingestion and custom OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

> [!NOTE]
> <span data-ttu-id="ac3f1-108">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ac3f1-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ac3f1-109">Prerequisites</span></span>

<span data-ttu-id="ac3f1-110">Windows 10, con los siguientes requisitos mínimos del sistema:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-110">Windows 10, with the following minimum system requirements:</span></span>

- <span data-ttu-id="ac3f1-111">Windows 10, versión 1903 con [KB4512941](https://support.microsoft.com/help/4512941/) y [KB4517211](https://support.microsoft.com/help/4517211/) instaladas</span><span class="sxs-lookup"><span data-stu-id="ac3f1-111">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/help/4512941/) and [KB4517211](https://support.microsoft.com/help/4517211/) installed</span></span>
- <span data-ttu-id="ac3f1-112">Windows 10, versión 1809 con [KB4512534](https://support.microsoft.com/help/4512534/) y [KB4520062](https://support.microsoft.com/help/4520062/) instaladas</span><span class="sxs-lookup"><span data-stu-id="ac3f1-112">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/help/4512534/) and [KB4520062](https://support.microsoft.com/help/4520062/) installed</span></span>
- <span data-ttu-id="ac3f1-113">Windows 10, versión 1803 con [KB4512509](https://support.microsoft.com/help/4512509/) y [KB4519978](https://support.microsoft.com/help/4519978) instaladas</span><span class="sxs-lookup"><span data-stu-id="ac3f1-113">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/help/4512509/) and [KB4519978](https://support.microsoft.com/help/4519978) installed</span></span>
- <span data-ttu-id="ac3f1-114">Windows 10, versión 1709 con [KB4516071](https://support.microsoft.com/help/4516071/) y [KB4520006](https://support.microsoft.com/help/4520006) instaladas</span><span class="sxs-lookup"><span data-stu-id="ac3f1-114">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/help/4516071/) and [KB4520006](https://support.microsoft.com/help/4520006) installed</span></span>

## <a name="overview"></a><span data-ttu-id="ac3f1-115">Introducción</span><span class="sxs-lookup"><span data-stu-id="ac3f1-115">Overview</span></span>

<span data-ttu-id="ac3f1-116">Puedes configurar Microsoft Edge en Windows 10 usando MDM con tu proveedor de administración de movilidad empresarial (EMM) o MDM preferido que admita [Ingesta ADMX](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-116">You can configure Microsoft Edge on Windows 10 using MDM with your preferred Enterprise Mobility Management (EMM) or MDM provider that supports [ADMX Ingestion](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span>

<span data-ttu-id="ac3f1-117">La configuración de Microsoft Edge con MDM es un proceso de dos partes:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-117">Configuring Microsoft Edge with MDM is a two part process:</span></span>

1. <span data-ttu-id="ac3f1-118">Ingestión del archivo ADMX de Microsoft Edge en el proveedor EMM o MDM.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-118">Ingesting the Microsoft Edge ADMX file into your EMM or MDM provider.</span></span> <span data-ttu-id="ac3f1-119">Consulta a tu proveedor para obtener instrucciones sobre cómo ingerir un archivo ADMX.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-119">See your provider for instructions on how to ingest an ADMX file.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ac3f1-120">Para Microsoft Intune, consulta [Configurar Microsoft Edge en intune con la ingesta ADMX](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-120">For Microsoft Intune, see [Configure Microsoft Edge in Intune using ADMX ingestion](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

2. <span data-ttu-id="ac3f1-121">[Creación de un OMA-URI para una directiva de Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-121">[Creating an OMA-URI for a Microsoft Edge policy](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>

## <a name="create-an-oma-uri-for-microsoft-edge-policies"></a><span data-ttu-id="ac3f1-122">Crear un OMA-URI para directivas de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ac3f1-122">Create an OMA-URI for Microsoft Edge policies</span></span>

<span data-ttu-id="ac3f1-123">En las siguientes secciones se describe cómo crear la ruta de acceso OMA-URI y buscar y definir el valor en formato XML para las directivas de explorador obligatorias y recomendadas.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-123">The following sections describe how to create the OMA-URI path and look up and define the value in XML format for mandatory and recommended browser polices.</span></span>

<span data-ttu-id="ac3f1-124">Antes de empezar, descarga el archivo de plantillas de directiva de Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) desde la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) y extrae el contenido.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-124">Before you get started download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span>

<span data-ttu-id="ac3f1-125">Hay tres pasos para definir el OMA-URI:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-125">There are three steps for defining the OMA-URI:</span></span>

1. [<span data-ttu-id="ac3f1-126">Crear la ruta OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-126">Create the OMA-URI path</span></span>](#create-the-oma-uri-path)
2. [<span data-ttu-id="ac3f1-127">Especificar el tipo de datos OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-127">Specify the OMA-URI data type</span></span>](#specify-the-data-type)
3. [<span data-ttu-id="ac3f1-128">Establecer el valor OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-128">Set the OMA-URI value</span></span>](#set-the-value-for-a-browser-policy)

### <a name="create-the-oma-uri-path"></a><span data-ttu-id="ac3f1-129">Crear la ruta OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-129">Create the OMA-URI path</span></span>

<span data-ttu-id="ac3f1-130">Usa la fórmula siguiente como guía para crear las rutas de acceso OMA-URI.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-130">Use the following formula as a guide for creating the OMA-URI paths.</span></span> <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| <span data-ttu-id="ac3f1-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac3f1-131">Parameter</span></span>         | <span data-ttu-id="ac3f1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac3f1-132">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | <span data-ttu-id="ac3f1-133">Usa "Edge" o lo que hayas definido al ingerir la plantilla administrativa.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-133">Use "Edge" or what you defined when ingesting the administrative template.</span></span> <span data-ttu-id="ac3f1-134">Por ejemplo, si usaste "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", usa "MicrosoftEdge".</span><span class="sxs-lookup"><span data-stu-id="ac3f1-134">For example, if you used "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", then use "MicrosoftEdge".</span></span><br/><br/> <span data-ttu-id="ac3f1-135">El `<ADMXIngestionName>` debe coincidir con lo usado al ingerir el archivo ADMX.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-135">The `<ADMXIngestionName>` must match what was used when you ingested the ADMX file.</span></span> |
| \<ADMXNamespace>  | <span data-ttu-id="ac3f1-136">"microsoft_edge" o "microsoft_edge_recommended", en función de si estás estableciendo una directiva obligatoria o recomendada.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-136">Either "microsoft_edge" or "microsoft_edge_recommended" depending on whether you're setting a mandatory or recommended policy.</span></span> |
| \<ADMXCategory>   | <span data-ttu-id="ac3f1-137">La "parentCategory" de la directiva se define en el archivo ADMX.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-137">The "parentCategory" of the policy is defined in the ADMX file.</span></span> <span data-ttu-id="ac3f1-138">Omite la `<ADMXCategory>` si la directiva no está agrupada (no está definida "parentCategory").</span><span class="sxs-lookup"><span data-stu-id="ac3f1-138">Omit the `<ADMXCategory>` if the policy isn't grouped (No "parentCategory" defined).</span></span> |
| \<PolicyName>     | <span data-ttu-id="ac3f1-139">El nombre de la directiva se puede encontrar en el artículo [Referencia de directivas de explorador](./microsoft-edge-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="ac3f1-139">The policy name can be found in the [Browser policy reference](./microsoft-edge-policies.md) article.</span></span> |

#### <a name="uri-path-example"></a><span data-ttu-id="ac3f1-140">Ejemplos de rutas de URI:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-140">URI path example:</span></span>

<span data-ttu-id="ac3f1-141">Para este ejemplo, supongamos que el nodo `<ADMXIngestName>` se denominó “Edge" y que estás estableciendo una directiva obligatoria.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-141">For this example, assume the `<ADMXIngestName>` node was named “Edge" and you're setting a mandatory policy.</span></span> <span data-ttu-id="ac3f1-142">La ruta de acceso URI sería:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-142">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

<span data-ttu-id="ac3f1-143">Si la directiva no está en un grupo (por ejemplo, DiskCacheSize), quita "`~<ADMXCategory>`".</span><span class="sxs-lookup"><span data-stu-id="ac3f1-143">If the policy isn't in a group (for example, DiskCacheSize) remove "`~<ADMXCategory>`".</span></span> <span data-ttu-id="ac3f1-144">Sustituye `<PolicyName>` por el nombre de la directiva, DiskCacheSize.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-144">Replace `<PolicyName>` with the name of the policy, DiskCacheSize.</span></span> <span data-ttu-id="ac3f1-145">La ruta URI sería:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-145">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

<span data-ttu-id="ac3f1-146">Si la directiva está en un grupo, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-146">If the policy is in a group, follow these steps:</span></span>

1. <span data-ttu-id="ac3f1-147">Abre **msedge.admx** con cualquier editor de xml.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-147">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="ac3f1-148">Busca el nombre de la directiva que deseas establecer.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-148">Search for the policy name you want to set.</span></span> <span data-ttu-id="ac3f1-149">Por ejemplo, "ExtensionInstallForceList".</span><span class="sxs-lookup"><span data-stu-id="ac3f1-149">For example, "ExtensionInstallForceList".</span></span>
3. <span data-ttu-id="ac3f1-150">Usa el valor del atributo *ref* del elemento *parentCategory*.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-150">Use the value of the *ref* attribute from the *parentCategory* element.</span></span> <span data-ttu-id="ac3f1-151">Por ejemplo, "Extensiones" de \<parentCategory ref=" Extensions"/>.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-151">For example, "Extensions" from \<parentCategory ref=" Extensions"/>.</span></span>
4. <span data-ttu-id="ac3f1-152">Reemplaza `<ADMXCategory>` por el valor del atributo *ref* para crear la ruta URI.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-152">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path.</span></span> <span data-ttu-id="ac3f1-153">La ruta URI sería:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-153">The URI path would be:</span></span><br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### <a name="specify-the-data-type"></a><span data-ttu-id="ac3f1-154">Especificar el tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ac3f1-154">Specify the data type</span></span>

<span data-ttu-id="ac3f1-155">El tipo de datos OMA-URI siempre es “String”.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-155">The OMA-URI data type is always “String”.</span></span>

### <a name="set-the-value-for-a-browser-policy"></a><span data-ttu-id="ac3f1-156">Establecer el valor de una directiva de explorador</span><span class="sxs-lookup"><span data-stu-id="ac3f1-156">Set the value for a browser policy</span></span>

<span data-ttu-id="ac3f1-157">En esta sección se describe cómo establecer el valor en formato XML para cada tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-157">This section describes how to set the value, in XML format, for each data type.</span></span> <span data-ttu-id="ac3f1-158">Ve a la [Referencia de directivas de explorador](./microsoft-edge-policies.md) para buscar el tipo de datos de la directiva.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-158">Go to [Browser policy reference](./microsoft-edge-policies.md) to look up the data type of the policy.</span></span>

> [!NOTE]
> <span data-ttu-id="ac3f1-159">Para los tipos de datos que no sean booleanos, el valor siempre comienza por `<enabled/>`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-159">For non-Boolean data types, the value always starts with `<enabled/>`.</span></span>

#### <a name="boolean-data-type"></a><span data-ttu-id="ac3f1-160">Tipo de datos booleano</span><span class="sxs-lookup"><span data-stu-id="ac3f1-160">Boolean data type</span></span>

<span data-ttu-id="ac3f1-161">Para las directivas que sean tipos booleanos, usa `<enabled/>` o `<disabled/>`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-161">For policies that are Boolean types use `<enabled/>` or `<disabled/>`.</span></span>

#### <a name="integer-data-type"></a><span data-ttu-id="ac3f1-162">Tipo de datos enteros</span><span class="sxs-lookup"><span data-stu-id="ac3f1-162">Integer data type</span></span>

<span data-ttu-id="ac3f1-163">El valor siempre debe comenzar con el elemento `<enabled/>`, seguido de `<data id="[valueName]" value="[decimal value]"/>`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-163">The value always needs to start with the `<enabled/>` element followed by `<data id="[valueName]" value="[decimal value]"/>`.</span></span>

<span data-ttu-id="ac3f1-164">Para buscar el nombre de valor y el valor decimal de una página de nueva pestaña, sigue los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-164">To find the value name and decimal value for a new tab page, use the following steps:</span></span>

1. <span data-ttu-id="ac3f1-165">Abre **msedge.admx** con cualquier editor de xml.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-165">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="ac3f1-166">Busca el elemento `<policy>` en el que el atributo de nombre coincida con el nombre de directiva que deseas establecer.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-166">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="ac3f1-167">Para "RestoreOnStartup", busca `name="RestoreOnStartup"`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-167">For "RestoreOnStartup", search for `name="RestoreOnStartup"`.</span></span>
3. <span data-ttu-id="ac3f1-168">En el nodo `<elements>`, busca el valor que quieras establecer.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-168">In the `<elements>` node, find the value you want to set.</span></span>
4. <span data-ttu-id="ac3f1-169">Usa el valor en el atributo "valueName" del nodo `<elements>`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-169">Use the value in the "valueName" attribute in the `<elements>` node.</span></span> <span data-ttu-id="ac3f1-170">Para "RestoreOnStartup", "valueName" es "RestoreOnStartup".</span><span class="sxs-lookup"><span data-stu-id="ac3f1-170">For "RestoreOnStartup" the "valueName" is "RestoreOnStartup".</span></span>
5. <span data-ttu-id="ac3f1-171">Usa el valor del atributo "value" en el nodo `<decimal>`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-171">Use the value in the "value" attribute in the `<decimal>` node.</span></span> <span data-ttu-id="ac3f1-172">Para que "RestoreOnStartup" abra la página de nueva pestaña, el valor es "5".</span><span class="sxs-lookup"><span data-stu-id="ac3f1-172">For "RestoreOnStartup" to open the new tab page the value is "5".</span></span>

<span data-ttu-id="ac3f1-173">Para abrir la página de nueva pestaña en el inicio, usa:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-173">To open the new tab page on startup use:</span></span><br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### <a name="list-of-strings-data-type"></a><span data-ttu-id="ac3f1-174">Lista de tipos de datos de cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-174">List of strings data type</span></span>

<span data-ttu-id="ac3f1-175">El valor siempre debe comenzar con el elemento `<enabled/>`, seguido de `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-175">The value always needs to start with the `<enabled/>` element followed by `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.</span></span>

> [!NOTE]
> <span data-ttu-id="ac3f1-176">El nombre de atributo "id=" no es el nombre de la directiva, incluso aunque en la mayoría de los casos coincida con el nombre de la directiva.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-176">The "id=" attribute name isn't the policy name, even though in most cases it matches the policy name.</span></span> <span data-ttu-id="ac3f1-177">Es el valor del atributo de id de nodo \<list>, que se encuentra en el archivo ADMX.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-177">It's the \<list> node id attribute value, which is found in the ADMX file.</span></span>

<span data-ttu-id="ac3f1-178">Para buscar el listID y definir el valor para bloquear una dirección URL, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-178">To find the listID and define the value to block a URL, follow these steps:</span></span>

1. <span data-ttu-id="ac3f1-179">Abre **msedge.admx** con cualquier editor de xml.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-179">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="ac3f1-180">Busca el elemento `<policy>` en el que el atributo de nombre coincida con el nombre de directiva que deseas establecer.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-180">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="ac3f1-181">Para "URLBlocklist", busca `name="URLBlocklist"`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-181">For "URLBlocklist", search for `name="URLBlocklist"`.</span></span>
3. <span data-ttu-id="ac3f1-182">Usa el valor del atributo "id" del nodo `<list> node for [listID]`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-182">Use the value in the "id" attribute of the `<list> node for [listID]`.</span></span>
4. <span data-ttu-id="ac3f1-183">El "value" es una lista de direcciones URL separadas por punto y coma (;)</span><span class="sxs-lookup"><span data-stu-id="ac3f1-183">The "value" is a list of URLs separated by a semicolon (;)</span></span>

<span data-ttu-id="ac3f1-184">Por ejemplo, para bloquear el acceso a `contoso.com` y `https://ssl.server.com`:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-184">For example, to block access to `contoso.com` and `https://ssl.server.com`:</span></span><br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### <a name="dictionary-or-string-data-type"></a><span data-ttu-id="ac3f1-185">Diccionario de tipos de datos de cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-185">Dictionary or String data type</span></span>

<span data-ttu-id="ac3f1-186">El valor siempre debe comenzar por `<enabled/>`, seguido de `<data id="[textID]" value="[string]"/>`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-186">The value always needs to start with the `<enabled/>` followed by `<data id="[textID]" value="[string]"/>` .</span></span>

<span data-ttu-id="ac3f1-187">Para buscar el textID y definir el valor establecido para la configuración regional, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-187">To find the textID and define the value set the locale, follow these steps:</span></span>

1. <span data-ttu-id="ac3f1-188">Abre **msedge.admx** con cualquier editor de xml.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-188">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="ac3f1-189">Busca el elemento `<policy>` en el que el atributo de nombre coincida con el nombre de directiva que deseas establecer.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-189">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="ac3f1-190">Para "ApplicationLocaleValue", busca `name="ApplicationLocaleValue"`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-190">For "ApplicationLocaleValue", search for `name="ApplicationLocaleValue"`.</span></span>
3. <span data-ttu-id="ac3f1-191">Usa el valor del atributo "id" del nodo `<text>` para `[textID]`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-191">Use the value in the "id" attribute of the `<text>` node for `[textID]`.</span></span>
4. <span data-ttu-id="ac3f1-192">Establece el "valor" en el código de cultura.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-192">Set the "value" to the culture code.</span></span>

<span data-ttu-id="ac3f1-193">Para establecer la configuración regional en "es-US" con la directiva "ApplicationLocaleValue":</span><span class="sxs-lookup"><span data-stu-id="ac3f1-193">To set the locale to "es-US" with the "ApplicationLocaleValue" policy:</span></span><br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### <a name="create-the-oma-uri-for-a-recommended-policies"></a><span data-ttu-id="ac3f1-194">Crear el OMA-URI para una directiva recomendada</span><span class="sxs-lookup"><span data-stu-id="ac3f1-194">Create the OMA-URI for a recommended policies</span></span>

<span data-ttu-id="ac3f1-195">La definición de la ruta URI para las directivas recomendadas depende de la directiva que quieras configurar.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-195">Defining the URI path for recommended policies depends on the policy you want to configure.</span></span>

#### <a name="to-define-the-uri-path-for-a-recommended-policy"></a><span data-ttu-id="ac3f1-196">Para definir la ruta URI para una directiva recomendada</span><span class="sxs-lookup"><span data-stu-id="ac3f1-196">To define the URI path for a recommended policy</span></span>

<span data-ttu-id="ac3f1-197">Usa la fórmula de ruta URI (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) y los siguientes pasos para definir la ruta URI:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-197">Use the URI path formula (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) and the following steps to define the URI path:</span></span>

1. <span data-ttu-id="ac3f1-198">Abre **msedge.admx** con cualquier editor de xml.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-198">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="ac3f1-199">Si la directiva que quieres configurar no está en un grupo, salta al paso 4 y quita `~<ADMXCategory>` de la ruta.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-199">If the policy you want to configure isn't in a group, skip to step 4 and remove `~<ADMXCategory>` from the path.</span></span>
3. <span data-ttu-id="ac3f1-200">Si la directiva que deseas configurar está en un grupo:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-200">If the policy you want to configure is in a group:</span></span>

   - <span data-ttu-id="ac3f1-201">Para buscar la `<ADMXCategory>`, busca la directiva que deseas establecer.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-201">To look up the `<ADMXCategory>`, search for the policy you want to set.</span></span> <span data-ttu-id="ac3f1-202">Al buscar, añade al final "_recommended" al nombre de la directiva.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-202">When searching append "_recommended" to the policy name.</span></span> <span data-ttu-id="ac3f1-203">Por ejemplo, una búsqueda de "RegisteredProtocolHandlers_recommended" presenta el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-203">For example, a search for "RegisteredProtocolHandlers_recommended” has the following result:</span></span>

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - <span data-ttu-id="ac3f1-204">Copia el valor del atributo *ref* del elemento `<parentCategory>`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-204">Copy the value of the *ref* attribute from the `<parentCategory>` element.</span></span> <span data-ttu-id="ac3f1-205">Para "ContentSettings", copia "ContentSettings_recommended" desde `<parentCategory ref=" ContentSettings_recommended"/>`.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-205">For "ContentSettings", copy "ContentSettings_recommended" from `<parentCategory ref=" ContentSettings_recommended"/>`.</span></span>
   - <span data-ttu-id="ac3f1-206">Reemplaza `<ADMXCategory>` por el valor del atributo *ref* para crear la ruta URI en la fórmula de ruta URI.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-206">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path in the URI path formula.</span></span>

4. <span data-ttu-id="ac3f1-207">El `<PolicyName>` es el nombre de la directiva con "_recommended" puesto al final.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-207">The `<PolicyName>` is the name of the policy with "_recommended" appended to it.</span></span>

#### <a name="oma-uri-path-examples-for-recommended-policies"></a><span data-ttu-id="ac3f1-208">Ejemplos de ruta OMA-URI para directivas recomendadas</span><span class="sxs-lookup"><span data-stu-id="ac3f1-208">OMA-URI path examples for recommended policies</span></span>

<span data-ttu-id="ac3f1-209">La siguiente tabla muestra ejemplos de rutas OMA-URI para las directivas recomendadas.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-209">The following table shows examples of OMA-URI paths for recommended policies.</span></span>

|              <span data-ttu-id="ac3f1-210">Directiva</span><span class="sxs-lookup"><span data-stu-id="ac3f1-210">Policy</span></span>               |             <span data-ttu-id="ac3f1-211">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-211">OMA-URI</span></span>                      |
|-----------------------------------|------------------------------------------|
| [<span data-ttu-id="ac3f1-212">RegisteredProtocolHandlers</span><span class="sxs-lookup"><span data-stu-id="ac3f1-212">RegisteredProtocolHandlers</span></span>](./microsoft-edge-policies.md#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [<span data-ttu-id="ac3f1-213">PasswordManagerEnabled</span><span class="sxs-lookup"><span data-stu-id="ac3f1-213">PasswordManagerEnabled</span></span>](./microsoft-edge-policies.md#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [<span data-ttu-id="ac3f1-214">PrintHeaderFooter</span><span class="sxs-lookup"><span data-stu-id="ac3f1-214">PrintHeaderFooter</span></span>](./microsoft-edge-policies.md#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [<span data-ttu-id="ac3f1-215">SmartScreenEnabled</span><span class="sxs-lookup"><span data-stu-id="ac3f1-215">SmartScreenEnabled</span></span>](./microsoft-edge-policies.md#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [<span data-ttu-id="ac3f1-216">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="ac3f1-216">HomePageLocation</span></span>](./microsoft-edge-policies.md#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [<span data-ttu-id="ac3f1-217">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="ac3f1-217">ShowHomeButton</span></span>](./microsoft-edge-policies.md#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [<span data-ttu-id="ac3f1-218">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ac3f1-218">FavoritesBarEnabled</span></span>](./microsoft-edge-policies.md#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### <a name="oma-uri-examples"></a><span data-ttu-id="ac3f1-219">Ejemplos de OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-219">OMA-URI examples</span></span>

<span data-ttu-id="ac3f1-220">Ejemplos de OMA-URI con su ruta URI, tipo y un valor de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-220">OMA-URI examples with their URI path, type, and an example value.</span></span>

#### <a name="boolean-data-type-examples"></a><span data-ttu-id="ac3f1-221">Ejemplos de tipo de datos booleano</span><span class="sxs-lookup"><span data-stu-id="ac3f1-221">Boolean data type examples</span></span>

*<span data-ttu-id="ac3f1-222">[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton):</span><span class="sxs-lookup"><span data-stu-id="ac3f1-222">[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton):</span></span>*

| <span data-ttu-id="ac3f1-223">Campo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-223">Field</span></span>   | <span data-ttu-id="ac3f1-224">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-224">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3f1-225">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac3f1-225">Name</span></span>    | <span data-ttu-id="ac3f1-226">Microsoft Edge: ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="ac3f1-226">Microsoft Edge: ShowHomeButton</span></span>                                                       |
| <span data-ttu-id="ac3f1-227">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-227">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| <span data-ttu-id="ac3f1-228">tipo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-228">type</span></span>    | <span data-ttu-id="ac3f1-229">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-229">String</span></span>                                                                               |
| <span data-ttu-id="ac3f1-230">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-230">Value</span></span>   | `<enabled/>`                                                                          |

*<span data-ttu-id="ac3f1-231">[DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled):</span><span class="sxs-lookup"><span data-stu-id="ac3f1-231">[DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled):</span></span>*

| <span data-ttu-id="ac3f1-232">Campo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-232">Field</span></span>   | <span data-ttu-id="ac3f1-233">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-233">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3f1-234">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac3f1-234">Name</span></span>    | <span data-ttu-id="ac3f1-235">Microsoft Edge: DefaultSearchProviderEnabled</span><span class="sxs-lookup"><span data-stu-id="ac3f1-235">Microsoft Edge: DefaultSearchProviderEnabled</span></span>                                         |
| <span data-ttu-id="ac3f1-236">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-236">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| <span data-ttu-id="ac3f1-237">tipo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-237">type</span></span>    | <span data-ttu-id="ac3f1-238">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-238">String</span></span>                                                                               |
| <span data-ttu-id="ac3f1-239">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-239">Value</span></span>   | `<disable/>`                                                                          |

### <a name="integer-data-type-examples"></a><span data-ttu-id="ac3f1-240">Ejemplos de tipo de datos enteros</span><span class="sxs-lookup"><span data-stu-id="ac3f1-240">Integer data type examples</span></span>

*<span data-ttu-id="ac3f1-241">[AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun):</span><span class="sxs-lookup"><span data-stu-id="ac3f1-241">[AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun):</span></span>*

| <span data-ttu-id="ac3f1-242">Campo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-242">Field</span></span>   | <span data-ttu-id="ac3f1-243">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-243">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3f1-244">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac3f1-244">Name</span></span>    | <span data-ttu-id="ac3f1-245">Microsoft Edge: AutoImportAtFirstRun</span><span class="sxs-lookup"><span data-stu-id="ac3f1-245">Microsoft Edge: AutoImportAtFirstRun</span></span>                                                 |
| <span data-ttu-id="ac3f1-246">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-246">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| <span data-ttu-id="ac3f1-247">tipo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-247">type</span></span>    | <span data-ttu-id="ac3f1-248">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-248">String</span></span>                                                                               |
| <span data-ttu-id="ac3f1-249">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-249">Value</span></span>   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*<span data-ttu-id="ac3f1-250">[DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting):</span><span class="sxs-lookup"><span data-stu-id="ac3f1-250">[DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting):</span></span>*

| <span data-ttu-id="ac3f1-251">Campo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-251">Field</span></span>   | <span data-ttu-id="ac3f1-252">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-252">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3f1-253">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac3f1-253">Name</span></span>    | <span data-ttu-id="ac3f1-254">Microsoft Edge: DefaultImagesSetting</span><span class="sxs-lookup"><span data-stu-id="ac3f1-254">Microsoft Edge: DefaultImagesSetting</span></span>                                                 |
| <span data-ttu-id="ac3f1-255">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-255">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| <span data-ttu-id="ac3f1-256">tipo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-256">type</span></span>    | <span data-ttu-id="ac3f1-257">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-257">String</span></span>                                                                               |
| <span data-ttu-id="ac3f1-258">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-258">Value</span></span>   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*<span data-ttu-id="ac3f1-259">[DiskCacheSize](./microsoft-edge-policies.md#diskcachesize):</span><span class="sxs-lookup"><span data-stu-id="ac3f1-259">[DiskCacheSize](./microsoft-edge-policies.md#diskcachesize):</span></span>*

| <span data-ttu-id="ac3f1-260">Campo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-260">Field</span></span>   | <span data-ttu-id="ac3f1-261">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-261">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3f1-262">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac3f1-262">Name</span></span>    | <span data-ttu-id="ac3f1-263">Microsoft Edge: DiskCacheSize</span><span class="sxs-lookup"><span data-stu-id="ac3f1-263">Microsoft Edge: DiskCacheSize</span></span>                                                        |
| <span data-ttu-id="ac3f1-264">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-264">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| <span data-ttu-id="ac3f1-265">tipo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-265">type</span></span>    | <span data-ttu-id="ac3f1-266">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-266">String</span></span>                                                                               |
| <span data-ttu-id="ac3f1-267">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-267">Value</span></span>   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### <a name="list-of-strings-data-type-examples"></a><span data-ttu-id="ac3f1-268">Lista de ejemplos de tipos de datos de cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-268">List of strings data type examples</span></span>
<!--
*[NotificationsAllowedForUrls](./microsoft-edge-policies.md#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                           |
-->
*<span data-ttu-id="ac3f1-269">[RestoreOnStartupURLS](./microsoft-edge-policies.md#restoreonstartupurls):</span><span class="sxs-lookup"><span data-stu-id="ac3f1-269">[RestoreOnStartupURLS](./microsoft-edge-policies.md#restoreonstartupurls):</span></span>*

| <span data-ttu-id="ac3f1-270">Campo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-270">Field</span></span>   | <span data-ttu-id="ac3f1-271">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-271">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3f1-272">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac3f1-272">Name</span></span>    | <span data-ttu-id="ac3f1-273">Microsoft Edge: RestoreOnStartupURLS</span><span class="sxs-lookup"><span data-stu-id="ac3f1-273">Microsoft Edge: RestoreOnStartupURLS</span></span>                                                 |
| <span data-ttu-id="ac3f1-274">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-274">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| <span data-ttu-id="ac3f1-275">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-275">Type</span></span>    | <span data-ttu-id="ac3f1-276">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-276">String</span></span>                                                                               |
| <span data-ttu-id="ac3f1-277">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-277">Value</span></span>   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br><span data-ttu-id="ac3f1-278">Para elementos de lista múltiples:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-278">For multiple list items:</span></span> `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*<span data-ttu-id="ac3f1-279">[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist):</span><span class="sxs-lookup"><span data-stu-id="ac3f1-279">[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist):</span></span>*

| <span data-ttu-id="ac3f1-280">Campo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-280">Field</span></span>   | <span data-ttu-id="ac3f1-281">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-281">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3f1-282">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac3f1-282">Name</span></span>    | <span data-ttu-id="ac3f1-283">Microsoft Edge: ExtensionInstallForcelist</span><span class="sxs-lookup"><span data-stu-id="ac3f1-283">Microsoft Edge: ExtensionInstallForcelist</span></span>                                            |
| <span data-ttu-id="ac3f1-284">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-284">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| <span data-ttu-id="ac3f1-285">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-285">Type</span></span>    | <span data-ttu-id="ac3f1-286">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-286">String</span></span>                                                                               |
| <span data-ttu-id="ac3f1-287">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-287">Value</span></span>   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### <a name="dictionary-and-string-data-type-example"></a><span data-ttu-id="ac3f1-288">Ejemplo de diccionario y tipo de datos de cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-288">Dictionary and String data type example</span></span>

*<span data-ttu-id="ac3f1-289">[ProxyMode](./microsoft-edge-policies.md#proxymode):</span><span class="sxs-lookup"><span data-stu-id="ac3f1-289">[ProxyMode](./microsoft-edge-policies.md#proxymode):</span></span>*

| <span data-ttu-id="ac3f1-290">Campo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-290">Field</span></span>   | <span data-ttu-id="ac3f1-291">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-291">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3f1-292">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac3f1-292">Name</span></span>    | <span data-ttu-id="ac3f1-293">Microsoft Edge: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="ac3f1-293">Microsoft Edge: ProxyMode</span></span>                                                            |
| <span data-ttu-id="ac3f1-294">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="ac3f1-294">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| <span data-ttu-id="ac3f1-295">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-295">Type</span></span>    | <span data-ttu-id="ac3f1-296">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac3f1-296">String</span></span>                                                                               |
| <span data-ttu-id="ac3f1-297">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f1-297">Value</span></span>   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## <a name="configure-microsoft-edge-in-intune-using-admx-ingestion"></a><span data-ttu-id="ac3f1-298">Configurar Microsoft Edge en intune usando la ingesta ADMX</span><span class="sxs-lookup"><span data-stu-id="ac3f1-298">Configure Microsoft Edge in Intune using ADMX ingestion</span></span>

<span data-ttu-id="ac3f1-299">La manera recomendada de configurar Microsoft Edge con Microsoft Intune es usar el perfil de plantillas administrativas, tal y como se describe en [Configurar las opciones de la directiva de Microsoft Edge con Microsoft Intune](./configure-edge-with-intune.md)c</span><span class="sxs-lookup"><span data-stu-id="ac3f1-299">The recommended way to configure Microsoft Edge with Microsoft Intune is to use the Administrative Templates profile as described in [Configure Microsoft Edge policy settings with Microsoft Intune](./configure-edge-with-intune.md).</span></span> <span data-ttu-id="ac3f1-300">Si deseas evaluar una directiva que actualmente no está disponible en las plantillas administrativas de Microsoft Edge en intune, puedes configurar Microsoft Edge usando una [configuración personalizada para dispositivos con Windows 10 en intune](/intune/configuration/custom-settings-windows-10).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-300">If you want to evaluate a policy that is currently not available in the Microsoft Edge Administrative Templates in Intune you can configure Microsoft Edge using  [custom settings for Windows 10 devices in Intune](/intune/configuration/custom-settings-windows-10).</span></span>

<span data-ttu-id="ac3f1-301">Esta sección describe cómo:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-301">This section describes how to:</span></span>

1. [<span data-ttu-id="ac3f1-302">Ingerir el archivo ADMX de Microsoft Edge en Intune</span><span class="sxs-lookup"><span data-stu-id="ac3f1-302">Ingest the Microsoft Edge ADMX file into Intune</span></span>](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [<span data-ttu-id="ac3f1-303">Establecer una Directiva con OMA-URI personalizado en Intune</span><span class="sxs-lookup"><span data-stu-id="ac3f1-303">Set a policy using custom OMA-URI in Intune</span></span>](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> <span data-ttu-id="ac3f1-304">Como procedimiento recomendado, no uses un perfil OMA-URI personalizado y un perfil de plantillas de administración para configurar la misma opción de Microsoft Edge en Intune.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-304">As a best practice, don’t use a custom OMA-URI profile and an Administration templates profile to configure the same Microsoft Edge setting in Intune.</span></span> <span data-ttu-id="ac3f1-305">Si implementas la misma directiva con un OMA-URI personalizado y un perfil de plantilla administrativa, pero con valores diferentes, los usuarios obtendrán resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-305">If you deploy the same policy using both a custom OMA-URI  and an Administrative template profile, but with different values, users will get unpredictable results.</span></span> <span data-ttu-id="ac3f1-306">Te recomendamos encarecidamente que quites tu perfil de OMA-URI antes de usar un perfil de plantillas de administración.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-306">We strongly recommend removing your OMA-URI profile before using an Administration templates profile.</span></span>

### <a name="ingest-the-microsoft-edge-admx-file-into-intune"></a><span data-ttu-id="ac3f1-307">Ingerir el archivo ADMX de Microsoft Edge en Intune</span><span class="sxs-lookup"><span data-stu-id="ac3f1-307">Ingest the Microsoft Edge ADMX file into Intune</span></span>

<span data-ttu-id="ac3f1-308">En esta sección se describe cómo ingerir la plantilla administrativa de Microsoft Edge (archivo **msedge.admx**) en Intune.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-308">This section describes how to ingest the Microsoft Edge administrative template (**msedge.admx** file) into Intune.</span></span>

> [!WARNING]
> <span data-ttu-id="ac3f1-309">No modifiques el archivo ADMX antes de ingerir el archivo.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-309">Don't modify the ADMX file before ingesting the file.</span></span>

<span data-ttu-id="ac3f1-310">Para ingerir el archivo ADMX, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-310">To ingest the ADMX file, follow these steps:</span></span>

1. <span data-ttu-id="ac3f1-311">Descarga el archivo de plantillas de directiva de Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) desde la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) y extrae el contenido.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-311">Download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span> <span data-ttu-id="ac3f1-312">El archivo que quieres ingerir es **msedge.admx**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-312">The file that you want to ingest is **msedge.admx**.</span></span>
2. <span data-ttu-id="ac3f1-313">Inicia sesión en [Microsoft Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-313">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
3. <span data-ttu-id="ac3f1-314">Selecciona **Intune** desde _Todos los servicios_, o busca Intune en el cuadro de búsqueda del portal.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-314">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
4. <span data-ttu-id="ac3f1-315">En _Microsoft Intune - Resumen_, selecciona **Configuración de dispositivos** | **Perfiles**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-315">From _Microsoft Intune - Overview_, select **Device configuration** | **Profiles**.</span></span>
5. <span data-ttu-id="ac3f1-316">En la barra de comandos superior, selecciona **+ Crear perfil**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-316">On the top command bar, select **+ Create profile**.</span></span>

   ![Crear un perfil de dispositivo](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. <span data-ttu-id="ac3f1-318">Facilita la siguiente información de perfil:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-318">Provide the following profile information:</span></span>

   - <span data-ttu-id="ac3f1-319">**Nombre**: introduce un nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-319">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="ac3f1-320">Para este ejemplo, "Configuración ingerida de ADMX de Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="ac3f1-320">For this example, "Microsoft Edge ADMX ingested configuration".</span></span>
   - <span data-ttu-id="ac3f1-321">**Descripción**: introduce una descripción opcional del perfil.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-321">**Description**: Enter an optional description for the profile.</span></span>
   - <span data-ttu-id="ac3f1-322">**Plataforma**: selecciona "Windows 10 y posteriores"</span><span class="sxs-lookup"><span data-stu-id="ac3f1-322">**Platform**: Select "Windows 10 and later"</span></span>
   - <span data-ttu-id="ac3f1-323">**Tipo de perfil**: Selecciona "Personalizado"</span><span class="sxs-lookup"><span data-stu-id="ac3f1-323">**Profile type**: Select "Custom"</span></span>

7. <span data-ttu-id="ac3f1-324">En **Configuración OMA-URI personalizada**, haz clic en **Agregar** para agregar una ingesta de ADMX.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-324">On **Custom OMA-URI Settings**, click **Add** to add an ADMX ingestion.</span></span>

   ![Agregar ingesta para OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. <span data-ttu-id="ac3f1-326">En **Agregar fila**, facilita la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-326">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="ac3f1-327">**Nombre**: introduce un nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-327">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="ac3f1-328">Para este ejemplo, usa "Ingesta de ADMX de Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="ac3f1-328">For this example, use "Microsoft Edge ADMX ingestion".</span></span>
   - <span data-ttu-id="ac3f1-329">**Descripción**: introduce una descripción opcional de la opción.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-329">**Description**: Enter an optional description for the setting.</span></span>
   - <span data-ttu-id="ac3f1-330">**OMA-URI**: introduce "*./Device/Vendor/msft/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"</span><span class="sxs-lookup"><span data-stu-id="ac3f1-330">**OMA-URI**: Enter "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"</span></span>
   - <span data-ttu-id="ac3f1-331">**Tipo de datos**: selecciona "Cadena"</span><span class="sxs-lookup"><span data-stu-id="ac3f1-331">**Data type**: Select "String"</span></span>
   - <span data-ttu-id="ac3f1-332">**Valor**: este área de entrada aparece después de seleccionar el **Tipo de datos**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-332">**Value**: This input area appears after you select the **Data type**.</span></span> <span data-ttu-id="ac3f1-333">Abre el archivo msedge.admx desde el archivo de plantillas de directiva de Microsoft Edge que extrajiste en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-333">Open the msedge.admx file from the Microsoft Edge policy templates file you extracted in step 1.</span></span> <span data-ttu-id="ac3f1-334">Copia **TODO el texto** desde el archivo msedge.admx y pégalo en el área de texto **Valor** que se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-334">Copy **ALL the text** from the msedge.admx file and paste it in the **Value** text area shown in the following screenshot.</span></span>

        ![Agregar una ingesta de ADMX](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - <span data-ttu-id="ac3f1-336">Haz clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-336">Click **OK**.</span></span>

9. <span data-ttu-id="ac3f1-337">En **Configuración OMA-URI personalizada**, haz click en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-337">On **Custom OMA-URI Settings**, click **OK**.</span></span>
10. <span data-ttu-id="ac3f1-338">En **Crear perfil**, haz clic en **Crear**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-338">On **Create profile**, click **Create**.</span></span> <span data-ttu-id="ac3f1-339">La siguiente captura de pantalla muestra información sobre el perfil recién creado.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-339">The next screenshot shows information about the newly created profile.</span></span>

    ![<span data-ttu-id="ac3f1-340">Información de nuevo perfil de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ac3f1-340">New device profile information</span></span> ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### <a name="set-a-policy-using-custom-oma-uri-in-intune"></a><span data-ttu-id="ac3f1-341">Establecer una Directiva con OMA-URI personalizado en Intune</span><span class="sxs-lookup"><span data-stu-id="ac3f1-341">Set a policy using custom OMA-URI in Intune</span></span>

> [!NOTE]
> <span data-ttu-id="ac3f1-342">Antes de seguir los pasos de esta sección, debes completar los pasos descritos en [Ingerir el archivo ADMX de Microsoft Edge en Intune](#ingest-the-microsoft-edge-admx-file-into-intune).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-342">Before using the steps in this section you must complete the steps described in [Ingest the Microsoft Edge ADMX file into Intune](#ingest-the-microsoft-edge-admx-file-into-intune).</span></span>

1. <span data-ttu-id="ac3f1-343">Inicia sesión en [Microsoft Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-343">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
2. <span data-ttu-id="ac3f1-344">Selecciona **Intune** desde _Todos los servicios_, o busca Intune en el cuadro de búsqueda del portal.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-344">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
3. <span data-ttu-id="ac3f1-345">Ve a **Intune**>**Configuración de dispositivo**>**Perfiles**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-345">Go to **Intune**>**Device configuration**>**Profiles**.</span></span>
4. <span data-ttu-id="ac3f1-346">Selecciona el perfil "Configuración ingerida de ADMX de Microsoft Edge" o el nombre que usaste para el perfil.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-346">Select the "Microsoft Edge ADMX ingested configuration" profile or the name you used for the profile.</span></span>
5. <span data-ttu-id="ac3f1-347">Para agregar la configuración de directiva de Microsoft Edge, debes abrir **Configuración OMA-URI personalizada**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-347">To add Microsoft Edge policy settings, you have to open **Custom OMA-URI Settings**.</span></span> <span data-ttu-id="ac3f1-348">En **Administrar**, haz clic en **Propiedades** y luego haz clic en **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-348">Under **Manage**, click **Properties**, and then click **Settings**.</span></span>

    ![Configurar opciones de perfil](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. <span data-ttu-id="ac3f1-350">En **Configuración OMA-URI personalizada**, haz clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-350">On **Custom OMA-URI Settings**, click **Add**.</span></span>

    ![Agregar fila a configuración OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. <span data-ttu-id="ac3f1-352">En **Agregar fila**, facilita la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-352">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="ac3f1-353">**Nombre**: introduce un nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-353">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="ac3f1-354">Es recomendable usar el nombre de la directiva que quieres configurar.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-354">We suggest using the policy name you want to configure.</span></span> <span data-ttu-id="ac3f1-355">Para este ejemplo, usa "ShowHomeButton".</span><span class="sxs-lookup"><span data-stu-id="ac3f1-355">For this example, use "ShowHomeButton".</span></span>
   - <span data-ttu-id="ac3f1-356">**Descripción** (opcional): introduce una descripción de la opción.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-356">**Description** (Optional): Enter a description for the setting.</span></span>
   - <span data-ttu-id="ac3f1-357">**OMA-URI**: introduce el OMA-URI para la directiva.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-357">**OMA-URI**: Enter the OMA-URI for the policy.</span></span> <span data-ttu-id="ac3f1-358">Usando la directiva para "ShowHomeButton" como ejemplo, emplea esta cadena: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"</span><span class="sxs-lookup"><span data-stu-id="ac3f1-358">Using the for "ShowHomeButton" policy as an example, use this string: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"</span></span>
   - <span data-ttu-id="ac3f1-359">**Tipo de datos**: selecciona el tipo de datos de configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-359">**Data type**: Select the policy settings data type.</span></span> <span data-ttu-id="ac3f1-360">Para la directiva "ShowHomeButton", usa "Cadena"</span><span class="sxs-lookup"><span data-stu-id="ac3f1-360">For the "ShowHomeButton" policy, use "String"</span></span>
   - <span data-ttu-id="ac3f1-361">**Valor**: especifica la opción que quieras configurar para la directiva.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-361">**Value**: Enter the setting that you want to configure for the policy.</span></span> <span data-ttu-id="ac3f1-362">Para el ejemplo "ShowHomeButton", introduce "\<enabled/>".</span><span class="sxs-lookup"><span data-stu-id="ac3f1-362">For "ShowHomeButton" example, enter "\<enabled/>".</span></span> <span data-ttu-id="ac3f1-363">La siguiente captura de pantalla muestra las opciones para configurar una directiva.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-363">The following screenshot shows the settings for configuring a policy.</span></span>

        ![Agregar fila, configuración OMA-URI personalizada](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - <span data-ttu-id="ac3f1-365">Haz clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-365">Click **OK**.</span></span>

8. <span data-ttu-id="ac3f1-366">En **Configuración OMA-URI personalizada**, haz click en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-366">On **Custom OMA-URI Settings**, click **OK**.</span></span>
9. <span data-ttu-id="ac3f1-367">En el perfil "**Configuración ingerida de ADMX de Microsoft Edge - Propiedades**" (o el nombre que hayas usado), haz clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-367">On the "**Microsoft Edge ADMX ingested configuration - Properties**" profile (or the name you used), click **Save**.</span></span>

<span data-ttu-id="ac3f1-368">Después de crear el perfil y establecer las propiedades, tendrás que [asignar el perfil en Microsoft Intune](/intune/configuration/device-profile-assign).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-368">After the profile is created and the properties set, you have to [assign the profile in Microsoft Intune](/intune/configuration/device-profile-assign).</span></span>

#### <a name="confirm-that-the-policy-was-set"></a><span data-ttu-id="ac3f1-369">Confirmar que se ha establecido la directiva</span><span class="sxs-lookup"><span data-stu-id="ac3f1-369">Confirm that the policy was set</span></span>

<span data-ttu-id="ac3f1-370">Usa los siguientes pasos para confirmar que la directiva de Microsoft Edge usa el perfil que has creado.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-370">Use the following steps to confirm that the Microsoft Edge policy is using the profile you created.</span></span> <span data-ttu-id="ac3f1-371">(Deja tiempo a Microsoft Intune para propagar la directiva a un dispositivo que hayas asignado en el ejemplo de perfil "Configuración ingerida de ADMX de Microsoft Edge").</span><span class="sxs-lookup"><span data-stu-id="ac3f1-371">(Give Microsoft Intune time to propagate the policy to a device you assigned in the "Microsoft Edge ADMX ingested configuration" profile example.)</span></span>

1. <span data-ttu-id="ac3f1-372">Abre Microsoft Edge y ve a *edge://policy*.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-372">Open Microsoft Edge and go to *edge://policy*.</span></span>
2. <span data-ttu-id="ac3f1-373">En la página **Directivas**, mira a ver si se enumera la directiva que estableciste en el perfil.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-373">On the **Policies** page, see if the policy you set in the profile is listed.</span></span>
3. <span data-ttu-id="ac3f1-374">Si no aparece la directiva, consulta [Diagnosticar errores de MDM en Windows 10](/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) o [Solucionar problemas de configuración de directiva](#troubleshoot-a-policy-setting).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-374">If your policy isn't shown, see [Diagnose MDM failures in Windows 10](/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) or [Troubleshoot a policy setting](#troubleshoot-a-policy-setting).</span></span>

#### <a name="troubleshoot-a-policy-setting"></a><span data-ttu-id="ac3f1-375">Solucionar problemas de configuración de directiva</span><span class="sxs-lookup"><span data-stu-id="ac3f1-375">Troubleshoot a policy setting</span></span>

<span data-ttu-id="ac3f1-376">Si una directiva de Microsoft Edge no surte efecto, sigue los pasos que se indican a continuación:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-376">If a Microsoft Edge policy isn’t taking effect, try the following steps:</span></span>

<span data-ttu-id="ac3f1-377">Abre la página *edge://policy* en el dispositivo de destino (un dispositivo al que asignaste el perfil en Microsoft Intune) y busca la directiva.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-377">Open the *edge://policy* page on the target device (a device you assigned the profile to in Microsoft Intune) and search for the policy.</span></span> <span data-ttu-id="ac3f1-378">Si la directiva no está en la página *edge://Policy*, intenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ac3f1-378">If the policy isn’t on the *edge://policy* page, try the following:</span></span>

- <span data-ttu-id="ac3f1-379">Comprueba que la directiva esté en el Registro y que sea correcta.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-379">Check that the policy is in the registry and is correct.</span></span> <span data-ttu-id="ac3f1-380">En el dispositivo de destino, abre el Editor del Registro de Windows 10 (**tecla Windows+ r**, introduce “*regedit*” y ,a continuación, presiona **Entrar**). Comprueba que la directiva esté definida correctamente en la ruta *\Software\Policies\ Microsoft\Edge*.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-380">On the target device open the Windows 10 Registry Editor (**Windows key + r**, enter “*regedit*” and then press **Enter**.) Check that the policy is correctly defined in the *\Software\Policies\ Microsoft\Edge* path.</span></span> <span data-ttu-id="ac3f1-381">Si no aparece la directiva en la ruta prevista, la directiva no se ha insertado correctamente en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-381">If you don’t find the policy in the expected path, then the policy wasn’t pushed to the device correctly.</span></span>
- <span data-ttu-id="ac3f1-382">Comprueba que la ruta OMA-URI sea correcta y que el valor sea una cadena XML válida.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-382">Check that the OMA-URI path is correct, and the value is a valid XML string.</span></span> <span data-ttu-id="ac3f1-383">Si alguno de estos valores es incorrecto, la directiva no se insertará en el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ac3f1-383">If either of these are incorrect the policy won’t be pushed to the target device.</span></span>

<span data-ttu-id="ac3f1-384">Para obtener más sugerencias sobre la solución de problemas, consulta [Configurar Microsoft Intune](/intune/fundamentals/setup-steps) y [Sincronizar dispositivos](/intune/remote-actions/device-sync).</span><span class="sxs-lookup"><span data-stu-id="ac3f1-384">For more trouble shooting tips, see [Set up Microsoft Intune](/intune/fundamentals/setup-steps) and [Sync devices](/intune/remote-actions/device-sync).</span></span>

## <a name="see-also"></a><span data-ttu-id="ac3f1-385">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ac3f1-385">See also</span></span>

- [<span data-ttu-id="ac3f1-386">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ac3f1-386">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ac3f1-387">Configurar la directiva de Microsoft Edge con Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="ac3f1-387">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>](configure-edge-with-intune.md)
- [<span data-ttu-id="ac3f1-388">Administración de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="ac3f1-388">Mobile device management</span></span>](/windows/client-management/mdm/)
- [<span data-ttu-id="ac3f1-389">Usar la configuración personalizada para dispositivos con Windows 10 en Intune</span><span class="sxs-lookup"><span data-stu-id="ac3f1-389">Use custom settings for Windows 10 devices in Intune</span></span>](/intune/configuration/custom-settings-windows-10)
- [<span data-ttu-id="ac3f1-390">Configuración de directiva de aplicaciones de Win32 y Puente de dispositivo de escritorio</span><span class="sxs-lookup"><span data-stu-id="ac3f1-390">Win32 and Desktop Bridge app policy configuration</span></span>](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [<span data-ttu-id="ac3f1-391">Descripción de las directivas respaldadas por ADMX</span><span class="sxs-lookup"><span data-stu-id="ac3f1-391">Understanding ADMX-backed policies</span></span>](/windows/client-management/mdm/understanding-admx-backed-policies)