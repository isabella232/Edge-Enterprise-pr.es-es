---
title: Implementar Microsoft Edge con actualizaciones de Windows 10
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Implementar Microsoft Edge con actualizaciones de Windows 10
ms.openlocfilehash: a000e3426792df79d1450c838b7848be10d6b0ca
ms.sourcegitcommit: 16a92a51560fdba6f6480e4533453348f026c7ef
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313965"
---
# <span data-ttu-id="e5639-103">Implementar Microsoft Edge con actualizaciones de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e5639-103">Deploy Microsoft Edge with Windows 10 updates</span></span>

<span data-ttu-id="e5639-104">El artículo proporciona información para los usuarios que están implementando Microsoft Edge con actualizaciones de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e5639-104">The article provides information for users who are deploying Microsoft Edge by using Windows 10 updates.</span></span>

## <span data-ttu-id="e5639-105">Para Windows 10 versión 20H2</span><span class="sxs-lookup"><span data-stu-id="e5639-105">For Windows 10 release 20H2</span></span>

<span data-ttu-id="e5639-106">Windows 10 versión 20H2 ya tiene Microsoft Edge instalado como explorador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e5639-106">Windows 10 version 20H2 already has Microsoft Edge installed as its default browser.</span></span>

## <span data-ttu-id="e5639-107">Para las versiones de Windows 10 RS4 a 20H1</span><span class="sxs-lookup"><span data-stu-id="e5639-107">For Windows 10 releases RS4 through 20H1</span></span>

<span data-ttu-id="e5639-108">Windows Server Update Services (WSUS) tiene actualizaciones para cada versión de Windows 10 desde RS4 a 20H1 que quitarán la aplicación de escritorio de Microsoft Edge (versión anterior) y la reemplazarán por Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e5639-108">Windows Server Update Services (WSUS) has updates for each version of Windows 10 from RS4 through 20H1 that will remove the Microsoft Edge Legacy desktop app and replace it with Microsoft Edge.</span></span> <span data-ttu-id="e5639-109">Para más información, consulta [este artículo de soporte técnico](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c) conocer la actualización de WSUS adecuada para tu versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="e5639-109">For more information, see [this support article](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c) to find out which WSUS update is right for your Windows version.</span></span>

## <span data-ttu-id="e5639-110">Para las versiones de Windows 10 anteriores a RS4 (y Windows 7, 8.1 y versiones anteriores)</span><span class="sxs-lookup"><span data-stu-id="e5639-110">For Windows 10 releases prior to RS4 (and Windows 7, 8.1, and earlier)</span></span>

<span data-ttu-id="e5639-111">Las actualizaciones de Windows para instalar Microsoft Edge no están disponibles para estas versiones.</span><span class="sxs-lookup"><span data-stu-id="e5639-111">Windows updates to install Microsoft Edge aren't available for these versions.</span></span> <span data-ttu-id="e5639-112">Considera otras opciones para implementar Microsoft Edge en estos dispositivos, como [Administrador de configuración](https://docs.microsoft.com/configmgr/apps/deploy-use/deploy-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json) o [Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge/?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json).</span><span class="sxs-lookup"><span data-stu-id="e5639-112">Consider other options for deploying Microsoft Edge to these devices such as [Configuration Manager](https://docs.microsoft.com/configmgr/apps/deploy-use/deploy-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json) or [Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge/?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json).</span></span>

## <span data-ttu-id="e5639-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e5639-113">See also</span></span>

- [<span data-ttu-id="e5639-114">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="e5639-114">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="e5639-115">Planear tu implementación de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e5639-115">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)