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
# <span data-ttu-id="6e2f3-103">Cómo usar las opciones de línea de comandos de Microsoft Edge para configurar las opciones del proxy</span><span class="sxs-lookup"><span data-stu-id="6e2f3-103">How to use Microsoft Edge command-line options to configure proxy settings</span></span>

<span data-ttu-id="6e2f3-104">En este artículo se describe cómo usar las opciones de línea de comandos para invalidar la configuración de red predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-104">This article describes how you can use command-line options to override the default system network settings.</span></span>

>[!NOTE]
><span data-ttu-id="6e2f3-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="6e2f3-106">Configuración de red del sistema</span><span class="sxs-lookup"><span data-stu-id="6e2f3-106">System network settings</span></span>

<span data-ttu-id="6e2f3-107">La pila de red de Microsoft Edge usa la configuración de red del sistema de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-107">The Microsoft Edge network stack uses the system network settings by default.</span></span> <span data-ttu-id="6e2f3-108">Estas configuraciones incluyen *configuración de proxy* y *almacenes de certificados y claves privadas*.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-108">These settings include *proxy settings*, and *certificate and private key stores*.</span></span>

<span data-ttu-id="6e2f3-109">Hay escenarios en los que los usuarios solicitan una alternativa al uso de la configuración de proxy predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-109">There are scenarios where users request an alternative to using the system's default proxy settings.</span></span> <span data-ttu-id="6e2f3-110">Para admitir estos escenarios, Microsoft Edge admite opciones de línea de comandos que puedes usar para configurar las opciones personalizadas del proxy.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-110">To support these scenarios, Microsoft Edge supports command-line options that you can use to configure custom proxy settings.</span></span>

<span data-ttu-id="6e2f3-111">Estas opciones de línea de comandos se corresponden con las siguientes directivas del grupo **Servidor proxy**:</span><span class="sxs-lookup"><span data-stu-id="6e2f3-111">These command-line options correspond to the following policies in the **Proxy server** group:</span></span>

