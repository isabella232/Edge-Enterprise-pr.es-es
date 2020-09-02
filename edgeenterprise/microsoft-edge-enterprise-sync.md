---
title: Sincronización de Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronización de Microsoft Edge Enterprise
ms.openlocfilehash: a6d01356db478871a7c6b386bbb731b32dc4739a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981197"
---
# <span data-ttu-id="fe074-103">Sincronización de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="fe074-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="fe074-104">Este artículo explica cómo usar Microsoft Edge para sincronizar los favoritos, las contraseñas y otros datos del explorador en todos los dispositivos que hayan iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="fe074-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="fe074-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fe074-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="fe074-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="fe074-106">Overview</span></span>

<span data-ttu-id="fe074-107">La sincronización de Microsoft Edge permite a los usuarios acceder a sus datos de exploración en todos sus dispositivos que hayan iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="fe074-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="fe074-108">Los datos admitidos por la sincronización incluyen:</span><span class="sxs-lookup"><span data-stu-id="fe074-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="fe074-109">Favoritos</span><span class="sxs-lookup"><span data-stu-id="fe074-109">Favorites</span></span>
- <span data-ttu-id="fe074-110">Contraseñas</span><span class="sxs-lookup"><span data-stu-id="fe074-110">Passwords</span></span>
- <span data-ttu-id="fe074-111">Direcciones y más (relleno de formularios)</span><span class="sxs-lookup"><span data-stu-id="fe074-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="fe074-112">Colecciones</span><span class="sxs-lookup"><span data-stu-id="fe074-112">Collections</span></span>
- <span data-ttu-id="fe074-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="fe074-113">Settings</span></span>

<span data-ttu-id="fe074-114">La funcionalidad de sincronización está habilitada a través del consentimiento del usuario y los usuarios pueden activar o desactivar la sincronización para cada uno de los tipos de datos enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fe074-114">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="fe074-115">Los datos de configuración y conectividad de dispositivo adicionales (como el nombre del dispositivo, la marca y el modelo) se cargan para admitir la funcionalidad de sincronización.</span><span class="sxs-lookup"><span data-stu-id="fe074-115">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="fe074-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fe074-116">Prerequisites</span></span>

<span data-ttu-id="fe074-117">Actualmente, la sincronización de Microsoft Edge para las cuentas de Azure Active Directory (Azure AD) está disponible para las siguientes suscripciones:</span><span class="sxs-lookup"><span data-stu-id="fe074-117">Currently Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for the following subscriptions:</span></span>

