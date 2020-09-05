---
title: Reversión de Microsoft Edge para empresas
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 09/02/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Cómo revertir Microsoft Edge a una versión anterior
ms.openlocfilehash: 9f659b0bcdd82f54a814c8ad4157521061cdfa7c
ms.sourcegitcommit: 827a47d641c7ddc1d89be5d5fc0615373dec18b0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993710"
---
# <span data-ttu-id="ab45f-103">Cómo revertir Microsoft Edge a una versión anterior</span><span class="sxs-lookup"><span data-stu-id="ab45f-103">How to roll back Microsoft Edge to a previous version</span></span>

<span data-ttu-id="ab45f-104">Este artículo describe cómo revertir a una versión anterior de Microsoft Edge con la característica de reversión.</span><span class="sxs-lookup"><span data-stu-id="ab45f-104">This article describes how to roll back to a previous version of Microsoft Edge using the rollback feature.</span></span>

>[!NOTE]
><span data-ttu-id="ab45f-105">Este artículo se aplica a Microsoft Edge, versión 86 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ab45f-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="ab45f-106">Introducción a la característica de reversión</span><span class="sxs-lookup"><span data-stu-id="ab45f-106">Introduction to rollback</span></span>

<span data-ttu-id="ab45f-107">La reversión permite sustituir la versión del navegador Microsoft Edge por una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="ab45f-107">Rollback lets you replace your Microsoft Edge browser version with an earlier version.</span></span> <span data-ttu-id="ab45f-108">Esta característica está diseñada para servir como red de seguridad para las empresas que implementan Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab45f-108">This feature is designed to be a safety net for enterprises deploying Microsoft Edge.</span></span> <span data-ttu-id="ab45f-109">Ofrece un método para solucionar problemas con Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab45f-109">It provides a way to troubleshoot issues with Microsoft Edge.</span></span> <span data-ttu-id="ab45f-110">Las ventajas de la reversión son la capacidad para revertir a la versión anterior del explorador de forma fácil y rápida.</span><span class="sxs-lookup"><span data-stu-id="ab45f-110">The benefits of rollback are the ability to revert to previous browser version easily and quickly.</span></span> <span data-ttu-id="ab45f-111">La reversión reduce el impacto potencial de un problema de Microsoft Edge en las operaciones empresariales.</span><span class="sxs-lookup"><span data-stu-id="ab45f-111">Rollback reduces the potential impact that a Microsoft Edge issue has on business operations.</span></span>

## <span data-ttu-id="ab45f-112">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="ab45f-112">Before you begin</span></span>

<span data-ttu-id="ab45f-113">Es importante comprender cómo se instala la característica de reversión en un entorno de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab45f-113">It's important to understand how the rollback feature is installed in a Microsoft Edge environment.</span></span> <span data-ttu-id="ab45f-114">Es posible implementar la reversión mediante dos métodos distintos: manualmente con un paquete MSI o con Microsoft Edge Update y la directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ab45f-114">You can deploy rollback using two different methods: manually with an MSI or by using Microsoft Edge update and Group Policy.</span></span> <span data-ttu-id="ab45f-115">También recomendamos el uso de una selección de directivas de grupo para una implementación más fluida.</span><span class="sxs-lookup"><span data-stu-id="ab45f-115">We also  encourage using a selection of Group Policies for a smoother deployment.</span></span>

### <span data-ttu-id="ab45f-116">Recomendaciones</span><span class="sxs-lookup"><span data-stu-id="ab45f-116">Recommendations</span></span>

<span data-ttu-id="ab45f-117">La característica de reversión tiene como objetivo ser una corrección temporal para problemas que se puedan encontrar en una actualización del explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab45f-117">The rollback feature is meant to be a temporary fix for issues you might find in a Microsoft Edge browser update.</span></span> <span data-ttu-id="ab45f-118">Se recomienda a los usuarios que instalen la última versión del explorador Microsoft Edge para usar la protección proporcionada por las últimas actualizaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ab45f-118">We recommend that users install the latest version of the Microsoft Edge browser to use the protection provided by the latest security updates.</span></span> <span data-ttu-id="ab45f-119">Revertir a una versión anterior supone un riesgo de exposición a problemas de seguridad conocidos.</span><span class="sxs-lookup"><span data-stu-id="ab45f-119">Rollback to an earlier version risks exposure to known security issues.</span></span>

