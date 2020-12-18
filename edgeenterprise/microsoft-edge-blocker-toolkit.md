---
title: Kit de herramientas de bloqueo para deshabilitar la entrega automática de Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 12/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Kit de herramientas de bloqueo para deshabilitar la entrega automática de Microsoft Edge
ms.openlocfilehash: 9fb97d2dfec4822f8ce76dc3e37b85118c6572ad
ms.sourcegitcommit: 606282995b466a968bab40c16005a6653323c763
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/16/2020
ms.locfileid: "11229621"
---
# <span data-ttu-id="75996-103">Kit de herramientas de bloqueo para deshabilitar la entrega automática de Microsoft Edge (basado en Chromium)</span><span class="sxs-lookup"><span data-stu-id="75996-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="75996-104">Este artículo describe el kit de herramientas de bloqueo para deshabilitar la entrega y la instalación automáticas de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="75996-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span>

<span data-ttu-id="75996-105">Se han realizado las siguientes actualizaciones en este artículo:</span><span class="sxs-lookup"><span data-stu-id="75996-105">The following updates have been made to this article:</span></span>

- <span data-ttu-id="75996-106">**01/09/2020** con más información sobre los dispositivos que pueden requerir que use el kit de herramientas de bloqueo</span><span class="sxs-lookup"><span data-stu-id="75996-106">**01/09/2020** with more information about devices that might require you to use the Blocker Toolkit</span></span>
- <span data-ttu-id="75996-107">**2/28/2020** para quitar "MDM administrado" de los criterios de los dispositivos que se deben excluir de esta actualización automática</span><span class="sxs-lookup"><span data-stu-id="75996-107">**2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update</span></span>
- <span data-ttu-id="75996-108">**6/30/2020** para reflejar que todos los dispositivos conectados a Windows Update están en el ámbito para recibir esta actualización (vigente no antes del 7/30/2020)</span><span class="sxs-lookup"><span data-stu-id="75996-108">**6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020)</span></span>
- <span data-ttu-id="75996-109">**12/10/2020** para explicar las situaciones pre 20H2 en las que se omitirá la configuración del kit de herramientas de bloqueo</span><span class="sxs-lookup"><span data-stu-id="75996-109">**12/10/2020** to explain pre 20H2 situations in which the Blocker Toolkit settings will be ignored</span></span>

> [!NOTE]
> <span data-ttu-id="75996-110">Esto es de aplicación al canal estable de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="75996-110">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="75996-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="75996-111">Overview</span></span>

<span data-ttu-id="75996-112">Para ayudar a nuestros clientes a estar más seguros y actualizados, Microsoft distribuirá Microsoft Edge (basado en Chromium) a todos los dispositivos conectados a Windows Update que ejecutan Windows10, versión 1803 y más recientes.</span><span class="sxs-lookup"><span data-stu-id="75996-112">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="75996-113">Este proceso se iniciará después del 15 de enero de 2020 y habrá más información disponible en esa fecha.</span><span class="sxs-lookup"><span data-stu-id="75996-113">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="75996-114">El kit de herramientas de bloqueo está pensado para las organizaciones que desean bloquear la entrega automática de Microsoft Edge (basado en Chromium) en dispositivos conectados a Windows Update que ejecutan Windows10, versión 1803 y más recientes.</span><span class="sxs-lookup"><span data-stu-id="75996-114">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="75996-115">Los dispositivos que estén administrados por Windows Server Update Services (WSUS) o Windows Update para empresas (WUfB) se excluirán de esta actualización automática de Windows, pero es posible que reciban el nuevo Microsoft Edge (basado en Chromium) a través de su organización.</span><span class="sxs-lookup"><span data-stu-id="75996-115">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic Windows Update, but may receive the new Microsoft Edge (Chromium-based) through their organization.</span></span>

**<span data-ttu-id="75996-116">Es importante tener en cuenta que:</span><span class="sxs-lookup"><span data-stu-id="75996-116">It's important to note that:</span></span>**

