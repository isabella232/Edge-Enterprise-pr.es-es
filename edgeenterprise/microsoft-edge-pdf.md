---
title: Lector de PDF en Microsoft Edge
ms.author: adigan
author: AndreaLBarr
manager: balajek
ms.date: 07/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Obtenga más información sobre el lector de PDF en Microsoft Edge.
ms.openlocfilehash: e8cf690f818e0fa103aa4f17154d9f95431287b5
ms.sourcegitcommit: 9088e839e82d80c72460586e9af0610c6ca71b83
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2021
ms.locfileid: "11675987"
---
# <a name="pdf-reader-in-microsoft-edge"></a>Lector de PDF en Microsoft Edge

Los archivos PDF forman una gran parte de nuestra vida diaria. Se incluyen en forma de contratos y acuerdos, boletines, formularios, artículos de investigación, currículos, etc. Estos archivos destacan la necesidad de un lector de PDF fiable, seguro y de gran capacidad que pueda ser adoptado por las empresas.

Microsoft Edge incorpora un lector de PDF integrado que le permite abrir archivos PDF locales, archivos PDF en línea o archivos PDF incrustados en páginas Web. Puede anotar estos archivos con entradas de lápiz y resaltado. Este lector de PDF ofrece a los usuarios una única aplicación para satisfacer las necesidades de documentos de páginas web y de PDF. El lector PDF de Microsoft Edge es una aplicación segura y fiable que funciona en todas las plataformas de escritorio de Windows y macOS.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="prerequisites-support-and-constraints"></a>Requisitos previos, soporte técnico y restricciones

En la tabla siguiente se muestran los canales y versiones de Microsoft Edge compatibles con la característica lector de PDF.

| Característica | Versión de canal estable |
|---------|------------------------|
| Ver e imprimir archivos PDF integrados, en línea y locales | 79.0.309.71                |
| Relleno básico de formularios<br>(Los formularios de JavaScript no son compatibles) | 79.0.309.71           |
|Tabla de contenido| 86.0.622.38 |
| Vista de página | 88.0.705.50 |
| Exploración del modo de cotejo |87.0.664.41 |
| Entrada manuscrita  | 80.0.361.48            |
| Personalización de entrada de lápiz | 83.0.478.54.  |
| Resaltar  | 81.0.416.53         |
| Notas de texto | 88.0.705.50 |
| Leer en voz alta | 84.0.522.63  |
| Ver Microsoft Information Protection (MIP) protegidos en el mismo inquilino empresarial | Soporte técnico de Windows en 80.0.361.48<br>Soporte técnico para Mac en 81.0.416.53 |
| Ver Microsoft Information Protection (MIP) protegidos entre inquilinos empresariales | 91.0.864.37  |
|  Ver archivos protegidos de Information Rights Management (IRM)  | 83.0.478.37            |


### <a name="constraints"></a>Restricciones

Tenga en cuenta las siguientes restricciones del lector de PDF actual:

-  La arquitectura de formularios XML (XFA) es un formato heredado de formularios que no es compatible con Microsoft Edge.
-  La documentación relacionada con los escenarios de accesibilidad que actualmente no son compatibles se puede encontrar en el blog [Informes de conformidad de accesibilidad de Microsoft](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/).

## <a name="features"></a>Características

El lector de PDF, integrado en Microsoft Edge, incluye las características básicas de lectura y navegación, como Zoom, Girar, Ajustar a página/ancho, saltar a la página y buscar, entre otras. Se puede acceder a ellos a través de una barra de herramientas anclada en la parte superior del contenido PDF. En esta sección se proporciona información general sobre algunas funciones importantes. La siguiente captura de pantalla muestra la barra de herramientas del lector de PDF.

![Barra de herramientas lector de PDF](media/microsoft-edge-pdf/pdf-reader-toolbar.png)

### <a name="table-of-contents"></a>Tabla de contenido

