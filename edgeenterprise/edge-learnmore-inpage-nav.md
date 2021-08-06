---
title: Mantener la navegación en la página en modo Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Mantener la navegación en la página en modo Internet Explorer
ms.openlocfilehash: f1c40977ba07f0a85bc64aab8e609163f9a68dd2eb7487adff6b6a1fcbd110f2
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724301"
---
# <a name="keep-in-page-navigation-in-internet-explorer-mode"></a>Mantener la navegación en la página en modo Internet Explorer

Puedes usar esta directiva como solución temporal para forzar toda la navegación en la página de los sitios en modo Internet Explorer (modo IE) para que permanezca en modo IE.

Una navegación en la página se inicia desde un vínculo, un script o un formulario en la página actual. También puede ser un redireccionamiento de servidor de un intento de navegación en la página anterior. Por otra parte, un usuario puede iniciar una navegación que no sea en la página y que sea independiente de la página actual, de varias formas con los controles del explorador. Por ejemplo, con la barra de direcciones, el botón Atrás o un vínculo favorito.

>[!NOTE]
>Este artículo se aplica a Microsoft Edge, versión 81 o posterior.

## <a name="prerequisites"></a>Requisitos previos

Las siguientes actualizaciones de Windows son necesarias para esta directiva:

- Windows 10, versiones 1909 y 1903; Windows Server, versiones 1909 y 1903  ([KB4532695](https://support.microsoft.com/help/4532695))
- Windows 10, versión 1809; Windows Server, versión 1809; Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))
- Windows 10, versión 1803 ([KB4534308](https://support.microsoft.com/help/4534308))
- Windows 10, versión 1709 ([KB4534318](https://support.microsoft.com/help/4534318))


## <a name="about-this-policy"></a>Acerca de esta directiva

Esta directiva te proporciona tiempo para identificar y configurar todos los servidores de autenticación usados por los sitios en modo IE. Sin embargo, esta directiva puede dar lugar a una experiencia de navegación incoherente, en la que algunos sitios se muestran en modo IE y en otras ocasiones se muestran en modo Microsoft Edge. Esta experiencia depende de si la navegación al sitio comenzó desde una página en modo IE. Cualquier sitio que no se haya configurado explícitamente para abrirse en un motor de procesamiento específico estará sujeto a esta incoherencia.

Si habilitas esta directiva, se recomienda que la deshabilites después de que hayas identificado todos los servidores de autenticación y los hayas agregado como neutros a la lista de sitios. De esta forma, te asegurarás de que los sitios modernos nunca se muestren accidentalmente en modo IE.

## <a name="keep-in-page-navigation-in-ie-mode"></a>Mantener la navegación en la página en modo IE

Para mantener toda la navegación en la página o la automática en modo Internet Explorer, sigue estos pasos:

1. Abre el Editor de directivas de grupo local.
2. Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Microsoft Edge**.
3. En **Configuración**, haz doble clic en **Especifica cómo se comportan las navegaciones "en la página" de los sitios no configurados al iniciarse en las páginas en modo Internet Explorer**.

   ![Configuración de directiva en la página](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. Selecciona **Habilitada** 

   ![Habilitar directiva en la página](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. En la lista desplegable, elije una de las siguientes opciones:

   - **Predeterminada** - Solo los sitios configurados para abrirse en el modo Internet Explorer se abrirán en ese modo. Cualquier sitio que no esté configurado para abrirse en modo Internet Explorer se redirigirá a Microsoft Edge.
   - **Mantener solo las navegaciones automáticas en modo Internet Explorer**: Usa esta opción si quieres la experiencia predeterminada, pero que todas las navegaciones automáticas (como las redirecciones 302) a sitios no configurados se mantengan en modo Internet Explorer.
   - **Mantener toda la navegación** en la página en modo Internet Explorer **_(menos recomendado):_** todas las navegaciónes de páginas cargadas en modo IE a sitios no configurados se mantienen en modo Internet Explorer.

6. Haz clic en **Aceptar** o **Aplicar** para guardar la configuración de la directiva.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
