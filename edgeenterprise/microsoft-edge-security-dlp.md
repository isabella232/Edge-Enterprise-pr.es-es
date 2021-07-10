---
title: Prevención de pérdida de datos en Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Prevención de pérdida de datos (DLP) en Microsoft Edge
ms.openlocfilehash: acbc9dab14c193f4f7cb06eb61e676083bfdf6ef
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642656"
---
# <a name="data-loss-prevention-dlp-in-microsoft-edge"></a>Prevención de pérdida de datos (DLP) en Microsoft Edge

La prevención de pérdida de datos (DLP) es un sistema de tecnologías que identifican y protegen los datos confidenciales de la empresa de la divulgación no autorizada. Con el fin de cumplir las normas de la industria y los estándares empresariales, las organizaciones deben proteger la información confidencial y evitar la divulgación no autorizada. La información confidencial incluye datos financieros o información de identificación personal (PII), como números de tarjeta de crédito, números de la seguridad social o registros de salud, entre muchas otras cosas.

El trabajo remoto ha aumentado el énfasis en el uso de DLP. Con el creciente uso de las actividades personales y laborales en los dispositivos, las empresas están experimentando un mayor riesgo de que se compartan de forma no autorizada datos corporativos externos al lugar de trabajo.

Esta mezcla de las actividades de los usuarios también se distribuye en los dispositivos, en la que los datos se mueven entre dispositivos corporativos y de la empresa a través de una variedad de redes privadas y públicas. El resultado neto es un riesgo mucho mayor de revelar datos confidenciales.

Microsoft Edge es compatible de forma nativa con dos soluciones DLP distintas, DLP de Microsoft Endpoint y la protección de información de Windows (WIP).

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a>Prevención de pérdida de datos de Microsoft Endpoint (DLP de Endpoint)

DLP de Microsoft Endpoint es la siguiente generación de prevención de pérdida de datos con conceptos modernos como la protección centrada en los datos. Está integrado en Windows 10 y Microsoft Edge, de modo que no necesitará agentes ni complementos adicionales en el dispositivo.

> [!NOTE]
> Esto se aplica a la versión 85 y a las posteriores de Microsoft Edge.

Para más información sobre DLP de punto de conexión, use los siguientes recursos:

- [Vídeo: Prevención de pérdida de datos (DLP) de Microsoft Edge](microsoft-edge-video-security-dlp.md)
- [Más información sobre la prevención de pérdida de datos de Endpoint de Microsoft 365](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide)
- [Introducción a la prevención de pérdida de datos de Endpoint](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide)

Microsoft Edge aplica directivas configuradas por el administrador para los archivos confidenciales y registra eventos de auditoría para las actividades que no cumplan con la normativa.

Entre las actividades de usuario que se pueden auditar y administrar en los dispositivos que ejecutan Windows 10 se incluyen las siguientes:

- Carga de archivos: proteger la carga de archivos confidenciales en ubicaciones en la nube no autorizadas. <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- Protección del portapapeles: proteger la copia de datos confidenciales desde el archivo.
- Protección de impresión: proteger el archivo confidencial para que no se imprima.
- Guardar en USB/red: proteger el archivo confidencial para que no se guarde en un almacenamiento USB extraíble o en ubicaciones de red no autorizadas.

Para obtener información más detallada sobre las actividades de usuario que se pueden auditar y administrar, consulte [actividades de Endpoint que se pueden supervisar y tomar medidas en](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).

## <a name="windows-information-protection"></a>Windows Information Protection

Consulte [Soporte técnico para protección de la información de Windows](./microsoft-edge-security-windows-information-protection.md), donde se describe cómo Microsoft Edge es compatible con la protección de información de Windows (WIP). Puede obtener más información sobre los requisitos del sistema, las prestaciones y las características compatibles en las secciones siguientes:

- [Requisitos del sistema](./microsoft-edge-security-windows-information-protection.md#system-requirements)
- [Beneficios de la Protección de la Información de Windows](./microsoft-edge-security-windows-information-protection.md#windows-information-protection-benefits)
- [Las características WIP compatibles en Microsoft Edge](./microsoft-edge-security-windows-information-protection.md#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: prevención de pérdida de datos-Microsoft Edge](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [Información general sobre la prevención de pérdida de datos](/microsoft-365/compliance/data-loss-prevention-policies?preserve-view=true&view=o365-worldwide)
- [Proteger los datos de tu empresa con Windows Information Protection (WIP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)