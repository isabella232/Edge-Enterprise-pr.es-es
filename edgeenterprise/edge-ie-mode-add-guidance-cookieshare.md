---
title: Compartir cookies de Microsoft Edge a Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Como compartir cookies de Microsoft Edge a Internet Explorer '
ms.openlocfilehash: 5740a4ce31a240573b9106e7a20a5c44688aca0a
ms.sourcegitcommit: 2024629929044e2dcf146674058c1d6312c32e9a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2020
ms.locfileid: "11157551"
---
# <span data-ttu-id="f36d4-103">Compartir cookies de Microsoft Edge a Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f36d4-103">Cookie sharing from Microsoft Edge to Internet Explorer</span></span>

<span data-ttu-id="f36d4-104">Este artículo explica cómo configurar el uso compartido de cookies de sesión de un proceso de Microsoft Edge al proceso de Internet Explorer, mientras se usa el modo de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f36d4-104">This article explains explains how to configure session cookie sharing from a Microsoft Edge process to Internet Explorer process, while using Internet Explorer mode.</span></span>

> [!NOTE]
> <span data-ttu-id="f36d4-105">Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f36d4-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="f36d4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f36d4-106">Prerequisites</span></span>

- <span data-ttu-id="f36d4-107">Actualizaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="f36d4-107">Windows updates</span></span>

  - <span data-ttu-id="f36d4-108">Windows 10, versión 2004; Windows Server, versión 2004 (KB4571744 o superior)</span><span class="sxs-lookup"><span data-stu-id="f36d4-108">Windows 10 version 2004, Windows server version 2004 - KB4571744 or higher</span></span>
  - <span data-ttu-id="f36d4-109">Windows 10, versión 1909; Windows Server, versión 1909 (KB4566116 o superior)</span><span class="sxs-lookup"><span data-stu-id="f36d4-109">Windows 10 version 1909, Windows server version 1909 – KB4566116 or higher</span></span>
  - <span data-ttu-id="f36d4-110">Windows 10, versión 1903; Windows Server, versión 1903 (KB4566116 o superior)</span><span class="sxs-lookup"><span data-stu-id="f36d4-110">Windows 10 version 1903, Windows server version 1903 – KB4566116 or higher</span></span>
  - <span data-ttu-id="f36d4-111">Windows 10, versión 1809; Windows Server, versión 1809, y Windows Server 2019 (KB4571748 o superior)</span><span class="sxs-lookup"><span data-stu-id="f36d4-111">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4571748 or higher</span></span>
  - <span data-ttu-id="f36d4-112">Windows 10, versión 1803 (KB4577032 o superior)</span><span class="sxs-lookup"><span data-stu-id="f36d4-112">Windows 10 version 1803 – KB4577032 or higher</span></span>

