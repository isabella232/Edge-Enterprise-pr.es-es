---
title: Documentación de directiva de WebView2 de Microsoft Edge
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 11/13/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentación de Windows y Mac para todas las directivas admitidas por Explorador Microsoft Edge
ms.openlocfilehash: 3a4d7aa66622baacc5719ec411190d4f88a083ce
ms.sourcegitcommit: 2b6808a4d1878fd2da886f9c6c56f592c6b200e1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/13/2020
ms.locfileid: "11168755"
---
# Microsoft Edge WebView2: directivas

La versión más reciente de Microsoft Edge WebView2 incluye las siguientes directivas. Puede usar estas directivas para configurar cómo se ejecuta Microsoft Edge WebView2 en su organización.

Para obtener información sobre un conjunto adicional de directivas usadas para controlar cómo y cuándo se actualiza Microsoft Edge WebView2, vea la [referencia de directiva de actualización de Microsoft Edge](microsoft-edge-update-policies.md).


> [!NOTE]
> Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.

## Directivas disponibles

En estas tablas se muestran todas las directivas de grupo disponibles en esta versión de Microsoft Edge WebView2. Usa los vínculos de la tabla para obtener más detalles sobre directivas específicas.

|||
|-|-|
|[Configuración de invalidación de Loader](#loader-override-settings)|

### [*Configuración de invalidación de Loader*](#loader-override-settings-policies)

|Nombre de directiva|Título|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Configure la ubicación de la carpeta ejecutable del explorador|
|[ReleaseChannelPreference](#releasechannelpreference)|Establezca las preferencias de pedido de búsqueda de canal de publicación|




  ## Directivas de configuración de invalidación de Loader

  [Volver al principio](#microsoft-edge-webview2---policies)

  ### BrowserExecutableFolder

  #### Configure la ubicación de la carpeta ejecutable del explorador

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 87 o posterior

  #### Descripción

  Esta directiva configura las aplicaciones de WebView2 para usar el tiempo de ejecución de WebView2 en la ruta de acceso especificada. La carpeta debe contener los siguientes archivos: msedgewebview2. exe, msedge. dll, etc.

Para establecer el valor de la ruta de acceso de la carpeta, especifique un par de valor y nombre de valor. Configure el nombre de valor en el ID. del modelo de usuario de la aplicación o en el nombre del archivo ejecutable. Puede usar el carácter comodín "*" como nombre de valor para aplicar a todas las aplicaciones.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: BrowserExecutableFolder
  - Nombre GP: configure la ubicación de la carpeta ejecutable del explorador.
  - Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge WebView2/Loader cambiar configuración
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo ADMX de GP: MSEdgeWebView2. ADMX

  ##### Configuración del Registro de Windows

  - Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: lista de REG_SZ
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [Volver al principio](#microsoft-edge-webview2---policies)

  ### ReleaseChannelPreference

  #### Establezca las preferencias de pedido de búsqueda de canal de publicación

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 87 o posterior

  #### Descripción

  El orden de búsqueda por canal predeterminado es WebView2 Runtime, Beta, Dev y Canarias.

Para invertir el orden de búsqueda predeterminado, establezca esta directiva en 1.

Para establecer el valor de las preferencias de canal de liberación, especifique un nombre de valor y un par de valores. Configure el nombre de valor en el ID. del modelo de usuario de la aplicación o en el nombre del archivo ejecutable. Puede usar el carácter comodín "*" como nombre de valor para aplicar a todas las aplicaciones.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ReleaseChannelPreference
  - Nombre GP: establecer el canal de lanzamiento de preferencias de pedido de búsqueda
  - Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge WebView2/Loader cambiar configuración
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo ADMX de GP: MSEdgeWebView2. ADMX

  ##### Configuración del Registro de Windows

  - Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: lista de REG_SZ
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [Volver al principio](#microsoft-edge-webview2---policies)


## Consulte también

- [Configuración de Microsoft Edge](configure-microsoft-edge.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Blog de líneas de base de seguridad de Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)