---
title: Deshabilitar Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Obtenga información sobre cómo deshabilitar Internet Explorer 11 y usar el modo de Internet Explorer en Microsoft Edge.
ms.openlocfilehash: a0486c2965b1868db67b6de1423f279905074410
ms.sourcegitcommit: f34ff11499a2b96941e704103bdd959d19e3d7e7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400610"
---
# <a name="disable-internet-explorer-11"></a><span data-ttu-id="5266f-103">Deshabilitar Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="5266f-103">Disable Internet Explorer 11</span></span>

<span data-ttu-id="5266f-104">En este artículo se describe cómo deshabilitar Internet Explorer 11 como un explorador independiente en su entorno.</span><span class="sxs-lookup"><span data-stu-id="5266f-104">This article describes how to disable Internet Explorer 11 as a standalone browser in your environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5266f-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5266f-105">Prerequisites</span></span>

<span data-ttu-id="5266f-106">Son necesarias las siguientes actualizaciones de Windows y el software Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="5266f-106">The following Windows updates and Microsoft Edge software are required:</span></span>

- <span data-ttu-id="5266f-107">Actualizaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="5266f-107">Windows updates</span></span>

  - <span data-ttu-id="5266f-108">Windows 10, versión 2004, Windows Server versión 2004, Windows 10, versión 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b)</span><span class="sxs-lookup"><span data-stu-id="5266f-108">Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) or later</span></span>
  - <span data-ttu-id="5266f-109">Windows 10, versión 1909, Windows Server versión 1909 [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) o posterior</span><span class="sxs-lookup"><span data-stu-id="5266f-109">Windows 10 version 1909, Windows Server version 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) or later</span></span>
  - <span data-ttu-id="5266f-110">Windows 10, versión 1809, Windows Server, versión 1809, y Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) o posterior</span><span class="sxs-lookup"><span data-stu-id="5266f-110">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) or later</span></span>
  - <span data-ttu-id="5266f-111">Windows 10, versión 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) o posterior</span><span class="sxs-lookup"><span data-stu-id="5266f-111">Windows 10, version 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) or later</span></span>
   - <span data-ttu-id="5266f-112">Versión inicial de Windows 10 (julio de 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) o posterior</span><span class="sxs-lookup"><span data-stu-id="5266f-112">Windows 10 initial version (July 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) or later</span></span>
  - <span data-ttu-id="5266f-113">Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) o posterior</span><span class="sxs-lookup"><span data-stu-id="5266f-113">Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) or later</span></span>
  - <span data-ttu-id="5266f-114">Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) o posterior</span><span class="sxs-lookup"><span data-stu-id="5266f-114">Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) or later</span></span>
  
- <span data-ttu-id="5266f-115">Canal Estable de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5266f-115">Microsoft Edge Stable Channel</span></span>


## <a name="overview"></a><span data-ttu-id="5266f-116">Introducción</span><span class="sxs-lookup"><span data-stu-id="5266f-116">Overview</span></span>

<span data-ttu-id="5266f-117">Para las organizaciones que necesitan Internet Explorer 11 (IE11) para compatibilidad heredada, el modo de Internet Explorer (modo IE) en Microsoft Edge proporciona una experiencia de explorador única y sin ningún problema.</span><span class="sxs-lookup"><span data-stu-id="5266f-117">For organizations that require Internet Explorer 11 (IE11) for legacy compatibility, Internet Explorer mode (IE mode) on Microsoft Edge provides a seamless, single browser experience.</span></span> <span data-ttu-id="5266f-118">Los usuarios pueden acceder a las aplicaciones heredadas desde Microsoft Edge sin tener que volver a IE11.</span><span class="sxs-lookup"><span data-stu-id="5266f-118">Users can access legacy applications from within Microsoft Edge without having to switch back to IE11.</span></span>

<span data-ttu-id="5266f-119">Después de configurar el modo IE, puede deshabilitar IE11 como explorador independiente **sin afectar a la funcionalidad del modo IE** toda la organización mediante directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="5266f-119">After you configure IE mode, you can disable IE11 as a standalone browser **without affecting IE mode functionality** across your organization using group policy.</span></span>