- [<span data-ttu-id="6e2f3-112">ProxyBypassList</span><span class="sxs-lookup"><span data-stu-id="6e2f3-112">ProxyBypassList</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist)
- [<span data-ttu-id="6e2f3-113">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="6e2f3-113">ProxyMode</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [<span data-ttu-id="6e2f3-114">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="6e2f3-114">ProxyPacUrl</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl)
- [<span data-ttu-id="6e2f3-115">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="6e2f3-115">ProxyServer</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver)
- [<span data-ttu-id="6e2f3-116">ProxySettings</span><span class="sxs-lookup"><span data-stu-id="6e2f3-116">ProxySettings</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxysettings)

## <span data-ttu-id="6e2f3-117">Opciones de línea de comandos para la configuración del proxy</span><span class="sxs-lookup"><span data-stu-id="6e2f3-117">Command-line options for proxy settings</span></span>

<span data-ttu-id="6e2f3-118">Microsoft Edge admite las siguientes opciones de línea de comandos relacionadas con el proxy.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-118">Microsoft Edge supports the following proxy-related command-line options.</span></span>

 **`--no-proxy-server`**
 
<span data-ttu-id="6e2f3-119">Indica a Microsoft Edge no usar proxy, incluso si el sistema está configurado para usar uno.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-119">Tells Microsoft Edge not to use a Proxy, even if the system is otherwise configured to use one.</span></span> <span data-ttu-id="6e2f3-120">Invalida cualquier otra configuración de proxy que se proporcione.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-120">It overrides any other proxy settings that are provided.</span></span>

**`--proxy-auto-detect`**

<span data-ttu-id="6e2f3-121">Indica a Mircrosoft Edge que intente detectar automáticamente la configuración de proxy.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-121">Tells Microsoft Edge to try and automatically detect your proxy configuration.</span></span> <span data-ttu-id="6e2f3-122">Este argumento se omite si está configurado `--proxy-server`.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-122">This argument is ignored if `--proxy-server` is configured.</span></span>

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

<span data-ttu-id="6e2f3-123">Indica a Microsoft Edge que use una configuración de proxy personalizada.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-123">Tells Microsoft Edge to use a custom proxy configuration.</span></span> <span data-ttu-id="6e2f3-124">Puedes especificar una configuración de proxy personalizada de tres maneras.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-124">You can specify a custom proxy configuration in three ways.</span></span>

1. <span data-ttu-id="6e2f3-125">Proporciona una asignación separada por punto y coma del esquema de lista a los pares url/puerto.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-125">Provide a semicolon-separated mapping of list scheme to url/port pairs.</span></span> <span data-ttu-id="6e2f3-126">Por ejemplo, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` indica a Microsoft Edge que use el proxy HTTP "proxy1:8080" para las direcciones URL http y las direcciones URL de proxy HTTP "ftpproxy: 80" para ftp.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-126">For example, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` tells Microsoft Edge to use HTTP proxy "proxy1:8080" for http URLs and HTTP proxy "ftpproxy:80" for ftp URLs.</span></span>
2. <span data-ttu-id="6e2f3-127">Proporciona un único uri con un puerto opcional para usar para todas las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-127">By providing a single uri with optional port to use for all URLs.</span></span> <span data-ttu-id="6e2f3-128">Por ejemplo, `--proxy-server="proxy2:8080"` usará el proxy en "proxy2:8080" para todo el tráfico.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-128">For example, `--proxy-server="proxy2:8080"` will use the proxy at "proxy2:8080" for all traffic.</span></span>
3. <span data-ttu-id="6e2f3-129">Mediante el valor especial "direct://".</span><span class="sxs-lookup"><span data-stu-id="6e2f3-129">By using the special "direct://" value.</span></span> <span data-ttu-id="6e2f3-130">Por ejemplo, `--proxy-server="direct://"` hará que todas las conexiones no usen un proxy.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-130">For example, `--proxy-server="direct://"` will make all connections not use a proxy.</span></span> 

>[!NOTE]
><span data-ttu-id="6e2f3-131">Puedes configurar Microsoft Edge para intentar usar un proxy y su reserva para ir directamente si el proxy no está disponible.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-131">You can configure Microsoft Edge to try using a proxy and fallback to going direct if the proxy isn't available.</span></span> <span data-ttu-id="6e2f3-132">Por ejemplo, `--proxy-server="http://proxy2:8080,direct://`.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-132">For example, `--proxy-server="http://proxy2:8080,direct://`.</span></span>

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

<span data-ttu-id="6e2f3-133">Indica a Microsoft Edge que ignore cualquier proxy especificado para la lista de hosts especificados separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-133">Tells Microsoft Edge to bypass any specified proxy for the specified semicolon-separated list of hosts.</span></span> <span data-ttu-id="6e2f3-134">Esta marca debe usarse con `--proxy-server`.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-134">This flag must be used with `--proxy-server`.</span></span>

>[!NOTE]
><span data-ttu-id="6e2f3-135">La coincidencia de dominio final no requiere separadores "." y "\*microsoft.com" coincidirá con "imicrosoft.com".</span><span class="sxs-lookup"><span data-stu-id="6e2f3-135">Trailing-domain matching doesn't require "." separators, "\*microsoft.com" will match "imicrosoft.com".</span></span> <span data-ttu-id="6e2f3-136">Por ejemplo, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` usará el servidor proxy "proxy2" en el puerto 8080 para todos los hosts, excepto las solicitudes de \*.microsoft.com, example.com y 127.0.0.1 en el puerto 8080.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-136">For example, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` will use the proxy server "proxy2" on port 8080 for all hosts except requests for \*.microsoft.com, example.com, and 127.0.0.1 on port 8080.</span></span> <span data-ttu-id="6e2f3-137">En el ejemplo anterior, las solicitudes de imicrosoft.com seguirán con proxy.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-137">In the previous example, imicrosoft.com requests will still be proxied.</span></span> <span data-ttu-id="6e2f3-138">Sin embargo, las solicitudes de iexample.com omitirán el proxy por haberse especificado \*example.com en lugar de \*.example.com.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-138">However, iexample.com requests will bypass the proxy because \*example.com was specified instead of \*.example.com.</span></span>

**`--proxy-pac-url=<pac-file-url>`**

<span data-ttu-id="6e2f3-139">Indica a Microsoft Edge que use el archivo PAC en la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-139">Tells Microsoft Edge to use the PAC file at the specified URL.</span></span> <span data-ttu-id="6e2f3-140">Por ejemplo, `--proxy-pac-url="https://wpad/proxy.pac"` indica a Microsoft Edge que resuelva la información de proxy de las solicitudes de direcciones URL usando el archivo **proxy.pac**.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-140">For example, `--proxy-pac-url="https://wpad/proxy.pac"` tells Microsoft Edge to resolve proxy information for URL requests using the **proxy.pac** file.</span></span>

## <span data-ttu-id="6e2f3-141">Licencia de contenido</span><span class="sxs-lookup"><span data-stu-id="6e2f3-141">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="6e2f3-142">Algunas partes de esta página son modificaciones que se basan en trabajo creado y compartido por Chromium.org y que se usan de acuerdo con los términos descritos en la [Licencia internacional de Creative Commons Atribution 4.0](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="6e2f3-142">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="6e2f3-143">La página original se puede encontrar [aquí](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).</span><span class="sxs-lookup"><span data-stu-id="6e2f3-143">The original page can be found [here](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="6e2f3-144">Este trabajo dispone de licencia conforme a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licencia internacional de Creative Commons Attribution 4.0</a>.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-144">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <span data-ttu-id="6e2f3-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6e2f3-145">See also</span></span>

- <span data-ttu-id="6e2f3-146">Para ver las opciones de configuración avanzadas y otras opciones, consulta la [documentación de proxy](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) en el proyecto de código abierto Chromium.</span><span class="sxs-lookup"><span data-stu-id="6e2f3-146">To see advanced configuration settings and additional options, consult the [proxy documentation](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) in the Chromium Open Source project.</span></span>
- [<span data-ttu-id="6e2f3-147">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="6e2f3-147">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
