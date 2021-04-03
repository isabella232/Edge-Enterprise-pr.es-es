---
title: Estrategia de configuración del sitio de la empresa
ms.author: shisub
author: shisub
manager: srugh
ms.date: 03/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Una guía paso a paso para configurar la lista de sitios en modo empresa para el modo de Internet Explorer..
ms.openlocfilehash: 1d0b80950439fce77513413c3f5d1143538487d1
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470158"
---
# <a name="enterprise-site-configuration-strategy"></a><span data-ttu-id="872b2-103">Estrategia de configuración del sitio de la empresa</span><span class="sxs-lookup"><span data-stu-id="872b2-103">Enterprise site configuration strategy</span></span>

<span data-ttu-id="872b2-104">En este artículo se describen los cambios realizados en la lista de sitios en modo empresa para la compatibilidad del modo de Internet Explorer con Microsoft Edge versión 77 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="872b2-104">This article describes changes to the Enterprise Mode Site List to support Internet Explorer mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="872b2-105">Para obtener más información sobre el esquema para el archivo XML de lista de sitios en el modo de empresa, consulte la [Guía de esquema de modo de empresa v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="872b2-105">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="872b2-106">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="872b2-106">This article applies to Microsoft Edge version 77 or later.</span></span>
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a><span data-ttu-id="872b2-107">Estrategia de configuración</span><span class="sxs-lookup"><span data-stu-id="872b2-107">Configuration strategy</span></span>

<span data-ttu-id="872b2-108">Los siguientes pasos forman parte de una estrategia de configuración del sitio para el modo IE:</span><span class="sxs-lookup"><span data-stu-id="872b2-108">The following steps are part of a site configuration strategy for IE mode:</span></span>
1. <span data-ttu-id="872b2-109">Prepare su lista de sitios</span><span class="sxs-lookup"><span data-stu-id="872b2-109">Prepare your site list</span></span>
2. <span data-ttu-id="872b2-110">Configurar los sitios neutros</span><span class="sxs-lookup"><span data-stu-id="872b2-110">Configure neutral sites</span></span>
3. <span data-ttu-id="872b2-111">(Opcional) Utilizar el uso compartido de cookies si es necesario</span><span class="sxs-lookup"><span data-stu-id="872b2-111">(Optional) Use cookie sharing if necessary</span></span>

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a><span data-ttu-id="872b2-112">Prepare su lista de sitios</span><span class="sxs-lookup"><span data-stu-id="872b2-112">Prepare your site list</span></span>

<span data-ttu-id="872b2-113">Si ya tiene una lista de sitios en modo de empresa para IE11 o Microsoft Edge Legacy, puede reutilizarla para configurar el modo IE.</span><span class="sxs-lookup"><span data-stu-id="872b2-113">If you already have an Enterprise Mode site list for IE11 or Microsoft Edge Legacy, you can reuse it to configure IE mode.</span></span>

<span data-ttu-id="872b2-114">Sin embargo, si no tiene una lista de sitios, puede utilizar la [herramienta Enterprise Site Discovery](https://docs.microsoft.com/deployedge/edge-ie-mode-site-discovery)para rellenar su lista de sitios.</span><span class="sxs-lookup"><span data-stu-id="872b2-114">However, if you don't have a site list, you can use the [Enterprise Site Discovery tool](https://docs.microsoft.com/deployedge/edge-ie-mode-site-discovery) to populate your site list.</span></span>

## <a name="configure-neutral-sites"></a><span data-ttu-id="872b2-115">Configurar los sitios neutros</span><span class="sxs-lookup"><span data-stu-id="872b2-115">Configure neutral sites</span></span>

<span data-ttu-id="872b2-116">Para que el modo IE funcione correctamente, los servidores de autenticación / Inicio de sesión único (SSO) tendrán que ser configurados explícitamente como sitios neutrales.</span><span class="sxs-lookup"><span data-stu-id="872b2-116">In order for IE mode to work properly, authentication / Single Sign-On (SSO) servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="872b2-117">De lo contrario, las páginas del modo IE intentarán redirigir a Microsoft Edge, y la autenticación fallará.</span><span class="sxs-lookup"><span data-stu-id="872b2-117">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="872b2-118">Un sitio neutral usará el explorador en el que se inició el desplazamiento, ya sea en el modo de Microsoft Edge o el modo de IE.</span><span class="sxs-lookup"><span data-stu-id="872b2-118">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="872b2-119">La configuración de los sitios neutros garantiza que todas las aplicaciones que utilicen los mismos servidores de autenticación, tanto modernos como heredados, sigan funcionando.</span><span class="sxs-lookup"><span data-stu-id="872b2-119">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="872b2-120">Para configurar sitios neutros, configure la lista desplegable *Abrir en* como "ninguna" en la Herramienta de Administración de Lista de Sitios del Modo de Empresa, o bien actualice el XML de la lista de sitios directamente:</span><span class="sxs-lookup"><span data-stu-id="872b2-120">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="872b2-121">Para identificar los servidores de autenticación, inspeccione el tráfico de red de una aplicación utilizando las herramientas de desarrollo de IE11.</span><span class="sxs-lookup"><span data-stu-id="872b2-121">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="872b2-122">Si necesita más tiempo para identificar sus servidores de autenticación, puede configurar una directiva para mantener todas las navegaciones dentro de la página en modo IE para permitir que sus usuarios continúen sus flujos de trabajo sin interrupción.</span><span class="sxs-lookup"><span data-stu-id="872b2-122">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigations in IE mode to allow your users to continue their workflows uninterrupted.</span></span> <span data-ttu-id="872b2-123">Para minimizar el uso del modo IE cuando sea innecesario, desactive esta configuración una vez que haya identificado y agregado sus servidores de autenticación a la lista de sitios.</span><span class="sxs-lookup"><span data-stu-id="872b2-123">To minimize the use of IE mode when unnecessary, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="872b2-124">Para obtener más información, consulte [Mantener la navegación en la página en modo IE](https://docs.microsoft.com/deployedge/edge-learnmore-inpage-nav).</span><span class="sxs-lookup"><span data-stu-id="872b2-124">For more information, see [Keep in-page navigation in IE mode](https://docs.microsoft.com/deployedge/edge-learnmore-inpage-nav).</span></span>

>[!NOTE]
   ><span data-ttu-id="872b2-125">El esquema v. 1 del modo de empresa no se admite para la integración de modo IE.</span><span class="sxs-lookup"><span data-stu-id="872b2-125">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="872b2-126">Si estás usando actualmente el esquema v. 1 con Internet Explorer 11, debes actualizar al esquema v. 2.</span><span class="sxs-lookup"><span data-stu-id="872b2-126">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="872b2-127">Para obtener más información, consulte [Guía sobre el esquema del Modo de empresa v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="872b2-127">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="optional-use-cookie-sharing-if-necessary"></a><span data-ttu-id="872b2-128">(Opcional) Utilizar el uso compartido de cookies si es necesario</span><span class="sxs-lookup"><span data-stu-id="872b2-128">(Optional) Use cookie sharing if necessary</span></span>

<span data-ttu-id="872b2-129">De forma predeterminada, los procesos de Microsoft Edge e Internet Explorer no comparten las cookies de sesión, y esta falta de compartición puede ser un inconveniente en algunos casos mientras se utiliza el modo IE.</span><span class="sxs-lookup"><span data-stu-id="872b2-129">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this lack of sharing can be inconvenient in some cases while using IE mode.</span></span> <span data-ttu-id="872b2-130">Por ejemplo, cuando un usuario tiene que volver a autenticarse en modo IE cuando previamente está acostumbrado a hacerlo o cuando al cerrar la sesión de Microsoft Edge no se cierra la sesión en modo Internet Explorer para las transacciones críticas.</span><span class="sxs-lookup"><span data-stu-id="872b2-130">For example, when a user has to reauthenticate in IE mode when previously they are accustomed to doing so or when signing out of a Microsoft Edge session doesn’t sign out of the Internet Explorer mode session for critical transactions.</span></span> <span data-ttu-id="872b2-131">En estos escenarios, puede configurar cookies específicas establecidas por SSO para que se envíen desde Microsoft Edge a Internet Explorer, de modo que la experiencia de autenticación sea más fluida al eliminar la necesidad de volver a autenticar.</span><span class="sxs-lookup"><span data-stu-id="872b2-131">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to reauthenticate.</span></span> <span data-ttu-id="872b2-132">Para obtener más información, consulte [Compartir cookies de Microsoft Edge a Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode-add-guidance-cookieshare).</span><span class="sxs-lookup"><span data-stu-id="872b2-132">For more information, see [Cookie sharing from Microsoft Edge to Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode-add-guidance-cookieshare).</span></span>

## <a name="see-also"></a><span data-ttu-id="872b2-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="872b2-133">See also</span></span>

- [<span data-ttu-id="872b2-134">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="872b2-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="872b2-135">Acerca del modo IE</span><span class="sxs-lookup"><span data-stu-id="872b2-135">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="872b2-136">Información adicional del modo de empresa</span><span class="sxs-lookup"><span data-stu-id="872b2-136">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
