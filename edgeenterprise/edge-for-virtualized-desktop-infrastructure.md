---
title: Edge para la infraestructura de escritorio de virtualización
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge para infraestructura de escritorio virtualizado.
ms.openlocfilehash: 5dc234b0e6fbba4778f8236399a0ff438f704578
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641856"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a><span data-ttu-id="a91eb-103">Microsoft Edge para infraestructura de escritorio virtualizado</span><span class="sxs-lookup"><span data-stu-id="a91eb-103">Microsoft Edge for Virtualized Desktop Infrastructure</span></span>

<span data-ttu-id="a91eb-104">En este artículo se describen los requisitos y limitaciones para usar Microsoft Edge en un entorno virtualizado.</span><span class="sxs-lookup"><span data-stu-id="a91eb-104">This article describes the requirements and limitations for using Microsoft Edge in a virtualized environment.</span></span>

## <a name="what-is-vdi"></a><span data-ttu-id="a91eb-105">¿Qué es la VDI?</span><span class="sxs-lookup"><span data-stu-id="a91eb-105">What is VDI?</span></span>

<span data-ttu-id="a91eb-106">La infraestructura de escritorio virtual (VDI) es una tecnología de virtualización que hospeda un sistema operativo de escritorio y aplicaciones en un servidor centralizado en un centro de datos.</span><span class="sxs-lookup"><span data-stu-id="a91eb-106">Virtual Desktop Infrastructure (VDI) is virtualization technology that hosts a desktop operating system and applications on a centralized server in a data center.</span></span> <span data-ttu-id="a91eb-107">Esto permite una experiencia de escritorio totalmente personalizada para los usuarios con un origen centralizado totalmente seguro y compatible.</span><span class="sxs-lookup"><span data-stu-id="a91eb-107">This enables a fully personalized desktop experience for users with a fully secured and compliant centralized source.</span></span>

<span data-ttu-id="a91eb-108">Microsoft Edge se pueden usar en un entorno virtualizado de las mismas maneras que en el dispositivo local, todo ello mientras se ejecuta desde un entorno de servidor seguro y controlado.</span><span class="sxs-lookup"><span data-stu-id="a91eb-108">Microsoft Edge can be used in such a virtualized environment in much the same ways as it can be used on the local device, all the while running from secure and controlled server environment.</span></span> <span data-ttu-id="a91eb-109">En función de la solución VDI elegida, también es posible proporcionar a los usuarios un acceso fluido a las aplicaciones y sitios de la intranet.</span><span class="sxs-lookup"><span data-stu-id="a91eb-109">Depending on your chosen VDI solution it may also be possible to give your users seamless access to intranet Applications and Sites.</span></span>

<span data-ttu-id="a91eb-110">La mayoría de las características de Edge se admiten en entornos VDI sin ninguna configuración especial.</span><span class="sxs-lookup"><span data-stu-id="a91eb-110">Most features of Edge are supported on VDI environments without any special configuration.</span></span> <span data-ttu-id="a91eb-111">Sin embargo, para garantizar una experiencia óptima, se recomienda seguir las instrucciones que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="a91eb-111">However, to ensure an optimal experience it’s recommended to follow the guidance below.</span></span>

## <a name="platforms-certified-for-edge"></a><span data-ttu-id="a91eb-112">Plataformas certificadas para Edge</span><span class="sxs-lookup"><span data-stu-id="a91eb-112">Platforms certified for Edge</span></span>

- <span data-ttu-id="a91eb-113">Azure Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="a91eb-113">Azure Virtual Desktop</span></span>
- <span data-ttu-id="a91eb-114">Citrix Virtual Apps and Desktops (anteriormente conocido como XenApp y XenDesktop)</span><span class="sxs-lookup"><span data-stu-id="a91eb-114">Citrix Virtual Apps and Desktops (formerly known as XenApp and XenDesktop)</span></span>

