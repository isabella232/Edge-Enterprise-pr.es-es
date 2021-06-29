---
title: Formato de filtro para directivas de direcciones URL de Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Obtén información sobre el formato de filtro usado para las directivas URLBlocklist y URLAllowlist de Microsoft Edge.
ms.openlocfilehash: 94378a9193269c73a7439dd019d6cb2d6ac547df
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617270"
---
# <a name="filter-format-for-url-list-based-policies"></a>Formato de filtro para directivas basadas en listas de direcciones URL

En este artículo se describe el formato de filtro que se usa para las directivas basadas en listas de direcciones URL de Microsoft Edge (por ejemplo, las directivas [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) y [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="the-filter-format"></a>Formato de filtro

El formato de filtro es:

```
    [scheme://][.]host[:port][/path][@query]
```

Los campos del formato de filtro son:

| Campo | Descripción |
| --- | --- |
| **esquema** (*opcional*) | Puede ser http://, https://, ftp://, edge://, etc. |
| **host** (*obligatorio*) | Debe ser un nombre de host válido y puede usar un carácter comodín ("\*"). Para deshabilitar la coincidencia de subdominios, incluya un punto opcional (".") antes del **host**. Se puede especificar un único nombre de host para un literal de dirección IP, pero no se admiten los caracteres comodín en este caso. |
| **puerto** (*opcional*) | Los valores válidos van de 1 a 65535. |
| **ruta** (*opcional*) | Puedes usar cualquier cadena de la ruta. |
| **consulta** (*opcional*) | La **consulta** es un valor clave o tokens solo de clave separados por un signo ampersand ("&"). Separa los tokens de valor clave con un signo igual ("="). Para indicar una coincidencia de prefijo, puedes usar un asterisco ("\*") al final de la **consulta**. |

## <a name="comparing-the-filter-format-to-the-url-format"></a>Comparación del formato de filtro con el formato de dirección URL

El formato de filtro se asemeja al formato de la dirección URL, excepto en lo siguiente:

- Si incluyes "user:pass", se ignorará. Por ejemplo, http://user:pass@ftp.contoso.com/pub/example.iso.
- Si incluyes un identificador de fragmento ("#"), el propio identificador y todo lo que le sigue se ignora.
- Puedes usar un carácter comodín ("*") como **host** y puedes poner un prefijo de un punto (".").
- Puedes usar una barra diagonal ("/") o un punto (".") como sufijo del **host**. En este caso, se ignora el sufijo.

## <a name="filter-selection-criteria"></a>Criterios de selección de filtros

El filtro seleccionado para una dirección URL es la coincidencia más específica encontrada después de procesar las siguientes reglas de selección de filtro:

1. En primer lugar, se seleccionan los filtros con la mayor coincidencia de **host**.
2. A partir de los filtros seleccionados, se descartan todos los filtros con esquema o puerto que no coincidan.
3. Desde los filtros restantes, se selecciona el filtro con coincidencia de **ruta** más larga.
4. A partir de los filtros restantes, se selecciona el filtro con los tokens de consulta más largos. En este paso, el filtro de la lista de permitidos tiene prioridad sobre el filtro de la lista de bloqueados si ambos filtros tienen la misma longitud de **ruta** y número de tokens de **consulta**.
5. Si no queda ningún filtro válido, el subdominio que está más a la izquierda se quita del **host** y el proceso de selección comienza de nuevo en el paso 1. El **host** de asterisco especial ("*") es el último buscado y coincide con todos los hosts.
6. Si un filtro está disponible, bloquea o permite la solicitud de dirección URL.

   >[!NOTE]
   >El comportamiento predeterminado es permitir la solicitud de dirección URL si no coincide con ningún filtro.

## <a name="example-filter-selection-criteria"></a>Ejemplo de criterios de selección de filtros

En este ejemplo, al buscar una coincidencia con "https://sub.contoso.com/docs", la selección de filtros hará lo siguiente:

1. Busca un filtro para "sub.contoso.com". Si encuentra un filtro, la búsqueda pasa al paso 2. Si no se encuentra un filtro, entonces intenta de nuevo con "contoso.com", "com" y, finalmente, "".
2. Desde los filtros seleccionados, se quitan los que no tengan "http" en el **esquema**.
3. De los filtros restantes, se quitan los que tengan un número de puerto exacto que no sea "80".
4. De los filtros restantes, se quitan los que no tengan "/docs" como prefijo de la **ruta**.
5. De los filtros restantes, se selecciona y aplica el filtro con el prefijo de ruta más larga. Si no se encuentra ningún filtro, el proceso de selección vuelve a iniciarse en el paso 1. El proceso se repite con el siguiente subdominio.

### <a name="additional-filter-information"></a>Información adicional de filtros

Si un filtro tiene un punto (".") como prefijo del **host**, solo se filtran las coincidencias exactas de **host**. Por ejemplo:

- "contoso.com" (sin punto) coincidirá con "contoso.com", "www.contoso.com" y "sub.www.contoso.com"
- ".www.contoso.com" (con un prefijo de punto) solo coincidirá con "www.contoso.com"

Puedes usar un **esquema** estándar o personalizado. Entre los esquemas de estándares admitidos, se encuentran los siguientes:

- _about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_ y _wss_.

Cualquier otro **esquema** se trata como un **esquema** personalizado, pero solo se permiten los patrones _schema:*_ y _schema://*_. Por ejemplo:

- "custom:\*" o "custom://\*" coincidirán con "custom:app"
- "custom:app" o "custom://app" no son válidos

**esquema** y **host** no distinguen entre mayúsculas y minúsculas. Por ejemplo:

- El filtro "http://contoso.com" coincide con "HTTP://contoso.com", "http://contoso.COM" y "http://contoso.com"

**ruta** y **consulta** distinguen entre mayúsculas y minúsculas. Por ejemplo:

- El filtro "http://contoso.com/path?query=A" no coincide con "http://contoso.com/Path?query=A" o "http://contoso.com/path?Query=A". Coincide con "http://contoso.COM/path?query=A".

## <a name="content-license"></a>Licencia de contenido

> [!NOTE]
> Algunas partes de esta página son modificaciones que se basan en trabajo creado y compartido por Chromium.org y que se usan de acuerdo con los términos descritos en la [Licencia internacional de Creative Commons Atribution 4.0](http://creativecommons.org/licenses/by/4.0/). La [página original de Chromium se puede encontrar aquí](https://www.chromium.org/administrators/url-blacklist-filter-format).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Este trabajo dispone de licencia conforme a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licencia internacional de Creative Commons Attribution 4.0</a>.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
