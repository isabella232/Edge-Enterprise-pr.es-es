---
title: Lista de permitidos para puntos de conexión de Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Lista de permitidos para puntos de conexión de Microsoft Edge
ms.openlocfilehash: 735e18e63095405dad4fdd51d51654956b564ca7
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641336"
---
# <a name="allow-list-for-microsoft-edge-endpoints"></a><span data-ttu-id="9c3ea-103">Lista de permitidos para puntos de conexión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9c3ea-103">Allow list for Microsoft Edge endpoints</span></span>

<span data-ttu-id="9c3ea-104">Microsoft Edge requiere conectividad a Internet para posibilitar sus funciones.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-104">Microsoft Edge requires connectivity to the Internet to support its features.</span></span> <span data-ttu-id="9c3ea-105">Este artículo identifica las direcciones URL de dominio que debes agregar a la Lista de permitidos para garantizar las comunicaciones a través de firewalls y otros mecanismos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-105">This article identifies the domain URLs that you need to add to the Allow list to ensure communications through firewalls and other security mechanisms.</span></span>

> [!NOTE]
> <span data-ttu-id="9c3ea-106">Esto se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-106">This applies  to Microsoft Edge version 77 or later.</span></span>

## <a name="domain-urls-to-allow"></a><span data-ttu-id="9c3ea-107">Direcciones URL a permitir</span><span class="sxs-lookup"><span data-stu-id="9c3ea-107">Domain URLs to allow</span></span>

<span data-ttu-id="9c3ea-108">Permite las siguientes direcciones URL de dominio para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-108">Allow the following domain URLs for Microsoft Edge.</span></span>

### <a name="update-service"></a><span data-ttu-id="9c3ea-109">Servicio de actualización</span><span class="sxs-lookup"><span data-stu-id="9c3ea-109">Update Service</span></span>

<span data-ttu-id="9c3ea-110">El servicio que Microsoft Edge usa para buscar nuevas actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-110">The service that Microsoft Edge uses to check for new updates.</span></span>

- `https://msedge.api.cdp.microsoft.com`

### <a name="experimentation-and-configuration-service"></a><span data-ttu-id="9c3ea-111">Servicio de experimentación y configuración</span><span class="sxs-lookup"><span data-stu-id="9c3ea-111">Experimentation and Configuration service</span></span>

- `https://config.edge.skype.com`

### <a name="download-locations-for-microsoft-edge"></a><span data-ttu-id="9c3ea-112">Ubicaciones de descarga para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9c3ea-112">Download locations for Microsoft Edge</span></span>

<span data-ttu-id="9c3ea-113">Las ubicaciones desde donde se puede descargar Microsoft Edge durante una instalación inicial o cuando haya una actualización disponible.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-113">Locations Microsoft Edge can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="9c3ea-114">La ubicación de descarga viene determinada por el servicio de actualización.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-114">The download location is determined by the Update Service.</span></span>

#### <a name="http"></a><span data-ttu-id="9c3ea-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="9c3ea-115">HTTP</span></span>

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a><span data-ttu-id="9c3ea-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="9c3ea-116">HTTPS</span></span>

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="9c3ea-117">Para simplificar la lista de permitidos para ubicaciones de descarga, se puede usar un comodín:</span><span class="sxs-lookup"><span data-stu-id="9c3ea-117">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <a name="download-locations-for-microsoft-edge-extensions"></a><span data-ttu-id="9c3ea-118">Ubicaciones de descarga para extensiones de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9c3ea-118">Download locations for Microsoft Edge Extensions</span></span>

<span data-ttu-id="9c3ea-119">Las ubicaciones desde donde se pueden descargar las extensiones de Microsoft Edge durante una instalación inicial o cuando haya una actualización disponible.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-119">Locations Microsoft Edge Extensions can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="9c3ea-120">La ubicación de descarga viene determinada por el servicio de actualización.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-120">The download location is determined by the Update Service.</span></span>

#### <a name="http"></a><span data-ttu-id="9c3ea-121">HTTP</span><span class="sxs-lookup"><span data-stu-id="9c3ea-121">HTTP</span></span>

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a><span data-ttu-id="9c3ea-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="9c3ea-122">HTTPS</span></span>

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="9c3ea-123">Para simplificar la lista de permitidos para ubicaciones de descarga, se puede usar un comodín:</span><span class="sxs-lookup"><span data-stu-id="9c3ea-123">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <a name="optionally-for-download-delivery-optimization"></a><span data-ttu-id="9c3ea-124">Opcionalmente para Optimización de distribución de descargas</span><span class="sxs-lookup"><span data-stu-id="9c3ea-124">Optionally for Download Delivery Optimization</span></span>