- <span data-ttu-id="fe074-118">Azure AD Premium (P1 y P2)</span><span class="sxs-lookup"><span data-stu-id="fe074-118">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="fe074-119">M365 Empresa Premium</span><span class="sxs-lookup"><span data-stu-id="fe074-119">M365 Business Premium</span></span>
- <span data-ttu-id="fe074-120">Office 365 E3 y superiores</span><span class="sxs-lookup"><span data-stu-id="fe074-120">Office 365 E3 and above</span></span>
- <span data-ttu-id="fe074-121">Azure Information Protection (AIP) (P1 y P2)</span><span class="sxs-lookup"><span data-stu-id="fe074-121">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="fe074-122">Todas las suscripciones de EDU (O365 A1 o superior, M365 A1 o superior, o bien Azure Information Protection P1 o P2 para estudiantes o profesores)</span><span class="sxs-lookup"><span data-stu-id="fe074-122">All EDU subscriptions (O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

> [!NOTE]
> <span data-ttu-id="fe074-123">La sincronización tiene una dependencia en el servicio de protección que ofrece Azure Information Protection (AIP) para proteger los datos de sincronización.</span><span class="sxs-lookup"><span data-stu-id="fe074-123">Sync has a dependency on the protection service offered by Azure Information Protection (AIP) to protect sync data.</span></span> <span data-ttu-id="fe074-124">Este servicio está disponible actualmente para las suscripciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="fe074-124">This service is currently available to the preceding subscriptions.</span></span> <span data-ttu-id="fe074-125">Para ver la lista completa de SKU con AIP, consulta [Precios de protección de la información](https://azure.microsoft.com/pricing/details/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="fe074-125">To see the full list of SKUs with AIP, see [Information Protection Pricing](https://azure.microsoft.com/pricing/details/information-protection/).</span></span>

## <span data-ttu-id="fe074-126">Opciones de configuración de sincronización de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fe074-126">Configuration options for Microsoft Edge sync</span></span>

<span data-ttu-id="fe074-127">Están disponibles las siguientes opciones de configuración para habilitar la sincronización de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="fe074-127">The following configuration options are available for enabling Microsoft Edge sync:</span></span>

- <span data-ttu-id="fe074-128">Azure Information Protection (AIP)</span><span class="sxs-lookup"><span data-stu-id="fe074-128">Azure Information Protection (AIP)</span></span>
- <span data-ttu-id="fe074-129">Azure AD Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="fe074-129">Azure AD Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="fe074-130">Si se deshabilitan tanto AIP como ESR, los usuarios verán un mensaje de error que indicará que la sincronización no está disponible para su cuenta.</span><span class="sxs-lookup"><span data-stu-id="fe074-130">If both AIP and ESR are disabled, users will see an error message indicating that sync is not available for their account.</span></span>

### <span data-ttu-id="fe074-131">Azure Information Protection (AIP)</span><span class="sxs-lookup"><span data-stu-id="fe074-131">Azure Information Protection (AIP)</span></span>

<span data-ttu-id="fe074-132">Si el servicio de Azure Information Protection (AIP) está habilitado para un inquilino, todos los usuarios pueden sincronizar datos de Microsoft Edge, independientemente de las licencias.</span><span class="sxs-lookup"><span data-stu-id="fe074-132">If the Azure Information Protection (AIP) service is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="fe074-133">Las instrucciones para habilitar AIP pueden encontrarse [aquí](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="fe074-133">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="fe074-134">Para restringir la sincronización a un conjunto específico de usuarios, puede habilitar la [directiva de control de incorporación AADRM](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) para estos usuarios.</span><span class="sxs-lookup"><span data-stu-id="fe074-134">To restrict sync to certain set of users, you can enable the [AADRM onboarding control policy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="fe074-135">Si la sincronización aún no está disponible después de asegurarse de que todos los usuarios necesarios estén incorporados, asegúrese de que la IPCv3Service está habilitada con el cmdlet de PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps).</span><span class="sxs-lookup"><span data-stu-id="fe074-135">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps) PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="fe074-136">La activación de Azure Information Protection también restringirá el acceso para otras aplicaciones con AIP, como Microsoft Word o Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="fe074-136">Activating Azure Information Protection will also restrict access for other applications using AIP, such as Microsoft Word or Microsoft Outlook.</span></span>

### <span data-ttu-id="fe074-137">Azure AD Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="fe074-137">Azure AD Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="fe074-138">Si la función Azure Active Directory [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) está habilitada para cualquier usuario o inquilino, estos podrán usar la función de sincronización de Microsoft Edge, independientemente de la configuración de directiva de control de incorporación.</span><span class="sxs-lookup"><span data-stu-id="fe074-138">If the Azure Active Directory [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) feature is enabled for any user or tenant, they can use the Microsoft Edge sync feature regardless of the onboarding control policy setting.</span></span>

## <span data-ttu-id="fe074-139">Microsoft Edge y Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="fe074-139">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="fe074-140">El nuevo Microsoft Edge es una aplicación multiplataforma con un ámbito expandido para sincronización de los datos de usuarios en todos sus dispositivos y ya no forma parte de Azure AD Enterprise State Roaming.</span><span class="sxs-lookup"><span data-stu-id="fe074-140">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="fe074-141">Sin embargo, el nuevo Microsoft Edge cumplirá las promesas de protección de datos de ESR, como la capacidad de llevar la propia clave.</span><span class="sxs-lookup"><span data-stu-id="fe074-141">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="fe074-142">Para obtener más información, consulta [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="fe074-142">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="fe074-143">Directivas de grupo de sincronización</span><span class="sxs-lookup"><span data-stu-id="fe074-143">Sync group policies</span></span>

<span data-ttu-id="fe074-144">Las siguientes directivas de grupo afectan a la sincronización de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="fe074-144">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="fe074-145">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): deshabilita la sincronización por completo.</span><span class="sxs-lookup"><span data-stu-id="fe074-145">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="fe074-146">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): deshabilita el almacenamiento y la sincronización del historial de exploración. Esto también deshabilita la sincronización de pestañas abiertas.</span><span class="sxs-lookup"><span data-stu-id="fe074-146">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="fe074-147">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configurar la lista de tipos que se excluyen de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="fe074-147">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>

## <span data-ttu-id="fe074-148">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="fe074-148">Frequently Asked Questions</span></span>

### <span data-ttu-id="fe074-149">CUMPLIMIENTO DE SEGURIDAD y SERVIDOR/DATOS</span><span class="sxs-lookup"><span data-stu-id="fe074-149">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="fe074-150">¿Se cifran los datos sincronizados?</span><span class="sxs-lookup"><span data-stu-id="fe074-150">Is the synced data encrypted?</span></span> 

<span data-ttu-id="fe074-151">Los datos están cifrados en el transporte con TLS 1.2 o posterior y además, permanece en reposo en el servicio de Microsoft con AES256.</span><span class="sxs-lookup"><span data-stu-id="fe074-151">The data is encrypted in transport using TLS 1.2 or greater, and additionally at rest in Microsoft's service using AES256.</span></span>

#### <span data-ttu-id="fe074-152">¿Dónde se almacenan los datos de sincronización de Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="fe074-152">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="fe074-153">Los datos sincronizados para las cuentas de Azure AD se almacenan en servidores seguros, en función del identificador de espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="fe074-153">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="fe074-154">Por ejemplo, los datos de un espacio empresarial que está registrado en Estados Unidos se almacenan en los servidores localizados en una ubicación geográfica para esa región y usan la misma solución de almacenamiento que las aplicaciones de Office.</span><span class="sxs-lookup"><span data-stu-id="fe074-154">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="fe074-155">¿Los datos salen de la nube en algún momento de Microsoft, aparte de sincronizarse con Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="fe074-155">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="fe074-156">No.</span><span class="sxs-lookup"><span data-stu-id="fe074-156">No.</span></span>

