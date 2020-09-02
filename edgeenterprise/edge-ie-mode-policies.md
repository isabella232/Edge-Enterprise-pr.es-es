---
title: Configurar directivas de modo IE
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 03/25/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar directivas de modo IE
ms.openlocfilehash: 2d2ded3a3fb338bdf2d815d681b52249007945ac
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981090"
---
# <span data-ttu-id="ab393-103">Configurar directivas de modo IE</span><span class="sxs-lookup"><span data-stu-id="ab393-103">Configure IE mode policies</span></span>

<span data-ttu-id="ab393-104">Este artículo explica cómo se configuran las directivas de modo IE.</span><span class="sxs-lookup"><span data-stu-id="ab393-104">This article explains how to configure IE mode policies.</span></span>

> [!NOTE]
> <span data-ttu-id="ab393-105">Este artículo se aplica a los canales de Microsoft Edge **Estable**, **Beta** y **Dev**, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ab393-105">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

<span data-ttu-id="ab393-106">La configuración del modo IE requiere tres pasos:</span><span class="sxs-lookup"><span data-stu-id="ab393-106">Configuring IE mode requires three steps:</span></span>

1. [<span data-ttu-id="ab393-107">Configurar la integración de Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="ab393-107">Configure Internet Explorer integration</span></span>](#configure-internet-explorer-integration)
2. [<span data-ttu-id="ab393-108">Redirigir sitios de Microsoft Edge al modo IE</span><span class="sxs-lookup"><span data-stu-id="ab393-108">Redirect sites from Microsoft Edge to IE mode</span></span>](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. <span data-ttu-id="ab393-109">(Opcional) [Redirigir sitios de IE a Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)</span><span class="sxs-lookup"><span data-stu-id="ab393-109">(Optional) [Redirect sites from IE to Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)</span></span>

> [!NOTE]
> <span data-ttu-id="ab393-110">Las directivas para habilitar el modo IE se pueden configurar con Intune.</span><span class="sxs-lookup"><span data-stu-id="ab393-110">Policies to enable IE mode can be configured through Intune.</span></span> <span data-ttu-id="ab393-111">Para obtener más información, consulta [Agregar Microsoft Edge a Microsoft Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json) y [Configurar las directivas de Microsoft Edge con Microsoft Intune](https://docs.microsoft.com/DeployEdge/configure-edge-with-intune).</span><span class="sxs-lookup"><span data-stu-id="ab393-111">For more information, see [Add Microsoft Edge to Microsoft Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json) and [Configure Microsoft Edge policies with Microsoft Intune](https://docs.microsoft.com/DeployEdge/configure-edge-with-intune).</span></span>

## <span data-ttu-id="ab393-112">Configurar la integración de Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="ab393-112">Configure Internet Explorer integration</span></span>

<span data-ttu-id="ab393-113">Se puede configurar Internet Explorer para abrirlo directamente desde Microsoft Edge (modo IE).</span><span class="sxs-lookup"><span data-stu-id="ab393-113">You can configure Internet Explorer to open directly within Microsoft Edge (IE mode).</span></span> <span data-ttu-id="ab393-114">También se puede configurar Internet Explorer para abrirlo con una ventana independiente de Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="ab393-114">You can also configure Internet Explorer to open with a standalone Internet Explorer 11 window.</span></span> <span data-ttu-id="ab393-115">La mayoría de los usuarios prefieren abrir los sitios directamente desde Microsoft Edge en modo IE.</span><span class="sxs-lookup"><span data-stu-id="ab393-115">Most users prefer when sites open directly within Microsoft Edge in IE mode.</span></span>

### <span data-ttu-id="ab393-116">Habilitar la integración de Internet Explorer mediante la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="ab393-116">Enable Internet Explorer integration using Group Policy</span></span>

1. <span data-ttu-id="ab393-117">Descarga u usa la última [plantilla administrativa de Microsoft Edge](https://www.microsoft.com/en-us/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="ab393-117">Download and use the latest [Microsoft Edge Policy Template](https://www.microsoft.com/en-us/edge/business/download).</span></span>
2. <span data-ttu-id="ab393-118">Abre el Editor de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="ab393-118">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="ab393-119">Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="ab393-119">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
4. <span data-ttu-id="ab393-120">Haz doble clic en **Configurar la integración de Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="ab393-120">Double-click **Configure Internet Explorer integration**.</span></span>
5. <span data-ttu-id="ab393-121">Seleccione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="ab393-121">Select **Enabled**.</span></span>
6. <span data-ttu-id="ab393-122">En **Opciones**, establece el valor de la lista desplegable en</span><span class="sxs-lookup"><span data-stu-id="ab393-122">Under **Options**, set the dropdown value to</span></span> 
   -  <span data-ttu-id="ab393-123">**Modo de Internet Explorer** para que los sitios se abran en modo IE en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ab393-123">**Internet Explorer mode** if you want sites to open in IE mode on Microsoft Edge</span></span>
   -  <span data-ttu-id="ab393-124">**Internet Explorer 11** si quiere que los sitios se abran en una ventana independiente de Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="ab393-124">**Internet Explorer 11** if you want sites to open in a standalone Internet Explorer 11 window</span></span>
   -  <span data-ttu-id="ab393-125">**Ninguno** para deshabilitar el modo de Internet Explorer cuando se establece por edge://flags o mediante opciones de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="ab393-125">**None** if you want to stop users from configuring Internet Explorer mode via edge://flags or through the command line</span></span>

   > [!NOTE]
   > <span data-ttu-id="ab393-126">Establecer la directiva en **Deshabilitado** implica que la directiva deshabilita el modo IE, pero puede establecerse con las opciones de línea de comandos o edge://flags.</span><span class="sxs-lookup"><span data-stu-id="ab393-126">Setting the policy to **Disabled** implies IE mode is disabled by policy, but can be set through edge://flags or command line options.</span></span>
7. <span data-ttu-id="ab393-127">Haz clic en **Aceptar** o en **Aplicar** para guardar esta configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="ab393-127">Click **OK** or **Apply** to save this policy setting.</span></span>

## <span data-ttu-id="ab393-128">Redirigir sitios de Microsoft Edge al modo IE</span><span class="sxs-lookup"><span data-stu-id="ab393-128">Redirect sites from Microsoft Edge to IE mode</span></span>

<span data-ttu-id="ab393-129">Hay 2 opciones para identificar qué sitios deben abrirse en modo IE:</span><span class="sxs-lookup"><span data-stu-id="ab393-129">There are two options for identifying which sites should open in IE mode:</span></span>

- <span data-ttu-id="ab393-130">(Recomendado) [Configurar sitios en la lista de sitios de empresa](#configure-sites-on-the-enterprise-site-list)</span><span class="sxs-lookup"><span data-stu-id="ab393-130">(Recommended) [Configure sites on the Enterprise Site list](#configure-sites-on-the-enterprise-site-list)</span></span>
- [<span data-ttu-id="ab393-131">Configurar todos los sitios de intranet</span><span class="sxs-lookup"><span data-stu-id="ab393-131">Configure all Intranet sites</span></span>](#configure-all-intranet-sites)

### <span data-ttu-id="ab393-132">Configurar los sitios de la lista de sitios de empresa</span><span class="sxs-lookup"><span data-stu-id="ab393-132">Configure sites on the Enterprise Site list</span></span>

<span data-ttu-id="ab393-133">Puedes usar las siguientes directivas de grupo para configurar sitios específicos a abrir en modo IE:</span><span class="sxs-lookup"><span data-stu-id="ab393-133">You can use the following group policies to configure specific sites to open in IE mode:</span></span>

- <span data-ttu-id="ab393-134">[Usar la lista de sitios web de IE del modo de empresa](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)</span><span class="sxs-lookup"><span data-stu-id="ab393-134">[Use the Enterprise Mode IE website list](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)</span></span>
- <span data-ttu-id="ab393-135">[Configurar la lista de sitios de modo de empresa](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, versión 78 o posterior)</span><span class="sxs-lookup"><span data-stu-id="ab393-135">[Configure the Enterprise Mode Site List](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, version 78 or later)</span></span><br/><span data-ttu-id="ab393-136">Esta directiva permite crear una lista de sitios del modo de empresa independiente para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab393-136">This policy lets you create a separate Enterprise Mode Site list for Microsoft Edge.</span></span> <span data-ttu-id="ab393-137">Al habilitar esta directiva, se invalida la configuración de la directiva "Usar la lista de sitios web de IE del modo de empresa", siempre que la opción "Configurar integración de Internet Explorer" esté habilitada.</span><span class="sxs-lookup"><span data-stu-id="ab393-137">Enabling this policy overrides the settings in the "Use the Enterprise Mode IE website list" policy, if "Configure Internet Explorer integration" is enabled.</span></span> <span data-ttu-id="ab393-138">La deshabilitación o la no configuración de esta directiva no afecta al comportamiento predeterminado de la directiva "Configurar integración de Internet Explorer".</span><span class="sxs-lookup"><span data-stu-id="ab393-138">Disabling or not configuring this policy doesn't affect the default behavior of the "Configure Internet Explorer integration" policy.</span></span>
    > [!NOTE]
    > <span data-ttu-id="ab393-139">No es obligatorio configurar la directiva de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab393-139">It is not mandatory to configure the Microsoft Edge policy.</span></span> <span data-ttu-id="ab393-140">Muchas organizaciones usan esto para invalidar, lo que les permite dirigir la Lista de sitios actual a todos los usuarios con la directiva de IE, y dirigir más fácilmente una versión actualizada a las pruebas piloto con la directiva de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab393-140">Many organizations use this as an override, allowing them to target the current Site List at all users with the IE policy, and more easily target an updated version to pilot uses with the Microsoft Edge policy.</span></span>

<span data-ttu-id="ab393-141">Para obtener más información sobre la lista de sitios de modo de empresa, consulta:</span><span class="sxs-lookup"><span data-stu-id="ab393-141">For more information about Enterprise Mode Site lists, see:</span></span>

- [<span data-ttu-id="ab393-142">Usar Enterprise Mode Site List Manager</span><span class="sxs-lookup"><span data-stu-id="ab393-142">Use the Enterprise Mode Site List Manager</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- <span data-ttu-id="ab393-143">[Agregar varios sitios a la lista de sitios del modo de empresa mediante un archivo y la herramienta Enterprise Mode Site List Manager (esquema v.2)](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).</span><span class="sxs-lookup"><span data-stu-id="ab393-143">[Add multiple sites to the Enterprise Mode site list using a file and the Enterprise Mode Site List Manager (schema v.2)](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).</span></span>

### <span data-ttu-id="ab393-144">Configurar usando la directiva de listas de sitios web de IE de modo de empresa</span><span class="sxs-lookup"><span data-stu-id="ab393-144">Configure using the Use the Enterprise Mode IE website list policy</span></span>

<span data-ttu-id="ab393-145">El modo IE puede usar la directiva existente que configura la Lista de sitios de empresas para Internet Explorer, lo que le permite crear y mantener una lista única.</span><span class="sxs-lookup"><span data-stu-id="ab393-145">IE mode can use the existing policy configuring the Enterprise Site List for Internet Explorer, allowing you to create and maintain a single list.</span></span>

1. <span data-ttu-id="ab393-146">Crear o volver a usar una lista de sitios XML</span><span class="sxs-lookup"><span data-stu-id="ab393-146">Create or reuse a Site List XML</span></span>
    1. <span data-ttu-id="ab393-147">Todos los sitios que tengan el elemento _\<open-in\>IE11\</open-in\>_ se abrirán ahora en modo IE.</span><span class="sxs-lookup"><span data-stu-id="ab393-147">All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.</span></span>
2. <span data-ttu-id="ab393-148">Abre el Editor de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="ab393-148">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="ab393-149">Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Componentes de Windows** > **Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="ab393-149">Click **Computer Configuration** > **Administrative Templates** > **Windows Components** > **Internet Explorer**.</span></span>
4. <span data-ttu-id="ab393-150">Haz doble clic en **Usar la lista de sitios web de IE del Modo de empresa**.</span><span class="sxs-lookup"><span data-stu-id="ab393-150">Double-click **Use the Enterprise Mode IE website list**.</span></span>
5. <span data-ttu-id="ab393-151">Seleccione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="ab393-151">Select **Enabled**.</span></span>
6. <span data-ttu-id="ab393-152">En **Opciones**, escribe la ubicación de la lista de sitios web.</span><span class="sxs-lookup"><span data-stu-id="ab393-152">Under **Options**, type the location of website list.</span></span> <span data-ttu-id="ab393-153">Puedes usar una de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="ab393-153">You can use one of the following locations:</span></span>
    - <span data-ttu-id="ab393-154">(Recomendado) Ubicación HTTPS: **https**:**//iemode/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab393-154">(Recommended) HTTPS location: **https**:**//iemode/sites.xml**</span></span>
    - <span data-ttu-id="ab393-155">Archivo de red local: **\\\network\shares\sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab393-155">Local network file: **\\\network\shares\sites.xml**</span></span>
    - <span data-ttu-id="ab393-156">Archivo local: **file:///c:/Users/\<user\>/Documents/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab393-156">Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**</span></span>
7. <span data-ttu-id="ab393-157">Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="ab393-157">Click **OK** or **Apply** to save these settings.</span></span>

### <span data-ttu-id="ab393-158">Configurar con la directiva configurar el modo de empresa de lista de sitios</span><span class="sxs-lookup"><span data-stu-id="ab393-158">Configure using the Configure the Enterprise Mode Site List policy</span></span>

<span data-ttu-id="ab393-159">También es posible configurar el modo IE con una directiva independiente para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab393-159">You can also configure IE mode with a separate policy for Microsoft Edge.</span></span> <span data-ttu-id="ab393-160">Esta directiva adicional permite anular la lista de sitios de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ab393-160">This additional policy allows you to override the IE site list.</span></span> <span data-ttu-id="ab393-161">Por ejemplo, algunas organizaciones dirigirán la lista de sitios de producción a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ab393-161">For example, some organizations will target the production site list to all users.</span></span> <span data-ttu-id="ab393-162">Después, será posible implementar la lista de sitios piloto para un pequeño grupo de usuarios que usen esta directiva.</span><span class="sxs-lookup"><span data-stu-id="ab393-162">You can then deploy the pilot site list to a small group of users using this policy.</span></span>

1. <span data-ttu-id="ab393-163">Crear o volver a usar una lista de sitios XML</span><span class="sxs-lookup"><span data-stu-id="ab393-163">Create or reuse a Site List XML</span></span>
    1. <span data-ttu-id="ab393-164">Todos los sitios que tengan el elemento _\<open-in\>IE11\</open-in\>_ se abrirán ahora en modo IE.</span><span class="sxs-lookup"><span data-stu-id="ab393-164">All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.</span></span>
2. <span data-ttu-id="ab393-165">Abre el Editor de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="ab393-165">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="ab393-166">Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="ab393-166">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
4. <span data-ttu-id="ab393-167">Haz doble clic en **Configurar la lista de sitios del modo de empresa**.</span><span class="sxs-lookup"><span data-stu-id="ab393-167">Double-click **Configure the Enterprise Mode Site List**.</span></span>
5. <span data-ttu-id="ab393-168">Seleccione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="ab393-168">Select **Enabled**.</span></span>
6. <span data-ttu-id="ab393-169">En **Opciones**, escribe la ubicación de la lista de sitios web.</span><span class="sxs-lookup"><span data-stu-id="ab393-169">Under **Options**, type the location of website list.</span></span> <span data-ttu-id="ab393-170">Puedes usar una de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="ab393-170">You can use one of the following locations:</span></span>
    - <span data-ttu-id="ab393-171">(Recomendado) Ubicación HTTPS: **https**:**//iemode/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab393-171">(Recommended) HTTPS location: **https**:**//iemode/sites.xml**</span></span> <!--Trying to keep this from being an active link in MD -->
    - <span data-ttu-id="ab393-172">Archivo de red local: **\\\network\shares\sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab393-172">Local network file: **\\\network\shares\sites.xml**</span></span>
    - <span data-ttu-id="ab393-173">Archivo local: **file:///c:/Users/\<user\>/Documents/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab393-173">Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**</span></span>
7. <span data-ttu-id="ab393-174">Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="ab393-174">Click **OK** or **Apply** to save these settings.</span></span>

### <span data-ttu-id="ab393-175">Configurar todos los sitios de intranet</span><span class="sxs-lookup"><span data-stu-id="ab393-175">Configure all intranet sites</span></span>

<span data-ttu-id="ab393-176">El modo IE se puede configurar como "para todos los sitios" en la zona Intranet local.</span><span class="sxs-lookup"><span data-stu-id="ab393-176">IE mode can be configured as for all sites in the Local Intranet zone.</span></span> <span data-ttu-id="ab393-177">Es posible quitar sitios individuales del modo IE con una lista de sitios de modo de empresa.</span><span class="sxs-lookup"><span data-stu-id="ab393-177">You can remove individual sites from IE mode using an Enterprise Mode Site List.</span></span>

>[!NOTE]
>
> <span data-ttu-id="ab393-178">La zona de Intranet local contiene sitios agregados explícitamente, pero también asigna sitios a esta zona mediante heurística.</span><span class="sxs-lookup"><span data-stu-id="ab393-178">The Local Intranet zone contains explicitly added sites, but also assigns sites to this zone using heuristics.</span></span> <span data-ttu-id="ab393-179">Esto puede incluir nombres de host sin punto (p.ej. **https**:**//nomina**) y sitios que el script de configuración de proxy configura para eludir el proxy.</span><span class="sxs-lookup"><span data-stu-id="ab393-179">This can include dotless host names (e.g. **https**:**//payroll**) and sites that the proxy configuration script configures to bypass the proxy.</span></span> <span data-ttu-id="ab393-180">Si un usuario externo controla DNS o proxy, podría exigir el uso de los sitios web en modo IE.</span><span class="sxs-lookup"><span data-stu-id="ab393-180">If an external party controls DNS or proxy, they could potentially force websites into IE mode.</span></span>

1. <span data-ttu-id="ab393-181">Abre el Editor de directivas de grupo local.</span><span class="sxs-lookup"><span data-stu-id="ab393-181">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="ab393-182">Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="ab393-182">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="ab393-183">Haz doble clic en **Enviar todos los sitios de intranet a Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="ab393-183">Double-click **Send all intranet sites to Internet Explorer**.</span></span>
4. <span data-ttu-id="ab393-184">Selecciona **Habilitado** y luego haz clic en **Aceptar** o **Aplicar** para guardar la configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="ab393-184">Select **Enabled**, and then click **OK** or **Apply** to save the policy settings.</span></span>

## <span data-ttu-id="ab393-185">Redirigir sitios de IE a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ab393-185">Redirect sites from IE to Microsoft Edge</span></span>

<span data-ttu-id="ab393-186">Es posible impedir que los usuarios usen Internet Explorer para los sitios que no lo necesiten.</span><span class="sxs-lookup"><span data-stu-id="ab393-186">You can prevent your users from using Internet Explorer for sites that don't need it.</span></span> <span data-ttu-id="ab393-187">Internet Explorer puede redirigir sitios automáticamente a Microsoft Edge si no están en la lista de sitios.</span><span class="sxs-lookup"><span data-stu-id="ab393-187">Internet Explorer can automatically redirect sites to Microsoft Edge if they aren't on your site list.</span></span>

1. <span data-ttu-id="ab393-188">Abre el Editor de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="ab393-188">Open Group Policy Editor.</span></span>
2. <span data-ttu-id="ab393-189">Haz clic en **Configuración del equipo** > **Herramientas administrativas** > **Componentes de Windows** > **Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="ab393-189">Click **Computer Configuration** > **Administrative Tools** > **Windows Components** > **Internet Explorer**.</span></span>
3. <span data-ttu-id="ab393-190">Haz doble clic en **Enviar todos los sitios que no se incluyan en la lista de sitios del modo de empresa a Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="ab393-190">Double-click **Send all sites not included in the Enterprise Mode Site List to Microsoft Edge.**</span></span>
4. <span data-ttu-id="ab393-191">Selecciona **Habilitado**</span><span class="sxs-lookup"><span data-stu-id="ab393-191">Select **Enabled**</span></span>
5. <span data-ttu-id="ab393-192">Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="ab393-192">Click **OK** or **Apply** to save these settings.</span></span>
6. <span data-ttu-id="ab393-193">Haga doble clic en **configurar qué canal de Microsoft Edge usar para abrir sitios redirigidos**.</span><span class="sxs-lookup"><span data-stu-id="ab393-193">Double-click **Configure which channel of Microsoft Edge to use for opening redirected sites**.</span></span>
7. <span data-ttu-id="ab393-194">Seleccione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="ab393-194">Select **Enabled**.</span></span>
8. <span data-ttu-id="ab393-195">En **Opciones**, selecciona las tres opciones principales para el canal que usará: Internet Explorer se redirigirá a la opción de mayor jerarquía que el usuario haya instalado en el dispositivo:</span><span class="sxs-lookup"><span data-stu-id="ab393-195">Under **Options**, select your top three choices for the channel to use - Internet Explorer will redirect to the highest ranked choice that the user has installed on that device:</span></span>
   - <span data-ttu-id="ab393-196">Microsoft Edge Stable</span><span class="sxs-lookup"><span data-stu-id="ab393-196">Microsoft Edge Stable</span></span>
   - <span data-ttu-id="ab393-197">Microsoft Edge Beta versión 77 o posterior</span><span class="sxs-lookup"><span data-stu-id="ab393-197">Microsoft Edge Beta version 77 or later</span></span>
   - <span data-ttu-id="ab393-198">Microsoft Edge Dev versión 77 o posterior</span><span class="sxs-lookup"><span data-stu-id="ab393-198">Microsoft Edge Dev version 77 or later</span></span>
   - <span data-ttu-id="ab393-199">Microsoft Edge Canary versión 77 o posterior</span><span class="sxs-lookup"><span data-stu-id="ab393-199">Microsoft Edge Canary version 77 or later</span></span>
   - <span data-ttu-id="ab393-200">Microsoft Edge versión 45 o anterior</span><span class="sxs-lookup"><span data-stu-id="ab393-200">Microsoft Edge version 45 or earlier</span></span>
9. <span data-ttu-id="ab393-201">Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="ab393-201">Click **OK** or **Apply** to save these settings.</span></span>

## <span data-ttu-id="ab393-202">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ab393-202">See also</span></span>

- [<span data-ttu-id="ab393-203">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ab393-203">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ab393-204">Acerca del modo IE</span><span class="sxs-lookup"><span data-stu-id="ab393-204">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="ab393-205">Información adicional del modo de empresa</span><span class="sxs-lookup"><span data-stu-id="ab393-205">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)