<span data-ttu-id="a91eb-115">Aunque el equipo de Edge aún no ha comprobado otras soluciones de VDI, se espera que los flujos de trabajo más comunes en Edge sean compatibles.</span><span class="sxs-lookup"><span data-stu-id="a91eb-115">While other VDI solutions have not yet been verified by the Edge team, it is expected that the most common workflows in Edge should be supported.</span></span> <span data-ttu-id="a91eb-116">Las instrucciones proporcionadas a continuación pueden o no ser aplicables a la solución elegida.</span><span class="sxs-lookup"><span data-stu-id="a91eb-116">Guidance provided below may or may not be applicable to your chosen solution.</span></span>

## <a name="edge-on-vdi-performance-considerations"></a><span data-ttu-id="a91eb-117">Consideraciones de rendimiento de Edge en VDI</span><span class="sxs-lookup"><span data-stu-id="a91eb-117">Edge on VDI performance considerations</span></span>

<span data-ttu-id="a91eb-118">Al diseñar el entorno de VDI, debe considerar cuidadosamente los flujos de trabajo y las necesidades de los usuarios para lograr un rendimiento óptimo, así como los límites de la configuración del servidor.</span><span class="sxs-lookup"><span data-stu-id="a91eb-118">When designing your VDI environment you should carefully consider the workflows and needs of your users to achieve optimal performance, as well as the limits of your server configuration.</span></span>

<span data-ttu-id="a91eb-119">Edge recomienda los siguientes requisitos mínimos para implementar Edge en entornos de VDI:</span><span class="sxs-lookup"><span data-stu-id="a91eb-119">Edge recommends the following minimal requirements for deploying Edge to VDI environments:</span></span>

- <span data-ttu-id="a91eb-120">vCPU: de 2 a 4 núcleos por usuario</span><span class="sxs-lookup"><span data-stu-id="a91eb-120">vCPU – 2-4 Cores per User</span></span>
- <span data-ttu-id="a91eb-121">RAM: 1 GB por usuario</span><span class="sxs-lookup"><span data-stu-id="a91eb-121">RAM – 1 GB per User</span></span>

<span data-ttu-id="a91eb-122">Tenga en cuenta que las extensiones y aplicaciones web complejas de gran tamaño requerirán más memoria y tendrán que tenerse en cuenta al configurar el entorno.</span><span class="sxs-lookup"><span data-stu-id="a91eb-122">Please note that large complex web applications and extensions will require more memory and will have to be accounted for when configuring your environment.</span></span>

## <a name="edge-on-non-persisted-vdi-environments"></a><span data-ttu-id="a91eb-123">Edge en entornos de VDI no persistentes</span><span class="sxs-lookup"><span data-stu-id="a91eb-123">Edge on non-persisted VDI environments</span></span>

<span data-ttu-id="a91eb-124">Muchas soluciones de VDI permiten el acceso a entornos persistentes, donde se asigna a los usuarios un entorno virtual que persiste entre sesiones, y entornos no persistentes, donde los usuarios se asignan a uno de varios equipos disponibles, posiblemente una máquina diferente cada sesión, los datos de usuario pueden o no sincronizarse entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="a91eb-124">Many VDI solutions allow access to persisted environments, where users are assigned a virtual environment that persists between sessions, and non-persisted environments, where users are assigned to one of several available machines, possibly a different machine each session, user data may or may not sync between sessions.</span></span>

<span data-ttu-id="a91eb-125">Cuando se usa un entorno no persistente, normalmente se crea una "imagen dorada" que se usa para cada dispositivo que incluye las aplicaciones y configuraciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="a91eb-125">When using a non-persisted environment, one usually creates a “golden image” which is used for each device that includes the needed apps and configurations.</span></span> <span data-ttu-id="a91eb-126">A continuación se muestran nuestras recomendaciones para preparar Edge para ese tipo de imagen.</span><span class="sxs-lookup"><span data-stu-id="a91eb-126">Below are our recommendations for preparing Edge for such an image.</span></span>

### <a name="deploy-edge"></a><span data-ttu-id="a91eb-127">Implementación de Edge</span><span class="sxs-lookup"><span data-stu-id="a91eb-127">Deploy Edge</span></span>

