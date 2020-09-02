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
ms.openlocfilehash: 5a0eff1ca7be17fccd1087716d426b13ea302847
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981135"
---
# <span data-ttu-id="e1384-103">Formato de filtro para directivas basadas en listas de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="e1384-103">Filter format for URL list-based policies</span></span>

<span data-ttu-id="e1384-104">En este artículo se describe el formato de filtro que se usa para las directivas basadas en listas de direcciones URL de Microsoft Edge (por ejemplo, las directivas [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) y [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).</span><span class="sxs-lookup"><span data-stu-id="e1384-104">This article describes the filter format used for the Microsoft Edge URL list-based policies (For example, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist), and [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) policies.</span></span>

> [!NOTE]
> <span data-ttu-id="e1384-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e1384-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="e1384-106">Formato de filtro</span><span class="sxs-lookup"><span data-stu-id="e1384-106">The filter format</span></span>

<span data-ttu-id="e1384-107">El formato de filtro es:</span><span class="sxs-lookup"><span data-stu-id="e1384-107">The filter format is:</span></span>

```
    [scheme://][.]host[:port][/path][@query]
```

<span data-ttu-id="e1384-108">Los campos del formato de filtro son:</span><span class="sxs-lookup"><span data-stu-id="e1384-108">The fields in the filter format are:</span></span>

| <span data-ttu-id="e1384-109">Campo</span><span class="sxs-lookup"><span data-stu-id="e1384-109">Field</span></span> | <span data-ttu-id="e1384-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1384-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="e1384-111">**esquema** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="e1384-111">**scheme** (*optional*)</span></span> | <span data-ttu-id="e1384-112">Puede ser http://, https://, ftp://, edge://, etc.</span><span class="sxs-lookup"><span data-stu-id="e1384-112">It can be http://, https://, ftp://, edge://, etc.</span></span> |
| <span data-ttu-id="e1384-113">**host** (*obligatorio*)</span><span class="sxs-lookup"><span data-stu-id="e1384-113">**host** (*required*)</span></span> | <span data-ttu-id="e1384-114">Debe ser un nombre de host o una dirección IP válidos y se puede usar un carácter comodín ("\*").</span><span class="sxs-lookup"><span data-stu-id="e1384-114">It must be a valid host name or IP address and you can use a wildcard ("\*").</span></span> <span data-ttu-id="e1384-115">Para deshabilitar la coincidencia de subdominios, incluye un punto opcional (".") antes de **host**.</span><span class="sxs-lookup"><span data-stu-id="e1384-115">To disable subdomain matching, include an optional dot (".") before **host**.</span></span> |
| <span data-ttu-id="e1384-116">**puerto** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="e1384-116">**port** (*optional*)</span></span> | <span data-ttu-id="e1384-117">Los valores válidos van de 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="e1384-117">Valid values range from 1 to 65535.</span></span> |
| <span data-ttu-id="e1384-118">**ruta** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="e1384-118">**path** (*optional*)</span></span> | <span data-ttu-id="e1384-119">Puedes usar cualquier cadena de la ruta.</span><span class="sxs-lookup"><span data-stu-id="e1384-119">You can use any string in the path.</span></span> |
| <span data-ttu-id="e1384-120">**consulta** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="e1384-120">**query** (*optional*)</span></span> | <span data-ttu-id="e1384-121">La **consulta** es un valor clave o tokens solo de clave separados por un signo ampersand ("&").</span><span class="sxs-lookup"><span data-stu-id="e1384-121">The **query** is either key-value or key-only tokens separated by an ampersand ("&").</span></span> <span data-ttu-id="e1384-122">Separa los tokens de valor clave con un signo igual ("=").</span><span class="sxs-lookup"><span data-stu-id="e1384-122">Separate key-value tokens with an equal sign ("=").</span></span> <span data-ttu-id="e1384-123">Para indicar una coincidencia de prefijo, puedes usar un asterisco ("\*") al final de la **consulta**.</span><span class="sxs-lookup"><span data-stu-id="e1384-123">To indicate a prefix match, you can use an asterisk ("\*") at the end of the **query**.</span></span> |

## <span data-ttu-id="e1384-124">Comparación del formato de filtro con el formato de dirección URL</span><span class="sxs-lookup"><span data-stu-id="e1384-124">Comparing the filter format to the URL format</span></span>

<span data-ttu-id="e1384-125">El formato de filtro se asemeja al formato de la dirección URL, excepto en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e1384-125">The filter format resembles the URL format, except for the following differences:</span></span>

- <span data-ttu-id="e1384-126">Si incluyes "user:pass", se ignorará.</span><span class="sxs-lookup"><span data-stu-id="e1384-126">If you include "user:pass", it will be ignored.</span></span> <span data-ttu-id="e1384-127">Por ejemplo, http://user:pass@ftp.contoso.com/pub/example.iso.</span><span class="sxs-lookup"><span data-stu-id="e1384-127">For example, http://user:pass@ftp.contoso.com/pub/example.iso.</span></span>
- <span data-ttu-id="e1384-128">Si incluyes un identificador de fragmento ("#"), el propio identificador y todo lo que le sigue se ignora.</span><span class="sxs-lookup"><span data-stu-id="e1384-128">If you include a fragment identifier ("#"), it and everything that follows the identifier is ignored.</span></span>
- <span data-ttu-id="e1384-129">Puedes usar un carácter comodín ("\*") como **host** y puedes poner un prefijo de un punto (".").</span><span class="sxs-lookup"><span data-stu-id="e1384-129">You can use a wildcard ("\*") as the **host** and you can prefix it with a dot (".").</span></span>
- <span data-ttu-id="e1384-130">Puedes usar una barra diagonal ("/") o un punto (".") como sufijo del **host**.</span><span class="sxs-lookup"><span data-stu-id="e1384-130">You can use a forward slash ("/") or a dot (".") as a suffix for the **host**.</span></span> <span data-ttu-id="e1384-131">En este caso, se ignora el sufijo.</span><span class="sxs-lookup"><span data-stu-id="e1384-131">In this case, the suffix is ignored.</span></span>

## <span data-ttu-id="e1384-132">Criterios de selección de filtros</span><span class="sxs-lookup"><span data-stu-id="e1384-132">Filter selection criteria</span></span>

<span data-ttu-id="e1384-133">El filtro seleccionado para una dirección URL es la coincidencia más específica encontrada después de procesar las siguientes reglas de selección de filtro:</span><span class="sxs-lookup"><span data-stu-id="e1384-133">The filter selected for a URL is the most specific match found after processing the following filter selection rules:</span></span>

1. <span data-ttu-id="e1384-134">En primer lugar, se seleccionan los filtros con la mayor coincidencia de **host**.</span><span class="sxs-lookup"><span data-stu-id="e1384-134">Filters with the longest **host** match are selected first.</span></span>
2. <span data-ttu-id="e1384-135">A partir de los filtros seleccionados, se descartan todos los filtros con esquema o puerto que no coincidan.</span><span class="sxs-lookup"><span data-stu-id="e1384-135">From the selected filters, any filter with a non-matching scheme or port is discarded.</span></span>
3. <span data-ttu-id="e1384-136">Desde los filtros restantes, se selecciona el filtro con coincidencia de **ruta** más larga.</span><span class="sxs-lookup"><span data-stu-id="e1384-136">From the remaining filters, the filter with the longest matching **path** is selected.</span></span>
4. <span data-ttu-id="e1384-137">A partir de los filtros restantes, se selecciona el filtro con los tokens de consulta más largos.</span><span class="sxs-lookup"><span data-stu-id="e1384-137">From the remaining filters, the filter with the longest set of query tokens is selected.</span></span> <span data-ttu-id="e1384-138">En este paso, el filtro de la lista de permitidos tiene prioridad sobre el filtro de la lista de bloqueados si ambos filtros tienen la misma longitud de **ruta** y número de tokens de **consulta**.</span><span class="sxs-lookup"><span data-stu-id="e1384-138">At this step, the allow list filter takes precedence over the block list filter if both filters have the same **path** length and number of **query** tokens.</span></span>
5. <span data-ttu-id="e1384-139">Si no queda ningún filtro válido, el subdominio que está más a la izquierda se quita del **host** y el proceso de selección comienza de nuevo en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="e1384-139">If there's no valid filter remaining, then the left-most subdomain is removed from **host** and the selection process starts over at step 1.</span></span> <span data-ttu-id="e1384-140">El **host** de asterisco especial ("\*") es el último buscado y coincide con todos los hosts.</span><span class="sxs-lookup"><span data-stu-id="e1384-140">The special asterisk ("\*") **host** is the last searched and it matches all hosts.</span></span>
6. <span data-ttu-id="e1384-141">Si un filtro está disponible, bloquea o permite la solicitud de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e1384-141">If a filter's available, it blocks or allows the URL request.</span></span>

   >[!NOTE]
   ><span data-ttu-id="e1384-142">El comportamiento predeterminado es permitir la solicitud de dirección URL si no coincide con ningún filtro.</span><span class="sxs-lookup"><span data-stu-id="e1384-142">The default behavior is to allow the URL request if no filter is matched.</span></span>

## <span data-ttu-id="e1384-143">Ejemplo de criterios de selección de filtros</span><span class="sxs-lookup"><span data-stu-id="e1384-143">Example filter selection criteria</span></span>

<span data-ttu-id="e1384-144">En este ejemplo, al buscar una coincidencia con "https://sub.contoso.com/docs", la selección de filtros hará lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e1384-144">In this example, when searching for a match to "https://sub.contoso.com/docs" the filter selection will:</span></span>

1. <span data-ttu-id="e1384-145">Busca un filtro para "sub.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="e1384-145">Search for a filter for "sub.contoso.com".</span></span> <span data-ttu-id="e1384-146">Si encuentra un filtro, la búsqueda pasa al paso 2.</span><span class="sxs-lookup"><span data-stu-id="e1384-146">If it finds a filter, the search moves to step 2.</span></span> <span data-ttu-id="e1384-147">Si no se encuentra un filtro, entonces intenta de nuevo con "contoso.com", "com" y, finalmente, "".</span><span class="sxs-lookup"><span data-stu-id="e1384-147">If a filter isn't found, then it tries again with "contoso.com", "com", and finally "".</span></span>
2. <span data-ttu-id="e1384-148">Desde los filtros seleccionados, se quitan los que no tengan "http" en el **esquema**.</span><span class="sxs-lookup"><span data-stu-id="e1384-148">From the selected filters, any that don't have "http" in the **scheme** are removed.</span></span>
3. <span data-ttu-id="e1384-149">De los filtros restantes, se quitan los que tengan un número de puerto exacto que no sea "80".</span><span class="sxs-lookup"><span data-stu-id="e1384-149">From the remaining filters, any that have an exact port number that isn't "80" are removed.</span></span>
4. <span data-ttu-id="e1384-150">De los filtros restantes, se quitan los que no tengan "/docs" como prefijo de la **ruta**.</span><span class="sxs-lookup"><span data-stu-id="e1384-150">From the remaining filters, any that don't have "/docs" as a prefix of the **path** are removed.</span></span>
5. <span data-ttu-id="e1384-151">De los filtros restantes, se selecciona y aplica el filtro con el prefijo de ruta más larga.</span><span class="sxs-lookup"><span data-stu-id="e1384-151">From the remaining filters, the filter with the longest path prefix is selected and applied.</span></span> <span data-ttu-id="e1384-152">Si no se encuentra ningún filtro, el proceso de selección vuelve a iniciarse en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="e1384-152">If a filter isn't found, the selection process starts over again at step 1.</span></span> <span data-ttu-id="e1384-153">El proceso se repite con el siguiente subdominio.</span><span class="sxs-lookup"><span data-stu-id="e1384-153">The process is repeated with the next subdomain.</span></span>

### <span data-ttu-id="e1384-154">Información adicional de filtros</span><span class="sxs-lookup"><span data-stu-id="e1384-154">Additional filter information</span></span>

<span data-ttu-id="e1384-155">Si un filtro tiene un punto (".") como prefijo del **host**, solo se filtran las coincidencias exactas de **host**.</span><span class="sxs-lookup"><span data-stu-id="e1384-155">If a filter has a dot (".") prefixing the **host** then only exact **host** matches are filtered.</span></span> <span data-ttu-id="e1384-156">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e1384-156">For example:</span></span>

- <span data-ttu-id="e1384-157">"contoso.com" (sin punto) coincidirá con "contoso.com", "www.contoso.com" y "sub.www.contoso.com"</span><span class="sxs-lookup"><span data-stu-id="e1384-157">"contoso.com" (no dot) will match "contoso.com", "www.contoso.com", and "sub.www.contoso.com"</span></span>
- <span data-ttu-id="e1384-158">".www.contoso.com" (con un prefijo de punto) solo coincidirá con "www.contoso.com"</span><span class="sxs-lookup"><span data-stu-id="e1384-158">".www.contoso.com" (with a dot prefix) will only match "www.contoso.com"</span></span>

<span data-ttu-id="e1384-159">Puedes usar un **esquema** estándar o de cliente.</span><span class="sxs-lookup"><span data-stu-id="e1384-159">You can use either a standard or customer **schema**.</span></span> <span data-ttu-id="e1384-160">Entre los esquemas de estándares admitidos se encuentran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e1384-160">Supported standard schemas include:</span></span>

- <span data-ttu-id="e1384-161">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_ y _wss_.</span><span class="sxs-lookup"><span data-stu-id="e1384-161">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, and _wss_.</span></span>

<span data-ttu-id="e1384-162">Cualquier otro **esquema** se trata como un **esquema** personalizado, pero solo se permiten los patrones _schema:\*_ y _schema://\*_.</span><span class="sxs-lookup"><span data-stu-id="e1384-162">Any other **schema** is treated as a custom **schema**, but only the _schema:\*_ and _schema://\*_ patterns are allowed.</span></span> <span data-ttu-id="e1384-163">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e1384-163">For example:</span></span>

- <span data-ttu-id="e1384-164">"custom:*" o "custom://*" coincidirán con "custom:app"</span><span class="sxs-lookup"><span data-stu-id="e1384-164">"custom:*" or "custom://*" will match "custom:app"</span></span>
- <span data-ttu-id="e1384-165">"custom:app" o "custom://app" no son válidos</span><span class="sxs-lookup"><span data-stu-id="e1384-165">"custom:app" or "custom://app" are invalid</span></span>

<span data-ttu-id="e1384-166">**esquema** y **host** no distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e1384-166">**schema** and **host** aren't case-sensitive.</span></span> <span data-ttu-id="e1384-167">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e1384-167">For example:</span></span>

- <span data-ttu-id="e1384-168">El filtro "http://contoso.com" coincide con "HTTP://contoso.com", "http://contoso.COM" y "http://contoso.com"</span><span class="sxs-lookup"><span data-stu-id="e1384-168">"http://contoso.com" filter matches "HTTP://contoso.com", "http://contoso.COM", and "http://contoso.com"</span></span>

<span data-ttu-id="e1384-169">**ruta** y **consulta** distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e1384-169">**path** and **query** are case-sensitive.</span></span> <span data-ttu-id="e1384-170">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e1384-170">For example:</span></span>

- <span data-ttu-id="e1384-171">El filtro "http://contoso.com/path?query=A" no coincide con "http://contoso.com/Path?query=A" o "http://contoso.com/path?Query=A".</span><span class="sxs-lookup"><span data-stu-id="e1384-171">"http://contoso.com/path?query=A" filter doesn't match "http://contoso.com/Path?query=A" or "http://contoso.com/path?Query=A".</span></span> <span data-ttu-id="e1384-172">Coincide con "http://contoso.COM/path?query=A".</span><span class="sxs-lookup"><span data-stu-id="e1384-172">It does match "http://contoso.COM/path?query=A".</span></span>

## <span data-ttu-id="e1384-173">Licencia de contenido</span><span class="sxs-lookup"><span data-stu-id="e1384-173">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="e1384-174">Algunas partes de esta página son modificaciones que se basan en trabajo creado y compartido por Chromium.org y que se usan de acuerdo con los términos descritos en la [Licencia internacional de Creative Commons Atribution 4.0](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="e1384-174">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="e1384-175">La [página original de Chromium se puede encontrar aquí](https://www.chromium.org/administrators/url-blacklist-filter-format).</span><span class="sxs-lookup"><span data-stu-id="e1384-175">The original [Chromium page can be found here](https://www.chromium.org/administrators/url-blacklist-filter-format).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="e1384-176">Este trabajo dispone de licencia conforme a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licencia internacional de Creative Commons Attribution 4.0</a>.</span><span class="sxs-lookup"><span data-stu-id="e1384-176">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <span data-ttu-id="e1384-177">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e1384-177">See also</span></span>

- [<span data-ttu-id="e1384-178">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="e1384-178">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
