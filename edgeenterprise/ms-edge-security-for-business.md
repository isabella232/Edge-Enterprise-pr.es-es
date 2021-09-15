---
title: Seguridad de Microsoft Edge para su empresa
ms.author: collw
author: seanongit
manager: chuckf
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Seguridad de Microsoft Edge para su empresa
ms.openlocfilehash: d16b22b63212e3f5319b0bb7df1e457e45cd6208
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11980332"
---
# <a name="microsoft-edge-security-for-your-business"></a>Seguridad de Microsoft Edge para su empresa

Microsoft Edge se basa en el proyecto de fuente abierta Chromium —el mismo proyecto en el que se basa Google Chrome—, lo que significa que tienen una base que comparte el mismo diseño y la arquitectura de seguridad bien diseñada y ampliamente probada. Hay más que contar sobre los aspectos de seguridad de Microsoft Edge. De hecho, **al usar Windows 10 para su empresa, Microsoft Edge es más seguro que Google Chrome**. Cuenta con defensas integradas y eficaces contra la suplantación de identidad (phishing) y el software malintencionado, y es compatible de forma nativa con el aislamiento de hardware en Windows 10, por lo que no se necesita ningún software adicional para lograr esta línea base segura. Asimismo, tiene aún más ventajas: cuando se empareja con la compatibilidad nativa con los servicios de seguridad y cumplimiento de Microsoft 365, Microsoft Edge ofrece funciones y características de seguridad adicionales y eficaces que contribuyen a proteger contra la pérdida de datos. Para más información, vea [Vídeo: Seguridad, compatibilidad y facilidad de administración de Microsoft Edge](microsoft-edge-video-security-compatibility-manageability.md).

Entremos en detalles: empezaremos por las **amenazas externas** y, después, pasaremos a los **riesgos internos y la protección de la información**.

## <a name="external-threat-protection"></a>Protección contra amenazas externas

### <a name="highest-rated-protection-against-phishing-and-malware"></a>La protección mejor valorada para hacer frente a la suplantación de identidad (phishing) y al software malintencionado