> [!NOTE]
> <span data-ttu-id="5266f-120">Si necesita la aplicación independiente IE11 para sitios específicos y quiere redirigir todo el tráfico del explorador a Microsoft Edge, puede configurar la política[Enviar todos los sitios que no están incluidos en la lista de sitios a Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) para redirigir sitios de IE a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5266f-120">If you need the standalone IE11 app for specific sites, and want to redirect all other browser traffic to Microsoft Edge, you can configure the [Send all sites not included in the site list to Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) policy to redirect sites from IE to Microsoft Edge.</span></span>

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a><span data-ttu-id="5266f-121">Experiencia del usuario después de redirigir tráfico a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5266f-121">User experience after redirecting traffic to Microsoft Edge</span></span>

<span data-ttu-id="5266f-122">Cuando habilita la política de **Deshabilitar Internet Explorer 11 como navegador independiente**, toda la actividad de IE11 se redirige a Microsoft Edge y los usuarios tienen la siguiente experiencia:</span><span class="sxs-lookup"><span data-stu-id="5266f-122">When you enable the **Disable Internet Explorer 11 as a standalone browser** policy, all IE11 activity is redirected to Microsoft Edge and users have the following experience:</span></span>

- <span data-ttu-id="5266f-123">Se quitará el icono IE11 del menú Inicio, pero se mantendrá el de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="5266f-123">The IE11 icon on the Start Menu will be removed, but the one on the taskbar will remain.</span></span>
- <span data-ttu-id="5266f-124">Cuando los usuarios intentan iniciar accesos directos o asociaciones de archivos que usan IE11, se les redirige para abrir el mismo archivo/URL en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5266f-124">When users try to launch shortcuts or file associations that use IE11, they will be redirected to open the same file/URL in Microsoft Edge.</span></span>
- <span data-ttu-id="5266f-125">Cuando los usuarios intentan iniciar IE11 invocando directamente el archivo binario iexplore.exe, se iniciará Microsoft Edge en su lugar.</span><span class="sxs-lookup"><span data-stu-id="5266f-125">When users try to launch IE11 by directly invoking the iexplore.exe binary, Microsoft Edge will launch instead.</span></span>

<span data-ttu-id="5266f-126">Como parte de la configuración de la directiva para esta experiencia, de manera opcional, puede mostrar un mensaje de redirección para cada usuario que intente iniciar IE11.</span><span class="sxs-lookup"><span data-stu-id="5266f-126">As part of setting the policy for this experience, you can optionally show a redirect message for each user who tries to launch IE11.</span></span> <span data-ttu-id="5266f-127">Este mensaje se puede establecer para mostrar "Siempre" o "Una vez por usuario".</span><span class="sxs-lookup"><span data-stu-id="5266f-127">This message can be set to display "Always" or "Once per user".</span></span> <span data-ttu-id="5266f-128">De forma predeterminada, el mensaje de redirección que se muestra en la siguiente captura de pantalla nunca se muestra.</span><span class="sxs-lookup"><span data-stu-id="5266f-128">By default, the redirect message shown in the next screenshot is never shown.</span></span>

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Aviso al intentar abrir IE después de que se active una redirección a Microsoft Edge.":::

<span data-ttu-id="5266f-130">Si la lista de sitios del modo de empresa contiene aplicaciones que están configuradas para abrirse en la aplicación IE11 y deshabilita IE11 con esta directiva, se abrirán en modo IE en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5266f-130">If your Enterprise Mode Site List contains applications that are configured to open in the IE11 app and you disable IE11 with this policy, they will open in IE mode on Microsoft Edge.</span></span>
> [!NOTE]
> <span data-ttu-id="5266f-131">Hay un problema conocido con el flujo de usuario cuando un sitio está configurado para abrirse en IE11 y se establece la directiva Deshabilitar IE11.</span><span class="sxs-lookup"><span data-stu-id="5266f-131">There is a known issue with the user flow when a site is configured to open in IE11 and the disable IE11 policy is set.</span></span> <span data-ttu-id="5266f-132">El problema se está investigando de forma activa.</span><span class="sxs-lookup"><span data-stu-id="5266f-132">The issue being actively investigated.</span></span>

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a><span data-ttu-id="5266f-133">Deshabilitar Internet Explorer 11 como explorador independiente</span><span class="sxs-lookup"><span data-stu-id="5266f-133">Disable Internet Explorer 11 as a standalone browser</span></span>

