---
title: Documentación de directiva de WebView2 de Microsoft Edge
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 06/29/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentación de Windows y Mac para todas las directivas admitidas por Explorador Microsoft Edge
ms.openlocfilehash: cec4ab92257322b93072b694ceddc7ab6351b287
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642946"
---
# <a name="microsoft-edge-webview2---policies"></a><span data-ttu-id="818bd-103">Microsoft Edge WebView2: directivas</span><span class="sxs-lookup"><span data-stu-id="818bd-103">Microsoft Edge WebView2 - Policies</span></span>

<span data-ttu-id="818bd-104">La versión más reciente de Microsoft Edge WebView2 incluye las siguientes directivas.</span><span class="sxs-lookup"><span data-stu-id="818bd-104">The latest version of Microsoft Edge WebView2 includes the following policies.</span></span> <span data-ttu-id="818bd-105">Puede usar estas directivas para configurar cómo se ejecuta Microsoft Edge WebView2 en su organización.</span><span class="sxs-lookup"><span data-stu-id="818bd-105">You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.</span></span>

<span data-ttu-id="818bd-106">Para obtener información sobre un conjunto adicional de directivas usadas para controlar cómo y cuándo se actualiza Microsoft Edge WebView2, vea la [referencia de directiva de actualización de Microsoft Edge](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="818bd-106">For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).</span></span>


> [!NOTE]
> <span data-ttu-id="818bd-107">Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.</span><span class="sxs-lookup"><span data-stu-id="818bd-107">This article applies to Microsoft Edge version 87 or later.</span></span>

## <a name="available-policies"></a><span data-ttu-id="818bd-108">Directivas disponibles</span><span class="sxs-lookup"><span data-stu-id="818bd-108">Available policies</span></span>

<span data-ttu-id="818bd-109">En estas tablas se muestran todas las directivas de grupo disponibles en esta versión de Microsoft Edge WebView2.</span><span class="sxs-lookup"><span data-stu-id="818bd-109">These tables list all of the group policies available in this release of Microsoft Edge WebView2.</span></span> <span data-ttu-id="818bd-110">Usa los vínculos de la tabla para obtener más detalles sobre directivas específicas.</span><span class="sxs-lookup"><span data-stu-id="818bd-110">Use the links in the table to get more details about specific policies.</span></span>

