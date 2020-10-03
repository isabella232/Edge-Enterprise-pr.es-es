---
title: Sincronización de Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 09/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronización de Microsoft Edge Enterprise
ms.openlocfilehash: d5868fb496c036d750925bb5ae6dfa3de0293fd2
ms.sourcegitcommit: 8a4479a1b034c3c13ea03ee3a2374a1af332cb38
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2020
ms.locfileid: "11091952"
---
# <span data-ttu-id="aa518-103">Sincronización de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="aa518-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="aa518-104">Este artículo explica cómo usar Microsoft Edge para sincronizar los favoritos, las contraseñas y otros datos del explorador en todos los dispositivos que hayan iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="aa518-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="aa518-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="aa518-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="aa518-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="aa518-106">Overview</span></span>

<span data-ttu-id="aa518-107">La sincronización de Microsoft Edge permite a los usuarios acceder a sus datos de exploración en todos sus dispositivos que hayan iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="aa518-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="aa518-108">Los datos admitidos por la sincronización incluyen:</span><span class="sxs-lookup"><span data-stu-id="aa518-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="aa518-109">Favoritos</span><span class="sxs-lookup"><span data-stu-id="aa518-109">Favorites</span></span>
- <span data-ttu-id="aa518-110">Contraseñas</span><span class="sxs-lookup"><span data-stu-id="aa518-110">Passwords</span></span>
- <span data-ttu-id="aa518-111">Direcciones y más (relleno de formularios)</span><span class="sxs-lookup"><span data-stu-id="aa518-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="aa518-112">Colecciones</span><span class="sxs-lookup"><span data-stu-id="aa518-112">Collections</span></span>
- <span data-ttu-id="aa518-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="aa518-113">Settings</span></span>

<span data-ttu-id="aa518-114">La funcionalidad de sincronización está habilitada a través del consentimiento del usuario y los usuarios pueden activar o desactivar la sincronización para cada uno de los tipos de datos enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="aa518-114">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="aa518-115">Los datos de configuración y conectividad de dispositivo adicionales (como el nombre del dispositivo, la marca y el modelo) se cargan para admitir la funcionalidad de sincronización.</span><span class="sxs-lookup"><span data-stu-id="aa518-115">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="aa518-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aa518-116">Prerequisites</span></span>

<span data-ttu-id="aa518-117">La sincronización de Microsoft Edge para las cuentas de Azure Active Directory (Azure AD) está disponible para cualquiera de las siguientes suscripciones:</span><span class="sxs-lookup"><span data-stu-id="aa518-117">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="aa518-118">Azure AD Premium (P1 y P2)</span><span class="sxs-lookup"><span data-stu-id="aa518-118">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="aa518-119">M365 Empresa Premium</span><span class="sxs-lookup"><span data-stu-id="aa518-119">M365 Business Premium</span></span>
- <span data-ttu-id="aa518-120">Office 365 E3 y superiores</span><span class="sxs-lookup"><span data-stu-id="aa518-120">Office 365 E3 and above</span></span>
- <span data-ttu-id="aa518-121">Azure Information Protection (AIP) (P1 y P2)</span><span class="sxs-lookup"><span data-stu-id="aa518-121">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="aa518-122">Todas las suscripciones de EDU (Microsoft Apps para estudiantes o profesores, Exchange Online para estudiantes o profesores, O365 A1 o superior, M365 A1 o superior, o Azure Information Protection P1 o P2 para estudiantes o profesores)</span><span class="sxs-lookup"><span data-stu-id="aa518-122">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="aa518-123">Configuración de la sincronización de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="aa518-123">Configuring Microsoft Edge sync</span></span>

