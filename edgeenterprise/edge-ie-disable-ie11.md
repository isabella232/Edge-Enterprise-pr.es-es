---
title: Deshabilitar Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Obtenga información sobre cómo deshabilitar Internet Explorer 11 y usar el modo de Internet Explorer en Microsoft Edge.
ms.openlocfilehash: 9ea99c794dc06a0eb5167e56e72b6e7b6ee70212
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641516"
---
# <a name="disable-internet-explorer-11"></a>Deshabilitar Internet Explorer 11

>[!Note]
> La aplicación de escritorio Internet Explorer 11 se retirará y dejará de recibir soporte el 15 de junio de 2022 (para ver una lista de lo que se verá afectado, [consulte las preguntas frecuentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Las mismas aplicaciones y sitios de IE11 que use hoy pueden abrirse en Microsoft Edge mediante el uso del modo Internet Explorer. [Más información aquí](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

En este artículo se describe cómo deshabilitar Internet Explorer 11 como un explorador independiente en su entorno.

## <a name="prerequisites"></a>Requisitos previos

Son necesarias las siguientes actualizaciones de Windows y el software Microsoft Edge:

- Actualizaciones de Windows

  - Windows 10, versión 2004, Windows Server versión 2004, Windows 10, versión 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b)
  - Windows 10, versión 1909, Windows Server versión 1909 [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) o posterior
  - Windows 10, versión 1809, Windows Server, versión 1809, y Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) o posterior
  - Windows 10, versión 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) o posterior
   - Versión inicial de Windows 10 (julio de 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) o posterior
  - Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) o posterior
  - Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) o posterior
  
- Canal Estable de Microsoft Edge


## <a name="overview"></a>Introducción

Para las organizaciones que necesitan Internet Explorer 11 (IE11) para compatibilidad heredada, el modo de Internet Explorer (modo IE) en Microsoft Edge proporciona una experiencia de explorador única y sin ningún problema. Los usuarios pueden acceder a las aplicaciones heredadas desde Microsoft Edge sin tener que volver a IE11.

Después de configurar el modo IE, puede deshabilitar IE11 como explorador independiente **sin afectar a la funcionalidad del modo IE** toda la organización mediante directivas de grupo.

> [!NOTE]
> Si necesita la aplicación independiente IE11 para sitios específicos y quiere redirigir todo el tráfico del explorador a Microsoft Edge, puede configurar la política[Enviar todos los sitios que no están incluidos en la lista de sitios a Microsoft Edge](./edge-ie-mode-policies.md#redirect-sites-from-ie-to-microsoft-edge) para redirigir sitios de IE a Microsoft Edge.

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a>Experiencia del usuario después de redirigir tráfico a Microsoft Edge

Cuando habilita la política de **Deshabilitar Internet Explorer 11 como navegador independiente**, toda la actividad de IE11 se redirige a Microsoft Edge y los usuarios tienen la siguiente experiencia:

- Se quitará el icono IE11 del menú Inicio, pero se mantendrá el de la barra de tareas.
- Cuando los usuarios intentan iniciar accesos directos o asociaciones de archivos que usan IE11, se les redirige para abrir el mismo archivo/URL en Microsoft Edge.
- Cuando los usuarios intentan iniciar IE11 invocando directamente el archivo binario iexplore.exe, se iniciará Microsoft Edge en su lugar.

Como parte de la configuración de la directiva para esta experiencia, de manera opcional, puede mostrar un mensaje de redirección para cada usuario que intente iniciar IE11. Este mensaje se puede establecer para mostrar "Siempre" o "Una vez por usuario". De forma predeterminada, el mensaje de redirección que se muestra en la siguiente captura de pantalla nunca se muestra.

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Aviso al intentar abrir IE después de que se active una redirección a Microsoft Edge.":::

Si la lista de sitios del modo de empresa contiene aplicaciones que están configuradas para abrirse en la aplicación IE11 y deshabilita IE11 con esta directiva, se abrirán en modo IE en Microsoft Edge.
> [!NOTE]
> Hubo un problema conocido con el flujo de usuario cuando un sitio está configurado para abrirse en la aplicación IE11 y se establece la directiva Deshabilitar IE11. El problema se ha corregido en Microsoft Edge, versiones 91.0.840.0 o posteriores.

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a>Deshabilitar Internet Explorer 11 como explorador independiente

Para deshabilitar Internet Explorer 11 con una directiva de grupo, siga estos pasos:

1. Asegúrese de que tiene las actualizaciones del sistema operativo necesarias previamente. Este paso actualizará los archivos ADMX directamente en el equipo (específicamente inetres.adml e inetres.admx). Tenga en cuenta que si quiere actualizar la Tienda central, deberá copiar los archivos .adml y .admx de una máquina que tenga las actualizaciones previas. Para más información, consulte [Crear y administrar la Tienda central](/troubleshoot/windows-client/group-policy/create-and-manage-central-store)
2. Abra el editor de directivas de grupo.
3. Vaya a **_Configuración del equipo/Plantillas administrativas/Windows componentes/Internet Explorer_*_. 
4. Haga doble clic en _*Deshabilitar Internet Explorer 11 como explorador independiente**.
5. Seleccione **habilitada**.
6. En **de**opciones, elija uno de los valores siguientes:

   - **No** si no desea notificar a los usuarios que IE11 está deshabilitado.
   - **tenga** siempre si desea notificar a los usuarios cada vez que se les redirija desde IE11.
   - **una vez por usuario** si desea notificar a los usuarios solo la primera vez que se les redirige.

7. Haga **clic en Aceptar** o **aplicar** para guardar esta configuración de directiva.

## <a name="see-also"></a>Vea también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Acerca del modo IE](./edge-ie-mode.md)
- [Información adicional del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