Integrado en Microsoft Edge, SmartScreen bloquea más intentos de [suplantación de identidad (phishing)](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWASN1) y [malware](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWANMW) que la navegación segura de Google Chrome, según un estudio independiente de NSS Labs. SmartScreen ofrece comprobaciones de reputación de los sitios y de las descargas en tiempo real mientras los usuarios trabajan en línea. Además, forma parte de [Microsoft Intelligent Security Graph](https://www.microsoft.com/microsoft-365/windows/intelligent-security), que obtiene información y señales generadas en la amplia red global de Microsoft de activos, investigadores y asociados. Microsoft Edge ejecuta comprobaciones de listas dinámicas y basadas en la nube de descargas y sitios peligrosos, lo que ayuda a detectar y a bloquear incluso amenazas efímeras que desaparecen rápidamente.  

[SmartScreen de Microsoft Edge](//DeployEdge/microsoft-edge-security-smartscreen) bloqueó el 95.5 % de los intentos de phishing durante la prueba de [Protección de phishing de NSS Labs](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWASN1) y el 98.5 % de los intentos de malware durante la prueba de [Protección de malware de NSS Labs](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWANMW), frente al 86.9 % y el 86.0 %, respectivamente, que obtuvo la navegación segura de Google Chrome.

### <a name="the-only-browser-on-windows-10-that-natively-supports-hardware-isolation"></a>El único explorador en Windows 10 que admite de forma nativa el aislamiento de hardware

Microsoft Edge es el único explorador en Windows 10 que admite de forma nativa funciones de aislamiento de hardware. Como parte de Windows 10 Pro o Enterprise, la Protección de aplicaciones de Microsoft defender (Protección de aplicaciones) ejecuta los sitios que no sean de confianza en un kernel aislado del dispositivo local y de las redes internas. Los sitios que no son de confianza se ejecutan en un "contenedor", de modo que, cuando tenga lugar un ataque, quede en un espacio aislado del resto de la red corporativa. Para más información, consulte [compatibilidad de Microsoft Edge con la Protección de aplicaciones](./microsoft-edge-security-windows-defender-application-guard.md).

Para Chrome, se encuentra disponible una extensión para poder emplear el aislamiento de hardware de Windows 10: la extensión MDAG. Esta extensión inicia Microsoft Edge para poder aprovechar el aislamiento de nivel de kernel de la Protección de aplicaciones. Además, para lograr un aislamiento de nivel de kernel similar en una solución que emplee Google Chrome exclusivamente, se necesita software de aislamiento de terceros.

> [!NOTE]
> La Protección de aplicaciones está disponible en Windows 10, 1809 y posteriores. La Protección de aplicaciones no está disponible en las ediciones de Windows 10 Home.

## <a name="internal-risks-and-information-protection"></a>Protección de la información y contra riesgos internos

### <a name="native-support-for-microsoft-365-security-without-additional-software"></a>Soporte nativo para la seguridad de Microsoft 365 sin software adicional

Además de proteger contra amenazas externas, los administradores de TI también deben proteger frente a riesgos internos. La protección —sólida y a escala— de datos corporativos confidenciales es una de las máximas prioridades de los administradores de TI, sobre todo teniendo en cuenta que el personal se ha descentralizado. Microsoft Edge es el único explorador con compatibilidad nativa para el Acceso condicional de Azure AD, para Windows Information Protection y para la nueva prevención de pérdida de datos (DLP) de Microsoft Endpoint sin necesidad de software adicional.

**Microsoft Edge es el único explorador que admite de forma nativa el Acceso condicional**. La [compatibilidad de Microsoft Edge con el acceso condicional](ms-edge-security-conditional-access.md) facilita a las organizaciones el uso de señales de identidad como parte de sus decisiones relacionadas con el control de acceso. El [Acceso condicional](/azure/active-directory/conditional-access/overview) es la herramienta que utiliza Azure Active Directory para reunir señales, tomar decisiones y aplicar directivas de la organización. El Acceso condicional constituye la base del nuevo plano de control controlado por identidad. Para obtener compatibilidad con el Acceso condicional en Google Chrome, se requiere un complemento adicional.

> [!NOTE]
> Para el Acceso condicional de Azure AD, se requiere una suscripción a Microsoft 365 E3 o superior.

**Microsoft Edge es el único explorador en el que se admite de forma nativa Windows Information Protection (WIP)**, que proporciona protección a los datos corporativos para contribuir a evitar que los usuarios pierdan datos de forma accidental en dispositivos con Windows 10. La [compatibilidad de Microsoft Edge para WIP](./microsoft-edge-security-windows-information-protection.md) puede configurarse para permitir exclusivamente a las aplicaciones exigidas por TI acceder a los datos corporativos. Asimismo, proporciona una experiencia de usuario perfecta y realiza controles de pérdida: protege el portapapeles, cifra los archivos al descargarlos y evita la carga de archivos en ubicaciones de la nube o recursos compartidos de red no autorizados. WIP emplea una configuración basada en el perímetro, en la que los administradores de TI definen el límite corporativo y todos los datos dentro de dicho límite se consideran corporativos. Google Chrome no está optimizado para el uso de WIP con controles de pérdida.

> [!NOTE]
> La configuración de Windows Information Protection (WIP) requiere la licencia de Microsoft Intune o del Administrador de configuración de Microsoft Endpoint, o bien el uso de una solución de administración de dispositivos móviles (MDM) de terceros, que puede tener requisitos de licencia adicionales.

La **prevención de pérdida de datos de Microsoft Endpoint (DLP de Endpoint) solo se admite de forma nativa en Microsoft Edge**. DLP de Endpoint se integra con el Centro de seguridad de Microsoft y amplía la protección de la información a Microsoft Edge para ayudar a alertar a los usuarios de la actividad que no cumpla con la normativa y evitar la pérdida de datos cuando los usuarios trabajen en línea. Detecta y etiqueta los datos confidenciales dentro de la empresa que coincidan con los criterios definidos por el administrador, como archivos que contengan números de tarjeta de crédito o Id. gubernamental (por ejemplo, números de la seguridad social), información financiera, etc. Las directivas de Microsoft Information Protection se pueden implementar en DLP de Microsoft Endpoint sin que sea necesaria una reconfiguración adicional, incluidos los identificadores de contenido confidencial y las directivas que los administradores de TI ya hayan personalizado. Así, los administradores de TI pueden realizar una implementación fluida de la protección de la información.

Para obtener más información sobre los requisitos previos de DLP de Endpoint y sobre cómo realizar la configuración, vaya a [Introducción a la prevención de pérdida de datos de Endpoint](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide).

> [!NOTE]
> Se requiere una suscripción a Microsoft 365 E5 o a Cumplimiento de Microsoft 365 E5 para obtener la prevención de pérdida de datos de Microsoft Endpoint.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: Seguridad, compatibilidad y capacidad de administración de Microsoft Edge](microsoft-edge-video-security-compatibility-manageability.md)