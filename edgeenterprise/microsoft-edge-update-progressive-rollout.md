---
title: Implementación progresiva para actualizaciones del canal estable de Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Implementación progresiva para actualizaciones del canal estable de Microsoft Edge
ms.openlocfilehash: bdcefdc118125d67057fa77513bd732cff6882e3
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642296"
---
# <a name="progressive-rollouts-for-microsoft-edge-stable-channel-updates"></a><span data-ttu-id="755ad-103">Implementación progresiva para actualizaciones del canal estable de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="755ad-103">Progressive rollouts for Microsoft Edge Stable channel updates</span></span>

<span data-ttu-id="755ad-104">A partir de la versión 83 de Microsoft Edge, realizaremos implementaciones graduales de las actualizaciones principales en el canal estable de Microsoft Edge en un lapso de pocos días.</span><span class="sxs-lookup"><span data-stu-id="755ad-104">Starting with Microsoft Edge 83 release, we will perform gradual rollouts of major updates to Microsoft Edge Stable channel over the span of a few days.</span></span> <span data-ttu-id="755ad-105">Este lanzamiento progresivo nos permite supervisar las actualizaciones y actualizar el explorador de forma segura en toda la organización.</span><span class="sxs-lookup"><span data-stu-id="755ad-105">This progressive rollout allows us to monitor upgrades and safely update the browser across the organization.</span></span>

> [!NOTE]
> <span data-ttu-id="755ad-106">Esto aplica a la versión 83 o posterior del canal estable de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="755ad-106">This applies to Microsoft Edge Stable channel version 83 or later.</span></span>

## <a name="why-do-we-need-progressive-rollout"></a><span data-ttu-id="755ad-107">¿Por qué necesitamos la implementación progresiva?</span><span class="sxs-lookup"><span data-stu-id="755ad-107">Why do we need progressive rollout?</span></span>

<span data-ttu-id="755ad-108">Al supervisar el estado de nuestras actualizaciones de manera cercana y llevar a cabo las actualizaciones a lo largo de varios días, podemos limitar el impacto de los problemas que se pueden producir en la nueva actualización.</span><span class="sxs-lookup"><span data-stu-id="755ad-108">By monitoring the health of our updates closely and rolling out the updates over the course of several days, we can limit the impact of issues that might occur with the new update.</span></span> <span data-ttu-id="755ad-109">Con la versión 83 de Microsoft Edge, las implementaciones progresivas se habilitarán para todas las versiones de Microsoft Edge para Windows 7, Windows 8 y 8.1, y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="755ad-109">With Microsoft Edge release 83, Progressive Rollouts will be enabled for all Windows 7, Windows 8 & 8.1, and Windows 10 versions of Microsoft Edge.</span></span> <span data-ttu-id="755ad-110">Ofreceremos soporte técnico de Microsoft Edge en Mac tan pronto como esté listo.</span><span class="sxs-lookup"><span data-stu-id="755ad-110">We will support Microsoft Edge on Mac as soon as it is ready.</span></span>

## <a name="how-will-the-updates-work"></a><span data-ttu-id="755ad-111">¿Cómo funcionan las actualizaciones?</span><span class="sxs-lookup"><span data-stu-id="755ad-111">How will the updates work?</span></span>

<span data-ttu-id="755ad-112">Cada instalación de Microsoft Edge se asigna a un valor de actualización.</span><span class="sxs-lookup"><span data-stu-id="755ad-112">Each installation of Microsoft Edge is assigned an upgrade value.</span></span> <span data-ttu-id="755ad-113">Cuando comencemos con las implementaciones, verá la actualización cuando el valor de su dispositivo se encuentre dentro del intervalo de valores de actualización.</span><span class="sxs-lookup"><span data-stu-id="755ad-113">When we start rolling out incrementally, you'll see the update when the value on your device falls within the upgrade value range.</span></span> <span data-ttu-id="755ad-114">A medida que progresa la implementación (en pocos días), todos los usuarios obtendrán la actualización.</span><span class="sxs-lookup"><span data-stu-id="755ad-114">As the rollout progresses (within a few days), all users will eventually get the update.</span></span> <span data-ttu-id="755ad-115">Las actualizaciones del explorador con correcciones de seguridad críticas tendrán una cadencia de lanzamiento más rápida que las actualizaciones que no tengan correcciones de seguridad importantes.</span><span class="sxs-lookup"><span data-stu-id="755ad-115">Browser updates with critical security fixes will have a faster rollout cadence than updates that don't have critical security fixes.</span></span> <span data-ttu-id="755ad-116">Esto se lleva a cabo para asegurar la protección inmediata frente a las vulnerabilidades.</span><span class="sxs-lookup"><span data-stu-id="755ad-116">This is done to ensure prompt protection from vulnerabilities.</span></span>

## <a name="how-does-this-affect-enterprises"></a><span data-ttu-id="755ad-117">¿Cómo afecta esto a las empresas?</span><span class="sxs-lookup"><span data-stu-id="755ad-117">How does this affect enterprises?</span></span>

<span data-ttu-id="755ad-118">Los artefactos de Microsoft Edge se distribuyen a las empresas a través de varios mecanismos, como Microsoft Intune, Windows Server Update Services (WSUS) y Administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="755ad-118">Microsoft Edge artifacts are distributed to enterprises using multiple mechanisms such as Microsoft Intune, Windows Server Update Service (WSUS), and Configuration Manager.</span></span> <span data-ttu-id="755ad-119">Estas herramientas de implementación se comportan de manera diferente en lo que respecta al lanzamiento progresivo:</span><span class="sxs-lookup"><span data-stu-id="755ad-119">These deployment tools behave differently with respect to Progressive Rollout:</span></span>

- <span data-ttu-id="755ad-120">Las empresas que administran la distribución mediante Microsoft Intune se registran para actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="755ad-120">Enterprises that manage distribution via Microsoft Intune are registered for auto-updates.</span></span> <span data-ttu-id="755ad-121">Se usa la implementación progresiva y todos los usuarios verán una actualización en unos días.</span><span class="sxs-lookup"><span data-stu-id="755ad-121">Progressive Rollout is used, and all the users will see an update in a few days.</span></span>
- <span data-ttu-id="755ad-122">Las empresas que administran la distribución mediante WSUS (Windows Server Update Services) o Administrador de configuración no están registradas para las actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="755ad-122">Enterprises that manage distribution through WSUS (Windows Server Update Services) or Configuration Manager are not registered for auto-updates.</span></span> <span data-ttu-id="755ad-123">Los administradores pueden administrar y aplicar las actualizaciones que estarán disponibles desde el principio.</span><span class="sxs-lookup"><span data-stu-id="755ad-123">Administrators manage and apply the updates that will be available from the start.</span></span> <span data-ttu-id="755ad-124">El lanzamiento progresivo no afecta a este proceso.</span><span class="sxs-lookup"><span data-stu-id="755ad-124">Progressive Rollout does not affect this process.</span></span>

<span data-ttu-id="755ad-125">Comparta sus valiosos comentarios a través de la opción de voz, el botón comentarios en la aplicación, o, sino, debajo de los comentarios, en caso de que tenga alguna duda o consulta.</span><span class="sxs-lookup"><span data-stu-id="755ad-125">Please share your valuable feedback through user voice, the in-application feedback button, or below in the comments if you have any concerns or questions.</span></span>

## <a name="see-also"></a><span data-ttu-id="755ad-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="755ad-126">See also</span></span>

- [<span data-ttu-id="755ad-127">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="755ad-127">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
