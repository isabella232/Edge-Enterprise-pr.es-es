---
title: Documentación de directiva de WebView2 de Microsoft Edge
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 10/16/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentación de Windows y Mac para todas las directivas admitidas por Explorador Microsoft Edge
ms.openlocfilehash: 4298b25f7f158bc54f798442b4426494f046fa68
ms.sourcegitcommit: 7d160257010f75b86b89c8802d0dd27f1f8761ef
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134449"
---
# <span data-ttu-id="f20f8-103">Microsoft Edge WebView2: directivas</span><span class="sxs-lookup"><span data-stu-id="f20f8-103">Microsoft Edge WebView2 - Policies</span></span>

<span data-ttu-id="f20f8-104">La versión más reciente de Microsoft Edge WebView2 incluye las siguientes directivas.</span><span class="sxs-lookup"><span data-stu-id="f20f8-104">The latest version of Microsoft Edge WebView2 includes the following policies.</span></span> <span data-ttu-id="f20f8-105">Puede usar estas directivas para configurar cómo se ejecuta Microsoft Edge WebView2 en su organización.</span><span class="sxs-lookup"><span data-stu-id="f20f8-105">You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.</span></span>

<span data-ttu-id="f20f8-106">Para obtener información sobre un conjunto adicional de directivas usadas para controlar cómo y cuándo se actualiza Microsoft Edge WebView2, vea la [referencia de directiva de actualización de Microsoft Edge](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="f20f8-106">For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).</span></span>


> [!NOTE]
> <span data-ttu-id="f20f8-107">Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f20f8-107">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="f20f8-108">Directivas disponibles</span><span class="sxs-lookup"><span data-stu-id="f20f8-108">Available policies</span></span>