- <span data-ttu-id="f36d4-113">Microsoft Edge, versión 87 o posterior</span><span class="sxs-lookup"><span data-stu-id="f36d4-113">Microsoft Edge version 87 or later</span></span>
- <span data-ttu-id="f36d4-114">[Modo IE](https://aka.ms/iemodeonedge) configurado con la lista de sitios del Modo de empresa</span><span class="sxs-lookup"><span data-stu-id="f36d4-114">[IE mode](https://aka.ms/iemodeonedge) configured with Enterprise Mode Site List</span></span>

## <span data-ttu-id="f36d4-115">Introducción</span><span class="sxs-lookup"><span data-stu-id="f36d4-115">Overview</span></span>

<span data-ttu-id="f36d4-116">Una configuración común en las organizaciones de gran tamaño consiste en tener una aplicación que funcione en un vínculo de explorador moderno a otra aplicación, que se puede configurar para abrir en modo de Internet Explorer con el inicio de sesión único (SSO) habilitado como parte del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f36d4-116">A common configuration in large organizations is to have an application that works on a modern browser link to another application, which might be configured to open in Internet Explorer mode with Single Sign On (SSO) enabled as part of the workflow.</span></span>

<span data-ttu-id="f36d4-117">De forma predeterminada, los procesos de Microsoft Edge e Internet Explorer no comparten las cookies de sesión, por lo que puede ser poco práctico en ciertos casos.</span><span class="sxs-lookup"><span data-stu-id="f36d4-117">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this can be inconvenient in some cases.</span></span> <span data-ttu-id="f36d4-118">Por ejemplo, cuando un usuario tiene que volver a autenticarse en el modo de Internet Explorer o al cerrar sesión en una sesión de Microsoft Edge no se firma en la sesión de modo de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f36d4-118">For example, when a user has to re-authenticate in Internet Explorer mode or when signing out of an Microsoft Edge session doesn’t sign out of the Internet Explorer mode session.</span></span> <span data-ttu-id="f36d4-119">En estos casos, puede configurar las cookies específicas establecidas por SSO para enviarlas de Microsoft Edge a Internet Explorer, de modo que la experiencia de autenticación sea más fluida eliminando la necesidad de realizar una nueva autenticación.</span><span class="sxs-lookup"><span data-stu-id="f36d4-119">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to re-authenticate.</span></span>

> [!NOTE]
> <span data-ttu-id="f36d4-120">Las cookies solo pueden ser compartidas de Microsoft Edge a Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f36d4-120">Session cookies can only be shared from Microsoft Edge to Internet Explorer.</span></span> <span data-ttu-id="f36d4-121">No es posible compartir cookies de sesión de en inverso (de Internet Explorer a Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="f36d4-121">Sharing session cookies in reverse (from Internet Explorer to Microsoft Edge) isn't possible.</span></span>

## <span data-ttu-id="f36d4-122">Cómo funciona el uso compartido de cookies</span><span class="sxs-lookup"><span data-stu-id="f36d4-122">How cookie sharing works</span></span>

<span data-ttu-id="f36d4-123">Se ha ampliado el XML de la lista de sitios de modo empresarial para permitir que otros elementos especifiquen cookies que se requieren compartir desde una sesión de Microsoft Edge con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f36d4-123">The Enterprise Mode site list XML has been extended to allow additional elements to specify cookies that need to be shared from a Microsoft Edge session with Internet Explorer.</span></span>  

<span data-ttu-id="f36d4-124">La primera vez que se crea una pestaña en modo de Internet Explorer en una sesión de Microsoft Edge, todas las cookies correspondientes se comparten en la sesión de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f36d4-124">The first time an Internet Explorer mode tab is created in a Microsoft Edge session, all matching cookies are shared to the Internet Explorer session.</span></span> <span data-ttu-id="f36d4-125">Por lo tanto, cada vez que se agregue, elimine o modifique un cookie que coincida con una regla, se enviará como una actualización de la sesión de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f36d4-125">Subsequently, any time a cookie that matches a rule is added, deleted, or modified it is sent as an update to the Internet Explorer session.</span></span> <span data-ttu-id="f36d4-126">Cuando se actualiza la lista de sitios, el conjunto de cookies compartidas también vuelve a evaluarse.</span><span class="sxs-lookup"><span data-stu-id="f36d4-126">The set of shared cookies is also re-evaluated when the site list is updated.</span></span>

### <span data-ttu-id="f36d4-127">Elementos de esquema actualizados</span><span class="sxs-lookup"><span data-stu-id="f36d4-127">Updated schema elements</span></span>

<span data-ttu-id="f36d4-128">En la siguiente tabla se describe el elemento de \<shared-cookie\> agregado para admitir la característica de uso compartido de cookies.</span><span class="sxs-lookup"><span data-stu-id="f36d4-128">The following table describes the \<shared-cookie\> element added to support the cookie sharing feature.</span></span>

| <span data-ttu-id="f36d4-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="f36d4-129">Element</span></span>| <span data-ttu-id="f36d4-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f36d4-130">Description</span></span> |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br><span data-ttu-id="f36d4-131">O bien,</span><span class="sxs-lookup"><span data-stu-id="f36d4-131">OR</span></span><br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |<span data-ttu-id="f36d4-132">**(obligatorio)** un elemento de \<shared-cookie\> requiere, como mínimo, un *de dominio* (para las cookies del dominio) o un atributo *host* (solo para cookies de host) y un atributo *nombre* .</span><span class="sxs-lookup"><span data-stu-id="f36d4-132">**(Required)** A \<shared-cookie\> element requires, at minimum, a *domain* (for domain cookies) or a *host* (for host-only cookies) attribute and a *name* attribute.</span></span><br><span data-ttu-id="f36d4-133">Deben ser coincidencias exactas con el dominio y el nombre de la cookie respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f36d4-133">These must be exact matches to the cookie's domain and name respectively.</span></span> <span data-ttu-id="f36d4-134">**Nota** los subdominios no coinciden.</span><span class="sxs-lookup"><span data-stu-id="f36d4-134">**Note** that subdomains do not match.</span></span><br><br><span data-ttu-id="f36d4-135">El atributo *dominio* se usa para las cookies de dominio (y se permite un punto inicial, pero es opcional).</span><span class="sxs-lookup"><span data-stu-id="f36d4-135">The *domain* attribute is used for domain cookies (and a leading dot is allowed but optional).</span></span><br><span data-ttu-id="f36d4-136">El atributo *host* se usa para las cookies solo de host (y un punto inicial es un error).</span><span class="sxs-lookup"><span data-stu-id="f36d4-136">The *host* attribute is used for host-only cookies (and a leading dot is an error).</span></span> <span data-ttu-id="f36d4-137">Especifica ninguno o ambos producirá un error.</span><span class="sxs-lookup"><span data-stu-id="f36d4-137">Specifying neither or both will result in an error.</span></span><br><span data-ttu-id="f36d4-138">\* Un cookie es una cookie de dominio si se especificó un dominio en la cadena de la cookie (a través de un encabezado o documento de respuesta cookie Set HTTP. cookie JS API).</span><span class="sxs-lookup"><span data-stu-id="f36d4-138">\* A cookie is a domain cookie if a domain was specified in the cookie string (via HTTP Set-Cookie response header or document.cookie JS API).</span></span> <span data-ttu-id="f36d4-139">Las cookies de dominio se aplican a los dominios y subdominios especificados.</span><span class="sxs-lookup"><span data-stu-id="f36d4-139">A domain cookie applies to the specified domain and all subdomains.</span></span> <span data-ttu-id="f36d4-140">Si un dominio no es establecido en la cadena cookie, el cookie es un cookie solo para host y solo se aplica al host específico en el que se haya establecido.</span><span class="sxs-lookup"><span data-stu-id="f36d4-140">If a domain was not specified in the cookie string, the cookie is a host-only cookie and only applies to the specific host that it was set for.</span></span> <span data-ttu-id="f36d4-141">Tenga en cuenta que algunas clases de direcciones URL, como nombres de host de una sola palabra (como, por ejemplo, http://intranetsite) y direcciones IP (por ejemplo, http://10.0.0.1) solo pueden establecer cookies solo de anfitrión.</span><span class="sxs-lookup"><span data-stu-id="f36d4-141">Note that some classes of URLs such as single-word hostnames (e.g. http://intranetsite) and IP addresses (e.g. http://10.0.0.1) can only set host-only cookies.</span></span>    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | <span data-ttu-id="f36d4-142">**(opcional)** un atributo *path* puede ser especificado</span><span class="sxs-lookup"><span data-stu-id="f36d4-142">**(Optional)** A *path* attribute may be specified.</span></span> <span data-ttu-id="f36d4-143">Si no se especifica ningún atributo Path (o si el atributo path está vacío), las cookies que coinciden con Domain/host y Name coinciden con la Directiva, independientemente de la ruta de acceso (regla comodín).</span><span class="sxs-lookup"><span data-stu-id="f36d4-143">If no path attribute is specified (or if the path attribute is empty), any cookies matching domain/host and name match the policy, regardless of path (wildcard rule).</span></span><br><br><span data-ttu-id="f36d4-144">Si se especifica una ruta de acceso, debe ser una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="f36d4-144">If a path is specified, it must be an exact match.</span></span><br><span data-ttu-id="f36d4-145">Si un cookie coincide con una regla con una ruta de acceso, tiene prioridad sobre una regla sin una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="f36d4-145">If a cookie matches a rule with a path, that takes precedence over a rule without a path.</span></span> |

#### <span data-ttu-id="f36d4-146">Ejemplo de uso compartido</span><span class="sxs-lookup"><span data-stu-id="f36d4-146">Sharing example</span></span>

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <span data-ttu-id="f36d4-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f36d4-147">See also</span></span>

- [<span data-ttu-id="f36d4-148">Acerca del modo IE</span><span class="sxs-lookup"><span data-stu-id="f36d4-148">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="f36d4-149">Información de sitios configurables</span><span class="sxs-lookup"><span data-stu-id="f36d4-149">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="f36d4-150">Información adicional del modo de empresa</span><span class="sxs-lookup"><span data-stu-id="f36d4-150">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="f36d4-151">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f36d4-151">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
