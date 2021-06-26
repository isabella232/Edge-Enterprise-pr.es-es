---
title: Diagnosticar y corregir problemas de sincronización de Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Instrucciones y herramientas que un administrador de Microsoft Edge puede usar para solucionar los problemas comunes de sincronización de la empresa
ms.openlocfilehash: d934e1ad73500fcb7f15bcd7dd29cb0f905577c5
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617910"
---
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a><span data-ttu-id="f6a63-103">Diagnosticar y corregir problemas de sincronización de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6a63-103">Diagnose and fix Microsoft Edge sync issues</span></span>

<span data-ttu-id="f6a63-104">En este artículo se proporcionan instrucciones de solución de problemas para los problemas de sincronización más frecuentes en un entorno de Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="f6a63-104">This article provides troubleshooting guidance for the most commonly encountered sync issues in an Azure Active Directory (Azure AD) environment.</span></span> <span data-ttu-id="f6a63-105">También incluye las herramientas recomendadas para recopilar los registros necesarios para solucionar un problema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="f6a63-105">It also includes the recommended tools for gathering the logs needed for troubleshooting a sync issue.</span></span>

<span data-ttu-id="f6a63-106">Si un usuario está experimentando un problema al sincronizar datos del explorador en sus dispositivos, puede intentar [restablecer la sincronización](edge-learnmore-reset-data-in-cloud.md). Si esto no funciona, los administradores o el personal de soporte técnico pueden usar las siguientes instrucciones para solucionar un problema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="f6a63-106">If a user is experiencing an issue syncing browser data across their devices they can try [resetting sync](edge-learnmore-reset-data-in-cloud.md). If this doesn't work, admins or support staff can use the following guidance to fix a sync issue.</span></span>

> [!NOTE]
> <span data-ttu-id="f6a63-107">Se aplica a la versión 77 de Microsoft Edge o posteriores, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="f6a63-107">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="identity-issues-versus-sync-issues"></a><span data-ttu-id="f6a63-108">Problemas de identidad versus problemas de sincronización</span><span class="sxs-lookup"><span data-stu-id="f6a63-108">Identity issues versus sync issues</span></span>

<span data-ttu-id="f6a63-109">Antes de comenzar, es importante comprender la diferencia entre los problemas de identidad y los problemas de sincronización.</span><span class="sxs-lookup"><span data-stu-id="f6a63-109">Before you begin it's important to understand the difference between identity issues and sync issues.</span></span> <span data-ttu-id="f6a63-110">Un caso de uso popular para mantener la identidad del usuario en el explorador es admitir la sincronización. Por este motivo, los problemas de identidad se confunden con frecuencia con los problemas de sincronización.</span><span class="sxs-lookup"><span data-stu-id="f6a63-110">A popular use case for maintaining user identity in the browser is to support sync. For this reason, identity issues are frequently confused with sync issues.</span></span> <span data-ttu-id="f6a63-111">Aprende la diferencia entre un problema de identidad y uno de sincronización antes de empezar a solucionar problemas de sincronización.</span><span class="sxs-lookup"><span data-stu-id="f6a63-111">Understand the difference between identity and sync issue before you start troubleshooting sync.</span></span>

<span data-ttu-id="f6a63-112">Antes de tratar un problema como un problema de sincronización, comprueba si el usuario ha iniciado sesión en el explorador con una cuenta válida.</span><span class="sxs-lookup"><span data-stu-id="f6a63-112">Before you treat an issue as a sync issue, check to see if the user is signed into the browser with a valid account.</span></span>

<span data-ttu-id="f6a63-113">La siguiente captura de pantalla muestra un ejemplo de un error de identidad.</span><span class="sxs-lookup"><span data-stu-id="f6a63-113">The next screenshot shows an example of an identity error.</span></span> <span data-ttu-id="f6a63-114">El error es "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea",** que se encuentra en *edge://sync-internals* en **Credenciales:**</span><span class="sxs-lookup"><span data-stu-id="f6a63-114">The error is "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**", which is found in *edge://sync-internals* under **Credentials**:</span></span>

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="common-sync-issues"></a><span data-ttu-id="f6a63-116">Problemas comunes de sincronización</span><span class="sxs-lookup"><span data-stu-id="f6a63-116">Common sync issues</span></span>

