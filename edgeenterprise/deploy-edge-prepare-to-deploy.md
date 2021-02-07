---
title: Microsoft Edge en tu entorno
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge en tu entorno
ms.openlocfilehash: e1418d21ff9e541d83d5b86baf5ff25c50d2299d
ms.sourcegitcommit: 16a92a51560fdba6f6480e4533453348f026c7ef
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313966"
---
# <span data-ttu-id="534cb-103">Microsoft Edge en tu entorno</span><span class="sxs-lookup"><span data-stu-id="534cb-103">Microsoft Edge in your environment</span></span>

<span data-ttu-id="534cb-104">En este artículo se describe cómo preparar la implementación de Microsoft Edge cuando Microsoft Edge (versión anterior) llegue al final del servicio.</span><span class="sxs-lookup"><span data-stu-id="534cb-104">This article describes how to prepare to deploy Microsoft Edge when Microsoft Edge Legacy reaches its end of service.</span></span>

<span data-ttu-id="534cb-105">Según la [entrada de blog](https://aka.ms/EdgeLegacyEOS) del equipo de productos de Microsoft Edge, la compatibilidad con la aplicación de escritorio Microsoft Edge (versión anterior) finalizará el 9 de marzo de 2021.</span><span class="sxs-lookup"><span data-stu-id="534cb-105">As per the Microsoft Edge Product Team’s [blog post](https://aka.ms/EdgeLegacyEOS), support for the Microsoft Edge Legacy desktop application will end on March 9, 2021.</span></span> <span data-ttu-id="534cb-106">Cuando apliques la versión de la actualización del martes (o "B") de abril, se eliminará Microsoft Edge (versión anterior) de los dispositivos que ejecuten desde Windows 10 RS4 a 20H1 y se sustituirá por Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="534cb-106">When you apply the Update Tuesday (or "B") release in April, it will remove Microsoft Edge Legacy from devices running Windows 10 RS4 through 20H1 and replace it with Microsoft Edge.</span></span>

## <span data-ttu-id="534cb-107">Cómo prepararse</span><span class="sxs-lookup"><span data-stu-id="534cb-107">How to Prepare</span></span>

<span data-ttu-id="534cb-108">Para prepararse para la instalación de Microsoft Edge en los dispositivos de Windows 10 RS4 a 20H1 con la versión de la actualización del martes de abril, recomendamos leer [Planificar tu implementación de Microsoft Edge](deploy-edge-plan-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="534cb-108">To prepare for Microsoft Edge being installed on Windows 10 RS4 through 20H1 devices with the Update Tuesday release in April, we recommend reading [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md).</span></span>

<span data-ttu-id="534cb-109">Después de planificar tu implementación, usa uno de los siguientes métodos para preparar la implementación de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="534cb-109">After you plan your deployment, use one of the following approaches to prepare to deploy Microsoft Edge.</span></span>

- <span data-ttu-id="534cb-110">**Instala directivas de grupo para personalizar tu enfoque de actualización de Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="534cb-110">**Install group policies to customize your Microsoft Edge update approach**.</span></span> <span data-ttu-id="534cb-111">Para obtener más información, ve [Configurar las opciones de directiva de Microsoft Edge en Windows](configure-microsoft-edge.md) y presta especial atención al material de [Referencia de la directiva de actualización](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="534cb-111">For more information, see [Configure Microsoft Edge policy settings on Windows](configure-microsoft-edge.md), and pay special attention to the [Update Policy reference](microsoft-edge-update-policies.md) material.</span></span> <span data-ttu-id="534cb-112">Si instalas directivas de grupo para administrar tus actualizaciones antes de instalar la versión de la actualización del martes de abril, Microsoft Edge empezará a respetar inmediatamente tu política.</span><span class="sxs-lookup"><span data-stu-id="534cb-112">If you install group policies to manage your updates before installing April’s Update Tuesday release, Microsoft Edge will immediately start respecting your policy.</span></span> <span data-ttu-id="534cb-113">Si no hay ninguna directiva de grupo instalada, Microsoft Edge se actualizará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="534cb-113">If there isn't any installed group policy, Microsoft Edge will automatically update itself.</span></span>

- <span data-ttu-id="534cb-114">**Quita la aplicación de escritorio de Microsoft Edge (versión anterior) antes de su fecha de finalización del servicio del 9 de marzo de 2021 e implementa Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="534cb-114">**Remove the Microsoft Edge Legacy desktop application before its end of service date of March 9, 2021 and deploy Microsoft Edge**.</span></span> <span data-ttu-id="534cb-115">Para Windows 10 RS4 a 20H1, puedes hacerlo mediante actualizaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="534cb-115">For Windows 10 RS4 through 20H1, you can do this by using Windows Updates.</span></span> <span data-ttu-id="534cb-116">Para obtener más información, ve [Implementar Microsoft Edge con actualizaciones de Windows 10](deploy-edge-with-windows-10-updates.md).</span><span class="sxs-lookup"><span data-stu-id="534cb-116">For more information, see [Deploy Microsoft Edge with Windows 10 updates](deploy-edge-with-windows-10-updates.md).</span></span>

## <span data-ttu-id="534cb-117">Ve también</span><span class="sxs-lookup"><span data-stu-id="534cb-117">See also</span></span>

- [<span data-ttu-id="534cb-118">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="534cb-118">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="534cb-119">Planear tu implementación de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="534cb-119">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)