- [<span data-ttu-id="818bd-111">Configuración de invalidación de Loader</span><span class="sxs-lookup"><span data-stu-id="818bd-111">Loader Override Settings</span></span>](#loader-override-settings)


### [*<a name="loader-override-settings"></a><span data-ttu-id="818bd-112">Configuración de invalidación de Loader</span><span class="sxs-lookup"><span data-stu-id="818bd-112">Loader Override Settings</span></span>*](#loader-override-settings-policies)

|<span data-ttu-id="818bd-113">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="818bd-113">Policy Name</span></span>|<span data-ttu-id="818bd-114">Título</span><span class="sxs-lookup"><span data-stu-id="818bd-114">Caption</span></span>|
|-|-|
|[<span data-ttu-id="818bd-115">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="818bd-115">BrowserExecutableFolder</span></span>](#browserexecutablefolder)|<span data-ttu-id="818bd-116">Configure la ubicación de la carpeta ejecutable del explorador</span><span class="sxs-lookup"><span data-stu-id="818bd-116">Configure the location of the browser executable folder</span></span>|
|[<span data-ttu-id="818bd-117">ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="818bd-117">ReleaseChannelPreference</span></span>](#releasechannelpreference)|<span data-ttu-id="818bd-118">Establezca las preferencias de pedido de búsqueda de canal de publicación</span><span class="sxs-lookup"><span data-stu-id="818bd-118">Set the release channel search order preference</span></span>|




  ## <a name="loader-override-settings-policies"></a><span data-ttu-id="818bd-119">Directivas de configuración de invalidación de Loader</span><span class="sxs-lookup"><span data-stu-id="818bd-119">Loader Override Settings policies</span></span>

  [<span data-ttu-id="818bd-120">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="818bd-120">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <a name="browserexecutablefolder"></a><span data-ttu-id="818bd-121">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="818bd-121">BrowserExecutableFolder</span></span>

  #### <a name="configure-the-location-of-the-browser-executable-folder"></a><span data-ttu-id="818bd-122">Configure la ubicación de la carpeta ejecutable del explorador</span><span class="sxs-lookup"><span data-stu-id="818bd-122">Configure the location of the browser executable folder</span></span>

  
  
  #### <a name="supported-versions"></a><span data-ttu-id="818bd-123">Versiones compatibles:</span><span class="sxs-lookup"><span data-stu-id="818bd-123">Supported versions:</span></span>

  - <span data-ttu-id="818bd-124">En Windows desde la versión 87 o posterior</span><span class="sxs-lookup"><span data-stu-id="818bd-124">On Windows since 87 or later</span></span>

  #### <a name="description"></a><span data-ttu-id="818bd-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="818bd-125">Description</span></span>

  <span data-ttu-id="818bd-126">Esta directiva configura las aplicaciones de WebView2 para usar el tiempo de ejecución de WebView2 en la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="818bd-126">This policy configures WebView2 applications to use the WebView2 Runtime in the specified path.</span></span> <span data-ttu-id="818bd-127">La carpeta debe contener los siguientes archivos: msedgewebview2. exe, msedge. dll, etc.</span><span class="sxs-lookup"><span data-stu-id="818bd-127">The folder should contain the following files: msedgewebview2.exe, msedge.dll, and so on.</span></span>

<span data-ttu-id="818bd-128">Para establecer el valor de la ruta de acceso de la carpeta, especifique un par de valor y nombre de valor.</span><span class="sxs-lookup"><span data-stu-id="818bd-128">To set the value for the folder path, provide a Value name and Value pair.</span></span> <span data-ttu-id="818bd-129">Configure el nombre de valor en el ID. del modelo de usuario de la aplicación o en el nombre del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="818bd-129">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="818bd-130">Puede usar el carácter comodín "\*" como nombre de valor para aplicar a todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="818bd-130">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <a name="supported-features"></a><span data-ttu-id="818bd-131">Características admitidas:</span><span class="sxs-lookup"><span data-stu-id="818bd-131">Supported features:</span></span>

  - <span data-ttu-id="818bd-132">Puede ser obligatorio: sí</span><span class="sxs-lookup"><span data-stu-id="818bd-132">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="818bd-133">Puede ser recomendable: no</span><span class="sxs-lookup"><span data-stu-id="818bd-133">Can be recommended: No</span></span>
  - <span data-ttu-id="818bd-134">Actualización de directiva dinámica: sí</span><span class="sxs-lookup"><span data-stu-id="818bd-134">Dynamic Policy Refresh: Yes</span></span>

  #### <a name="data-type"></a><span data-ttu-id="818bd-135">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="818bd-135">Data Type:</span></span>

  - <span data-ttu-id="818bd-136">Lista de cadenas</span><span class="sxs-lookup"><span data-stu-id="818bd-136">List of strings</span></span>

  #### <a name="windows-information-and-settings"></a><span data-ttu-id="818bd-137">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="818bd-137">Windows information and settings</span></span>

  ##### <a name="group-policy-admx-info"></a><span data-ttu-id="818bd-138">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="818bd-138">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="818bd-139">Nombre único de GP: BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="818bd-139">GP unique name: BrowserExecutableFolder</span></span>
  - <span data-ttu-id="818bd-140">Nombre GP: configure la ubicación de la carpeta ejecutable del explorador.</span><span class="sxs-lookup"><span data-stu-id="818bd-140">GP name: Configure the location of the browser executable folder</span></span>
  - <span data-ttu-id="818bd-141">Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge WebView2/Loader cambiar configuración</span><span class="sxs-lookup"><span data-stu-id="818bd-141">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="818bd-142">Ruta de acceso de GP (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="818bd-142">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="818bd-143">Nombre de archivo ADMX de GP: MSEdgeWebView2. ADMX</span><span class="sxs-lookup"><span data-stu-id="818bd-143">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <a name="windows-registry-settings"></a><span data-ttu-id="818bd-144">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="818bd-144">Windows Registry Settings</span></span>

  - <span data-ttu-id="818bd-145">Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="818bd-145">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder</span></span>
  - <span data-ttu-id="818bd-146">Ruta de acceso (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="818bd-146">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="818bd-147">Nombre del valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="818bd-147">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="818bd-148">Tipo de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="818bd-148">Value Type: list of REG_SZ</span></span>

  ##### <a name="example-value"></a><span data-ttu-id="818bd-149">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="818bd-149">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [<span data-ttu-id="818bd-150">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="818bd-150">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <a name="releasechannelpreference"></a><span data-ttu-id="818bd-151">ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="818bd-151">ReleaseChannelPreference</span></span>

  #### <a name="set-the-release-channel-search-order-preference"></a><span data-ttu-id="818bd-152">Establezca las preferencias de pedido de búsqueda de canal de publicación</span><span class="sxs-lookup"><span data-stu-id="818bd-152">Set the release channel search order preference</span></span>

  
  
  #### <a name="supported-versions"></a><span data-ttu-id="818bd-153">Versiones compatibles:</span><span class="sxs-lookup"><span data-stu-id="818bd-153">Supported versions:</span></span>

  - <span data-ttu-id="818bd-154">En Windows desde la versión 87 o posterior</span><span class="sxs-lookup"><span data-stu-id="818bd-154">On Windows since 87 or later</span></span>

  #### <a name="description"></a><span data-ttu-id="818bd-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="818bd-155">Description</span></span>

  <span data-ttu-id="818bd-156">El orden de búsqueda por canal predeterminado es WebView2 Runtime, Beta, Dev y Canarias.</span><span class="sxs-lookup"><span data-stu-id="818bd-156">The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.</span></span>

<span data-ttu-id="818bd-157">Para invertir el orden de búsqueda predeterminado, establezca esta directiva en 1.</span><span class="sxs-lookup"><span data-stu-id="818bd-157">To reverse the default search order, set this policy to 1.</span></span>

<span data-ttu-id="818bd-158">Para establecer el valor de las preferencias de canal de liberación, especifique un nombre de valor y un par de valores.</span><span class="sxs-lookup"><span data-stu-id="818bd-158">To set the value for the release channel preference, provide a Value name and Value pair.</span></span> <span data-ttu-id="818bd-159">Configure el nombre de valor en el ID. del modelo de usuario de la aplicación o en el nombre del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="818bd-159">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="818bd-160">Puede usar el carácter comodín "\*" como nombre de valor para aplicar a todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="818bd-160">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <a name="supported-features"></a><span data-ttu-id="818bd-161">Características admitidas:</span><span class="sxs-lookup"><span data-stu-id="818bd-161">Supported features:</span></span>

  - <span data-ttu-id="818bd-162">Puede ser obligatorio: sí</span><span class="sxs-lookup"><span data-stu-id="818bd-162">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="818bd-163">Puede ser recomendable: no</span><span class="sxs-lookup"><span data-stu-id="818bd-163">Can be recommended: No</span></span>
  - <span data-ttu-id="818bd-164">Actualización de directiva dinámica: sí</span><span class="sxs-lookup"><span data-stu-id="818bd-164">Dynamic Policy Refresh: Yes</span></span>

  #### <a name="data-type"></a><span data-ttu-id="818bd-165">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="818bd-165">Data Type:</span></span>

  - <span data-ttu-id="818bd-166">Lista de cadenas</span><span class="sxs-lookup"><span data-stu-id="818bd-166">List of strings</span></span>

  #### <a name="windows-information-and-settings"></a><span data-ttu-id="818bd-167">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="818bd-167">Windows information and settings</span></span>

  ##### <a name="group-policy-admx-info"></a><span data-ttu-id="818bd-168">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="818bd-168">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="818bd-169">Nombre único de GP: ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="818bd-169">GP unique name: ReleaseChannelPreference</span></span>
  - <span data-ttu-id="818bd-170">Nombre GP: establecer el canal de lanzamiento de preferencias de pedido de búsqueda</span><span class="sxs-lookup"><span data-stu-id="818bd-170">GP name: Set the release channel search order preference</span></span>
  - <span data-ttu-id="818bd-171">Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge WebView2/Loader cambiar configuración</span><span class="sxs-lookup"><span data-stu-id="818bd-171">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="818bd-172">Ruta de acceso de GP (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="818bd-172">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="818bd-173">Nombre de archivo ADMX de GP: MSEdgeWebView2. ADMX</span><span class="sxs-lookup"><span data-stu-id="818bd-173">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <a name="windows-registry-settings"></a><span data-ttu-id="818bd-174">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="818bd-174">Windows Registry Settings</span></span>

  - <span data-ttu-id="818bd-175">Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="818bd-175">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference</span></span>
  - <span data-ttu-id="818bd-176">Ruta de acceso (recomendado): N/D</span><span class="sxs-lookup"><span data-stu-id="818bd-176">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="818bd-177">Nombre del valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="818bd-177">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="818bd-178">Tipo de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="818bd-178">Value Type: list of REG_SZ</span></span>

  ##### <a name="example-value"></a><span data-ttu-id="818bd-179">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="818bd-179">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [<span data-ttu-id="818bd-180">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="818bd-180">Back to top</span></span>](#microsoft-edge-webview2---policies)


## <a name="see-also"></a><span data-ttu-id="818bd-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="818bd-181">See also</span></span>

- [<span data-ttu-id="818bd-182">Configuración de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="818bd-182">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="818bd-183">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="818bd-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="818bd-184">Blog de líneas de base de seguridad de Microsoft</span><span class="sxs-lookup"><span data-stu-id="818bd-184">Microsoft Security Baselines Blog</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)