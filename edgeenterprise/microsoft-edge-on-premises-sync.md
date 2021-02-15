---
title: Sincronización local para usuarios de Active Directory (AD)
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 02/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronización local para usuarios de Active Directory (AD)
ms.openlocfilehash: adf0adc8370aa1e18d07d0d2e91727d1ac607bf1
ms.sourcegitcommit: 90b8eab62edbed0e0a84780abd7d3854bf95c130
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2021
ms.locfileid: "11328052"
---
# <span data-ttu-id="a26a2-103">Sincronización local para usuarios de Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="a26a2-103">On-premises sync for Active Directory (AD) users</span></span>

<span data-ttu-id="a26a2-104">En este artículo, se explica cómo los usuarios de Active Directory (AD) pueden desplazarse por los favoritos y las configuraciones de Microsoft Edge entre equipos sin una conexión a los servicios en la nube de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a26a2-104">This article explains how Active Directory (AD) users can roam Microsoft Edge favorites and settings between computers without connecting to Microsoft cloud services.</span></span>

> [!NOTE]
> <span data-ttu-id="a26a2-105">Este artículo se aplica a Microsoft Edge, versión 85 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a26a2-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="a26a2-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="a26a2-106">Introduction</span></span>

<span data-ttu-id="a26a2-107">Sincronizar los datos de usuario en Microsoft Edge requiere, de manera usual, una cuenta de Microsoft o una cuenta de Azure Active Directory (Azure AD), y una conexión a los servicios en la nube de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a26a2-107">Syncing user data in Microsoft Edge normally requires either a Microsoft Account or an Azure Active Directory (Azure AD) account, and a connection to Microsoft cloud services.</span></span> <span data-ttu-id="a26a2-108">Con la sincronización local, Microsoft Edge guarda los favoritos y la configuración de un usuario de Active Directory en un archivo que se puede mover entre diferentes equipos.</span><span class="sxs-lookup"><span data-stu-id="a26a2-108">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can be moved between different computers.</span></span> <span data-ttu-id="a26a2-109">La sincronización local no interfiere con la sincronización en la nube para los perfiles que admiten esta característica.</span><span class="sxs-lookup"><span data-stu-id="a26a2-109">On-premises sync doesn't interfere with cloud syncing for those profiles that allow it.</span></span>

## <span data-ttu-id="a26a2-110">Cómo funciona</span><span class="sxs-lookup"><span data-stu-id="a26a2-110">How it works</span></span>

<span data-ttu-id="a26a2-111">Microsoft Edge permite asociar perfiles con cuentas de Active Directory (AD), los cuales no se pueden usar con la sincronización en la nube. Cuando está habilitada la sincronización local, los datos del perfil de AD se guardan en un archivo llamado profile.pb.</span><span class="sxs-lookup"><span data-stu-id="a26a2-111">Microsoft Edge allows profiles to be associated with Active Directory (AD) accounts, which can't be used with cloud sync. When on-premises sync is enabled, the data from the AD profile is saved to a file named profile.pb.</span></span> <span data-ttu-id="a26a2-112">De forma predeterminada, este archivo se almacena en *%APPDATA%/Microsoft/Edge*.</span><span class="sxs-lookup"><span data-stu-id="a26a2-112">By default, this file is stored in *%APPDATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="a26a2-113">Después de escribir el archivo, este puede moverse entre distintos equipos, y los datos de usuario se leerán y se escribirán en cada uno de estos equipos.</span><span class="sxs-lookup"><span data-stu-id="a26a2-113">After this file is written, it can be moved between different computers, and user data will be read and written on each computer.</span></span> <span data-ttu-id="a26a2-114">Microsoft Edge solo lee y escribe desde este archivo, es responsabilidad del administrador asegurarse de que el archivo se mueve según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a26a2-114">Microsoft Edge only reads and writes from this file; it is the admin's responsibility to ensure that the file is moved as needed.</span></span>

## <span data-ttu-id="a26a2-115">Usar la sincronización local</span><span class="sxs-lookup"><span data-stu-id="a26a2-115">Use on-premises sync</span></span>

