---
title: Configurar sitios en la lista de sitios de modo de empresa
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar la lista de sitios de empresas
ms.openlocfilehash: 9b1943e4d50dcc770b4a634b99ecbd001d1ffbcc
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447654"
---
# <a name="configure-sites-on-the-enterprise-mode-site-list"></a><span data-ttu-id="a5ef4-103">Configurar sitios en la lista de sitios de modo de empresa</span><span class="sxs-lookup"><span data-stu-id="a5ef4-103">Configure Sites on the Enterprise Mode Site List</span></span>

<span data-ttu-id="a5ef4-104">En este artículo se describen los cambios en la lista de sitios de modo de empresa que admiten la configuración de Internet Explorer para Microsoft Edge, versión 77 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-104">This article describes changes to the Enterprise Mode Site List that support configuring IE mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="a5ef4-105">Para obtener más información sobre el esquema para el archivo XML de lista de sitios en el modo de empresa, consulte la [Guía de esquema de modo de empresa v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="a5ef4-105">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="a5ef4-106">Este artículo se aplica a los canales de Microsoft Edge **Estable**, **Beta** y **Dev**, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-106">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

## <a name="updated-schema-elements"></a><span data-ttu-id="a5ef4-107">Elementos de esquema actualizados</span><span class="sxs-lookup"><span data-stu-id="a5ef4-107">Updated schema elements</span></span>

<span data-ttu-id="a5ef4-108">En la siguiente tabla se describe el elemento \<open-in app\> añadido a la v.2 del esquema del Modo de empresa:</span><span class="sxs-lookup"><span data-stu-id="a5ef4-108">The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:</span></span>

| **<span data-ttu-id="a5ef4-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a5ef4-109">Element</span></span>** | **<span data-ttu-id="a5ef4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5ef4-110">Description</span></span>** |
| --- | --- |
| \<open-in app="**true**"\> | <span data-ttu-id="a5ef4-111">Un elemento secundario que controla qué explorador se usa para sitios.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-111">A child element that controls what browser is used for sites.</span></span> <span data-ttu-id="a5ef4-112">Este elemento es necesario para los sitios que necesitan **abrirse en IE11**.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-112">This element is required for sites that need to **open in IE11**.</span></span>|

**<span data-ttu-id="a5ef4-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a5ef4-113">Example:</span></span>**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

<span data-ttu-id="a5ef4-114">La siguiente tabla muestra los posibles valores del elemento \<open-in\>:</span><span class="sxs-lookup"><span data-stu-id="a5ef4-114">The following table shows the possible values of the \<open-in\> element:</span></span>

| **<span data-ttu-id="a5ef4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ef4-115">Value</span></span>** | **<span data-ttu-id="a5ef4-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5ef4-116">Description</span></span>** |
| --- | --- |
| **\<open-in\><span data-ttu-id="a5ef4-117">IE11</span><span class="sxs-lookup"><span data-stu-id="a5ef4-117">IE11</span></span>\</open-in\>** | <span data-ttu-id="a5ef4-118">Abra el sitio en modo IE o en una ventana de IE11 completa.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-118">Opens the site in IE mode or a full IE11 window.</span></span> <span data-ttu-id="a5ef4-119">Para habilitar el modo IE, consulte [configurar las directivas de modo IE](./edge-ie-mode-policies.md)</span><span class="sxs-lookup"><span data-stu-id="a5ef4-119">To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)</span></span>|
| **\<open-in app="**true**"\><span data-ttu-id="a5ef4-120">IE11</span><span class="sxs-lookup"><span data-stu-id="a5ef4-120">IE11</span></span>\</open-in\>** | <span data-ttu-id="a5ef4-121">Abre el sitio en una ventana de IE11 completa.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-121">Opens the site in a full IE11 window</span></span> |
| **\<open-in\><span data-ttu-id="a5ef4-122">MSEdge</span><span class="sxs-lookup"><span data-stu-id="a5ef4-122">MSEdge</span></span>\</open-in\>** | <span data-ttu-id="a5ef4-123">Abre el sitio en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-123">Opens the site in Microsoft Edge</span></span> |
| **\<open-in\><span data-ttu-id="a5ef4-124">Ninguno o no especificado</span><span class="sxs-lookup"><span data-stu-id="a5ef4-124">None or not specified</span></span>\</open-in\>** | <span data-ttu-id="a5ef4-125">Abre el sitio en el explorador predeterminado o en el explorador donde el usuario se desplaza al sitio.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-125">Opens the site in the default browser or in the browser where the user navigated to the site.</span></span> |
|**\<open-in\><span data-ttu-id="a5ef4-126">Configurable</span><span class="sxs-lookup"><span data-stu-id="a5ef4-126">Configurable</span></span>\</open-in\>** | <span data-ttu-id="a5ef4-127">Permite al sitio participar en la determinación del motor en modo IE.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-127">Allows the site to participate in IE mode engine determination.</span></span> <span data-ttu-id="a5ef4-128">Para más información, consulte [Información sobre los sitios configurables en modo IE](edge-learnmore-configurable-sites-ie-mode.md).</span><span class="sxs-lookup"><span data-stu-id="a5ef4-128">To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).</span></span>  |

