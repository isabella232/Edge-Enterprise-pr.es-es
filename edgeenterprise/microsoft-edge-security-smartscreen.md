---
title: Soporte técnico de Microsoft Edge para SmartScreen de Microsoft Defender
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Soporte técnico de Microsoft Edge para SmartScreen de Microsoft Defender
ms.openlocfilehash: 2de93b4ebe26b4a90592f7ee9143f6f775b682ce
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314693"
---
# Soporte técnico de Microsoft Edge para SmartScreen de Microsoft Defender

Este artículo describe los beneficios de usar SmartScreen de Microsoft Defender, explica cómo funciona y describe cómo configurar esta característica de Microsoft Edge.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

SmartScreen de Microsoft Defender es un servicio que Microsoft Edge utiliza para mantenerlo seguro mientras navega por la web. SmartScreen de Microsoft Defender proporciona un sistema de alerta temprana contra los sitios web que podrían participar en ataques de suplantación de identidad o intentar distribuir malware a través de un ataque focalizado. Para más información, vea [Vídeo: Exploración segura en Microsoft Edge](microsoft-edge-video-security-smartscreen.md).

> [!NOTE]
> Antes de Windows 10, versión 1703, esta característica se llamaba el filtro SmartScreen cuando se usaba dentro del navegador y Microsoft SmartScreen cuando se usaba fuera del navegador.

## Ventajas de SmartScreen de Microsoft Defender