### <a name="issue-cant-access-m365-or-azure-information-protection-subscription"></a><span data-ttu-id="f6a63-117">Problema: no se puede acceder a la suscripción de M365 o Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="f6a63-117">Issue: Can't access M365 or Azure Information Protection subscription</span></span>

<span data-ttu-id="f6a63-118">¿Tiene una suscripción anterior de M365 o Azure Information Protection (AIP) que expiró y se reemplazó por una nueva suscripción?</span><span class="sxs-lookup"><span data-stu-id="f6a63-118">Do you have a previous M365 or Azure Information Protection (AIP) subscription that expired and then replaced with a new subscription?</span></span> <span data-ttu-id="f6a63-119">En ese caso, la identificación del inquilino ha cambiado y es necesario restablecer los datos de servicio.</span><span class="sxs-lookup"><span data-stu-id="f6a63-119">If so, then the tenant ID has changed and the service data needs to be reset.</span></span> <span data-ttu-id="f6a63-120">Consulte las instrucciones para restablecer los datos en el problema del **error de Cryptographer encontrado**.</span><span class="sxs-lookup"><span data-stu-id="f6a63-120">See the instructions for resetting data in the **Cryptographer error encountered** issue.</span></span>

### <a name="issue-sync-is-not-available-for-this-account"></a><span data-ttu-id="f6a63-121">Problema: "La sincronización no está disponible para esta cuenta".</span><span class="sxs-lookup"><span data-stu-id="f6a63-121">Issue: “Sync is not available for this account.”</span></span>

<span data-ttu-id="f6a63-122">Si se produce este error en una cuenta de Azure Active Directory, o si aparece DISABLED_BY_ADMIN en *edge://sync-internals*, sigue los pasos del siguiente procedimiento de manera secuencial hasta que se solucione el problema.</span><span class="sxs-lookup"><span data-stu-id="f6a63-122">If this error is encountered for an Azure Active Directory account, or if DISABLED_BY_ADMIN appears in *edge://sync-internals*, follow the steps in the next procedure sequentially until the problem is fixed.</span></span>

> [!NOTE]
> <span data-ttu-id="f6a63-123">Como el origen de este error suele ser un cambio de configuración en una cuenta empresarial de Azure Active Directory, estos pasos de solución de problemas solo los puede realizar un administrador de inquilinos y no los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="f6a63-123">Because the source of this error is usually requires a configuration change in an Azure Active Directory tenant, these troubleshooting steps can only performed by a tenant admin and not by end users.</span></span>

