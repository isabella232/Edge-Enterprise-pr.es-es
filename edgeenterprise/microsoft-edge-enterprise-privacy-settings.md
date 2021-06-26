---
title: Configuración de privacidad empresarial de Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 09/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar las opciones de privacidad empresarial de Microsoft Edge
ms.openlocfilehash: 9af3ce14b9ee717d4c64fa3b920e8c63224613e6
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617780"
---
# <a name="configure-microsoft-edge-policies-to-support-enterprise-privacy"></a>Configurar directivas de Microsoft Edge para admitir la privacidad empresarial

Microsoft se compromete a proporcionar a las empresas la información y los controles necesarios para tomar decisiones sobre la recopilación de datos en Microsoft Edge.

## <a name="overview"></a>Introducción

Cuando Microsoft Edge está implementado en Windows 10, de forma predeterminada los datos de diagnóstico se envían en función de la [configuración de datos de diagnóstico de Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) del usuario.

Cuando Microsoft Edge está implementado en plataformas que no son Windows, los datos de diagnóstico se recopilan según la configuración de las siguientes directivas de grupo:

- (OBSOLETO) [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled): Habilitar el uso y los informes de datos relacionados con bloqueos. Esta directiva quedará obsoleta en la versión 89 de Microsoft Edge.
- (OBSOLETO) [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices): Enviar información de sitios para mejorar los servicios Microsoft. Esta directiva quedará obsoleta en la versión 89 de Microsoft Edge.

Las directivas obsoletas mencionadas antes se reemplazarán por [Permitir telemetría](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) en Windows 10 y la directiva [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) para las demás plataformas.  

## <a name="configure-policy-settings"></a>Configurar opciones de directiva

Antes de empezar, descarga y usa la última plantilla de directiva de Microsoft Edge (para más información, consulta [Configurar Microsoft Edge](configure-microsoft-edge.md)).

### <a name="send-required-and-optional-diagnostic-data-about-browser-usage"></a>Enviar datos de diagnóstico necesarios y opcionales sobre el uso del explorador

Si la directiva [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) está configurada, tiene prioridad sobre [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) y [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).

#### <a name="required-and-optional-diagnostic-data"></a>Datos de diagnóstico necesarios y opcionales

Los datos de diagnóstico necesarios se recopilan para proteger, actualizar y mejorar el rendimiento de Microsoft Edge.

Los datos de diagnóstico opcionales incluyen datos sobre cómo se usa el explorador, los sitios web que visita y los informes de bloqueos para ayudar a, de la mejor manera posible, proteger, actualizar y mejorar el rendimiento de Microsoft Edge y otros productos y servicios de Microsoft para todos los usuarios.

