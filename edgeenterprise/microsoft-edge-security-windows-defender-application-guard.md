---
title: Microsoft Edge y Protección de aplicaciones de Microsoft Defender
ms.author: srugh
author: AndreaLBarr
manager: seanlyn
ms.date: 05/06/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Compatibilidad de Microsoft Edge para la Protección de aplicaciones de Microsoft Defender
ms.openlocfilehash: 7374810eb19ada298963817844e52184c0271a8c
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618000"
---
# <a name="microsoft-edge-support-for-microsoft-defender-application-guard"></a>Compatibilidad de Microsoft Edge para la Protección de aplicaciones de Microsoft Defender

En el presente artículo se describe la compatibilidad de Microsoft Edge con la Protección de aplicaciones de Microsoft Defender (Protección de aplicaciones).

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="overview"></a>Introducción

Los arquitectos de seguridad en la empresa deben lidiar con la tensión que existe entre la productividad y la seguridad. Es relativamente fácil bloquear un navegador y sólo permitir que se cargue un puñado de sitios de confianza. Este enfoque mejorará la postura general de seguridad, pero podría decirse que es menos productivo. Si lo hace menos restrictivo para mejorar la productividad, aumenta el perfil de riesgo. ¡Es un equilibrio difícil de conseguir!

Es aún más difícil mantenerse al día con las nuevas amenazas emergentes en este paisaje de amenazas en constante cambio. Los navegadores siguen siendo la principal superficie de ataque a los dispositivos clientes porque el trabajo básico del navegador es permitir a los usuarios acceder, descargar y abrir contenido no fiable de fuentes no fiables. Los actores malintencionados trabajan constantemente en la ingeniería social de nuevas formas de ataques en contra del navegador. La prevención de incidentes de seguridad o las estrategias de detección/respuesta no pueden garantizar el 100% de seguridad.

Una estrategia de seguridad clave a considerar es la [Metodología de supresión de Infracciones](/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology), lo que significa que se acepta que un ataque va a tener éxito al menos una vez, independientemente de los esfuerzos para evitarlo. Esta mentalidad requiere la construcción de defensas para contener el daño, lo que asegura que la red corporativa y otros recursos permanezcan protegidos en este escenario.  El despliegue de la protección de aplicaciones para Microsoft Edge encaja perfectamente en esta estrategia

## <a name="about-application-guard"></a>Acerca de la protección de aplicaciones

Diseñado para la protección de aplicaciones de Windows 10 y Microsoft Edge, utiliza un enfoque de aislamiento de hardware. Este enfoque permite que la navegación de sitios no confiables se lance dentro de un contenedor. El aislamiento de hardware ayuda a las empresas a proteger su red corporativa y sus datos en caso de que los usuarios visiten un sitio que esté comprometido o sea malintencionado.

El administrador de la empresa define el concepto de sitios de confianza, los recursos de la nube y las redes internas. Todo lo que no está en la lista de sitios de confianza se considera no confiable. Estos sitios están aislados de la red corporativa y de los datos del dispositivo del usuario.

Para más información:

- vea nuestro vídeo [aislamiento del explorador Microsoft Edge usando Protección de aplicaciones](microsoft-edge-video-security-application-guard.md)
- consulte [Qué es la Protección de aplicaciones y cómo funciona?](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work)

La siguiente captura de pantalla muestra un ejemplo del mensaje de protección de aplicaciones en donde muestra que el usuario está navegando en un espacio seguro.

