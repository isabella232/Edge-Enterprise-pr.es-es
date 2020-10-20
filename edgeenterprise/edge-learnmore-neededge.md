---
title: Redirección de Internet Explorer a Microsoft Edge por motivos de compatibilidad con sitios web modernos
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 10/19/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Redirección de Internet Explorer a Microsoft Edge por motivos de compatibilidad con sitios web modernos
ms.openlocfilehash: ce9e8dabdff25cc3ba375746ec82ddd78b6d7694
ms.sourcegitcommit: cf991cc4bd2e70169902cbda9ddc870d70e31ca2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120525"
---
# <span data-ttu-id="2a4a4-103">Redirección de Internet Explorer a Microsoft Edge por motivos de compatibilidad con sitios web modernos</span><span class="sxs-lookup"><span data-stu-id="2a4a4-103">Redirection from Internet Explorer to Microsoft Edge for compatibility with modern web sites</span></span>

> [!NOTE]
> <span data-ttu-id="2a4a4-104">Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-104">This article applies to Microsoft Edge Stable version 87 or later.</span></span>

## <span data-ttu-id="2a4a4-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="2a4a4-105">Overview</span></span>

<span data-ttu-id="2a4a4-106">Muchos sitios web modernos tienen diseños que no son compatibles con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-106">Many modern websites have designs that are incompatible with Internet Explorer.</span></span> <span data-ttu-id="2a4a4-107">Siempre que un usuario de Internet Explorer visite un sitio público incompatible, recibirá un mensaje en el que se indicará que el sitio no es compatible con el explorador y tendrá que cambiar de forma manual a otro explorador.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-107">Whenever an Internet Explorer user visits an incompatible public site, they get a message that tells them the site is incompatible with their browser, and they need to manually switch to a different browser.</span></span>

<span data-ttu-id="2a4a4-108">La necesidad de cambiar manualmente a otro navegador diferente, cambia a partir de la versión estable de Microsoft Edge 87.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-108">The need to  manually switch to a different browser changes starting with Microsoft Edge Stable version 87.</span></span>

<span data-ttu-id="2a4a4-109">Cuando un usuario se dirige a un sitio que no es compatible con Internet Explorer, se le redirigirá automáticamente a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-109">When a user goes to a site that is incompatible with Internet Explorer, they will be automatically redirected to Microsoft Edge.</span></span> <span data-ttu-id="2a4a4-110">En este artículo se describe la experiencia de usuario para la redirección y las directivas de grupo que se usan para configurar o deshabilitar el redireccionamiento automático.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-110">This article describes the user experience for redirection and the group policies that are used to configure or disable automatic redirection.</span></span>

> [!NOTE]
> <span data-ttu-id="2a4a4-111">Microsoft mantiene una lista de todos los sitios que se sabe que son incompatibles con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-111">Microsoft maintains a list of all sites that are known to be incompatible with Internet Explorer.</span></span>

## <span data-ttu-id="2a4a4-112">Experiencia de redirección</span><span class="sxs-lookup"><span data-stu-id="2a4a4-112">Redirection experience</span></span>

<span data-ttu-id="2a4a4-113">En el redireccionamiento a Microsoft Edge, los usuarios se muestran en el cuadro de diálogo único en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-113">On redirection to Microsoft Edge, users are shown the one-time dialog in the next screenshot.</span></span> <span data-ttu-id="2a4a4-114">Este cuadro de diálogo explica por qué se les redirige y pide consentimiento para copiar los datos de exploración y las preferencias de Internet Explorer en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-114">This dialog explains why they're getting redirected and prompts for consent to copy their browsing data and preferences from Internet Explorer to Microsoft Edge.</span></span> <span data-ttu-id="2a4a4-115">Se importarán los siguientes datos de examen: favoritos, contraseñas, motores de búsqueda, pestañas abiertas, historial, configuración, cookies y la Página principal.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-115">The following browsing data will be imported: Favorites, Passwords, Search engines, open tabs, History, settings, cookies, and the Home Page.</span></span>

![Examen de notificación y solicitud para importar datos y preferencias.](media/edge-learnmore-neededge/neededge-dialog1.png)