<span data-ttu-id="5266f-134">Para deshabilitar Internet Explorer 11 con una directiva de grupo, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="5266f-134">To disable Internet Explorer 11 using group policy, follow these steps:</span></span>

1. <span data-ttu-id="5266f-135">Asegúrese de que tiene las actualizaciones del sistema operativo necesarias previamente.</span><span class="sxs-lookup"><span data-stu-id="5266f-135">Ensure you have the pre-requisite operating system updates.</span></span> <span data-ttu-id="5266f-136">Este paso actualizará los archivos ADMX directamente en el equipo (específicamente inetres.adml e inetres.admx).</span><span class="sxs-lookup"><span data-stu-id="5266f-136">This step will update the ADMX files on your machine directly (specifically inetres.adml and inetres.admx).</span></span> <span data-ttu-id="5266f-137">Tenga en cuenta que si quiere actualizar la Tienda central, deberá copiar los archivos .adml y .admx de una máquina que tenga las actualizaciones previas.</span><span class="sxs-lookup"><span data-stu-id="5266f-137">Please note that if you want to update your Central Store, you will need to copy over the .adml and .admx files from a machine that has the pre-requisite updates.</span></span> <span data-ttu-id="5266f-138">Para más información, consulte [Crear y administrar la Tienda central](https://docs.microsoft.com/troubleshoot/windows-client/group-policy/create-and-manage-central-store)</span><span class="sxs-lookup"><span data-stu-id="5266f-138">For more information, see [Create and manage Central Store](https://docs.microsoft.com/troubleshoot/windows-client/group-policy/create-and-manage-central-store)</span></span>
2. <span data-ttu-id="5266f-139">Abra el editor de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="5266f-139">Open the Group Policy Editor.</span></span>
3. <span data-ttu-id="5266f-140">Vaya a ***configuración del equipo/Plantillas administrativas/Componentes de Windows/Internet Explorer***.</span><span class="sxs-lookup"><span data-stu-id="5266f-140">Go to ***Computer Configuration/Administrative Templates/Windows Components/Internet Explorer***.</span></span> 
4. <span data-ttu-id="5266f-141">Haga doble clic en **Deshabilitar Internet Explorer 11 como explorador independiente**.</span><span class="sxs-lookup"><span data-stu-id="5266f-141">Double-click **Disable Internet Explorer 11 as a standalone browser**.</span></span>
5. <span data-ttu-id="5266f-142">Seleccione **habilitada**.</span><span class="sxs-lookup"><span data-stu-id="5266f-142">Select **Enabled**.</span></span>
6. <span data-ttu-id="5266f-143">En **de**opciones, elija uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="5266f-143">Under **Options**, pick one of the following values:</span></span>

   - <span data-ttu-id="5266f-144">**No** si no desea notificar a los usuarios que IE11 está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5266f-144">**Never** if you don’t want to notify users that IE11 is disabled.</span></span>
   - <span data-ttu-id="5266f-145">**tenga** siempre si desea notificar a los usuarios cada vez que se les redirija desde IE11.</span><span class="sxs-lookup"><span data-stu-id="5266f-145">**Always** if you want to notify users every time they're redirected from IE11.</span></span>
   - <span data-ttu-id="5266f-146">**una vez por usuario** si desea notificar a los usuarios solo la primera vez que se les redirige.</span><span class="sxs-lookup"><span data-stu-id="5266f-146">**Once per user** if you want to notify users only the first time they are redirected.</span></span>

7. <span data-ttu-id="5266f-147">Haga **clic en Aceptar** o **aplicar** para guardar esta configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="5266f-147">Click **OK** or **Apply** to save this policy setting.</span></span>

## <a name="see-also"></a><span data-ttu-id="5266f-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="5266f-148">See also</span></span>

- [<span data-ttu-id="5266f-149">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="5266f-149">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="5266f-150">Acerca del modo IE</span><span class="sxs-lookup"><span data-stu-id="5266f-150">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="5266f-151">Información adicional del modo de empresa</span><span class="sxs-lookup"><span data-stu-id="5266f-151">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
