---
title: Preguntas frecuentes sobre sincronización empresarial de Microsoft Edge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Preguntas más frecuentes sobre la sincronización empresarial de Microsoft Edge.
ms.openlocfilehash: e25ee985f65ee61dda5cacece73d43be7f1e6d7d
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447874"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a><span data-ttu-id="7f963-103">Preguntas frecuentes sobre sincronización empresarial de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7f963-103">Microsoft Edge enterprise sync FAQ</span></span>

<span data-ttu-id="7f963-104">Este artículo responde a las preguntas más frecuentes acerca de la sincronización empresarial para Microsoft Edge versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="7f963-104">This article answers frequently asked questions about enterprise sync for Microsoft Edge version 77 or later.</span></span>

## <a name="security-and-serverdata-compliance"></a><span data-ttu-id="7f963-105">Seguridad y cumplimiento de datos/servidor</span><span class="sxs-lookup"><span data-stu-id="7f963-105">Security and Server/Data Compliance</span></span>

### <a name="is-the-synced-data-encrypted"></a><span data-ttu-id="7f963-106">¿Se cifran los datos sincronizados?</span><span class="sxs-lookup"><span data-stu-id="7f963-106">Is the synced data encrypted?</span></span>

<span data-ttu-id="7f963-107">Los datos se cifran en el transporte con TLS 1.2 o superior.</span><span class="sxs-lookup"><span data-stu-id="7f963-107">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="7f963-108">Todos los tipos de datos también se cifran en reposo en el servicio de Microsoft con AES128.</span><span class="sxs-lookup"><span data-stu-id="7f963-108">All data types are additionally encrypted at rest in Microsoft's service using AES128.</span></span> <span data-ttu-id="7f963-109">Todos los tipos de datos, excepto los que se usan para la sincronización de pestañas abiertas e historial, también se cifran antes de salir del dispositivo del usuario con claves administradas a través de [Azure Information Protection](./microsoft-edge-policies.md#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="7f963-109">All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via the [Azure Information Protection](./microsoft-edge-policies.md#restrictsignintopattern) policy.</span></span>

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a><span data-ttu-id="7f963-110">¿Por qué las pestañas abiertas y los datos del historial no tienen un cifrado adicional del lado del cliente?</span><span class="sxs-lookup"><span data-stu-id="7f963-110">Why don’t open tab and history data have more client-side encryption?</span></span>

<span data-ttu-id="7f963-111">Para reducir la utilización de recursos en los dispositivos de los usuarios finales, los datos del historial se generan del lado del servidor en función de los datos de itinerancia de las pestaña abiertas.</span><span class="sxs-lookup"><span data-stu-id="7f963-111">To reduce resource utilization on end-user devices, history data is generated server-side based on open tab roaming data.</span></span> <span data-ttu-id="7f963-112">Este proceso no sería posible con el cifrado de datos del lado del cliente.</span><span class="sxs-lookup"><span data-stu-id="7f963-112">This process would not be possible with client-side encryption of this data.</span></span> <span data-ttu-id="7f963-113">Para deshabilitar la sincronización de pestañas abiertas e historial, aplique las directivas [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) o [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled).</span><span class="sxs-lookup"><span data-stu-id="7f963-113">To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) or [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) policies.</span></span>

### <a name="can-tenant-admins-bring-their-own-key"></a><span data-ttu-id="7f963-114">¿Los administradores de espacios empresariales pueden poner su propia clave?</span><span class="sxs-lookup"><span data-stu-id="7f963-114">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="7f963-115">Sí, a través de [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="7f963-115">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

### <a name="where-is-microsoft-edge-sync-data-stored"></a><span data-ttu-id="7f963-116">¿Dónde se almacenan los datos de sincronización de Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="7f963-116">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="7f963-117">Los datos sincronizados para las cuentas de Azure AD se almacenan en servidores seguros, en función del identificador de espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="7f963-117">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="7f963-118">Por ejemplo, los datos de un espacio empresarial que está registrado en Estados Unidos se almacenan en los servidores localizados en una ubicación geográfica para esa región y usan la misma solución de almacenamiento que las aplicaciones de Office.</span><span class="sxs-lookup"><span data-stu-id="7f963-118">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a><span data-ttu-id="7f963-119">¿Los datos salen de la nube en algún momento de Microsoft, aparte de sincronizarse con Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="7f963-119">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="7f963-120">No.</span><span class="sxs-lookup"><span data-stu-id="7f963-120">No.</span></span>

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a><span data-ttu-id="7f963-121">¿Qué términos de servicio se aplican a la sincronización empresarial?</span><span class="sxs-lookup"><span data-stu-id="7f963-121">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="7f963-122">Las condiciones de servicio para la sincronización de Microsoft Edge se incluyen en la licencia del software de Microsoft visible en Microsoft Edge en *edge://terms*.</span><span class="sxs-lookup"><span data-stu-id="7f963-122">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span> <span data-ttu-id="7f963-123">En última instancia, la suscripción y los términos de servicio de Azure AD se incluyen en los [Términos del servicio en línea](https://www.microsoft.com/licensing/product-licensing/products)de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7f963-123">Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a><span data-ttu-id="7f963-124">¿Microsoft Edge es compatible con el cumplimiento normativo de Government Community Cloud (GCC) High?</span><span class="sxs-lookup"><span data-stu-id="7f963-124">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="7f963-125">Actualmente, no.</span><span class="sxs-lookup"><span data-stu-id="7f963-125">Not today.</span></span> <span data-ttu-id="7f963-126">Para los clientes de la nube de GCC High, la sincronización de Microsoft Edge está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="7f963-126">For customers in the GCC High cloud, Microsoft Edge sync is disabled.</span></span>