<span data-ttu-id="aa518-124">Las opciones de configuración para la sincronización de Microsoft Edge están disponibles a través del servicio de Azure Information Protection (AIP).</span><span class="sxs-lookup"><span data-stu-id="aa518-124">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="aa518-125">Cuando AIP está habilitado para un espacio empresarial, todos los usuarios pueden sincronizar los datos de Microsoft Edge, independientemente de la licencia.</span><span class="sxs-lookup"><span data-stu-id="aa518-125">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="aa518-126">Las instrucciones para habilitar AIP pueden encontrarse [aquí](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="aa518-126">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="aa518-127">Para restringir la sincronización a un conjunto específico de usuarios, puedes habilitar la [directiva de control de incorporación AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) para estos usuarios.</span><span class="sxs-lookup"><span data-stu-id="aa518-127">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="aa518-128">Si la sincronización aún no está disponible después de asegurarte de que todos los usuarios necesarios estén incorporados, asegúrate de que IPCv3Service está habilitado con el cmdlet de PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps).</span><span class="sxs-lookup"><span data-stu-id="aa518-128">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="aa518-129">La activación de Azure Information Protection también permitirá el acceso a otras aplicaciones, como Microsoft Word o Microsoft Outlook, para proteger el contenido con AIP.</span><span class="sxs-lookup"><span data-stu-id="aa518-129">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="aa518-130">Además, las directivas de control de incorporación que se usan para restringir la sincronización de Microsoft Edge también evitarán que otras aplicaciones protejan el contenido con AIP.</span><span class="sxs-lookup"><span data-stu-id="aa518-130">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="aa518-131">Microsoft Edge y Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="aa518-131">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="aa518-132">El nuevo Microsoft Edge es una aplicación multiplataforma con un ámbito expandido para sincronización de los datos de usuarios en todos sus dispositivos y ya no forma parte de Azure AD Enterprise State Roaming.</span><span class="sxs-lookup"><span data-stu-id="aa518-132">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="aa518-133">Sin embargo, el nuevo Microsoft Edge cumplirá las promesas de protección de datos de ESR, como la capacidad de llevar la propia clave.</span><span class="sxs-lookup"><span data-stu-id="aa518-133">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="aa518-134">Para obtener más información, consulta [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="aa518-134">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="aa518-135">Directivas de grupo de sincronización</span><span class="sxs-lookup"><span data-stu-id="aa518-135">Sync group policies</span></span>

<span data-ttu-id="aa518-136">Las siguientes directivas de grupo afectan a la sincronización de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="aa518-136">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="aa518-137">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): deshabilita la sincronización por completo.</span><span class="sxs-lookup"><span data-stu-id="aa518-137">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="aa518-138">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): deshabilita el almacenamiento y la sincronización del historial de exploración. Esto también deshabilita la sincronización de pestañas abiertas.</span><span class="sxs-lookup"><span data-stu-id="aa518-138">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="aa518-139">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configurar la lista de tipos que se excluyen de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="aa518-139">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="aa518-140">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permitir que los perfiles de Active Directory (AD) usen almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="aa518-140">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="aa518-141">Para más información, consulte [Sincronización local para usuarios de Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span><span class="sxs-lookup"><span data-stu-id="aa518-141">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="aa518-142">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): activar la sincronización de forma predeterminada y no requerir el consentimiento del usuario para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="aa518-142">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="aa518-143">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="aa518-143">Frequently Asked Questions</span></span>

### <span data-ttu-id="aa518-144">CUMPLIMIENTO DE SEGURIDAD y SERVIDOR/DATOS</span><span class="sxs-lookup"><span data-stu-id="aa518-144">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="aa518-145">¿Se cifran los datos sincronizados?</span><span class="sxs-lookup"><span data-stu-id="aa518-145">Is the synced data encrypted?</span></span> 

<span data-ttu-id="aa518-146">Los datos se cifran en el transporte con TLS 1.2 o superior.</span><span class="sxs-lookup"><span data-stu-id="aa518-146">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="aa518-147">La mayoría de los tipos de datos se cifran también al almacenarlos en el servicio de Microsoft con AES256.</span><span class="sxs-lookup"><span data-stu-id="aa518-147">Most data types are additionally encrypted at rest in Microsoft's service using AES256.</span></span> 

#### <span data-ttu-id="aa518-148">¿Dónde se almacenan los datos de sincronización de Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="aa518-148">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="aa518-149">Los datos sincronizados para las cuentas de Azure AD se almacenan en servidores seguros, en función del identificador de espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="aa518-149">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="aa518-150">Por ejemplo, los datos de un espacio empresarial que está registrado en Estados Unidos se almacenan en los servidores localizados en una ubicación geográfica para esa región y usan la misma solución de almacenamiento que las aplicaciones de Office.</span><span class="sxs-lookup"><span data-stu-id="aa518-150">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="aa518-151">¿Los datos salen de la nube en algún momento de Microsoft, aparte de sincronizarse con Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="aa518-151">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="aa518-152">No.</span><span class="sxs-lookup"><span data-stu-id="aa518-152">No.</span></span>

