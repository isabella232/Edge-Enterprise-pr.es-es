---
title: Configuraciones y experimentación de Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configuraciones y experimentación de Microsoft Edge
ms.openlocfilehash: d6aee10133b5cbc0f7a784fab561864303d3dc6eb4e1cb6547562b9e6107961a
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726173"
---
# <a name="microsoft-edge-configurations-and-experimentation"></a>Configuraciones y experimentación de Microsoft Edge

En este artículo se describe la interacción entre Microsoft Edge y el servicio de experimentación y configuración (ECS). Microsoft Edge se comunica con este servicio para solicitar y recibir distintos tipos de cargas. Estas cargas incluyen configuraciones, implementaciones de funciones y experimentos.

> [!IMPORTANT]
> Asegúrese de que los clientes puedan obtener acceso a `https://config.edge.skype.com` para poder recibir cargas.

> [!NOTE]
> Esto se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="configurations"></a>Configuraciones

Las configuraciones son la carga pensada para garantizar el cumplimiento del estado, la seguridad y la privacidad del producto, y tienen el mismo valor para todos los usuarios (en función de las plataformas y los canales). Esto podría ser habilitar una marca de función para una acción de dominio, y también puede usarse para deshabilitar una marca de función en el caso de un error.

## <a name="controlled-feature-rollout"></a>Lanzamiento de funciones controladas

La implementación de funciones controlada (CFR) es un procedimiento para aumentar lentamente el tamaño del grupo de usuarios que recibe una función. Al distribuir una nueva función a un subconjunto seleccionado aleatoriamente de la población de usuarios, es posible comparar los comentarios de los usuarios con un grupo de controles de igual tamaño sin la característica para medir el impacto de la función.

## <a name="experiments"></a>Experimentos

Las compilaciones de Microsoft Edge tienen características y funciones que aún están en desarrollo o que son experimentales. Los experimentos son como CFR, pero el tamaño del grupo de usuarios es mucho más pequeño para probar el nuevo concepto. Estas funciones se ocultan de manera predeterminada hasta que se lanza la función o finaliza el experimento. Las marcas de experimento se usan para habilitar y deshabilitar estas funciones.

## <a name="about-the-ecs"></a>Acerca del ECS

En todos los escenarios anteriores, el servicio proporciona los valores de marca de funciones al cliente del explorador, para que puedan aplicarse. En función de la actualización, las configuraciones se aplican inmediatamente o cuando el usuario reinicia el explorador.

La interacción de Microsoft Edge con este servicio se controla mediante la configuración de la directiva [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol). Puedes configurar las opciones de directiva para:

- Solo recuperar configuraciones
- Recuperar configuraciones y experimentos
- Deshabilitar la comunicación con el servicio

  > [!CAUTION]
  > Si deshabilitas las comunicaciones con el servicio, esto afectará a la capacidad de Microsoft para responder a un error grave de manera puntual.

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoftedgeinsider.com/enterprise)
- [Página de aterrizaje de documentación de Microsoft Edge](./index.yml)