>[!NOTE]
> <span data-ttu-id="a5ef4-129">El atributo app=**"true"** solo se reconoce cuando está asociado a _'open-in' IE11_.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-129">The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_.</span></span> <span data-ttu-id="a5ef4-130">Agregarlo a los otros elementos 'open-in' no cambiará el comportamiento del explorador.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-130">Adding it to the other 'open-in' elements won't change browser behavior.</span></span>   

## <a name="configure-neutral-sites"></a><span data-ttu-id="a5ef4-131">Configurar los sitios neutros</span><span class="sxs-lookup"><span data-stu-id="a5ef4-131">Configure neutral sites</span></span>

<span data-ttu-id="a5ef4-132">Para que el modo de IE funcione correctamente, la autenticación y los servidores de inicio de sesión único tendrán que configurarse explícitamente como sitios neutrales.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-132">In order for IE mode to work properly, authentication / Single Sign-On servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="a5ef4-133">Si no, las páginas en modo IE intentarán redirigir a Microsoft Edge y se producirá un error de autenticación.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-133">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="a5ef4-134">Un sitio neutral usará el explorador en el que se inició el desplazamiento, ya sea en el modo de Microsoft Edge o el modo de IE.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-134">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="a5ef4-135">La configuración de los sitios neutros garantiza que todas las aplicaciones que utilicen los mismos servidores de autenticación, tanto modernos como heredados, sigan funcionando.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-135">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="a5ef4-136">Para configurar sitios neutros, configure la lista desplegable *Abrir en* como "ninguna" en la Herramienta de Administración de Lista de Sitios del Modo de Empresa, o bien actualice el XML de la lista de sitios directamente:</span><span class="sxs-lookup"><span data-stu-id="a5ef4-136">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="a5ef4-137">Para identificar servidores de autenticación, inspeccione el tráfico de red de una aplicación con las herramientas para desarrolladores de IE11.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-137">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="a5ef4-138">Si necesita más tiempo para identificar los servidores de autenticación, puede configurar una directiva para mantener toda la navegación en la página en modo IE.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-138">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigation in IE mode.</span></span> <span data-ttu-id="a5ef4-139">Para minimizar el uso del modo IE, deshabilite esta configuración una vez que haya identificado y agregado los servidores de autenticación en la lista de sitios.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-139">To minimize the use of IE mode, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="a5ef4-140">Para obtener más información, consulte [configurar la navegación en la página para permanecer en el modo IE](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).</span><span class="sxs-lookup"><span data-stu-id="a5ef4-140">For more information, see [Configure in-page navigation to remain in IE mode](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).</span></span>

>[!NOTE]
   ><span data-ttu-id="a5ef4-141">El esquema v. 1 del modo de empresa no se admite para la integración de modo IE.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-141">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="a5ef4-142">Si estás usando actualmente el esquema v. 1 con Internet Explorer 11, debes actualizar al esquema v. 2.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-142">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="a5ef4-143">Para obtener más información, consulta [Guía del esquema v.2 del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="a5ef4-143">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="see-also"></a><span data-ttu-id="a5ef4-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a5ef4-144">See also</span></span>

- [<span data-ttu-id="a5ef4-145">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a5ef4-145">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a5ef4-146">Acerca del modo IE</span><span class="sxs-lookup"><span data-stu-id="a5ef4-146">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="a5ef4-147">Información adicional del modo de empresa</span><span class="sxs-lookup"><span data-stu-id="a5ef4-147">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)