1. <span data-ttu-id="f6a63-124">Comprueba que el inquilino empresarial tenga una suscripción compatible con M365.</span><span class="sxs-lookup"><span data-stu-id="f6a63-124">Verify that the enterprise tenant has a supported M365 subscription.</span></span> <span data-ttu-id="f6a63-125">Aquí se proporciona la lista actual de los tipos de suscripción [aquí](/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="f6a63-125">The current list of available subscription types is [provided here](/azure/information-protection/activate-office365).</span></span> <span data-ttu-id="f6a63-126">Si el inquilino no tiene una suscripción compatible, puede comprar Azure Information Protection por separado o actualizar a una de las suscripciones compatibles.</span><span class="sxs-lookup"><span data-stu-id="f6a63-126">If the tenant doesn't have a supported subscription, they can either purchase Azure Information Protection separately, or upgrade to one of the supported subscriptions.</span></span>
2. <span data-ttu-id="f6a63-127">Si hay disponible una suscripción compatible, compruebe que el inquilino tenga disponible Azure Information Protection (AIP).</span><span class="sxs-lookup"><span data-stu-id="f6a63-127">If a supported subscription is available, verify that the tenant has Azure Information Protection (AIP) available.</span></span> <span data-ttu-id="f6a63-128">Las instrucciones para comprobar el estado de AIP y, si es necesario, activar AIP [aquí](/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="f6a63-128">The instructions for checking the AIP status and, if necessary, activating AIP are [here](/azure/information-protection/activate-office365).</span></span>
3. <span data-ttu-id="f6a63-129">Si el paso 2 muestra que AIP está activo pero la sincronización sigue sin funcionar, activa la itinerancia de estado empresarial (ESR).</span><span class="sxs-lookup"><span data-stu-id="f6a63-129">If step 2 shows that AIP is active but sync still doesn't work, turn on Enterprise State Roaming (ESR).</span></span> <span data-ttu-id="f6a63-130">[Aquí](/azure/active-directory/devices/enterprise-state-roaming-enable) se indican las instrucciones para habilitar ESR.</span><span class="sxs-lookup"><span data-stu-id="f6a63-130">The instructions for enabling ESR are [here](/azure/active-directory/devices/enterprise-state-roaming-enable).</span></span> <span data-ttu-id="f6a63-131">Ten en cuenta que ESR no necesita mantenerse activa.</span><span class="sxs-lookup"><span data-stu-id="f6a63-131">Note that ESR does not need to stay on.</span></span> <span data-ttu-id="f6a63-132">Puede desactivar ESR si este paso soluciona el problema.</span><span class="sxs-lookup"><span data-stu-id="f6a63-132">You can turn off ESR if this step fixes the issue.</span></span>
4. <span data-ttu-id="f6a63-133">Confirme que Azure Information Protection no tiene un ámbito a través de una directiva de incorporación.</span><span class="sxs-lookup"><span data-stu-id="f6a63-133">Confirm that Azure Information Protection is not scoped via an onboarding policy.</span></span> <span data-ttu-id="f6a63-134">Puede usar el applet [Get-AadrmOnboardingControlPolicy](/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) de PowerShell para ver si el ámbito está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f6a63-134">You can use the [Get-AadrmOnboardingControlPolicy](/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet to see if scoping is enabled.</span></span> <span data-ttu-id="f6a63-135">Los dos ejemplos siguientes muestran una configuración sin ámbito y una configuración con ámbito para un grupo de seguridad específico.</span><span class="sxs-lookup"><span data-stu-id="f6a63-135">The next two examples show an unscoped configuration and a configuration scoped to a specific security group.</span></span>

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```

   <span data-ttu-id="f6a63-136">Si el ámbito está habilitado, el usuario afectado debe agregarse al grupo de seguridad del ámbito o debería quitarse.</span><span class="sxs-lookup"><span data-stu-id="f6a63-136">If scoping is enabled, the affected user should either be added to the security group for the scope, or the scope should be removed.</span></span> <span data-ttu-id="f6a63-137">En el ejemplo siguiente, la integración tiene ámbito AIP para el grupo de seguridad indicado y el ámbito debe quitarse con el sub applet set-AadrmOnboardingControlPolicy[](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell de [.](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps)</span><span class="sxs-lookup"><span data-stu-id="f6a63-137">In the example below, onboarding has scoped AIP to the indicated security group and the scoping should be removed with the [Set-AadrmOnboardingControlPolicy](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet.</span></span>

5. <span data-ttu-id="f6a63-138">Confirma que IP DomainService esté activado en el espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="f6a63-138">Confirm that the IPCv3Service is turned on in the tenant.</span></span> <span data-ttu-id="f6a63-139">El applet de PowerShell [Get-AadrmConfiguración](/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) muestra el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="f6a63-139">The [Get-AadrmConfiguration](/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps)  PowerShell applet shows the status of the service.</span></span>

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Comprueba si IPCv3Service está habilitado.":::

6. <span data-ttu-id="f6a63-141">Si el problema no se solucionó, contacta el [soporte técnico de Microsoft Edge](https://www.microsoftedgeinsider.com/support).</span><span class="sxs-lookup"><span data-stu-id="f6a63-141">If the issue isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).</span></span>

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a><span data-ttu-id="f6a63-142">Problema: Se atasca en "Configurando la sincronización..." o "No se pudo conectar al servidor de sincronización.</span><span class="sxs-lookup"><span data-stu-id="f6a63-142">Issue: Stuck at "Setting up sync..." or “Couldn’t connect to the sync server.</span></span> <span data-ttu-id="f6a63-143">Reintentar..."</span><span class="sxs-lookup"><span data-stu-id="f6a63-143">Retrying…”</span></span>

1. <span data-ttu-id="f6a63-144">Cierra y vuelve a iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="f6a63-144">Try to sign out and then sign in.</span></span>
2. <span data-ttu-id="f6a63-145">Ve a *edge://sync-internals*.</span><span class="sxs-lookup"><span data-stu-id="f6a63-145">Go to *edge://sync-internals*.</span></span> <span data-ttu-id="f6a63-146">Si en la sección "**Type info**" está presente el siguiente error, entonces ve al siguiente problema, **error de criptografía encontrado**.</span><span class="sxs-lookup"><span data-stu-id="f6a63-146">If under the "**Type info**" section the following error is present, then  skip to the following issue, **Cryptographer error encountered**.</span></span>

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. <span data-ttu-id="f6a63-147">Intenta hacer ping al punto de conexión del servidor.</span><span class="sxs-lookup"><span data-stu-id="f6a63-147">Try pinging the server endpoint.</span></span> <span data-ttu-id="f6a63-148">El punto de conexión del servidor para un cliente está disponible en *edge://sync-internals*.</span><span class="sxs-lookup"><span data-stu-id="f6a63-148">The server endpoint for a client is available in *edge://sync-internals*.</span></span> <span data-ttu-id="f6a63-149">En la siguiente captura de pantalla se muestra la información del punto de conexión bajo **Información del entorno**.</span><span class="sxs-lookup"><span data-stu-id="f6a63-149">The next screenshot shows endpoint information under **Environment Info**.</span></span>

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Información de puntos de conexión":::

4. <span data-ttu-id="f6a63-151">Si el punto de conexión del servidor está vacío, o no se puede hacer ping al servidor y hay un firewall presente en el entorno, asegúrate de que los puntos de conexión de servicio necesarios estén disponibles en el computador del cliente.</span><span class="sxs-lookup"><span data-stu-id="f6a63-151">If the server endpoint is empty, or if server cannot be pinged and a firewall is present in the environment, confirm that the necessary service endpoints are available to the client computer.</span></span>

   - <span data-ttu-id="f6a63-152">Puntos de conexión del servicio de sincronización de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="f6a63-152">Microsoft Edge sync service endpoints:</span></span>
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - <span data-ttu-id="f6a63-153">Puntos de conexión de Azure Information Protection:</span><span class="sxs-lookup"><span data-stu-id="f6a63-153">Azure Information Protection endpoints:</span></span>
      - <span data-ttu-id="f6a63-154">[https://api.aadrm.com](https://api.aadrm.com)(para la mayoría de los espacios empresariales)</span><span class="sxs-lookup"><span data-stu-id="f6a63-154">[https://api.aadrm.com](https://api.aadrm.com) (for most tenants)</span></span>
      - <span data-ttu-id="f6a63-155">[https://api.aadrm.de](https://api.aadrm.de)(para los espacios empresariales de Alemania)</span><span class="sxs-lookup"><span data-stu-id="f6a63-155">[https://api.aadrm.de](https://api.aadrm.de) (for tenants in Germany)</span></span>
      - <span data-ttu-id="f6a63-156">[https://api.aadrm.cn](https://api.aadrm.cn)(para los espacios empresariales de China)</span><span class="sxs-lookup"><span data-stu-id="f6a63-156">[https://api.aadrm.cn](https://api.aadrm.cn) (for tenants in China)</span></span>
   - <span data-ttu-id="f6a63-157">[Puntos de conexión del Servicio de notificaciones de Windows](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).</span><span class="sxs-lookup"><span data-stu-id="f6a63-157">[Windows Notification Service endpoints](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).</span></span>

5. <span data-ttu-id="f6a63-158">Si el problema aún no está arreglado, contacta el [soporte técnico de Microsoft Edge](https://www.microsoftedgeinsider.com/support).</span><span class="sxs-lookup"><span data-stu-id="f6a63-158">If the issue still isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).</span></span>

### <a name="issue-cryptographer-error-encountered"></a><span data-ttu-id="f6a63-159">Problema: Se encontró un error de criptografía</span><span class="sxs-lookup"><span data-stu-id="f6a63-159">Issue: Cryptographer error encountered</span></span>

<span data-ttu-id="f6a63-160">Este error está visible en la parte inferior de **Escribir información** en *edge://sync-internals* y puede significar que es necesario restablecer los datos del lado del servicio del usuario.</span><span class="sxs-lookup"><span data-stu-id="f6a63-160">This error is visible under **Type info** in *edge://sync-internals* and may mean that the user's service side data needs to be reset.</span></span> <span data-ttu-id="f6a63-161">En el siguiente ejemplo se muestra un mensaje de error de criptografía:</span><span class="sxs-lookup"><span data-stu-id="f6a63-161">The following example shows a cryptography error message:</span></span>
<br><span data-ttu-id="f6a63-162">"Error:GenerateCryptoErrorsForTypes@.. /.. /components/sync/driver/data_type_manager_impl.cc:42, se encontró un error de criptografía".</span><span class="sxs-lookup"><span data-stu-id="f6a63-162">"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".</span></span>

1. <span data-ttu-id="f6a63-163">Reinicia Microsoft Edge y navega hasta el *edge://sync-internals* y comprueba la sección "**Estado de la clave de cuenta de AAD**"</span><span class="sxs-lookup"><span data-stu-id="f6a63-163">Restart Microsoft Edge and navigate to *edge://sync-internals* and check the “**AAD Account Key Status**” section</span></span>
   - <span data-ttu-id="f6a63-164">"Correcto" en "Último resultado de MIP": el error de criptografía significa que los datos del servidor pueden haber sido cifrados con una clave perdida.</span><span class="sxs-lookup"><span data-stu-id="f6a63-164">"Success" in "Last MIP Result": the cryptographer error means server data might be encrypted with a lost key.</span></span> <span data-ttu-id="f6a63-165">Es necesario restablecer los datos para reanudar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="f6a63-165">Data reset is needed to resume sync.</span></span>
   - <span data-ttu-id="f6a63-166">"Ningún permiso" en "Último resultado de MIP": es posible que se deba a un cambio de Azure AD o a cambios en la suscripción de inquilino.</span><span class="sxs-lookup"><span data-stu-id="f6a63-166">"No permissions" in "Last MIP Result": It is possibly caused by an Azure AD change or tenant subscription changes.</span></span> <span data-ttu-id="f6a63-167">Es necesario restablecer los datos para reanudar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="f6a63-167">Data reset is needed to resume sync.</span></span>
   - <span data-ttu-id="f6a63-168">Otros errores pueden significar problemas de configuración del servidor.</span><span class="sxs-lookup"><span data-stu-id="f6a63-168">Other errors may mean server configuration issues.</span></span>
2. <span data-ttu-id="f6a63-169">Si es necesario restablecer los datos, consulta [Restablecer datos de Microsoft Edge en la nube](edge-learnmore-reset-data-in-cloud.md).</span><span class="sxs-lookup"><span data-stu-id="f6a63-169">If data reset is needed, see [Reset Microsoft Edge data in the cloud](edge-learnmore-reset-data-in-cloud.md).</span></span>

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a><span data-ttu-id="f6a63-170">Problema: "Tu administrador ha desactivado la sincronización."</span><span class="sxs-lookup"><span data-stu-id="f6a63-170">Issue: “Sync has been turned off by your administrator.”</span></span>

<span data-ttu-id="f6a63-171">Asegúrese de que las [Directiva SyncDisabled](./microsoft-edge-policies.md#syncdisabled)  no esté establecida.</span><span class="sxs-lookup"><span data-stu-id="f6a63-171">Make sure that the [SyncDisabled policy](./microsoft-edge-policies.md#syncdisabled)  is not set.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6a63-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6a63-172">See also</span></span>

- [<span data-ttu-id="f6a63-173">Sincronización de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f6a63-173">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="f6a63-174">Microsoft Edge y Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="f6a63-174">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="f6a63-175">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f6a63-175">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)