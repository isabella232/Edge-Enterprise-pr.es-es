---
title: Documentación de directiva de explorador Microsoft Edge
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 10/08/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentación de Windows y Mac para todas las directivas admitidas por Explorador Microsoft Edge
ms.openlocfilehash: 56abadf907dfffec733af2456cc20db36510880b
ms.sourcegitcommit: 4e6188ade942ca6fd599a4ce1c8e0d90d3d03399
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2020
ms.locfileid: "11105773"
---
# <span data-ttu-id="ecf29-103">Microsoft Edge WebView2: directivas</span><span class="sxs-lookup"><span data-stu-id="ecf29-103">Microsoft Edge WebView2 - Policies</span></span>

<span data-ttu-id="ecf29-104">La versión más reciente de Microsoft Edge WebView2 incluye las siguientes directivas.</span><span class="sxs-lookup"><span data-stu-id="ecf29-104">The latest version of Microsoft Edge WebView2 includes the following policies.</span></span> <span data-ttu-id="ecf29-105">Puede usar estas directivas para configurar cómo se ejecuta Microsoft Edge WebView2 en su organización.</span><span class="sxs-lookup"><span data-stu-id="ecf29-105">You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.</span></span>

<span data-ttu-id="ecf29-106">Para obtener información sobre un conjunto adicional de directivas usadas para controlar cómo y cuándo se actualiza Microsoft Edge WebView2, vea la [referencia de directiva de actualización de Microsoft Edge](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ecf29-106">For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ecf29-107">Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ecf29-107">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="ecf29-108">Directivas disponibles</span><span class="sxs-lookup"><span data-stu-id="ecf29-108">Available policies</span></span>
<span data-ttu-id="ecf29-109">En estas tablas se muestran todas las directivas de grupo disponibles en esta versión de Microsoft Edge WebView2.</span><span class="sxs-lookup"><span data-stu-id="ecf29-109">These tables list all of the group policies available in this release of Microsoft Edge WebView2.</span></span> <span data-ttu-id="ecf29-110">Usa los vínculos de la tabla para obtener más detalles sobre directivas específicas.</span><span class="sxs-lookup"><span data-stu-id="ecf29-110">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="ecf29-111">Configuración de invalidación de Loader</span><span class="sxs-lookup"><span data-stu-id="ecf29-111">Loader Override Settings</span></span>](#loader-override-settings)|

### [*<span data-ttu-id="ecf29-112">Configuración de invalidación de Loader</span><span class="sxs-lookup"><span data-stu-id="ecf29-112">Loader Override Settings</span></span>*](#loader-override-settings-policies)
|<span data-ttu-id="ecf29-113">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="ecf29-113">Policy Name</span></span>|<span data-ttu-id="ecf29-114">Título</span><span class="sxs-lookup"><span data-stu-id="ecf29-114">Caption</span></span>|
|-|-|
|[<span data-ttu-id="ecf29-115">browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="ecf29-115">browserExecutableFolder</span></span>](#browserexecutablefolder)|<span data-ttu-id="ecf29-116">Configure la ubicación de la carpeta ejecutable del explorador</span><span class="sxs-lookup"><span data-stu-id="ecf29-116">Configure the location of the browser executable folder</span></span>|
|[<span data-ttu-id="ecf29-117">releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="ecf29-117">releaseChannelPreference</span></span>](#releasechannelpreference)|<span data-ttu-id="ecf29-118">Establezca las preferencias de pedido de búsqueda de canal de publicación</span><span class="sxs-lookup"><span data-stu-id="ecf29-118">Set the release channel search order preference</span></span>|




  ## <span data-ttu-id="ecf29-119">Directivas de configuración de invalidación de Loader</span><span class="sxs-lookup"><span data-stu-id="ecf29-119">Loader Override Settings policies</span></span>

  [<span data-ttu-id="ecf29-120">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="ecf29-120">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="ecf29-121">browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="ecf29-121">browserExecutableFolder</span></span>
  #### <span data-ttu-id="ecf29-122">Configure la ubicación de la carpeta ejecutable del explorador</span><span class="sxs-lookup"><span data-stu-id="ecf29-122">Configure the location of the browser executable folder</span></span>
  
  
  #### <span data-ttu-id="ecf29-123">Versiones compatibles:</span><span class="sxs-lookup"><span data-stu-id="ecf29-123">Supported versions:</span></span>
  - <span data-ttu-id="ecf29-124">En Windows desde la versión 87 o posterior</span><span class="sxs-lookup"><span data-stu-id="ecf29-124">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="ecf29-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecf29-125">Description</span></span>
  <span data-ttu-id="ecf29-126">Esta directiva configura las aplicaciones de WebView2 para usar el tiempo de ejecución de WebView2 en la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="ecf29-126">This policy configures WebView2 applications to use the WebView2 Runtime in the specified path.</span></span> <span data-ttu-id="ecf29-127">La carpeta debe contener los siguientes archivos: msedgewebview2. exe, msedge. dll, etc.</span><span class="sxs-lookup"><span data-stu-id="ecf29-127">The folder should contain the following files: msedgewebview2.exe, msedge.dll, and so on.</span></span>

<span data-ttu-id="ecf29-128">Para establecer el valor de la ruta de acceso de la carpeta, especifique un par de valor y nombre de valor.</span><span class="sxs-lookup"><span data-stu-id="ecf29-128">To set the value for the folder path, provide a Value name and Value pair.</span></span> <span data-ttu-id="ecf29-129">Configure el nombre de valor en el ID. del modelo de usuario de la aplicación o en el nombre del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="ecf29-129">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="ecf29-130">Puede usar el carácter comodín "\*" como nombre de valor para aplicar a todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ecf29-130">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="ecf29-131">Características admitidas:</span><span class="sxs-lookup"><span data-stu-id="ecf29-131">Supported features:</span></span>
  - <span data-ttu-id="ecf29-132">Puede ser obligatorio: sí</span><span class="sxs-lookup"><span data-stu-id="ecf29-132">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="ecf29-133">Puede ser recomendable: no</span><span class="sxs-lookup"><span data-stu-id="ecf29-133">Can be recommended: No</span></span>
  - <span data-ttu-id="ecf29-134">Actualización de directiva dinámica: sí</span><span class="sxs-lookup"><span data-stu-id="ecf29-134">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="ecf29-135">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ecf29-135">Data Type:</span></span>
  - <span data-ttu-id="ecf29-136">Lista de cadenas</span><span class="sxs-lookup"><span data-stu-id="ecf29-136">List of strings</span></span>

  #### <span data-ttu-id="ecf29-137">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="ecf29-137">Windows information and settings</span></span>
  ##### <span data-ttu-id="ecf29-138">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ecf29-138">Group Policy (ADMX) info</span></span>
  - <span data-ttu-id="ecf29-139">Nombre único de GP: browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="ecf29-139">GP unique name: browserExecutableFolder</span></span>
  - <span data-ttu-id="ecf29-140">Nombre GP: configure la ubicación de la carpeta ejecutable del explorador.</span><span class="sxs-lookup"><span data-stu-id="ecf29-140">GP name: Configure the location of the browser executable folder</span></span>
  - <span data-ttu-id="ecf29-141">Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge WebView2/Loader cambiar configuración</span><span class="sxs-lookup"><span data-stu-id="ecf29-141">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="ecf29-142">Ruta de acceso de GP (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="ecf29-142">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="ecf29-143">Nombre de archivo ADMX de GP: MSEdgeWebView2. ADMX</span><span class="sxs-lookup"><span data-stu-id="ecf29-143">GP ADMX file name: MSEdgeWebView2.admx</span></span>
  ##### <span data-ttu-id="ecf29-144">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="ecf29-144">Windows Registry Settings</span></span>
  - <span data-ttu-id="ecf29-145">Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="ecf29-145">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder</span></span>
  - <span data-ttu-id="ecf29-146">Ruta de acceso (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="ecf29-146">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="ecf29-147">Nombre del valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ecf29-147">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="ecf29-148">Tipo de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ecf29-148">Value Type: list of REG_SZ</span></span>
  ##### <span data-ttu-id="ecf29-149">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ecf29-149">Example value:</span></span>
```
SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```


  

  [<span data-ttu-id="ecf29-150">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="ecf29-150">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="ecf29-151">releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="ecf29-151">releaseChannelPreference</span></span>
  #### <span data-ttu-id="ecf29-152">Establezca las preferencias de pedido de búsqueda de canal de publicación</span><span class="sxs-lookup"><span data-stu-id="ecf29-152">Set the release channel search order preference</span></span>
  
  
  #### <span data-ttu-id="ecf29-153">Versiones compatibles:</span><span class="sxs-lookup"><span data-stu-id="ecf29-153">Supported versions:</span></span>
  - <span data-ttu-id="ecf29-154">En Windows desde la versión 87 o posterior</span><span class="sxs-lookup"><span data-stu-id="ecf29-154">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="ecf29-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecf29-155">Description</span></span>
  <span data-ttu-id="ecf29-156">El orden de búsqueda por canal predeterminado es WebView2 Runtime, Beta, Dev y Canarias.</span><span class="sxs-lookup"><span data-stu-id="ecf29-156">The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.</span></span>

<span data-ttu-id="ecf29-157">Para invertir el orden de búsqueda predeterminado, establezca esta directiva en 1.</span><span class="sxs-lookup"><span data-stu-id="ecf29-157">To reverse the default search order, set this policy to 1.</span></span>

<span data-ttu-id="ecf29-158">Para establecer el valor de las preferencias de canal de liberación, especifique un nombre de valor y un par de valores.</span><span class="sxs-lookup"><span data-stu-id="ecf29-158">To set the value for the release channel preference, provide a Value name and Value pair.</span></span> <span data-ttu-id="ecf29-159">Configure el nombre de valor en el ID. del modelo de usuario de la aplicación o en el nombre del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="ecf29-159">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="ecf29-160">Puede usar el carácter comodín "\*" como nombre de valor para aplicar a todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ecf29-160">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="ecf29-161">Características admitidas:</span><span class="sxs-lookup"><span data-stu-id="ecf29-161">Supported features:</span></span>
  - <span data-ttu-id="ecf29-162">Puede ser obligatorio: sí</span><span class="sxs-lookup"><span data-stu-id="ecf29-162">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="ecf29-163">Puede ser recomendable: no</span><span class="sxs-lookup"><span data-stu-id="ecf29-163">Can be recommended: No</span></span>
  - <span data-ttu-id="ecf29-164">Actualización de directiva dinámica: sí</span><span class="sxs-lookup"><span data-stu-id="ecf29-164">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="ecf29-165">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ecf29-165">Data Type:</span></span>
  - <span data-ttu-id="ecf29-166">Lista de cadenas</span><span class="sxs-lookup"><span data-stu-id="ecf29-166">List of strings</span></span>

  #### <span data-ttu-id="ecf29-167">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="ecf29-167">Windows information and settings</span></span>
  ##### <span data-ttu-id="ecf29-168">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ecf29-168">Group Policy (ADMX) info</span></span>
  - <span data-ttu-id="ecf29-169">Nombre único de GP: releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="ecf29-169">GP unique name: releaseChannelPreference</span></span>
  - <span data-ttu-id="ecf29-170">Nombre GP: establecer el canal de lanzamiento de preferencias de pedido de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ecf29-170">GP name: Set the release channel search order preference</span></span>
  - <span data-ttu-id="ecf29-171">Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge WebView2/Loader cambiar configuración</span><span class="sxs-lookup"><span data-stu-id="ecf29-171">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="ecf29-172">Ruta de acceso de GP (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="ecf29-172">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="ecf29-173">Nombre de archivo ADMX de GP: MSEdgeWebView2. ADMX</span><span class="sxs-lookup"><span data-stu-id="ecf29-173">GP ADMX file name: MSEdgeWebView2.admx</span></span>
  ##### <span data-ttu-id="ecf29-174">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="ecf29-174">Windows Registry Settings</span></span>
  - <span data-ttu-id="ecf29-175">Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="ecf29-175">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference</span></span>
  - <span data-ttu-id="ecf29-176">Ruta de acceso (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="ecf29-176">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="ecf29-177">Nombre del valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ecf29-177">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="ecf29-178">Tipo de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ecf29-178">Value Type: list of REG_SZ</span></span>
  ##### <span data-ttu-id="ecf29-179">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ecf29-179">Example value:</span></span>
```
SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference = "Name: *, Value: 1"

```


  

  [<span data-ttu-id="ecf29-180">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="ecf29-180">Back to top</span></span>](#microsoft-edge-webview2---policies)


## <span data-ttu-id="ecf29-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ecf29-181">See also</span></span>
- [<span data-ttu-id="ecf29-182">Configuración de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ecf29-182">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="ecf29-183">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ecf29-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ecf29-184">Blog de líneas de base de seguridad de Microsoft</span><span class="sxs-lookup"><span data-stu-id="ecf29-184">Microsoft Security Baselines Blog</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)