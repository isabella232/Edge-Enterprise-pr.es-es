---
title: Introducción a los canales de Microsoft Edge
ms.author: srugh
author: RyanHechtMSFT
manager: seanlynd
ms.date: 09/23/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Introducción a los canales de Microsoft Edge
ms.openlocfilehash: dd65d932950be90d3d9278fa41ae843335b2074d
ms.sourcegitcommit: 8e5294e82cf62abc916cfd24692f55925330d42b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2021
ms.locfileid: "12037199"
---
# <a name="overview-of-the-microsoft-edge-channels"></a>Información general sobre los canales de Microsoft Edge

Una de las ventajas de la próxima versión de Microsoft Edge es que Microsoft puede proporcionar nuevas características de forma periódica. Sin embargo, como administrador que implementa Microsoft Edge para los usuarios de su organización, es posible que quieras tener un mayor control sobre la frecuencia con la que los usuarios obtienen estas nuevas características. Microsoft proporciona cuatro opciones, denominadas canales, para controlar la frecuencia con la que Microsoft Edge se actualiza con las nuevas características. Esta es una introducción a las cuatro opciones.

Para obtener más información sobre la compatibilidad con cada canal, lea: [Ciclo de vida de Microsoft Edge](/deployedge/microsoft-edge-support-lifecycle)
  
> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="channel-overview"></a>Introducción a los canales

