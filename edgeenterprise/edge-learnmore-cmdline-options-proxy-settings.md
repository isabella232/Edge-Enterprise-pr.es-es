---
title: Configuración de proxy de Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Usar las opciones de línea de comandos para configurar las opciones del proxy '
ms.openlocfilehash: b5e2326e075ad89481560a6642944a8e88f4daa3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981190"
---
# Cómo usar las opciones de línea de comandos de Microsoft Edge para configurar las opciones del proxy

En este artículo se describe cómo usar las opciones de línea de comandos para invalidar la configuración de red predeterminada del sistema.

>[!NOTE]
>Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## Configuración de red del sistema

La pila de red de Microsoft Edge usa la configuración de red del sistema de manera predeterminada. Estas configuraciones incluyen *configuración de proxy* y *almacenes de certificados y claves privadas*.

Hay escenarios en los que los usuarios solicitan una alternativa al uso de la configuración de proxy predeterminada del sistema. Para admitir estos escenarios, Microsoft Edge admite opciones de línea de comandos que puedes usar para configurar las opciones personalizadas del proxy.

Estas opciones de línea de comandos se corresponden con las siguientes directivas del grupo **Servidor proxy**:

- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl)
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver)
- [ProxySettings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxysettings)

## Opciones de línea de comandos para la configuración del proxy

Microsoft Edge admite las siguientes opciones de línea de comandos relacionadas con el proxy.

 **`--no-proxy-server`**
 
Indica a Microsoft Edge no usar proxy, incluso si el sistema está configurado para usar uno. Invalida cualquier otra configuración de proxy que se proporcione.

**`--proxy-auto-detect`**

Indica a Mircrosoft Edge que intente detectar automáticamente la configuración de proxy. Este argumento se omite si está configurado `--proxy-server`.

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

Indica a Microsoft Edge que use una configuración de proxy personalizada. Puedes especificar una configuración de proxy personalizada de tres maneras.

1. Proporciona una asignación separada por punto y coma del esquema de lista a los pares url/puerto. Por ejemplo, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` indica a Microsoft Edge que use el proxy HTTP "proxy1:8080" para las direcciones URL http y las direcciones URL de proxy HTTP "ftpproxy: 80" para ftp.
2. Proporciona un único uri con un puerto opcional para usar para todas las direcciones URL. Por ejemplo, `--proxy-server="proxy2:8080"` usará el proxy en "proxy2:8080" para todo el tráfico.
3. Mediante el valor especial "direct://". Por ejemplo, `--proxy-server="direct://"` hará que todas las conexiones no usen un proxy. 

>[!NOTE]
>Puedes configurar Microsoft Edge para intentar usar un proxy y su reserva para ir directamente si el proxy no está disponible. Por ejemplo, `--proxy-server="http://proxy2:8080,direct://`.

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

Indica a Microsoft Edge que ignore cualquier proxy especificado para la lista de hosts especificados separados por punto y coma. Esta marca debe usarse con `--proxy-server`.

>[!NOTE]
>La coincidencia de dominio final no requiere separadores "." y "\*microsoft.com" coincidirá con "imicrosoft.com". Por ejemplo, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` usará el servidor proxy "proxy2" en el puerto 8080 para todos los hosts, excepto las solicitudes de \*.microsoft.com, example.com y 127.0.0.1 en el puerto 8080. En el ejemplo anterior, las solicitudes de imicrosoft.com seguirán con proxy. Sin embargo, las solicitudes de iexample.com omitirán el proxy por haberse especificado \*example.com en lugar de \*.example.com.

**`--proxy-pac-url=<pac-file-url>`**

Indica a Microsoft Edge que use el archivo PAC en la dirección URL especificada. Por ejemplo, `--proxy-pac-url="https://wpad/proxy.pac"` indica a Microsoft Edge que resuelva la información de proxy de las solicitudes de direcciones URL usando el archivo **proxy.pac**.

## Licencia de contenido

> [!NOTE]
> Algunas partes de esta página son modificaciones que se basan en trabajo creado y compartido por Chromium.org y que se usan de acuerdo con los términos descritos en la [Licencia internacional de Creative Commons Atribution 4.0](http://creativecommons.org/licenses/by/4.0/). La página original se puede encontrar [aquí](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Este trabajo dispone de licencia conforme a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licencia internacional de Creative Commons Attribution 4.0</a>.

## Consulte también

- Para ver las opciones de configuración avanzadas y otras opciones, consulta la [documentación de proxy](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) en el proyecto de código abierto Chromium.
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
