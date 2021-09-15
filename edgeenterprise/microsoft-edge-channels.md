---
title: Introducción a los canales de Microsoft Edge
ms.author: srugh
author: srugh
manager: seanlynd
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Introducción a los canales de Microsoft Edge
ms.openlocfilehash: 7d1fb72b458569cb4e4c6f44a6d89be7f65984df
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11980322"
---
# <a name="overview-of-the-microsoft-edge-channels"></a>Información general sobre los canales de Microsoft Edge

Una de las ventajas de la próxima versión de Microsoft Edge es que Microsoft puede proporcionar nuevas características de forma periódica. Sin embargo, como administrador que implementa Microsoft Edge para los usuarios de su organización, es posible que quieras tener un mayor control sobre la frecuencia con la que los usuarios obtienen estas nuevas características. Microsoft proporciona cuatro opciones, denominadas canales, para controlar la frecuencia con la que Microsoft Edge se actualiza con las nuevas características. Esta es una introducción a las cuatro opciones.

Para obtener más información sobre la compatibilidad con cada canal, lea: [Ciclo de vida de Microsoft Edge](/deployedge/microsoft-edge-support-lifecycle)
  
> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="channel-overview"></a>Introducción a los canales

|Canal|Finalidad principal|Frecuencia con la que se actualiza con nuevas características|¿Compatible?|
|:---:|---|:---:|:---:|
|[Estable](#stable-channel)|Amplia implementación|~6 semanas|Sí|
|[Beta](#beta-channel)|Validación representativa en la organización|~6 semanas|Sí|
|[Dev](#dev-channel)|Planificación y desarrollo|Semanal|No|
|[Canary](#canary-channel)|Contenido de vanguardia|Diariamente|No|

El canal de actualización que decidas implementar para tus usuarios depende de varios factores, como el número de aplicaciones de línea de negocio que el usuario aprovecha y que necesitas probar cada vez que tengan una versión actualizada de Microsoft Edge. Para ayudarte a tomar esta decisión, revisa la siguiente información sobre los cuatro canales de actualización disponibles para Microsoft Edge.

### <a name="stable-channel"></a>Canal estable

El canal estable está pensado para una implementación amplia en la organización y es el canal en el que deberían estar la mayoría de los usuarios. Es el canal más estable y es el resultado de la estabilización del conjunto de características disponibles en la versión del canal beta anterior. Se distribuyen nuevas características cada 6 semanas. Se distribuyen actualizaciones de seguridad y calidad según sea necesario. Se otorga servicio a una versión del canal estable hasta que la siguiente versión del canal esté disponible.

### <a name="beta-channel"></a>Canal beta

El canal beta está pensado para la implementación de producción en la organización para un conjunto de muestra representativo de usuarios. Es una versión compatible y se otorga servicio a todas las versiones de la versión beta hasta que la siguiente versión de este canal esté disponible. Esta es una excelente oportunidad para validar que las cosas funcionan según lo previsto en tu entorno y, si se produce un problema, solucionarlo antes de que la versión se publique en el canal estable. Se distribuyen nuevas características cada 6 semanas. Se distribuyen actualizaciones de seguridad y calidad según sea necesario.

### <a name="dev-channel"></a>Canal Dev

El canal Dev está pensado para ayudarte a planear y desarrollar con las últimas funciones de Microsoft Edge, pero con una mayor calidad que el canal Canary. Esta es tu oportunidad de echarle un vistazo a lo que viene en camino y de prepararte para la próxima versión Beta.

### <a name="canary-channel"></a>Canal Canary

El canal Canary se distribuye a diario y es el que está más en la vanguardia de todos los canales. Si quieres obtener acceso a las inversiones más recientes, primero aparecerán aquí. Debido a la naturaleza de esta cadencia, surgirán problemas con el tiempo, por lo que es posible que quieras que se instale otro canal en paralelo si estás aprovechando las versiones Canary.

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Descargas de canales](https://aka.ms/EdgeEnterprise)
