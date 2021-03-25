---
title: Configurar la sincronización de Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Opciones de administrador y usuario para configurar Microsoft Edge para sincronizar favoritos, contraseñas y otros datos del explorador.
ms.openlocfilehash: 93af96bd864f08bb17bb1d6f0669f602a56fd8ca
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448124"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a><span data-ttu-id="085d9-103">Configurar la sincronización de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="085d9-103">Configure Microsoft Edge enterprise sync</span></span>

<span data-ttu-id="085d9-104">En este artículo se explica cómo los administradores pueden configurar Microsoft Edge para sincronizar los favoritos del usuario, las contraseñas y otros datos del explorador en todos los dispositivos que han iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="085d9-104">This article explains how admins can configure Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="085d9-105">Se aplica a la versión 77 de Microsoft Edge o posteriores, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="085d9-105">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="overview"></a><span data-ttu-id="085d9-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="085d9-106">Overview</span></span>

<span data-ttu-id="085d9-107">La sincronización de Microsoft Edge permite a los usuarios acceder a sus datos de exploración en todos sus dispositivos que hayan iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="085d9-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="085d9-108">Los datos admitidos por la sincronización incluyen:</span><span class="sxs-lookup"><span data-stu-id="085d9-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="085d9-109">Favoritos</span><span class="sxs-lookup"><span data-stu-id="085d9-109">Favorites</span></span>
- <span data-ttu-id="085d9-110">Contraseñas</span><span class="sxs-lookup"><span data-stu-id="085d9-110">Passwords</span></span>
- <span data-ttu-id="085d9-111">Direcciones y más (relleno de formularios)</span><span class="sxs-lookup"><span data-stu-id="085d9-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="085d9-112">Colecciones</span><span class="sxs-lookup"><span data-stu-id="085d9-112">Collections</span></span>
- <span data-ttu-id="085d9-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="085d9-113">Settings</span></span>
- <span data-ttu-id="085d9-114">Extensión</span><span class="sxs-lookup"><span data-stu-id="085d9-114">Extension</span></span>
- <span data-ttu-id="085d9-115">Pestañas abiertas (disponibles en la versión 88 de Microsoft Edge)</span><span class="sxs-lookup"><span data-stu-id="085d9-115">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="085d9-116">Historial (disponible en la versión 88 de Microsoft Edge)</span><span class="sxs-lookup"><span data-stu-id="085d9-116">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="085d9-117">La funcionalidad de sincronización está habilitada mediante el consentimiento del usuario, y los usuarios pueden activar o desactivar la sincronización para cada uno de los tipos de datos enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="085d9-117">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span> <span data-ttu-id="085d9-118">Si un usuario está experimentando un problema de sincronización, es posible que deba restablecer la sincronización en **Configuración** > **Perfiles** > **Restablecer sincronización**.</span><span class="sxs-lookup"><span data-stu-id="085d9-118">If a user is experiencing a sync issue they might need to reset sync in **Settings** > **Profiles** > **Reset sync**.</span></span>

> [!NOTE]
> <span data-ttu-id="085d9-119">Los datos de configuración y conectividad de dispositivos adicionales (como el nombre del dispositivo, la marca y el modelo) se cargan para admitir la funcionalidad de sincronización.</span><span class="sxs-lookup"><span data-stu-id="085d9-119">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="085d9-120">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="085d9-120">Prerequisites</span></span>

<span data-ttu-id="085d9-121">La sincronización de Microsoft Edge para las cuentas de Azure Active Directory (Azure AD) está disponible para cualquiera de las siguientes suscripciones:</span><span class="sxs-lookup"><span data-stu-id="085d9-121">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="085d9-122">Azure AD Premium (P1 o P2)</span><span class="sxs-lookup"><span data-stu-id="085d9-122">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="085d9-123">M365 Empresa Premium</span><span class="sxs-lookup"><span data-stu-id="085d9-123">M365 Business Premium</span></span>
- <span data-ttu-id="085d9-124">Office 365 E1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="085d9-124">Office 365 E1 and above</span></span>
- <span data-ttu-id="085d9-125">Azure Information Protection (AIP) (P1 o P2)</span><span class="sxs-lookup"><span data-stu-id="085d9-125">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="085d9-126">Todas las suscripciones de EDU (Microsoft Apps para estudiantes o profesores, Exchange Online para estudiantes o profesores, O365 A1 o superior, M365 A1 o superior, o Azure Information Protection P1 o P2 para estudiantes o profesores)</span><span class="sxs-lookup"><span data-stu-id="085d9-126">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <a name="sync-group-policies"></a><span data-ttu-id="085d9-127">Directivas de grupo de sincronización</span><span class="sxs-lookup"><span data-stu-id="085d9-127">Sync group policies</span></span>