<span data-ttu-id="2a4a4-117">Incluso si no dan su consentimiento al comprobar "traer siempre mis datos y preferencias de navegación de Internet Explorer", pueden hacer clic en **continuar explorando** para continuar la sesión.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-117">Even if they don't give their consent by checking "Always bring over my browsing data and preferences from Internet Explorer", they can click **Continue browsing** to continue their session.</span></span>

<span data-ttu-id="2a4a4-118">Por último, un banner de incompatibilidad con el sitio web, que se muestra en la siguiente captura de pantalla, aparece debajo de la barra de direcciones para cada redirección.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-118">Finally, a website incompatibility banner, shown in the next screenshot, appears below the address bar for every redirection.</span></span>

![Notificación sobre sitios modernos y preguntar si se establece Microsoft Edge como explorador predeterminado o explorar Microsoft Edge.](media/edge-learnmore-neededge/neededge-banner.png)

<span data-ttu-id="2a4a4-120">El anuncio de incompatibilidad del sitio web:</span><span class="sxs-lookup"><span data-stu-id="2a4a4-120">The website incompatibility banner:</span></span>

- <span data-ttu-id="2a4a4-121">alienta al usuario a cambiar a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2a4a4-121">encourages the user to switch to Microsoft Edge</span></span>
- <span data-ttu-id="2a4a4-122">pide establecer a Microsoft Edge como explorador predeterminado</span><span class="sxs-lookup"><span data-stu-id="2a4a4-122">offers to make Microsoft Edge as the default browser</span></span>
- <span data-ttu-id="2a4a4-123">ofrece al usuario la opción de explorar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-123">gives the user the option to explore Microsoft Edge</span></span>

<span data-ttu-id="2a4a4-124">Cuando se redirige un sitio de Internet Explorer a Microsoft Edge, la pestaña de Internet Explorer que comenzó a cargar el sitio se cierra si no tenía contenido anterior.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-124">When a site is redirected from Internet Explorer to Microsoft Edge, the Internet Explorer tab that started loading the site is closed if it had no prior content.</span></span> <span data-ttu-id="2a4a4-125">En caso contrario, la vista de pestañas activa va a una página de  [Soporte técnico de Microsoft](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) que explica por qué el sitio se redirigió a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-125">Otherwise, the active tab view goes to a  Microsoft [support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) page that explains why the site was redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="2a4a4-126">Después de que un usuario redireccionamiento pueda volver a usar Internet Explorer para los sitios que no están en la lista de compatibilidad de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-126">After a redirection users can go back to using Internet Explorer for sites that are not on the Internet Explorer incompatibility list.</span></span>  

## <span data-ttu-id="2a4a4-127">Directivas para configurar el redireccionamiento a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2a4a4-127">Policies to configure redirection to Microsoft Edge</span></span>

> [!NOTE]
> <span data-ttu-id="2a4a4-128">Estas directivas estarán disponibles como actualizaciones de archivos ADMX en el 26 de octubre de 2020, y estarán disponibles en Intune el 9 de noviembre de 2020.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-128">These policies will be available as ADMX file updates by October 26, 2020 and will be available in Intune by November 9, 2020.</span></span>

<span data-ttu-id="2a4a4-129">Se deben configurar tres directivas de grupo para habilitar el redireccionamiento automático a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-129">Three group policies must be configured to enable automatic redirection to Microsoft Edge.</span></span> <span data-ttu-id="2a4a4-130">Estas directivas son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="2a4a4-130">These policies are:</span></span>

- <span data-ttu-id="2a4a4-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="2a4a4-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>
- <span data-ttu-id="2a4a4-132">RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="2a4a4-132">RedirectSitesFromInternetExplorerRedirectMode</span></span>
- <span data-ttu-id="2a4a4-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="2a4a4-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

### <span data-ttu-id="2a4a4-134">Directiva: RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="2a4a4-134">Policy: RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>

