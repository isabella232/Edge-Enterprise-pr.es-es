---
title: Mantener la navegación en la página en modo Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Mantener la navegación en la página en modo Internet Explorer
ms.openlocfilehash: 20b18d121c3babfaacffd4a08316b25be714d95e
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641366"
---
# <a name="keep-in-page-navigation-in-internet-explorer-mode"></a><span data-ttu-id="373f2-103">Mantener la navegación en la página en modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="373f2-103">Keep in-page navigation in Internet Explorer mode</span></span>

<span data-ttu-id="373f2-104">Puedes usar esta directiva como solución temporal para forzar toda la navegación en la página de los sitios en modo Internet Explorer (modo IE) para que permanezca en modo IE.</span><span class="sxs-lookup"><span data-stu-id="373f2-104">You can use this policy as a temporary solution to force all in-page navigation from Internet Explorer mode (IE mode) sites to stay in IE mode.</span></span>

<span data-ttu-id="373f2-105">Una navegación en la página se inicia desde un vínculo, un script o un formulario en la página actual.</span><span class="sxs-lookup"><span data-stu-id="373f2-105">An in-page navigation is started from a link, a script, or a form on the current page.</span></span> <span data-ttu-id="373f2-106">También puede ser un redireccionamiento de servidor de un intento de navegación en la página anterior.</span><span class="sxs-lookup"><span data-stu-id="373f2-106">It can also be a server-side redirect of a previous in-page navigation attempt.</span></span> <span data-ttu-id="373f2-107">Por otra parte, un usuario puede iniciar una navegación que no sea en la página y que sea independiente de la página actual, de varias formas con los controles del explorador.</span><span class="sxs-lookup"><span data-stu-id="373f2-107">Conversely, a user can start a navigation that isn't in-page that's independent of the current page in several ways by using the browser controls.</span></span> <span data-ttu-id="373f2-108">Por ejemplo, con la barra de direcciones, el botón Atrás o un vínculo favorito.</span><span class="sxs-lookup"><span data-stu-id="373f2-108">For example, using the address bar, the back button, or a favorite link.</span></span>

>[!NOTE]
><span data-ttu-id="373f2-109">Este artículo se aplica a Microsoft Edge, versión 81 o posterior.</span><span class="sxs-lookup"><span data-stu-id="373f2-109">This article applies to Microsoft Edge version 81 or later.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="373f2-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="373f2-110">Prerequisites</span></span>

<span data-ttu-id="373f2-111">Las siguientes actualizaciones de Windows son necesarias para esta directiva:</span><span class="sxs-lookup"><span data-stu-id="373f2-111">The following Windows updates are required for this policy:</span></span>

