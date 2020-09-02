---
title: Lector de PDF en Microsoft Edge
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 08/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Obtenga más información sobre el lector de PDF en Microsoft Edge.
ms.openlocfilehash: c189bc08d4af0c9d5c4d9c573e0b5b7ef32a7fb3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981213"
---
# Lector de PDF en Microsoft Edge

Los archivos PDF constituyen una parte importante de nuestra vida diaria. Se incluyen en forma de contratos y acuerdos, boletines, formularios, artículos de investigación, currículos, etc. Estos archivos destacan la necesidad de un lector de PDF fiable, seguro y de gran capacidad que pueda ser adoptado por las empresas.

Microsoft Edge incorpora un lector de PDF integrado que le permite abrir archivos PDF locales, archivos PDF en línea o archivos PDF incrustados en páginas Web. Puede anotar estos archivos con entradas de lápiz y resaltado. Este lector de PDF ofrece a los usuarios una única aplicación para satisfacer las necesidades de documentos de páginas web y de PDF. El lector PDF de Microsoft Edge es una aplicación segura y fiable que funciona en todas las plataformas de escritorio de Windows y macOS.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## Requisitos previos, soporte técnico y restricciones

En la tabla siguiente se muestran los canales y versiones de Microsoft Edge compatibles con la característica lector de PDF.