<span data-ttu-id="2a4a4-135">El redireccionamiento de Internet Explorer a Microsoft Edge necesita un objeto de aplicación auxiliar de Internet Explorer (BHO) denominado "IEtoEdge BHO".</span><span class="sxs-lookup"><span data-stu-id="2a4a4-135">Redirection from Internet Explorer to Microsoft Edge requires an Internet Explorer Browser Helper Object (BHO) named "IEtoEdge BHO".</span></span> <span data-ttu-id="2a4a4-136">La Directiva **RedirectSitesFromInternetExplorerPreventBHOInstall** controla si este BHO está instalado.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-136">The **RedirectSitesFromInternetExplorerPreventBHOInstall** policy controls whether or not this BHO is installed.</span></span>  

- <span data-ttu-id="2a4a4-137">Si habilita esta Directiva, el BHO necesario para la redirección no se instalará y los usuarios podrán seguir viendo mensajes de incompatibilidad para determinados sitios web en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-137">If you enable this policy, the BHO required for redirection will not be installed and your users will continue to see incompatibility messages for certain websites on Internet Explorer.</span></span> <span data-ttu-id="2a4a4-138">Si el BHO ya está instalado, se desinstalará la próxima vez que se actualice el canal estable de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-138">If the BHO is already installed, it will be uninstalled the next time the Microsoft Edge Stable channel is updated.</span></span>
- <span data-ttu-id="2a4a4-139">Si deshabilita o no configura esta Directiva, se instalará el BHO.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-139">If you disable or don't configure this policy, the BHO will be installed.</span></span> <span data-ttu-id="2a4a4-140">Este es el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-140">This is the default behavior.</span></span>

<span data-ttu-id="2a4a4-141">Además de requerir el BHO, hay una dependencia en la **RedirectSitesFromInternetExplorerRedirectMode**, que se debe establecer en "sitelist" o "no configurado".</span><span class="sxs-lookup"><span data-stu-id="2a4a4-141">In addition to needing the BHO, there is a dependency on the **RedirectSitesFromInternetExplorerRedirectMode**, which needs to be set to "Sitelist" or "Not Configured".</span></span>

### <span data-ttu-id="2a4a4-142">Directiva: RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="2a4a4-142">Policy: RedirectSitesFromInternetExplorerRedirectMode</span></span>

 <span data-ttu-id="2a4a4-143">Esta Directiva corresponde al Microsoft Edge **explorador predeterminado** la configuración "permitir que Internet Explorer abra sitios en Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="2a4a4-143">This policy corresponds to the Microsoft Edge **Default browser** setting "Let Internet Explorer open sites in Microsoft Edge".</span></span> <span data-ttu-id="2a4a4-144">Para obtener acceso a esta configuración, vaya a la *edge://settings/defaultbrowser* URL.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-144">You can access this setting by going to the *edge://settings/defaultbrowser* URL.</span></span>  

- <span data-ttu-id="2a4a4-145">Si no configura esta Directiva o la configura en "sitelist", Internet Explorer redirigirá sitios incompatibles a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-145">If you don't configure this policy or set it to "Sitelist", Internet Explorer will redirect incompatible sites to Microsoft Edge.</span></span> <span data-ttu-id="2a4a4-146">Este es el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-146">This is the default behavior.</span></span>
- <span data-ttu-id="2a4a4-147">Si deshabilita esta Directiva, los sitios incompatibles no se redirigirán a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-147">If you disable this policy, incompatible sites aren't redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="2a4a4-148">Si se encuentra en un dispositivo personal que no está administrado por su organización, verá otra opción denominada "permitir que los sitios se carguen en modo Internet Explorer", en **Compatibilidad de Internet**. Explorer.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-148">If you're on a personal device that isn't  managed by your organization, you'll see another setting named "Allow sites to be loaded in Internet Explorer mode" under **Internet Explorer compatibility**.</span></span>
>
><span data-ttu-id="2a4a4-149">Si se encuentra en un dispositivo inscrito en un dominio Unido o en la administración de dispositivos móviles (MDM), no verá esta opción.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-149">If you're on a domain joined or Mobile Device Management (MDM) enrolled device, you won't see this option.</span></span>
>
> <span data-ttu-id="2a4a4-150">En su lugar, si quiere permitir que los usuarios carguen los sitios en el modo de Internet Explorer, puede hacerlo configurando la Directiva [permitir la realización de pruebas en el modo de Internet Explorer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).</span><span class="sxs-lookup"><span data-stu-id="2a4a4-150">Instead, if you want to let your users load sites in Internet Explorer mode, you can do so by configuring the policy [Allow Internet Explorer mode testing](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).</span></span>