<span data-ttu-id="a26a2-116">Para usar la sincronización local, tiene que habilitarla, asociar un perfil a una cuenta de AD y, de manera opcional, cambiar la ubicación de los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="a26a2-116">To use on-premises sync, you have to enable it, associate a profile with an AD account, and optionally, change the location of the user data.</span></span>

### <span data-ttu-id="a26a2-117">Habilitar la sincronización local</span><span class="sxs-lookup"><span data-stu-id="a26a2-117">Enable on-premises sync</span></span>

<span data-ttu-id="a26a2-118">Para habilitar la sincronización local en Microsoft Edge, configure la directiva [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled).</span><span class="sxs-lookup"><span data-stu-id="a26a2-118">To enable on-premises sync in Microsoft Edge, configure the [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) policy.</span></span>

### <span data-ttu-id="a26a2-119">Asegúrese de que existe un perfil asociado a una cuenta de Active Directory</span><span class="sxs-lookup"><span data-stu-id="a26a2-119">Ensure that a profile is associated with an Active Directory account</span></span>

<span data-ttu-id="a26a2-120">La sincronización local solo funciona con el perfil asociado a una cuenta de Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="a26a2-120">On-premises sync only works with the profile associated with an Active Directory (AD) account.</span></span> <span data-ttu-id="a26a2-121">Si no existe dicho perfil, la sincronización local no funcionará.</span><span class="sxs-lookup"><span data-stu-id="a26a2-121">If no such profile exists, on-premises sync will not function.</span></span> <span data-ttu-id="a26a2-122">Para asegurarse de que los usuarios inicien sesión con una cuenta de AD, configure la directiva [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin).</span><span class="sxs-lookup"><span data-stu-id="a26a2-122">To ensure that users sign on with an AD account, configure the [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) policy.</span></span> <span data-ttu-id="a26a2-123">Para la sincronización local, Microsoft Edge solo depende de AD para establecer una identidad para los datos de usuario y no hay ninguna relación directa entre cómo lee y escribe datos locales Microsoft Edge y cómo ha configurado el administrador la itinerancia de un usuario de AD.</span><span class="sxs-lookup"><span data-stu-id="a26a2-123">For on-premises sync, Microsoft Edge only relies on AD to establish an identity for the user data, and there's no direct relationship between how Microsoft Edge reads and writes on-premises data to how the admin has configured roaming for an AD user.</span></span>

### <span data-ttu-id="a26a2-124">Cambiar la ubicación de los datos de usuario (opcional)</span><span class="sxs-lookup"><span data-stu-id="a26a2-124">Change the location of the user data (optional)</span></span>

<span data-ttu-id="a26a2-125">De forma predeterminada, los datos del usuario se almacenan en un archivo con el nombre **profile.pb** en *% APPDATA%/Microsoft/Edge*.</span><span class="sxs-lookup"><span data-stu-id="a26a2-125">By default, the user data is stored in a filed named **profile.pb** in *%APPDATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="a26a2-126">Para cambiar la ubicación de este archivo, configure la directiva [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation).</span><span class="sxs-lookup"><span data-stu-id="a26a2-126">To change the location of this file, configure the [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) policy.</span></span>

## <span data-ttu-id="a26a2-127">Cambios en la experiencia de usuario cuando está habilitada la sincronización local</span><span class="sxs-lookup"><span data-stu-id="a26a2-127">Changes in the user experience when on-premises sync is enabled</span></span>

<span data-ttu-id="a26a2-128">Cuando se habilita la sincronización local, no se le pedirá a los usuarios que habiliten la sincronización. Además, los usuarios no pueden desactivar la sincronización en la Configuración de sincronización, y tampoco pueden activar los tipos de sincronización que no son compatibles con la sincronización local.</span><span class="sxs-lookup"><span data-stu-id="a26a2-128">When on-premises sync is enabled, users won't be asked to enable sync. In addition, users can't turn off sync in Sync settings, and they can't turn on sync types that aren't supported by on-premises sync.</span></span>

## <span data-ttu-id="a26a2-129">Notas de uso de sincronización local</span><span class="sxs-lookup"><span data-stu-id="a26a2-129">On-premises sync usage notes</span></span>

