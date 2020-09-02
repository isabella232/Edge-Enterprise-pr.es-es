---
title: Microsoft Edge y sitios configurables en modo IE
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/28/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge y sitios configurables en modo IE
ms.openlocfilehash: a846d71d63a4f837041acc9b601f704999bb826a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981188"
---
# <span data-ttu-id="008a4-103">Obtenga información sobre los sitios configurables en modo IE</span><span class="sxs-lookup"><span data-stu-id="008a4-103">Learn about Configurable sites in IE mode</span></span>

<span data-ttu-id="008a4-104">En este artículo, se explica la característica de sitios configurables de la lista de sitios del Modo de empresa al usar el modo IE en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="008a4-104">This article explains the Configurable sites feature of the Enterprise Mode Site List when using IE mode in Microsoft Edge.</span></span>

## <span data-ttu-id="008a4-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="008a4-105">Prerequisites</span></span>

- <span data-ttu-id="008a4-106">Actualizaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="008a4-106">Windows updates</span></span>

  - <span data-ttu-id="008a4-107">Windows 10, versión 1909; Windows Server, versión 1909 (KB4550945 o superior)</span><span class="sxs-lookup"><span data-stu-id="008a4-107">Windows 10 version 1909, Windows server version 1909 – KB4550945  or higher</span></span>
  - <span data-ttu-id="008a4-108">Windows 10, versión 1903; Windows Server, versión 1903 (KB4550945 o superior)</span><span class="sxs-lookup"><span data-stu-id="008a4-108">Windows 10 version 1903, Windows server version 1903 – KB4550945  or higher</span></span>
  - <span data-ttu-id="008a4-109">Windows 10, versión 1809; Windows Server, versión 1809, y Windows Server 2019 (KB4550969 o superior)</span><span class="sxs-lookup"><span data-stu-id="008a4-109">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4550969 or higher</span></span>
  - <span data-ttu-id="008a4-110">Windows 10, versión 1803 (KB4550944 o superior)</span><span class="sxs-lookup"><span data-stu-id="008a4-110">Windows 10 version 1803 – KB4550944 or higher</span></span>
  - <span data-ttu-id="008a4-111">Windows 10, versión 1607; Windows Server 2016 (KB4556826 o superior)</span><span class="sxs-lookup"><span data-stu-id="008a4-111">Windows 10 version 1607, Windows Server 2016 - KB4556826 or higher</span></span>
  - <span data-ttu-id="008a4-112">Versión inicial de Windows 10, julio de 2015 (KB4550947 o superior)</span><span class="sxs-lookup"><span data-stu-id="008a4-112">Windows 10 initial version, July 2015 - KB4550947 or higher</span></span>
  - <span data-ttu-id="008a4-113">Windows 8.1 (KB4556798 o superior)</span><span class="sxs-lookup"><span data-stu-id="008a4-113">Windows 8.1 – KB4556798 or higher</span></span>