- <span data-ttu-id="75996-117">El kit de herramientas de bloqueo no impedirá que los usuarios instalen manualmente Microsoft Edge (basado en Chromium) a partir de descargas desde Internet o desde medios externos.</span><span class="sxs-lookup"><span data-stu-id="75996-117">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="75996-118">Las organizaciones con actualizaciones administradas a través de Windows Update para empresas (WUfB) no recibirán automáticamente esta actualización y no tienen que implementar el kit de herramientas de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="75996-118">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="75996-119">Las organizaciones con entornos administrados con una solución de administración de actualizaciones, como Windows Server Update Services (WSUS) o System Center Configuration Manager (SCCM) no tienen que implementar el kit de herramientas de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="75996-119">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="75996-120">Pueden usar esos productos para administrar completamente la implementación de actualizaciones publicadas a través de Windows Update y Microsoft Update, incluida la [actualización en WSUS para el nuevo Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), dentro de su entorno.</span><span class="sxs-lookup"><span data-stu-id="75996-120">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including the [Update in WSUS for the new Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), within their environment.</span></span>
- <span data-ttu-id="75996-121">Esta actualización es una actualización independiente (no forma parte de la actualización acumulativa mensual) para ofrecer flexibilidad a los clientes de Enterprise y un control máximo sobre la implementación de esta actualización.</span><span class="sxs-lookup"><span data-stu-id="75996-121">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="75996-122">El nuevo Microsoft Edge (basado en cromo) se incluye como parte de la actualización de características de Windows 10, versión 20H2, en la segunda mitad de 2020.</span><span class="sxs-lookup"><span data-stu-id="75996-122">The new Microsoft Edge (Chromium-based) is included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="75996-123">El kit de herramientas de bloqueo no impacta en los comportamientos o la implementación de la versión 20H2.</span><span class="sxs-lookup"><span data-stu-id="75996-123">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="75996-124">Puede ver más información sobre Windows 10, versión 20H2, [aquí](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span><span class="sxs-lookup"><span data-stu-id="75996-124">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="75996-125">Puedes descargar el archivo ejecutable del kit de herramientas de bloqueo desde [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span><span class="sxs-lookup"><span data-stu-id="75996-125">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="75996-126">Componentes del kit de herramientas</span><span class="sxs-lookup"><span data-stu-id="75996-126">Toolkit components</span></span>

<span data-ttu-id="75996-127">Este kit de herramientas incluye los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="75996-127">This toolkit contains the following components:</span></span>

- <span data-ttu-id="75996-128">Script bloqueador ejecutable (.CMD)</span><span class="sxs-lookup"><span data-stu-id="75996-128">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="75996-129">Plantilla administrativa de directiva de grupo (.ADMX y .ADML)</span><span class="sxs-lookup"><span data-stu-id="75996-129">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="75996-130">Sistemas operativos compatibles</span><span class="sxs-lookup"><span data-stu-id="75996-130">Supported Operating Systems</span></span>

<span data-ttu-id="75996-131">Windows 10, versión 1803 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75996-131">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="75996-132">Script bloqueador</span><span class="sxs-lookup"><span data-stu-id="75996-132">Blocker script</span></span>

<span data-ttu-id="75996-133">El script crea una clave del Registro y establece el valor asociado en bloquear o no bloquear (en función de la opción de línea de comandos usada) la entrega automática de Microsoft Edge (basado en Chromium) en la máquina local o en una máquina remota de destino.</span><span class="sxs-lookup"><span data-stu-id="75996-133">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="75996-134">Clave del Registro:</span><span class="sxs-lookup"><span data-stu-id="75996-134">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="75996-135">Nombre del valor clave:</span><span class="sxs-lookup"><span data-stu-id="75996-135">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="75996-136">Valor</span><span class="sxs-lookup"><span data-stu-id="75996-136">Value</span></span>                | <span data-ttu-id="75996-137">Resultado</span><span class="sxs-lookup"><span data-stu-id="75996-137">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="75996-138">La clave no está definida.</span><span class="sxs-lookup"><span data-stu-id="75996-138">Key is not defined</span></span>* | <span data-ttu-id="75996-139">La distribución *no* está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="75996-139">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="75996-140">0</span><span class="sxs-lookup"><span data-stu-id="75996-140">0</span></span>                    | <span data-ttu-id="75996-141">La distribución *no* está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="75996-141">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="75996-142">1</span><span class="sxs-lookup"><span data-stu-id="75996-142">1</span></span>                    | <span data-ttu-id="75996-143">La distribución está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="75996-143">Distribution is blocked.</span></span>       |

<span data-ttu-id="75996-144">El script tiene la siguiente sintaxis de línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="75996-144">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="75996-145">Nombre de máquina</span><span class="sxs-lookup"><span data-stu-id="75996-145">Machine name</span></span>

<span data-ttu-id="75996-146">El parámetro `<machine name>` es opcional.</span><span class="sxs-lookup"><span data-stu-id="75996-146">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="75996-147">Si no se especifica, la acción se realiza en la máquina local.</span><span class="sxs-lookup"><span data-stu-id="75996-147">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="75996-148">De lo contrario, se accede al equipo remoto a través de las funciones de Registro remoto del comando `REG`.</span><span class="sxs-lookup"><span data-stu-id="75996-148">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="75996-149">Si no se puede acceder al registro remoto debido a los permisos de seguridad o no se encuentra la máquina remota, el comando `REG` devuelve un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="75996-149">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="75996-150">Conmutadores</span><span class="sxs-lookup"><span data-stu-id="75996-150">Switches</span></span>

<span data-ttu-id="75996-151">Los conmutadores que usa el script son mutuamente excluyentes y solo se actúa sobre el primer conmutador válido de un comando determinado.</span><span class="sxs-lookup"><span data-stu-id="75996-151">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="75996-152">El script puede ejecutarse varias veces en la misma máquina.</span><span class="sxs-lookup"><span data-stu-id="75996-152">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="75996-153">Conmutador</span><span class="sxs-lookup"><span data-stu-id="75996-153">Switch</span></span>       | <span data-ttu-id="75996-154">descripción</span><span class="sxs-lookup"><span data-stu-id="75996-154">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="75996-155">Bloquea la distribución</span><span class="sxs-lookup"><span data-stu-id="75996-155">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="75996-156">No bloquea la distribución</span><span class="sxs-lookup"><span data-stu-id="75996-156">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="75996-157">o</span><span class="sxs-lookup"><span data-stu-id="75996-157">or</span></span> `/?` | <span data-ttu-id="75996-158">Muestra la siguiente ayuda resumida:</span><span class="sxs-lookup"><span data-stu-id="75996-158">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="75996-159">Plantilla administrativa de directiva de grupo (archivos .ADMX y .ADML)</span><span class="sxs-lookup"><span data-stu-id="75996-159">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="75996-160">La plantilla administrativa de directiva de grupo (archivos .ADMX y .ADML) permite a los administradores importar la nueva configuración de directiva de grupo para bloquear o no bloquear la entrega automática de Microsoft Edge (basado en Chromium) en el entorno de la directiva de grupo y usar la directiva de grupo para ejecutar la acción de forma centralizada entre sistemas de su entorno.</span><span class="sxs-lookup"><span data-stu-id="75996-160">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="75996-161">Los usuarios que ejecuten Windows 10 RS3 Enterprise/EDU y RS4 y posteriores podrán ver la directiva en la siguiente ruta de acceso:</span><span class="sxs-lookup"><span data-stu-id="75996-161">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="75996-162">Esta opción solo está disponible como configuración del equipo; no hay una opción para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="75996-162">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75996-163">Esta configuración del Registro no se almacena en una clave de directivas y se considera una *preferencia*.</span><span class="sxs-lookup"><span data-stu-id="75996-163">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="75996-164">Por lo tanto, si el objeto de directiva de grupo que implementa la configuración se quita alguna vez o si la directiva está establecida en **No configurada**, la opción se mantendrá.</span><span class="sxs-lookup"><span data-stu-id="75996-164">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="75996-165">Para desbloquear la distribución de Microsoft Edge (basado en Chromium) mediante la directiva de grupo, establece la directiva en **Deshabilitada**.</span><span class="sxs-lookup"><span data-stu-id="75996-165">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="75996-166">Consulta también</span><span class="sxs-lookup"><span data-stu-id="75996-166">See also</span></span>

- [<span data-ttu-id="75996-167">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="75996-167">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="75996-168">Actualizaciones de Windows para compatibilidad con Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="75996-168">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="75996-169">Cómo acceder a la versión anterior de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="75996-169">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
