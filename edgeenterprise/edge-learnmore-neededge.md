---
title: Redirección de Internet Explorer a Microsoft Edge por motivos de compatibilidad con sitios web modernos
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Redirección de Internet Explorer a Microsoft Edge por motivos de compatibilidad con sitios web modernos
ms.openlocfilehash: ec59380b82dc975ba3075d6e008bc0da05136f72
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642116"
---
# <a name="redirection-from-internet-explorer-to-microsoft-edge-for-compatibility-with-modern-web-sites"></a>Redirección de Internet Explorer a Microsoft Edge por motivos de compatibilidad con sitios web modernos

> [!NOTE]
> Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.

## <a name="overview"></a>Introducción

>[!Note]
> La aplicación de escritorio Internet Explorer 11 será retirada y dejará de recibir soporte el 15 de junio de 2022 (para ver una lista de lo que está en juego, [consulte las preguntas frecuentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Las mismas aplicaciones y sitios de IE11 que use hoy pueden abrirse en Microsoft Edge mediante el uso del modo Internet Explorer. [Más información aquí](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Muchos sitios web modernos tienen diseños que no son compatibles con Internet Explorer. Siempre que un usuario de Internet Explorer visite un sitio público incompatible, recibirá un mensaje en el que se indicará que el sitio no es compatible con el explorador y tendrá que cambiar de forma manual a otro explorador.

La necesidad de cambiar manualmente a otro navegador diferente, cambia a partir de la versión estable de Microsoft Edge 87.

Cuando un usuario se dirige a un sitio que no es compatible con Internet Explorer, se le redirigirá automáticamente a Microsoft Edge. En este artículo se describe la experiencia de usuario para la redirección y las directivas de grupo que se usan para configurar o deshabilitar el redireccionamiento automático.

> [!NOTE]
> Microsoft mantiene una lista de todos los sitios que se sabe que son incompatibles con Internet Explorer. Para obtener más información, consulte [Solicitar actualizaciones a la lista de sitios incompatibles](/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)

## <a name="prerequisites"></a>Requisitos previos
- Microsoft Edge Versión estable 87 o posterior
- Versiones de Windows
    - Windows 10 versión 1709 o posterior
    - Windows 8.1
    - Windows 7



## <a name="redirection-experience"></a>Experiencia de redirección

En el redireccionamiento a Microsoft Edge, los usuarios se muestran en el cuadro de diálogo único en la siguiente captura de pantalla. Este cuadro de diálogo explica por qué se les redirige y pide consentimiento para copiar los datos de exploración y las preferencias de Internet Explorer en Microsoft Edge. Se importarán los siguientes datos de examen: favoritos, contraseñas, motores de búsqueda, pestañas abiertas, historial, configuración, cookies y la Página principal.

![Examen de notificación y solicitud para importar datos y preferencias.](media/edge-learnmore-neededge/neededge-dialog1.png)

Incluso si no dan su consentimiento al comprobar "traer siempre mis datos y preferencias de navegación de Internet Explorer", pueden hacer clic en **continuar explorando** para continuar la sesión.

Por último, un banner de incompatibilidad con el sitio web, que se muestra en la siguiente captura de pantalla, aparece debajo de la barra de direcciones para cada redirección.

![Notificación sobre sitios modernos y preguntar si se establece Microsoft Edge como explorador predeterminado o explorar Microsoft Edge.](media/edge-learnmore-neededge/neededge-banner.png)

El anuncio de incompatibilidad del sitio web:

- alienta al usuario a cambiar a Microsoft Edge
- pide establecer a Microsoft Edge como explorador predeterminado
- ofrece al usuario la opción de explorar Microsoft Edge.

Cuando se redirige un sitio de Internet Explorer a Microsoft Edge, la pestaña de Internet Explorer que comenzó a cargar el sitio se cierra si no tenía contenido anterior. En caso contrario, la vista de pestañas activa va a una página de  [Soporte técnico de Microsoft](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) que explica por qué el sitio se redirigió a Microsoft Edge.

> [!NOTE]
> Después de que un usuario redireccionamiento pueda volver a usar Internet Explorer para los sitios que no están en la lista de compatibilidad de Internet Explorer.  

## <a name="policies-to-configure-redirection-to-microsoft-edge"></a>Directivas para configurar el redireccionamiento a Microsoft Edge

> [!NOTE]
> Estas directivas estarán disponibles como actualizaciones de archivos ADMX en el 26 de octubre de 2020, y estarán disponibles en Intune el 9 de noviembre de 2020.

Se deben configurar tres directivas de grupo para habilitar el redireccionamiento automático a Microsoft Edge. Estas directivas son las siguientes:

- RedirectSitesFromInternetExplorerPreventBHOInstall
- RedirectSitesFromInternetExplorerRedirectMode
- HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

### <a name="policy-redirectsitesfrominternetexplorerpreventbhoinstall"></a>Directiva: RedirectSitesFromInternetExplorerPreventBHOInstall

El redireccionamiento de Internet Explorer a Microsoft Edge necesita un objeto de aplicación auxiliar de Internet Explorer (BHO) denominado "IEtoEdge BHO". La Directiva **RedirectSitesFromInternetExplorerPreventBHOInstall** controla si este BHO está instalado.  

- Si habilita esta Directiva, el BHO necesario para la redirección no se instalará y los usuarios podrán seguir viendo mensajes de incompatibilidad para determinados sitios web en Internet Explorer. Si el BHO ya está instalado, se desinstalará la próxima vez que se actualice el canal estable de Microsoft Edge.
- Si deshabilita o no configura esta Directiva, se instalará el BHO. Este es el comportamiento predeterminado.

Además de requerir el BHO, hay una dependencia en **RedirectSitesFromInternetExplorerRedirectMode**, que se debe establecer en "Redirigir los sitios de acuerdo con la lista se sitios incompatibles" o en "No configurado".

### <a name="policy-redirectsitesfrominternetexplorerredirectmode"></a>Directiva: RedirectSitesFromInternetExplorerRedirectMode

 Esta Directiva corresponde al Microsoft Edge **explorador predeterminado** la configuración "permitir que Internet Explorer abra sitios en Microsoft Edge". Para obtener acceso a esta configuración, vaya a la *edge://settings/defaultbrowser* URL.  

- Si no configura esta Directiva o la configura en "sitelist", Internet Explorer redirigirá sitios incompatibles a Microsoft Edge. Este es el comportamiento predeterminado.
- Para deshabilitar esta directiva, seleccione **Habilitado** Y, a continuación, en la lista desplegable de Opciones: Redirigir los sitios incompatibles de Internet Explorer a Microsoft Edge, seleccione **Deshabilitar**. En este estado, los sitios incompatibles no se redirigen a Microsoft Edge.

> [!NOTE]
> Si se encuentra en un dispositivo personal que no está administrado por su organización, verá otra opción denominada "permitir que los sitios se carguen en modo Internet Explorer", en **Compatibilidad de Internet**. Explorer.
>
>Si se encuentra en un dispositivo inscrito en un dominio Unido o en la administración de dispositivos móviles (MDM), no verá esta opción.
>
> En su lugar, si quiere permitir que los usuarios carguen los sitios en el modo de Internet Explorer, puede hacerlo configurando la Directiva [permitir la realización de pruebas en el modo de Internet Explorer](./microsoft-edge-policies.md#intranetredirectbehavior).

### <a name="policy-hideinternetexplorerredirectuxforincompatiblesitesenabled"></a>Directiva: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

Esta directiva configura la experiencia de usuario para la redirección del sitio no compatible con Microsoft Edge.  

- Si habilita esta Directiva, los usuarios nunca verán el cuadro de diálogo de redirección y la pancarta de redirección. No se importan datos de explorador ni preferencias de usuario.
- Si deshabilita o no configura esta Directiva, el cuadro de diálogo de redirección se mostrará en la primera redirección y se mostrará el encabezado de redirección persistente para las sesiones que comiencen con una redirección.

  > [!NOTE]
  > Los datos de búsqueda de usuarios se importarán cada vez que un usuario encuentre un nuevo redireccionamiento. Sin embargo, esto solo se produce si el usuario se ha enviado a la importación en el cuadro de diálogo redirección único.

## <a name="disable-redirection-to-microsoft-edge"></a>Deshabilitar la redirección a Microsoft Edge

Si desea deshabilitar la redirección antes de actualizar a la versión estable 87 de Microsoft Edge, siga el procedimiento siguiente:

1. Configure la Directiva **RedirectSitesFromInternetExplorerPreventBHOInstall** en **Activada**.

Si desea deshabilitar la redirección después de actualizar a la versión estable 87 de Microsoft Edge, siga estos pasos:

1. Configure la directiva **RedirectSitesFromInternetExplorerRedirectMode** en **Habilitada** Y, a continuación, en la lista desplegable en Opciones: Redirigir los sitios incompatibles de Internet Explorer a Microsoft Edge, seleccione **Deshabilitar**. Esta configuración dejará de redirigirse tan pronto como se aplique la drectiva.
2. Configure la Directiva **RedirectSitesFromInternetExplorerPreventBHOInstall** en **Activada**. Se desinstalará el BHO después de la siguiente actualización de Microsoft Edge.

## <a name="see-also"></a>Vea también

- [Solicitar actualizaciones a la lista de sitios incompatibles](/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Directivas de Microsoft Edge](./microsoft-edge-policies.md)