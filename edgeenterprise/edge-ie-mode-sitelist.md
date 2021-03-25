---
title: Configurar sitios en la lista de sitios de modo de empresa
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar la lista de sitios de empresas
ms.openlocfilehash: 9b1943e4d50dcc770b4a634b99ecbd001d1ffbcc
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447654"
---
# <a name="configure-sites-on-the-enterprise-mode-site-list"></a>Configurar sitios en la lista de sitios de modo de empresa

En este artículo se describen los cambios en la lista de sitios de modo de empresa que admiten la configuración de Internet Explorer para Microsoft Edge, versión 77 y posteriores.

Para obtener más información sobre el esquema para el archivo XML de lista de sitios en el modo de empresa, consulte la [Guía de esquema de modo de empresa v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

> [!NOTE]
> Este artículo se aplica a los canales de Microsoft Edge **Estable**, **Beta** y **Dev**, versión 77 o posterior.

## <a name="updated-schema-elements"></a>Elementos de esquema actualizados

En la siguiente tabla se describe el elemento \<open-in app\> añadido a la v.2 del esquema del Modo de empresa:

| **Elemento** | **Descripción** |
| --- | --- |
| \<open-in app="**true**"\> | Un elemento secundario que controla qué explorador se usa para sitios. Este elemento es necesario para los sitios que necesitan **abrirse en IE11**.|

**Por ejemplo:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

La siguiente tabla muestra los posibles valores del elemento \<open-in\>:

| **Valor** | **Descripción** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Abra el sitio en modo IE o en una ventana de IE11 completa. Para habilitar el modo IE, consulte [configurar las directivas de modo IE](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Abre el sitio en una ventana de IE11 completa. |
| **\<open-in\>MSEdge\</open-in\>** | Abre el sitio en Microsoft Edge. |
| **\<open-in\>Ninguno o no especificado\</open-in\>** | Abre el sitio en el explorador predeterminado o en el explorador donde el usuario se desplaza al sitio. |
|**\<open-in\>Configurable\</open-in\>** | Permite al sitio participar en la determinación del motor en modo IE. Para más información, consulte [Información sobre los sitios configurables en modo IE](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> El atributo app=**"true"** solo se reconoce cuando está asociado a _'open-in' IE11_. Agregarlo a los otros elementos 'open-in' no cambiará el comportamiento del explorador.   

## <a name="configure-neutral-sites"></a>Configurar los sitios neutros

Para que el modo de IE funcione correctamente, la autenticación y los servidores de inicio de sesión único tendrán que configurarse explícitamente como sitios neutrales. Si no, las páginas en modo IE intentarán redirigir a Microsoft Edge y se producirá un error de autenticación.

Un sitio neutral usará el explorador en el que se inició el desplazamiento, ya sea en el modo de Microsoft Edge o el modo de IE. La configuración de los sitios neutros garantiza que todas las aplicaciones que utilicen los mismos servidores de autenticación, tanto modernos como heredados, sigan funcionando.

Para configurar sitios neutros, configure la lista desplegable *Abrir en* como "ninguna" en la Herramienta de Administración de Lista de Sitios del Modo de Empresa, o bien actualice el XML de la lista de sitios directamente:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

Para identificar servidores de autenticación, inspeccione el tráfico de red de una aplicación con las herramientas para desarrolladores de IE11. Si necesita más tiempo para identificar los servidores de autenticación, puede configurar una directiva para mantener toda la navegación en la página en modo IE. Para minimizar el uso del modo IE, deshabilite esta configuración una vez que haya identificado y agregado los servidores de autenticación en la lista de sitios. Para obtener más información, consulte [configurar la navegación en la página para permanecer en el modo IE](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).

>[!NOTE]
   >El esquema v. 1 del modo de empresa no se admite para la integración de modo IE. Si estás usando actualmente el esquema v. 1 con Internet Explorer 11, debes actualizar al esquema v. 2. Para obtener más información, consulta [Guía del esquema v.2 del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Acerca del modo IE](./edge-ie-mode.md)
- [Información adicional del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)