- <span data-ttu-id="008a4-114">Microsoft Edge, versión 83 o posterior</span><span class="sxs-lookup"><span data-stu-id="008a4-114">Microsoft Edge version 83 or later</span></span>
- <span data-ttu-id="008a4-115">[Modo IE](https://aka.ms/iemodeonedge) configurado con la lista de sitios del Modo de empresa</span><span class="sxs-lookup"><span data-stu-id="008a4-115">[IE mode](https://aka.ms/iemodeonedge) configured with Enterprise Mode Site List</span></span>

## <span data-ttu-id="008a4-116">Introducción</span><span class="sxs-lookup"><span data-stu-id="008a4-116">Overview</span></span>

<span data-ttu-id="008a4-117">La configuración de sitios que necesitan el modo IE en la lista de sitios del Modo de empresa funcionará correctamente para la mayoría de los entornos con aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="008a4-117">Configuring sites needing IE mode in the Enterprise Mode Site List will work well for most environments with legacy applications.</span></span> <span data-ttu-id="008a4-118">Sin embargo, en algunos casos, este método no es el más adecuado para configurar un subconjunto de sitios para abrirlo en modo IE sin representar un dominio completo en modo IE.</span><span class="sxs-lookup"><span data-stu-id="008a4-118">However, in some cases this approach isn't the best to configure a subset of sites to open in IE mode without rendering an entire domain in IE mode.</span></span> <span data-ttu-id="008a4-119">Por ejemplo, este método no es el más adecuado cuando el entorno contiene tanto aplicaciones modernas como heredadas que se ejecutan en un único servidor y usted quiere tener flexibilidad para representar en modo IE solo las aplicaciones heredadas, y para representar las aplicaciones restantes en el modo de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="008a4-119">For example, when your environment contains both modern and legacy applications running on a single server and you would like the flexibility to render only the legacy applications in IE mode and the remaining applications to render in Microsoft Edge mode.</span></span>

<span data-ttu-id="008a4-120">La solución consiste en usar la característica de sitios configurables de la lista de sitios del Modo de empresa.</span><span class="sxs-lookup"><span data-stu-id="008a4-120">The solution is to use the Configurable sites feature of the Enterprise Mode Site List.</span></span> <span data-ttu-id="008a4-121">Cuando la característica está habilitada, Microsoft Edge permite a los sitios con la etiqueta "configurable" participar en la determinación del motor en modo IE.</span><span class="sxs-lookup"><span data-stu-id="008a4-121">When the feature is enabled, Microsoft Edge will allow sites with the "configurable" tag to participate in IE mode engine determination.</span></span>

## <span data-ttu-id="008a4-122">Funcionamiento de los sitios configurables</span><span class="sxs-lookup"><span data-stu-id="008a4-122">How Configurable sites works</span></span>

### <span data-ttu-id="008a4-123">Cambio automático del motor de Microsoft Edge al motor en modo IE</span><span class="sxs-lookup"><span data-stu-id="008a4-123">Automatic switching from the Microsoft Edge engine to the IE mode engine</span></span>

<span data-ttu-id="008a4-124">Para usar la característica de sitios configurables, necesitará uno o más sitios de la lista de sitios del Modo de empresa para tener la opción `<open-in>Configurable</open-in>`.</span><span class="sxs-lookup"><span data-stu-id="008a4-124">To use the Configurable sites feature, you'll need one or more sites in the Enterprise Mode Site List to have the `<open-in>Configurable</open-in>` option.</span></span>

<span data-ttu-id="008a4-125">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="008a4-125">Example:</span></span>

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

<span data-ttu-id="008a4-126">Cuando la característica de sitios configurables está habilitada, sucede lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="008a4-126">When the Configurable sites feature is enabled, the following behavior occurs:</span></span>

1. <span data-ttu-id="008a4-127">Cuando se realiza una solicitud a un sitio configurable, Microsoft Edge envía el encabezado de solicitud HTTP "`X-InternetExplorerModeConfigurable: 1`".</span><span class="sxs-lookup"><span data-stu-id="008a4-127">When making a request to a Configurable site, Microsoft Edge will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`".</span></span>
2. <span data-ttu-id="008a4-128">Es posible que un sitio configurable envíe una respuesta de redirección (por ejemplo, HTTP 302) con el encabezado de respuesta HTTP "`X-InternetExplorerMode: 1`", para solicitar que Microsoft Edge cargue el sitio en modo IE.</span><span class="sxs-lookup"><span data-stu-id="008a4-128">A Configurable site may send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 1`" to request that Microsoft Edge loads the site in IE mode.</span></span>
3. <span data-ttu-id="008a4-129">El destino del redireccionamiento (es decir, el valor del encabezado de respuesta de **Ubicación**) también tiene que ser un sitio **Configurable** o **Neutro**; de lo contrario, el encabezado de respuesta en modo IE se omitirá.</span><span class="sxs-lookup"><span data-stu-id="008a4-129">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="008a4-130">Por lo general, se espera que el destino del redireccionamiento sea el mismo que la dirección URL original.</span><span class="sxs-lookup"><span data-stu-id="008a4-130">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="008a4-131">Sin embargo, no tiene por qué ser así necesariamente.</span><span class="sxs-lookup"><span data-stu-id="008a4-131">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="008a4-132">La respuesta de redirección está sujeta al almacenamiento en caché, según el comportamiento normal de almacenamiento en caché de HTTP de Microsoft Edge para redirecciones.</span><span class="sxs-lookup"><span data-stu-id="008a4-132">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

### <span data-ttu-id="008a4-133">Volver a cambiar el motor del modo IE al motor de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="008a4-133">Switching back from IE mode engine to Microsoft Edge engine</span></span>

<span data-ttu-id="008a4-134">Al habilitar los sitios configurables en Microsoft Edge, se habilitan automáticamente los siguientes comportamientos en las pestañas del modo IE:</span><span class="sxs-lookup"><span data-stu-id="008a4-134">Enabling Configurable sites in Microsoft Edge automatically enables the following behaviors in IE mode tabs:</span></span>

1. <span data-ttu-id="008a4-135">Al realizar una solicitud a un sitio configurable, las pestañas del modo IE envían el encabezado de solicitud HTTP "`X-InternetExplorerModeConfigurable: 1`", al igual que las pestañas de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="008a4-135">When making a request to a Configurable site, IE mode tabs will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`", the same as Microsoft Edge tabs.</span></span>
2. <span data-ttu-id="008a4-136">Es posible que un sitio configurable envíe una respuesta de redirección (por ejemplo, HTTP 302) con el encabezado de respuesta HTTP "`X-InternetExplorerMode: 0`", para solicitar que la navegación vuelva al modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="008a4-136">A Configurable site might send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 0`" to request that the navigation switch back to Microsoft Edge mode.</span></span>
3. <span data-ttu-id="008a4-137">El destino del redireccionamiento (es decir, el valor del encabezado de respuesta de **Ubicación**) también tiene que ser un sitio **Configurable** o **Neutro**; de lo contrario, el encabezado de respuesta en modo IE se omitirá.</span><span class="sxs-lookup"><span data-stu-id="008a4-137">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="008a4-138">Por lo general, se espera que el destino del redireccionamiento sea el mismo que la dirección URL original.</span><span class="sxs-lookup"><span data-stu-id="008a4-138">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="008a4-139">Sin embargo, no tiene por qué ser así necesariamente.</span><span class="sxs-lookup"><span data-stu-id="008a4-139">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="008a4-140">La respuesta de redirección está sujeta al almacenamiento en caché, según el comportamiento normal de almacenamiento en caché de HTTP de Microsoft Edge para redirecciones.</span><span class="sxs-lookup"><span data-stu-id="008a4-140">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

> [!TIP]
> <span data-ttu-id="008a4-141">Ambos motores de exploración envían el mismo encabezado de solicitud "`X-InternetExplorerModeConfigurable: 1`" a sitios configurables.</span><span class="sxs-lookup"><span data-stu-id="008a4-141">Both browser engines send the same "`X-InternetExplorerModeConfigurable: 1`" request header to Configurable sites.</span></span> <span data-ttu-id="008a4-142">Debe usar el encabezado de solicitud de agente de usuario para distinguir las solicitudes del modo de Microsoft Edge de las del modo IE, para evitar el redireccionamiento cuando el sitio ya se está cargando en el motor adecuado.</span><span class="sxs-lookup"><span data-stu-id="008a4-142">You should use the User-Agent request header to distinguish between requests from Microsoft Edge mode vs. IE mode to avoid redirecting when the site is already loading in the correct engine.</span></span>

## <span data-ttu-id="008a4-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="008a4-143">See also</span></span>

- [<span data-ttu-id="008a4-144">Acerca del modo IE</span><span class="sxs-lookup"><span data-stu-id="008a4-144">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="008a4-145">Información adicional del modo de empresa</span><span class="sxs-lookup"><span data-stu-id="008a4-145">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="008a4-146">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="008a4-146">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)