![Mensaje de navegación segura de protección de aplicaciones](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## <a name="whats-new"></a>Novedades

La Protección de aplicaciones tiene la misma compatibilidad con el nuevo navegador Microsoft Edge que con Microsoft Edge (versión anterior), e incluye varias mejoras.

### <a name="favorites-synchronizing-from-the-host-to-the-container"></a>Sincronización de favoritos desde el host al contenedor

Algunos de nuestros clientes han estado preguntando acerca de la sincronización de favoritos entre el navegador host y el contenedor en la Protección de aplicaciones. A partir de Microsoft Edge 91, los usuarios ahora tienen la opción de configurar la Protección de aplicaciones para sincronizar sus favoritos desde el host al contenedor. Esto garantiza que aparezcan también nuevos favoritos en el contenedor.

Se puede controlar esta compatibilidad por medio de una directiva. Puede actualizar la directiva de Edge [ApplicationGuardFavoritesSyncEnabled](/deployedge/microsoft-edge-policies#applicationguardfavoritessyncenabled) para habilitar o deshabilitar la sincronización de favoritos.

> [!Note]
> Por motivos de seguridad, la sincronización de favoritos solo es posible desde el host al contenedor y no en el sentido contrario. Para garantizar una lista unificada de favoritos en el host y el contenedor, hemos deshabilitado la administración de favoritos dentro del contenedor.

### <a name="identify-network-traffic-originating-from-the-container"></a>Identificar el tráfico de red que se genera desde el contenedor

Varios clientes usan WDAG en una configuración específica en la que desean identificar el tráfico de red procedente del contenedor. Algunos de los escenarios para esto son:

- Para restringir el acceso a solo un puñado de sitios que no sean de confianza
- Para permitir el acceso a Internet solo desde el contenedor

A partir de Microsoft Edge versión 91, existe compatibilidad integrada para etiquetar el tráfico de red procedente de los contenedores de la Protección de aplicaciones, lo que permite que las empresas utilicen proxy para filtrar el tráfico y aplicar directivas específicas. Puede usar el encabezado para identificar el tráfico del contenedor o del host mediante [ApplicationGuardTrafficIdentificationEnabled](/deployedge/microsoft-edge-policies#applicationguardtrafficidentificationenabled).

### <a name="extension-support-inside-the-container"></a>Compatibilidad de extensión dentro del contenedor

La compatibilidad de extensión dentro del contenedor ha sido una de las principales peticiones de los clientes. Los escenarios varían desde querer ejecutar bloqueadores de anuncios dentro del contenedor para aumentar el rendimiento del navegador hasta tener la capacidad de ejecutar extensiones caseras personalizadas dentro del contenedor.

La extensión que se instala en el contenedor es ahora compatible, a partir de la versión 81 de Microsoft Edge. Este apoyo puede ser controlado a través de la directiva. La `updateURL` que se usa en la directiva[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist)debe agregarse como recursos neutros en las directivas de aislamiento de red usados por la protección de aplicaciones.

Algunos ejemplos de compatibilidad con los contenedores incluyen los siguientes escenarios:

- Instalación forzosa de una extensión en el host
- Retirar una extensión del host
- Extensiones bloqueadas en el host

> [!NOTE]
> También es posible instalar manualmente extensiones individuales dentro del contenedor desde el almacén de extensiones. Las extensiones instaladas manualmente sólo persistirán en el contenedor cuando se active la directiva de [Permitir persistencia](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings).

### <a name="identifying-application-guard-traffic-via-dual-proxy"></a>Identificar el tráfico de Protección de aplicaciones mediante proxy doble

Algunos clientes empresariales están implementando la Protección de aplicaciones en un caso de uso específico en el que es necesario identificar el tráfico web que sale de un contenedor de la Protección de aplicaciones de Microsoft Defender a nivel de proxy. Para cumplir este requisito, a partir de la versión de canal estable 84, Microsoft Edge es compatible con el proxy doble. Para configurar esta funcionalidad, puede usar la directiva [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy).

El siguiente dibujo muestra la arquitectura de proxy doble para Microsoft Edge.

![Arquitectura de proxy doble para la Protección de aplicaciones](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### <a name="diagnostic-page-for-troubleshooting"></a>Página de diagnóstico para la solución de problemas

Otro punto de dificultad para el usuario es la resolución de problemas de la configuración de aplicaciones la protección de en un dispositivo cuando se informa de un problema. Microsoft Edge tiene una página de diagnóstico (`edge://application-guard-internals`) para solucionar los problemas de los usuarios. Uno de estos diagnósticos es poder comprobar la confianza de la URL en base a la configuración del dispositivo del usuario.

La siguiente captura de pantalla muestra una página de diagnóstico de múltiples pestañas para ayudar a diagnosticar los problemas reportados por el usuario en el dispositivo.

![Página diagnóstico de protección de aplicaciones](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### <a name="microsoft-edge-updates-in-the-container"></a>Las actualizaciones de Microsoft Edge en el contenedor

Las actualizaciones de Microsoft Edge Legacy en el contenedor son parte del ciclo de actualización del sistema operativo Windows. Debido a que la nueva versión de Microsoft Edge se actualiza a sí misma independientemente del sistema operativo Windows, ya no hay dependencia de las actualizaciones de los contenedores. El canal y la versión del host Microsoft Edge se replica en el interior del contenedor.

## <a name="prerequisites"></a>Requisitos previos

Los siguientes requisitos se aplican a los dispositivos que utilizan la protección de aplicaciones con Microsoft Edge:

- Windows 10 1809 (RS5) y superior.
- Sólo SKUs de clientes de Windows

  > [!NOTE]
  > La protección de aplicaciones sólo es compatible con las SKU de Windows 10 Pro y Windows 10 Enterprise.

- Una de las soluciones de administración descritas en [Requisitos de software](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)

## <a name="how-to-install-application-guard"></a>Como instalar la protección de aplicaciones

Los siguientes artículos proporcionan la información necesaria para instalar, configurar y probar la protección de aplicaciones con Microsoft Edge.

- [Requisitos del sistema](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [Instalar la Protección de aplicaciones de Microsoft Defender](/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [Configurar los ajustes de la directiva de grupo de Microsoft Defender](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [Probar la protección de aplicaciones.](/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

### <a name="does-application-guard-work-in-ie-mode"></a>¿La Protección de aplicaciones funciona en el modo IE?

El modo IE admite la funcionalidad de Protección de aplicaciones, pero no se anticipa mucho el uso de esta característica en este modo. Se recomienda implementar el modo IE para una lista de sitios internos de confianza y la Protección de aplicaciones solo para sitios que no sean de confianza. Asegúrese de que todos los sitios o direcciones IP del modo IE se añadan también a la directiva de aislamiento de la red para que la protección de aplicaciones los considere como un recurso de confianza.

### <a name="do-i-need-to-install-the-application-guard-chrome-extension"></a>¿Necesito instalar la extensión de protección de aplicaciones en Chrome?

No, la función de protección de aplicaciones es compatible de forma nativa en Microsoft Edge. De hecho, la extensión protección de aplicaciones de Chrome no es una configuración compatible con Microsoft Edge.

### <a name="are-there-any-other-platform-related-faqs"></a>¿Hay otras preguntas más frecuentes relacionadas con la plataforma?

Sí. [Preguntas más frecuentes: Protección de aplicaciones de Microsoft Defender](/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Protección contra amenazas avanzada de Microsoft Defender](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [Vídeo: aislamiento de explorador de Microsoft Edge usando protección de aplicaciones](https://www.youtube.com/watch?v=zQjaRqNXMqw&t=3s)