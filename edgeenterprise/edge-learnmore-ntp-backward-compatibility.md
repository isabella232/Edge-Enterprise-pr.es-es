---
title: Compatibilidad con versiones anteriores para la página de nueva pestaña para empresas
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 10/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Compatibilidad con versiones anteriores para la página de nueva pestaña para empresas
ms.openlocfilehash: c10671a6ec8e1ff4dcb0db3f3c085f82ae973122
ms.sourcegitcommit: af6ab070d0c09bca4a9cf505b107ed7e04839763
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/29/2020
ms.locfileid: "11144501"
---
# <span data-ttu-id="9cce7-103">Compatibilidad con versiones anteriores para la página de nueva pestaña para empresas</span><span class="sxs-lookup"><span data-stu-id="9cce7-103">Backwards compatibility for the Enterprise New tab page</span></span>

<span data-ttu-id="9cce7-104">Este artículo describe el cambio de la página de la Nueva pestaña y cómo los usuarios pueden ser compatibles con la versión 87 y anteriores de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9cce7-104">This article describes the change to the New tab page and how users can be backwards compatible with Microsoft Edge version 87 and earlier.</span></span>

> [!NOTE]
> <span data-ttu-id="9cce7-105">Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9cce7-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="9cce7-106">Fuentes de información desde un único extremo</span><span class="sxs-lookup"><span data-stu-id="9cce7-106">Information feeds from single endpoint</span></span>

<span data-ttu-id="9cce7-107">La nueva versión de la página de nueva pestaña para empresas combina el contenido compatible con Microsoft 365 con información relevante para el sector que se sirve a través del punto de conexión de MSN.com.</span><span class="sxs-lookup"><span data-stu-id="9cce7-107">The new version of the Enterprise New tab page combines compliant Microsoft 365 content with industry relevant and compliant information feeds that are served via the MSN.com endpoint.</span></span>

