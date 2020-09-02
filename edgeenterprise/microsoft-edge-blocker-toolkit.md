---
title: Kit de herramientas de bloqueo para deshabilitar la entrega automática de Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Kit de herramientas de bloqueo para deshabilitar la entrega automática de Microsoft Edge
ms.openlocfilehash: 7563d2c94cf91a8434328699e46c75dbcfb77561
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981205"
---
# <span data-ttu-id="6e713-103">Kit de herramientas de bloqueo para deshabilitar la entrega automática de Microsoft Edge (basado en Chromium)</span><span class="sxs-lookup"><span data-stu-id="6e713-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="6e713-104">Este artículo describe el kit de herramientas de bloqueo para deshabilitar la entrega y la instalación automáticas de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6e713-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span> <span data-ttu-id="6e713-105">Este artículo se actualizó en el **9/1/2020** con más información sobre los dispositivos que pueden requerir que use el kit de herramientas de bloqueo, el **28/2/2020** para quitar "Administrado por MDM" de los criterios de los dispositivos que se excluirán de esta actualización automática y el **30/6/2020** para reflejar que todos los dispositivos de Windows Update conectados deben recibir esta actualización (efectivo como pronto el 30/7/2020).</span><span class="sxs-lookup"><span data-stu-id="6e713-105">This article was updated on **01/09/2020** with more information about devices that might require you to use the Blocker Toolkit, on **2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update, and on **6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020).</span></span>

> [!NOTE]
> <span data-ttu-id="6e713-106">Esto es de aplicación al canal Estable de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6e713-106">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="6e713-107">Introducción</span><span class="sxs-lookup"><span data-stu-id="6e713-107">Overview</span></span>

<span data-ttu-id="6e713-108">Para ayudar a nuestros clientes a estar más seguros y actualizados, Microsoft distribuirá Microsoft Edge (basado en Chromium) a todos los dispositivos conectados a Windows Update que ejecutan Windows10, versión 1803 y más recientes.</span><span class="sxs-lookup"><span data-stu-id="6e713-108">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="6e713-109">Este proceso se iniciará después del 15 de enero de 2020 y habrá más información disponible en esa fecha.</span><span class="sxs-lookup"><span data-stu-id="6e713-109">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="6e713-110">El kit de herramientas de bloqueo está pensado para las organizaciones que desean bloquear la entrega automática de Microsoft Edge (basado en Chromium) en dispositivos conectados a Windows Update que ejecutan Windows10, versión 1803 y más recientes.</span><span class="sxs-lookup"><span data-stu-id="6e713-110">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span>
<span data-ttu-id="6e713-111">Los dispositivos administrados por Windows Server Update Services (WSUS) o Windows Update para empresas (WUfB) se excluirán de esta actualización automática.</span><span class="sxs-lookup"><span data-stu-id="6e713-111">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic update.</span></span>

**<span data-ttu-id="6e713-112">Es importante tener en cuenta que:</span><span class="sxs-lookup"><span data-stu-id="6e713-112">It's important to note that:</span></span>**

