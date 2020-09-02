---
title: Configuraciones y experimentación de Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configuraciones y experimentación de Microsoft Edge
ms.openlocfilehash: f66da4075c33c1f375dfb593c1a1bd2b4a139833
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981100"
---
# <span data-ttu-id="83761-103">Configuraciones y experimentación de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="83761-103">Microsoft Edge configurations and experimentation</span></span>

<span data-ttu-id="83761-104">En este artículo se describe la interacción entre Microsoft Edge y el servicio de experimentación y configuración (ECS).</span><span class="sxs-lookup"><span data-stu-id="83761-104">This article describes the interaction between Microsoft Edge and the Experimentation and Configuration Service (ECS).</span></span> <span data-ttu-id="83761-105">Microsoft Edge se comunica con este servicio para solicitar y recibir distintos tipos de cargas.</span><span class="sxs-lookup"><span data-stu-id="83761-105">Microsoft Edge communicates with this service to request and receive different kinds of payloads.</span></span> <span data-ttu-id="83761-106">Estas cargas incluyen configuraciones, implementaciones de funciones y experimentos.</span><span class="sxs-lookup"><span data-stu-id="83761-106">These payloads include configurations, feature rollouts, and experiments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83761-107">Asegúrese de que los clientes puedan obtener acceso a `https://config.edge.skype.com` para poder recibir cargas.</span><span class="sxs-lookup"><span data-stu-id="83761-107">Make sure clients are able to access `https://config.edge.skype.com` so payloads can be received.</span></span>

> [!NOTE]
> <span data-ttu-id="83761-108">Esto se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="83761-108">This applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="83761-109">Configuraciones</span><span class="sxs-lookup"><span data-stu-id="83761-109">Configurations</span></span>

<span data-ttu-id="83761-110">Las configuraciones son la carga pensada para garantizar el cumplimiento del estado, la seguridad y la privacidad del producto, y tienen el mismo valor para todos los usuarios (en función de las plataformas y los canales). Esto podría ser habilitar una marca de función para una acción de dominio, y también puede usarse para deshabilitar una marca de función en el caso de un error.</span><span class="sxs-lookup"><span data-stu-id="83761-110">Configurations are the payload meant to ensure product health, security, and privacy compliance, and are intended to have the same value for all the users (based on platforms and channels.) This could be to enable a feature flag for a domain action, and can also be used to disable a feature flag in the event of a bug.</span></span>

## <span data-ttu-id="83761-111">Lanzamiento de funciones controladas</span><span class="sxs-lookup"><span data-stu-id="83761-111">Controlled Feature Rollout</span></span>

<span data-ttu-id="83761-112">La implementación de funciones controlada (CFR) es un procedimiento para aumentar lentamente el tamaño del grupo de usuarios que recibe una función.</span><span class="sxs-lookup"><span data-stu-id="83761-112">Controlled Feature Rollout (CFR) is a procedure for slowly increasing the size of the user group that receives a feature.</span></span> <span data-ttu-id="83761-113">Al distribuir una nueva función a un subconjunto seleccionado aleatoriamente de la población de usuarios, es posible comparar los comentarios de los usuarios con un grupo de controles de igual tamaño sin la característica para medir el impacto de la función.</span><span class="sxs-lookup"><span data-stu-id="83761-113">By distributing a new feature to a randomly selected subset of the user population, it’s possible to compare user feedback to an equally sized control group without the feature to measure the impact of the feature.</span></span>

## <span data-ttu-id="83761-114">Experimentos</span><span class="sxs-lookup"><span data-stu-id="83761-114">Experiments</span></span>

<span data-ttu-id="83761-115">Las compilaciones de Microsoft Edge tienen características y funciones que aún están en desarrollo o que son experimentales.</span><span class="sxs-lookup"><span data-stu-id="83761-115">Microsoft Edge builds have features and functionality that are still in development or are experimental.</span></span> <span data-ttu-id="83761-116">Los experimentos son como CFR, pero el tamaño del grupo de usuarios es mucho más pequeño para probar el nuevo concepto.</span><span class="sxs-lookup"><span data-stu-id="83761-116">Experiments are like CFR, but the size of the user group is much smaller for testing the new concept.</span></span> <span data-ttu-id="83761-117">Estas funciones se ocultan de manera predeterminada hasta que se lanza la función o finaliza el experimento.</span><span class="sxs-lookup"><span data-stu-id="83761-117">These features are hidden by default until the feature's rolled out or the experiment's finished.</span></span> <span data-ttu-id="83761-118">Las marcas de experimento se usan para habilitar y deshabilitar estas funciones.</span><span class="sxs-lookup"><span data-stu-id="83761-118">Experiment flags are used to enable and disable these features.</span></span>

## <span data-ttu-id="83761-119">Acerca del ECS</span><span class="sxs-lookup"><span data-stu-id="83761-119">About the ECS</span></span>

<span data-ttu-id="83761-120">En todos los escenarios anteriores, el servicio proporciona los valores de marca de funciones al cliente del explorador, para que puedan aplicarse.</span><span class="sxs-lookup"><span data-stu-id="83761-120">In all the preceding scenarios, the service delivers the feature flag values to the browser client so they can be applied.</span></span> <span data-ttu-id="83761-121">En función de la actualización, las configuraciones se aplican inmediatamente o cuando el usuario reinicia el explorador.</span><span class="sxs-lookup"><span data-stu-id="83761-121">Depending on the update, configurations are applied immediately or when the user restarts the browser.</span></span>

<span data-ttu-id="83761-122">La interacción de Microsoft Edge con este servicio se controla mediante la configuración de la directiva [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol).</span><span class="sxs-lookup"><span data-stu-id="83761-122">Microsoft Edge's interaction with this service is controlled by settings in the [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) policy.</span></span> <span data-ttu-id="83761-123">Puedes configurar las opciones de directiva para:</span><span class="sxs-lookup"><span data-stu-id="83761-123">You can configure policy settings to:</span></span>

- <span data-ttu-id="83761-124">Solo recuperar configuraciones</span><span class="sxs-lookup"><span data-stu-id="83761-124">Retrieve configurations only</span></span>
- <span data-ttu-id="83761-125">Recuperar configuraciones y experimentos</span><span class="sxs-lookup"><span data-stu-id="83761-125">Retrieve configurations and experiments</span></span>
- <span data-ttu-id="83761-126">Deshabilitar la comunicación con el servicio</span><span class="sxs-lookup"><span data-stu-id="83761-126">Disable communication with the service</span></span>

  > [!CAUTION]
  > <span data-ttu-id="83761-127">Si deshabilitas las comunicaciones con el servicio, esto afectará a la capacidad de Microsoft para responder a un error grave de manera puntual.</span><span class="sxs-lookup"><span data-stu-id="83761-127">If you disable communications with the service, this will affect Microsoft’s ability to respond to a severe bug in a timely manner.</span></span>

## <span data-ttu-id="83761-128">Consulta también</span><span class="sxs-lookup"><span data-stu-id="83761-128">See also</span></span>

- [<span data-ttu-id="83761-129">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="83761-129">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="83761-130">Página de aterrizaje de documentación de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="83761-130">Microsoft Edge documentation landing page</span></span>](https://docs.microsoft.com/DeployEdge/)
