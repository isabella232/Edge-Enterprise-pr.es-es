---
title: Documentación de directiva de Microsoft Edge Update
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 06/10/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentación de todas las directivas admitidas por Microsoft Edge Update
ms.openlocfilehash: d772d8dd6f60b89e9bd12a77b740e5fad699756a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981162"
---
# <span data-ttu-id="c153d-103">Microsoft Edge: Directivas de actualización</span><span class="sxs-lookup"><span data-stu-id="c153d-103">Microsoft Edge - Update policies</span></span>
<span data-ttu-id="c153d-104">La última versión de Microsoft Edge incluye las siguientes directivas que puedes usar para controlar cómo y cuándo se actualiza Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c153d-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

           
<span data-ttu-id="c153d-105">Para obtener información sobre otras directivas disponibles en Microsoft Edge, consulta la [referencia de directiva del explorador Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="c153d-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="c153d-106">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c153d-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="c153d-107">Directivas disponibles</span><span class="sxs-lookup"><span data-stu-id="c153d-107">Available policies</span></span>
<span data-ttu-id="c153d-108">Estas tablas enumeran todas las directivas de grupo relacionadas con la actualización disponibles en esta versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c153d-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="c153d-109">Usa los vínculos de la tabla para obtener más detalles sobre directivas específicas.</span><span class="sxs-lookup"><span data-stu-id="c153d-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="c153d-110">Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c153d-110">Applications</span></span>](#applications)|[<span data-ttu-id="c153d-111">Preferencias</span><span class="sxs-lookup"><span data-stu-id="c153d-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="c153d-112">Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-112">Proxy Server</span></span>](#proxy-server)||

### [<span data-ttu-id="c153d-113">Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c153d-113">Applications</span></span>](#applications-policies)
|<span data-ttu-id="c153d-114">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="c153d-114">Policy Name</span></span>|<span data-ttu-id="c153d-115">Título</span><span class="sxs-lookup"><span data-stu-id="c153d-115">Caption</span></span>|
|-|-|
|[<span data-ttu-id="c153d-116">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-116">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="c153d-117">Valor predeterminado de Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="c153d-117">Allow installation default</span></span>|
|[<span data-ttu-id="c153d-118">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-118">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="c153d-119">Valor predeterminado de Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="c153d-119">Update policy override default</span></span>|
|[<span data-ttu-id="c153d-120">Instalar</span><span class="sxs-lookup"><span data-stu-id="c153d-120">Install</span></span>](#install)|<span data-ttu-id="c153d-121">Permitir instalación (por canal)</span><span class="sxs-lookup"><span data-stu-id="c153d-121">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="c153d-122">Actualizar</span><span class="sxs-lookup"><span data-stu-id="c153d-122">Update</span></span>](#update)|<span data-ttu-id="c153d-123">Invalidar directiva de actualización (por canal)</span><span class="sxs-lookup"><span data-stu-id="c153d-123">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="c153d-124">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="c153d-124">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="c153d-125">Permitir la experiencia de exploradores Microsoft Edge en paralelo</span><span class="sxs-lookup"><span data-stu-id="c153d-125">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="c153d-126">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-126">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="c153d-127">Impedir la creación de accesos directos de escritorio durante la instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="c153d-127">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="c153d-128">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="c153d-128">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="c153d-129">Impedir la creación de accesos directos de escritorio durante la instalación (por canal)</span><span class="sxs-lookup"><span data-stu-id="c153d-129">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="c153d-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="c153d-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="c153d-131">Invalidación de versión de destino (por canal)</span><span class="sxs-lookup"><span data-stu-id="c153d-131">Target version override (per channel)</span></span>|

### [<span data-ttu-id="c153d-132">Preferencias</span><span class="sxs-lookup"><span data-stu-id="c153d-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="c153d-133">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="c153d-133">Policy Name</span></span>|<span data-ttu-id="c153d-134">Título</span><span class="sxs-lookup"><span data-stu-id="c153d-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="c153d-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="c153d-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="c153d-136">invalidar el período de buscar actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="c153d-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="c153d-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="c153d-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="c153d-138">Período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="c153d-138">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="c153d-139">Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="c153d-140">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="c153d-140">Policy Name</span></span>|<span data-ttu-id="c153d-141">Leyenda</span><span class="sxs-lookup"><span data-stu-id="c153d-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="c153d-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="c153d-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="c153d-143">Elegir cómo especificar la configuración del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="c153d-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="c153d-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="c153d-145">Dirección URL a un archivo proxy .pac</span><span class="sxs-lookup"><span data-stu-id="c153d-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="c153d-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="c153d-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="c153d-147">Dirección o dirección URL del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-147">Address or URL of proxy server</span></span>|

                 
      
  
             
            
                  

## <span data-ttu-id="c153d-148">Directivas de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c153d-148">Applications policies</span></span>

[<span data-ttu-id="c153d-149">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-149">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="c153d-150">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-150">InstallDefault</span></span>
#### <span data-ttu-id="c153d-151">Valor predeterminado de Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="c153d-151">Allow installation default</span></span>
><span data-ttu-id="c153d-152">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-152">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c153d-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-153">Description</span></span>
<span data-ttu-id="c153d-154">Puede especificar el comportamiento predeterminado de todos los canales para permitir o bloquear las actualizaciones de Microsoft Edge cuando se usa Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-154">You can specify the default behavior of all channels to allow or block Microsoft Edge updates when Microsoft Edge Update is used.</span></span>

<span data-ttu-id="c153d-155">Puede reemplazar esta directiva para canales individuales si habilita la directiva [Permitir instalación](#install) para canales específicos.</span><span class="sxs-lookup"><span data-stu-id="c153d-155">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="c153d-156">Si deshabilita esta directiva, se bloquea la instalación de Microsoft Edge a través de Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-156">If you disable this policy, the installation of Microsoft Edge through Microsoft Edge Update is blocked.</span></span> <span data-ttu-id="c153d-157">Afecta solo a la instalación de software de Microsoft Edge solo cuando los usuarios ejecutan Microsoft Edge Update y solo cuando no han configurado la directiva '[Permitir instalación](#install)'.</span><span class="sxs-lookup"><span data-stu-id="c153d-157">This only affects the installation of Microsoft Edge software only when users are running Microsoft Edge Update and when they haven't configured the '[Allow installation](#install)' policy.</span></span>

<span data-ttu-id="c153d-158">Esta directiva no impide que se ejecute Microsoft Edge Update ni impide que los usuarios instalen software de Microsoft Edge con otros métodos.</span><span class="sxs-lookup"><span data-stu-id="c153d-158">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>
#### <span data-ttu-id="c153d-159">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-159">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-160">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-160">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-161">Nombre único de GP: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-161">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="c153d-162">Nombre de GP: valor predeterminado de Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="c153d-162">GP name: Allow installation default</span></span>
- <span data-ttu-id="c153d-163">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c153d-163">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="c153d-164">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-164">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-165">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-165">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-166">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-166">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-167">Nombre de valor: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-167">Value Name: InstallDefault</span></span>
- <span data-ttu-id="c153d-168">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c153d-168">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c153d-169">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-169">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c153d-170">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-170">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c153d-171">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-171">UpdateDefault</span></span>
#### <span data-ttu-id="c153d-172">Valor predeterminado de Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="c153d-172">Update policy override default</span></span>
><span data-ttu-id="c153d-173">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-173">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c153d-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-174">Description</span></span>
<span data-ttu-id="c153d-175">Permite especificar el comportamiento predeterminado de todos los canales relacionados con la manera en que Microsoft Edge Update trata las actualizaciones disponibles para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c153d-175">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="c153d-176">Se puede invalidar para canales individuales especificando la directiva '[Invalidar directiva de actualización](#update)' para esos canales específicos.</span><span class="sxs-lookup"><span data-stu-id="c153d-176">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="c153d-177">Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge de acuerdo con la configuración de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="c153d-177">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="c153d-178">Permitir siempre las actualizaciones: las actualizaciones siempre se aplican cuando se encuentran, ya sea mediante la búsqueda de actualizaciones periódicas o mediante una búsqueda de actualizaciones manual.</span><span class="sxs-lookup"><span data-stu-id="c153d-178">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="c153d-179">Solo actualizaciones silenciosas automáticas: las actualizaciones solo se aplican cuando las encuentra la búsqueda periódica de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="c153d-179">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="c153d-180">Solo actualizaciones manuales: las actualizaciones se aplican solo cuando el usuario ejecuta una búsqueda manual de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="c153d-180">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="c153d-181">Actualizaciones deshabilitadas: las actualizaciones nunca se aplican.</span><span class="sxs-lookup"><span data-stu-id="c153d-181">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="c153d-182">Si seleccionas las actualizaciones manuales, asegúrate de buscar periódicamente actualizaciones mediante el mecanismo de actualización manual de la aplicación, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="c153d-182">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="c153d-183">Si deshabilitas las actualizaciones, comprueba periódicamente si las hay y distribúyelas a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c153d-183">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="c153d-184">Si no habilitas ni configuras esta directiva, Microsoft Edge Update administra las actualizaciones disponibles según se especifica en la directiva '[Invalidar directiva de actualizaciones](#update)'.</span><span class="sxs-lookup"><span data-stu-id="c153d-184">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>
#### <span data-ttu-id="c153d-185">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-185">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-186">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-186">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-187">Nombre único de GP: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-187">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="c153d-188">Nombre de GP: Valor predeterminado de Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="c153d-188">GP name: Update policy override default</span></span>
- <span data-ttu-id="c153d-189">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c153d-189">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="c153d-190">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-190">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-191">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-191">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-192">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-192">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-193">Nombre de valor: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-193">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="c153d-194">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c153d-194">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c153d-195">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-195">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="c153d-196">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-196">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c153d-197">Instalar</span><span class="sxs-lookup"><span data-stu-id="c153d-197">Install</span></span>
#### <span data-ttu-id="c153d-198">Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="c153d-198">Allow installation</span></span>
><span data-ttu-id="c153d-199">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-199">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c153d-200">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-200">Description</span></span>
<span data-ttu-id="c153d-201">Especifica si se puede instalar un canal de Microsoft Edge mediante Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-201">Specifies whether a Microsoft Edge channel can be installed using Microsoft Edge Update.</span></span>

  <span data-ttu-id="c153d-202">Si habilitas esta directiva para un canal, los usuarios pueden instalar el canal de Microsoft Edge a través de Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-202">If you enable this policy for a channel, users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="c153d-203">Si deshabilitas esta directiva para un canal, los usuarios no pueden instalar el canal de Microsoft Edge a través de Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-203">If you disable this policy for a channel, users cannot install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="c153d-204">Si no configuras esta directiva para un canal, la configuración de la directiva '[Valor predeterminado de Permitir instalación](#installdefault)' determina si los usuarios pueden instalar el canal de Microsoft Edge a través de Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-204">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="c153d-205">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-205">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-206">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-206">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-207">Nombre único de GP: Install</span><span class="sxs-lookup"><span data-stu-id="c153d-207">GP unique name: Install</span></span>
- <span data-ttu-id="c153d-208">Nombre de GP: Permitir instalación</span><span class="sxs-lookup"><span data-stu-id="c153d-208">GP name: Allow installation</span></span>
- <span data-ttu-id="c153d-209">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="c153d-209">GP path:</span></span> 
  - <span data-ttu-id="c153d-210">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c153d-210">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="c153d-211">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="c153d-211">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="c153d-212">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="c153d-212">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="c153d-213">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="c153d-213">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="c153d-214">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-214">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-215">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-215">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-216">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-216">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-217">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="c153d-217">Value Name:</span></span> 
  - <span data-ttu-id="c153d-218">(Estable): instalar{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="c153d-218">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="c153d-219">(Beta): instalar{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="c153d-219">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="c153d-220">(Canarias): instalar{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="c153d-220">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="c153d-221">(Dev): instalar{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="c153d-221">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="c153d-222">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c153d-222">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c153d-223">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-223">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c153d-224">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-224">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c153d-225">Actualizar</span><span class="sxs-lookup"><span data-stu-id="c153d-225">Update</span></span>
#### <span data-ttu-id="c153d-226">Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="c153d-226">Update policy override</span></span>
><span data-ttu-id="c153d-227">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-227">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c153d-228">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-228">Description</span></span>
<span data-ttu-id="c153d-229">Especifica cómo trata Microsoft Edge Update las actualizaciones disponibles de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c153d-229">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

  <span data-ttu-id="c153d-230">Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge de acuerdo con la configuración de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="c153d-230">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="c153d-231">Permitir siempre las actualizaciones: las actualizaciones siempre se aplican cuando se encuentran, ya sea mediante la búsqueda de actualizaciones periódicas o mediante una búsqueda de actualizaciones manual.</span><span class="sxs-lookup"><span data-stu-id="c153d-231">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="c153d-232">Solo actualizaciones silenciosas automáticas: las actualizaciones solo se aplican cuando las encuentra la búsqueda periódica de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="c153d-232">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="c153d-233">Solo actualizaciones manuales: las actualizaciones se aplican solo cuando el usuario ejecuta una búsqueda manual de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="c153d-233">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="c153d-234">(No todas las aplicaciones ofrecen una interfaz para esta opción).</span><span class="sxs-lookup"><span data-stu-id="c153d-234">(Not all apps provide an interface for this option.)</span></span>
   - <span data-ttu-id="c153d-235">Actualizaciones deshabilitadas: las actualizaciones nunca se aplican.</span><span class="sxs-lookup"><span data-stu-id="c153d-235">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="c153d-236">Si seleccionas las actualizaciones manuales, asegúrate de buscar periódicamente actualizaciones mediante el mecanismo de actualización manual de la aplicación, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="c153d-236">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="c153d-237">Si deshabilitas las actualizaciones, comprueba periódicamente si las hay y distribúyelas a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c153d-237">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="c153d-238">Si no habilitas ni configuras esta directiva, Microsoft Edge Update administra las actualizaciones disponibles según se especifica en la directiva '[Valor predeterminado de Invalidar directiva de actualizaciones](#updatedefault)'.</span><span class="sxs-lookup"><span data-stu-id="c153d-238">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>
#### <span data-ttu-id="c153d-239">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-239">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-240">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-240">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-241">Nombre único de GP: Actualización</span><span class="sxs-lookup"><span data-stu-id="c153d-241">GP unique name: Update</span></span>
- <span data-ttu-id="c153d-242">Nombre de GP: Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="c153d-242">GP name: Update policy override</span></span>
- <span data-ttu-id="c153d-243">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="c153d-243">GP path:</span></span> 
  - <span data-ttu-id="c153d-244">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c153d-244">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="c153d-245">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="c153d-245">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="c153d-246">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="c153d-246">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="c153d-247">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="c153d-247">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="c153d-248">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-248">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-249">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-249">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-250">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-250">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-251">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="c153d-251">Value Name:</span></span> 
  - <span data-ttu-id="c153d-252">(Estable): actualizar{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="c153d-252">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="c153d-253">(Beta): actualizar{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="c153d-253">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="c153d-254">(Canarias): actualizar{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="c153d-254">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="c153d-255">(Dev): actualizar{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="c153d-255">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="c153d-256">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c153d-256">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c153d-257">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-257">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c153d-258">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-258">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c153d-259">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="c153d-259">Allowsxs</span></span>
#### <span data-ttu-id="c153d-260">Permitir la experiencia de exploradores Microsoft Edge en paralelo</span><span class="sxs-lookup"><span data-stu-id="c153d-260">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="c153d-261">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-261">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c153d-262">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-262">Description</span></span>
<span data-ttu-id="c153d-263">Esta directiva permite a un usuario ejecutar Microsoft Edge (Edge HTML) y Microsoft Edge (basado en Chromium) en paralelo.</span><span class="sxs-lookup"><span data-stu-id="c153d-263">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="c153d-264">Si esta directiva se establece en “No configurado”, Microsoft Edge (basado en Chromium) reemplazará a Microsoft Edge (Edge HTML) después del canal estable de Microsoft Edge (basado en Chromium) y se instalarán las actualizaciones de seguridad de noviembre de 2019.</span><span class="sxs-lookup"><span data-stu-id="c153d-264">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="c153d-265">Este es el mismo comportamiento que la opción “Deshabilitado”.</span><span class="sxs-lookup"><span data-stu-id="c153d-265">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="c153d-266">La opción “Deshabilitado” bloquea la experiencia en paralelo y Microsoft Edge (basado en Chromium) reemplazará a Microsoft Edge (Edge HTML) después del canal estable de Microsoft Edge (basado en Chromium) y se instalarán las actualizaciones de seguridad de noviembre de 2019.</span><span class="sxs-lookup"><span data-stu-id="c153d-266">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="c153d-267">Este es el mismo comportamiento que la opción “No configurado”.</span><span class="sxs-lookup"><span data-stu-id="c153d-267">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="c153d-268">Cuando esta directiva está “Habilitada”, se pueden ejecutar en paralelo Microsoft Edge (Edge HTML) y Microsoft Edge (basado en Chromium) después de instalado Microsoft Edge (basado en Chromium).</span><span class="sxs-lookup"><span data-stu-id="c153d-268">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="c153d-269">Para que esta directiva de grupo surta efecto, debe configurarse antes de la instalación automática de Microsoft Edge (basado en Chromium) por parte de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-269">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="c153d-270">Nota: un usuario puede bloquear la actualización automática de Microsoft Edge (basado en Chromium) mediante el kit de herramientas de bloqueo de Microsoft Edge (basado en Chromium).</span><span class="sxs-lookup"><span data-stu-id="c153d-270">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="c153d-271">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-271">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-272">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-272">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-273">Nombre único de GP: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="c153d-273">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="c153d-274">Nombre de GP: permitir la experiencia en paralelo de exploradores Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c153d-274">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="c153d-275">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c153d-275">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="c153d-276">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-276">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-277">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-277">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-278">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-278">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-279">Nombre del valor: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="c153d-279">Value Name: Allowsxs</span></span>
- <span data-ttu-id="c153d-280">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c153d-280">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c153d-281">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-281">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c153d-282">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-282">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c153d-283">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-283">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="c153d-284">Impedir la creación de accesos directos de escritorio durante la instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="c153d-284">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="c153d-285">Microsoft Edge Update 1.3.128.0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-285">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="c153d-286">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-286">Description</span></span>
<span data-ttu-id="c153d-287">Permite especificar el comportamiento predeterminado de todos los canales para crear un acceso directo en el escritorio cuando se instala Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c153d-287">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="c153d-288">Si habilita esta directiva, se creará un acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c153d-288">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="c153d-289">Si deshabilita esta directiva, no se creará ningún acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c153d-289">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="c153d-290">Si no configura esta directiva, se creará un acceso directo de escritorio a Microsoft Edge durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="c153d-290">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="c153d-291">Si Microsoft Edge ya está instalado, esta directiva no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="c153d-291">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="c153d-292">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-292">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-293">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-293">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-294">Nombre único de GP: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-294">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="c153d-295">Nombre de GP: configuración predeterminada para impedir la creación de accesos directos de escritorio durante la instalación</span><span class="sxs-lookup"><span data-stu-id="c153d-295">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="c153d-296">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c153d-296">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="c153d-297">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-297">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-298">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-298">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-299">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-299">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-300">Nombre del valor: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="c153d-300">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="c153d-301">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c153d-301">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c153d-302">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-302">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c153d-303">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-303">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c153d-304">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="c153d-304">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="c153d-305">Impedir la creación de accesos directos de escritorio durante la instalación</span><span class="sxs-lookup"><span data-stu-id="c153d-305">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="c153d-306">Microsoft Edge Update 1.3.128.0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-306">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="c153d-307">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-307">Description</span></span>
<span data-ttu-id="c153d-308">Si habilita esta directiva, se creará un acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c153d-308">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="c153d-309">Si deshabilita esta directiva, no se creará ningún acceso directo de escritorio cuando se instale Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c153d-309">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="c153d-310">Si no configura esta directiva, se creará un acceso directo de escritorio a Microsoft Edge durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="c153d-310">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="c153d-311">Si Microsoft Edge ya está instalado, esta directiva no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="c153d-311">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="c153d-312">Si no configura esta directiva para un canal, la configuración de directiva '[Impedir la creación de accesos directos de escritorio durante la instalación predeterminada](#createdesktopshortcutdefault)' determina la creación de accesos directos cuando se instala Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c153d-312">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="c153d-313">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-313">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-314">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-314">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-315">Nombre único de GP: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="c153d-315">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="c153d-316">Nombre de GP: impedir la creación de métodos abreviados de escritorio durante la instalación</span><span class="sxs-lookup"><span data-stu-id="c153d-316">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="c153d-317">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="c153d-317">GP path:</span></span> 
  - <span data-ttu-id="c153d-318">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c153d-318">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="c153d-319">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="c153d-319">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="c153d-320">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="c153d-320">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="c153d-321">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="c153d-321">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="c153d-322">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-322">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-323">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-323">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-324">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-324">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-325">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="c153d-325">Value Name:</span></span> 
  - <span data-ttu-id="c153d-326">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="c153d-326">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="c153d-327">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="c153d-327">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="c153d-328">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="c153d-328">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="c153d-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="c153d-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="c153d-330">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c153d-330">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c153d-331">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-331">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c153d-332">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-332">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c153d-333">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="c153d-333">TargetVersionPrefix</span></span>
#### <span data-ttu-id="c153d-334">Invalidación de versión de destino</span><span class="sxs-lookup"><span data-stu-id="c153d-334">Target version override</span></span>
><span data-ttu-id="c153d-335">Microsoft Edge Update 1.3.119.43 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-335">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="c153d-336">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-336">Description</span></span>
<span data-ttu-id="c153d-337">Cuando se habilita esta directiva y la actualización automática está habilitada, Microsoft Edge se actualizará a la versión especificada por este valor de directiva.</span><span class="sxs-lookup"><span data-stu-id="c153d-337">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="c153d-338">El valor de directiva debe ser una versión específica de Microsoft Edge, como 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="c153d-338">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="c153d-339">Si un dispositivo tiene una versión más reciente de Microsoft Edge que el valor especificado, Microsoft Edge permanecerá en la versión más reciente, mas no desactualizada a la versión especificada.</span><span class="sxs-lookup"><span data-stu-id="c153d-339">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="c153d-340">Si la versión especificada no existe o no tiene el formato correcto, Microsoft Edge permanecerá en su versión actual y no se actualizará a versiones futuras de manera automática.</span><span class="sxs-lookup"><span data-stu-id="c153d-340">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>
#### <span data-ttu-id="c153d-341">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-341">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-342">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-342">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-343">Nombre único de GP: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="c153d-343">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="c153d-344">Nombre de GP: Invalidación de versión de destino</span><span class="sxs-lookup"><span data-stu-id="c153d-344">GP name: Target version override</span></span>
- <span data-ttu-id="c153d-345">Ruta de GP:</span><span class="sxs-lookup"><span data-stu-id="c153d-345">GP path:</span></span> 
  - <span data-ttu-id="c153d-346">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c153d-346">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="c153d-347">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="c153d-347">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="c153d-348">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="c153d-348">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="c153d-349">Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="c153d-349">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="c153d-350">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-350">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-351">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-351">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-352">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-352">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-353">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="c153d-353">Value Name:</span></span> 
  - <span data-ttu-id="c153d-354">(Estable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="c153d-354">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="c153d-355">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="c153d-355">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="c153d-356">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="c153d-356">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="c153d-357">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="c153d-357">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="c153d-358">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c153d-358">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="c153d-359">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-359">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="c153d-360">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-360">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="c153d-361">Directivas de preferencias</span><span class="sxs-lookup"><span data-stu-id="c153d-361">Preferences policies</span></span>

[<span data-ttu-id="c153d-362">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-362">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="c153d-363">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="c153d-363">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="c153d-364">invalidar el período de buscar actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="c153d-364">Auto-update check period override</span></span>
><span data-ttu-id="c153d-365">Microsoft Edge Update 1.2.145.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-365">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c153d-366">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-366">Description</span></span>
<span data-ttu-id="c153d-367">Si se habilita, esta directiva permite establecer un valor para el número mínimo de minutos entre las búsquedas de actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="c153d-367">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="c153d-368">De lo contrario, de manera predeterminada, la actualización automática busca actualizaciones cada 10 horas.</span><span class="sxs-lookup"><span data-stu-id="c153d-368">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="c153d-369">Si quieres deshabilitar todas las búsquedas de actualizaciones automáticas, establece el valor en 0 (no recomendado).</span><span class="sxs-lookup"><span data-stu-id="c153d-369">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="c153d-370">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-370">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-371">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-371">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-372">Nombre único de GP: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="c153d-372">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="c153d-373">Nombre de GP: invalidar el período de buscar actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="c153d-373">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="c153d-374">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Preferencias</span><span class="sxs-lookup"><span data-stu-id="c153d-374">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="c153d-375">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-375">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-376">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-376">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-377">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-378">Nombre de valor: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="c153d-378">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="c153d-379">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c153d-379">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c153d-380">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-380">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="c153d-381">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-381">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c153d-382">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="c153d-382">UpdatesSuppressed</span></span>
#### <span data-ttu-id="c153d-383">Período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="c153d-383">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="c153d-384">Microsoft Edge Update 1.3.33.5 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-384">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="c153d-385">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-385">Description</span></span>
<span data-ttu-id="c153d-386">Si habilitas esta Directiva, las búsquedas de actualizaciones se suprimirán cada día, a partir de Hora:Minuto durante un período de tiempo (en minutos).</span><span class="sxs-lookup"><span data-stu-id="c153d-386">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="c153d-387">La duración no se ve afectada por el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c153d-387">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="c153d-388">Por ejemplo, si la hora de inicio es 22:00 y la duración es 480 minutos, las actualizaciones se suprimirán durante 8 horas exactamente, independientemente de si el horario de verano comienza o finaliza durante este período.</span><span class="sxs-lookup"><span data-stu-id="c153d-388">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="c153d-389">Si deshabilitas o no configuras esta directiva, las búsquedas de actualizaciones no se suprimirán durante ningún período determinado.</span><span class="sxs-lookup"><span data-stu-id="c153d-389">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="c153d-390">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-390">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-391">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-391">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-392">Nombre único de GP: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="c153d-392">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="c153d-393">Nombre de GP: período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="c153d-393">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="c153d-394">Opciones {Hora, Minuto, Duración}</span><span class="sxs-lookup"><span data-stu-id="c153d-394">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="c153d-395">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Preferencias</span><span class="sxs-lookup"><span data-stu-id="c153d-395">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="c153d-396">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-396">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-397">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-397">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-398">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-398">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-399">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="c153d-399">Value Name:</span></span> 
  - <span data-ttu-id="c153d-400">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="c153d-400">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="c153d-401">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="c153d-401">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="c153d-402">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="c153d-402">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="c153d-403">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c153d-403">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c153d-404">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-404">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="c153d-405">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-405">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="c153d-406">Directivas de servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-406">Proxy Server policies</span></span>
  
  

[<span data-ttu-id="c153d-407">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-407">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="c153d-408">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="c153d-408">ProxyMode</span></span>
#### <span data-ttu-id="c153d-409">Elegir cómo especificar la configuración del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-409">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="c153d-410">Microsoft Edge Update 1.3.21.81 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-410">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="c153d-411">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-411">Description</span></span>
<span data-ttu-id="c153d-412">Permite especificar la configuración del servidor proxy que usa Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-412">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="c153d-413">Si habilitas esta directiva, puedes elegir entre las siguientes opciones de servidor proxy:</span><span class="sxs-lookup"><span data-stu-id="c153d-413">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="c153d-414">Si eliges no usar nunca un servidor proxy y siempre te conectas directamente, se ignora el resto de opciones.</span><span class="sxs-lookup"><span data-stu-id="c153d-414">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="c153d-415">Si elige usar la configuración proxy del sistema o detectar automáticamente el servidor proxy, se ignora el resto de opciones.</span><span class="sxs-lookup"><span data-stu-id="c153d-415">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="c153d-416">Si eliges el modo de servidor proxy fijo, puedes especificar más opciones en '[Dirección o dirección URL del servidor proxy](#proxyserver)'.</span><span class="sxs-lookup"><span data-stu-id="c153d-416">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="c153d-417">Si decides usar un script de proxy .pac, debes especificar la dirección URL del script en '[Dirección URL de un archivo de proxy .pac](#proxypacurl)'.</span><span class="sxs-lookup"><span data-stu-id="c153d-417">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="c153d-418">Si habilitas esta directiva, los usuarios de la organización no pueden cambiar la configuración de proxy en Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-418">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="c153d-419">Si deshabilitas o no configuras esta directiva, no se configuran las opciones del servidor proxy, pero los usuarios de la organización pueden elegir su propia configuración de proxy para Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-419">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="c153d-420">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-420">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-421">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-421">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-422">Nombre único de GP: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="c153d-422">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="c153d-423">Nombre de GP: elige cómo especificar la configuración del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-423">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="c153d-424">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-424">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="c153d-425">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-425">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-426">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-426">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-427">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-427">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-428">Nombre del valor: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="c153d-428">Value Name: ProxyMode</span></span>
- <span data-ttu-id="c153d-429">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c153d-429">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="c153d-430">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-430">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="c153d-431">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-431">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c153d-432">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="c153d-432">ProxyPacUrl</span></span>
#### <span data-ttu-id="c153d-433">Dirección URL a un archivo proxy .pac</span><span class="sxs-lookup"><span data-stu-id="c153d-433">URL to a proxy .pac file</span></span>
><span data-ttu-id="c153d-434">Microsoft Edge Update 1.3.21.81 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-434">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="c153d-435">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-435">Description</span></span>
<span data-ttu-id="c153d-436">Permite especificar una dirección URL para un archivo de configuración automática de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="c153d-436">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="c153d-437">Si habilitas esta directiva, puedes especificar una dirección URL para un archivo PAC que automatice cómo Microsoft Edge Update selecciona el servidor proxy adecuado para localizar un sitio web en particular.</span><span class="sxs-lookup"><span data-stu-id="c153d-437">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="c153d-438">Esta directiva solo se aplica si has especificado una configuración de proxy manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="c153d-438">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="c153d-439">No configures esta directiva si has especificado una configuración de proxy diferente de manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="c153d-439">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="c153d-440">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-440">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-441">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-441">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-442">Nombre único de GP: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="c153d-442">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="c153d-443">Nombre de GP: dirección URL a un archivo proxy .pac</span><span class="sxs-lookup"><span data-stu-id="c153d-443">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="c153d-444">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-444">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="c153d-445">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-445">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-446">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-446">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-447">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-447">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-448">Nombre del valor: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="c153d-448">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="c153d-449">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c153d-449">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="c153d-450">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-450">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="c153d-451">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-451">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c153d-452">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="c153d-452">ProxyServer</span></span>
#### <span data-ttu-id="c153d-453">Dirección o dirección URL del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-453">Address or URL of proxy server</span></span>
><span data-ttu-id="c153d-454">Microsoft Edge Update 1.3.21.81 y posteriores</span><span class="sxs-lookup"><span data-stu-id="c153d-454">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="c153d-455">Descripción</span><span class="sxs-lookup"><span data-stu-id="c153d-455">Description</span></span>
<span data-ttu-id="c153d-456">Permite especificar la dirección URL del servidor proxy que usa Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c153d-456">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="c153d-457">Si habilitas esta directiva, puedes establecer la dirección URL del servidor proxy usado por Microsoft Edge Update en tu organización.</span><span class="sxs-lookup"><span data-stu-id="c153d-457">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="c153d-458">Esta directiva solo se aplica si has seleccionado una configuración de proxy manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="c153d-458">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="c153d-459">No configures esta directiva si has especificado una configuración de proxy diferente de manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="c153d-459">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="c153d-460">Información y configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-460">Windows information and settings</span></span>
##### <span data-ttu-id="c153d-461">Información de directiva de grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c153d-461">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c153d-462">Nombre único de GP: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="c153d-462">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="c153d-463">Nombre de GP: dirección o dirección URL del servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-463">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="c153d-464">Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c153d-464">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="c153d-465">Nombre de archivo GP ADMX: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c153d-465">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="c153d-466">Configuración del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c153d-466">Windows Registry Settings</span></span>
- <span data-ttu-id="c153d-467">Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c153d-467">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c153d-468">Nombre del valor: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="c153d-468">Value Name: ProxyServer</span></span>
- <span data-ttu-id="c153d-469">Tipo de valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c153d-469">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="c153d-470">Valor de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c153d-470">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="c153d-471">Volver al principio</span><span class="sxs-lookup"><span data-stu-id="c153d-471">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="c153d-472">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c153d-472">See also</span></span>
  - [<span data-ttu-id="c153d-473">Configuración de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c153d-473">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="c153d-474">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c153d-474">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