#### <span data-ttu-id="fe074-157">¿Los administradores de espacios empresariales pueden llevar su propia clave?</span><span class="sxs-lookup"><span data-stu-id="fe074-157">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="fe074-158">Sí, mediante [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="fe074-158">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="fe074-159">¿Qué términos de servicio se aplican a la sincronización empresarial?</span><span class="sxs-lookup"><span data-stu-id="fe074-159">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="fe074-160">Los términos de servicio son los mismas que para la suscripción de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="fe074-160">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="fe074-161">Todos los términos de servicio de Azure AD, en última instancia, corresponden a los [Términos del servicio en línea](https://www.microsoft.com/licensing/product-licensing/products) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe074-161">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="fe074-162">¿Es compatible Microsoft Edge con el cumplimiento normativo de Government Community Cloud (GCC) High?</span><span class="sxs-lookup"><span data-stu-id="fe074-162">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="fe074-163">Actualmente, no.</span><span class="sxs-lookup"><span data-stu-id="fe074-163">Not today.</span></span> <span data-ttu-id="fe074-164">GCC High es de nivel D, mientras que Microsoft Edge admite hasta el nivel C.</span><span class="sxs-lookup"><span data-stu-id="fe074-164">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="fe074-165">APLICAR LA SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="fe074-165">APPLYING SYNC</span></span>

#### <span data-ttu-id="fe074-166">¿Qué sucede con los clientes de empresa y del sector educativo que deciden mantener Microsoft Edge heredado?</span><span class="sxs-lookup"><span data-stu-id="fe074-166">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="fe074-167">La versión actual del explorador Microsoft Edge seguirá participando en la oferta de ESR.</span><span class="sxs-lookup"><span data-stu-id="fe074-167">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="fe074-168">¿Por qué necesito una suscripción de Azure AD Premium para sincronizar?</span><span class="sxs-lookup"><span data-stu-id="fe074-168">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="fe074-169">La sincronización de empresa depende de Azure Information Protection, que no está disponible en todos los niveles de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="fe074-169">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="fe074-170">¿La sincronización de Microsoft Edge está basada en Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="fe074-170">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="fe074-171">No.</span><span class="sxs-lookup"><span data-stu-id="fe074-171">No.</span></span> <span data-ttu-id="fe074-172">ESR se puede usar para habilitar la sincronización, pero la sincronización de Microsoft Edge no forma parte de ESR.</span><span class="sxs-lookup"><span data-stu-id="fe074-172">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="fe074-173">Para más información, consulte [Sincronización de Microsoft Edge](microsoft-edge-enterprise-sync.md) y [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="fe074-173">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="fe074-174">¿Microsoft Edge admitirá en algún momento la sincronización entre Microsoft Edge e IE?</span><span class="sxs-lookup"><span data-stu-id="fe074-174">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="fe074-175">No hay planes para admitir esta sincronización.</span><span class="sxs-lookup"><span data-stu-id="fe074-175">There are no plans to support this syncing.</span></span> <span data-ttu-id="fe074-176">Si aún necesita Internet Explorer en su entorno para usar aplicaciones heredadas, considere la posibilidad de usar el [nuevo modo de IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="fe074-176">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="fe074-177">¿El nuevo explorador de Microsoft Edge se sincronizará con Microsoft Edge Legacy?</span><span class="sxs-lookup"><span data-stu-id="fe074-177">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="fe074-178">No, no lo hará.</span><span class="sxs-lookup"><span data-stu-id="fe074-178">No, it won't.</span></span> <span data-ttu-id="fe074-179">Creemos que la conexión de estos dos ecosistemas dará lugar a compromisos en la confiabilidad de la sincronización del nuevo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fe074-179">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="fe074-180">Se garantizará que los datos existentes se migren al nuevo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fe074-180">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="fe074-181">Además, los usuarios podrán importar datos desde el explorador de su elección.</span><span class="sxs-lookup"><span data-stu-id="fe074-181">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="fe074-182">Esto también significa que el nuevo explorador Microsoft Edge no tendrá una forma de sincronizarse con IE.</span><span class="sxs-lookup"><span data-stu-id="fe074-182">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="fe074-183">ADMINISTRAR LA SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="fe074-183">MANAGING SYNC</span></span>

#### <span data-ttu-id="fe074-184">¿Es posible impedir que los usuarios sincronicen con un espacio empresarial personal?</span><span class="sxs-lookup"><span data-stu-id="fe074-184">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="fe074-185">No directamente, pero puede determinar qué perfiles pueden iniciar sesión en Microsoft Edge mediante la directiva [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="fe074-185">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="fe074-186">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fe074-186">See also</span></span>

- [<span data-ttu-id="fe074-187">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="fe074-187">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="fe074-188">Microsoft Edge y Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="fe074-188">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