> [!NOTE]
> Esta directiva no es compatible con dispositivos Windows 10. Para controlar la colección de datos en Windows 10, los administradores de TI tienen que usar la directiva de grupo de datos de diagnóstico de Windows. Esta directiva será la de **Permitir telemetría** o la de **Permitir datos de diagnóstico**, en función de la versión de Windows. Más información sobre la [colección de datos de diagnóstico de Windows 10](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Use una de las opciones siguientes para configurar **DiagnosticData**:

- Desactivado (no recomendado) (0) desactiva la recopilación de datos de diagnóstico necesarios y opcionales. 
- Datos necesarios (1) envía los datos de diagnóstico necesarios y desactiva la recopilación de datos de diagnóstico opcionales. Microsoft Edge enviará los datos de diagnóstico necesarios para que Microsoft Edge esté protegido y actualizado, y para que funcione como se espera. 
- Datos opcionales (2) envía los datos de diagnóstico opcionales, que incluyen datos sobre el uso del explorador, los sitios web que visita y los informes de bloqueos para ayudar a, de la mejor manera posible, proteger, actualizar y mejorar el rendimiento de Microsoft Edge y otros productos y servicios de Microsoft para todos los usuarios.

En Windows 7, Windows 8 y 8.1, y macOS, esta directiva controla el envío de datos necesarios y opcionales a Microsoft.

Si no configura esta directiva o la deshabilita, Microsoft Edge se ajustará de forma predeterminada a las preferencias del usuario.

### <a name="deprecated-enable-usage-and-crash-related-data-reporting"></a>(OBSOLETO) Habilitar el uso y los informes de datos relacionados con bloqueos

La directiva **MetricsReportingEnabled** permite los informes de datos de uso y relacionados con bloqueos acerca de Microsoft Edge para Microsoft.

Microsoft Edge recopila un conjunto de datos necesarios que son necesarios para mantener el producto actualizado, seguro y funcionando de manera adecuada. Estos datos incluyen la información de configuración y conectividad de dispositivo básica desde Microsoft Edge sobre el consentimiento de la colección de datos actual, la versión de la aplicación y el estado de instalación acerca de la instalación de Microsoft Edge.Para desactivar la recopilación de estos datos, deshabilite la directiva.

Habilita esta directiva para enviar informes de datos de uso y relacionados con bloqueos a Microsoft. Deshabilita esta directiva para no enviar los datos a Microsoft. En ambos casos, los usuarios no pueden cambiar ni invalidar la configuración.

Cuando Microsoft Edge se ejecuta en Windows 10:

- Si esta directiva no está configurada, Microsoft Edge se establecerá de forma predeterminada a la configuración de datos de diagnóstico de Windows.
- Si esta directiva está habilitada, Microsoft Edge solo enviará datos de uso si la configuración de datos de diagnóstico de Windows está establecida en **Mejorado** o **Completo**.
  - Si esta directiva está habilitada, Microsoft Edge solo enviará datos de uso si [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) también está habilitada.
- Si esta directiva está deshabilitada, Microsoft Edge no enviará datos de uso. Los datos relacionados con bloqueos se envían en función de la configuración de datos de diagnóstico de Windows. [Obtenga más información acerca de la configuración de datos de diagnóstico de Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Cuando Microsoft Edge se ejecuta en Windows 7, 8 y macOS:

- Si esta directiva no está configurada, Microsoft Edge se establece, de forma predeterminada, en la preferencia del usuario.
-  Si esta directiva está habilitada, Microsoft Edge solo enviará datos de uso si [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) también está habilitada.

### <a name="deprecated-send-site-information-to-improve-microsoft-services"></a>(OBSOLETO) Enviar información de sitios para mejorar los servicios Microsoft

La directiva **SendSiteInformationToImproveServices** permite enviar información acerca de los sitios web visitados en Microsoft Edge a Microsoft para mejorar los productos y servicios de Microsoft como la búsqueda.

Habilita esta directiva para enviar información acerca de los sitios web que visitas en Microsoft Edge a Microsoft. Deshabilita esta directiva para no enviar información sobre los sitios web que se visitan en Microsoft Edge a Microsoft. En ambos casos, los usuarios no pueden cambiar ni invalidar la configuración.

Cuando Microsoft Edge se ejecuta en Windows 10:

- Si esta directiva no está configurada, Microsoft Edge se establecerá de forma predeterminada a la configuración de datos de diagnóstico de Windows.
- Si esta directiva está habilitada, Microsoft Edge solo enviará información acerca de los sitios web que se visitan si la configuración de datos de diagnóstico de Windows está establecida en **Completo**.
  - Si esta directiva está habilitada, Microsoft Edge solo enviará datos de uso si [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) también está habilitada. 
- Si esta directiva está deshabilitada, Microsoft Edge no enviará información acerca de los sitios web visitados. Para [obtener más información acerca de la configuración de datos de diagnóstico de Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Cuando Microsoft Edge se ejecuta en Windows 7, 8 y macOS:

- Si esta directiva está habilitada, Microsoft Edge solo enviará datos de uso si [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) también está habilitada.
- Si esta directiva no está configurada, Microsoft Edge se establece, de forma predeterminada, en la preferencia del usuario.

## <a name="implementation-details"></a>Detalles de implementación

Para dispositivos sin Windows 10: 
- Si la directiva [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) está configurada, tiene prioridad sobre [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) y [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices). 
- Si la directiva [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) no está configurada, Microsoft responde a [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) y [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).  

Para que Windows 10 comprenda nuestra implementación con la dependencia en la configuración de datos de diagnóstico de Windows, en la siguiente tabla, se indica si los datos de diagnóstico  **Necesarios** y **Opcionales** se envían a Microsoft.

| Configuración de datos de diagnóstico de Windows | Datos de diagnóstico necesarios  | Datos de diagnóstico opcionales |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Seguridad                        | No enviado                                      | No enviado                                            |
| Básico                           | Enviado                                      | No enviado                                            |
| Mejorado                        | Enviado                                          | No enviado                                            |
| Completo                            | Enviado                                          | Enviado                                                |

> [!IMPORTANT]
> Microsoft Edge admite **MetricsReportingEnabled** y **SendSiteInfoToImproveServices** para las versiones de Microsoft Edge 86 a 88, ambas incluidas. En la versión 89 de Microsoft Edge, **MetricsReportingEnabled** y **SendSiteInfoToImproveServices** ya no se admitirán; y se mostrarán, de forma predeterminada, **DiagnosticData** en plataformas que no sean Windows 10, o la directiva **Permitir telemetría** en Windows 10.

## <a name="additional-privacy-policy-options"></a>Otras opciones de directiva de privacidad

Puede que te resulten de interés las siguientes directivas de grupo relacionadas con la privacidad de los datos:

- Bloquear las cookies en determinados sitios
- Bloquear cookies de terceros
- Configurar No realizar seguimiento
- Deshabilitar el modo InPrivate

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Directivas de Microsoft Edge](microsoft-edge-policies.md)
- [notas del producto sobre la privacidad de Microsoft Edge](/microsoft-edge/privacy-whitepaper)