### <span data-ttu-id="a26a2-130">Ejecución de sincronización en la nube y sincronización local en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="a26a2-130">Running cloud sync and on-premises sync on the same computer</span></span>

<span data-ttu-id="a26a2-131">La sincronización local no interfiere con la sincronización en la nube. Si Microsoft Edge tiene varias cuentas de Microsoft o perfiles de Azure Active Directory que se sincronizan con la nube, estos perfiles continuarán sincronizándose mientras la sincronización local esté habilitada.</span><span class="sxs-lookup"><span data-stu-id="a26a2-131">On-premises sync doesn't interfere with cloud sync. If Microsoft Edge has multiple Microsoft Account or Azure Active Directory profiles that sync to the cloud, these profiles will continue to sync while on-premises sync is enabled.</span></span>

### <span data-ttu-id="a26a2-132">No se recomienda ejecutar Microsoft Edge en más de un equipo a la vez</span><span class="sxs-lookup"><span data-stu-id="a26a2-132">Running Microsoft Edge on more than one computer at a time isn't recommended</span></span>

<span data-ttu-id="a26a2-133">Como la sincronización local funciona moviendo un archivo de datos de usuario entre equipos, esta no sincroniza los cambios entre sesiones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="a26a2-133">Because on-premises sync works by moving a user data file between computers, on-premises sync doesn't sync changes between simultaneous sessions.</span></span> <span data-ttu-id="a26a2-134">Por este motivo, la sincronización local funciona mejor cuando se usa en un solo equipo a la vez.</span><span class="sxs-lookup"><span data-stu-id="a26a2-134">For this reason, on-premises sync works best when used on one computer at a time.</span></span> <span data-ttu-id="a26a2-135">Si hay sesiones locales simultáneas en ejecución, es posible que los datos de otro equipo se sobrescriban de forma inesperada sobre los datos de cualquiera de los equipos la próxima vez que inicie sesión en un explorador.</span><span class="sxs-lookup"><span data-stu-id="a26a2-135">If there are simultaneous on-premises sessions running, data on any of the computers may be unexpectedly overwritten by data from another computer the next time you start a browser session.</span></span>

> [!NOTE]
> <span data-ttu-id="a26a2-136">Microsoft Edge bloquea el archivo **profile.pb** cuando está habilitada la sincronización local.</span><span class="sxs-lookup"><span data-stu-id="a26a2-136">Microsoft Edge locks the **profile.pb** file when on-premises sync is enabled.</span></span> <span data-ttu-id="a26a2-137">Si se usa el redireccionamiento de carpetas para compartir un único archivo **profile.pb** entre equipos diferentes, solo se puede iniciar una sesión de Microsoft Edge que use ese archivo.</span><span class="sxs-lookup"><span data-stu-id="a26a2-137">If folder redirection is used to share a single **profile.pb** file between different computers, then only one instance of Microsoft Edge using that file can be started.</span></span>

### <span data-ttu-id="a26a2-138">Usar otras directivas de sincronización con la sincronización local</span><span class="sxs-lookup"><span data-stu-id="a26a2-138">Using other sync policies with on-premises sync</span></span>

<span data-ttu-id="a26a2-139">Se puede usar la directiva [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) para deshabilitar de forma selectiva la sincronización de la configuración o de los favoritos, si así lo desea.</span><span class="sxs-lookup"><span data-stu-id="a26a2-139">The [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policy can be used to selectively disable either favorites or settings sync if desired.</span></span> <span data-ttu-id="a26a2-140">La directiva [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) no tiene ningún impacto en la sincronización local.</span><span class="sxs-lookup"><span data-stu-id="a26a2-140">The [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) policy has no impact on on-premises sync.</span></span>

## <span data-ttu-id="a26a2-141">Ve también</span><span class="sxs-lookup"><span data-stu-id="a26a2-141">See also</span></span>

- [<span data-ttu-id="a26a2-142">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a26a2-142">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a26a2-143">Microsoft Edge y Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="a26a2-143">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="a26a2-144">Sincronización de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a26a2-144">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
