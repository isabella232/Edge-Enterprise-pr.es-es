---
title: Configuración de privacidad empresarial de Microsoft Edge
ms.author: likravit
author: dan-wesley
manager: srugh
ms.date: 05/26/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar las opciones de privacidad empresarial de Microsoft Edge
ms.openlocfilehash: 2b7a33087ae5110c53d18b3192486d4ae62fa540
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981198"
---
# Configurar directivas de Microsoft Edge para admitir la privacidad empresarial

Microsoft se compromete a proporcionar a las empresas la información y los controles necesarios para tomar decisiones sobre la recopilación de datos en Microsoft Edge.

## Introducción

De forma predeterminada, Microsoft Edge implementado en plataformas distintas de Windows no envía datos de diagnóstico o información del sitio a Microsoft. Cuando Microsoft Edge está implementado en Windows 10, de forma predeterminada los datos de diagnóstico se envían en función de la [configuración de datos de diagnóstico de Windows](https://go.microsoft.com/fwlink/?linkid=2099569) del usuario.

Asimismo, puedes configurar cómo administra Microsoft Edge la recopilación de datos para tu organización con las siguientes directivas de grupo:

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): habilitar el uso y los informes de datos relacionados con bloqueos.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): enviar información de sitios para mejorar los servicios Microsoft.

## Configurar opciones de directiva

Antes de empezar, descarga y usa la última plantilla de directiva de Microsoft Edge (para más información, consulta [Configurar Microsoft Edge](configure-microsoft-edge.md)).

### Habilitar el uso y los informes de datos relacionados con bloqueos

Esta directiva permite los informes de datos de uso y relacionados con bloqueos acerca de Microsoft Edge para Microsoft.

Microsoft Edge recopila un conjunto de datos requeridos que son necesarios para mantener el producto actualizado, seguro y funcionando correctamente. Estos datos incluyen la información de configuración y conectividad de dispositivo básica desde Microsoft Edge sobre el consentimiento de la colección de datos actual, la versión de la aplicación y el estado de instalación acerca de la instalación de Microsoft Edge.Para desactivar la recopilación de estos datos, deshabilite la directiva.

Habilita esta directiva para enviar informes de datos de uso y relacionados con bloqueos a Microsoft. Deshabilita esta directiva para no enviar los datos a Microsoft. En ambos casos, los usuarios no pueden cambiar ni invalidar la configuración.

Cuando Microsoft Edge se ejecuta en Windows 10:

- Si esta directiva no está configurada, Microsoft Edge se establecerá de forma predeterminada a la configuración de datos de diagnóstico de Windows.
- Si esta directiva está habilitada, Microsoft Edge solo enviará datos de uso si la configuración de datos de diagnóstico de Windows está establecida en **Mejorado** o **Completo**.
- Si esta directiva está deshabilitada, Microsoft Edge no enviará datos de uso. Los datos relacionados con bloqueos se envían en función de la configuración de datos de diagnóstico de Windows. [Obtenga más información acerca de la configuración de datos de diagnóstico de Windows](https://go.microsoft.com/fwlink/?linkid=2099569).

Cuando Microsoft Edge se ejecuta en Windows 7, 8 y macOS:

- Si esta directiva no está configurada, Microsoft Edge se establecerá de forma predeterminada en la preferencia del usuario.

### Enviar información de sitios para mejorar los servicios Microsoft

Esta directiva permite enviar información acerca de los sitios web visitados en Microsoft Edge a Microsoft para mejorar los productos y servicios de Microsoft como la búsqueda.

Habilita esta directiva para enviar información acerca de los sitios web que visitas en Microsoft Edge a Microsoft. Deshabilita esta directiva para no enviar información sobre los sitios web que se visitan en Microsoft Edge a Microsoft. En ambos casos, los usuarios no pueden cambiar ni invalidar la configuración.

Cuando Microsoft Edge se ejecuta en Windows 10:

- Si esta directiva no está configurada, Microsoft Edge se establecerá de forma predeterminada a la configuración de datos de diagnóstico de Windows.
- Si esta directiva está habilitada, Microsoft Edge solo enviará información acerca de los sitios web que se visitan si la configuración de datos de diagnóstico de Windows está establecida en **Completo**.
- Si esta directiva está deshabilitada, Microsoft Edge no enviará información acerca de los sitios web visitados. Para [obtener más información acerca de la configuración de datos de diagnóstico de Windows](https://go.microsoft.com/fwlink/?linkid=2099569).

Cuando Microsoft Edge se ejecuta en Windows 7, 8 y macOS:

- Si esta directiva no está configurada, Microsoft Edge se establecerá de forma predeterminada en la preferencia del usuario.

## Detalles de implementación

Para que Windows 10 comprenda nuestra implementación con la dependencia en la configuración de datos de diagnóstico de Windows, en la siguiente tabla se describe nuestra configuración si los valores de **Habilitar el uso y los informes de datos relacionados con bloqueos** y **Enviar información de sitios para mejorar los servicios Microsoft** no estaban configurados.

| Configuración de datos de diagnóstico de Windows | Habilitar el uso y los informes de datos relacionados con bloqueos | Enviar información de sitios para mejorar los servicios Microsoft |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Seguridad                        | No enviado                                      | No enviado                                            |
| Básico                           | No enviado                                      | No enviado                                            |
| Mejorado                        | Enviado                                          | No enviado                                            |
| Completo                            | Enviado                                          | Enviado                                                |

Si las configuraciones de Windows 10 no están definidas correctamente según lo establecido en la tabla anterior, se revertirá a la configuración de colección de datos inferior.

Por ejemplo:

- Estableces la directiva "Habilitar el uso y los informes de datos relacionados con bloqueos" en **Habilitado**, pero la configuración de datos de diagnóstico de Windows se establece en **Básico**. No enviaremos datos de uso y relacionados con bloqueos.
- Estableces la opción "Enviar información de sitios para mejorar los servicios Microsoft" en **Deshabilitado**, pero la configuración de datos de diagnóstico de Windows se establece en **Completo**. No enviaremos información sobre los sitios visitados.

La implementación correcta sería establecer la directiva "Habilitar el uso y los informes de datos relacionados con bloqueos" en **Habilitado** con la configuración de datos de diagnóstico de Windows establecida en **Mejorado** o **Completo**.

## Otras opciones de directiva de privacidad

Puede que te resulten de interés las siguientes directivas de grupo relacionadas con la privacidad de los datos:

- Bloquear las cookies en determinados sitios
- Bloquear cookies de terceros
- Configurar No realizar seguimiento
- Deshabilitar el modo InPrivate

## Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Directivas de Microsoft Edge](microsoft-edge-policies.md)
- [notas del producto sobre la privacidad de Microsoft Edge](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper)