- <span data-ttu-id="6e713-113">El kit de herramientas de bloqueo no impedirá que los usuarios instalen manualmente Microsoft Edge (basado en Chromium) a partir de descargas desde Internet o desde medios externos.</span><span class="sxs-lookup"><span data-stu-id="6e713-113">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="6e713-114">Las organizaciones con actualizaciones administradas a través de Windows Update para empresas (WUfB) no recibirán automáticamente esta actualización y no tienen que implementar el kit de herramientas de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="6e713-114">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="6e713-115">Las organizaciones con entornos administrados con una solución de administración de actualizaciones, como Windows Server Update Services (WSUS) o System Center Configuration Manager (SCCM) no tienen que implementar el kit de herramientas de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="6e713-115">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="6e713-116">Pueden usar esos productos para administrar completamente la implementación de actualizaciones publicadas a través de Windows Update y Microsoft Update, incluidas las de Microsoft Edge (basado en Chromium), dentro de su entorno.</span><span class="sxs-lookup"><span data-stu-id="6e713-116">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including Microsoft Edge (Chromium-based), within their environment.</span></span>
- <span data-ttu-id="6e713-117">Esta actualización es una actualización independiente (no forma parte de la actualización acumulativa mensual) para ofrecer flexibilidad a los clientes de Enterprise y un control máximo sobre la implementación de esta actualización.</span><span class="sxs-lookup"><span data-stu-id="6e713-117">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="6e713-118">El nuevo Microsoft Edge (basado en Chromium) se incluirá como parte de la actualización de características de Windows 10, versión 20H2, en la segunda mitad de 2020.</span><span class="sxs-lookup"><span data-stu-id="6e713-118">The new Microsoft Edge (Chromium-based) will be included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="6e713-119">El kit de herramientas de bloqueo no impacta en los comportamientos o la implementación de 20H2.</span><span class="sxs-lookup"><span data-stu-id="6e713-119">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="6e713-120">Puede ver más información sobre Windows 10, versión 20H2, [aquí](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span><span class="sxs-lookup"><span data-stu-id="6e713-120">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="6e713-121">Puedes descargar el archivo ejecutable del kit de herramientas de bloqueo desde [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span><span class="sxs-lookup"><span data-stu-id="6e713-121">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="6e713-122">Componentes del kit de herramientas</span><span class="sxs-lookup"><span data-stu-id="6e713-122">Toolkit components</span></span>

<span data-ttu-id="6e713-123">Este kit de herramientas incluye los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="6e713-123">This toolkit contains the following components:</span></span>

- <span data-ttu-id="6e713-124">Script bloqueador ejecutable (.CMD)</span><span class="sxs-lookup"><span data-stu-id="6e713-124">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="6e713-125">Plantilla administrativa de directiva de grupo (.ADMX y .ADML)</span><span class="sxs-lookup"><span data-stu-id="6e713-125">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="6e713-126">Sistemas operativos compatibles</span><span class="sxs-lookup"><span data-stu-id="6e713-126">Supported Operating Systems</span></span>

<span data-ttu-id="6e713-127">Windows 10, versión 1803 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6e713-127">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="6e713-128">Script bloqueador</span><span class="sxs-lookup"><span data-stu-id="6e713-128">Blocker script</span></span>

<span data-ttu-id="6e713-129">El script crea una clave del Registro y establece el valor asociado en bloquear o no bloquear (en función de la opción de línea de comandos usada) la entrega automática de Microsoft Edge (basado en Chromium) en la máquina local o en una máquina remota de destino.</span><span class="sxs-lookup"><span data-stu-id="6e713-129">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="6e713-130">Clave del Registro:</span><span class="sxs-lookup"><span data-stu-id="6e713-130">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="6e713-131">Nombre del valor clave:</span><span class="sxs-lookup"><span data-stu-id="6e713-131">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="6e713-132">Valor</span><span class="sxs-lookup"><span data-stu-id="6e713-132">Value</span></span>                | <span data-ttu-id="6e713-133">Resultado</span><span class="sxs-lookup"><span data-stu-id="6e713-133">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="6e713-134">La clave no está definida.</span><span class="sxs-lookup"><span data-stu-id="6e713-134">Key is not defined</span></span>* | <span data-ttu-id="6e713-135">La distribución *no* está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="6e713-135">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="6e713-136">0</span><span class="sxs-lookup"><span data-stu-id="6e713-136">0</span></span>                    | <span data-ttu-id="6e713-137">La distribución *no* está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="6e713-137">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="6e713-138">1</span><span class="sxs-lookup"><span data-stu-id="6e713-138">1</span></span>                    | <span data-ttu-id="6e713-139">La distribución está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="6e713-139">Distribution is blocked.</span></span>       |

<span data-ttu-id="6e713-140">El script tiene la siguiente sintaxis de línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="6e713-140">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="6e713-141">Nombre de máquina</span><span class="sxs-lookup"><span data-stu-id="6e713-141">Machine name</span></span>

<span data-ttu-id="6e713-142">El parámetro `<machine name>` es opcional.</span><span class="sxs-lookup"><span data-stu-id="6e713-142">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="6e713-143">Si no se especifica, la acción se realiza en la máquina local.</span><span class="sxs-lookup"><span data-stu-id="6e713-143">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="6e713-144">De lo contrario, se accede al equipo remoto a través de las funciones de Registro remoto del comando `REG`.</span><span class="sxs-lookup"><span data-stu-id="6e713-144">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="6e713-145">Si no se puede acceder al registro remoto debido a los permisos de seguridad o no se encuentra la máquina remota, el comando `REG` devuelve un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="6e713-145">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="6e713-146">Conmutadores</span><span class="sxs-lookup"><span data-stu-id="6e713-146">Switches</span></span>

<span data-ttu-id="6e713-147">Los conmutadores que usa el script son mutuamente excluyentes y solo se actúa sobre el primer conmutador válido de un comando determinado.</span><span class="sxs-lookup"><span data-stu-id="6e713-147">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="6e713-148">El script puede ejecutarse varias veces en la misma máquina.</span><span class="sxs-lookup"><span data-stu-id="6e713-148">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="6e713-149">Conmutador</span><span class="sxs-lookup"><span data-stu-id="6e713-149">Switch</span></span>       | <span data-ttu-id="6e713-150">descripción</span><span class="sxs-lookup"><span data-stu-id="6e713-150">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="6e713-151">Bloquea la distribución</span><span class="sxs-lookup"><span data-stu-id="6e713-151">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="6e713-152">No bloquea la distribución</span><span class="sxs-lookup"><span data-stu-id="6e713-152">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="6e713-153">o</span><span class="sxs-lookup"><span data-stu-id="6e713-153">or</span></span> `/?` | <span data-ttu-id="6e713-154">Muestra la siguiente ayuda resumida:</span><span class="sxs-lookup"><span data-stu-id="6e713-154">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="6e713-155">Plantilla administrativa de directiva de grupo (archivos .ADMX y .ADML)</span><span class="sxs-lookup"><span data-stu-id="6e713-155">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="6e713-156">La plantilla administrativa de directiva de grupo (archivos .ADMX y .ADML) permite a los administradores importar la nueva configuración de directiva de grupo para bloquear o no bloquear la entrega automática de Microsoft Edge (basado en Chromium) en el entorno de la directiva de grupo y usar la directiva de grupo para ejecutar la acción de forma centralizada entre sistemas de su entorno.</span><span class="sxs-lookup"><span data-stu-id="6e713-156">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="6e713-157">Los usuarios que ejecuten Windows 10 RS3 Enterprise/EDU y RS4 y posteriores podrán ver la directiva en la siguiente ruta de acceso:</span><span class="sxs-lookup"><span data-stu-id="6e713-157">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="6e713-158">Esta opción solo está disponible como configuración del equipo; no hay una opción para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="6e713-158">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e713-159">Esta configuración del Registro no se almacena en una clave de directivas y se considera una *preferencia*.</span><span class="sxs-lookup"><span data-stu-id="6e713-159">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="6e713-160">Por lo tanto, si el objeto de directiva de grupo que implementa la configuración se quita alguna vez o si la directiva está establecida en **No configurada**, la opción se mantendrá.</span><span class="sxs-lookup"><span data-stu-id="6e713-160">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="6e713-161">Para desbloquear la distribución de Microsoft Edge (basado en Chromium) mediante la directiva de grupo, establece la directiva en **Deshabilitada**.</span><span class="sxs-lookup"><span data-stu-id="6e713-161">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="6e713-162">Consulta también</span><span class="sxs-lookup"><span data-stu-id="6e713-162">See also</span></span>

- [<span data-ttu-id="6e713-163">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="6e713-163">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="6e713-164">Actualizaciones de Windows para compatibilidad con Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6e713-164">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="6e713-165">Cómo acceder a la versión anterior de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6e713-165">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