### <span data-ttu-id="2a4a4-151">Directiva: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="2a4a4-151">Policy: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

<span data-ttu-id="2a4a4-152">Esta directiva configura la experiencia de usuario para la redirección del sitio no compatible con Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-152">This policy configures the user experience for incompatible site redirection to Microsoft Edge.</span></span>  

- <span data-ttu-id="2a4a4-153">Si habilita esta Directiva, los usuarios nunca verán el cuadro de diálogo de redirección y la pancarta de redirección.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-153">If you enable this policy, users never see the one-time redirection dialog and the redirection banner.</span></span> <span data-ttu-id="2a4a4-154">No se importan datos de explorador ni preferencias de usuario.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-154">No browser data or user preferences are imported.</span></span>
- <span data-ttu-id="2a4a4-155">Si deshabilita o no configura esta Directiva, el cuadro de diálogo de redirección se mostrará en la primera redirección y se mostrará el encabezado de redirección persistente para las sesiones que comiencen con una redirección.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-155">If you disable or don't configure this policy, the redirection dialog will be shown on the first redirection and the persistent redirection banner will be shown for sessions that start with a redirection.</span></span>

  > [!NOTE]
  > <span data-ttu-id="2a4a4-156">Los datos de búsqueda de usuarios se importarán cada vez que un usuario encuentre un nuevo redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-156">User browsing data will be imported every time a user encounters a new redirection.</span></span> <span data-ttu-id="2a4a4-157">Sin embargo, esto solo se produce si el usuario se ha enviado a la importación en el cuadro de diálogo redirección único.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-157">However, this only happens if the user consented to the import on the one-time redirection dialog.</span></span>

## <span data-ttu-id="2a4a4-158">Deshabilitar la redirección a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2a4a4-158">Disable redirection to Microsoft Edge</span></span>

<span data-ttu-id="2a4a4-159">Si desea deshabilitar la redirección antes de actualizar a la versión estable 87 de Microsoft Edge, siga el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="2a4a4-159">If you want to disable redirection BEFORE updating to Microsoft Edge Stable version 87, use the following step:</span></span>

1. <span data-ttu-id="2a4a4-160">Configure la drectiva **RedirectSitesFromInternetExplorerRedirectMode** como **Activada**..</span><span class="sxs-lookup"><span data-stu-id="2a4a4-160">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Enabled**.</span></span> <span data-ttu-id="2a4a4-161">Esta configuración dejará de redirigirse tan pronto como se aplique la drectiva.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-161">This setting will stop redirecting as soon as the policy takes effect.</span></span>

<span data-ttu-id="2a4a4-162">Si desea deshabilitar la redirección después de actualizar a la versión estable 87 de Microsoft Edge, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="2a4a4-162">If you want to disable redirection AFTER updating to Microsoft Edge Stable version 87, use the following steps:</span></span>

1. <span data-ttu-id="2a4a4-163">Configure la Directiva **RedirectSitesFromInternetExplorerRedirectMode** como **Deshabilitada**.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-163">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Disabled**.</span></span> <span data-ttu-id="2a4a4-164">Esta configuración dejará de redirigirse tan pronto como se aplique la drectiva.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-164">This setting will stop redirecting as soon as the policy takes effect.</span></span>
2. <span data-ttu-id="2a4a4-165">Configure la Directiva **RedirectSitesFromInternetExplorerPreventBHOInstall** en **Activada**.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-165">Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**.</span></span> <span data-ttu-id="2a4a4-166">Se desinstalará el BHO después de la siguiente actualización de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-166">This will uninstall the BHO after the next Microsoft Edge update.</span></span>

## <span data-ttu-id="2a4a4-167">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2a4a4-167">See also</span></span>

- [<span data-ttu-id="2a4a4-168">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="2a4a4-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="2a4a4-169">Directivas de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2a4a4-169">Microsoft Edge Policies</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies)