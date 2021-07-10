---
title: Documentación de directiva de Microsoft Edge Update
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
description: Documentación de todas las directivas admitidas por Microsoft Edge Update
ms.openlocfilehash: a9808981acad544042c6e0ccb59ff755a670c848
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642326"
---
# <a name="microsoft-edge---update-policies"></a><span data-ttu-id="76bfd-103">Microsoft Edge: Directivas de actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-103">Microsoft Edge - Update policies</span></span>

<span data-ttu-id="76bfd-104">La última versión de Microsoft Edge incluye las siguientes directivas que puedes usar para controlar cómo y cuándo se actualiza Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="76bfd-105">Para obtener información sobre otras directivas disponibles en Microsoft Edge, consulta la [referencia de directiva del explorador Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="76bfd-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="76bfd-106">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="76bfd-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <a name="available-policies"></a><span data-ttu-id="76bfd-107">Directivas disponibles</span><span class="sxs-lookup"><span data-stu-id="76bfd-107">Available policies</span></span>
<span data-ttu-id="76bfd-108">Estas tablas enumeran todas las directivas de grupo relacionadas con la actualización disponibles en esta versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="76bfd-109">Usa los vínculos de la tabla para obtener más detalles sobre directivas específicas.</span><span class="sxs-lookup"><span data-stu-id="76bfd-109">Use the links in the table to get more details about specific policies.</span></span>

<span data-ttu-id="76bfd-110">|&nbsp;|&nbsp;| |**-**|-| |**[Aplicaciones](#applications)**|[Preferencias](#preferences)| |**[Servidor proxy](#proxy-server)**|[Vista web de Microsoft Edge](#microsoft-edge-webview)|</span><span class="sxs-lookup"><span data-stu-id="76bfd-110">|&nbsp;|&nbsp;| |**-**|-| |**[Applications](#applications)**|[Preferences](#preferences)| |**[Proxy Server](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span></span>
### [<a name="applications"></a><span data-ttu-id="76bfd-111">Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="76bfd-111">Applications</span></span>](#applications-policies)
|<span data-ttu-id="76bfd-112">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="76bfd-112">Policy Name</span></span>|<span data-ttu-id="76bfd-113">Título</span><span class="sxs-lookup"><span data-stu-id="76bfd-113">Caption</span></span>|
|-|-|
|[<span data-ttu-id="76bfd-114">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-114">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="76bfd-115">Valor predeterminado de Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-115">Allow installation default</span></span>|
|[<span data-ttu-id="76bfd-116">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-116">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="76bfd-117">Valor predeterminado de Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-117">Update policy override default</span></span>|
|[<span data-ttu-id="76bfd-118">Instalar</span><span class="sxs-lookup"><span data-stu-id="76bfd-118">Install</span></span>](#install)|<span data-ttu-id="76bfd-119">Permitir instalación (por canal)</span><span class="sxs-lookup"><span data-stu-id="76bfd-119">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="76bfd-120">Actualizar</span><span class="sxs-lookup"><span data-stu-id="76bfd-120">Update</span></span>](#update)|<span data-ttu-id="76bfd-121">Invalidar directiva de actualización (por canal)</span><span class="sxs-lookup"><span data-stu-id="76bfd-121">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="76bfd-122">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="76bfd-122">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="76bfd-123">Permitir la experiencia de exploradores Microsoft Edge en paralelo</span><span class="sxs-lookup"><span data-stu-id="76bfd-123">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="76bfd-124">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-124">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="76bfd-125">Impedir la creación de accesos directos de escritorio durante la instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="76bfd-125">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="76bfd-126">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="76bfd-126">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="76bfd-127">Impedir la creación de accesos directos de escritorio durante la instalación (por canal)</span><span class="sxs-lookup"><span data-stu-id="76bfd-127">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="76bfd-128">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="76bfd-128">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="76bfd-129">Revertir a la versión de destino (por canal)</span><span class="sxs-lookup"><span data-stu-id="76bfd-129">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="76bfd-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="76bfd-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="76bfd-131">Invalidación de versión de destino (por canal)</span><span class="sxs-lookup"><span data-stu-id="76bfd-131">Target version override (per channel)</span></span>|

### [<a name="preferences"></a><span data-ttu-id="76bfd-132">Preferencias</span><span class="sxs-lookup"><span data-stu-id="76bfd-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="76bfd-133">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="76bfd-133">Policy Name</span></span>|<span data-ttu-id="76bfd-134">Título</span><span class="sxs-lookup"><span data-stu-id="76bfd-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="76bfd-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="76bfd-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="76bfd-136">invalidar el período de buscar actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="76bfd-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="76bfd-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="76bfd-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="76bfd-138">Período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="76bfd-138">Time period in each day to suppress auto-update check</span></span>|

### [<a name="proxy-server"></a><span data-ttu-id="76bfd-139">Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="76bfd-140">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="76bfd-140">Policy Name</span></span>|<span data-ttu-id="76bfd-141">Leyenda</span><span class="sxs-lookup"><span data-stu-id="76bfd-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="76bfd-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="76bfd-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="76bfd-143">Elegir cómo especificar la configuración del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="76bfd-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="76bfd-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="76bfd-145">Dirección URL a un archivo proxy .pac</span><span class="sxs-lookup"><span data-stu-id="76bfd-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="76bfd-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="76bfd-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="76bfd-147">Dirección o dirección URL del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-147">Address or URL of proxy server</span></span>|

### [<a name="microsoft-edge-webview"></a><span data-ttu-id="76bfd-148">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="76bfd-148">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="76bfd-149">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="76bfd-149">Policy Name</span></span>|<span data-ttu-id="76bfd-150">Título</span><span class="sxs-lookup"><span data-stu-id="76bfd-150">Caption</span></span>|
|-|-|
|[<span data-ttu-id="76bfd-151">Instalar</span><span class="sxs-lookup"><span data-stu-id="76bfd-151">Install</span></span>](#install-webview)|<span data-ttu-id="76bfd-152">Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-152">Allow installation</span></span>|
|[<span data-ttu-id="76bfd-153">Actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-153">Update</span></span>](#update-webview)|<span data-ttu-id="76bfd-154">Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-154">Update policy override</span></span>|

## <a name="applications-policies"></a><span data-ttu-id="76bfd-155">Directivas de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="76bfd-155">Applications policies</span></span>

[<span data-ttu-id="76bfd-156">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-156">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="installdefault"></a><span data-ttu-id="76bfd-157">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-157">InstallDefault</span></span>
#### <a name="allow-installation-default"></a><span data-ttu-id="76bfd-158">Valor predeterminado de Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-158">Allow installation default</span></span>
><span data-ttu-id="76bfd-159">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-159">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-160">Description</span></span>
<span data-ttu-id="76bfd-161">Puede especificar el comportamiento predeterminado de todos los canales para permitir o bloquear Microsoft Edge en dispositivos unidos al dominio.</span><span class="sxs-lookup"><span data-stu-id="76bfd-161">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="76bfd-162">Puede reemplazar esta directiva para canales individuales si habilita la directiva [Permitir instalación](#install) para canales específicos.</span><span class="sxs-lookup"><span data-stu-id="76bfd-162">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="76bfd-163">Si deshabilita esta directiva, se bloquea la instalación de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-163">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="76bfd-164">Esto solo afecta a la instalación de software de Microsoft Edge cuando la directiva "[Permitir instalación](#install)" está establecida en No configurada.</span><span class="sxs-lookup"><span data-stu-id="76bfd-164">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="76bfd-165">Esta directiva no impide que se ejecute Microsoft Edge Update ni impide que los usuarios instalen software de Microsoft Edge con otros métodos.</span><span class="sxs-lookup"><span data-stu-id="76bfd-165">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="76bfd-166">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="76bfd-166">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-167">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-167">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-168">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-168">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-169">Nombre único de GP: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-169">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="76bfd-170">Nombre de GP: valor predeterminado de Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-170">GP name: Allow installation default</span></span>
- <span data-ttu-id="76bfd-171">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="76bfd-171">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="76bfd-172">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-172">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-173">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-173">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-174">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-174">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-175">Nombre de valor: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-175">Value Name: InstallDefault</span></span>
- <span data-ttu-id="76bfd-176">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-176">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-177">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-177">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="76bfd-178">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-178">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatedefault"></a><span data-ttu-id="76bfd-179">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-179">UpdateDefault</span></span>
#### <a name="update-policy-override-default"></a><span data-ttu-id="76bfd-180">Valor predeterminado de Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-180">Update policy override default</span></span>
><span data-ttu-id="76bfd-181">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-181">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-182">Description</span></span>
<span data-ttu-id="76bfd-183">Permite especificar el comportamiento predeterminado de todos los canales relacionados con la manera en que Microsoft Edge Update trata las actualizaciones disponibles para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-183">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="76bfd-184">Se puede invalidar para canales individuales especificando la directiva '[Invalidar directiva de actualización](#update)' para esos canales específicos.</span><span class="sxs-lookup"><span data-stu-id="76bfd-184">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="76bfd-185">Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge de acuerdo con la configuración de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="76bfd-185">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="76bfd-186">Permitir siempre las actualizaciones: las actualizaciones siempre se aplican cuando se encuentran, ya sea mediante la búsqueda de actualizaciones periódicas o mediante una búsqueda de actualizaciones manual.</span><span class="sxs-lookup"><span data-stu-id="76bfd-186">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="76bfd-187">Solo actualizaciones silenciosas automáticas: las actualizaciones solo se aplican cuando las encuentra la búsqueda periódica de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="76bfd-187">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="76bfd-188">Solo actualizaciones manuales: las actualizaciones se aplican solo cuando el usuario ejecuta una búsqueda manual de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="76bfd-188">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="76bfd-189">Actualizaciones deshabilitadas: las actualizaciones nunca se aplican.</span><span class="sxs-lookup"><span data-stu-id="76bfd-189">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="76bfd-190">Si seleccionas las actualizaciones manuales, asegúrate de buscar periódicamente actualizaciones mediante el mecanismo de actualización manual de la aplicación, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="76bfd-190">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="76bfd-191">Si deshabilitas las actualizaciones, comprueba periódicamente si las hay y distribúyelas a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="76bfd-191">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="76bfd-192">Si no habilitas ni configuras esta directiva, Microsoft Edge Update administra las actualizaciones disponibles según se especifica en la directiva '[Invalidar directiva de actualizaciones](#update)'.</span><span class="sxs-lookup"><span data-stu-id="76bfd-192">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="76bfd-193">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="76bfd-193">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-194">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-194">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-195">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-195">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-196">Nombre único de GP: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-196">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="76bfd-197">Nombre de GP: Valor predeterminado de Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-197">GP name: Update policy override default</span></span>
- <span data-ttu-id="76bfd-198">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="76bfd-198">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="76bfd-199">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-199">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-200">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-200">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-201">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-201">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-202">Nombre de valor: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-202">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="76bfd-203">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-203">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-204">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-204">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="76bfd-205">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-205">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="install"></a><span data-ttu-id="76bfd-206">Instalar</span><span class="sxs-lookup"><span data-stu-id="76bfd-206">Install</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="76bfd-207">Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-207">Allow installation</span></span>
><span data-ttu-id="76bfd-208">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-208">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-209">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-209">Description</span></span>
<span data-ttu-id="76bfd-210">Especifica si se puede instalar un canal de Microsoft Edge en dispositivos unidos al dominio.</span><span class="sxs-lookup"><span data-stu-id="76bfd-210">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="76bfd-211">Si habilita esta directiva para un canal, no se bloqueará la instalación de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-211">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="76bfd-212">Si deshabilita esta directiva para un canal, se bloqueará la instalación de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-212">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="76bfd-213">Si no configura esta directiva para un canal, la configuración de la directiva "[Valor predeterminado de Permitir instalación](#installdefault)" determinará si los usuarios pueden instalar dicho canal de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-213">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="76bfd-214">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="76bfd-214">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-215">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-215">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-216">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-216">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-217">Nombre único de GP: Install</span><span class="sxs-lookup"><span data-stu-id="76bfd-217">GP unique name: Install</span></span>
- <span data-ttu-id="76bfd-218">Nombre de GP: Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-218">GP name: Allow installation</span></span>
- <span data-ttu-id="76bfd-219">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="76bfd-219">GP path:</span></span> 
  - <span data-ttu-id="76bfd-220">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76bfd-220">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="76bfd-221">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="76bfd-221">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="76bfd-222">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="76bfd-222">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="76bfd-223">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="76bfd-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="76bfd-224">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-224">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-225">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-225">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-226">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-226">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-227">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="76bfd-227">Value Name:</span></span> 
  - <span data-ttu-id="76bfd-228">(Estable): instalar{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="76bfd-228">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="76bfd-229">(Beta): instalar{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="76bfd-229">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="76bfd-230">(Canarias): instalar{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="76bfd-230">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="76bfd-231">(Dev): instalar{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="76bfd-231">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="76bfd-232">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-232">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-233">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-233">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="76bfd-234">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-234">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update"></a><span data-ttu-id="76bfd-235">Actualizar</span><span class="sxs-lookup"><span data-stu-id="76bfd-235">Update</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="76bfd-236">Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-236">Update policy override</span></span>
><span data-ttu-id="76bfd-237">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-237">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-238">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-238">Description</span></span>
<span data-ttu-id="76bfd-239">Especifica cómo trata Microsoft Edge Update las actualizaciones disponibles de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-239">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="76bfd-240">Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge de acuerdo con la configuración de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="76bfd-240">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="76bfd-241">Permitir siempre las actualizaciones: las actualizaciones siempre se aplican cuando se encuentran, ya sea mediante la búsqueda de actualizaciones periódicas o mediante una búsqueda de actualizaciones manual.</span><span class="sxs-lookup"><span data-stu-id="76bfd-241">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="76bfd-242">Solo actualizaciones silenciosas automáticas: las actualizaciones solo se aplican cuando las encuentra la búsqueda periódica de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="76bfd-242">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="76bfd-243">Solo actualizaciones manuales: las actualizaciones se aplican solo cuando el usuario ejecuta una búsqueda manual de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="76bfd-243">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="76bfd-244">(No todas las aplicaciones ofrecen una interfaz para esta opción).</span><span class="sxs-lookup"><span data-stu-id="76bfd-244">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="76bfd-245">Actualizaciones deshabilitadas: las actualizaciones nunca se aplican.</span><span class="sxs-lookup"><span data-stu-id="76bfd-245">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="76bfd-246">Si seleccionas las actualizaciones manuales, asegúrate de buscar periódicamente actualizaciones mediante el mecanismo de actualización manual de la aplicación, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="76bfd-246">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="76bfd-247">Si deshabilitas las actualizaciones, comprueba periódicamente si las hay y distribúyelas a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="76bfd-247">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="76bfd-248">Si no habilitas ni configuras esta directiva, Microsoft Edge Update administra las actualizaciones disponibles según se especifica en la directiva '[Valor predeterminado de Invalidar directiva de actualizaciones](#updatedefault)'.</span><span class="sxs-lookup"><span data-stu-id="76bfd-248">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="76bfd-249">Vea [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="76bfd-249">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="76bfd-250">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="76bfd-250">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-251">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-251">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-252">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-252">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-253">Nombre único de GP: Actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-253">GP unique name: Update</span></span>
- <span data-ttu-id="76bfd-254">Nombre de GP: Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-254">GP name: Update policy override</span></span>
- <span data-ttu-id="76bfd-255">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="76bfd-255">GP path:</span></span> 
  - <span data-ttu-id="76bfd-256">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76bfd-256">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="76bfd-257">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="76bfd-257">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="76bfd-258">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="76bfd-258">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="76bfd-259">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="76bfd-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="76bfd-260">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-260">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-261">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-261">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-262">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-262">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-263">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="76bfd-263">Value Name:</span></span> 
  - <span data-ttu-id="76bfd-264">(Estable): actualizar{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="76bfd-264">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="76bfd-265">(Beta): actualizar{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="76bfd-265">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="76bfd-266">(Canarias): actualizar{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="76bfd-266">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="76bfd-267">(Dev): actualizar{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="76bfd-267">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="76bfd-268">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-268">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-269">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-269">Example value:</span></span>
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[<span data-ttu-id="76bfd-270">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-270">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="allowsxs"></a><span data-ttu-id="76bfd-271">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="76bfd-271">Allowsxs</span></span>
#### <a name="allow-microsoft-edge-side-by-side-browser-experience"></a><span data-ttu-id="76bfd-272">Permitir la experiencia de exploradores Microsoft Edge en paralelo</span><span class="sxs-lookup"><span data-stu-id="76bfd-272">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="76bfd-273">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-273">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-274">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-274">Description</span></span>
<span data-ttu-id="76bfd-275">Esta directiva permite a un usuario ejecutar Microsoft Edge (Edge HTML) y Microsoft Edge (basado en Chromium) en paralelo.</span><span class="sxs-lookup"><span data-stu-id="76bfd-275">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="76bfd-276">Si esta directiva se establece en “No configurado”, Microsoft Edge (basado en Chromium) reemplazará a Microsoft Edge (Edge HTML) después del canal estable de Microsoft Edge (basado en Chromium) y se instalarán las actualizaciones de seguridad de noviembre de 2019.</span><span class="sxs-lookup"><span data-stu-id="76bfd-276">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="76bfd-277">Este es el mismo comportamiento que la opción “Deshabilitado”.</span><span class="sxs-lookup"><span data-stu-id="76bfd-277">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="76bfd-278">La opción “Deshabilitado” bloquea la experiencia en paralelo y Microsoft Edge (basado en Chromium) reemplazará a Microsoft Edge (Edge HTML) después del canal estable de Microsoft Edge (basado en Chromium) y se instalarán las actualizaciones de seguridad de noviembre de 2019.</span><span class="sxs-lookup"><span data-stu-id="76bfd-278">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="76bfd-279">Este es el mismo comportamiento que la opción “No configurado”.</span><span class="sxs-lookup"><span data-stu-id="76bfd-279">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="76bfd-280">Cuando esta directiva está “Habilitada”, se pueden ejecutar en paralelo Microsoft Edge (Edge HTML) y Microsoft Edge (basado en Chromium) después de instalado Microsoft Edge (basado en Chromium).</span><span class="sxs-lookup"><span data-stu-id="76bfd-280">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="76bfd-281">Para que esta directiva de grupo surta efecto, debe configurarse antes de la instalación automática de Microsoft Edge (basado en Chromium) por parte de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="76bfd-281">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="76bfd-282">Nota: un usuario puede bloquear la actualización automática de Microsoft Edge (basado en Chromium) mediante el kit de herramientas de bloqueo de Microsoft Edge (basado en Chromium).</span><span class="sxs-lookup"><span data-stu-id="76bfd-282">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-283">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-283">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-284">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-284">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-285">Nombre único de GP: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="76bfd-285">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="76bfd-286">Nombre de GP: permitir la experiencia en paralelo de exploradores Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76bfd-286">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="76bfd-287">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="76bfd-287">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="76bfd-288">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-288">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-289">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-289">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-290">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-290">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-291">Nombre del valor: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="76bfd-291">Value Name: Allowsxs</span></span>
- <span data-ttu-id="76bfd-292">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-292">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-293">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-293">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="76bfd-294">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-294">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcutdefault"></a><span data-ttu-id="76bfd-295">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-295">CreateDesktopShortcutDefault</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install-default"></a><span data-ttu-id="76bfd-296">Impedir la creación de accesos directos de escritorio durante la instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="76bfd-296">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="76bfd-297">Microsoft Edge Update 1.3.128.0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-297">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-298">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-298">Description</span></span>
<span data-ttu-id="76bfd-299">Permite especificar el comportamiento predeterminado de todos los canales para crear un acceso directo en el escritorio cuando se instala Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-299">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="76bfd-300">Si habilita esta directiva, se creará un acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-300">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="76bfd-301">Si deshabilita esta directiva, no se creará ningún acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-301">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="76bfd-302">Si no configura esta directiva, se creará un acceso directo de escritorio a Microsoft Edge durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="76bfd-302">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="76bfd-303">Si Microsoft Edge ya está instalado, esta directiva no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="76bfd-303">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-304">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-304">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-305">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-305">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-306">Nombre único de GP: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-306">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="76bfd-307">Nombre de GP: configuración predeterminada para impedir la creación de accesos directos de escritorio durante la instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-307">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="76bfd-308">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="76bfd-308">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="76bfd-309">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-309">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-310">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-310">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-311">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-311">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-312">Nombre del valor: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="76bfd-312">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="76bfd-313">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-313">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-314">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-314">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="76bfd-315">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-315">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcut"></a><span data-ttu-id="76bfd-316">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="76bfd-316">CreateDesktopShortcut</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install"></a><span data-ttu-id="76bfd-317">Impedir la creación de accesos directos de escritorio durante la instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-317">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="76bfd-318">Microsoft Edge Update 1.3.128.0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-318">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-319">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-319">Description</span></span>
<span data-ttu-id="76bfd-320">Si habilita esta directiva, se creará un acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-320">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="76bfd-321">Si deshabilita esta directiva, no se creará ningún acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-321">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="76bfd-322">Si no configura esta directiva, se creará un acceso directo de escritorio a Microsoft Edge durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="76bfd-322">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="76bfd-323">Si Microsoft Edge ya está instalado, esta directiva no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="76bfd-323">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="76bfd-324">Si no configura esta directiva para un canal, la configuración de directiva '[Impedir la creación de accesos directos de escritorio durante la instalación predeterminada](#createdesktopshortcutdefault)' determina la creación de accesos directos cuando se instala Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-324">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-325">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-325">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-326">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-326">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-327">Nombre único de GP: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="76bfd-327">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="76bfd-328">Nombre de GP: impedir la creación de métodos abreviados de escritorio durante la instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-328">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="76bfd-329">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="76bfd-329">GP path:</span></span> 
  - <span data-ttu-id="76bfd-330">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76bfd-330">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="76bfd-331">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="76bfd-331">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="76bfd-332">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="76bfd-332">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="76bfd-333">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="76bfd-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="76bfd-334">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-334">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-335">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-335">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-336">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-336">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-337">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="76bfd-337">Value Name:</span></span> 
  - <span data-ttu-id="76bfd-338">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="76bfd-338">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="76bfd-339">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="76bfd-339">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="76bfd-340">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="76bfd-340">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="76bfd-341">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="76bfd-341">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="76bfd-342">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-342">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-343">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-343">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="76bfd-344">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-344">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="rollbacktotargetversion"></a><span data-ttu-id="76bfd-345">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="76bfd-345">RollbackToTargetVersion</span></span>
#### <a name="rollback-to-target-version"></a><span data-ttu-id="76bfd-346">Revertir a la versión de destino</span><span class="sxs-lookup"><span data-stu-id="76bfd-346">Rollback to Target version</span></span>
><span data-ttu-id="76bfd-347">Microsoft Edge Update 1.3.133.3 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-347">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-348">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-348">Description</span></span>
<span data-ttu-id="76bfd-349">Especifica que Microsoft Edge Update debe revertir las instalaciones de Microsoft Edge a la versión que se indica en "[Invalidación de la versión de destino](#targetversionprefix)".</span><span class="sxs-lookup"><span data-stu-id="76bfd-349">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="76bfd-350">Esta directiva no surte efecto a menos que "[Invalidación de la versión de destino](#targetversionprefix)" e "[Invalidación de la directiva de actualización](#update)" se establezcan en uno de los estados activados (es decir, Permitir siempre las actualizaciones, Solo actualizaciones silenciosas automáticas o Solo actualizaciones manuales).</span><span class="sxs-lookup"><span data-stu-id="76bfd-350">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="76bfd-351">Si deshabilita esta directiva o no la configura, las instalaciones que tengan una versión superior a la especificada por la "[Invalidación de la versión de destino](#targetversionprefix)" quedarán tal cual están.</span><span class="sxs-lookup"><span data-stu-id="76bfd-351">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="76bfd-352">Si habilita esta directiva, las instalaciones que tengan una versión actual superior a la especificada por la "[Invalidación de la versión de destino](#targetversionprefix)" serán degradadas a la versión de destino.</span><span class="sxs-lookup"><span data-stu-id="76bfd-352">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="76bfd-353">Se recomienda a los usuarios que instalen la última versión del explorador Microsoft Edge para estar seguros de contar con la protección que proporcionan las últimas actualizaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="76bfd-353">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="76bfd-354">Revertir a una versión anterior supone un riesgo de exposición a problemas de seguridad conocidos.</span><span class="sxs-lookup"><span data-stu-id="76bfd-354">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="76bfd-355">Esta directiva está pensada para usarse como una solución provisional para resolver problemas relacionados con una actualización del explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76bfd-355">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="76bfd-356">Antes de revertir temporalmente a la versión anterior del explorador, recomendamos activar la sincronización ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) para todos los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="76bfd-356">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="76bfd-357">Si no se activa la sincronización, se corre el riesgo de pérdida definitiva de datos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="76bfd-357">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="76bfd-358">Utilice esta directiva bajo su propia responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="76bfd-358">Use this policy at your own risk.</span></span>

<span data-ttu-id="76bfd-359">Nota: todas las versiones disponibles para la reversión se pueden ver aquí [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="76bfd-359">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="76bfd-360">Esta directiva se aplica a Microsoft Edge, versión 86 o posterior.</span><span class="sxs-lookup"><span data-stu-id="76bfd-360">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="76bfd-361">Vea [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="76bfd-361">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="76bfd-362">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="76bfd-362">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-363">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-363">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-364">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-364">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-365">Nombre único de GP: RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="76bfd-365">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="76bfd-366">Nombre de GP: Revertir a la versión de destino</span><span class="sxs-lookup"><span data-stu-id="76bfd-366">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="76bfd-367">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="76bfd-367">GP path:</span></span> 
  - <span data-ttu-id="76bfd-368">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76bfd-368">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="76bfd-369">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="76bfd-369">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="76bfd-370">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="76bfd-370">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="76bfd-371">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="76bfd-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="76bfd-372">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-372">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-373">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-373">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-374">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-374">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-375">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="76bfd-375">Value Name:</span></span> 
  - <span data-ttu-id="76bfd-376">(Estable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="76bfd-376">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="76bfd-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="76bfd-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="76bfd-378">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="76bfd-378">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="76bfd-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="76bfd-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="76bfd-380">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-380">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-381">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-381">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="76bfd-382">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-382">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="targetversionprefix"></a><span data-ttu-id="76bfd-383">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="76bfd-383">TargetVersionPrefix</span></span>
#### <a name="target-version-override"></a><span data-ttu-id="76bfd-384">Invalidación de versión de destino</span><span class="sxs-lookup"><span data-stu-id="76bfd-384">Target version override</span></span>
><span data-ttu-id="76bfd-385">Microsoft Edge Update 1.3.119.43 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-385">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-386">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-386">Description</span></span>
<span data-ttu-id="76bfd-387">Cuando se habilita esta directiva y la actualización automática está habilitada, Microsoft Edge se actualizará a la versión especificada por este valor de directiva.</span><span class="sxs-lookup"><span data-stu-id="76bfd-387">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="76bfd-388">El valor de directiva debe ser una versión específica de Microsoft Edge, como 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="76bfd-388">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="76bfd-389">Si un dispositivo tiene una versión más reciente de Microsoft Edge que el valor especificado, Microsoft Edge permanecerá en la versión más reciente, mas no desactualizada a la versión especificada.</span><span class="sxs-lookup"><span data-stu-id="76bfd-389">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="76bfd-390">Si la versión especificada no existe o no tiene el formato correcto, Microsoft Edge permanecerá en su versión actual y no se actualizará a versiones futuras de manera automática.</span><span class="sxs-lookup"><span data-stu-id="76bfd-390">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="76bfd-391">Vea [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="76bfd-391">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="76bfd-392">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="76bfd-392">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-393">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-393">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-394">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-394">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-395">Nombre único de GP: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="76bfd-395">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="76bfd-396">Nombre de GP: Invalidación de versión de destino</span><span class="sxs-lookup"><span data-stu-id="76bfd-396">GP name: Target version override</span></span>
- <span data-ttu-id="76bfd-397">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="76bfd-397">GP path:</span></span> 
  - <span data-ttu-id="76bfd-398">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76bfd-398">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="76bfd-399">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="76bfd-399">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="76bfd-400">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="76bfd-400">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="76bfd-401">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="76bfd-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="76bfd-402">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-402">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-403">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-403">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-404">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-404">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-405">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="76bfd-405">Value Name:</span></span> 
  - <span data-ttu-id="76bfd-406">(Estable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="76bfd-406">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="76bfd-407">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="76bfd-407">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="76bfd-408">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="76bfd-408">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="76bfd-409">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="76bfd-409">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="76bfd-410">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="76bfd-410">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-411">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-411">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="76bfd-412">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-412">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="preferences-policies"></a><span data-ttu-id="76bfd-413">Directivas de preferencias</span><span class="sxs-lookup"><span data-stu-id="76bfd-413">Preferences policies</span></span>

[<span data-ttu-id="76bfd-414">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-414">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="autoupdatecheckperiodminutes"></a><span data-ttu-id="76bfd-415">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="76bfd-415">AutoUpdateCheckPeriodMinutes</span></span>
#### <a name="auto-update-check-period-override"></a><span data-ttu-id="76bfd-416">invalidar el período de buscar actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="76bfd-416">Auto-update check period override</span></span>
><span data-ttu-id="76bfd-417">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-417">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-418">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-418">Description</span></span>
<span data-ttu-id="76bfd-419">Si se habilita, esta directiva permite establecer un valor para el número mínimo de minutos entre las búsquedas de actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="76bfd-419">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="76bfd-420">De lo contrario, de manera predeterminada, la actualización automática busca actualizaciones cada 10 horas.</span><span class="sxs-lookup"><span data-stu-id="76bfd-420">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="76bfd-421">Si quieres deshabilitar todas las búsquedas de actualizaciones automáticas, establece el valor en 0 (no recomendado).</span><span class="sxs-lookup"><span data-stu-id="76bfd-421">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-422">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-422">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-423">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-423">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-424">Nombre único de GP: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="76bfd-424">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="76bfd-425">Nombre de GP: invalidar el período de buscar actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="76bfd-425">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="76bfd-426">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Preferencias</span><span class="sxs-lookup"><span data-stu-id="76bfd-426">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="76bfd-427">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-427">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-428">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-428">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-429">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-429">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-430">Nombre de valor: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="76bfd-430">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="76bfd-431">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-431">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-432">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-432">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="76bfd-433">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-433">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatessuppressed"></a><span data-ttu-id="76bfd-434">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="76bfd-434">UpdatesSuppressed</span></span>
#### <a name="time-period-in-each-day-to-suppress-auto-update-check"></a><span data-ttu-id="76bfd-435">Período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="76bfd-435">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="76bfd-436">Microsoft Edge Update 1.3.33.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-436">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-437">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-437">Description</span></span>
<span data-ttu-id="76bfd-438">Si habilitas esta Directiva, las búsquedas de actualizaciones se suprimirán cada día, a partir de Hora:Minuto durante un período de tiempo (en minutos).</span><span class="sxs-lookup"><span data-stu-id="76bfd-438">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="76bfd-439">La duración no se ve afectada por el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="76bfd-439">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="76bfd-440">Por ejemplo, si la hora de inicio es 22:00 y la duración es 480 minutos, las actualizaciones se suprimirán durante 8 horas exactamente, independientemente de si el horario de verano comienza o finaliza durante este período.</span><span class="sxs-lookup"><span data-stu-id="76bfd-440">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="76bfd-441">Si deshabilitas o no configuras esta directiva, las búsquedas de actualizaciones no se suprimirán durante ningún período determinado.</span><span class="sxs-lookup"><span data-stu-id="76bfd-441">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-442">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-442">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-443">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-443">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-444">Nombre único de GP: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="76bfd-444">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="76bfd-445">Nombre de GP: período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="76bfd-445">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="76bfd-446">Opciones {Hora, Minuto, Duración}</span><span class="sxs-lookup"><span data-stu-id="76bfd-446">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="76bfd-447">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Preferencias</span><span class="sxs-lookup"><span data-stu-id="76bfd-447">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="76bfd-448">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-448">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-449">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-449">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-450">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-450">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-451">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="76bfd-451">Value Name:</span></span> 
  - <span data-ttu-id="76bfd-452">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="76bfd-452">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="76bfd-453">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="76bfd-453">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="76bfd-454">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="76bfd-454">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="76bfd-455">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-455">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-456">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-456">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="76bfd-457">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-457">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="proxy-server-policies"></a><span data-ttu-id="76bfd-458">Directivas de servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-458">Proxy Server policies</span></span>

[<span data-ttu-id="76bfd-459">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-459">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="proxymode"></a><span data-ttu-id="76bfd-460">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="76bfd-460">ProxyMode</span></span>
#### <a name="choose-how-to-specify-proxy-server-settings"></a><span data-ttu-id="76bfd-461">Elegir cómo especificar la configuración del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-461">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="76bfd-462">Microsoft Edge Update 1.3.21.81 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-462">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-463">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-463">Description</span></span>
<span data-ttu-id="76bfd-464">Permite especificar la configuración del servidor proxy que usa Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="76bfd-464">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="76bfd-465">Si habilitas esta directiva, puedes elegir entre las siguientes opciones de servidor proxy:</span><span class="sxs-lookup"><span data-stu-id="76bfd-465">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="76bfd-466">Si eliges no usar nunca un servidor proxy y siempre te conectas directamente, se ignora el resto de opciones.</span><span class="sxs-lookup"><span data-stu-id="76bfd-466">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="76bfd-467">Si elige usar la configuración proxy del sistema o detectar automáticamente el servidor proxy, se ignora el resto de opciones.</span><span class="sxs-lookup"><span data-stu-id="76bfd-467">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="76bfd-468">Si eliges el modo de servidor proxy fijo, puedes especificar más opciones en '[Dirección o dirección URL del servidor proxy](#proxyserver)'.</span><span class="sxs-lookup"><span data-stu-id="76bfd-468">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="76bfd-469">Si decides usar un script de proxy .pac, debes especificar la dirección URL del script en '[Dirección URL de un archivo de proxy .pac](#proxypacurl)'.</span><span class="sxs-lookup"><span data-stu-id="76bfd-469">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="76bfd-470">Si habilitas esta directiva, los usuarios de la organización no pueden cambiar la configuración de proxy en Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="76bfd-470">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="76bfd-471">Si deshabilitas o no configuras esta directiva, no se configuran las opciones del servidor proxy, pero los usuarios de la organización pueden elegir su propia configuración de proxy para Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="76bfd-471">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-472">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-472">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-473">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-473">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-474">Nombre único de GP: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="76bfd-474">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="76bfd-475">Nombre de GP: elige cómo especificar la configuración del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-475">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="76bfd-476">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-476">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="76bfd-477">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-477">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-478">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-478">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-479">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-479">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-480">Nombre del valor: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="76bfd-480">Value Name: ProxyMode</span></span>
- <span data-ttu-id="76bfd-481">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="76bfd-481">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-482">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-482">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="76bfd-483">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-483">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxypacurl"></a><span data-ttu-id="76bfd-484">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="76bfd-484">ProxyPacUrl</span></span>
#### <a name="url-to-a-proxy-pac-file"></a><span data-ttu-id="76bfd-485">Dirección URL a un archivo proxy .pac</span><span class="sxs-lookup"><span data-stu-id="76bfd-485">URL to a proxy .pac file</span></span>
><span data-ttu-id="76bfd-486">Microsoft Edge Update 1.3.21.81 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-486">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-487">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-487">Description</span></span>
<span data-ttu-id="76bfd-488">Permite especificar una dirección URL para un archivo de configuración automática de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="76bfd-488">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="76bfd-489">Si habilitas esta directiva, puedes especificar una dirección URL para un archivo PAC que automatice cómo Microsoft Edge Update selecciona el servidor proxy adecuado para localizar un sitio web en particular.</span><span class="sxs-lookup"><span data-stu-id="76bfd-489">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="76bfd-490">Esta directiva solo se aplica si has especificado una configuración de proxy manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="76bfd-490">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="76bfd-491">No configures esta directiva si has especificado una configuración de proxy diferente de manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="76bfd-491">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-492">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-492">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-493">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-493">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-494">Nombre único de GP: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="76bfd-494">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="76bfd-495">Nombre de GP: dirección URL a un archivo proxy .pac</span><span class="sxs-lookup"><span data-stu-id="76bfd-495">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="76bfd-496">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-496">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="76bfd-497">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-497">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-498">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-498">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-499">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-499">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-500">Nombre del valor: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="76bfd-500">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="76bfd-501">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="76bfd-501">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-502">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-502">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="76bfd-503">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-503">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxyserver"></a><span data-ttu-id="76bfd-504">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="76bfd-504">ProxyServer</span></span>
#### <a name="address-or-url-of-proxy-server"></a><span data-ttu-id="76bfd-505">Dirección o dirección URL del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-505">Address or URL of proxy server</span></span>
><span data-ttu-id="76bfd-506">Microsoft Edge Update 1.3.21.81 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-506">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-507">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-507">Description</span></span>
<span data-ttu-id="76bfd-508">Permite especificar la dirección URL del servidor proxy que usa Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="76bfd-508">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="76bfd-509">Si habilitas esta directiva, puedes establecer la dirección URL del servidor proxy usado por Microsoft Edge Update en tu organización.</span><span class="sxs-lookup"><span data-stu-id="76bfd-509">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="76bfd-510">Esta directiva solo se aplica si has seleccionado una configuración de proxy manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="76bfd-510">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="76bfd-511">No configures esta directiva si has especificado una configuración de proxy diferente de manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="76bfd-511">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-512">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-512">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-513">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-513">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-514">Nombre único de GP: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="76bfd-514">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="76bfd-515">Nombre de GP: dirección o dirección URL del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-515">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="76bfd-516">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="76bfd-516">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="76bfd-517">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-517">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-518">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-518">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-519">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-519">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-520">Nombre del valor: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="76bfd-520">Value Name: ProxyServer</span></span>
- <span data-ttu-id="76bfd-521">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="76bfd-521">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-522">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-522">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="76bfd-523">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-523">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="microsoft-edge-webview-policies"></a><span data-ttu-id="76bfd-524">Directivas de Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="76bfd-524">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="76bfd-525">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-525">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="install-webview"></a><span data-ttu-id="76bfd-526">Instalar (WebView)</span><span class="sxs-lookup"><span data-stu-id="76bfd-526">Install (WebView)</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="76bfd-527">Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-527">Allow installation</span></span>
><span data-ttu-id="76bfd-528">Microsoft Edge Update 1.3.127.1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-528">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-529">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-529">Description</span></span>
<span data-ttu-id="76bfd-530">Le permite especificar si Microsoft Edge WebView se puede instalar con Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="76bfd-530">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="76bfd-531">Si habilita esta directiva, los usuarios pueden instalar Microsoft Edge WebView con Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="76bfd-531">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="76bfd-532">Si deshabilita esta directiva, los usuarios no pueden instalar Microsoft Edge WebView con Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="76bfd-532">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="76bfd-533">Si no configura esta directiva, la configuración de la directiva del "[Valor predeterminado de Permitir instalación](#installdefault)" determinará si los usuarios pueden instalar Microsoft Edge WebView con Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="76bfd-533">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-534">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-534">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-535">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-535">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-536">Nombre único de GP: Install</span><span class="sxs-lookup"><span data-stu-id="76bfd-536">GP unique name: Install</span></span>
- <span data-ttu-id="76bfd-537">Nombre de GP: Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="76bfd-537">GP name: Allow installation</span></span>
- <span data-ttu-id="76bfd-538">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="76bfd-538">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="76bfd-539">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-539">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-540">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-540">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-541">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-541">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-542">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="76bfd-542">Value Name:</span></span> 
  - <span data-ttu-id="76bfd-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="76bfd-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="76bfd-544">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-544">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-545">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-545">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="76bfd-546">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-546">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update-webview"></a><span data-ttu-id="76bfd-547">Actualización (WebView)</span><span class="sxs-lookup"><span data-stu-id="76bfd-547">Update (WebView)</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="76bfd-548">Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-548">Update policy override</span></span>
><span data-ttu-id="76bfd-549">Microsoft Edge Update 1.3.127.1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="76bfd-549">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="76bfd-550">Descripción</span><span class="sxs-lookup"><span data-stu-id="76bfd-550">Description</span></span>
<span data-ttu-id="76bfd-551">Te permite especificar si las actualizaciones automáticas están habilitadas para Microsoft Edge WebView.</span><span class="sxs-lookup"><span data-stu-id="76bfd-551">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="76bfd-552">Microsoft Edge WebView es un componente usado por las aplicaciones para mostrar contenido web.</span><span class="sxs-lookup"><span data-stu-id="76bfd-552">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="76bfd-553">Las actualizaciones automáticas están habilitadas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="76bfd-553">Automatic updates are enabled by default.</span></span> <span data-ttu-id="76bfd-554">Al deshabilitar las actualizaciones automáticas de Microsoft Edge WebView, se pueden producir problemas de compatibilidad con las aplicaciones que dependen de este componente.</span><span class="sxs-lookup"><span data-stu-id="76bfd-554">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="76bfd-555">Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge WebView de acuerdo con la configuración de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="76bfd-555">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="76bfd-556">Permitir siempre las actualizaciones: las actualizaciones se descargan y aplican automáticamente</span><span class="sxs-lookup"><span data-stu-id="76bfd-556">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="76bfd-557">Actualizaciones deshabilitadas: las actualizaciones nunca se descargan ni aplican</span><span class="sxs-lookup"><span data-stu-id="76bfd-557">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="76bfd-558">Si no habilitas esta directiva, las actualizaciones se descargan y se aplican automáticamente.</span><span class="sxs-lookup"><span data-stu-id="76bfd-558">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="76bfd-559">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-559">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="76bfd-560">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="76bfd-560">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="76bfd-561">Nombre único de GP: Actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-561">GP unique name: Update</span></span>
- <span data-ttu-id="76bfd-562">Nombre de GP: Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="76bfd-562">GP name: Update policy override</span></span>
- <span data-ttu-id="76bfd-563">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="76bfd-563">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="76bfd-564">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="76bfd-564">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="76bfd-565">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="76bfd-565">Windows Registry Settings</span></span>
- <span data-ttu-id="76bfd-566">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="76bfd-566">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="76bfd-567">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="76bfd-567">Value Name:</span></span> 
  - <span data-ttu-id="76bfd-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="76bfd-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="76bfd-569">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="76bfd-569">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="76bfd-570">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76bfd-570">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="76bfd-571">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="76bfd-571">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="see-also"></a><span data-ttu-id="76bfd-572">Consulte también</span><span class="sxs-lookup"><span data-stu-id="76bfd-572">See also</span></span>
  - [<span data-ttu-id="76bfd-573">Configuración de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76bfd-573">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="76bfd-574">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="76bfd-574">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