La tabla de contenido permite a los usuarios navegar fácilmente por documentos PDF que tienen una tabla de contenido. Cuando un usuario hace clic en el icono Tabla de contenido, se muestra un panel de navegación que muestra una lista de las secciones y subsecciones etiquetadas en el documento PDF. A continuación, el usuario puede hacer clic en cualquiera de las etiquetas del panel para navegar a esa sección del documento. El panel permanece abierto durante el tiempo que sea necesario y se puede cerrar cuando el usuario desea volver a leer el documento. La siguiente captura de pantalla muestra el panel de navegación de un documento abierto.

![Navegación del lector de PDF con tabla de contenido](media/microsoft-edge-pdf/pdf-reader-toc.png)

### <a name="page-view"></a>Vista de página

Microsoft Edge admite diferentes vistas para documentos PDF en nuestros canales Dev y Canary. Los usuarios pueden cambiar el diseño de un documento de una vista de página única a dos páginas que se muestran en paralelo. Para cambiar la forma en que se está visualizando el documento PDF, los usuarios pueden hacer clic en el botón Vista de página de la barra de herramientas de PDF y, a continuación, elegir cualquiera de las vistas que quieran usar. La vista de dos páginas se muestra en la siguiente captura de pantalla.

![Lector de PDF con dos vistas de página del documento.](media/microsoft-edge-pdf/pdf-reader-page-view.png)

### <a name="caret-mode-browsing"></a>Exploración del modo de cotejo

La exploración de modo cotejo está disponible para los archivos PDF abiertos en Microsoft Edge, lo que significa que los usuarios pueden interactuar con archivos PDF con el teclado. Si un usuario presiona la tecla F7 en cualquier parte del explorador, se le preguntará si se debe desactivar la exploración de la ventana. Si está habilitada, la exploración de la característica de cotejo se encuentra disponible para cualquier contenido abierto en el explorador, ya sean archivos PDF o páginas web. Cuando un usuario presiona F7 de nuevo, se desactivará la exploración de modo cotejo. Cuando la exploración modo cotejo está activa y el foco está en el contenido, los usuarios verán un cursor parpadeante en el archivo PDF. El cotejo también se puede usar para desplazarse por el archivo o para seleccionar texto presionando Mayús mientras mueve el cursor. Esta capacidad permite a los usuarios crear fácilmente elementos como resaltados o interactuar con elementos como vínculos, campos de formulario con el teclado. La siguiente captura de pantalla muestra el menú emergente para activar la exploración en modo de cotejo.

![Menú lector de PDF para la exploración del modo cotejo](media/microsoft-edge-pdf/pdf-reader-caret-mode.png)

### <a name="inking"></a>Entrada manuscrita

Las entradas manuscritas en archivos PDF son útiles para tomar notas rápidas para facilitar referencias, firmar o rellenar formularios PDF. Esta función ya está disponible en Microsoft Edge. Además de los archivos PDF de entrada manuscrita cuando es necesario, puede usar el color y el ancho del trazo para ofrecer atención a las distintas partes del archivo PDF. La siguiente captura de pantalla muestra cómo un usuario puede Agregar entradas manuscritas a una página PDF.

![Agregar la página de entrada manuscrita al pdf](media/microsoft-edge-pdf/pdf-reader-inking.png)

### <a name="highlight"></a>Resaltar

Lector de PDF en Microsoft Edge tiene la compatibilidad para agregar y editar los puntos destacados. Para crear un resaltado, el usuario solo tiene que seleccionar el texto, haga clic con el botón derecho en él y seleccione iluminado en el menú y elija el color que desee. Los resaltados también se pueden crear con un lápiz o un teclado. La siguiente captura de pantalla muestra las opciones de resaltado disponibles.

