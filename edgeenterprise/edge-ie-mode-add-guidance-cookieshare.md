---
title: Compartir cookies de Microsoft Edge a Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/19/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Como compartir cookies de Microsoft Edge a Internet Explorer '
ms.openlocfilehash: 563179852ff23142b540345222ba7e943547535d
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617470"
---
# <a name="cookie-sharing-from-microsoft-edge-to-internet-explorer"></a>Compartir cookies de Microsoft Edge a Internet Explorer

>[!Note]
> La aplicación de escritorio Internet Explorer 11 será retirada y dejará de recibir soporte el 15 de junio de 2022 (para ver una lista de lo que está en juego, [consulte las preguntas frecuentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Las mismas aplicaciones y sitios de IE11 que use hoy pueden abrirse en Microsoft Edge mediante el uso del modo Internet Explorer. [Más información aquí](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Este artículo explica cómo configurar el uso compartido de cookies de sesión de un proceso de Microsoft Edge al proceso de Internet Explorer, mientras se usa el modo de Internet Explorer.

> [!NOTE]
> Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.

## <a name="prerequisites"></a>Requisitos previos

- Actualizaciones de Windows

  - Windows 10 versión 2004, Windows Server versión 2004: KB4571744 o superior
  - Windows 10 versión 1909, Windows Server versión 1909: KB4566116 o superior
  - Windows 10 versión 1903, Windows Server versión 1903: KB4566116 o superior
  - Windows 10, versión 1809; Windows Server, versión 1809, y Windows Server 2019: KB4571748 o superior
  - Windows 10, versión 1803 (KB4577032 o superior)

- Microsoft Edge, versión 87 o posterior
- [Modo IE](./edge-ie-mode.md) configurado con la lista de sitios del Modo de empresa

## <a name="overview"></a>Introducción

Una configuración común en las organizaciones de gran tamaño consiste en tener una aplicación que funcione en un vínculo de explorador moderno a otra aplicación, que se puede configurar para abrir en modo de Internet Explorer con el inicio de sesión único (SSO) habilitado como parte del flujo de trabajo.

De forma predeterminada, los procesos de Microsoft Edge e Internet Explorer no comparten las cookies de sesión, por lo que puede ser poco práctico en ciertos casos. Por ejemplo, cuando un usuario tiene que volver a autenticarse en el modo de Internet Explorer o al cerrar sesión en una sesión de Microsoft Edge no se firma en la sesión de modo de Internet Explorer. En estos casos, puede configurar las cookies específicas establecidas por SSO para enviarlas de Microsoft Edge a Internet Explorer, de modo que la experiencia de autenticación sea más fluida eliminando la necesidad de realizar una nueva autenticación.

> [!NOTE]
> Las cookies solo pueden ser compartidas de Microsoft Edge a Internet Explorer. No es posible compartir cookies de sesión de en inverso (de Internet Explorer a Microsoft Edge).

## <a name="how-cookie-sharing-works"></a>Cómo funciona el uso compartido de cookies

Se ha ampliado el XML de la lista de sitios de modo empresarial para permitir que otros elementos especifiquen cookies que se requieren compartir desde una sesión de Microsoft Edge con Internet Explorer.  

La primera vez que se crea una pestaña en modo de Internet Explorer en una sesión de Microsoft Edge, todas las cookies correspondientes se comparten en la sesión de Internet Explorer. Por lo tanto, cada vez que se agregue, elimine o modifique un cookie que coincida con una regla, se enviará como una actualización de la sesión de Internet Explorer. Cuando se actualiza la lista de sitios, el conjunto de cookies compartidas también vuelve a evaluarse.

### <a name="updated-schema-elements"></a>Elementos de esquema actualizados

En la siguiente tabla se describe el elemento de \<shared-cookie\> agregado para admitir la característica de uso compartido de cookies.

| Elemento| Descripción |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>O bien,<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(obligatorio)** un elemento de \<shared-cookie\> requiere, como mínimo, un *de dominio* (para las cookies del dominio) o un atributo *host* (solo para cookies de host) y un atributo *nombre* .<br>Deben ser coincidencias exactas con el dominio y el nombre de la cookie respectivamente. **Nota** los subdominios no coinciden.<br><br>El atributo *dominio* se usa para las cookies de dominio (y se permite un punto inicial, pero es opcional).<br>El atributo *host* se usa para las cookies solo de host (y un punto inicial es un error). Especifica ninguno o ambos producirá un error.<br>* Un cookie es una cookie de dominio si se especificó un dominio en la cadena de la cookie (a través de un encabezado o documento de respuesta cookie Set HTTP. cookie JS API). Las cookies de dominio se aplican a los dominios y subdominios especificados. Si un dominio no es establecido en la cadena cookie, el cookie es un cookie solo para host y solo se aplica al host específico en el que se haya establecido. Tenga en cuenta que algunas clases de direcciones URL, como nombres de host de una sola palabra (como, por ejemplo, http://intranetsite) y direcciones IP (por ejemplo, http://10.0.0.1) solo pueden establecer cookies solo de anfitrión.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | **(opcional)** un atributo *path* puede ser especificado Si no se especifica ningún atributo Path (o si el atributo path está vacío), las cookies que coinciden con Domain/host y Name coinciden con la Directiva, independientemente de la ruta de acceso (regla comodín).<br><br>Si se especifica una ruta de acceso, debe ser una coincidencia exacta.<br>Si un cookie coincide con una regla con una ruta de acceso, tiene prioridad sobre una regla sin una ruta de acceso. |

#### <a name="sharing-example"></a>Ejemplo de uso compartido

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <a name="see-also"></a>Consulte también

- [Acerca del modo IE](./edge-ie-mode.md)
- [Información de sitios configurables](./edge-learnmore-configurable-sites-ie-mode.md)
- [Información adicional del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)