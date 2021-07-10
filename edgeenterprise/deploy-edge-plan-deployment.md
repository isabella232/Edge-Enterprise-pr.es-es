---
title: Planear tu implementación de Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Planear tu implementación de Microsoft Edge
ms.openlocfilehash: be85aa5182bbee51f90fe42e80cdee0b9c793b4e
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641946"
---
# <a name="plan-your-deployment-of-microsoft-edge"></a>Planear tu implementación de Microsoft Edge

En este artículo se describen los procedimientos recomendados para la implementación de Microsoft Edge en un entorno empresarial.

>[!NOTE]
>Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

En las secciones siguientes se proporcionan instrucciones específicas para planear la implementación de Microsoft Edge.

- [Evalúa tu entorno de explorador y requisitos](#evaluate-your-existing-browser-environment-and-browser-needs)
- [Asegúrate de que los dispositivos con Windows 10 están listos](#make-sure-your-windows-10-devices-are-ready)
- [Elige la metodología de implementación](#determine-your-deployment-methodology)
- [Realizar detección de sitio](#do-site-discovery)
- [Elige la estrategia del canal](#determine-your-channel-strategy)
- [Identifica y configura directivas](#define-and-configure-policies)
- [Realiza pruebas de compatibilidad de aplicaciones](#do-app-compatibility-testing)
- [Piloto de Microsoft Edge](#deploy-microsoft-edge-to-a-pilot-group)
- [Evalúa el piloto](#validate-your-deployment)
- [Implementa Microsoft Edge en toda la empresa](#broad-deployment-of-microsoft-edge)

## <a name="evaluate-your-existing-browser-environment-and-browser-needs"></a>Evalúa las necesidades del explorador y del entorno del explorador existentes

Dedica tiempo a comprender la visión del proyecto y el estado del explorador actual para garantizar que todas las partes interesadas del proyecto están coordinadas y trabajan por el mismo resultado.

Para empezar, define tu estado actual:

- ¿Qué exploradores están implementados actualmente en tu entorno?
- ¿Qué explorador está establecido como explorador predeterminado?
- ¿Necesitas usar Internet Explorer para algunas de tus aplicaciones?
- ¿Usas una lista de sitios del Modo de empresa para configurar Internet Explorer hoy?
- ¿Qué plataformas del SO se admiten con tu entorno? (Windows 10, macOS, Windows 7, Windows Server, etc.)
- ¿Qué herramientas de administración usas para la administración del explorador?
- ¿Quién es responsable de la configuración y la administración del explorador?
- ¿Cuál es tu proceso para validar la compatibilidad de explorador?

Después de comprender el estado actual, puedes determinar los objetivos deseados para la implementación del explorador, teniendo en cuenta lo siguiente:

- ¿Quieres [establecer Microsoft Edge como tu explorador predeterminado](./edge-default-browser.md)?
- ¿Cómo [configurarás Microsoft Edge](./configure-microsoft-edge.md)?
- ¿Qué características son críticas para configurarlas como parte de tu implementación inicial?
- ¿Cuál es el proceso para abordar los problemas de compatibilidad o configuración identificados?

También debes comprender los **requisitos previos** para las características que te interesan, como:

- [Protección de aplicaciones de Windows Defender](/windows/security/threat-protection/windows-defender-application-guard/reqs-wd-app-guard)
- [Modo Internet Explorer](./edge-ie-mode.md)
- [Autenticación y sincronización](./microsoft-edge-security-identity.md)

Teniendo en cuenta estas respuestas, estás listo para planear la implementación de Microsoft Edge.
<!--bookmark -->

## <a name="make-sure-your-windows-10-devices-are-ready"></a>Asegúrate de que los dispositivos con Windows 10 están listos

El canal estable de Microsoft Edge requiere la última actualización acumulativa (LCU) de octubre 2019 (o posterior). Si intentas implementar en un dispositivo Windows 10 que tiene una LCU anterior, la instalación fallará. Para más información sobre la LCU mínima que se debe aplicar antes de implementar Edge, consulta [Actualizaciones de Windows para admitir la próxima versión de Microsoft Edge](./microsoft-edge-sysupdate-windows-updates.md).

## <a name="determine-your-deployment-methodology"></a>Determinar tu metodología de implementación

Cuando sepas el estado final que deseas, estarás listo para empezar a planear cómo llegar allí. Los dos métodos principales para implementar Microsoft Edge son por rol y por sitio.

### <a name="deploy-to-end-users-by-role"></a>Implementar en usuarios finales por rol

Si la compatibilidad de aplicaciones es tu principal preocupación y no sabes bien qué aplicaciones probar, es posible que quieras considerar la posibilidad de implementar para usuarios finales por rol. Esto permite que cada oleada de una implementación por fases proporcione comentarios e información sobre las aplicaciones que quizás deban modificarse para tener su configuración modificada para abordar problemas de compatibilidad.

### <a name="deploy-to-end-users-by-site"></a>Implementar en usuarios finales por sitio

Si el ancho de banda es tu principal preocupación, es posible que quieras considerar la posibilidad de realizar pruebas de compatibilidad de aplicaciones por adelantado. Una vez finalizadas la pruebas, implementa en usuarios finales por sitio para que puedas aprovechar el almacenamiento en caché de otras optimizaciones de distribución de software.

## <a name="do-site-discovery"></a>Realizar detección de sitio

Si tienes una dependencia de aplicaciones web heredadas y planeas usar el modo Internet Explorer (lo que hacen la mayoría de los clientes), es probable que tengas que realizar una detección adicional del sitio.

### <a name="if-youve-already-deployed-and-configured-the-legacy-version-of-microsoft-edge"></a>Si ya has implementado y configurado la versión heredada de Microsoft Edge

Si ya has configurado tu lista de sitios de empresa para que funcione con la versión heredada de Microsoft Edge, tu trabajo está casi hecho. Lo único que puedes tener que agregar son sitios neutros.

Los sitios neutros son normalmente sitios que proporcionan inicio de sesión único (SSO). Si navegas a un sitio neutro desde Microsoft Edge, querrás quedarte en Microsoft Edge para autenticar. Si navegas a un sitio neutro en el modo Internet Explorer, querrás quedarte en el modo Internet Explorer para autenticar.

Identifica cualquier sitio SSO (u otros sitios neutros) que uses y agrégalos a tu lista de sitios de empresa.

### <a name="if-youve-configured-internet-explorer-as-your-default-browser"></a>Si has configurado Internet Explorer como explorador predeterminado

Si actualmente solo usas Internet Explorer, es posible que no sepas qué sitios se han actualizado a los estándares web modernos y que aún requieren Internet Explorer. Quieres encontrar estos sitios y agregarlos a la lista de sitios de empresa. Esto te permite usar el modo Internet Explorer solo en los sitios que lo necesitan.

> [!TIP]
> Usa las herramientas de [detección de sitio de empresa](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery) para detectar los sitios que pueden necesitar el modo Internet Explorer. Puedes recopilar datos de equipos que ejecutan Windows Internet Explorer 8 a través de Internet Explorer 11 en Windows 10, Windows 8.1 o Windows 7.

### <a name="analyze-site-discovery-data"></a>Analizar datos de detección de sitios

Una vez que hayas recopilado los datos del sitio, te recomendamos que sigas un proceso de cuatro pasos para analizar los datos:

1. Ordenar los datos por dominio y, a continuación, por URL.
2. Definir los límites de una "aplicación" que debes configurar para el modo Internet Explorer. Quieres incluir todos los sitios y controles web que definen la aplicación. Pero no quieres incluir más sitios ni controles adicionales definiendo la aplicación de forma demasiado general. Algunos sitios pueden ser tan sencillos como "http://contoso.com/app1" , mientras que otros pueden requerir que definas varios sitios y páginas.
3. Prueba la aplicación para comprobar que no funciona de forma nativa. Muchos sitios ofrecerán contenido moderno cuando detecten un explorador moderno y solo ofrecerán contenido heredado cuando detecten Internet Explorer.
4. Agrega la aplicación a la lista de sitios de empresa si la prueba no se realiza correctamente.

   > [!NOTE]
   > Como práctica recomendada, agrupa todos los sitios que componen una aplicación. Si se necesitan todos los sitios para realizar una tarea y tienden a actualizarse a la vez, es una buen indicador que deben agruparse. De esta manera, al actualizar una aplicación, es más sencillo eliminar todo el sitio del modo Internet Explorer y empezar a usar un explorador moderno para esa aplicación.

## <a name="determine-your-channel-strategy"></a>Determinar la estrategia de canal

Microsoft Edge se publica en [varios canales](./microsoft-edge-channels.md).

> [!NOTE]
> Puedes instalar más de un canal en un dispositivo.

El canal estable es lo que querrás implementar en la mayoría de los dispositivos. Sin embargo, debes pensar en una estrategia de implementación que incluya varios dispositivos y canales.

### <a name="multiple-devices-and-channels"></a>Varios dispositivos y canales

Se recomienda tener un subconjunto representativo de dispositivos configurados para usar el canal beta. Esto te permite obtener una vista previa de los próximos cambios al explorador. Puedes ver si estos cambios van a afectar a los usuarios finales o a las aplicaciones.

Es posible que también quieras que el canal Dev (o incluso el canal Canary) esté disponible para algunos roles, como los desarrolladores web. Piensa si deseas tener como objetivo algunos dispositivos con canales más fluidos y que cambian rápidamente, o simplemente hacer que estos canales estén disponibles para que los usuarios puedan elegir instalarlos.

Dado que es posible instalar varios canales en un dispositivo, puedes reducir el riesgo de pruebas para los usuarios que hayan decidido instalar un canal de versión preliminar. Por ejemplo, si tienes un usuario que usa el canal Beta y hay un problema, puede cambiar al canal estable y seguir trabajando. De esta forma, se desbloquearán hasta que se pueda solucionar el problema.

> [!NOTE]
> Si el usuario ha habilitado la sincronización, su configuración se sincronizará entre los canales, lo que facilitará aún más la transición entre canales.

## <a name="define-and-configure-policies"></a>Definir y configurar directivas

Una vez que hayas creado tu lista de sitios de empresa, recomendamos identificar y configurar las directivas que piensas implementar con Microsoft Edge. De esta forma, se garantiza que estas directivas se aplican al realizar las pruebas.

En primer lugar, ten en cuenta la experiencia de primera ejecución que quieres que tengan los usuarios. Si quieres importar automáticamente la configuración desde el explorador actual, configura la directiva para [AutoImportAtFirstRun.](./microsoft-edge-policies.md#autoimportatfirstrun)

Para las directivas de seguridad, te recomendamos que comiences con la línea base de seguridad de Microsoft Edge. La línea base de seguridad puede aplicarse mediante la [configuración recomendada de la línea base de configuración de seguridad](https://techcommunity.microsoft.com/t5/Microsoft-Security-Baselines/Security-baseline-DRAFT-for-Chromium-based-Microsoft-Edge/ba-p/949991) o con [Microsoft Intune](/intune/protect/security-baseline-settings-edge).

Para otras directivas, te recomendamos que revises las configuraciones de directiva para [Microsoft Edge](./microsoft-edge-policies.md) y [Microsoft Edge Updates](./microsoft-edge-update-policies.md).

### <a name="define-your-update-strategy-and-policies"></a>Definir la estrategia de actualización y las directivas

También quieres determinar cómo quieres realizar las actualizaciones después de implementar Microsoft Edge:

- **Permitir que Microsoft Edge se actualice** (predeterminado). Si eliges permitir las actualizaciones automáticas de Microsoft Edge, Microsoft Edge se actualizará automáticamente al ritmo determinado por los canales que has implementado.
- **Actualiza Microsoft Edge a tu propio ritmo**. Si prefieres tener un control explícito sobre cuándo se implementan las actualizaciones, puedes deshabilitar las actualizaciones automáticas e implementarlas tú mismo(consulta [Actualizar referencia de directiva](./microsoft-edge-update-policies.md)). Después de deshabilitar las actualizaciones automáticas, puedes implementar actualizaciones para cada canal con una de las siguientes herramientas:

- [Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
- [Configuration Manager](./deploy-edge-with-configuration-manager.md)
- La herramienta de implementación que elijas.

Con independencia de la estrategia de actualización, te recomendamos que aproveches una estrategia de implementación anillada. Con las actualizaciones automáticas, esto implica tener una muestra representativa de los usuarios que ejecutan el canal beta para identificar problemas de lo que se convertirá en el canal estable. Con las actualizaciones manuales, esto también puede incluir una validación adicional de un grupo piloto después de que se publique una nueva compilación de canal estable. Esto va seguido de una amplia implementación.

>[!NOTE]
>El soporte de Microsoft Edge solo se aplicará a la versión más reciente de Microsoft Edge de cada canal

## <a name="do-app-compatibility-testing"></a>Realizar pruebas de compatibilidad de aplicaciones

La compatibilidad de aplicaciones para Microsoft Edge es muy alta, tan alta que Microsoft proporciona las siguientes promesas de compatibilidad:

1. Si funciona en Microsoft Edge *versión 45 y versiones anteriores*, funcionará en Microsoft Edge *versión 77 y posteriores*.
2. Si funciona en Internet Explorer, funcionará en Microsoft Edge en el modo Internet Explorer.
3. Si funciona en Google Chrome, funcionará en Microsoft Edge.

Si dispones de una aplicación en la que no se cumple esta promesa de compatibilidad, lo solucionaremos con [Microsoft App Assure](https://www.microsoft.com/fasttrack/microsoft-365/desktop-app-assure).

### <a name="internal-line-of-business-app-testing"></a>Línea interna de pruebas de aplicaciones de negocio

A pesar de nuestra promesa de compatibilidad, sabemos que muchas organizaciones deben validar algunas aplicaciones por motivos de cumplimiento o administración de riesgos. Aunque esperamos que esto sea muy sencillo, es importante que ser organizado y riguroso en las pruebas de la aplicación.

Hay dos maneras de realizar las pruebas de compatibilidad de aplicaciones:

1. Pruebas de laboratorio. Las aplicaciones se validan en un entorno de muy controlado con configuraciones específicas.
2. Pruebas piloto. Un número limitado de usuarios validan las aplicaciones en su entorno de trabajo diario usando sus propios dispositivos.

Elige el método más apropiado para cada aplicación, para administrar el riesgo sin invertir demasiado en pruebas de compatibilidad.

### <a name="third-party-app-support"></a>Soporte para aplicaciones de terceros

A parte de sus propias líneas de aplicaciones de negocio, muchas organizaciones usan aplicaciones de orígenes externos. El artículo [Preparado para Microsoft Edge](deploy-edge-ready-for-edge.md) contiene una lista de aplicaciones web que pueden usarse en la organización. En esta lista se proporcionan vínculos a las instrucciones de soporte técnico de los productos cuando se usan con Microsoft Edge.

## <a name="deploy-microsoft-edge-to-a-pilot-group"></a>Implementar Microsoft Edge en un grupo piloto

Una vez que hayas definido las directivas y hayas finalizado la prueba de compatibilidad de aplicación inicial, estarás listo para implementar en tu grupo piloto. Implementa en tu grupo piloto mediante una de las siguientes herramientas:

- [Microsoft Intune para Windows](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) o [Microsoft Intune para macOS](/intune/apps/apps-edge-macos?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
- [Configuration Manager](./deploy-edge-with-configuration-manager.md).
- Otra herramienta de administración, descarga e implementa [el archivo MSI para Microsoft Edge](https://www.microsoftedgeinsider.com/enterprise).

## <a name="validate-your-deployment"></a>Validar tu implementación

Después de implementar tu piloto, quieres capturar todos los comentarios que recibes de tus usuarios.

- Captura comentarios sobre la compatibilidad. Identifica los sitios que pertenecen a la lista de sitios de empresa que no se identificaron durante la detección de sitios.
- Capturar comentarios sobre la configuración de directiva. Asegúrate de que los usuarios puedan usar características clave y que realicen su trabajo mientras siguen las directrices de seguridad.
- Captura comentarios sobre la facilidad de uso y las nuevas características. Identifica las áreas en las que se debe desarrollar y ofrecer la formación en función de las preguntas del usuario.

## <a name="broad-deployment-of-microsoft-edge"></a>Amplia implementación de Microsoft Edge

Después de finalizar el piloto y actualizar el plan de implementación con las lecciones aprendidas del piloto, estarás listo para realizar una implementación completa de Microsoft Edge para todos los usuarios.  ¡Enhorabuena!

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: Implementación de Microsoft Edge](microsoft-edge-video-deploy.md)