![Use la opción resaltar del lector de PDF](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### <a name="text-notes"></a>Notas de texto

Al leer un archivo PDF, las notas de texto se pueden agregar al texto del archivo para anotar ideas para facilitar la referencia más adelante.

Los usuarios pueden agregar una nota seleccionando el texto para el que desean agregar una nota e invocando el menú contextual con el botón secundario. Si selecciona la opción **Agregar comentario** en el menú, se abrirá un cuadro de texto donde los usuarios podrán agregar sus comentarios. Pueden escribir el comentario y, a continuación, hacer clic en la marca de verificación para guardar el comentario.

Después de agregar una nota, se resaltará el texto seleccionado y aparecerá un icono de comentario para indicar el comentario. Los usuarios pueden pasar el puntero sobre ese icono para obtener una vista previa del comentario o hacer clic en él para abrir y editar la nota.

La siguiente captura de pantalla muestra una nota que se agrega al texto resaltado.

![Lector de PDF agrega nota de texto al documento.](media/microsoft-edge-pdf/pdf-reader-text-note.png)

### <a name="read-aloud"></a>Leer en voz alta

Leer en voz alta para PDF agrega la comodidad de escuchar contenido PDF mientras se llevan a cabo otras tareas que pueden ser importantes para los usuarios. También ayuda a que los estudiantes se centren en el contenido, lo que facilita mucho más el aprendizaje. La siguiente captura de pantalla muestra un ejemplo de lectura en voz alta. El resaltado muestra el texto que se está leyendo actualmente.

![Usar la opción de resaltado para Leer en voz alta en el lector de PDF](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### <a name="protected-pdfs"></a>Documentos PDF protegidos

[ Microsoft Information Protection (MIP)](/microsoft-365/compliance/protect-information?preserve-view=true&view=o365-worldwide) permite que los usuarios colaboren con otras personas con seguridad, a la vez que se respetan las directivas de cumplimiento normativo de la organización. Una vez que un archivo está protegido, las acciones que los usuarios pueden llevar a cabo están determinadas por los permisos que tienen asignados.

> [!IMPORTANT]
> Se requiere una licencia para MIP. Para obtener más información, vea esta [guía de licencias de Microsoft 365.](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection)

Estos archivos pueden abrirse directamente en el explorador, sin necesidad de descargar ningún otro software ni de instalar ningún complemento. Esta funcionalidad integra la seguridad proporcionada por MIP directamente en el explorador, lo que proporciona un flujo de trabajo sin problemas.
Puede ver los archivos protegidos de MIP entre inquilinos empresariales. Actualmente, no se admite la visualización de archivos con identidades de consumidor.

![Documentos PDF protegidos.](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

Además de los archivos protegidos por el MIP, los archivos PDF de las bibliotecas SharePoint protegidas por la [Information Rights Management (IRM)](/microsoft-365/compliance/set-up-irm-in-sp-admin-center?preserve-view=true&view=o365-worldwide) también pueden abrirse de forma nativa en el explorador.

Con Microsoft Edge, los usuarios pueden ver los archivos protegidos MIP guardados localmente o en la nube. Si se guarda localmente, el archivo puede abrirse directamente en el explorador. Si el archivo se abre desde un servicio en la nube como SharePoint, es posible que el usuario tenga que utilizar la opción "Abrir en el explorador".

Si el perfil con el que el usuario ha iniciado sesión en Microsoft Edge tiene al menos permisos de visualización del archivo, este se abrirá en Microsoft Edge.

![Preguntar si se guarda la página PDF de SharePoint protegida por MIP](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

### <a name="view-and-validate-certificate-based-digital-signatures"></a>Ver y validar firmas digitales basadas en certificados

En este mundo digital, es importante establecer la autenticidad y la propiedad del contenido del documento. Las firmas digitales basadas en certificados se usan habitualmente en documentos PDF para garantizar que el contenido del documento es el mismo que el autor quería que era y que no se ha cambiado. Con Microsoft Edge, puede ver y validar firmas digitales de certificado en archivos PDF.

Estamos trabajando activamente para mejorar el soporte para abordar más escenarios y esperamos recibir comentarios sobre el mismo.

## <a name="accessibility"></a>Accesibilidad

El lector de PDF es compatible con la accesibilidad de teclado, el modo de contraste alto y la compatibilidad con lectores de pantalla en dispositivos Windows y Mac OS.

### <a name="keyboard-accessibility"></a>Accesibilidad de teclado

Los usuarios pueden usar el teclado para desplazarse por las distintas partes del documento con las que un usuario puede interactuar, como campos de formulario y resaltados. Los usuarios también pueden usar el modo de cotejo para navegar e interactuar con los archivos PDF con el teclado.

### <a name="high-contrast-mode"></a>Modo de contraste alto

El lector de PDF usará la configuración definida en el nivel de sistema operativo para representar el contenido de PDF en el modo de contraste alto.

### <a name="screen-reader-support"></a>Compatibilidad con lector de pantalla

Los usuarios pueden navegar y leer archivos PDF usando lectores de pantalla en computadoras Windows y Mac.

## <a name="security-and-reliability"></a>Seguridad y confiabilidad

La seguridad se encuentra entre los principios más importantes para cualquier organización. La seguridad del lector de PDF es una parte integral del diseño de seguridad de Microsoft Edge. Dos de las características de seguridad más importantes desde el punto de vista del lector de PDF, dos características de seguridad importantes son el aislamiento de procesos y la protección de Protección de aplicaciones de Microsoft Defender (protección de aplicaciones).

- Aislado del proceso. Los archivos PDF abiertos desde diferentes sitios web están completamente aislados del proceso. El explorador no tiene que comunicarse con ningún sitio web o archivos PDF abiertos desde otro origen. La exploración de PDF está protegida frente a cualquier ataque que planee usar archivos PDF comprometidos como superficie de ataque.

- Protección de aplicaciones. Con Protección de aplicaciones, los administradores pueden configurar una lista de sitios de confianza para su organización. Si los usuarios abren otros sitios, se abren en una ventana de Protección de la aplicación independiente que se ejecuta en su propio contenedor. El contenedor ayuda a proteger la red corporativa y cualquier dato del ordenador del usuario para que no se vea comprometido.<br><br>
Esta protección también se aplica a todos los archivos PDF en línea que se vean. Además, todos los archivos PDF que se descargan desde una ventana de Protección de aplicaciones se almacenan y, cuando es necesario, se vuelven a abrir en el contenedor. Esto ayuda a mantener la seguridad de su entorno, no solo cuando se descarga el archivo, sino durante todo su ciclo de vida. Para obtener más información, vea [Protección de aplicaciones](./microsoft-edge-security-windows-defender-application-guard.md).

### <a name="reliability"></a>Confiabilidad

Dado que Microsoft Edge está basado en Chromium, los usuarios pueden esperar el mismo nivel de confiabilidad que están acostumbrados a ver en otros exploradores basados en Chromium.

## <a name="deploy-and-update-pdf-reader"></a>Implementación y actualización del lector de PDF

Se implementará el lector de PDF y se actualizará con el resto del explorador Microsoft Edge. Para más información sobre la implementación de Microsoft Edge, vea el vídeo [Implementar Microsoft Edge en cientos o miles de dispositivos](microsoft-edge-video-deploy.md). También puede encontrar más información sobre la implementación en la página de aterrizaje de [Documentación de Microsoft Edge](./index.yml).

> [!TIP]
> Puede hacer de Microsoft Edge el lector de PDF predeterminado de su organización. Para ello, [siga estos pasos](./edge-default-browser.md).

## <a name="roadmap-and-feedback"></a>Plan de desarrollo y comentarios

La guía básica para el lector de PDF en Microsoft Edge está disponible [aquí.](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667)

Buscamos constantemente su opinión sobre las características que le parecen importantes. No dude en enviarnos comentarios a través del foro [de la aplicación de Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider) Microsoft Edge.

## <a name="see-also"></a>Vea también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Plan de desarrollo de Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap)
- [Vídeo: Lector de PDF de nivel empresarial de Microsoft Edge](microsoft-edge-video-pdf-reader.md)