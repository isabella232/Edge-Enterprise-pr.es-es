---
title: Obtener acceso a la versión anterior de Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Obtén información acerca de cómo obtener acceso a la versión heredada de Microsoft Edge.
ms.openlocfilehash: e4733d020f3a681ded50e5a087fe086d39362201
ms.sourcegitcommit: f7f7eb69d2298b0f9779a9fd28e3c4e297ef2e05
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125522"
---
# <span data-ttu-id="ad929-103">Obtener acceso a la versión heredada de Microsoft Edge tras la instalación de la nueva versión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ad929-103">Access Microsoft Edge Legacy after installing the new version of Microsoft Edge</span></span>

<span data-ttu-id="ad929-104">Obtén información acerca de cómo obtener acceso a la versión heredada de Microsoft Edge tras la instalación de la nueva versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-104">Learn how to access Microsoft Edge Legacy after installing the new version of Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="ad929-105">Este artículo se aplica al [canal Estable](microsoft-edge-channels.md) de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-105">This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).</span></span>

<span data-ttu-id="ad929-106">Si bien la mayoría de las organizaciones querrán reemplazar Microsoft Edge heredado por la nueva versión, hay algunas situaciones en las que los usuarios necesitarán obtener acceso a ambas versiones.</span><span class="sxs-lookup"><span data-stu-id="ad929-106">While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions.</span></span> <span data-ttu-id="ad929-107">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ad929-107">For example:</span></span>

- <span data-ttu-id="ad929-108">Personal de soporte técnico y de asistencia que interactúa con usuarios que usan una o ambas versiones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-108">Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.</span></span>
- <span data-ttu-id="ad929-109">Desarrolladores que dan soporte a clientes que usan una o ambas versiones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-109">Developers who support customers who are using either or both versions of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad929-110">No se recomienda el uso para producción de Microsoft Edge (versión anterior) en paralelo con la nueva versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-110">Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production.</span></span> <span data-ttu-id="ad929-111">Esta configuración solo debería usarse en casos específicos en los que se necesitan pruebas con ambas versiones del explorador.</span><span class="sxs-lookup"><span data-stu-id="ad929-111">This configuration should only be used in specific cases where testing with both browser versions is required.</span></span>
>
> <span data-ttu-id="ad929-112">La aplicación de Microsoft Edge (versión anterior) llegará al fin de soporte el 9 de marzo de 2021 para dar paso al nuevo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-112">The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge.</span></span> <span data-ttu-id="ad929-113">Esto significa que Microsoft Edge (versión anterior) no recibirá actualizaciones de seguridad después de esa fecha.</span><span class="sxs-lookup"><span data-stu-id="ad929-113">This means that Microsoft Edge Legacy will not receive security updates after that date.</span></span> <span data-ttu-id="ad929-114">Este cambio se aplica a todas las experiencias que se ejecutan en la aplicación de escritorio de Microsoft Edge (versión anterior).</span><span class="sxs-lookup"><span data-stu-id="ad929-114">This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app.</span></span> <span data-ttu-id="ad929-115">[Más información](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span><span class="sxs-lookup"><span data-stu-id="ad929-115">[Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span></span>

## <span data-ttu-id="ad929-116">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="ad929-116">Before you begin</span></span>
> [!NOTE]
> <span data-ttu-id="ad929-117">A partir de la versión 20H2 de Windows 10, se dejará de incluir Microsoft Edge (versión anterior).</span><span class="sxs-lookup"><span data-stu-id="ad929-117">Starting with Windows 10 version 20H2 Microsoft Edge Legacy is no longer included.</span></span> <span data-ttu-id="ad929-118">A partir de esta versión de Windows 10, no se admite la experiencia en paralelo.</span><span class="sxs-lookup"><span data-stu-id="ad929-118">Starting with this version of Windows 10 the side-by-side experience is not supported.</span></span>

<span data-ttu-id="ad929-119">Los procedimientos descritos en este artículo se aplican a los sistemas que se han actualizado con las últimas actualizaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ad929-119">The procedures in this article apply to systems that have been updated with the latest security updates.</span></span> <span data-ttu-id="ad929-120">Cuando se instale la nueva versión de Microsoft Edge, se ocultará la versión antigua (Microsoft Edge [versión heredada]).</span><span class="sxs-lookup"><span data-stu-id="ad929-120">When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden.</span></span> <span data-ttu-id="ad929-121">De manera predeterminada, todos los intentos de iniciar la versión anterior redirigirán al usuario a la versión recientemente instalada de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-121">By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge.</span></span> <span data-ttu-id="ad929-122">En este artículo se describe cómo puede seguir usando Microsoft Edge heredado después de instalar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-122">This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.</span></span>

