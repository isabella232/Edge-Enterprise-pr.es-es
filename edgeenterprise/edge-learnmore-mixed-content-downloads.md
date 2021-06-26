---
title: Descargas de contenido mixto en Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 04/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Descargas de contenido mixto en Microsoft Edge
ms.openlocfilehash: a81c44754865b2303320bfe87346c7f7533e6133
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617310"
---
# <a name="learn-about-microsoft-edge-and-mixed-content-downloads"></a>Obtén más información sobre las descargas de contenido mixto en Microsoft Edge

En este artículo se explican las descargas de contenido mixto y cómo Microsoft Edge las maneja.

>[!NOTE]
>Este artículo se aplica a Microsoft Edge, versión 85 o posterior.

## <a name="what-are-mixed-content-downloads"></a>¿Qué son las descargas de contenido mixto?

Se produce una descarga de contenido mixto cuando inicias una descarga desde una página HTML que se cargó a través de una conexión HTTPS segura, pero se produce una de las siguientes condiciones:

- Una o más redirecciones de la ubicación de descarga se ha cargado mediante una conexión HTTP no segura.
- La ubicación de descarga final se ha cargado mediante una conexión HTTP no segura.

En cualquier de los dos escenarios se produce la descarga de contenido mixto porque la solicitud se realizó mediante una conexión de HTTPS segura y el contenido, tanto HTTP como HTTPS, se invoca cuando llega al destino final de descarga. Los exploradores modernos muestran advertencias sobre este tipo de contenido para indicar al usuario que esa descarga podría transferirse de forma insegura, aunque la página original a la que se accedió era segura.

## <a name="download-warnings-and-user-options"></a>Advertencias de descarga y opciones de usuario

La advertencia de descarga garantiza que los usuarios sepan que el archivo que se está descargando podría ser leído por atacantes malintencionados en su red. Esta advertencia permite a los usuarios tomar decisiones fundamentadas sobre si se debe descargar el archivo.

En Microsoft Edge, las descargas de contenido mixto se bloquearán, pero los usuarios podrán invalidar el bloqueo y descargar el archivo si lo desean. Microsoft Edge planea empezar a bloquear la descarga de archivos ejecutables de contenido mixto desde la versión 85 de Microsoft Edge. Además, bloqueará diferentes tipos de archivo en futuras versiones.

> [!NOTE]
> La implementación de esta característica está sujeta a cambios en función de la programación de lanzamiento y los comentarios de los usuarios.

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

En el estante de descarga, el mensaje de advertencia de bloqueo es similar al ejemplo en la siguiente captura de pantalla.

 ![Advertencia de contenido mixto en la bandeja de descarga](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

En la página de descarga, la advertencia de bloqueo es similar al ejemplo en la siguiente captura de pantalla:

 ![Aviso de invalidación de bloqueo de contenido mixto](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

Si el usuario decide mantener la descarga, se le pedirá que confirme la acción. La siguiente captura de pantalla muestra un ejemplo de este aviso de confirmación.

 ![Elegir el modo Internet Explorer](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <a name="supporting-policies"></a>Directivas de apoyo

Las empresas que deseen excluir el bloqueo de contenido mixto en sitios web específicos, pueden usar la directiva [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) para ello.

## <a name="content-license"></a>Licencia de contenido

> [!NOTE]
> Algunas partes de esta página son modificaciones que se basan en trabajo creado y compartido por Chromium.org y que se usan de acuerdo con los términos descritos en la [Licencia internacional de Creative Commons Atribution 4.0](http://creativecommons.org/licenses/by/4.0/). La página original se puede encontrar [aquí](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Este trabajo dispone de licencia conforme a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licencia internacional de Creative Commons Attribution 4.0</a>.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)