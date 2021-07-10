---
title: Formato de filtro para directivas de direcciones URL de Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Obtén información sobre el formato de filtro usado para las directivas URLBlocklist y URLAllowlist de Microsoft Edge.
ms.openlocfilehash: e178dad518ff4bee07bf89d9faca3231ee6cf246
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642026"
---
# <a name="filter-format-for-url-list-based-policies"></a><span data-ttu-id="ca61b-103">Formato de filtro para directivas basadas en listas de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="ca61b-103">Filter format for URL list-based policies</span></span>

<span data-ttu-id="ca61b-104">En este artículo se describe el formato de filtro que se usa para las directivas basadas en listas de direcciones URL de Microsoft Edge (por ejemplo, las directivas [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) y [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).</span><span class="sxs-lookup"><span data-stu-id="ca61b-104">This article describes the filter format used for the Microsoft Edge URL list-based policies (For example, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist), and [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) policies.</span></span>

> [!NOTE]
> <span data-ttu-id="ca61b-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ca61b-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="the-filter-format"></a><span data-ttu-id="ca61b-106">Formato de filtro</span><span class="sxs-lookup"><span data-stu-id="ca61b-106">The filter format</span></span>

<span data-ttu-id="ca61b-107">El formato de filtro es:</span><span class="sxs-lookup"><span data-stu-id="ca61b-107">The filter format is:</span></span>

```
    [scheme://][.]host[:port][/path][@query]
```

<span data-ttu-id="ca61b-108">Los campos del formato de filtro son:</span><span class="sxs-lookup"><span data-stu-id="ca61b-108">The fields in the filter format are:</span></span>

| <span data-ttu-id="ca61b-109">Campo</span><span class="sxs-lookup"><span data-stu-id="ca61b-109">Field</span></span> | <span data-ttu-id="ca61b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca61b-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="ca61b-111">**esquema** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="ca61b-111">**scheme** (*optional*)</span></span> | <span data-ttu-id="ca61b-112">Puede ser http://, https://, ftp://, edge://, etc.</span><span class="sxs-lookup"><span data-stu-id="ca61b-112">It can be http://, https://, ftp://, edge://, etc.</span></span> |
| <span data-ttu-id="ca61b-113">**host** (*obligatorio*)</span><span class="sxs-lookup"><span data-stu-id="ca61b-113">**host** (*required*)</span></span> | <span data-ttu-id="ca61b-114">Debe ser un nombre de host válido y puede usar un carácter comodín ("\*").</span><span class="sxs-lookup"><span data-stu-id="ca61b-114">It must be a valid host name and you can use a wildcard ("\*").</span></span> <span data-ttu-id="ca61b-115">Para deshabilitar la coincidencia de subdominios, incluya un punto opcional (".") antes del **host**.</span><span class="sxs-lookup"><span data-stu-id="ca61b-115">To disable subdomain matching, include an optional dot (".") before **host**.</span></span> <span data-ttu-id="ca61b-116">Se puede especificar un único nombre de host para un literal de dirección IP, pero no se admiten los caracteres comodín en este caso.</span><span class="sxs-lookup"><span data-stu-id="ca61b-116">A single IP Address Literal hostname may be specified, but wildcarding is not supported for an IP Address Literal hostname.</span></span> |
| <span data-ttu-id="ca61b-117">**puerto** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="ca61b-117">**port** (*optional*)</span></span> | <span data-ttu-id="ca61b-118">Los valores válidos van de 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="ca61b-118">Valid values range from 1 to 65535.</span></span> |
| <span data-ttu-id="ca61b-119">**ruta** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="ca61b-119">**path** (*optional*)</span></span> | <span data-ttu-id="ca61b-120">Puedes usar cualquier cadena de la ruta.</span><span class="sxs-lookup"><span data-stu-id="ca61b-120">You can use any string in the path.</span></span> |
| <span data-ttu-id="ca61b-121">**consulta** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="ca61b-121">**query** (*optional*)</span></span> | <span data-ttu-id="ca61b-122">La **consulta** es un valor clave o tokens solo de clave separados por un signo ampersand ("&").</span><span class="sxs-lookup"><span data-stu-id="ca61b-122">The **query** is either key-value or key-only tokens separated by an ampersand ("&").</span></span> <span data-ttu-id="ca61b-123">Separa los tokens de valor clave con un signo igual ("=").</span><span class="sxs-lookup"><span data-stu-id="ca61b-123">Separate key-value tokens with an equal sign ("=").</span></span> <span data-ttu-id="ca61b-124">Para indicar una coincidencia de prefijo, puedes usar un asterisco ("\*") al final de la **consulta**.</span><span class="sxs-lookup"><span data-stu-id="ca61b-124">To indicate a prefix match, you can use an asterisk ("\*") at the end of the **query**.</span></span> |

## <a name="comparing-the-filter-format-to-the-url-format"></a><span data-ttu-id="ca61b-125">Comparación del formato de filtro con el formato de dirección URL</span><span class="sxs-lookup"><span data-stu-id="ca61b-125">Comparing the filter format to the URL format</span></span>

<span data-ttu-id="ca61b-126">El formato de filtro se asemeja al formato de la dirección URL, excepto en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ca61b-126">The filter format resembles the URL format, except for the following differences:</span></span>

- <span data-ttu-id="ca61b-127">Si incluyes "user:pass", se ignorará.</span><span class="sxs-lookup"><span data-stu-id="ca61b-127">If you include "user:pass", it will be ignored.</span></span> <span data-ttu-id="ca61b-128">Por ejemplo, http://user:pass@ftp.contoso.com/pub/example.iso.</span><span class="sxs-lookup"><span data-stu-id="ca61b-128">For example, http://user:pass@ftp.contoso.com/pub/example.iso.</span></span>
- <span data-ttu-id="ca61b-129">Si incluyes un identificador de fragmento ("#"), el propio identificador y todo lo que le sigue se ignora.</span><span class="sxs-lookup"><span data-stu-id="ca61b-129">If you include a fragment identifier ("#"), it and everything that follows the identifier is ignored.</span></span>
- <span data-ttu-id="ca61b-130">Puedes usar un carácter comodín ("\*") como **host** y puedes poner un prefijo de un punto (".").</span><span class="sxs-lookup"><span data-stu-id="ca61b-130">You can use a wildcard ("\*") as the **host** and you can prefix it with a dot (".").</span></span>
- <span data-ttu-id="ca61b-131">Puedes usar una barra diagonal ("/") o un punto (".") como sufijo del **host**.</span><span class="sxs-lookup"><span data-stu-id="ca61b-131">You can use a forward slash ("/") or a dot (".") as a suffix for the **host**.</span></span> <span data-ttu-id="ca61b-132">En este caso, se ignora el sufijo.</span><span class="sxs-lookup"><span data-stu-id="ca61b-132">In this case, the suffix is ignored.</span></span>

## <a name="filter-selection-criteria"></a><span data-ttu-id="ca61b-133">Criterios de selección de filtros</span><span class="sxs-lookup"><span data-stu-id="ca61b-133">Filter selection criteria</span></span>

<span data-ttu-id="ca61b-134">El filtro seleccionado para una dirección URL es la coincidencia más específica encontrada después de procesar las siguientes reglas de selección de filtro:</span><span class="sxs-lookup"><span data-stu-id="ca61b-134">The filter selected for a URL is the most specific match found after processing the following filter selection rules:</span></span>

1. <span data-ttu-id="ca61b-135">En primer lugar, se seleccionan los filtros con la mayor coincidencia de **host**.</span><span class="sxs-lookup"><span data-stu-id="ca61b-135">Filters with the longest **host** match are selected first.</span></span>
2. <span data-ttu-id="ca61b-136">A partir de los filtros seleccionados, se descartan todos los filtros con esquema o puerto que no coincidan.</span><span class="sxs-lookup"><span data-stu-id="ca61b-136">From the selected filters, any filter with a non-matching scheme or port is discarded.</span></span>
3. <span data-ttu-id="ca61b-137">Desde los filtros restantes, se selecciona el filtro con coincidencia de **ruta** más larga.</span><span class="sxs-lookup"><span data-stu-id="ca61b-137">From the remaining filters, the filter with the longest matching **path** is selected.</span></span>
4. <span data-ttu-id="ca61b-138">A partir de los filtros restantes, se selecciona el filtro con los tokens de consulta más largos.</span><span class="sxs-lookup"><span data-stu-id="ca61b-138">From the remaining filters, the filter with the longest set of query tokens is selected.</span></span> <span data-ttu-id="ca61b-139">En este paso, el filtro de la lista de permitidos tiene prioridad sobre el filtro de la lista de bloqueados si ambos filtros tienen la misma longitud de **ruta** y número de tokens de **consulta**.</span><span class="sxs-lookup"><span data-stu-id="ca61b-139">At this step, the allow list filter takes precedence over the block list filter if both filters have the same **path** length and number of **query** tokens.</span></span>
5. <span data-ttu-id="ca61b-140">Si no queda ningún filtro válido, el subdominio que está más a la izquierda se quita del **host** y el proceso de selección comienza de nuevo en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="ca61b-140">If there's no valid filter remaining, then the left-most subdomain is removed from **host** and the selection process starts over at step 1.</span></span> <span data-ttu-id="ca61b-141">El **host** de asterisco especial ("\*") es el último buscado y coincide con todos los hosts.</span><span class="sxs-lookup"><span data-stu-id="ca61b-141">The special asterisk ("\*") **host** is the last searched and it matches all hosts.</span></span>
6. <span data-ttu-id="ca61b-142">Si un filtro está disponible, bloquea o permite la solicitud de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="ca61b-142">If a filter's available, it blocks or allows the URL request.</span></span>

   >[!NOTE]
   ><span data-ttu-id="ca61b-143">El comportamiento predeterminado es permitir la solicitud de dirección URL si no coincide con ningún filtro.</span><span class="sxs-lookup"><span data-stu-id="ca61b-143">The default behavior is to allow the URL request if no filter is matched.</span></span>

## <a name="example-filter-selection-criteria"></a><span data-ttu-id="ca61b-144">Ejemplo de criterios de selección de filtros</span><span class="sxs-lookup"><span data-stu-id="ca61b-144">Example filter selection criteria</span></span>

<span data-ttu-id="ca61b-145">En este ejemplo, al buscar una coincidencia con "https://sub.contoso.com/docs", la selección de filtros hará lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ca61b-145">In this example, when searching for a match to "https://sub.contoso.com/docs" the filter selection will:</span></span>

1. <span data-ttu-id="ca61b-146">Busca un filtro para "sub.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="ca61b-146">Search for a filter for "sub.contoso.com".</span></span> <span data-ttu-id="ca61b-147">Si encuentra un filtro, la búsqueda pasa al paso 2.</span><span class="sxs-lookup"><span data-stu-id="ca61b-147">If it finds a filter, the search moves to step 2.</span></span> <span data-ttu-id="ca61b-148">Si no se encuentra un filtro, entonces intenta de nuevo con "contoso.com", "com" y, finalmente, "".</span><span class="sxs-lookup"><span data-stu-id="ca61b-148">If a filter isn't found, then it tries again with "contoso.com", "com", and finally "".</span></span>
2. <span data-ttu-id="ca61b-149">Desde los filtros seleccionados, se quitan los que no tengan "http" en el **esquema**.</span><span class="sxs-lookup"><span data-stu-id="ca61b-149">From the selected filters, any that don't have "http" in the **scheme** are removed.</span></span>
3. <span data-ttu-id="ca61b-150">De los filtros restantes, se quitan los que tengan un número de puerto exacto que no sea "80".</span><span class="sxs-lookup"><span data-stu-id="ca61b-150">From the remaining filters, any that have an exact port number that isn't "80" are removed.</span></span>
4. <span data-ttu-id="ca61b-151">De los filtros restantes, se quitan los que no tengan "/docs" como prefijo de la **ruta**.</span><span class="sxs-lookup"><span data-stu-id="ca61b-151">From the remaining filters, any that don't have "/docs" as a prefix of the **path** are removed.</span></span>
5. <span data-ttu-id="ca61b-152">De los filtros restantes, se selecciona y aplica el filtro con el prefijo de ruta más larga.</span><span class="sxs-lookup"><span data-stu-id="ca61b-152">From the remaining filters, the filter with the longest path prefix is selected and applied.</span></span> <span data-ttu-id="ca61b-153">Si no se encuentra ningún filtro, el proceso de selección vuelve a iniciarse en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="ca61b-153">If a filter isn't found, the selection process starts over again at step 1.</span></span> <span data-ttu-id="ca61b-154">El proceso se repite con el siguiente subdominio.</span><span class="sxs-lookup"><span data-stu-id="ca61b-154">The process is repeated with the next subdomain.</span></span>

### <a name="additional-filter-information"></a><span data-ttu-id="ca61b-155">Información adicional de filtros</span><span class="sxs-lookup"><span data-stu-id="ca61b-155">Additional filter information</span></span>

<span data-ttu-id="ca61b-156">Si un filtro tiene un punto (".") como prefijo del **host**, solo se filtran las coincidencias exactas de **host**.</span><span class="sxs-lookup"><span data-stu-id="ca61b-156">If a filter has a dot (".") prefixing the **host** then only exact **host** matches are filtered.</span></span> <span data-ttu-id="ca61b-157">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ca61b-157">For example:</span></span>

- <span data-ttu-id="ca61b-158">"contoso.com" (sin punto) coincidirá con "contoso.com", "www.contoso.com" y "sub.www.contoso.com"</span><span class="sxs-lookup"><span data-stu-id="ca61b-158">"contoso.com" (no dot) will match "contoso.com", "www.contoso.com", and "sub.www.contoso.com"</span></span>
- <span data-ttu-id="ca61b-159">".www.contoso.com" (con un prefijo de punto) solo coincidirá con "www.contoso.com"</span><span class="sxs-lookup"><span data-stu-id="ca61b-159">".www.contoso.com" (with a dot prefix) will only match "www.contoso.com"</span></span>

<span data-ttu-id="ca61b-160">Puedes usar un **esquema** estándar o personalizado.</span><span class="sxs-lookup"><span data-stu-id="ca61b-160">You can use either a standard or custom **schema**.</span></span> <span data-ttu-id="ca61b-161">Entre los esquemas de estándares admitidos, se encuentran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ca61b-161">Supported standard schemas include:</span></span>

- <span data-ttu-id="ca61b-162">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_ y _wss_.</span><span class="sxs-lookup"><span data-stu-id="ca61b-162">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, and _wss_.</span></span>

<span data-ttu-id="ca61b-163">Cualquier otro **esquema** se trata como un **esquema** personalizado, pero solo se permiten los patrones _schema:\*_ y _schema://\*_.</span><span class="sxs-lookup"><span data-stu-id="ca61b-163">Any other **schema** is treated as a custom **schema**, but only the _schema:\*_ and _schema://\*_ patterns are allowed.</span></span> <span data-ttu-id="ca61b-164">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ca61b-164">For example:</span></span>

- <span data-ttu-id="ca61b-165">"custom:\*" o "custom://\*" coincidirán con "custom:app"</span><span class="sxs-lookup"><span data-stu-id="ca61b-165">"custom:\*" or "custom://\*" will match "custom:app"</span></span>
- <span data-ttu-id="ca61b-166">"custom:app" o "custom://app" no son válidos</span><span class="sxs-lookup"><span data-stu-id="ca61b-166">"custom:app" or "custom://app" are invalid</span></span>

<span data-ttu-id="ca61b-167">**esquema** y **host** no distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ca61b-167">**schema** and **host** aren't case-sensitive.</span></span> <span data-ttu-id="ca61b-168">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ca61b-168">For example:</span></span>

- <span data-ttu-id="ca61b-169">El filtro "http://contoso.com" coincide con "HTTP://contoso.com", "http://contoso.COM" y "http://contoso.com"</span><span class="sxs-lookup"><span data-stu-id="ca61b-169">"http://contoso.com" filter matches "HTTP://contoso.com", "http://contoso.COM", and "http://contoso.com"</span></span>

<span data-ttu-id="ca61b-170">**ruta** y **consulta** distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ca61b-170">**path** and **query** are case-sensitive.</span></span> <span data-ttu-id="ca61b-171">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ca61b-171">For example:</span></span>

- <span data-ttu-id="ca61b-172">El filtro "http://contoso.com/path?query=A" no coincide con "http://contoso.com/Path?query=A" o "http://contoso.com/path?Query=A".</span><span class="sxs-lookup"><span data-stu-id="ca61b-172">"http://contoso.com/path?query=A" filter doesn't match "http://contoso.com/Path?query=A" or "http://contoso.com/path?Query=A".</span></span> <span data-ttu-id="ca61b-173">Coincide con "http://contoso.COM/path?query=A".</span><span class="sxs-lookup"><span data-stu-id="ca61b-173">It does match "http://contoso.COM/path?query=A".</span></span>

## <a name="content-license"></a><span data-ttu-id="ca61b-174">Licencia de contenido</span><span class="sxs-lookup"><span data-stu-id="ca61b-174">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="ca61b-175">Algunas partes de esta página son modificaciones que se basan en trabajo creado y compartido por Chromium.org y que se usan de acuerdo con los términos descritos en la [Licencia internacional de Creative Commons Atribution 4.0](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="ca61b-175">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="ca61b-176">La [página original de Chromium se puede encontrar aquí](https://www.chromium.org/administrators/url-blacklist-filter-format).</span><span class="sxs-lookup"><span data-stu-id="ca61b-176">The original [Chromium page can be found here](https://www.chromium.org/administrators/url-blacklist-filter-format).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="ca61b-177">Este trabajo dispone de licencia conforme a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licencia internacional de Creative Commons Attribution 4.0</a>.</span><span class="sxs-lookup"><span data-stu-id="ca61b-177">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca61b-178">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ca61b-178">See also</span></span>

- [<span data-ttu-id="ca61b-179">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ca61b-179">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
