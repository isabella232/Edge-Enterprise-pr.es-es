---
title: Estrategia de configuración del sitio de la empresa
ms.author: shisub
author: shisub
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Una guía paso a paso para configurar la lista de sitios en modo empresa para el modo de Internet Explorer..
ms.openlocfilehash: ec0d1364f3db00bc78e29bab8abbfcf1748f68494791fd5288a435a8b1230018
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724423"
---
# <a name="enterprise-site-configuration-strategy"></a>Estrategia de configuración del sitio de la empresa

>[!Note]
> La aplicación de escritorio Internet Explorer 11 se retirará y dejará de recibir soporte el 15 de junio de 2022 (para ver una lista de lo que se verá afectado, [consulte las preguntas frecuentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Las mismas aplicaciones y sitios de IE11 que use hoy pueden abrirse en Microsoft Edge mediante el uso del modo Internet Explorer. [Más información aquí](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

En este artículo, se describen los cambios realizados en la lista de sitios en modo empresa para la compatibilidad del modo de Internet Explorer con Microsoft Edge versión 77 y posteriores.

Para obtener más información sobre el esquema para el archivo XML de lista de sitios en el modo de empresa, consulte la [Guía de esquema de modo de empresa v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a>Estrategia de configuración

Los siguientes pasos forman parte de una estrategia de configuración del sitio para el modo IE:
1. Prepare su lista de sitios
2. Configurar los sitios neutros
3. (Opcional) Utilizar el uso compartido de cookies si es necesario

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a>Prepare su lista de sitios

Si ya tiene una lista de sitios en modo de empresa para IE11 o Microsoft Edge Legacy, puede reutilizarla para configurar el modo IE.

Sin embargo, si no tiene una lista de sitios, puede utilizar la [herramienta Enterprise Site Discovery](/deployedge/edge-ie-mode-site-discovery)para rellenar su lista de sitios.

## <a name="configure-neutral-sites"></a>Configurar los sitios neutros

Para que el modo IE funcione correctamente, los servidores de autenticación / Inicio de sesión único (SSO) tendrán que ser configurados explícitamente como sitios neutrales. De lo contrario, las páginas del modo IE intentarán redirigir a Microsoft Edge, y la autenticación fallará.

Un sitio neutral usará el explorador en el que se inició el desplazamiento, ya sea en el modo de Microsoft Edge o el modo de IE. La configuración de los sitios neutros garantiza que todas las aplicaciones que utilicen los mismos servidores de autenticación, tanto modernos como heredados, sigan funcionando.

Para configurar sitios neutros, configure la lista desplegable *Abrir en* como "ninguna" en la Herramienta de Administración de Lista de Sitios del Modo de Empresa, o bien actualice el XML de la lista de sitios directamente:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

Para identificar los servidores de autenticación, inspeccione el tráfico de red de una aplicación utilizando las herramientas de desarrollo de IE11. Si necesita más tiempo para identificar sus servidores de autenticación, puede configurar una directiva para mantener todas las navegaciones dentro de la página en modo IE para permitir que sus usuarios continúen sus flujos de trabajo sin interrupción. Para minimizar el uso del modo IE cuando sea innecesario, desactive esta configuración una vez que haya identificado y agregado sus servidores de autenticación a la lista de sitios. Para obtener más información, consulte [Mantener la navegación en la página en modo IE](/deployedge/edge-learnmore-inpage-nav).

>[!NOTE]
   >El esquema v. 1 del modo de empresa no se admite para la integración de modo IE. Si estás usando actualmente el esquema v. 1 con Internet Explorer 11, debes actualizar al esquema v. 2. Para obtener más información, consulte [Guía sobre el esquema del Modo de empresa v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## <a name="optional-use-cookie-sharing-if-necessary"></a>(Opcional) Utilizar el uso compartido de cookies si es necesario

De forma predeterminada, los procesos de Microsoft Edge e Internet Explorer no comparten las cookies de sesión, y esta falta de compartición puede ser un inconveniente en algunos casos mientras se utiliza el modo IE. Por ejemplo, cuando un usuario tiene que volver a autenticarse en modo IE cuando previamente está acostumbrado a hacerlo o cuando al cerrar la sesión de Microsoft Edge no se cierra la sesión en modo Internet Explorer para las transacciones críticas. En estos escenarios, puede configurar cookies específicas establecidas por SSO para que se envíen desde Microsoft Edge a Internet Explorer, de modo que la experiencia de autenticación sea más fluida al eliminar la necesidad de volver a autenticar. Para obtener más información, consulte [Compartir cookies de Microsoft Edge a Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Acerca del modo IE](./edge-ie-mode.md)
- [Información adicional del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