## <a name="applying-sync"></a><span data-ttu-id="7f963-127">Aplicación de sincronización</span><span class="sxs-lookup"><span data-stu-id="7f963-127">Applying Sync</span></span>

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a><span data-ttu-id="7f963-128">¿Por qué la sincronización de Microsoft Edge no es compatible con todas las suscripciones de M365?</span><span class="sxs-lookup"><span data-stu-id="7f963-128">Why isn’t Microsoft Edge sync supported in all M365 subscriptions?</span></span>

<span data-ttu-id="7f963-129">La sincronización empresarial depende de [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), que no está disponible en todas las suscripciones de M365.</span><span class="sxs-lookup"><span data-stu-id="7f963-129">Enterprise sync depends on [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), which is not available in all M365 subscriptions.</span></span>

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a><span data-ttu-id="7f963-130">¿La sincronización de Microsoft Edge está basada en Enterprise State Roaming (ESR)?</span><span class="sxs-lookup"><span data-stu-id="7f963-130">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="7f963-131">No.</span><span class="sxs-lookup"><span data-stu-id="7f963-131">No.</span></span> <span data-ttu-id="7f963-132">ESR se puede usar para habilitar la sincronización, pero la sincronización de Microsoft Edge no forma parte de ESR.</span><span class="sxs-lookup"><span data-stu-id="7f963-132">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="7f963-133">Para más información, consulte [Sincronización de Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) y [Microsoft Edge y Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).</span><span class="sxs-lookup"><span data-stu-id="7f963-133">For more information, see [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) and [Microsoft Edge and Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).</span></span>

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a><span data-ttu-id="7f963-134">¿Microsoft Edge admitirá en algún momento la sincronización entre Microsoft Edge e IE?</span><span class="sxs-lookup"><span data-stu-id="7f963-134">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="7f963-135">No hay planes para admitir esta sincronización.</span><span class="sxs-lookup"><span data-stu-id="7f963-135">There are no plans to support this syncing.</span></span> <span data-ttu-id="7f963-136">Si aún necesita Internet Explorer (IE) en su entorno para usar aplicaciones heredadas, considere la posibilidad de usar el [nuevo modo de IE](./edge-ie-mode.md).</span><span class="sxs-lookup"><span data-stu-id="7f963-136">If you still need IE in your environment to support legacy apps, consider our [new IE mode](./edge-ie-mode.md).</span></span>

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a><span data-ttu-id="7f963-137">¿Microsoft Edge se sincronizará con Microsoft Edge (versión anterior)?</span><span class="sxs-lookup"><span data-stu-id="7f963-137">Will Microsoft Edge sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="7f963-138">No lo hará.</span><span class="sxs-lookup"><span data-stu-id="7f963-138">No, it won't.</span></span> <span data-ttu-id="7f963-139">Creemos que la conexión de estos dos ecosistemas provocará un compromiso respecto de la confiabilidad de la sincronización en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7f963-139">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge.</span></span> <span data-ttu-id="7f963-140">Nos aseguraremos de que los datos existentes se migren a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7f963-140">We will ensure that existing data is migrated to the Microsoft Edge.</span></span> <span data-ttu-id="7f963-141">Los usuarios también podrán importar datos desde el explorador de su elección, lo que también significa que Microsoft Edge no tendrá una forma de sincronizar con IE.</span><span class="sxs-lookup"><span data-stu-id="7f963-141">Users will also be able to import data from browser of their choice, which also means that Microsoft Edge won't have a way to sync with IE.</span></span>

## <a name="managing-sync"></a><span data-ttu-id="7f963-142">Administración de sincronización</span><span class="sxs-lookup"><span data-stu-id="7f963-142">Managing Sync</span></span>

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a><span data-ttu-id="7f963-143">¿Es posible impedir que los usuarios sincronicen con un espacio empresarial personal?</span><span class="sxs-lookup"><span data-stu-id="7f963-143">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="7f963-144">No directamente, pero puede determinar qué perfiles pueden iniciar sesión en Microsoft Edge mediante la directiva [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="7f963-144">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern) policy.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f963-145">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7f963-145">See also</span></span>

- [<span data-ttu-id="7f963-146">Sincronización de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="7f963-146">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="7f963-147">Microsoft Edge y Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="7f963-147">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="7f963-148">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="7f963-148">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)