<span data-ttu-id="085d9-128">Los administradores pueden usar las siguientes directivas de grupo para configurar y administrar la sincronización de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="085d9-128">Admins can use the following group policies to configure and manage Microsoft Edge sync:</span></span>

- <span data-ttu-id="085d9-129">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled): deshabilita la sincronización por completo.</span><span class="sxs-lookup"><span data-stu-id="085d9-129">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="085d9-130">[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): deshabilita el almacenamiento del historial de exploración y la sincronización. Esta directiva también deshabilita la sincronización de pestañas abiertas.</span><span class="sxs-lookup"><span data-stu-id="085d9-130">[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="085d9-131">[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): cuando esta directiva está deshabilitada, la sincronización del historial también se deshabilitará.</span><span class="sxs-lookup"><span data-stu-id="085d9-131">[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="085d9-132">[SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): configurar la lista de tipos que se excluyen de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="085d9-132">[SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="085d9-133">[RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): permitir que los perfiles de Active Directory (AD) usen almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="085d9-133">[RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="085d9-134">Para más información, consulte [Sincronización local para usuarios de Active Directory (AD)](./microsoft-edge-on-premises-sync.md).</span><span class="sxs-lookup"><span data-stu-id="085d9-134">For more information, see [On-premises sync for Active Directory (AD) users](./microsoft-edge-on-premises-sync.md).</span></span>
- <span data-ttu-id="085d9-135">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): activa la sincronización de forma predeterminada y no requiere el consentimiento del usuario para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="085d9-135">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn on sync by default and do not require user consent to sync.</span></span>  

## <a name="configure-microsoft-edge-sync"></a><span data-ttu-id="085d9-136">Configurar la sincronización de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="085d9-136">Configure Microsoft Edge sync</span></span>

<span data-ttu-id="085d9-137">Las opciones de configuración para la sincronización de Microsoft Edge están disponibles a través del servicio de Azure Information Protection (AIP).</span><span class="sxs-lookup"><span data-stu-id="085d9-137">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="085d9-138">Cuando AIP está habilitado para un espacio empresarial, todos los usuarios pueden sincronizar los datos de Microsoft Edge, independientemente de la licencia.</span><span class="sxs-lookup"><span data-stu-id="085d9-138">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="085d9-139">Las instrucciones para habilitar AIP pueden encontrarse [aquí](/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="085d9-139">Instructions on how to enable AIP can be found [here](/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="085d9-140">Para restringir la sincronización a un conjunto específico de usuarios, puedes habilitar la [directiva de control de incorporación AIP](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) para estos usuarios.</span><span class="sxs-lookup"><span data-stu-id="085d9-140">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) for those users.</span></span> <span data-ttu-id="085d9-141">Si la sincronización aún no está disponible después de asegurarte de que todos los usuarios necesarios estén incorporados, asegúrate de que IPCv3Service está habilitado con el cmdlet de PowerShell [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps).</span><span class="sxs-lookup"><span data-stu-id="085d9-141">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="085d9-142">La activación de Azure Information Protection también permitirá el acceso a otras aplicaciones, como Microsoft Word o Microsoft Outlook, para proteger el contenido con AIP.</span><span class="sxs-lookup"><span data-stu-id="085d9-142">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="085d9-143">Además, las directivas de control de incorporación que se usan para restringir la sincronización de Microsoft Edge también evitarán que otras aplicaciones protejan el contenido con AIP.</span><span class="sxs-lookup"><span data-stu-id="085d9-143">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a><span data-ttu-id="085d9-144">Microsoft Edge y Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="085d9-144">Microsoft Edge and Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="085d9-145">Microsoft Edge es una aplicación multiplataforma con un ámbito expandido para sincronizar datos de usuario en todos sus dispositivos y ya no forma parte de Azure AD Enterprise State Roaming.</span><span class="sxs-lookup"><span data-stu-id="085d9-145">Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="085d9-146">Sin embargo, Microsoft Edge cumplirá las promesas de protección de datos de ESR, como la capacidad de crear su propia clave.</span><span class="sxs-lookup"><span data-stu-id="085d9-146">However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="085d9-147">Para obtener más información, consulta [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="085d9-147">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="085d9-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="085d9-148">See also</span></span>

- [<span data-ttu-id="085d9-149">Sincronización de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="085d9-149">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="085d9-150">Diagnosticar y corregir problemas de sincronización de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="085d9-150">Diagnose and fix Microsoft Edge sync issues</span></span>](microsoft-edge-troubleshoot-enterprise-sync.md)
- [<span data-ttu-id="085d9-151">Microsoft Edge y Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="085d9-151">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="085d9-152">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="085d9-152">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)