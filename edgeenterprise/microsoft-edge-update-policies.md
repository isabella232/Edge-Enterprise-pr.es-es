---
title: Documentación de directiva de Microsoft Edge Update
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 10/07/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentación de todas las directivas admitidas por Microsoft Edge Update
ms.openlocfilehash: feb7859f062ae39e2bbfe08d8e478386defb85cf
ms.sourcegitcommit: 4e6188ade942ca6fd599a4ce1c8e0d90d3d03399
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2020
ms.locfileid: "11105574"
---
# <span data-ttu-id="8bee3-103">Microsoft Edge: Directivas de actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-103">Microsoft Edge - Update policies</span></span>
<span data-ttu-id="8bee3-104">La última versión de Microsoft Edge incluye las siguientes directivas que puedes usar para controlar cómo y cuándo se actualiza Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="8bee3-105">Para obtener información sobre otras directivas disponibles en Microsoft Edge, consulta la [referencia de directiva del explorador Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="8bee3-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="8bee3-106">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="8bee3-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <span data-ttu-id="8bee3-107">Directivas disponibles</span><span class="sxs-lookup"><span data-stu-id="8bee3-107">Available policies</span></span>
<span data-ttu-id="8bee3-108">Estas tablas enumeran todas las directivas de grupo relacionadas con la actualización disponibles en esta versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="8bee3-109">Usa los vínculos de la tabla para obtener más detalles sobre directivas específicas.</span><span class="sxs-lookup"><span data-stu-id="8bee3-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="8bee3-110">Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8bee3-110">Applications</span></span>](#applications)|[<span data-ttu-id="8bee3-111">Preferencias</span><span class="sxs-lookup"><span data-stu-id="8bee3-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="8bee3-112">Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-112">Proxy Server</span></span>](#proxy-server)|[<span data-ttu-id="8bee3-113">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="8bee3-113">Microsoft Edge WebView</span></span>](#microsoft-edge-webview)|

### [<span data-ttu-id="8bee3-114">Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8bee3-114">Applications</span></span>](#applications-policies)
|<span data-ttu-id="8bee3-115">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="8bee3-115">Policy Name</span></span>|<span data-ttu-id="8bee3-116">Título</span><span class="sxs-lookup"><span data-stu-id="8bee3-116">Caption</span></span>|
|-|-|
|[<span data-ttu-id="8bee3-117">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-117">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="8bee3-118">Valor predeterminado de Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-118">Allow installation default</span></span>|
|[<span data-ttu-id="8bee3-119">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-119">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="8bee3-120">Valor predeterminado de Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-120">Update policy override default</span></span>|
|[<span data-ttu-id="8bee3-121">Instalar</span><span class="sxs-lookup"><span data-stu-id="8bee3-121">Install</span></span>](#install)|<span data-ttu-id="8bee3-122">Permitir instalación (por canal)</span><span class="sxs-lookup"><span data-stu-id="8bee3-122">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="8bee3-123">Actualizar</span><span class="sxs-lookup"><span data-stu-id="8bee3-123">Update</span></span>](#update)|<span data-ttu-id="8bee3-124">Invalidar directiva de actualización (por canal)</span><span class="sxs-lookup"><span data-stu-id="8bee3-124">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="8bee3-125">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="8bee3-125">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="8bee3-126">Permitir la experiencia de exploradores Microsoft Edge en paralelo</span><span class="sxs-lookup"><span data-stu-id="8bee3-126">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="8bee3-127">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-127">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="8bee3-128">Impedir la creación de accesos directos de escritorio durante la instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="8bee3-128">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="8bee3-129">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="8bee3-129">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="8bee3-130">Impedir la creación de accesos directos de escritorio durante la instalación (por canal)</span><span class="sxs-lookup"><span data-stu-id="8bee3-130">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="8bee3-131">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="8bee3-131">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="8bee3-132">Revertir a la versión de destino (por canal)</span><span class="sxs-lookup"><span data-stu-id="8bee3-132">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="8bee3-133">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="8bee3-133">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="8bee3-134">Invalidación de versión de destino (por canal)</span><span class="sxs-lookup"><span data-stu-id="8bee3-134">Target version override (per channel)</span></span>|

### [<span data-ttu-id="8bee3-135">Preferencias</span><span class="sxs-lookup"><span data-stu-id="8bee3-135">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="8bee3-136">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="8bee3-136">Policy Name</span></span>|<span data-ttu-id="8bee3-137">Título</span><span class="sxs-lookup"><span data-stu-id="8bee3-137">Caption</span></span>|
|-|-|
|[<span data-ttu-id="8bee3-138">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="8bee3-138">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="8bee3-139">invalidar el período de buscar actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="8bee3-139">Auto-update check period override</span></span>|
|[<span data-ttu-id="8bee3-140">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="8bee3-140">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="8bee3-141">Período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="8bee3-141">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="8bee3-142">Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-142">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="8bee3-143">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="8bee3-143">Policy Name</span></span>|<span data-ttu-id="8bee3-144">Leyenda</span><span class="sxs-lookup"><span data-stu-id="8bee3-144">Caption</span></span>|
|-|-|
|[<span data-ttu-id="8bee3-145">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="8bee3-145">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="8bee3-146">Elegir cómo especificar la configuración del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-146">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="8bee3-147">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="8bee3-147">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="8bee3-148">Dirección URL a un archivo proxy .pac</span><span class="sxs-lookup"><span data-stu-id="8bee3-148">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="8bee3-149">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="8bee3-149">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="8bee3-150">Dirección o dirección URL del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-150">Address or URL of proxy server</span></span>|

### [<span data-ttu-id="8bee3-151">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="8bee3-151">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="8bee3-152">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="8bee3-152">Policy Name</span></span>|<span data-ttu-id="8bee3-153">Título</span><span class="sxs-lookup"><span data-stu-id="8bee3-153">Caption</span></span>|
|-|-|
|[<span data-ttu-id="8bee3-154">Instalar</span><span class="sxs-lookup"><span data-stu-id="8bee3-154">Install</span></span>](#install-webview)|<span data-ttu-id="8bee3-155">Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-155">Allow installation</span></span>|
|[<span data-ttu-id="8bee3-156">Actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-156">Update</span></span>](#update-webview)|<span data-ttu-id="8bee3-157">Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-157">Update policy override</span></span>|

## <span data-ttu-id="8bee3-158">Directivas de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8bee3-158">Applications policies</span></span>

[<span data-ttu-id="8bee3-159">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-159">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="8bee3-160">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-160">InstallDefault</span></span>
#### <span data-ttu-id="8bee3-161">Valor predeterminado de Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-161">Allow installation default</span></span>
><span data-ttu-id="8bee3-162">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-162">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="8bee3-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-163">Description</span></span>
<span data-ttu-id="8bee3-164">Puede especificar el comportamiento predeterminado de todos los canales para permitir o bloquear Microsoft Edge en dispositivos unidos al dominio.</span><span class="sxs-lookup"><span data-stu-id="8bee3-164">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="8bee3-165">Puede reemplazar esta directiva para canales individuales si habilita la directiva [Permitir instalación](#install) para canales específicos.</span><span class="sxs-lookup"><span data-stu-id="8bee3-165">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="8bee3-166">Si deshabilita esta directiva, se bloquea la instalación de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-166">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="8bee3-167">Esto solo afecta a la instalación de software de Microsoft Edge cuando la directiva "[Permitir instalación](#install)" está establecida en No configurada.</span><span class="sxs-lookup"><span data-stu-id="8bee3-167">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="8bee3-168">Esta directiva no impide que se ejecute Microsoft Edge Update ni impide que los usuarios instalen software de Microsoft Edge con otros métodos.</span><span class="sxs-lookup"><span data-stu-id="8bee3-168">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="8bee3-169">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="8bee3-169">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="8bee3-170">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-170">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-171">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-171">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-172">Nombre único de GP: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-172">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="8bee3-173">Nombre de GP: valor predeterminado de Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-173">GP name: Allow installation default</span></span>
- <span data-ttu-id="8bee3-174">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8bee3-174">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="8bee3-175">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-175">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-176">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-176">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-177">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-177">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-178">Nombre de valor: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-178">Value Name: InstallDefault</span></span>
- <span data-ttu-id="8bee3-179">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-179">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-180">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-180">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="8bee3-181">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-181">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-182">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-182">UpdateDefault</span></span>
#### <span data-ttu-id="8bee3-183">Valor predeterminado de Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-183">Update policy override default</span></span>
><span data-ttu-id="8bee3-184">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-184">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="8bee3-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-185">Description</span></span>
<span data-ttu-id="8bee3-186">Permite especificar el comportamiento predeterminado de todos los canales relacionados con la manera en que Microsoft Edge Update trata las actualizaciones disponibles para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-186">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="8bee3-187">Se puede invalidar para canales individuales especificando la directiva '[Invalidar directiva de actualización](#update)' para esos canales específicos.</span><span class="sxs-lookup"><span data-stu-id="8bee3-187">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="8bee3-188">Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge de acuerdo con la configuración de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="8bee3-188">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="8bee3-189">Permitir siempre las actualizaciones: las actualizaciones siempre se aplican cuando se encuentran, ya sea mediante la búsqueda de actualizaciones periódicas o mediante una búsqueda de actualizaciones manual.</span><span class="sxs-lookup"><span data-stu-id="8bee3-189">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="8bee3-190">Solo actualizaciones silenciosas automáticas: las actualizaciones solo se aplican cuando las encuentra la búsqueda periódica de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="8bee3-190">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="8bee3-191">Solo actualizaciones manuales: las actualizaciones se aplican solo cuando el usuario ejecuta una búsqueda manual de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="8bee3-191">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="8bee3-192">Actualizaciones deshabilitadas: las actualizaciones nunca se aplican.</span><span class="sxs-lookup"><span data-stu-id="8bee3-192">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="8bee3-193">Si seleccionas las actualizaciones manuales, asegúrate de buscar periódicamente actualizaciones mediante el mecanismo de actualización manual de la aplicación, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="8bee3-193">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="8bee3-194">Si deshabilitas las actualizaciones, comprueba periódicamente si las hay y distribúyelas a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="8bee3-194">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="8bee3-195">Si no habilitas ni configuras esta directiva, Microsoft Edge Update administra las actualizaciones disponibles según se especifica en la directiva '[Invalidar directiva de actualizaciones](#update)'.</span><span class="sxs-lookup"><span data-stu-id="8bee3-195">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="8bee3-196">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="8bee3-196">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="8bee3-197">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-197">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-198">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-198">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-199">Nombre único de GP: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-199">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="8bee3-200">Nombre de GP: Valor predeterminado de Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-200">GP name: Update policy override default</span></span>
- <span data-ttu-id="8bee3-201">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8bee3-201">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="8bee3-202">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-202">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-203">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-203">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-204">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-204">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-205">Nombre de valor: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-205">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="8bee3-206">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-206">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-207">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-207">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="8bee3-208">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-208">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-209">Instalar</span><span class="sxs-lookup"><span data-stu-id="8bee3-209">Install</span></span>
#### <span data-ttu-id="8bee3-210">Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-210">Allow installation</span></span>
><span data-ttu-id="8bee3-211">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-211">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="8bee3-212">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-212">Description</span></span>
<span data-ttu-id="8bee3-213">Especifica si se puede instalar un canal de Microsoft Edge en dispositivos unidos al dominio.</span><span class="sxs-lookup"><span data-stu-id="8bee3-213">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="8bee3-214">Si habilita esta directiva para un canal, no se bloqueará la instalación de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-214">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="8bee3-215">Si deshabilita esta directiva para un canal, se bloqueará la instalación de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-215">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="8bee3-216">Si no configura esta directiva para un canal, la configuración de la directiva "[Valor predeterminado de Permitir instalación](#installdefault)" determinará si los usuarios pueden instalar dicho canal de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-216">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="8bee3-217">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="8bee3-217">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="8bee3-218">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-218">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-219">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-219">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-220">Nombre único de GP: Install</span><span class="sxs-lookup"><span data-stu-id="8bee3-220">GP unique name: Install</span></span>
- <span data-ttu-id="8bee3-221">Nombre de GP: Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-221">GP name: Allow installation</span></span>
- <span data-ttu-id="8bee3-222">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="8bee3-222">GP path:</span></span> 
  - <span data-ttu-id="8bee3-223">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8bee3-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="8bee3-224">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="8bee3-224">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="8bee3-225">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="8bee3-225">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="8bee3-226">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="8bee3-226">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="8bee3-227">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-227">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-228">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-228">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-229">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-229">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-230">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="8bee3-230">Value Name:</span></span> 
  - <span data-ttu-id="8bee3-231">(Estable): instalar{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="8bee3-231">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="8bee3-232">(Beta): instalar{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="8bee3-232">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="8bee3-233">(Canarias): instalar{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="8bee3-233">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="8bee3-234">(Dev): instalar{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="8bee3-234">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="8bee3-235">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-235">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-236">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-236">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="8bee3-237">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-237">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-238">Actualizar</span><span class="sxs-lookup"><span data-stu-id="8bee3-238">Update</span></span>
#### <span data-ttu-id="8bee3-239">Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-239">Update policy override</span></span>
><span data-ttu-id="8bee3-240">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-240">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="8bee3-241">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-241">Description</span></span>
<span data-ttu-id="8bee3-242">Especifica cómo trata Microsoft Edge Update las actualizaciones disponibles de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-242">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="8bee3-243">Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge de acuerdo con la configuración de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="8bee3-243">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="8bee3-244">Permitir siempre las actualizaciones: las actualizaciones siempre se aplican cuando se encuentran, ya sea mediante la búsqueda de actualizaciones periódicas o mediante una búsqueda de actualizaciones manual.</span><span class="sxs-lookup"><span data-stu-id="8bee3-244">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="8bee3-245">Solo actualizaciones silenciosas automáticas: las actualizaciones solo se aplican cuando las encuentra la búsqueda periódica de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="8bee3-245">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="8bee3-246">Solo actualizaciones manuales: las actualizaciones se aplican solo cuando el usuario ejecuta una búsqueda manual de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="8bee3-246">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="8bee3-247">(No todas las aplicaciones ofrecen una interfaz para esta opción).</span><span class="sxs-lookup"><span data-stu-id="8bee3-247">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="8bee3-248">Actualizaciones deshabilitadas: las actualizaciones nunca se aplican.</span><span class="sxs-lookup"><span data-stu-id="8bee3-248">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="8bee3-249">Si seleccionas las actualizaciones manuales, asegúrate de buscar periódicamente actualizaciones mediante el mecanismo de actualización manual de la aplicación, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="8bee3-249">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="8bee3-250">Si deshabilitas las actualizaciones, comprueba periódicamente si las hay y distribúyelas a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="8bee3-250">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="8bee3-251">Si no habilitas ni configuras esta directiva, Microsoft Edge Update administra las actualizaciones disponibles según se especifica en la directiva '[Valor predeterminado de Invalidar directiva de actualizaciones](#updatedefault)'.</span><span class="sxs-lookup"><span data-stu-id="8bee3-251">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="8bee3-252">Vea [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8bee3-252">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="8bee3-253">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="8bee3-253">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="8bee3-254">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-254">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-255">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-255">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-256">Nombre único de GP: Actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-256">GP unique name: Update</span></span>
- <span data-ttu-id="8bee3-257">Nombre de GP: Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-257">GP name: Update policy override</span></span>
- <span data-ttu-id="8bee3-258">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="8bee3-258">GP path:</span></span> 
  - <span data-ttu-id="8bee3-259">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8bee3-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="8bee3-260">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="8bee3-260">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="8bee3-261">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="8bee3-261">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="8bee3-262">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="8bee3-262">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="8bee3-263">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-263">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-264">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-264">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-265">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-265">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-266">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="8bee3-266">Value Name:</span></span> 
  - <span data-ttu-id="8bee3-267">(Estable): actualizar{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="8bee3-267">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="8bee3-268">(Beta): actualizar{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="8bee3-268">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="8bee3-269">(Canarias): actualizar{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="8bee3-269">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="8bee3-270">(Dev): actualizar{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="8bee3-270">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="8bee3-271">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-271">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-272">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-272">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="8bee3-273">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-273">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-274">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="8bee3-274">Allowsxs</span></span>
#### <span data-ttu-id="8bee3-275">Permitir la experiencia de exploradores Microsoft Edge en paralelo</span><span class="sxs-lookup"><span data-stu-id="8bee3-275">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="8bee3-276">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-276">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="8bee3-277">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-277">Description</span></span>
<span data-ttu-id="8bee3-278">Esta directiva permite a un usuario ejecutar Microsoft Edge (Edge HTML) y Microsoft Edge (basado en Chromium) en paralelo.</span><span class="sxs-lookup"><span data-stu-id="8bee3-278">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="8bee3-279">Si esta directiva se establece en “No configurado”, Microsoft Edge (basado en Chromium) reemplazará a Microsoft Edge (Edge HTML) después del canal estable de Microsoft Edge (basado en Chromium) y se instalarán las actualizaciones de seguridad de noviembre de 2019.</span><span class="sxs-lookup"><span data-stu-id="8bee3-279">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="8bee3-280">Este es el mismo comportamiento que la opción “Deshabilitado”.</span><span class="sxs-lookup"><span data-stu-id="8bee3-280">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="8bee3-281">La opción “Deshabilitado” bloquea la experiencia en paralelo y Microsoft Edge (basado en Chromium) reemplazará a Microsoft Edge (Edge HTML) después del canal estable de Microsoft Edge (basado en Chromium) y se instalarán las actualizaciones de seguridad de noviembre de 2019.</span><span class="sxs-lookup"><span data-stu-id="8bee3-281">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="8bee3-282">Este es el mismo comportamiento que la opción “No configurado”.</span><span class="sxs-lookup"><span data-stu-id="8bee3-282">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="8bee3-283">Cuando esta directiva está “Habilitada”, se pueden ejecutar en paralelo Microsoft Edge (Edge HTML) y Microsoft Edge (basado en Chromium) después de instalado Microsoft Edge (basado en Chromium).</span><span class="sxs-lookup"><span data-stu-id="8bee3-283">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="8bee3-284">Para que esta directiva de grupo surta efecto, debe configurarse antes de la instalación automática de Microsoft Edge (basado en Chromium) por parte de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="8bee3-284">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="8bee3-285">Nota: un usuario puede bloquear la actualización automática de Microsoft Edge (basado en Chromium) mediante el kit de herramientas de bloqueo de Microsoft Edge (basado en Chromium).</span><span class="sxs-lookup"><span data-stu-id="8bee3-285">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="8bee3-286">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-286">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-287">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-287">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-288">Nombre único de GP: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="8bee3-288">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="8bee3-289">Nombre de GP: permitir la experiencia en paralelo de exploradores Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8bee3-289">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="8bee3-290">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8bee3-290">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="8bee3-291">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-291">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-292">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-292">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-293">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-293">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-294">Nombre del valor: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="8bee3-294">Value Name: Allowsxs</span></span>
- <span data-ttu-id="8bee3-295">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-295">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-296">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-296">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="8bee3-297">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-297">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-298">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-298">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="8bee3-299">Impedir la creación de accesos directos de escritorio durante la instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="8bee3-299">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="8bee3-300">Microsoft Edge Update 1.3.128.0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-300">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="8bee3-301">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-301">Description</span></span>
<span data-ttu-id="8bee3-302">Permite especificar el comportamiento predeterminado de todos los canales para crear un acceso directo en el escritorio cuando se instala Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-302">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="8bee3-303">Si habilita esta directiva, se creará un acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-303">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="8bee3-304">Si deshabilita esta directiva, no se creará ningún acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-304">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="8bee3-305">Si no configura esta directiva, se creará un acceso directo de escritorio a Microsoft Edge durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="8bee3-305">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="8bee3-306">Si Microsoft Edge ya está instalado, esta directiva no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="8bee3-306">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="8bee3-307">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-307">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-308">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-308">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-309">Nombre único de GP: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-309">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="8bee3-310">Nombre de GP: configuración predeterminada para impedir la creación de accesos directos de escritorio durante la instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-310">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="8bee3-311">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8bee3-311">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="8bee3-312">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-312">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-313">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-313">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-314">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-314">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-315">Nombre del valor: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="8bee3-315">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="8bee3-316">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-316">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-317">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-317">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="8bee3-318">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-318">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-319">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="8bee3-319">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="8bee3-320">Impedir la creación de accesos directos de escritorio durante la instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-320">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="8bee3-321">Microsoft Edge Update 1.3.128.0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-321">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="8bee3-322">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-322">Description</span></span>
<span data-ttu-id="8bee3-323">Si habilita esta directiva, se creará un acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-323">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="8bee3-324">Si deshabilita esta directiva, no se creará ningún acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-324">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="8bee3-325">Si no configura esta directiva, se creará un acceso directo de escritorio a Microsoft Edge durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="8bee3-325">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="8bee3-326">Si Microsoft Edge ya está instalado, esta directiva no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="8bee3-326">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="8bee3-327">Si no configura esta directiva para un canal, la configuración de directiva '[Impedir la creación de accesos directos de escritorio durante la instalación predeterminada](#createdesktopshortcutdefault)' determina la creación de accesos directos cuando se instala Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-327">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="8bee3-328">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-328">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-329">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-329">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-330">Nombre único de GP: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="8bee3-330">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="8bee3-331">Nombre de GP: impedir la creación de métodos abreviados de escritorio durante la instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-331">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="8bee3-332">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="8bee3-332">GP path:</span></span> 
  - <span data-ttu-id="8bee3-333">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8bee3-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="8bee3-334">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="8bee3-334">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="8bee3-335">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="8bee3-335">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="8bee3-336">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="8bee3-336">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="8bee3-337">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-337">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-338">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-338">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-339">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-339">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-340">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="8bee3-340">Value Name:</span></span> 
  - <span data-ttu-id="8bee3-341">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="8bee3-341">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="8bee3-342">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="8bee3-342">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="8bee3-343">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="8bee3-343">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="8bee3-344">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="8bee3-344">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="8bee3-345">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-345">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-346">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-346">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="8bee3-347">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-347">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-348">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="8bee3-348">RollbackToTargetVersion</span></span>
#### <span data-ttu-id="8bee3-349">Revertir a la versión de destino</span><span class="sxs-lookup"><span data-stu-id="8bee3-349">Rollback to Target version</span></span>
><span data-ttu-id="8bee3-350">Microsoft Edge Update 1.3.133.3 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-350">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <span data-ttu-id="8bee3-351">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-351">Description</span></span>
<span data-ttu-id="8bee3-352">Especifica que Microsoft Edge Update debe revertir las instalaciones de Microsoft Edge a la versión que se indica en "[Invalidación de la versión de destino](#targetversionprefix)".</span><span class="sxs-lookup"><span data-stu-id="8bee3-352">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="8bee3-353">Esta directiva no surte efecto a menos que "[Invalidación de la versión de destino](#targetversionprefix)" e "[Invalidación de la directiva de actualización](#update)" se establezcan en uno de los estados activados (es decir, Permitir siempre las actualizaciones, Solo actualizaciones silenciosas automáticas o Solo actualizaciones manuales).</span><span class="sxs-lookup"><span data-stu-id="8bee3-353">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="8bee3-354">Si deshabilita esta directiva o no la configura, las instalaciones que tengan una versión superior a la especificada por la "[Invalidación de la versión de destino](#targetversionprefix)" quedarán tal cual están.</span><span class="sxs-lookup"><span data-stu-id="8bee3-354">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="8bee3-355">Si habilita esta directiva, las instalaciones que tengan una versión actual superior a la especificada por la "[Invalidación de la versión de destino](#targetversionprefix)" serán degradadas a la versión de destino.</span><span class="sxs-lookup"><span data-stu-id="8bee3-355">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="8bee3-356">Se recomienda a los usuarios que instalen la última versión del explorador Microsoft Edge para estar seguros de contar con la protección que proporcionan las últimas actualizaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8bee3-356">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="8bee3-357">Revertir a una versión anterior supone un riesgo de exposición a problemas de seguridad conocidos.</span><span class="sxs-lookup"><span data-stu-id="8bee3-357">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="8bee3-358">Esta directiva está pensada para usarse como una solución provisional para resolver problemas relacionados con una actualización del explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bee3-358">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="8bee3-359">Antes de revertir temporalmente a la versión anterior del explorador, recomendamos activar la sincronización ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) para todos los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="8bee3-359">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="8bee3-360">Si no se activa la sincronización, se corre el riesgo de pérdida definitiva de datos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8bee3-360">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="8bee3-361">Utilice esta directiva bajo su propia responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="8bee3-361">Use this policy at your own risk.</span></span>

<span data-ttu-id="8bee3-362">Nota: todas las versiones disponibles para la reversión se pueden ver aquí [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="8bee3-362">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="8bee3-363">Esta directiva se aplica a Microsoft Edge, versión 86 o posterior.</span><span class="sxs-lookup"><span data-stu-id="8bee3-363">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="8bee3-364">Vea [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8bee3-364">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="8bee3-365">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="8bee3-365">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="8bee3-366">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-366">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-367">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-367">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-368">Nombre único de GP: RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="8bee3-368">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="8bee3-369">Nombre de GP: Revertir a la versión de destino</span><span class="sxs-lookup"><span data-stu-id="8bee3-369">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="8bee3-370">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="8bee3-370">GP path:</span></span> 
  - <span data-ttu-id="8bee3-371">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8bee3-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="8bee3-372">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="8bee3-372">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="8bee3-373">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="8bee3-373">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="8bee3-374">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="8bee3-374">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="8bee3-375">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-375">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-376">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-376">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-377">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-378">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="8bee3-378">Value Name:</span></span> 
  - <span data-ttu-id="8bee3-379">(Estable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="8bee3-379">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="8bee3-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="8bee3-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="8bee3-381">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="8bee3-381">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="8bee3-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="8bee3-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="8bee3-383">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-383">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-384">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-384">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="8bee3-385">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-385">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-386">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="8bee3-386">TargetVersionPrefix</span></span>
#### <span data-ttu-id="8bee3-387">Invalidación de versión de destino</span><span class="sxs-lookup"><span data-stu-id="8bee3-387">Target version override</span></span>
><span data-ttu-id="8bee3-388">Microsoft Edge Update 1.3.119.43 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-388">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="8bee3-389">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-389">Description</span></span>
<span data-ttu-id="8bee3-390">Cuando se habilita esta directiva y la actualización automática está habilitada, Microsoft Edge se actualizará a la versión especificada por este valor de directiva.</span><span class="sxs-lookup"><span data-stu-id="8bee3-390">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="8bee3-391">El valor de directiva debe ser una versión específica de Microsoft Edge, como 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="8bee3-391">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="8bee3-392">Si un dispositivo tiene una versión más reciente de Microsoft Edge que el valor especificado, Microsoft Edge permanecerá en la versión más reciente, mas no desactualizada a la versión especificada.</span><span class="sxs-lookup"><span data-stu-id="8bee3-392">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="8bee3-393">Si la versión especificada no existe o no tiene el formato correcto, Microsoft Edge permanecerá en su versión actual y no se actualizará a versiones futuras de manera automática.</span><span class="sxs-lookup"><span data-stu-id="8bee3-393">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="8bee3-394">Vea [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8bee3-394">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="8bee3-395">Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="8bee3-395">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="8bee3-396">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-396">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-397">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-397">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-398">Nombre único de GP: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="8bee3-398">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="8bee3-399">Nombre de GP: Invalidación de versión de destino</span><span class="sxs-lookup"><span data-stu-id="8bee3-399">GP name: Target version override</span></span>
- <span data-ttu-id="8bee3-400">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="8bee3-400">GP path:</span></span> 
  - <span data-ttu-id="8bee3-401">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8bee3-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="8bee3-402">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="8bee3-402">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="8bee3-403">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="8bee3-403">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="8bee3-404">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="8bee3-404">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="8bee3-405">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-405">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-406">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-406">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-407">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-407">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-408">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="8bee3-408">Value Name:</span></span> 
  - <span data-ttu-id="8bee3-409">(Estable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="8bee3-409">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="8bee3-410">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="8bee3-410">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="8bee3-411">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="8bee3-411">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="8bee3-412">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="8bee3-412">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="8bee3-413">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="8bee3-413">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="8bee3-414">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-414">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="8bee3-415">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-415">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="8bee3-416">Directivas de preferencias</span><span class="sxs-lookup"><span data-stu-id="8bee3-416">Preferences policies</span></span>

[<span data-ttu-id="8bee3-417">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-417">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="8bee3-418">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="8bee3-418">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="8bee3-419">invalidar el período de buscar actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="8bee3-419">Auto-update check period override</span></span>
><span data-ttu-id="8bee3-420">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-420">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="8bee3-421">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-421">Description</span></span>
<span data-ttu-id="8bee3-422">Si se habilita, esta directiva permite establecer un valor para el número mínimo de minutos entre las búsquedas de actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="8bee3-422">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="8bee3-423">De lo contrario, de manera predeterminada, la actualización automática busca actualizaciones cada 10 horas.</span><span class="sxs-lookup"><span data-stu-id="8bee3-423">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="8bee3-424">Si quieres deshabilitar todas las búsquedas de actualizaciones automáticas, establece el valor en 0 (no recomendado).</span><span class="sxs-lookup"><span data-stu-id="8bee3-424">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="8bee3-425">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-425">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-426">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-426">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-427">Nombre único de GP: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="8bee3-427">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="8bee3-428">Nombre de GP: invalidar el período de buscar actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="8bee3-428">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="8bee3-429">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Preferencias</span><span class="sxs-lookup"><span data-stu-id="8bee3-429">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="8bee3-430">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-430">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-431">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-431">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-432">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-432">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-433">Nombre de valor: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="8bee3-433">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="8bee3-434">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-434">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-435">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-435">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="8bee3-436">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-436">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-437">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="8bee3-437">UpdatesSuppressed</span></span>
#### <span data-ttu-id="8bee3-438">Período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="8bee3-438">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="8bee3-439">Microsoft Edge Update 1.3.33.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-439">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="8bee3-440">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-440">Description</span></span>
<span data-ttu-id="8bee3-441">Si habilitas esta Directiva, las búsquedas de actualizaciones se suprimirán cada día, a partir de Hora:Minuto durante un período de tiempo (en minutos).</span><span class="sxs-lookup"><span data-stu-id="8bee3-441">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="8bee3-442">La duración no se ve afectada por el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="8bee3-442">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="8bee3-443">Por ejemplo, si la hora de inicio es 22:00 y la duración es 480 minutos, las actualizaciones se suprimirán durante 8 horas exactamente, independientemente de si el horario de verano comienza o finaliza durante este período.</span><span class="sxs-lookup"><span data-stu-id="8bee3-443">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="8bee3-444">Si deshabilitas o no configuras esta directiva, las búsquedas de actualizaciones no se suprimirán durante ningún período determinado.</span><span class="sxs-lookup"><span data-stu-id="8bee3-444">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="8bee3-445">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-445">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-446">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-446">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-447">Nombre único de GP: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="8bee3-447">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="8bee3-448">Nombre de GP: período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="8bee3-448">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="8bee3-449">Opciones {Hora, Minuto, Duración}</span><span class="sxs-lookup"><span data-stu-id="8bee3-449">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="8bee3-450">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Preferencias</span><span class="sxs-lookup"><span data-stu-id="8bee3-450">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="8bee3-451">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-451">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-452">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-452">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-453">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-453">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-454">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="8bee3-454">Value Name:</span></span> 
  - <span data-ttu-id="8bee3-455">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="8bee3-455">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="8bee3-456">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="8bee3-456">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="8bee3-457">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="8bee3-457">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="8bee3-458">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-458">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-459">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-459">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="8bee3-460">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-460">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="8bee3-461">Directivas de servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-461">Proxy Server policies</span></span>

[<span data-ttu-id="8bee3-462">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-462">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="8bee3-463">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="8bee3-463">ProxyMode</span></span>
#### <span data-ttu-id="8bee3-464">Elegir cómo especificar la configuración del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-464">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="8bee3-465">Microsoft Edge Update 1.3.21.81 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-465">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="8bee3-466">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-466">Description</span></span>
<span data-ttu-id="8bee3-467">Permite especificar la configuración del servidor proxy que usa Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="8bee3-467">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="8bee3-468">Si habilitas esta directiva, puedes elegir entre las siguientes opciones de servidor proxy:</span><span class="sxs-lookup"><span data-stu-id="8bee3-468">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="8bee3-469">Si eliges no usar nunca un servidor proxy y siempre te conectas directamente, se ignora el resto de opciones.</span><span class="sxs-lookup"><span data-stu-id="8bee3-469">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="8bee3-470">Si elige usar la configuración proxy del sistema o detectar automáticamente el servidor proxy, se ignora el resto de opciones.</span><span class="sxs-lookup"><span data-stu-id="8bee3-470">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="8bee3-471">Si eliges el modo de servidor proxy fijo, puedes especificar más opciones en '[Dirección o dirección URL del servidor proxy](#proxyserver)'.</span><span class="sxs-lookup"><span data-stu-id="8bee3-471">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="8bee3-472">Si decides usar un script de proxy .pac, debes especificar la dirección URL del script en '[Dirección URL de un archivo de proxy .pac](#proxypacurl)'.</span><span class="sxs-lookup"><span data-stu-id="8bee3-472">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="8bee3-473">Si habilitas esta directiva, los usuarios de la organización no pueden cambiar la configuración de proxy en Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="8bee3-473">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="8bee3-474">Si deshabilitas o no configuras esta directiva, no se configuran las opciones del servidor proxy, pero los usuarios de la organización pueden elegir su propia configuración de proxy para Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="8bee3-474">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="8bee3-475">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-475">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-476">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-476">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-477">Nombre único de GP: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="8bee3-477">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="8bee3-478">Nombre de GP: elige cómo especificar la configuración del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-478">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="8bee3-479">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-479">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="8bee3-480">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-480">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-481">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-481">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-482">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-482">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-483">Nombre del valor: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="8bee3-483">Value Name: ProxyMode</span></span>
- <span data-ttu-id="8bee3-484">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="8bee3-484">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="8bee3-485">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-485">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="8bee3-486">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-486">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-487">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="8bee3-487">ProxyPacUrl</span></span>
#### <span data-ttu-id="8bee3-488">Dirección URL a un archivo proxy .pac</span><span class="sxs-lookup"><span data-stu-id="8bee3-488">URL to a proxy .pac file</span></span>
><span data-ttu-id="8bee3-489">Microsoft Edge Update 1.3.21.81 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-489">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="8bee3-490">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-490">Description</span></span>
<span data-ttu-id="8bee3-491">Permite especificar una dirección URL para un archivo de configuración automática de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="8bee3-491">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="8bee3-492">Si habilitas esta directiva, puedes especificar una dirección URL para un archivo PAC que automatice cómo Microsoft Edge Update selecciona el servidor proxy adecuado para localizar un sitio web en particular.</span><span class="sxs-lookup"><span data-stu-id="8bee3-492">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="8bee3-493">Esta directiva solo se aplica si has especificado una configuración de proxy manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="8bee3-493">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="8bee3-494">No configures esta directiva si has especificado una configuración de proxy diferente de manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="8bee3-494">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="8bee3-495">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-495">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-496">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-496">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-497">Nombre único de GP: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="8bee3-497">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="8bee3-498">Nombre de GP: dirección URL a un archivo proxy .pac</span><span class="sxs-lookup"><span data-stu-id="8bee3-498">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="8bee3-499">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-499">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="8bee3-500">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-500">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-501">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-501">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-502">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-502">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-503">Nombre del valor: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="8bee3-503">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="8bee3-504">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="8bee3-504">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="8bee3-505">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-505">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="8bee3-506">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-506">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-507">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="8bee3-507">ProxyServer</span></span>
#### <span data-ttu-id="8bee3-508">Dirección o dirección URL del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-508">Address or URL of proxy server</span></span>
><span data-ttu-id="8bee3-509">Microsoft Edge Update 1.3.21.81 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-509">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="8bee3-510">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-510">Description</span></span>
<span data-ttu-id="8bee3-511">Permite especificar la dirección URL del servidor proxy que usa Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="8bee3-511">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="8bee3-512">Si habilitas esta directiva, puedes establecer la dirección URL del servidor proxy usado por Microsoft Edge Update en tu organización.</span><span class="sxs-lookup"><span data-stu-id="8bee3-512">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="8bee3-513">Esta directiva solo se aplica si has seleccionado una configuración de proxy manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="8bee3-513">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="8bee3-514">No configures esta directiva si has especificado una configuración de proxy diferente de manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="8bee3-514">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="8bee3-515">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-515">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-516">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-516">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-517">Nombre único de GP: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="8bee3-517">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="8bee3-518">Nombre de GP: dirección o dirección URL del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-518">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="8bee3-519">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="8bee3-519">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="8bee3-520">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-520">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-521">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-521">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-522">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-522">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-523">Nombre del valor: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="8bee3-523">Value Name: ProxyServer</span></span>
- <span data-ttu-id="8bee3-524">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="8bee3-524">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="8bee3-525">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-525">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="8bee3-526">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-526">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="8bee3-527">Directivas de Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="8bee3-527">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="8bee3-528">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-528">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="8bee3-529">Instalar (WebView)</span><span class="sxs-lookup"><span data-stu-id="8bee3-529">Install (WebView)</span></span>
#### <span data-ttu-id="8bee3-530">Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-530">Allow installation</span></span>
><span data-ttu-id="8bee3-531">Microsoft Edge Update 1.3.127.1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-531">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="8bee3-532">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-532">Description</span></span>
<span data-ttu-id="8bee3-533">Le permite especificar si Microsoft Edge WebView se puede instalar con Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="8bee3-533">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="8bee3-534">Si habilita esta directiva, los usuarios pueden instalar Microsoft Edge WebView con Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="8bee3-534">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="8bee3-535">Si deshabilita esta directiva, los usuarios no pueden instalar Microsoft Edge WebView con Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="8bee3-535">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="8bee3-536">Si no configura esta directiva, la configuración de la directiva del "[Valor predeterminado de Permitir instalación](#installdefault)" determinará si los usuarios pueden instalar Microsoft Edge WebView con Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="8bee3-536">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="8bee3-537">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-537">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-538">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-538">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-539">Nombre único de GP: Install</span><span class="sxs-lookup"><span data-stu-id="8bee3-539">GP unique name: Install</span></span>
- <span data-ttu-id="8bee3-540">Nombre de GP: Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="8bee3-540">GP name: Allow installation</span></span>
- <span data-ttu-id="8bee3-541">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="8bee3-541">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="8bee3-542">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-542">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-543">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-543">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-544">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-544">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-545">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="8bee3-545">Value Name:</span></span> 
  - <span data-ttu-id="8bee3-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="8bee3-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="8bee3-547">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-547">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-548">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-548">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="8bee3-549">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-549">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="8bee3-550">Actualización (WebView)</span><span class="sxs-lookup"><span data-stu-id="8bee3-550">Update (WebView)</span></span>
#### <span data-ttu-id="8bee3-551">Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-551">Update policy override</span></span>
><span data-ttu-id="8bee3-552">Microsoft Edge Update 1.3.127.1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="8bee3-552">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="8bee3-553">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bee3-553">Description</span></span>
<span data-ttu-id="8bee3-554">Te permite especificar si las actualizaciones automáticas están habilitadas para Microsoft Edge WebView.</span><span class="sxs-lookup"><span data-stu-id="8bee3-554">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="8bee3-555">Microsoft Edge WebView es un componente usado por las aplicaciones para mostrar contenido web.</span><span class="sxs-lookup"><span data-stu-id="8bee3-555">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="8bee3-556">Las actualizaciones automáticas están habilitadas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8bee3-556">Automatic updates are enabled by default.</span></span> <span data-ttu-id="8bee3-557">Al deshabilitar las actualizaciones automáticas de Microsoft Edge WebView, se pueden producir problemas de compatibilidad con las aplicaciones que dependen de este componente.</span><span class="sxs-lookup"><span data-stu-id="8bee3-557">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="8bee3-558">Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge WebView de acuerdo con la configuración de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="8bee3-558">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="8bee3-559">Permitir siempre las actualizaciones: las actualizaciones se descargan y aplican automáticamente</span><span class="sxs-lookup"><span data-stu-id="8bee3-559">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="8bee3-560">Actualizaciones deshabilitadas: las actualizaciones nunca se descargan ni aplican</span><span class="sxs-lookup"><span data-stu-id="8bee3-560">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="8bee3-561">Si no habilitas esta directiva, las actualizaciones se descargan y se aplican automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8bee3-561">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <span data-ttu-id="8bee3-562">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-562">Windows information and settings</span></span>
##### <span data-ttu-id="8bee3-563">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="8bee3-563">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="8bee3-564">Nombre único de GP: Actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-564">GP unique name: Update</span></span>
- <span data-ttu-id="8bee3-565">Nombre de GP: Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="8bee3-565">GP name: Update policy override</span></span>
- <span data-ttu-id="8bee3-566">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="8bee3-566">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="8bee3-567">Nombre de archivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="8bee3-567">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="8bee3-568">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="8bee3-568">Windows Registry Settings</span></span>
- <span data-ttu-id="8bee3-569">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="8bee3-569">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="8bee3-570">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="8bee3-570">Value Name:</span></span> 
  - <span data-ttu-id="8bee3-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="8bee3-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="8bee3-572">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="8bee3-572">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="8bee3-573">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8bee3-573">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="8bee3-574">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="8bee3-574">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="8bee3-575">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8bee3-575">See also</span></span>
  - [<span data-ttu-id="8bee3-576">Configuración de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8bee3-576">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="8bee3-577">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="8bee3-577">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)