## <span data-ttu-id="ad929-123">Inicio rápido: experiencia en paralelo con el canal Microsoft Edge Beta y Microsoft Edge (versión anterior)</span><span class="sxs-lookup"><span data-stu-id="ad929-123">Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="ad929-124">Antes de usar las instrucciones detalladas de este artículo, tenga en cuenta los dos pasos siguientes para permitir que los usuarios ejecuten Microsoft Edge (versión anterior) y el [canal Microsoft Edge Beta](microsoft-edge-channels.md) en paralelo.</span><span class="sxs-lookup"><span data-stu-id="ad929-124">Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.</span></span>

1. <span data-ttu-id="ad929-125">Impide la instalación automática del canal estable de Microsoft Edge por parte de [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span><span class="sxs-lookup"><span data-stu-id="ad929-125">Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span></span>

   > [!TIP]
   > <span data-ttu-id="ad929-126">Usa el [kit de herramientas de bloqueo](microsoft-edge-blocker-toolkit.md) para deshabilitar la entrega automática de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-126">Use the [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) to disable automatic delivery of Microsoft Edge.</span></span>

2. <span data-ttu-id="ad929-127">Instale el [canal beta](https://www.microsoft.com/edge/business/download) de la nueva versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-127">Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ad929-128">Lea [información adicional](#additional-information) para obtener información sobre la configuración de las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="ad929-128">Read [Additional information](#additional-information) for information about Registry Key settings.</span></span>

<span data-ttu-id="ad929-129">Esta solución es menos compleja y requiere menos administración que la solución detallada descrita en este artículo.</span><span class="sxs-lookup"><span data-stu-id="ad929-129">This side-by-side solution is less complex and requires less management than the detailed solution described in this article.</span></span> <span data-ttu-id="ad929-130">Sin embargo, esto significa que ejecutará el canal Beta en lugar del canal estable.</span><span class="sxs-lookup"><span data-stu-id="ad929-130">However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.</span></span>

## <span data-ttu-id="ad929-131">Experiencia en paralelo con el canal estable de Microsoft Edge y Microsoft Edge (versión anterior)</span><span class="sxs-lookup"><span data-stu-id="ad929-131">Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="ad929-132">Si instala el canal estable de la siguiente versión de Microsoft Edge en el nivel del sistema, se ocultará la versión actual (Microsoft Edge heredado).</span><span class="sxs-lookup"><span data-stu-id="ad929-132">Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden.</span></span> <span data-ttu-id="ad929-133">Si desea permitir que los usuarios vean las dos versiones de Microsoft Edge en paralelo en Windows, puede habilitar esta experiencia si configura la directiva de grupo **Permitir la experiencia de exploradores Microsoft Edge en paralelo** como **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="ad929-133">If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.</span></span>

<span data-ttu-id="ad929-134">Esta directiva de grupo se documenta [aquí](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span><span class="sxs-lookup"><span data-stu-id="ad929-134">This group policy is documented [here](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span></span>

### <span data-ttu-id="ad929-135">Para configurar la directiva de experiencia de explorador en paralelo:</span><span class="sxs-lookup"><span data-stu-id="ad929-135">To set up the side-by-side browser experience policy:</span></span>

1. <span data-ttu-id="ad929-136">Instale las definiciones de directiva desde [Microsoft Edge para la empresa](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="ad929-136">Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span></span>

   - <span data-ttu-id="ad929-137">Elija el canal, la compilación y la plataforma que desee usar y haga clic en Obtener archivos de directiva.</span><span class="sxs-lookup"><span data-stu-id="ad929-137">Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.</span></span>
   - <span data-ttu-id="ad929-138">Extraiga los archivos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="ad929-138">Extract the zipped files.</span></span>
   - <span data-ttu-id="ad929-139">Copia msedge.admx y msedgeupdate.admx en el directorio `C:\Windows\PolicyDefinitions`.</span><span class="sxs-lookup"><span data-stu-id="ad929-139">Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.</span></span>
   - <span data-ttu-id="ad929-140">Copie msedge.adml y msedgeupdate.adml (del directorio correspondiente del idioma o la configuración regional) en el directorio `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]`.</span><span class="sxs-lookup"><span data-stu-id="ad929-140">Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.</span></span>

2. <span data-ttu-id="ad929-141">Abre el Editor de directivas de grupo (gpedit.msc).</span><span class="sxs-lookup"><span data-stu-id="ad929-141">Open the Group Policy Editor (gpedit.msc).</span></span>
3. <span data-ttu-id="ad929-142">En **Configuración del equipo**, ve a *Plantillas administrativas > Microsoft Edge Update > Aplicaciones*.</span><span class="sxs-lookup"><span data-stu-id="ad929-142">Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ad929-143">Si no ve la carpeta *Microsoft Edge Update*, compruebe que el paso 1 se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad929-143">If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.</span></span>

4. <span data-ttu-id="ad929-144">En **Aplicaciones**, haz doble clic en "Permitir la experiencia en paralelo de exploradores Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="ad929-144">Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience".</span></span> <span data-ttu-id="ad929-145">Consulta nuestras [directrices de procedimientos recomendados](#best-practice-guidance) antes de continuar con el siguiente paso.</span><span class="sxs-lookup"><span data-stu-id="ad929-145">See our [best practice guidance](#best-practice-guidance) before continuing to the next step.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ad929-146">De forma predeterminada, esta directiva de grupo está establecida en "Sin configurar", lo que hace que se oculte Microsoft Edge (versión heredada) cuando la nueva versión de Microsoft Edge está instalada.</span><span class="sxs-lookup"><span data-stu-id="ad929-146">By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.</span></span>

5. <span data-ttu-id="ad929-147">Selecciona **Habilitada** y, después, haz clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ad929-147">Select **Enabled** and then click **OK**.</span></span>  

<span data-ttu-id="ad929-148">Al configurar esta directiva, se establecerá la siguiente clave de registro en '00000001':</span><span class="sxs-lookup"><span data-stu-id="ad929-148">Setting this policy will set the following Registry Key  to '00000001':</span></span>

- <span data-ttu-id="ad929-149">Clave:</span><span class="sxs-lookup"><span data-stu-id="ad929-149">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- <span data-ttu-id="ad929-150">Nombre del valor:</span><span class="sxs-lookup"><span data-stu-id="ad929-150">Value Name:</span></span> `Allowsxs`
- <span data-ttu-id="ad929-151">Tipo de valor:</span><span class="sxs-lookup"><span data-stu-id="ad929-151">Value Type:</span></span> `'REG_DWORD'`

#### <span data-ttu-id="ad929-152">Instrucciones de prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="ad929-152">Best practice guidance</span></span>

<span data-ttu-id="ad929-153">Para disfrutar de la mejor experiencia **Permitir la experiencia de exploradores Microsoft Edge en paralelo** debería estar habilitada antes de que se implemente la nueva versión de Microsoft Edge en los dispositivos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ad929-153">For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.</span></span>

<span data-ttu-id="ad929-154">Si la directiva de grupo está habilitada después de implementar Microsoft Edge, tendrá los siguientes efectos secundarios y acciones requeridas:</span><span class="sxs-lookup"><span data-stu-id="ad929-154">If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:</span></span>

1. <span data-ttu-id="ad929-155">**Permitir la experiencia de exploradores Microsoft Edge en paralelo** no surtirá efecto hasta hasta después de que se vuelva a ejecutar el instalador para la nueva versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-155">**Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ad929-156">El instalador se puede ejecutar directamente o de manera automática cuando se actualice la nueva versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-156">The installer can be run directly or automatically when the new version of Microsoft Edge updates.</span></span>

2. <span data-ttu-id="ad929-157">Microsoft Edge (versión heredada) tendrá que volverse a anclar a Inicio o a la barra de tareas porque el anclaje se migra cuando se implementa la nueva versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-157">Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.</span></span>
3. <span data-ttu-id="ad929-158">Los sitios que se anclaron a Inicio o a la barra de tareas para Microsoft Edge (versión heredada) se migrarán a la nueva versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-158">Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.</span></span>

## <span data-ttu-id="ad929-159">Información adicional</span><span class="sxs-lookup"><span data-stu-id="ad929-159">Additional information</span></span>

<span data-ttu-id="ad929-160">Una vez que se han actualizado por completo los sistemas y se ha instalado el canal estable de la próxima versión de Microsoft Edge, se establecen la siguiente clave del Registro y valor:</span><span class="sxs-lookup"><span data-stu-id="ad929-160">After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:</span></span>

- <span data-ttu-id="ad929-161">Clave:</span><span class="sxs-lookup"><span data-stu-id="ad929-161">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- <span data-ttu-id="ad929-162">Valor de la clave:</span><span class="sxs-lookup"><span data-stu-id="ad929-162">Key value:</span></span> `BrowserReplacement`

  > [!IMPORTANT]
  > <span data-ttu-id="ad929-163">Esta clave se sobrescribe cada vez que se actualiza el canal estable Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-163">This key is over-written every time the Microsoft Edge Stable channel is updated.</span></span> <span data-ttu-id="ad929-164">Como práctica recomendada, se aconseja que NO elimines esta clave para permitir que los usuarios accedan a las dos versiones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ad929-164">As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.</span></span>

## <span data-ttu-id="ad929-165">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ad929-165">See also</span></span>

- [<span data-ttu-id="ad929-166">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ad929-166">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ad929-167">Actualizaciones de Windows para compatibilidad con Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ad929-167">Windows updates to support Microsoft Edge</span></span>](microsoft-edge-sysupdate-windows-updates.md)