|Canal|Finalidad principal|Frecuencia con la que se actualiza con nuevas características|¿Compatible?|
|:---:|---|:---:|:---:|
|[Estable](#stable-channel)|Amplia implementación|~4 semanas|Sí|
|[Estable extendido](#extended-stable-channel)|Una opción de versión empresarial para Stable alineada a un ciclo de lanzamiento más largo |~8 semanas|Sí|
|[Beta](#beta-channel)|Validación representativa en la organización|~4 semanas|Sí|
|[Dev](#dev-channel)|Planificación y desarrollo|Semanal|No|
|[Canary](#canary-channel)|Contenido de vanguardia|Diariamente|No|

El canal de actualización que decida implementar para los usuarios depende de varios factores, como cuántas aplicaciones de línea de negocio aprovecha el usuario y que necesita probar cada vez que tengan una versión actualizada de Microsoft Edge. Para ayudarte a tomar esta decisión, revisa la siguiente información sobre los cuatro canales de actualización disponibles para Microsoft Edge.

### <a name="stable-channel"></a>Canal estable

El canal estable está pensado para una implementación amplia en la organización y es el canal en el que deberían estar la mayoría de los usuarios. Es el más estable de los canales y es el resultado de la estabilización del conjunto de características disponible en la versión anterior del Canal Beta. Las nuevas características se envían cada 4 semanas. Se distribuyen actualizaciones de seguridad y calidad según sea necesario. Se otorga servicio a una versión del canal estable hasta que la siguiente versión del canal esté disponible.

### <a name="beta-channel"></a>Canal beta

El canal beta está pensado para la implementación de producción en la organización para un conjunto de muestra representativo de usuarios. Es una versión compatible y se otorga servicio a todas las versiones de la versión beta hasta que la siguiente versión de este canal esté disponible. Esta es una excelente oportunidad para validar que las cosas funcionan según lo previsto en tu entorno y, si se produce un problema, solucionarlo antes de que la versión se publique en el canal estable. Las nuevas características se envían cada 4 semanas. Se distribuyen actualizaciones de seguridad y calidad según sea necesario.

### <a name="dev-channel"></a>Canal Dev

El canal Dev está pensado para ayudarte a planear y desarrollar con las últimas funciones de Microsoft Edge, pero con una mayor calidad que el canal Canary. Esta es tu oportunidad de echarle un vistazo a lo que viene en camino y de prepararte para la próxima versión Beta.

### <a name="canary-channel"></a>Canal Canary

El canal Canary se distribuye a diario y es el que está más en la vanguardia de todos los canales. Si desea tener acceso a las inversiones más nuevas, aparecerán aquí primero. Debido a la naturaleza de esta cadencia, surgirán problemas con las horas extra, por lo que es posible que quieras que se instale otro canal en paralelo si estás aprovechando las versiones de Canary.

### <a name="extended-stable-channel"></a>Canal estable extendido

A diferencia de nuestros canales de vista previa (Canary, Dev y Beta), el canal estable extendido no está disponible como una aplicación de explorador independiente; en su lugar, es una opción de versión de empresa para la aplicación estable de Microsoft Edge que está alineada a un ciclo de lanzamiento principal de 8 semanas más largo (en lugar del ciclo de lanzamiento principal de 4 semanas que se encuentra en Estable). Aunque se recomienda actualizar automáticamente Stable en su ciclo de lanzamiento de 4 semanas, Extended Stable existe para servir de forma más eficaz a las organizaciones que pueden requerir una escala de tiempo más larga para probar y validar nuevas versiones de explorador.

La opción de ciclo de lanzamiento "Estable extendido" de 8 semanas para __ Microsoft Edge Stable ofrece actualizaciones de características acumulativas alineadas con versiones numeradas uniformes a partir de Microsoft Edge 94; las actualizaciones de características de las versiones impares se empaquetarán y entregarán como parte de la versión pares posterior. Por ejemplo, si una organización selecciona el ciclo de lanzamiento "Estable extendido" de 8 semanas con Microsoft Edge 94, recibirá actualizaciones de características posteriores con Microsoft Edge 96, Microsoft Edge 98, y así sucesivamente. Aunque las actualizaciones de características se empaquetan y se entregan con nuevas versiones basadas en el ciclo de lanzamiento seleccionado, las revisiones y correcciones de seguridad importantes se entregarán según sea necesario independientemente de la opción de versión seleccionada para ayudar a mantener la seguridad del explorador. Los clientes pueden optar por la opción de versión estable extendida en cualquier momento y tendrá efecto con la próxima versión estable extendida.

![Ejemplo de comparación Microsoft Edge de ciclo de lanzamiento estable y estable extendido.](./media/microsoft-edge-channels/extended-stable-explainer.png)

#### <a name="opting-in-to-the-extended-stable-release-cadence"></a>Participar en la cadencia de versión estable extendida

##### <a name="opting-in-to-extended-stable-on-windows-with-automatic-updates-recommended"></a>Opting-in to Extended Stable on Windows with Automatic Updates (recommended)

Si actualiza automáticamente Microsoft Edge, puede usar objetos de directiva de grupo para participar en la Cadencia de versión estable extendida. [Siga esta guía para](/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template) obtener más información sobre cómo descargar e instalar las plantillas administrativas más recientes Microsoft Edge directivas de grupo.

1. Abra el editor de directivas de grupo local y vaya a _Configuración del equipo>Plantillas administrativas>Microsoft Edge Update>Aplicaciones>Microsoft Edge>_.
2. Seleccione **Reemplazar canal de destino** y, a continuación, seleccione **Habilitado**.
3. En **Opciones,** seleccione **"Estable extendido"** de la lista desplegable Directiva.

Cuando se lanza la siguiente actualización del canal estable extendido que tiene un número de versión mayor que el que tiene instalado actualmente el dispositivo, Microsoft Edge se actualizará automáticamente al canal estable extendido. La cadena de versión `edge://settings/help` en indicará que está ejecutando un canal diferente.

> [!NOTE]
> La suscripción a Estable extendido surte efecto cuando haya una nueva actualización en el canal estable extendido con un número de versión mayor (mayor o menor) que el que está instalado actualmente en el dispositivo. Si ejecuta la versión más reciente de Microsoft Edge Stable y opt-in a Extended Stable, tendrá efecto con la siguiente revisión o actualización de Microsoft Edge.
>
> De forma predeterminada, Microsoft Edge no se degradará por sí mismo. Si actualmente está ejecutando una versión impar numerada de Microsoft Edge Stable, la suscripción a Extended Stable significará que no recibirá actualizaciones hasta la siguiente versión de Microsoft Edge pares.
>
> Si quieres asegurarte de que todos los dispositivos comiencen con una versión específica de Extended Stable, puedes implementar esa versión específica de Edge Stable como msi con reversión habilitada. Por ejemplo, si quieres empezar con Extended Stable 94, pero algunos dispositivos ya se han actualizado a Stable 95, puedes implementar un MSI de Edge 94 con reversión habilitada. Para obtener más información sobre cómo implementar MSIs perimetrales con reversión habilitada, consulte nuestra [guía de reversión.](/DeployEdge/edge-learnmore-rollback)

##### <a name="opting-in-to-extended-stable-on-windows-via-intune"></a>Opting-in to Extended Stable on Windows via Intune

Microsoft Edge Las plantillas administrativas se pueden administrar de forma similar a los objetos de directiva de grupo locales desde Microsoft Endpoint Manager centro de administración. Siga nuestra [guía sobre cómo configurar Microsoft Edge con Intune](/mem/intune/configuration/administrative-templates-configure-edge). 

La configuración "**Reemplazo de**canal de destino " se encuentra en las subcarpetas " Microsoft Edge Update >_Aplicaciones>Microsoft Edge_" . Debe establecerse en "**Estable extendido"** 

Cuando se lanza la siguiente actualización del canal estable extendido que tiene un número de versión mayor que el que tiene instalado actualmente el dispositivo, Microsoft Edge se actualizará automáticamente al canal estable extendido. La cadena de versión `edge://settings/help` en indicará que está ejecutando un canal diferente.

##### <a name="opting-in-to-extended-stable-on-windows-via-configuration-manager"></a>Opting-in to Extended Stable on Windows via Configuration Manager

Consulte nuestra guía sobre cómo [actualizar Microsoft Edge con Configuration Manager](/mem/configmgr/apps/deploy-use/deploy-edge#update-microsoft-edge) para obtener más información sobre cómo sincronizar y aprobar Microsoft Edge actualizaciones en Configuration Manager.

Las actualizaciones estables extendidas se distribuyen en la biblioteca de software en la categoría de producto "Microsoft Edge", similar a las actualizaciones existentes para los canales Estable, Beta y Desarrollo. Sin embargo, a diferencia de Beta y Dev, que se aplican a sus propias aplicaciones de explorador, las actualizaciones estables extendidas se aplican Microsoft Edge aplicación estable. Por lo tanto, para que el Windows Update determine si se deben aplicar actualizaciones estables o estables extendidas, comprueba el estado de la directiva de grupo "Invalidación de canal de destino". Si la directiva no está configurada o está establecida en "Estable", se aplicarán actualizaciones estables. Si se establece en "Estable extendido", se aplicarán actualizaciones estables extendidas. Siga las instrucciones anteriores para participar en Estable extendido con actualizaciones automáticas para obtener instrucciones sobre cómo establecer correctamente la directiva de grupo. 

## <a name="flighting-pre-release-channels-in-your-organization"></a>Flighting Pre-release Channels in your Organization

La directiva de grupo "Invalidación de canal de destino" también se puede usar para realizar un vuelo sin problemas de los canales de versión previa de Microsoft Edge en la organización sin que los usuarios necesiten usar una segunda aplicación de explorador web. Por ejemplo, puede establecer la directiva "Invalidación de canal de destino" en "Beta" para un conjunto de ejemplo representativo de usuarios de la organización. Cuando esos usuarios abran Microsoft Edge, ejecutarán la versión del canal beta en lugar de Estable (probablemente sin que ni siquiera se den cuenta). Esto puede proporcionar una visión temprana de cómo se llevará a cabo la próxima versión de Microsoft Edge en su empresa y ayudar a validar que todo funciona según lo esperado en su entorno. Los usuarios que encuentren algún problema y puedan asegurarse de que se corrigen antes de la publicación de la versión en el canal estable, se obtienen las primeras señales de los usuarios que se encuentran con algún problema. Como parte de la solución del problema de un usuario, la cadena de versión en le informará si el canal del usuario es diferente del `edge://settings/help` canal estable predeterminado.

> [!NOTE]
> Dado que la compilación en los canales "Beta" y "Dev" de Microsoft Edge tienen números de versión principales mayores que el de "Estable", si lleva una actualización al canal "Beta" o "Dev" y desea volver a Estable, se requiere la característica de reversión de [Microsoft Edge.](/DeployEdge/edge-learnmore-rollback) Si simplemente estableces "Invalidación de canal de destino" en Estable, no recibirás actualizaciones hasta que la versión estable más reciente tenga un número de versión mayor que la versión de Microsoft Edge que estás ejecutando actualmente en el dispositivo.

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Descargas de canales](https://aka.ms/EdgeEnterprise)