<span data-ttu-id="a91eb-128">Si está en Windows 10, versión 1803 y posteriores, debe tener Microsoft Edge instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a91eb-128">If you are on Windows 10, version 1803 and above, you should have Microsoft Edge installed on your system.</span></span> <span data-ttu-id="a91eb-129">Sin embargo, si tiene una versión anterior de Windows o quiere implementar un canal diferente de Edge, se recomiendan los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a91eb-129">However, if you are on an older version of Windows or wish to deploy a different channel of Edge, the following steps are recommended.</span></span>

1. <span data-ttu-id="a91eb-130">Descargue el paquete MSI de Edge que coincida con el sistema operativo de la máquina virtual de VDI desde:</span><span class="sxs-lookup"><span data-stu-id="a91eb-130">Download the Edge MSI package matching your VDI VM operating system from:</span></span>

    - [<span data-ttu-id="a91eb-131">Descargar Microsoft Edge para empresas - Microsoft</span><span class="sxs-lookup"><span data-stu-id="a91eb-131">Download Microsoft Edge for Business - Microsoft</span></span>](https://www.microsoft.com/edge/business/download)

2. <span data-ttu-id="a91eb-132">Instale MSI en la máquina virtual de VDI mediante la ejecución del siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a91eb-132">Install the MSI to the VDI VM by running the following command:</span></span>

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a><span data-ttu-id="a91eb-133">Deshabilitar actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="a91eb-133">Disable automatic updates</span></span>

<span data-ttu-id="a91eb-134">En el caso de las máquinas no persistentes, se recomienda deshabilitar las actualizaciones automáticas y, en su lugar, actualizar Edge actualizando la "imagen dorada" para asegurarse de que no haya discrepancias de versiones entre el grupo de máquinas.</span><span class="sxs-lookup"><span data-stu-id="a91eb-134">For non-persisted machines it is best practice to disable automatic updates and instead update Edge by updating the “golden image” to ensure that there are no version mismatches among the pool of machines.</span></span>

<span data-ttu-id="a91eb-135">Consulte las siguientes directivas para deshabilitar las actualizaciones automáticas:</span><span class="sxs-lookup"><span data-stu-id="a91eb-135">See the following policies for disabling automatic updates:</span></span>

- [<span data-ttu-id="a91eb-136">Valor predeterminado de Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="a91eb-136">Update policy override default</span></span>](/deployedge/microsoft-edge-update-policies#updatedefault)

- [<span data-ttu-id="a91eb-137">Invalidar directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="a91eb-137">Update policy override</span></span>](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a><span data-ttu-id="a91eb-138">Administración de perfiles</span><span class="sxs-lookup"><span data-stu-id="a91eb-138">Profile management</span></span>

<span data-ttu-id="a91eb-139">En las configuraciones no persistentes, es importante tener en cuenta que es posible que las máquinas virtuales no mantengan el estado de usuario entre sesiones o que a los usuarios se les asigne una máquina virtual que nunca hayan usado antes y, por tanto, no tengan ninguno de sus datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="a91eb-139">On non-persisted setups it is important to consider that VMs may not maintain user state between sessions or users may be assigned a VM they have never used before and as such has none of their user data.</span></span>

<span data-ttu-id="a91eb-140">Edge admite varios métodos para sincronizar datos de usuario, de modo que estén disponibles independientemente de cómo accedan a Edge.</span><span class="sxs-lookup"><span data-stu-id="a91eb-140">Edge supports several methods for syncing user data such that it is available regardless of how they are accessing Edge.</span></span>

### <a name="azure-ad-sync"></a><span data-ttu-id="a91eb-141">Sincronización de Azure AD</span><span class="sxs-lookup"><span data-stu-id="a91eb-141">Azure AD Sync</span></span>

<span data-ttu-id="a91eb-142">Si su plan de Azure AD lo admite, la sincronización empresarial es el método más rápido y sencillo para asegurarse de que los datos de usuario de Edge se sincronizan con todos los dispositivos de usuario.</span><span class="sxs-lookup"><span data-stu-id="a91eb-142">If your Azure AD plan supports it, Enterprise sync is the fastest and easiest method to ensure that Edge user data is synced to all user devices.</span></span>  

<span data-ttu-id="a91eb-143">Consulte lo siguiente para más información sobre los requisitos y la configuración.</span><span class="sxs-lookup"><span data-stu-id="a91eb-143">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="a91eb-144">Configurar la sincronización empresarial de Microsoft Edge | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="a91eb-144">Configure Microsoft Edge enterprise sync | Microsoft Docs</span></span>](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a><span data-ttu-id="a91eb-145">Sincronización local para usuarios de Active Directory</span><span class="sxs-lookup"><span data-stu-id="a91eb-145">On-premise Sync for Active Directory Users</span></span>

<span data-ttu-id="a91eb-146">Con la sincronización local, Microsoft Edge guarda los favoritos y la configuración de un usuario de Active Directory en un archivo que se puede mover entre diferentes equipos.</span><span class="sxs-lookup"><span data-stu-id="a91eb-146">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can easily be moved between different computers.</span></span>  

<span data-ttu-id="a91eb-147">Consulte lo siguiente para más información sobre los requisitos y la configuración.</span><span class="sxs-lookup"><span data-stu-id="a91eb-147">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="a91eb-148">Sincronización local para usuarios de Active Directory (AD) | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="a91eb-148">On-premises sync for Active Directory (AD) users | Microsoft Docs</span></span>](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a><span data-ttu-id="a91eb-149">Redirección de perfiles de usuario</span><span class="sxs-lookup"><span data-stu-id="a91eb-149">User Profile Redirection</span></span>  

<span data-ttu-id="a91eb-150">Hay varias soluciones para migrar y redirigir toda la carpeta de usuario para asegurarse de que el contexto de usuario se mantiene en estos entornos no persistentes.</span><span class="sxs-lookup"><span data-stu-id="a91eb-150">There are several solutions for migrating and redirecting the entire user folder to ensure that user context is maintained in such non-persisted environments.</span></span> <span data-ttu-id="a91eb-151">Póngase en contacto con su proveedor de VDI para determinar la solución recomendada.</span><span class="sxs-lookup"><span data-stu-id="a91eb-151">Check with your VDI provider to determine the recommended solution.</span></span>

<span data-ttu-id="a91eb-152">Algunas soluciones populares incluyen:</span><span class="sxs-lookup"><span data-stu-id="a91eb-152">Some popular solutions include:</span></span>

- [<span data-ttu-id="a91eb-153">Introducción a FSLogix: | FSLogix | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="a91eb-153">FSLogix Overview - FSLogix | Microsoft Docs</span></span>](/fslogix/overview)
- [<span data-ttu-id="a91eb-154">Configuración de Citrix Profile Management</span><span class="sxs-lookup"><span data-stu-id="a91eb-154">How to Configure Citrix Profile Management</span></span>](https://support.citrix.com/article/CTX222893)

<span data-ttu-id="a91eb-155">También se puede recomendar que, al usar este método, se excluyan las carpetas innecesarias de la carpeta de usuario de la que se ha hecho una copia de seguridad para reducir los tiempos de carga iniciales cuando los usuarios inician sesión en una máquina y se migra el perfil.</span><span class="sxs-lookup"><span data-stu-id="a91eb-155">It is also may be recommended that when using this method unnecessary folders be excluded from the backed-up user folder to reduce initial loading times when users are logging on to a machine and the profile is being migrated.</span></span> <span data-ttu-id="a91eb-156">Si es así, se recomienda excluir las siguientes carpetas de la copia de seguridad para reducir el tamaño.</span><span class="sxs-lookup"><span data-stu-id="a91eb-156">If so, we recommend the following folders be excluded from your backup to reduce size.</span></span>

- <span data-ttu-id="a91eb-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span><span class="sxs-lookup"><span data-stu-id="a91eb-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span></span>
- <span data-ttu-id="a91eb-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span><span class="sxs-lookup"><span data-stu-id="a91eb-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span></span>
- <span data-ttu-id="a91eb-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span><span class="sxs-lookup"><span data-stu-id="a91eb-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span></span>
- <span data-ttu-id="a91eb-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span><span class="sxs-lookup"><span data-stu-id="a91eb-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span></span>

## <a name="known-issues"></a><span data-ttu-id="a91eb-161">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="a91eb-161">Known issues</span></span>

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a><span data-ttu-id="a91eb-162">Microsoft Edge se bloquea en versiones anteriores de XenApp y XenDesktop</span><span class="sxs-lookup"><span data-stu-id="a91eb-162">Microsoft Edge crashes in older versions of XenApp and XenDesktop</span></span>

<span data-ttu-id="a91eb-163">Este problema debería mitigarse en las versiones más recientes. Sin embargo, si encuentra este problema en su entorno, puede solucionar el problema deshabilitando Citrix API Hooks para Edge. Consulte [Cómo deshabilitar Citrix API Hooks por cada aplicación.](https://support.citrix.com/article/CTX107825)</span><span class="sxs-lookup"><span data-stu-id="a91eb-163">This issue should be mitigated in newer versions however if you are encountering this issue in your environment, you can work around the issue by disabling Citrix API Hooks for Edge, see [How to Disable Citrix API Hooks on a Per-application Basis.](https://support.citrix.com/article/CTX107825)</span></span>

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a><span data-ttu-id="a91eb-164">Rendimiento degradado al representar páginas con tablas HTML excepcionalmente grandes</span><span class="sxs-lookup"><span data-stu-id="a91eb-164">Degraded performance when rendering pages with exceptionally large HTML tables</span></span>

<span data-ttu-id="a91eb-165">Se sabe que las siguientes directivas de Citrix ralentizan la representación de páginas HTML con tablas muy grandes (más de 30 000 filas).</span><span class="sxs-lookup"><span data-stu-id="a91eb-165">The following Citrix policies are known to slow rendering of html pages with very large (30,000+ row) tables.</span></span>

- <span data-ttu-id="a91eb-166">Pantalla del teclado automático</span><span class="sxs-lookup"><span data-stu-id="a91eb-166">Automatic keyboard display</span></span>
- <span data-ttu-id="a91eb-167">Control remoto del cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="a91eb-167">Remote the combo box</span></span>

<span data-ttu-id="a91eb-168">Para más información, consulte [Configuración de directivas de experiencia móvil (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html).</span><span class="sxs-lookup"><span data-stu-id="a91eb-168">See [Mobile experience policy settings (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) for more information.</span></span> <span data-ttu-id="a91eb-169">Deshabilitar estas directivas debería mitigar el problema.</span><span class="sxs-lookup"><span data-stu-id="a91eb-169">Disabling these policies should mitigate the issue.</span></span>

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a><span data-ttu-id="a91eb-170">Los escenarios de autorización del Administrador de cuentas de Windows (Azure Sync) producen un error en Edge cuando se ejecutan como una aplicación de conexión directa de Citrix</span><span class="sxs-lookup"><span data-stu-id="a91eb-170">Windows Account Manager authorization scenarios (i.e.  Azure sync) fail in Edge when run as a Citrix seamless application</span></span>

<span data-ttu-id="a91eb-171">Se trata de un problema conocido en Edge y otras aplicaciones que usan WAM (como Office) debido a que los componentes de Windows necesarios para estos escenarios no se inicializan cuando se ejecutan en el modo "directo".</span><span class="sxs-lookup"><span data-stu-id="a91eb-171">This is a known issue in Edge and other applications that use WAM (i.e. Office) due to Windows components necessary for such scenarios not being initialized when running in the “seamless” mode.</span></span> <span data-ttu-id="a91eb-172">Una solución alternativa para este problema:</span><span class="sxs-lookup"><span data-stu-id="a91eb-172">To work around this issue:</span></span>

- <span data-ttu-id="a91eb-173">Use Edge a través de un Escritorio remoto al host de Citrix en lugar de como una aplicación remota directa.</span><span class="sxs-lookup"><span data-stu-id="a91eb-173">Use Edge via a Remote Desktop to the Citrix Host instead of as a seamless remote application.</span></span>
- <span data-ttu-id="a91eb-174">En su lugar, use aplicaciones remotas de Azure Virtual Desktop, que tienen mitigaciones para este problema.</span><span class="sxs-lookup"><span data-stu-id="a91eb-174">Use Azure Virtual Desktop remote apps instead, which has mitigation's for this issue.</span></span>