SmartScreen de Microsoft Defender proporciona varios beneficios, que se resumen en la siguiente lista. Estos beneficios se describen en detalle en la documentación de[SmartScreen de Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#benefits-of-windows-defender-smartscreen). Las ventajas son:

- Soporte técnico contra la suplantación de identidad y el malware
- Protección de URL y aplicaciones basada en la reputación
- Integración del sistema operativo
- Mejora de la heurística y los datos de diagnóstico
- Administración a través de la Directiva de grupo y Microsoft Intune
- Bloqueo de URLs asociadas a aplicaciones potencialmente no deseadas

## Comprender cómo funciona SmartScreen de Microsoft Defender 

Una serie de entradas contribuyen a las advertencias de SmartScreen de Microsoft Defender. Los datos se reciben de muchas fuentes, entre ellas la retro alimentación de los usuarios, los proveedores de datos y los modelos de inteligencia. Estos datos se utilizan para ayudar a identificar el contenido potencialmente malicioso. SmartScreen de Microsoft Defender también comprueba las aplicaciones descargadas o los instaladores de aplicaciones para ver si son maliciosas. En ambos escenarios, SmartScreen de Microsoft Defender advierte a los usuarios de forma adecuada sobre contenidos sospechosos.

### Análisis del sitio

SmartScreen de Microsoft Defender determina si un sitio es potencialmente malicioso por:

- Analizando las páginas web visitadas en busca de indicios de comportamiento sospechoso.
- Comprobando los sitios visitados con un registro dinámico de los sitios de suplantación de identidad denunciados..

Si SmartScreen de Microsoft Defender determina que una página es maliciosa, mostrará una página de advertencia para notificar al usuario que ese sitio es reportado como inseguro. La siguiente captura de pantalla muestra un ejemplo de una página de advertencia de SmartScreen de Microsoft Defender cuando un usuario intenta abrir un sitio web malicioso.

![La página de bloqueo de SmartScreen de Microsoft Defender para un enlace a un sitio externo](media/microsoft-edge-security-smartscreen/microsoft-edge-smartscreen-warning.png)

Los usuarios tienen la opción de reportar un sitio como seguro o inseguro dentro del mensaje de advertencia. Para más información, consulte [como reportar un sitio](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device#how-users-can-report-websites-as-safe-or-unsafe).

### Análisis de archivo

SmartScreen de Microsoft Defender determina si una aplicación descargada o un instalador de aplicaciones es potencialmente malicioso basándose en muchos criterios, como el tráfico de descargas, el historial de descargas, los resultados anteriores del antivirus y la reputación de la URL.

- Los archivos con una reputación segura conocida se descargarán sin ninguna notificación.  
- Los archivos con una reputación maliciosa conocida muestran una advertencia para que el usuario sepa que el archivo no es seguro y ha sido reportado como malicioso. La siguiente captura de pantalla es un ejemplo de una advertencia para un archivo malicioso.

  ![SmartScreen de Microsoft Defender bloquea la notificación del archivo con reputación maliciosa](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-known-malicious.png)

- Los archivos desconocidos muestran una advertencia para que el usuario sepa que la descarga no tiene una huella conocida y aconseja precaución. La siguiente captura de pantalla es un ejemplo de una advertencia para un archivo desconocido.

  ![Notificación de bloqueo de SmartScreen de Microsoft Defender para un archivo con reputación maliciosa](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious.png)

No todos los programas desconocidos son maliciosos, y la advertencia de desconocido tiene por objeto proporcionar un contexto y una orientación a los usuarios que lo necesitan, especialmente si la advertencia es inesperada.

  ![Mantener un archivo con reputación maliciosa](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious-keep.png)

Sin embargo, los usuarios todavía pueden descargar y ejecutar la aplicación haciendo clic en **... | Seguir | Mostrar más | Seguir de todos modos**.

> [!TIP]
> **FYI para clientes empresariales.** De forma predeterminada, SmartScreen de Microsoft Defender permite a los usuarios omitir las advertencias. Debido a que esta interacción con el usuario es potencialmente riesgosa, le recomendamos que revise estas [configuraciones de directivas de grupo recomendadas.](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-available-settings#recommended-group-policy-and-mdm-settings-for-your-organization).

Verá cómo SmartScreen de Microsoft Defender responde a diferentes escenarios usando nuestro [sitio de demostración.](https://demo.smartscreen.msft.net/).

## SmartScreen de Microsoft Defender y la privacidad del usuario

SmartScreen de Microsoft Defender protege a los usuarios mientras navegan por internet mediante un sistema de control de reputación. Microsoft Edge pasa la información relevante sobre la URL o el archivo al servicio SmartScreen de Microsoft Defender para iniciar la comprobación de la reputación. La comprobación compara el sitio web o el archivo con listas dinámicas de sitios y archivos que se sabe que son peligrosos. Todas las solicitudes al servicio SmartScreen de Microsoft Defender se hacen con cifrado TLS. El servicio devuelve los resultados de la comprobación de la reputación, lo que puede llevar a que Microsoft Edge muestre una advertencia para el sitio o el archivo. Estos resultados se almacenan de forma local en el dispositivo.

El servicio SmartScreen de Microsoft Defender almacena datos sobre los controles de reputación. A medida que se identifican nuevos sitios, el servicio se añade a una base de datos dinámica de URL y archivos maliciosos conocidos. Estos datos se almacenan en servidores seguros de Microsoft y sólo se utilizan para los servicios de seguridad de Microsoft. Estos datos no se utilizarán nunca para identificar o dirigir a los usuarios de ninguna manera. Borrar la caché de navegación borra todos los datos de URL de SmartScreen de Microsoft Defender almacenados de forma local. Borrar el historial de descargas eliminará cualquier dato almacenado de forma local en SmartScreen sobre las descargas de archivos.

Para obtener más información sobre SmartScreen de Microsoft Defender y la privacidad en Microsoft Edge, lea el[artículo técnico sobre privacidad en Microsoft Edge](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#smartscreen).

## Configuración de SmartScreen de Microsoft Defender para los administradores

Los administradores pueden configurar SmartScreen de Microsoft Defender utilizando la directiva de grupo, Microsoft Intune o la configuración de administración de dispositivos móviles (MDM). Basándose en la configuración de SmartScreen de Microsoft Defender, puedes mostrar a los usuarios una página de advertencia y dejarles que continúen en el sitio o que bloqueen el sitio por completo.

### La pantalla SmartScreen de Microsoft Defender se ha configurado utilizando la directiva de grupo

Para obtener una lista completa de las directivas de SmartScreen, consulte[la configuración de SmartScreen de Microsoft Defender](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreen-settings)

### SmartScreen de Microsoft Defender configurado con MDM

Para más información, consulta lo siguiente:

- [Configuración de Windows Intune para SmartScreen de Microsoft Defender](https://docs.microsoft.com/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)
- [Configuración de la directiva de MDM](https://docs.microsoft.com/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)

## Configuración de SmartScreen de Microsoft Defender para los usuarios

SmartScreen de Microsoft Defender está activado de forma predeterminada para Microsoft Edge. Para desactivar SmartScreen de Microsoft Defender, diríjase a*edge://settings/privacy > Servicios > SmartScreen de Microsoft Defender*. Esta configuración es la misma para todos los perfiles asociados a la instalación de Microsoft Edge en un dispositivo. Esta configuración no está sincronizada entre los dispositivos. La configuración se aplica a la navegación InPrivate y al modo de invitado. Si un dispositivo se administra con directivas de grupo establecidas por una organización, esta configuración se reflejará en*edge://settings/privacy*.

> [!NOTE]
> Los usuarios pueden configurar SmartScreen de Microsoft Defender para un dispositivo individual, a menos que la directiva de grupo o MDM esté configurada para evitarlo. Para obtener más información, consulte [configurar y usar SmartScreen de Microsoft Defender en dispositivos individuales](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device).

## Preguntas frecuentes

### ¿Cómo funciona el sistema de control de reputación?

Mientras navega por la web, SmartScreen de Microsoft Defender categoriza los sitios web y las descargas como de mayor tráfico, peligrosos o desconocidos. El tráfico principal son los sitios populares que SmartScreen de Microsoft Defender ha determinado que son dignos de confianza. Si visita un sitio marcado como peligroso, SmartScreen de Microsoft Defender bloquea inmediatamente el acceso al sitio. Cuando se dirija a un sitio desconocido, SmartScreen de Microsoft Defender comprueba su reputación para determinar si debe acceder al sitio.

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: Exploración segura en Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Información general de SmartScreen de Microsoft Defender ](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview)
- [Protección contra amenazas](https://docs.microsoft.com/windows/security/threat-protection/index)
- [Proteger contra aplicaciones potencialmente no deseadas](https://docs.microsoft.com/DeployEdge/microsoft-edge-potentially-unwanted-apps)