<span data-ttu-id="9c3ea-125">Para obtener más información sobre la optimización de distribución en general, consulta [Optimización de distribución para actualizaciones de Windows 10](/windows/deployment/update/waas-delivery-optimization).</span><span class="sxs-lookup"><span data-stu-id="9c3ea-125">For information about delivery optimization, see [Delivery Optimization for Windows 10 updates](/windows/deployment/update/waas-delivery-optimization).</span></span>

- <span data-ttu-id="9c3ea-126">Comunicación entre cliente y servicio: `*.do.dsp.mp.microsoft.com` (Puerto HTTP 80, puerto HTTPS 443)</span><span class="sxs-lookup"><span data-stu-id="9c3ea-126">Client to Service communication: `*.do.dsp.mp.microsoft.com` (HTTP Port 80, HTTPS Port 443)</span></span>
- <span data-ttu-id="9c3ea-127">Comunicación entre cliente y cliente: el puerto TCP 7680 debe estar abierto para el tráfico entrante</span><span class="sxs-lookup"><span data-stu-id="9c3ea-127">Client to Client communication: TCP port 7680 should be open for inbound traffic</span></span>

### <a name="sync"></a><span data-ttu-id="9c3ea-128">Sincronización</span><span class="sxs-lookup"><span data-stu-id="9c3ea-128">Sync</span></span>

<span data-ttu-id="9c3ea-129">Estos puntos de conexión administran la lectura y escritura de datos sincronizados, la administración de derechos para datos seguros y la notificación al explorador cuando hay nuevos datos de sincronización disponibles.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-129">These endpoints manage the reading and writing of synced data, rights management for secure data, and notifying the browser when new sync data is available.</span></span>

- <span data-ttu-id="9c3ea-130">Puntos de conexión del servicio de sincronización de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="9c3ea-130">Edge sync service endpoints:</span></span>

  - `https://edge-enterprise.activity.windows.com`
  - `https://edge.activity.windows.com`

- <span data-ttu-id="9c3ea-131">Puntos de conexión de Azure Information Protection:</span><span class="sxs-lookup"><span data-stu-id="9c3ea-131">Azure Information Protection endpoints:</span></span>

  - `https://api.aadrm.com` <span data-ttu-id="9c3ea-132">(para la mayoría de los espacios empresariales)</span><span class="sxs-lookup"><span data-stu-id="9c3ea-132">(for most tenants)</span></span>
  - `https://api.aadrm.de` <span data-ttu-id="9c3ea-133">(para los espacios empresariales de Alemania)</span><span class="sxs-lookup"><span data-stu-id="9c3ea-133">(for tenants in Germany)</span></span>
  - `https://api.aadrm.cn` <span data-ttu-id="9c3ea-134">(para los espacios empresariales de China)</span><span class="sxs-lookup"><span data-stu-id="9c3ea-134">(for tenants in China)</span></span>

- [<span data-ttu-id="9c3ea-135">Puntos de conexión del Servicio de notificaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="9c3ea-135">Windows Notification Service endpoints</span></span>](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## <a name="other-browser-support-services"></a><span data-ttu-id="9c3ea-136">Otros servicios de soporte del explorador</span><span class="sxs-lookup"><span data-stu-id="9c3ea-136">Other browser support services</span></span>

<span data-ttu-id="9c3ea-137">Proporciona metadatos para las funciones del explorador, como protección de rastreo, listas de revocación de certificados y otras actualizaciones de componentes del explorador.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-137">Provide metadata for browser features such as tracking protection, certificate revocation lists, and other browser component updates.</span></span> <span data-ttu-id="9c3ea-138">Proporciona diccionarios de ortografía descargables y listas de bloqueados para bloqueo de anuncios.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-138">Provide downloadable spellcheck dictionaries and ad-blocking block lists.</span></span> <span data-ttu-id="9c3ea-139">Proporciona servicios para posibilitar las funciones del explorador, como las colecciones, el autorrellenado y el almacén de extensión.</span><span class="sxs-lookup"><span data-stu-id="9c3ea-139">Provide services to support browser features such as collections, autofill, and extension store.</span></span>

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <a name="see-also"></a><span data-ttu-id="9c3ea-140">Consulta también</span><span class="sxs-lookup"><span data-stu-id="9c3ea-140">See also</span></span>

- [<span data-ttu-id="9c3ea-141">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="9c3ea-141">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="9c3ea-142">Página de aterrizaje de documentación de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9c3ea-142">Microsoft Edge documentation landing page</span></span>](./index.yml)
- [<span data-ttu-id="9c3ea-143">Administrar puntos de conexión de conexión para Windows 10 Enterprise, versión 1903</span><span class="sxs-lookup"><span data-stu-id="9c3ea-143">Manage connection endpoints for Windows 10 Enterprise, version 1903</span></span>](/windows/privacy/manage-windows-1903-endpoints)