<span data-ttu-id="ab45f-120">Antes de revertir temporalmente a la versión anterior, recomendamos encarecidamente que se habilite la sincronización para todos los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="ab45f-120">Before temporarily rolling back your browser version, we also highly recommend that you enable Sync for all the users in your organization.</span></span> <span data-ttu-id="ab45f-121">Si no se activa la sincronización, se corre el riesgo de pérdida definitiva de datos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ab45f-121">If you don't turn on Sync, there's a risk of permanent browsing data loss.</span></span> <span data-ttu-id="ab45f-122">Para obtener más información sobre la sincronización, consulte [Sugerencias de Microsoft Edge](microsoft-edge-enterprise-sync.md).</span><span class="sxs-lookup"><span data-stu-id="ab45f-122">For more information about Sync, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md).</span></span>

> [!CAUTION]
> <span data-ttu-id="ab45f-123">Usa la reversión solo cuando sea necesario: siempre se corre el riesgo de perder datos.</span><span class="sxs-lookup"><span data-stu-id="ab45f-123">Only use rollback when necessary, there's always the risk of data loss.</span></span>

## <span data-ttu-id="ab45f-124">Habilitar la reversión manual con un MSI</span><span class="sxs-lookup"><span data-stu-id="ab45f-124">Enable rollback manually with an MSI</span></span>

<span data-ttu-id="ab45f-125">Siga los pasos que se indican a continuación para la reversión manual con un MSI.</span><span class="sxs-lookup"><span data-stu-id="ab45f-125">Use the following steps to roll back manually with an MSI.</span></span>