> [!NOTE]
> <span data-ttu-id="9cce7-108">El contenido de Office 365 se sirvió originalmente utilizando el dominio [Office.com](https://www.office.com).</span><span class="sxs-lookup"><span data-stu-id="9cce7-108">Office 365 content was originally served using the [Office.com](https://www.office.com) domain.</span></span>

<span data-ttu-id="9cce7-109">Si el acceso al dominio MSN.com está restringido para su organización, le recomendamos encarecidamente que le dé a los usuarios acceso a esta [url](https://ntp.msn.com).</span><span class="sxs-lookup"><span data-stu-id="9cce7-109">If access to the MSN.com domain is restricted for your organization, we strongly recommend giving users access to this [url](https://ntp.msn.com).</span></span>

<span data-ttu-id="9cce7-110">Si necesita más tiempo para habilitar el acceso al dominio de MSN, le recomendamos que utilice el [NewTabPageSetFeedType](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagesetfeedtype), que le permite elegir la experiencia de alimentación de Microsoft News u Office 365 para la nueva página de pestañas.</span><span class="sxs-lookup"><span data-stu-id="9cce7-110">If you need more time to enable access to the MSN domain, we recommend using the [NewTabPageSetFeedType](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagesetfeedtype), that lets you choose either the Microsoft News or Office 365 feed experience for the new tab page.</span></span>

### <span data-ttu-id="9cce7-111">Seguir usando Office.com</span><span class="sxs-lookup"><span data-stu-id="9cce7-111">Keep using Office.com</span></span>

 <span data-ttu-id="9cce7-112">Puede configurar la directiva **NewTabPageSetFeedType** para seguir usando el dominio obsoleto Office.com.</span><span class="sxs-lookup"><span data-stu-id="9cce7-112">You can configure the **NewTabPageSetFeedType** policy to keep using the deprecated Office.com domain.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9cce7-113">La directiva **NewTabPageSetFeedType** y el dominio Office.com que sirve el contenido de Office 365 dejarán de funcionar cuando se publique la versión 90 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9cce7-113">The **NewTabPageSetFeedType** policy and the Office.com domain that serves Office 365 content will quit working when Microsoft Edge version 90 is released.</span></span>

<span data-ttu-id="9cce7-114">La siguiente configuración de la directiva obligará a la página de la Nueva pestaña de la empresa a mostrar el contenido de los documentos de Office desde el dominio Office.com.</span><span class="sxs-lookup"><span data-stu-id="9cce7-114">The following policy settings will force the Enterprise New tab page to render Office document content from the Office.com domain.</span></span>

- <span data-ttu-id="9cce7-115">Establezca la directiva como **Obligatoria**.</span><span class="sxs-lookup"><span data-stu-id="9cce7-115">Set the policy as **Mandatory**.</span></span>
- <span data-ttu-id="9cce7-116">Establezca el valor del asignación de directivas en **Office (1) = Office 365 alimenta la experiencia**.</span><span class="sxs-lookup"><span data-stu-id="9cce7-116">Set the value of the policy mapping to **Office (1) = Office 365 feed experience**.</span></span>

<span data-ttu-id="9cce7-117">Si el cambio a Office.com no es posible, comuníquese con nosotros y envíenos sus comentarios.</span><span class="sxs-lookup"><span data-stu-id="9cce7-117">If the switch to the Office.com isn't possible, reach out and send us feedback.</span></span> <span data-ttu-id="9cce7-118">Otra opción es configurar [NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) para que apunte a una URL de extremo que esté permitida por su organización.</span><span class="sxs-lookup"><span data-stu-id="9cce7-118">Another option is to configure the [NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) so it points to an endpoint URL that's allowed by your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="9cce7-119">La directiva **NewTabPageLocation** tiene prioridad si la directiva **NewTabPageSetFeedType** también está configurada.</span><span class="sxs-lookup"><span data-stu-id="9cce7-119">The **NewTabPageLocation** policy has precedence if the **NewTabPageSetFeedType** policy is also configured.</span></span>

## <span data-ttu-id="9cce7-120">Los usuarios de empresas recibirán ahora el contenido de las noticias de Microsoft a través de Mi fuente</span><span class="sxs-lookup"><span data-stu-id="9cce7-120">Enterprise users will now get Microsoft news content via My Feed</span></span>

<span data-ttu-id="9cce7-121">La página de nueva pestaña de empresa ofrecerá información relevante para el sector en el contenido de **Mi fuente** y Office 365 en una sola vista para los usuarios que hayan iniciado sesión con su cuenta de Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="9cce7-121">The Enterprise New tab page will offer industry relevant information in **My Feed** and Office 365 content in a single view for users signed in with their Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="9cce7-122">Para los usuarios que iniciaron sesión con su Azure Active Directory (Azure AD) y que seleccionaron la opción Microsoft News en el control flotante de configuración, su vista de la página de nueva pestañas será reemplazada por el contenido de **Mi fuente**.</span><span class="sxs-lookup"><span data-stu-id="9cce7-122">For users signed in with their Azure Active Directory (Azure AD) who selected the Microsoft News option in the settings flyout, their new tab page view will be replaced with **My Feed** content.</span></span> <span data-ttu-id="9cce7-123">Cuando abran una nueva pestaña en el navegador se verá como en el ejemplo en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9cce7-123">When they open a new tab page in the browser it will look like the example in the next screenshot.</span></span>

![Página de nueva pestañas que muestra el contenido de Mi fuente.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> <span data-ttu-id="9cce7-125">Los usuarios que no hayan iniciado sesión con Azure AD continuarán viendo la fuente de noticias de MSN cuando abran una nueva pestaña.</span><span class="sxs-lookup"><span data-stu-id="9cce7-125">Users who aren't signed in with Azure AD will continue to see the MSN News feed when they open a new tab.</span></span>

## <span data-ttu-id="9cce7-126">Diseño de página</span><span class="sxs-lookup"><span data-stu-id="9cce7-126">Page layout</span></span>

<span data-ttu-id="9cce7-127">Con los cambios en la página de nueva pestaña, el diseño de la página ya no tiene que controlar dos tipos de contenido específicos (Office 365 y Microsoft News), por lo que el cambio de contenido no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9cce7-127">With the changes to the New tab page, the Page layout no longer has to control two specific content types (Office 365 and Microsoft News), so the content toggle isn't available.</span></span> <span data-ttu-id="9cce7-128">La siguiente captura de pantalla muestra el control flotante para el diseño de la página</span><span class="sxs-lookup"><span data-stu-id="9cce7-128">The next screenshot shows the flyout for the Page layout.</span></span>

![Vista de diseño de página de nueva pestaña.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

<span data-ttu-id="9cce7-130">Si desea seguir teniendo acceso al contenido de las Microsoft News que no está vinculado a su organización, debe utilizar un perfil de explorador diferente.</span><span class="sxs-lookup"><span data-stu-id="9cce7-130">If you want to keep accessing Microsoft News content that isn't tied to your organization, you must use a different browser profile.</span></span> <span data-ttu-id="9cce7-131">Vaya a *"edge://settings/profiles"* y cierre sesión en su perfil de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9cce7-131">Go to  *edge://settings/profiles* and sign out of your Azure AD profile.</span></span> <span data-ttu-id="9cce7-132">Esta acción traerá la vista estándar para la página de nueva pestaña de empresas.</span><span class="sxs-lookup"><span data-stu-id="9cce7-132">This action will bring up the  standard view for the Enterprise new tab page.</span></span> 

## <span data-ttu-id="9cce7-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9cce7-133">See also</span></span>

- [<span data-ttu-id="9cce7-134">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="9cce7-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="9cce7-135">Modo de empresa para Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="9cce7-135">Enterprise Mode for Internet Explorer 11</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