| Característica | Versión de canal estable |
|---------|------------------------|
| Ver e imprimir archivos PDF integrados, en línea y locales | 79.0.309.71                |
| Relleno básico de formularios<br>(Los formularios de JavaScript no son compatibles) | 79.0.309.71           |
| Entrada manuscrita  | 80.0.361.48            |
| Personalización de entrada de lápiz | 83.0.478.54.  |
| Resaltar  | 81.0.416.53         |
| Lectura en voz alta | Se promueve actualmente en canales de [Insider de Microsoft Edge](https://www.microsoftedgeinsider.com/) |
| Ver archivos protegidos MIP | Soporte técnico de Windows en 80.0.361.48<br>Soporte técnico para Mac en 81.0.416.53 |
|  Ver archivos protegidos por IRM  | 83.0.478.37            |

### Restricciones

Tenga en cuenta las siguientes restricciones del lector de PDF actual:

-  La arquitectura de formularios XML (XFA) es un formato heredado de formularios que no es compatible con Microsoft Edge.
-  La documentación relacionada con los escenarios de accesibilidad que actualmente no son compatibles se puede encontrar en el blog [Informes de conformidad de accesibilidad de Microsoft](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/).

## Características

### Entrada manuscrita

Las entradas manuscritas en archivos PDF son útiles para tomar notas rápidas para facilitar referencias, firmar o rellenar formularios PDF. Esta función ya está disponible en Microsoft Edge. Además de los archivos PDF de entrada manuscrita cuando es necesario, puede usar el color y el ancho del trazo para ofrecer atención a las distintas partes del archivo PDF. La siguiente captura de pantalla muestra cómo un usuario puede Agregar entradas manuscritas a una página PDF.

<!-- SCREENSHOT -->
![Agregar la página de entrada manuscrita al pdf](media/microsoft-edge-pdf/pdf-reader-inking.png)

### Resaltar

Lector de PDF en Microsoft Edge tiene la compatibilidad para agregar y editar los puntos destacados. Para crear un resaltado, el usuario solo tiene que seleccionar el texto, haga clic con el botón derecho en él y seleccione iluminado en el menú y elija el color que desee. La siguiente captura de pantalla muestra las opciones de resaltado disponibles.

![Use la opción resaltar del lector de PDF](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### Lectura en voz alta

Leer en voz alta para PDF aumenta la comodidad de escuchar el contenido de PDF mientras lleva a cabo otras tareas que pueden ser importantes para los usuarios. También ayuda a que los estudiantes se centren en el contenido, lo que facilita mucho más el aprendizaje. La siguiente captura de pantalla muestra un ejemplo de Lectura en voz alta. El resaltado muestra el texto que se está leyendo actualmente.

![Use la opción resaltar del lector de PDF](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### Documentos PDF protegidos

[ Microsoft Information Protection (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) permite que los usuarios colaboren con otras personas con seguridad, a la vez que se respetan las directivas de cumplimiento normativo de la organización. Una vez que un archivo está protegido, las acciones que los usuarios pueden llevar a cabo están determinadas por los permisos que tienen asignados.

Estos archivos pueden abrirse directamente en el explorador, sin necesidad de descargar ningún otro software ni de instalar ningún complemento. Esto integra la seguridad proporcionada por el MIP directamente en el explorador, proporcionando un flujo de trabajo perfecto.

<!-- SCREENSHOT -->
![Documentos PDF protegidos.](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

Además de los archivos protegidos por el MIP, los archivos PDF de las bibliotecas SharePoint protegidas por la [Information Rights Management (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide) también pueden abrirse de forma nativa en el explorador.

Con Microsoft Edge, los usuarios pueden ver los archivos protegidos MIP guardados localmente o en la nube. Si se guarda localmente, el archivo puede abrirse directamente en el explorador. Si el archivo se abre desde un servicio en la nube como SharePoint, es posible que el usuario tenga que utilizar la opción "Abrir en el explorador".

Si el perfil con el que el usuario ha iniciado sesión en Microsoft Edge tiene al menos permisos de visualización del archivo, este se abrirá en Microsoft Edge.

<!-- SCREENSHOT -->
![Preguntar si se guarda la página PDF de SharePoint protegida por MIP](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

## Accesibilidad

El lector de PDF es compatible con la accesibilidad de teclado, el modo de contraste alto y la compatibilidad con lectores de pantalla en dispositivos Windows y Mac OS.

### Accesibilidad de teclado

Los usuarios pueden usar el teclado para desplazarse por las distintas partes del documento con las que un usuario puede interactuar, como campos de formulario y resaltados.

<!-- SCREENSHOT -->

### Modo de contraste alto

El lector de PDF usará la configuración definida en el nivel de sistema operativo para representar el contenido de PDF en el modo de contraste alto.

<!-- SCREENSHOT -->
<!--![High contrast mode for pdf file](media/microsoft-edge-pdf/pdf-reader-high-contrast.png)-->

### Compatibilidad con lector de pantalla

Los usuarios pueden navegar y leer archivos PDF usando lectores de pantalla en computadoras Windows y Mac. <!--The next screenshot shows the toolbar that users can use for audio settings when they're using the Read Aloud option in PDF reader. -->

<!-- SCREENSHOT -->
<!--
![Screen reader toolbar](media/microsoft-edge-pdf/pdf-reader-read-aloud.png) -->

## Seguridad y confiabilidad

La seguridad se encuentra entre los principios más importantes para cualquier organización. La seguridad del lector de PDF es una parte integral del diseño de seguridad de Microsoft Edge. Dos de las características de seguridad más importantes desde el punto de vista del lector de PDF, dos características de seguridad importantes son el aislamiento de procesos y la protección de Protección de aplicaciones de Microsoft Defender (protección de aplicaciones).

- Aislado del proceso. Los archivos PDF abiertos desde diferentes sitios web están completamente aislados del proceso. El explorador no tiene que comunicarse con ningún sitio web o archivos PDF abiertos desde otro origen. La exploración de PDF está protegida frente a cualquier ataque que planee usar archivos PDF comprometidos como superficie de ataque.

- Protección de aplicaciones. Con Protección de aplicaciones, los administradores pueden configurar una lista de sitios de confianza para su organización. Si los usuarios abren otros sitios, se abren en una ventana de Protección de la aplicación independiente que se ejecuta en su propio contenedor. El contenedor ayuda a proteger la red corporativa y cualquier dato del ordenador del usuario para que no se vea comprometido.<br><br>
Esta protección también se aplica a todos los archivos PDF en línea que se vean. Además, todos los archivos PDF que se descargan desde una ventana de Protección de aplicaciones se almacenan y, cuando es necesario, se vuelven a abrir en el contenedor. Esto ayuda a mantener la seguridad de su entorno, no solo cuando se descarga el archivo, sino durante todo su ciclo de vida. Para obtener más información, vea [Protección de aplicaciones](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).

### Confiabilidad

Debido a que Microsoft Edge está basado en Chromium, los usuarios pueden esperar el mismo nivel de fiabilidad que están acostumbrados a ver en Google Chrome.

## Implementación y actualización del lector de PDF

Se implementará el lector de PDF y se actualizará con el resto del explorador Microsoft Edge. Para más información sobre la implementación de Microsoft Edge, vea el vídeo [Implementar Microsoft Edge en cientos o miles de dispositivos](microsoft-edge-video-deploy.md). También puede encontrar más información sobre la implementación en la página de aterrizaje de [Documentación de Microsoft Edge](https://docs.microsoft.com/DeployEdge/).

> [!TIP]
> Puede hacer de Microsoft Edge el lector de PDF predeterminado de su organización. Para ello, [siga estos pasos](https://docs.microsoft.com/deployedge/edge-default-browser).

## Plan de desarrollo y comentarios

La hoja de ruta para el lector de PDF en Microsoft Edge se encuentra disponible [aquí](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667).

Buscamos constantemente su opinión sobre las características que le parecen importantes. No dude en enviarnos sus comentarios a través de [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/) y en [Foro de Insider de Microsoft Edge](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider).

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)