1. <span data-ttu-id="ab45f-126">Deshabilite las actualizaciones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab45f-126">Disable Microsoft Edge Updates.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ab45f-127">Recomendamos instalar las plantillas administrativas más recientes.</span><span class="sxs-lookup"><span data-stu-id="ab45f-127">We recommend that you install the most current Administrative templates.</span></span> <span data-ttu-id="ab45f-128">Para obtener más información, consulte [Descarga e instala la plantilla administrativa de Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span><span class="sxs-lookup"><span data-stu-id="ab45f-128">For more information, see [Download and install the Microsoft Edge administrative template](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span></span>

   - <span data-ttu-id="ab45f-129">Abra el editor de directivas de grupo local y vaya a *Configuración del equipo>Plantillas administrativas>Microsoft Edge Update>Aplicaciones>Microsoft Edge>*.</span><span class="sxs-lookup"><span data-stu-id="ab45f-129">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
   - <span data-ttu-id="ab45f-130">Seleccione **Invalidar directiva de actualización** y, a continuación, seleccione **Habilitar**.</span><span class="sxs-lookup"><span data-stu-id="ab45f-130">Select **Update policy override** and then select **Enabled**.</span></span>
   - <span data-ttu-id="ab45f-131">En **Opciones**, seleccione **Actualización deshabilitada** en la lista desplegable Directiva.</span><span class="sxs-lookup"><span data-stu-id="ab45f-131">Under **Options**, pick **Update disabled** from the Policy dropdown list.</span></span>

2. <span data-ttu-id="ab45f-132">Obtenga el MSI.</span><span class="sxs-lookup"><span data-stu-id="ab45f-132">Get the MSI.</span></span>

   - <span data-ttu-id="ab45f-133">Descargue [desde aquí](https://www.microsoft.com/edge/business/download) el archivo MSI para la versión a la que desea volver.</span><span class="sxs-lookup"><span data-stu-id="ab45f-133">Download the MSI for the version you want to roll back to [from here](https://www.microsoft.com/edge/business/download).</span></span>
   - <span data-ttu-id="ab45f-134">Guarde el MSI en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="ab45f-134">Save the MSI to your desktop.</span></span>

3. <span data-ttu-id="ab45f-135">Ejecute el comando de reversión.</span><span class="sxs-lookup"><span data-stu-id="ab45f-135">Run the rollback command.</span></span>

   - <span data-ttu-id="ab45f-136">Abra el símbolo del sistema de Windows con **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="ab45f-136">Open the Windows command prompt with **Run as administrator**.</span></span>
   - <span data-ttu-id="ab45f-137">Escriba el comando siguiente, donde: *C:\Users\username\Desktop\test* es la ruta de acceso al MSI previamente descargado y FileName es el nombre del archivo .msi:</span><span class="sxs-lookup"><span data-stu-id="ab45f-137">Type the following command, where: *C:\Users\username\Desktop\test* is the path to the MSI you downloaded, and FileName is the name of the .msi file:</span></span><br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > <span data-ttu-id="ab45f-138">Para obtener más información sobre msiexec, consulte [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span><span class="sxs-lookup"><span data-stu-id="ab45f-138">For more information about msiexec, see [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span></span>
   - <span data-ttu-id="ab45f-139">Cierre y vuelva a abrir Microsoft Edge para comprobar que la reversión se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab45f-139">Close and reopen Microsoft Edge to verify that the rollback worked.</span></span> <span data-ttu-id="ab45f-140">En **Configuración y más** (ALT + F), ve a **Configuración** y seleccione **Acerca de Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="ab45f-140">Under **Settings and more** (ALT + F), go to **Settings** and select **About Microsoft Edge**.</span></span>

## <span data-ttu-id="ab45f-141">Habilitar la reversión con Microsoft Edge Update y la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="ab45f-141">Enable rollback with Microsoft Edge update and Group Policy</span></span>

<span data-ttu-id="ab45f-142">Siga los pasos siguientes para habilitar la reversión con Microsoft Edge Update y la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="ab45f-142">Use the following steps to enable rollback with Microsoft Edge update and Group Policy.</span></span>

1. <span data-ttu-id="ab45f-143">Abra el editor de directivas de grupo local y vaya a *Configuración del equipo>Plantillas administrativas>Microsoft Edge Update>Aplicaciones>Microsoft Edge>*.</span><span class="sxs-lookup"><span data-stu-id="ab45f-143">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
2. <span data-ttu-id="ab45f-144">Seleccione **Revertir a la versión de destino** y, a continuación, seleccione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="ab45f-144">Select **Rollback to target version** and then select **Enabled**.</span></span>
3. <span data-ttu-id="ab45f-145">Seleccione **Anular la versión de destino** y elija la versión del explorador a la que se desea revertir.</span><span class="sxs-lookup"><span data-stu-id="ab45f-145">Select **Target version override** and pick the browser version you want to roll back to.</span></span>
4. <span data-ttu-id="ab45f-146">Seleccione **Invalidar directiva de actualización** y, a continuación, seleccione **Habilitar**.</span><span class="sxs-lookup"><span data-stu-id="ab45f-146">Select **Update policy override** and then select **Enabled**.</span></span> <span data-ttu-id="ab45f-147">En **Opciones**, elija una de las siguientes opciones de la lista desplegable Directiva (excepto **Actualización deshabilitada**):</span><span class="sxs-lookup"><span data-stu-id="ab45f-147">Under **Options**, pick one of the following options from the Policy dropdown list (except for **Update disabled**):</span></span>

   - <span data-ttu-id="ab45f-148">Permitir siempre actualizaciones</span><span class="sxs-lookup"><span data-stu-id="ab45f-148">Always allow updates</span></span>
   - <span data-ttu-id="ab45f-149">Solo actualizaciones silenciosas automáticas</span><span class="sxs-lookup"><span data-stu-id="ab45f-149">Automatic silent updates only</span></span>

     > [!NOTE]
     > <span data-ttu-id="ab45f-150">Para forzar una actualización de directiva de grupo, escriba `dsregcmd /status` en el símbolo del sistema de Administrador de Windows (ejecutar como administrador).</span><span class="sxs-lookup"><span data-stu-id="ab45f-150">To force a group policy update, type `dsregcmd /status` at the Windows administrator Command Prompt (Run as administrator).</span></span>

5. <span data-ttu-id="ab45f-151">Haz clic en **Aceptar** para guardar la configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="ab45f-151">Click **OK** to save the policy settings.</span></span> <span data-ttu-id="ab45f-152">La reversión se producirá la próxima vez que Microsoft Edge Update compruebe si hay alguna actualización.</span><span class="sxs-lookup"><span data-stu-id="ab45f-152">Rollback will happen the next time Microsoft Edge Update checks for an update.</span></span> <span data-ttu-id="ab45f-153">Si desea que la actualización se realice antes, puede cambiar el intervalo de sondeo de Microsoft Edge Update o habilitar la reversión mediante un MSI.</span><span class="sxs-lookup"><span data-stu-id="ab45f-153">If you want the update to happen sooner, you can change the Microsoft Edge Update polling interval or enable rollback using an MSI.</span></span>

### <span data-ttu-id="ab45f-154">Errores comunes de reversión</span><span class="sxs-lookup"><span data-stu-id="ab45f-154">Common rollback errors</span></span>

<span data-ttu-id="ab45f-155">Los siguientes errores impiden la reversión:</span><span class="sxs-lookup"><span data-stu-id="ab45f-155">The following errors will prevent rollback:</span></span>

- <span data-ttu-id="ab45f-156">La entrada es una versión de destino no compatible</span><span class="sxs-lookup"><span data-stu-id="ab45f-156">Input is an unsupported target version</span></span>
- <span data-ttu-id="ab45f-157">La entrada es una versión de destino no existente</span><span class="sxs-lookup"><span data-stu-id="ab45f-157">Input is a non-existent target version</span></span>
- <span data-ttu-id="ab45f-158">El formato de la entrada es incorrecto</span><span class="sxs-lookup"><span data-stu-id="ab45f-158">Input is incorrectly formatted</span></span>

### <span data-ttu-id="ab45f-159">Directivas de grupo recomendadas</span><span class="sxs-lookup"><span data-stu-id="ab45f-159">Recommended Group Policies</span></span>

<span data-ttu-id="ab45f-160">Las siguientes directivas de grupo y configuraciones son muy recomendables para la reversión.</span><span class="sxs-lookup"><span data-stu-id="ab45f-160">The following group policies and settings are highly recommended for using rollback.</span></span>

#### <span data-ttu-id="ab45f-161">Directivas de grupo de sincronización</span><span class="sxs-lookup"><span data-stu-id="ab45f-161">Sync Group Policies</span></span>

- <span data-ttu-id="ab45f-162">ForceSync.</span><span class="sxs-lookup"><span data-stu-id="ab45f-162">ForceSync.</span></span> <span data-ttu-id="ab45f-163">Establece ForceSync como habilitado.</span><span class="sxs-lookup"><span data-stu-id="ab45f-163">Set ForceSync to enabled.</span></span> <span data-ttu-id="ab45f-164">Esta directiva forzará la habilitación de la sincronización en todos los usuarios de Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="ab45f-164">This policy will force enable Sync on all Azure Active Directory (Azure AD) users.</span></span> <span data-ttu-id="ab45f-165">Esta directiva solo es válida para las versiones 86 y posteriores de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab45f-165">This policy is only effective for Microsoft Edge versions 86 and later.</span></span>
- <span data-ttu-id="ab45f-166">*Configurar la lista de los tipos que se excluyen de la directiva de sincronización* permite a los administradores controlar los datos que los usuarios pueden sincronizar.</span><span class="sxs-lookup"><span data-stu-id="ab45f-166">The *Configure the list of the types that are excluded from synchronization policy* allows admins to control what data can be synced by users.</span></span>

#### <span data-ttu-id="ab45f-167">Reinicio de las directivas de grupo del explorador</span><span class="sxs-lookup"><span data-stu-id="ab45f-167">Browser restart Group Policies</span></span>

<span data-ttu-id="ab45f-168">Se recomienda forzar un reinicio en los usuarios después de habilitar la reversión.</span><span class="sxs-lookup"><span data-stu-id="ab45f-168">We recommend forcing a restart on users after rollback is enabled.</span></span>

- <span data-ttu-id="ab45f-169">Habilite *Notificar al usuario que se recomienda o se requiere el reinicio del navegador para realizar las actualizaciones pendientes*.</span><span class="sxs-lookup"><span data-stu-id="ab45f-169">Enable *Notify a user that a browser restart is recommended or required for pending updates*.</span></span> <span data-ttu-id="ab45f-170">En opciones, seleccione **Necesario**.</span><span class="sxs-lookup"><span data-stu-id="ab45f-170">Under Options, select **Required**.</span></span>
- <span data-ttu-id="ab45f-171">Habilite *Establecer el período de tiempo de las notificaciones de actualización* y, a continuación, establezca el tiempo deseado en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="ab45f-171">Enable *Set the time period for update notifications* and then set the desired time in milliseconds.</span></span>

## <span data-ttu-id="ab45f-172">Instantánea</span><span class="sxs-lookup"><span data-stu-id="ab45f-172">Snapshot</span></span>

<span data-ttu-id="ab45f-173">Una instantánea es una copia de la versión marcada de la carpeta de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="ab45f-173">A snapshot is a version stamped copy of the user data folder.</span></span> <span data-ttu-id="ab45f-174">Durante una actualización de versión, se crea una instantánea de la versión anterior y se almacena en la carpeta de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="ab45f-174">During a version upgrade, a snapshot of the previous version is made and stored in the snapshot folder.</span></span> <span data-ttu-id="ab45f-175">Tras la reversión, se copia una instantánea de una versión coincidente en la nueva carpeta de datos de usuario y se elimina de la carpeta de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="ab45f-175">After rollback occurs, a version matched snapshot will be copied into the new user data folder and deleted from the snapshot folder.</span></span> <span data-ttu-id="ab45f-176">Si no hay disponible una instantánea que coincida con la versión al cambiar a una versión anterior, la reversión confiará en la sincronización para rellenar los datos de usuario en la nueva versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab45f-176">If no version matched snapshot is available upon downgrade, rollback will rely on Sync to populate user data into the new Microsoft Edge version.</span></span>

<span data-ttu-id="ab45f-177">La directiva de grupo [UserDataSnapshotRetentionLimit] permite establecer un límite para el número de instantáneas que se pueden conservar en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="ab45f-177">The [UserDataSnapshotRetentionLimit] group policy allows you to set a limit for the number of snapshots that can be retained at any given time.</span></span> <span data-ttu-id="ab45f-178">De forma predeterminada, se conservan tres instantáneas.</span><span class="sxs-lookup"><span data-stu-id="ab45f-178">By default, three snapshots are kept.</span></span> <span data-ttu-id="ab45f-179">Puede configurar esta directiva para mantener entre 0 y 5 instantáneas.</span><span class="sxs-lookup"><span data-stu-id="ab45f-179">You can configure this policy to keep from 0-5 snapshots.</span></span>

## <span data-ttu-id="ab45f-180">Preguntas frecuentes</span><span class="sxs-lookup"><span data-stu-id="ab45f-180">Frequently asked questions</span></span>

### <span data-ttu-id="ab45f-181">Reversión manual mediante MSI</span><span class="sxs-lookup"><span data-stu-id="ab45f-181">Manual MSI rollback</span></span>

#### <span data-ttu-id="ab45f-182">¿Qué errores genéricos de MSI se pueden producir?</span><span class="sxs-lookup"><span data-stu-id="ab45f-182">What generic MSI failures that can happen?</span></span>

1. <span data-ttu-id="ab45f-183">Si la directiva de grupo Instalar actualización está deshabilitada, no se realizará la reversión.</span><span class="sxs-lookup"><span data-stu-id="ab45f-183">If the Install update group policy is disabled, rollback won't occur.</span></span>

   - <span data-ttu-id="ab45f-184">Para usar la reversión, asegúrese de que Instalar está **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="ab45f-184">To use rollback, make sure Install is set to **Enabled**.</span></span> <span data-ttu-id="ab45f-185">Si esta directiva está deshabilitada, impide la instalación de los canales de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab45f-185">When this policy is disabled, it prevents Microsoft Edge channels from being installed.</span></span> <span data-ttu-id="ab45f-186">Para obtener más información, consulte [Instalar](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span><span class="sxs-lookup"><span data-stu-id="ab45f-186">For more information, see [Install](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span></span>

2. <span data-ttu-id="ab45f-187">Si no hay actualizaciones predefinidas, se bloquearán las instalaciones de Microsoft Edge, a no ser que *Permitir la experiencia de exploradores en paralelo de Microsoft Edge* está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ab45f-187">If Enlightenment Updates aren't present, Microsoft Edge installations will be blocked unless *Allow Microsoft Edge Side by Side browser experience* is enabled.</span></span>

   - <span data-ttu-id="ab45f-188">Para las versiones de Windows 1903 y 1909: Si la última actualización es anterior a octubre de 2019, es posible que tenga este problema.</span><span class="sxs-lookup"><span data-stu-id="ab45f-188">For Windows versions 1903 and 1909: If your last update was before October 2019, you may have this issue.</span></span>
   - <span data-ttu-id="ab45f-189">Para las versiones de Windows 1709, 1803 y 1809: Si la última actualización es anterior a noviembre de 2019, es posible que tenga este problema.</span><span class="sxs-lookup"><span data-stu-id="ab45f-189">For Windows versions 1709, 1803, and 1809: If your last update was before November 2019, you may have this issue.</span></span><br>
<span data-ttu-id="ab45f-190">Para obtener más información, consulte [Actualizaciones de Windows para admitir la próxima versión de Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)</span><span class="sxs-lookup"><span data-stu-id="ab45f-190">For more information, see [Windows updates to support the next version of Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)</span></span>

#### <span data-ttu-id="ab45f-191">Se mostró el siguiente mensaje de error después de usar el símbolo del sistema y no se realizó la reversión.</span><span class="sxs-lookup"><span data-stu-id="ab45f-191">The following error message was shown after using the Command Prompt and rollback didn't occur.</span></span> <span data-ttu-id="ab45f-192">¿Cuál es el problema?</span><span class="sxs-lookup"><span data-stu-id="ab45f-192">What's wrong?</span></span>

![Mensaje de estado de la reversión](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

<span data-ttu-id="ab45f-194">*ALLOWDOWNGRADE=1* no se ha ejecutado.</span><span class="sxs-lookup"><span data-stu-id="ab45f-194">*ALLOWDOWNGRADE=1* was not executed.</span></span>

### <span data-ttu-id="ab45f-195">Reversión con Microsoft Edge Update y la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="ab45f-195">Microsoft Edge Update and Group Policy rollback</span></span>

#### <span data-ttu-id="ab45f-196">Configuro *Reversión a la versión de destino*, con *Invalidación de directiva de actualización* habilitada; escribo la versión del explorador deseada para *Invalidación de versión de destino*, pero la versión del explorador no es la que esperaba.</span><span class="sxs-lookup"><span data-stu-id="ab45f-196">I set *Rollback to target version*, enabled *Update policy override*, input my desired browser version for *Target version override*, but the browser version wasn't what I expected.</span></span> <span data-ttu-id="ab45f-197">¿Cuál es el problema?</span><span class="sxs-lookup"><span data-stu-id="ab45f-197">What's wrong?</span></span>

<span data-ttu-id="ab45f-198">Algunos errores comunes que impiden la reversión son:</span><span class="sxs-lookup"><span data-stu-id="ab45f-198">Some common errors that prevent rollback are:</span></span>

- <span data-ttu-id="ab45f-199">Si no se ha establecido Revertir a la versión de destino, la reversión no se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="ab45f-199">If Rollback to target version isn't set, rollback will not be executed.</span></span>
- <span data-ttu-id="ab45f-200">Existe uno de los siguientes problemas con la configuración de invalidación de la versión de destino:</span><span class="sxs-lookup"><span data-stu-id="ab45f-200">There are one of the following issues with the target version override setting:</span></span>

  - <span data-ttu-id="ab45f-201">Invalidación de versión de destino se ha establecido en una versión de destino no compatible.</span><span class="sxs-lookup"><span data-stu-id="ab45f-201">Target version override is set to an unsupported target version.</span></span>
  - <span data-ttu-id="ab45f-202">Invalidación de versión de destino se ha establecido en una versión de destino que no existe.</span><span class="sxs-lookup"><span data-stu-id="ab45f-202">Target version override is set to a non-existent target version.</span></span>
  - <span data-ttu-id="ab45f-203">La entrada de Invalidación de versión de destino tiene un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="ab45f-203">Target version override input is incorrectly formatted.</span></span>

- <span data-ttu-id="ab45f-204">Si se establece la Invalidación de directiva de actualización en "Actualizaciones deshabilitadas", Microsoft Edge Update no aceptará ninguna actualización y no se ejecutará la reversión.</span><span class="sxs-lookup"><span data-stu-id="ab45f-204">If Update policy override is set to "Updates disabled", Microsoft Edge Update won't accept any updates and rollback isn't executed.</span></span>

### <span data-ttu-id="ab45f-205">Configuro todas las directivas de grupo correctamente, pero no se ha ejecutado la reversión.</span><span class="sxs-lookup"><span data-stu-id="ab45f-205">I set all the group policies correctly, but rollback didn't execute.</span></span> <span data-ttu-id="ab45f-206">¿Qué ha ocurrido?</span><span class="sxs-lookup"><span data-stu-id="ab45f-206">What happened?</span></span>

<span data-ttu-id="ab45f-207">Microsoft Edge Update todavía no ha ejecutado una búsqueda de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="ab45f-207">Microsoft Edge Update hasn't run a check for updates yet.</span></span> <span data-ttu-id="ab45f-208">De manera predeterminada, la actualización automática busca actualizaciones cada 10 horas.</span><span class="sxs-lookup"><span data-stu-id="ab45f-208">By default, auto-update checks for updates every 10 hours.</span></span> <span data-ttu-id="ab45f-209">Para solucionar este problema, puede cambiar el intervalo de sondeo de Microsoft Edge Update con la directiva de grupo de invalidación del período de búsqueda actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="ab45f-209">You can fix this issue by changing Microsoft Edge Update's polling interval with the Auto-update check period override group policy.</span></span> <span data-ttu-id="ab45f-210">Para obtener más información, consulte la directiva [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes).</span><span class="sxs-lookup"><span data-stu-id="ab45f-210">For more information, see the [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes) policy.</span></span>

### <span data-ttu-id="ab45f-211">Como administrador de TI, he seguido todos los pasos para revertir correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab45f-211">As an IT admin, I followed all the steps for rollback correctly.</span></span> <span data-ttu-id="ab45f-212">Solo se revirtió una parte del grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="ab45f-212">Only a portion of my user group was rolled back.</span></span> <span data-ttu-id="ab45f-213">¿Por qué todavía no se han revertido el resto de usuarios?</span><span class="sxs-lookup"><span data-stu-id="ab45f-213">Why haven't the other users been rolled back yet?</span></span>

<span data-ttu-id="ab45f-214">La configuración de directiva de grupo todavía no se ha sincronizado con todos los clientes.</span><span class="sxs-lookup"><span data-stu-id="ab45f-214">The group policy setting hasn't synced to all the clients yet.</span></span> <span data-ttu-id="ab45f-215">Cuando los administradores configuran una directiva de grupo, los clientes no reciben esta configuración de forma instantánea.</span><span class="sxs-lookup"><span data-stu-id="ab45f-215">When admins set a group policy, clients don't receive these settings instantaneously.</span></span> <span data-ttu-id="ab45f-216">Puede [Forzar una actualización de directiva de grupo remota](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="ab45f-216">You can [Force a Remote Group Policy Refresh](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11)).</span></span>


## <span data-ttu-id="ab45f-217">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ab45f-217">See also</span></span>

- [<span data-ttu-id="ab45f-218">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ab45f-218">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