- <span data-ttu-id="373f2-112">Windows 10, versiones 1909 y 1903; Windows Server, versiones 1909 y 1903  ([KB4532695](https://support.microsoft.com/help/4532695))</span><span class="sxs-lookup"><span data-stu-id="373f2-112">Windows 10 version 1909 & 1903, Windows Server version 1909 & 1903  ([KB4532695](https://support.microsoft.com/help/4532695))</span></span>
- <span data-ttu-id="373f2-113">Windows 10, versión 1809; Windows Server, versión 1809; Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span><span class="sxs-lookup"><span data-stu-id="373f2-113">Windows 10 version 1809, Windows Server version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span></span>
- <span data-ttu-id="373f2-114">Windows 10, versión 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span><span class="sxs-lookup"><span data-stu-id="373f2-114">Windows 10 version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span></span>
- <span data-ttu-id="373f2-115">Windows 10, versión 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span><span class="sxs-lookup"><span data-stu-id="373f2-115">Windows 10 version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span></span>


## <a name="about-this-policy"></a><span data-ttu-id="373f2-116">Acerca de esta directiva</span><span class="sxs-lookup"><span data-stu-id="373f2-116">About this policy</span></span>

<span data-ttu-id="373f2-117">Esta directiva te proporciona tiempo para identificar y configurar todos los servidores de autenticación usados por los sitios en modo IE.</span><span class="sxs-lookup"><span data-stu-id="373f2-117">This policy gives you time to identify and configure all of the authentication servers used by your IE mode sites.</span></span> <span data-ttu-id="373f2-118">Sin embargo, esta directiva puede dar lugar a una experiencia de navegación incoherente, en la que algunos sitios se muestran en modo IE y en otras ocasiones se muestran en modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="373f2-118">However, this policy can result in an inconsistent browsing experience, where some sites are rendered in IE mode and at other times rendered in Microsoft Edge mode.</span></span> <span data-ttu-id="373f2-119">Esta experiencia depende de si la navegación al sitio comenzó desde una página en modo IE.</span><span class="sxs-lookup"><span data-stu-id="373f2-119">This experience depends on whether the navigation to the site began from an IE mode page.</span></span> <span data-ttu-id="373f2-120">Cualquier sitio que no se haya configurado explícitamente para abrirse en un motor de procesamiento específico estará sujeto a esta incoherencia.</span><span class="sxs-lookup"><span data-stu-id="373f2-120">Any site that isn't explicitly configured to open in a specific rendering engine will be subject to this inconsistency.</span></span>

<span data-ttu-id="373f2-121">Si habilitas esta directiva, se recomienda que la deshabilites después de que hayas identificado todos los servidores de autenticación y los hayas agregado como neutros a la lista de sitios.</span><span class="sxs-lookup"><span data-stu-id="373f2-121">If you enable this policy, we recommend that you disable it after you've identified all the authentication servers and added them to the site list as neutral.</span></span> <span data-ttu-id="373f2-122">De esta forma, te asegurarás de que los sitios modernos nunca se muestren accidentalmente en modo IE.</span><span class="sxs-lookup"><span data-stu-id="373f2-122">This action ensures that your modern sites never inadvertently render in IE mode.</span></span>

## <a name="keep-in-page-navigation-in-ie-mode"></a><span data-ttu-id="373f2-123">Mantener la navegación en la página en modo IE</span><span class="sxs-lookup"><span data-stu-id="373f2-123">Keep in-page navigation in IE mode</span></span>

<span data-ttu-id="373f2-124">Para mantener toda la navegación en la página o la automática en modo Internet Explorer, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="373f2-124">To keep automatic or all in-page navigation in Internet Explorer mode, follow these steps:</span></span>

1. <span data-ttu-id="373f2-125">Abre el Editor de directivas de grupo local.</span><span class="sxs-lookup"><span data-stu-id="373f2-125">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="373f2-126">Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="373f2-126">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="373f2-127">En **Configuración**, haz doble clic en **Especifica cómo se comportan las navegaciones "en la página" de los sitios no configurados al iniciarse en las páginas en modo Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="373f2-127">Under **Setting**, double-click **Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages**.</span></span>

   ![Configuración de directiva en la página](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. <span data-ttu-id="373f2-129">Selecciona **Habilitada**</span><span class="sxs-lookup"><span data-stu-id="373f2-129">Select **Enabled**</span></span> 

   ![Habilitar directiva en la página](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. <span data-ttu-id="373f2-131">En la lista desplegable, elije una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="373f2-131">Choose one of the following options from the dropdown list:</span></span>

   - <span data-ttu-id="373f2-132">**Predeterminada** - Solo los sitios configurados para abrirse en el modo Internet Explorer se abrirán en ese modo.</span><span class="sxs-lookup"><span data-stu-id="373f2-132">**Default** - Only sites configured to open in Internet Explorer mode will open in that mode.</span></span> <span data-ttu-id="373f2-133">Cualquier sitio que no esté configurado para abrirse en modo Internet Explorer se redirigirá a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="373f2-133">Any site not configured to open in Internet Explorer mode will be redirected back to Microsoft Edge.</span></span>
   - <span data-ttu-id="373f2-134">**Mantener solo las navegaciones automáticas en modo Internet Explorer**: Usa esta opción si quieres la experiencia predeterminada, pero que todas las navegaciones automáticas (como las redirecciones 302) a sitios no configurados se mantengan en modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="373f2-134">**Keep only automatic navigations in Internet Explorer mode** - Use this option if you want the default experience except that all automatic navigations (such as 302 redirects) to unconfigured sites will be kept in Internet Explorer mode.</span></span>
   - <span data-ttu-id="373f2-135">**Mantener toda la navegación en la página en modo Internet Explorer**  \* *_(Menos recomendado)_*_ : todas las navegaciónes de páginas cargadas en modo IE a sitios no configurados se mantienen en modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="373f2-135">**Keep all in-page navigation in Internet Explorer mode** \**_(Least Recommended)_*_ - All navigations from pages loaded in IE mode to unconfigured sites are kept in Internet Explorer mode.</span></span>

6. <span data-ttu-id="373f2-136">Haga clic en _*Aceptar*\* **o Aplicar** para guardar la configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="373f2-136">Click _*OK*\* or **Apply** to save the policy settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="373f2-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="373f2-137">See also</span></span>

- [<span data-ttu-id="373f2-138">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="373f2-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
