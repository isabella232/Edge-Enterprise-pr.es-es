---
title: Lista de sitios local para el modo IE
ms.author: shisub
author: AndreaLBarr
manager: srugh
ms.date: 07/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Obtenga información sobre cómo habilitar listas de sitios locales y acceso fácil al modo IE
ms.openlocfilehash: 0c79622a1f96cad83a2436f5e79e69914f4a2c40
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979761"
---
## <a name="local-site-list-for-ie-mode"></a>Lista de sitios local para el modo IE

>[!Note]
> La aplicación de escritorio Internet Explorer 11 se retirará y dejará de recibir soporte el 15 de junio de 2022 (para ver una lista de lo que se verá afectado, [consulte las preguntas frecuentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Las mismas aplicaciones y sitios de IE11 que use hoy pueden abrirse en Microsoft Edge mediante el uso del modo Internet Explorer. [Más información aquí](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

En este artículo se explica cómo configurar el fácil acceso al modo de Internet Explorer (modo IE) y permitir el uso de listas de sitios locales en su organización.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge versión 92 o posterior.

### <a name="prerequisites"></a>Requisitos previos

1. Actualizaciones de Windows

- Windows 10, versión 1909: [KB5003698](https://support.microsoft.com/topic/june-15-2021-kb5003698-os-build-18363-1645-preview-1ecf117e-1f89-40f9-a0a5-ed5766737620) o posterior  

- Windows 10, versión 2004; Windows 10, versión 20H2 y Windows 10, versión 21H1 – [KB5003690](https://support.microsoft.com/topic/june-21-2021-kb5003690-os-builds-19041-1081-19042-1081-and-19043-1081-preview-11a7581f-2a01-47d5-ba12-431709ee2248) o posterior

2. Microsoft Edge versión 92 (92.0.925.0 o posterior)

## <a name="overview"></a>Introducción

El modo IE funciona con la configuración de la Enterprise de sitio de modo de instalación. Mientras identifica y configura sitios en la lista de sitios para que usen el modo IE, los usuarios ya no necesitan esperar ni volver a la aplicación IE11 independiente.

A partir Microsoft Edge versión 92, el acceso repetido a sitios de modo *IE* sin configurar es más fácil. Los usuarios pueden volver a cargar sitios en modo IE. Pueden agregar estos sitios a su lista de sitios local para representarlos automáticamente en modo IE durante un período de 30 días, mientras se actualiza la lista de sitios de la organización. Cuando [IE11 está deshabilitado](/deployedge/edge-ie-disable-ie11) en el entorno, los usuarios ya no dependen únicamente de la lista de sitios de la organización.

Puede configurar esta experiencia a través de directivas de grupo para su organización.

Nota: Un *sitio no* configurado es aquel que requiere el modo IE, pero no está configurado para abrirse en modo IE en la lista de sitios Enterprise modo de configuración.

## <a name="local-site-list-experience"></a>Experiencia de lista de sitios local

Para habilitar la experiencia de lista de sitios local, los usuarios pueden ir a la dirección URL *edge://settings/defaultBrowser* y establecer Permitir que los sitios se vuelvan a cargar en el modo **de Internet Explorer** en **Permitir**.

:::image type="content" source="media/Edge-hybrid-IE-mode/internet-explorer-compatibilitiy.png" alt-text="Compatibilidad con Internet Explorer":::

>[! Nota:]  

>1. Si ha habilitado las pruebas del modo IE a través de la directiva *InternetExplorerIntegrationTestingAllowed,* verá esta configuración, pero se mostrará en gris a menos que habilite explícitamente la directiva *InternetExplorerIntegrationReloadInIEModeAllowed.*  
>2. Si **Permitir que los** sitios se vuelvan a cargar en modo Internet Explorer está establecido en Predeterminado, es posible que los usuarios puedan volver a cargar sitios en modo IE si tienen uso de Internet Explorer 11 existente. ****  

Cuando esta configuración está habilitada, los usuarios pueden volver a cargar un sitio en modo IE seleccionando Configuración y más **(el**icono de puntos suspensivos ...) > Recargar en modo Internet Explorer . Los usuarios también pueden seleccionar la pestaña Volver a cargar en modo **Internet Explorer** cuando hacen clic con el botón secundario en una pestaña o cuando hacen clic con el botón secundario en un vínculo, elija Abrir vínculo en la nueva pestaña modo de **Internet Explorer.**

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-screenshot.png" alt-text="Volver a cargar en el modo de Internet Explorer":::

El **icono Volver a cargar en modo de Internet Explorer** se puede anclar a la barra de herramientas. El botón de la barra de herramientas permite a los usuarios entrar y salir fácilmente del modo IE y se pueden administrar a través de la dirección URL *edge://settings/appearance* usuario.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-icon-screenshot.png" alt-text="Volver a cargar en el icono del modo de Internet Explorer":::

>[!Note]
>Si el usuario se encuentra en un sitio que ya está en la lista de sitios del modo Enterprise de la organización, las opciones para volver a cargar en (o salir) el modo de Internet Explorer estarán visibles pero grises.

Cuando se selecciona la opción, el sitio se vuelve a cargar en modo IE. El icono del indicador de modo IE está visible a la izquierda de la barra de direcciones y el control desplegable muestra una opción que los usuarios pueden alternar a Abrir la página en modo Internet Explorer la próxima vez. Esto agrega la página específica en la que el usuario está en la lista de sitios local y se abrirá automáticamente en modo IE durante los próximos 30 días.

:::image type="content" source="media/Edge-hybrid-IE-mode/site-has-been-reloaded-in-ie-mode-screenshot.png" alt-text="Esta página está abierta en el modo de Internet Explorer":::

Una vez que se haya recargado un sitio en modo IE, las navegaciónes "en la página" permanecerán en modo IE (por ejemplo, un vínculo, un script o un formulario en la página, o un redireccionamiento del lado servidor desde otra navegación "en la página").  

Mientras se encuentra en modo IE, los usuarios verán un banner que indica que están en modo IE, la opción dejar el modo IE y anclar el icono del modo IE a la barra de herramientas (si aún no está anclado).

:::image type="content" source="media/Edge-hybrid-IE-mode/ie-mode-banner-screenshot.png" alt-text="Banner del modo IE":::

Los usuarios pueden elegir salir del modo IE con el botón Dejar en el banner, el icono del modo IE anclado o Configuración y mucho más (el icono de puntos suspensivos ...) > Salir del modo **Internet Explorer,** de lo contrario Microsoft Edge saldrá automáticamente del modo IE cuando se produzca una navegación que no sea "en la página" (por ejemplo, mediante la barra de direcciones, el botón atrás o un vínculo favorito).

Las entradas permanecen en la lista de sitios locales durante un período predeterminado de 30 días. Se recomienda configurar sitios heredados para su organización en la lista de sitios Enterprise modo de configuración. La lista de sitios local garantizará que los usuarios puedan continuar su flujo de trabajo sin que se interrumpan mientras se actualiza la lista de sitios de la organización. El día 31, cuando los usuarios naveguen al sitio, verán un banner que explica que el sitio ya no se cargará en modo IE. Los usuarios pueden volver a agregarlo a la lista de sitios local si así lo deciden.

:::image type="content" source="media/Edge-hybrid-IE-mode/page-will-no-longer-load-in-ie-mode-screenshot.png" alt-text="La página ya no se cargará en modo IE":::

## <a name="policies-to-configure-the-use-of-local-site-lists-for-ie-mode"></a>Directivas para configurar el uso de listas de sitios locales para el modo IE

Hay dos directivas de grupo disponibles para configurar la experiencia de lista de sitios local en Microsoft Edge. Estas directivas son las siguientes:

### *<a name="policy-internetexplorerintegrationreloadiniemodeallowed"></a>Directiva: InternetExplorerIntegrationReloadInIEModeAllowed*

Esta directiva corresponde a la configuración Microsoft Edge configuración "Permitir que los sitios se vuelvan a cargar en el modo de Internet Explorer". Para obtener acceso a esta configuración, vaya a la *edge://settings/defaultbrowser* URL.

- Si habilita esta directiva, los usuarios pueden volver a cargar un sitio en modo IE seleccionando Configuración y más **(el**icono de puntos suspensivos ... > Recargar en modo Internet Explorer . Los usuarios también pueden seleccionar la pestaña Volver a cargar en modo **Internet Explorer** cuando hacen clic con el botón secundario en una pestaña o elegir Abrir vínculo en la nueva pestaña modo de **Internet Explorer** cuando hacen clic con el botón secundario en un vínculo.
Los usuarios pueden, opcionalmente, Microsoft Edge usar el modo IE para el sitio en el futuro. Esta opción se recordará durante un valor predeterminado de 30 días y se puede administrar mediante la directiva *InternetExplorerIntegrationLocalSiteListExpirationDays*.

- Si deshabilita esta directiva, los usuarios no podrán volver a cargar un sitio no configurado en modo IE.

- Si no configura esta directiva, mostraremos las opciones de los usuarios para volver a cargar sitios no configurados en modo IE en función del uso reciente de Internet Explorer 11.

Tenga en cuenta que esta directiva tiene prioridad sobre cómo configuró la directiva [InternetExplorerIntegrationTestingAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) y esa directiva se deshabilitará.

### *<a name="policy-internetexplorerintegrationlocalsitelistexpirationdays"></a>Directiva: InternetExplorerIntegrationLocalSiteListExpirationDays*

Esta directiva se puede usar para ajustar el número de días que un sitio permanece en la lista de sitios local para los usuarios.  

- Si deshabilita o no configura esta directiva, se usa un valor predeterminado de 30 días.

- Si habilita la directiva, debe especificar un valor entre 0-90 días para mantener el sitio en la lista de sitios local de un usuario.

Esta directiva no tiene efecto si deshabilitó la directiva *InternetExplorerIntegrationReloadInIEModeAllowed.*

**Nota:**

La lista de sitios local no se sincroniza actualmente entre dispositivos. Esta mejora se encuentra actualmente en nuestro registro pendiente y se actualizará cuando esté disponible.

## <a name="see-also"></a>Consulta también

Deshabilitar Internet Explorer 11: [deshabilitar Internet Explorer 11 | Microsoft Docs](/deployedge/edge-ie-disable-ie11)

Configurar directivas de modo IE: [configurar directivas de modo IE | Microsoft Docs](/deployedge/edge-ie-mode-policies)