#### <span data-ttu-id="aa518-153">¿Los administradores de espacios empresariales pueden llevar su propia clave?</span><span class="sxs-lookup"><span data-stu-id="aa518-153">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="aa518-154">Sí, mediante [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="aa518-154">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="aa518-155">¿Qué términos de servicio se aplican a la sincronización empresarial?</span><span class="sxs-lookup"><span data-stu-id="aa518-155">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="aa518-156">Los términos de servicio son los mismas que para la suscripción de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="aa518-156">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="aa518-157">Todos los términos de servicio de Azure AD, en última instancia, corresponden a los [Términos del servicio en línea](https://www.microsoft.com/licensing/product-licensing/products) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aa518-157">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="aa518-158">¿Es compatible Microsoft Edge con el cumplimiento normativo de Government Community Cloud (GCC) High?</span><span class="sxs-lookup"><span data-stu-id="aa518-158">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="aa518-159">Actualmente, no.</span><span class="sxs-lookup"><span data-stu-id="aa518-159">Not today.</span></span> <span data-ttu-id="aa518-160">GCC High es de nivel D, mientras que Microsoft Edge admite hasta el nivel C.</span><span class="sxs-lookup"><span data-stu-id="aa518-160">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="aa518-161">APLICAR LA SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="aa518-161">APPLYING SYNC</span></span>

#### <span data-ttu-id="aa518-162">¿Qué sucede con los clientes de empresa y del sector educativo que deciden mantener Microsoft Edge heredado?</span><span class="sxs-lookup"><span data-stu-id="aa518-162">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="aa518-163">La versión actual del explorador Microsoft Edge seguirá participando en la oferta de ESR.</span><span class="sxs-lookup"><span data-stu-id="aa518-163">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="aa518-164">¿Por qué necesito una suscripción de Azure AD Premium para sincronizar?</span><span class="sxs-lookup"><span data-stu-id="aa518-164">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="aa518-165">La sincronización de empresa depende de Azure Information Protection, que no está disponible en todos los niveles de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="aa518-165">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="aa518-166">¿La sincronización de Microsoft Edge está basada en Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="aa518-166">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="aa518-167">No.</span><span class="sxs-lookup"><span data-stu-id="aa518-167">No.</span></span> <span data-ttu-id="aa518-168">ESR se puede usar para habilitar la sincronización, pero la sincronización de Microsoft Edge no forma parte de ESR.</span><span class="sxs-lookup"><span data-stu-id="aa518-168">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="aa518-169">Para más información, consulte [Sincronización de Microsoft Edge](microsoft-edge-enterprise-sync.md) y [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="aa518-169">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="aa518-170">¿Microsoft Edge admitirá en algún momento la sincronización entre Microsoft Edge e IE?</span><span class="sxs-lookup"><span data-stu-id="aa518-170">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="aa518-171">No hay planes para admitir esta sincronización.</span><span class="sxs-lookup"><span data-stu-id="aa518-171">There are no plans to support this syncing.</span></span> <span data-ttu-id="aa518-172">Si aún necesita Internet Explorer en su entorno para usar aplicaciones heredadas, considere la posibilidad de usar el [nuevo modo de IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="aa518-172">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="aa518-173">¿El nuevo explorador de Microsoft Edge se sincronizará con Microsoft Edge Legacy?</span><span class="sxs-lookup"><span data-stu-id="aa518-173">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="aa518-174">No, no lo hará.</span><span class="sxs-lookup"><span data-stu-id="aa518-174">No, it won't.</span></span> <span data-ttu-id="aa518-175">Creemos que la conexión de estos dos ecosistemas dará lugar a compromisos en la confiabilidad de la sincronización del nuevo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa518-175">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="aa518-176">Se garantizará que los datos existentes se migren al nuevo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa518-176">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="aa518-177">Además, los usuarios podrán importar datos desde el explorador de su elección.</span><span class="sxs-lookup"><span data-stu-id="aa518-177">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="aa518-178">Esto también significa que el nuevo explorador Microsoft Edge no tendrá una forma de sincronizarse con IE.</span><span class="sxs-lookup"><span data-stu-id="aa518-178">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="aa518-179">ADMINISTRAR LA SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="aa518-179">MANAGING SYNC</span></span>

#### <span data-ttu-id="aa518-180">¿Es posible impedir que los usuarios sincronicen con un espacio empresarial personal?</span><span class="sxs-lookup"><span data-stu-id="aa518-180">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="aa518-181">No directamente, pero puede determinar qué perfiles pueden iniciar sesión en Microsoft Edge mediante la directiva [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="aa518-181">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="aa518-182">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aa518-182">See also</span></span>

- [<span data-ttu-id="aa518-183">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="aa518-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="aa518-184">Microsoft Edge y Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="aa518-184">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
