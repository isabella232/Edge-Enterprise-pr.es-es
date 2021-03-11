---
title: Documentación de directiva de WebView2 de Microsoft Edge
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 03/10/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentación de Windows y Mac para todas las directivas admitidas por Explorador Microsoft Edge
ms.openlocfilehash: 47072c6e39944bb51fd4c683a9597125d8776d08
ms.sourcegitcommit: e3762b1a204c143b4e2264100affae3d9ddaaffc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/11/2021
ms.locfileid: "11406361"
---
# <a name="microsoft-edge-webview2---policies"></a>Microsoft Edge WebView2: directivas

La versión más reciente de Microsoft Edge WebView2 incluye las siguientes directivas. Puede usar estas directivas para configurar cómo se ejecuta Microsoft Edge WebView2 en su organización.

Para obtener información sobre un conjunto adicional de directivas usadas para controlar cómo y cuándo se actualiza Microsoft Edge WebView2, vea la [referencia de directiva de actualización de Microsoft Edge](microsoft-edge-update-policies.md).

> [!NOTE]
> Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.

## <a name="available-policies"></a>Directivas disponibles

En estas tablas se muestran todas las directivas de grupo disponibles en esta versión de Microsoft Edge WebView2. Usa los vínculos de la tabla para obtener más detalles sobre directivas específicas.

- [Configuración de invalidación de Loader](#loader-override-settings)


### [*<a name="loader-override-settings"></a>Configuración de invalidación de Loader*](#loader-override-settings-policies)

|Nombre de directiva|Título|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Configure la ubicación de la carpeta ejecutable del explorador|
|[ReleaseChannelPreference](#releasechannelpreference)|Establezca las preferencias de pedido de búsqueda de canal de publicación|




  ## <a name="loader-override-settings-policies"></a>Directivas de configuración de invalidación de Loader

  [Volver al principio](#microsoft-edge-webview2---policies)

  ### <a name="browserexecutablefolder"></a>BrowserExecutableFolder

  #### <a name="configure-the-location-of-the-browser-executable-folder"></a>Configure la ubicación de la carpeta ejecutable del explorador

  
  
  #### <a name="supported-versions"></a>Versiones compatibles:

  - En Windows desde la versión 87 o posterior

  #### <a name="description"></a>Descripción

  Esta directiva configura las aplicaciones de WebView2 para usar el tiempo de ejecución de WebView2 en la ruta de acceso especificada. La carpeta debe contener los siguientes archivos: msedgewebview2. exe, msedge. dll, etc.

Para establecer el valor de la ruta de acceso de la carpeta, especifique un par de valor y nombre de valor. Configure el nombre de valor en el ID. del modelo de usuario de la aplicación o en el nombre del archivo ejecutable. Puede usar el carácter comodín "*" como nombre de valor para aplicar a todas las aplicaciones.

  #### <a name="supported-features"></a>Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### <a name="data-type"></a>Tipo de datos:

  - Lista de cadenas

  #### <a name="windows-information-and-settings"></a>Información y configuración de Windows

  ##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)

  - Nombre único de GP: BrowserExecutableFolder
  - Nombre GP: configure la ubicación de la carpeta ejecutable del explorador.
  - Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge WebView2/Loader cambiar configuración
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo ADMX de GP: MSEdgeWebView2. ADMX

  ##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows

  - Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: lista de REG_SZ
  - Tipo de valor: lista de REG_SZ

  ##### <a name="example-value"></a>Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [Volver al principio](#microsoft-edge-webview2---policies)

  ### <a name="releasechannelpreference"></a>ReleaseChannelPreference

  #### <a name="set-the-release-channel-search-order-preference"></a>Establezca las preferencias de pedido de búsqueda de canal de publicación

  
  
  #### <a name="supported-versions"></a>Versiones compatibles:

  - En Windows desde la versión 87 o posterior

  #### <a name="description"></a>Descripción

  El orden de búsqueda por canal predeterminado es WebView2 Runtime, Beta, Dev y Canarias.

Para invertir el orden de búsqueda predeterminado, establezca esta directiva en 1.

Para establecer el valor de las preferencias de canal de liberación, especifique un nombre de valor y un par de valores. Configure el nombre de valor en el ID. del modelo de usuario de la aplicación o en el nombre del archivo ejecutable. Puede usar el carácter comodín "*" como nombre de valor para aplicar a todas las aplicaciones.

  #### <a name="supported-features"></a>Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### <a name="data-type"></a>Tipo de datos:

  - Lista de cadenas

  #### <a name="windows-information-and-settings"></a>Información y configuración de Windows

  ##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)

  - Nombre único de GP: ReleaseChannelPreference
  - Nombre GP: establecer el canal de lanzamiento de preferencias de pedido de búsqueda
  - Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge WebView2/Loader cambiar configuración
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo ADMX de GP: MSEdgeWebView2. ADMX

  ##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows

  - Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: lista de REG_SZ
  - Tipo de valor: lista de REG_SZ

  ##### <a name="example-value"></a>Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [Volver al principio](#microsoft-edge-webview2---policies)


## <a name="see-also"></a>Consulte también

- [Configuración de Microsoft Edge](configure-microsoft-edge.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Blog de líneas de base de seguridad de Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)