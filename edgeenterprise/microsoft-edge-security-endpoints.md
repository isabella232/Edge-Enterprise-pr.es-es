---
title: Lista de permitidos para puntos de conexión de Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 10/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Lista de permitidos para puntos de conexión de Microsoft Edge
ms.openlocfilehash: 48a3a72e5af3744516e3b72d02b5254ad2e0504a
ms.sourcegitcommit: b32d8d64ae65dc5a46e47b7c34b0211097a0cc65
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "11133125"
---
# Lista de permitidos para puntos de conexión de Microsoft Edge

Microsoft Edge requiere conectividad a Internet para posibilitar sus funciones. Este artículo identifica las direcciones URL de dominio que debes agregar a la Lista de permitidos para garantizar las comunicaciones a través de firewalls y otros mecanismos de seguridad.

> [!NOTE]
> Esto se aplica a Microsoft Edge, versión 77 o posterior.

## Direcciones URL a permitir

Permite las siguientes direcciones URL de dominio para Microsoft Edge.

### Servicio de actualización

El servicio que Microsoft Edge usa para buscar nuevas actualizaciones.

- `https://msedge.api.cdp.microsoft.com`

### Servicio de experimentación y configuración

- `https://config.edge.skype.com`

### Ubicaciones de descarga para Microsoft Edge

Las ubicaciones desde donde se puede descargar Microsoft Edge durante una instalación inicial o cuando haya una actualización disponible. La ubicación de descarga viene determinada por el servicio de actualización.

#### HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Para simplificar la lista de permitidos para ubicaciones de descarga, se puede usar un comodín: `*.dl.delivery.mp.microsoft.com`

### Ubicaciones de descarga para extensiones de Microsoft Edge

Las ubicaciones desde donde se pueden descargar las extensiones de Microsoft Edge durante una instalación inicial o cuando haya una actualización disponible. La ubicación de descarga viene determinada por el servicio de actualización.

#### HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Para simplificar la lista de permitidos para ubicaciones de descarga, se puede usar un comodín: `*.dl.delivery.mp.microsoft.com`

### Opcionalmente para Optimización de distribución de descargas

Para obtener más información sobre la optimización de distribución en general, consulta [Optimización de distribución para actualizaciones de Windows 10](https://aka.ms/waas-do).

- Comunicación entre cliente y servicio: `*.do.dsp.mp.microsoft.com` (Puerto HTTP 80, puerto HTTPS 443)
- Comunicación entre cliente y cliente: el puerto TCP 7680 debe estar abierto para el tráfico entrante

### Sincronización

Estos puntos de conexión administran la lectura y escritura de datos sincronizados, la administración de derechos para datos seguros y la notificación al explorador cuando hay nuevos datos de sincronización disponibles.

- Puntos de conexión del servicio de sincronización de Microsoft Edge:

  - `https://enterprise.edge.activity.windows.com`
  - `https://edge.activity.windows.com`

- Puntos de conexión de Azure Information Protection:

  - `https://api.aadrm.com` (para la mayoría de los espacios empresariales)
  - `https://api.aadrm.de` (para los espacios empresariales de Alemania)
  - `https://api.aadrm.cn` (para los espacios empresariales de China)

- [Puntos de conexión del Servicio de notificaciones de Windows](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## Otros servicios de soporte del explorador

Proporciona metadatos para las funciones del explorador, como protección de rastreo, listas de revocación de certificados y otras actualizaciones de componentes del explorador. Proporciona diccionarios de ortografía descargables y listas de bloqueados para bloqueo de anuncios. Proporciona servicios para posibilitar las funciones del explorador, como las colecciones, el autorrellenado y el almacén de extensión.

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Página de aterrizaje de documentación de Microsoft Edge](https://docs.microsoft.com/DeployEdge/)
- [Administrar puntos de conexión de conexión para Windows 10 Enterprise, versión 1903](https://docs.microsoft.com/windows/privacy/manage-windows-1903-endpoints)
