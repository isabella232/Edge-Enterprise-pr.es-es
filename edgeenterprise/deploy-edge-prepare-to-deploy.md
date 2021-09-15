---
title: Microsoft Edge en tu entorno
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge en tu entorno
ms.openlocfilehash: 2381380cb399f6a1fbb5efa9378ffeba20fa774f
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979666"
---
# <a name="microsoft-edge-in-your-environment"></a>Microsoft Edge en tu entorno

En este artículo se describe cómo preparar la implementación de Microsoft Edge cuando Microsoft Edge (versión anterior) llegue al final del servicio.

Según la [entrada de blog](https://aka.ms/EdgeLegacyEOS) del equipo de productos de Microsoft Edge, la compatibilidad con la aplicación de escritorio Microsoft Edge (versión anterior) finalizará el 9 de marzo de 2021. Cuando apliques la versión de la actualización del martes (o "B") de abril, se eliminará Microsoft Edge (versión anterior) de los dispositivos que ejecuten desde Windows 10 RS4 a 20H1 y se sustituirá por Microsoft Edge.

## <a name="how-to-prepare"></a>Cómo prepararse

Para prepararse para la instalación de Microsoft Edge en los dispositivos de Windows 10 RS4 a 20H1 con la versión de la actualización del martes de abril, recomendamos leer [Planificar tu implementación de Microsoft Edge](deploy-edge-plan-deployment.md).

Después de planificar tu implementación, usa uno de los siguientes métodos para preparar la implementación de Microsoft Edge.

- **Instala directivas de grupo para personalizar tu enfoque de actualización de Microsoft Edge**. Para obtener más información, ve [Configurar las opciones de directiva de Microsoft Edge en Windows](configure-microsoft-edge.md) y presta especial atención al material de [Referencia de la directiva de actualización](microsoft-edge-update-policies.md). Si instalas directivas de grupo para administrar tus actualizaciones antes de instalar la versión de la actualización del martes de abril, Microsoft Edge empezará a respetar inmediatamente tu política. Si no hay ninguna directiva de grupo instalada, Microsoft Edge se actualizará automáticamente.

- **Quita la aplicación de escritorio de Microsoft Edge (versión anterior) antes de su fecha de finalización del servicio del 9 de marzo de 2021 e implementa Microsoft Edge**. Para Windows 10 RS4 a 20H1, puedes hacerlo mediante actualizaciones de Windows. Para obtener más información, ve [Implementar Microsoft Edge con actualizaciones de Windows 10](deploy-edge-with-windows-10-updates.md).

## <a name="see-also"></a>Ve también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Planear tu implementación de Microsoft Edge](deploy-edge-plan-deployment.md)