<span data-ttu-id="f20f8-109">En estas tablas se muestran todas las directivas de grupo disponibles en esta versión de Microsoft Edge WebView2.</span><span class="sxs-lookup"><span data-stu-id="f20f8-109">These tables list all of the group policies available in this release of Microsoft Edge WebView2.</span></span> <span data-ttu-id="f20f8-110">Usa los vínculos de la tabla para obtener más detalles sobre directivas específicas.</span><span class="sxs-lookup"><span data-stu-id="f20f8-110">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="f20f8-111">Configuración de invalidación de Loader</span><span class="sxs-lookup"><span data-stu-id="f20f8-111">Loader Override Settings</span></span>](#loader-override-settings)|

### [*<span data-ttu-id="f20f8-112">Configuración de invalidación de Loader</span><span class="sxs-lookup"><span data-stu-id="f20f8-112">Loader Override Settings</span></span>*](#loader-override-settings-policies)

|<span data-ttu-id="f20f8-113">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="f20f8-113">Policy Name</span></span>|<span data-ttu-id="f20f8-114">Título</span><span class="sxs-lookup"><span data-stu-id="f20f8-114">Caption</span></span>|
|-|-|
|[<span data-ttu-id="f20f8-115">browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="f20f8-115">browserExecutableFolder</span></span>](#browserexecutablefolder)|<span data-ttu-id="f20f8-116">Configure la ubicación de la carpeta ejecutable del explorador</span><span class="sxs-lookup"><span data-stu-id="f20f8-116">Configure the location of the browser executable folder</span></span>|
|[<span data-ttu-id="f20f8-117">releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="f20f8-117">releaseChannelPreference</span></span>](#releasechannelpreference)|<span data-ttu-id="f20f8-118">Establezca las preferencias de pedido de búsqueda de canal de publicación</span><span class="sxs-lookup"><span data-stu-id="f20f8-118">Set the release channel search order preference</span></span>|




  ## <span data-ttu-id="f20f8-119">Directivas de configuración de invalidación de Loader</span><span class="sxs-lookup"><span data-stu-id="f20f8-119">Loader Override Settings policies</span></span>

  [<span data-ttu-id="f20f8-120">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="f20f8-120">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="f20f8-121">browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="f20f8-121">browserExecutableFolder</span></span>

  #### <span data-ttu-id="f20f8-122">Configure la ubicación de la carpeta ejecutable del explorador</span><span class="sxs-lookup"><span data-stu-id="f20f8-122">Configure the location of the browser executable folder</span></span>

  
  
  #### <span data-ttu-id="f20f8-123">Versiones compatibles:</span><span class="sxs-lookup"><span data-stu-id="f20f8-123">Supported versions:</span></span>

  - <span data-ttu-id="f20f8-124">En Windows desde la versión 87 o posterior</span><span class="sxs-lookup"><span data-stu-id="f20f8-124">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="f20f8-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="f20f8-125">Description</span></span>

  <span data-ttu-id="f20f8-126">Esta directiva configura las aplicaciones de WebView2 para usar el tiempo de ejecución de WebView2 en la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="f20f8-126">This policy configures WebView2 applications to use the WebView2 Runtime in the specified path.</span></span> <span data-ttu-id="f20f8-127">La carpeta debe contener los siguientes archivos: msedgewebview2. exe, msedge. dll, etc.</span><span class="sxs-lookup"><span data-stu-id="f20f8-127">The folder should contain the following files: msedgewebview2.exe, msedge.dll, and so on.</span></span>

<span data-ttu-id="f20f8-128">Para establecer el valor de la ruta de acceso de la carpeta, especifique un par de valor y nombre de valor.</span><span class="sxs-lookup"><span data-stu-id="f20f8-128">To set the value for the folder path, provide a Value name and Value pair.</span></span> <span data-ttu-id="f20f8-129">Configure el nombre de valor en el ID. del modelo de usuario de la aplicación o en el nombre del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="f20f8-129">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="f20f8-130">Puede usar el carácter comodín "\*" como nombre de valor para aplicar a todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f20f8-130">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="f20f8-131">Características admitidas:</span><span class="sxs-lookup"><span data-stu-id="f20f8-131">Supported features:</span></span>

  - <span data-ttu-id="f20f8-132">Puede ser obligatorio: sí</span><span class="sxs-lookup"><span data-stu-id="f20f8-132">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="f20f8-133">Puede ser recomendable: no</span><span class="sxs-lookup"><span data-stu-id="f20f8-133">Can be recommended: No</span></span>
  - <span data-ttu-id="f20f8-134">Actualización de directiva dinámica: sí</span><span class="sxs-lookup"><span data-stu-id="f20f8-134">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="f20f8-135">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f20f8-135">Data Type:</span></span>

  - <span data-ttu-id="f20f8-136">Lista de cadenas</span><span class="sxs-lookup"><span data-stu-id="f20f8-136">List of strings</span></span>

  #### <span data-ttu-id="f20f8-137">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="f20f8-137">Windows information and settings</span></span>

  ##### <span data-ttu-id="f20f8-138">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="f20f8-138">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="f20f8-139">Nombre único de GP: browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="f20f8-139">GP unique name: browserExecutableFolder</span></span>
  - <span data-ttu-id="f20f8-140">Nombre GP: configure la ubicación de la carpeta ejecutable del explorador.</span><span class="sxs-lookup"><span data-stu-id="f20f8-140">GP name: Configure the location of the browser executable folder</span></span>
  - <span data-ttu-id="f20f8-141">Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge WebView2/Loader cambiar configuración</span><span class="sxs-lookup"><span data-stu-id="f20f8-141">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="f20f8-142">Ruta de acceso de GP (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="f20f8-142">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="f20f8-143">Nombre de archivo ADMX de GP: MSEdgeWebView2. ADMX</span><span class="sxs-lookup"><span data-stu-id="f20f8-143">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <span data-ttu-id="f20f8-144">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="f20f8-144">Windows Registry Settings</span></span>

  - <span data-ttu-id="f20f8-145">Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="f20f8-145">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder</span></span>
  - <span data-ttu-id="f20f8-146">Ruta de acceso (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="f20f8-146">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="f20f8-147">Nombre del valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f20f8-147">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="f20f8-148">Tipo de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f20f8-148">Value Type: list of REG_SZ</span></span>

  ##### <span data-ttu-id="f20f8-149">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f20f8-149">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [<span data-ttu-id="f20f8-150">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="f20f8-150">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="f20f8-151">releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="f20f8-151">releaseChannelPreference</span></span>

  #### <span data-ttu-id="f20f8-152">Establezca las preferencias de pedido de búsqueda de canal de publicación</span><span class="sxs-lookup"><span data-stu-id="f20f8-152">Set the release channel search order preference</span></span>

  
  
  #### <span data-ttu-id="f20f8-153">Versiones compatibles:</span><span class="sxs-lookup"><span data-stu-id="f20f8-153">Supported versions:</span></span>

  - <span data-ttu-id="f20f8-154">En Windows desde la versión 87 o posterior</span><span class="sxs-lookup"><span data-stu-id="f20f8-154">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="f20f8-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="f20f8-155">Description</span></span>

  <span data-ttu-id="f20f8-156">El orden de búsqueda por canal predeterminado es WebView2 Runtime, Beta, Dev y Canarias.</span><span class="sxs-lookup"><span data-stu-id="f20f8-156">The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.</span></span>

<span data-ttu-id="f20f8-157">Para invertir el orden de búsqueda predeterminado, establezca esta directiva en 1.</span><span class="sxs-lookup"><span data-stu-id="f20f8-157">To reverse the default search order, set this policy to 1.</span></span>

<span data-ttu-id="f20f8-158">Para establecer el valor de las preferencias de canal de liberación, especifique un nombre de valor y un par de valores.</span><span class="sxs-lookup"><span data-stu-id="f20f8-158">To set the value for the release channel preference, provide a Value name and Value pair.</span></span> <span data-ttu-id="f20f8-159">Configure el nombre de valor en el ID. del modelo de usuario de la aplicación o en el nombre del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="f20f8-159">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="f20f8-160">Puede usar el carácter comodín "\*" como nombre de valor para aplicar a todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f20f8-160">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="f20f8-161">Características admitidas:</span><span class="sxs-lookup"><span data-stu-id="f20f8-161">Supported features:</span></span>

  - <span data-ttu-id="f20f8-162">Puede ser obligatorio: sí</span><span class="sxs-lookup"><span data-stu-id="f20f8-162">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="f20f8-163">Puede ser recomendable: no</span><span class="sxs-lookup"><span data-stu-id="f20f8-163">Can be recommended: No</span></span>
  - <span data-ttu-id="f20f8-164">Actualización de directiva dinámica: sí</span><span class="sxs-lookup"><span data-stu-id="f20f8-164">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="f20f8-165">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f20f8-165">Data Type:</span></span>

  - <span data-ttu-id="f20f8-166">Lista de cadenas</span><span class="sxs-lookup"><span data-stu-id="f20f8-166">List of strings</span></span>

  #### <span data-ttu-id="f20f8-167">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="f20f8-167">Windows information and settings</span></span>

  ##### <span data-ttu-id="f20f8-168">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="f20f8-168">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="f20f8-169">Nombre único de GP: releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="f20f8-169">GP unique name: releaseChannelPreference</span></span>
  - <span data-ttu-id="f20f8-170">Nombre GP: establecer el canal de lanzamiento de preferencias de pedido de búsqueda</span><span class="sxs-lookup"><span data-stu-id="f20f8-170">GP name: Set the release channel search order preference</span></span>
  - <span data-ttu-id="f20f8-171">Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge WebView2/Loader cambiar configuración</span><span class="sxs-lookup"><span data-stu-id="f20f8-171">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="f20f8-172">Ruta de acceso de GP (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="f20f8-172">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="f20f8-173">Nombre de archivo ADMX de GP: MSEdgeWebView2. ADMX</span><span class="sxs-lookup"><span data-stu-id="f20f8-173">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <span data-ttu-id="f20f8-174">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="f20f8-174">Windows Registry Settings</span></span>

  - <span data-ttu-id="f20f8-175">Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="f20f8-175">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference</span></span>
  - <span data-ttu-id="f20f8-176">Ruta de acceso (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="f20f8-176">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="f20f8-177">Nombre del valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f20f8-177">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="f20f8-178">Tipo de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f20f8-178">Value Type: list of REG_SZ</span></span>

  ##### <span data-ttu-id="f20f8-179">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f20f8-179">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference = "Name: *, Value: 1"

```

  

  [<span data-ttu-id="f20f8-180">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="f20f8-180">Back to top</span></span>](#microsoft-edge-webview2---policies)


## <span data-ttu-id="f20f8-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f20f8-181">See also</span></span>

- [<span data-ttu-id="f20f8-182">Configuración de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f20f8-182">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="f20f8-183">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f20f8-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f20f8-184">Blog de líneas de base de seguridad de Microsoft</span><span class="sxs-lookup"><span data-stu-id="f20f8-184">Microsoft Security Baselines Blog</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)