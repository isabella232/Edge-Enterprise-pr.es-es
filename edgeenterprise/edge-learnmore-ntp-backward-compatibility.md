---
title: Compatibilidad con versiones anteriores para la página de nueva pestaña para empresas
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Compatibilidad con versiones anteriores para la página de nueva pestaña para empresas
ms.openlocfilehash: 9643a7009fdc60859efaadc2adff6e47ce0918567195e9745a4a93c151aefc80
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724231"
---
# <a name="backwards-compatibility-for-the-enterprise-new-tab-page"></a>Compatibilidad con versiones anteriores para la página de nueva pestaña para empresas

Este artículo describe el cambio de la página de la Nueva pestaña y cómo los usuarios pueden ser compatibles con la versión 87 y anteriores de Microsoft Edge.

> [!NOTE]
> Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.

## <a name="information-feeds-from-single-endpoint"></a>Fuentes de información desde un único extremo

La nueva versión de la página de nueva pestaña para empresas combina el contenido compatible con Microsoft 365 con información relevante para el sector que se sirve a través del punto de conexión de MSN.com.

> [!NOTE]
> El contenido de Office 365 se sirvió originalmente utilizando el dominio [Office.com](https://www.office.com).

Si el acceso al dominio MSN.com está restringido para su organización, le recomendamos encarecidamente que le dé a los usuarios acceso a esta [url](https://ntp.msn.com).

Si necesita más tiempo para habilitar el acceso al dominio de MSN, le recomendamos que utilice el [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype), que le permite elegir la experiencia de alimentación de Microsoft News u Office 365 para la nueva página de pestañas.

### <a name="keep-using-officecom"></a>Seguir usando Office.com

 Puede configurar la directiva **NewTabPageSetFeedType** para seguir usando el dominio obsoleto Office.com.

> [!IMPORTANT]
> La directiva **NewTabPageSetFeedType** y el dominio Office.com que sirve el contenido de Office 365 dejarán de funcionar cuando se publique la versión 90 de Microsoft Edge.

La siguiente configuración de la directiva obligará a la página de la Nueva pestaña de la empresa a mostrar el contenido de los documentos de Office desde el dominio Office.com.

- Establezca la directiva como **Obligatoria**.
- Establezca el valor del asignación de directivas en **Office (1) = Office 365 alimenta la experiencia**.

Si el cambio a Office.com no es posible, comuníquese con nosotros y envíenos sus comentarios. Otra opción es configurar [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) para que apunte a una URL de extremo que esté permitida por su organización.

> [!NOTE]
> La directiva **NewTabPageLocation** tiene prioridad si la directiva **NewTabPageSetFeedType** también está configurada.

## <a name="enterprise-users-will-now-get-microsoft-news-content-via-my-feed"></a>Los usuarios de empresas recibirán ahora el contenido de las noticias de Microsoft a través de Mi fuente

La página de nueva pestaña de empresa ofrecerá información relevante para el sector en el contenido de **Mi fuente** y Office 365 en una sola vista para los usuarios que hayan iniciado sesión con su cuenta de Azure Active Directory (Azure AD). Para los usuarios que iniciaron sesión con su Azure Active Directory (Azure AD) y que seleccionaron la opción Microsoft News en el control flotante de configuración, su vista de la página de nueva pestañas será reemplazada por el contenido de **Mi fuente**. Cuando abran una nueva pestaña en el navegador se verá como en el ejemplo en la siguiente captura de pantalla.

![Página de nueva pestañas que muestra el contenido de Mi fuente.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> Los usuarios que no hayan iniciado sesión con Azure AD continuarán viendo la fuente de noticias de MSN cuando abran una nueva pestaña.

## <a name="page-layout"></a>Diseño de página

Con los cambios en la página de nueva pestaña, el diseño de la página ya no tiene que controlar dos tipos de contenido específicos (Office 365 y Microsoft News), por lo que el cambio de contenido no está disponible. La siguiente captura de pantalla muestra el control flotante para el diseño de la página

![Vista de diseño de página de nueva pestaña.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

Si desea seguir teniendo acceso al contenido de las Microsoft News que no está vinculado a su organización, debe utilizar un perfil de explorador diferente. Vaya a *"edge://settings/profiles"* y cierre sesión en su perfil de Azure AD. Esta acción traerá la vista estándar para la página de nueva pestaña de empresas. 

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Modo de empresa para Internet Explorer 11](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)