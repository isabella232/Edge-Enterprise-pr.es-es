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
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a>Diagnosticar y corregir problemas de sincronización de Microsoft Edge

En este artículo se proporcionan instrucciones de solución de problemas para los problemas de sincronización más frecuentes en un entorno de Azure Active Directory (Azure AD). También incluye las herramientas recomendadas para recopilar los registros necesarios para solucionar un problema de sincronización.

Si un usuario está experimentando un problema al sincronizar datos del explorador en sus dispositivos, puede intentar [restablecer la sincronización](edge-learnmore-reset-data-in-cloud.md). Si esto no funciona, los administradores o el personal de soporte técnico pueden usar las siguientes instrucciones para solucionar un problema de sincronización.

> [!NOTE]
> Se aplica a la versión 77 de Microsoft Edge o posteriores, a menos que se indique lo contrario.

## <a name="identity-issues-versus-sync-issues"></a>Problemas de identidad versus problemas de sincronización

Antes de comenzar, es importante comprender la diferencia entre los problemas de identidad y los problemas de sincronización. Un caso de uso popular para mantener la identidad del usuario en el explorador es admitir la sincronización. Por este motivo, los problemas de identidad se confunden con frecuencia con los problemas de sincronización. Aprende la diferencia entre un problema de identidad y uno de sincronización antes de empezar a solucionar problemas de sincronización.

Antes de tratar un problema como un problema de sincronización, comprueba si el usuario ha iniciado sesión en el explorador con una cuenta válida.

La siguiente captura de pantalla muestra un ejemplo de un error de identidad. El error es "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea",** que se encuentra en *edge://sync-internals* en **Credenciales:**

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="common-sync-issues"></a>Problemas comunes de sincronización

### <a name="issue-cant-access-m365-or-azure-information-protection-subscription"></a>Problema: no se puede acceder a la suscripción de M365 o Azure Information Protection

¿Tiene una suscripción anterior de M365 o Azure Information Protection (AIP) que expiró y se reemplazó por una nueva suscripción? En ese caso, la identificación del inquilino ha cambiado y es necesario restablecer los datos de servicio. Consulte las instrucciones para restablecer los datos en el problema del **error de Cryptographer encontrado**.

### <a name="issue-sync-is-not-available-for-this-account"></a>Problema: "La sincronización no está disponible para esta cuenta".

Si se produce este error en una cuenta de Azure Active Directory, o si aparece DISABLED_BY_ADMIN en *edge://sync-internals*, sigue los pasos del siguiente procedimiento de manera secuencial hasta que se solucione el problema.

> [!NOTE]
> Como el origen de este error suele ser un cambio de configuración en una cuenta empresarial de Azure Active Directory, estos pasos de solución de problemas solo los puede realizar un administrador de inquilinos y no los usuarios finales.

1. Comprueba que el inquilino empresarial tenga una suscripción compatible con M365. Aquí se proporciona la lista actual de los tipos de suscripción [aquí](/azure/information-protection/activate-office365). Si el inquilino no tiene una suscripción compatible, puede comprar Azure Information Protection por separado o actualizar a una de las suscripciones compatibles.
2. Si hay disponible una suscripción compatible, compruebe que el inquilino tenga disponible Azure Information Protection (AIP). Las instrucciones para comprobar el estado de AIP y, si es necesario, activar AIP [aquí](/azure/information-protection/activate-office365).
3. Si el paso 2 muestra que AIP está activo pero la sincronización sigue sin funcionar, activa la itinerancia de estado empresarial (ESR). [Aquí](/azure/active-directory/devices/enterprise-state-roaming-enable) se indican las instrucciones para habilitar ESR. Ten en cuenta que ESR no necesita mantenerse activa. Puede desactivar ESR si este paso soluciona el problema.
4. Confirme que Azure Information Protection no tiene un ámbito a través de una directiva de incorporación. Puede usar el applet [Get-AadrmOnboardingControlPolicy](/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) de PowerShell para ver si el ámbito está habilitado. Los dos ejemplos siguientes muestran una configuración sin ámbito y una configuración con ámbito para un grupo de seguridad específico.

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

   Si el ámbito está habilitado, el usuario afectado debe agregarse al grupo de seguridad del ámbito o debería quitarse. En el ejemplo siguiente, la integración tiene ámbito AIP para el grupo de seguridad indicado y el ámbito debe quitarse con el sub applet set-AadrmOnboardingControlPolicy[](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell de [.](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps)

5. Confirma que IP DomainService esté activado en el espacio empresarial. El applet de PowerShell [Get-AadrmConfiguración](/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) muestra el estado del servicio.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Comprueba si IPCv3Service está habilitado.":::

6. Si el problema no se solucionó, contacta el [soporte técnico de Microsoft Edge](https://www.microsoftedgeinsider.com/support).

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a>Problema: Se atasca en "Configurando la sincronización..." o "No se pudo conectar al servidor de sincronización. Reintentar..."

1. Cierra y vuelve a iniciar sesión.
2. Ve a *edge://sync-internals*. Si en la sección "**Type info**" está presente el siguiente error, entonces ve al siguiente problema, **error de criptografía encontrado**.

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. Intenta hacer ping al punto de conexión del servidor. El punto de conexión del servidor para un cliente está disponible en *edge://sync-internals*. En la siguiente captura de pantalla se muestra la información del punto de conexión bajo **Información del entorno**.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Información de puntos de conexión":::

4. Si el punto de conexión del servidor está vacío, o no se puede hacer ping al servidor y hay un firewall presente en el entorno, asegúrate de que los puntos de conexión de servicio necesarios estén disponibles en el computador del cliente.

   - Puntos de conexión del servicio de sincronización de Microsoft Edge:
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - Puntos de conexión de Azure Information Protection:
      - [https://api.aadrm.com](https://api.aadrm.com)(para la mayoría de los espacios empresariales)
      - [https://api.aadrm.de](https://api.aadrm.de)(para los espacios empresariales de Alemania)
      - [https://api.aadrm.cn](https://api.aadrm.cn)(para los espacios empresariales de China)
   - [Puntos de conexión del Servicio de notificaciones de Windows](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. Si el problema aún no está arreglado, contacta el [soporte técnico de Microsoft Edge](https://www.microsoftedgeinsider.com/support).

### <a name="issue-cryptographer-error-encountered"></a>Problema: Se encontró un error de criptografía

Este error está visible en la parte inferior de **Escribir información** en *edge://sync-internals* y puede significar que es necesario restablecer los datos del lado del servicio del usuario. En el siguiente ejemplo se muestra un mensaje de error de criptografía:
<br>"Error:GenerateCryptoErrorsForTypes@.. /.. /components/sync/driver/data_type_manager_impl.cc:42, se encontró un error de criptografía".

1. Reinicia Microsoft Edge y navega hasta el *edge://sync-internals* y comprueba la sección "**Estado de la clave de cuenta de AAD**"
   - "Correcto" en "Último resultado de MIP": el error de criptografía significa que los datos del servidor pueden haber sido cifrados con una clave perdida. Es necesario restablecer los datos para reanudar la sincronización.
   - "Ningún permiso" en "Último resultado de MIP": es posible que se deba a un cambio de Azure AD o a cambios en la suscripción de inquilino. Es necesario restablecer los datos para reanudar la sincronización.
   - Otros errores pueden significar problemas de configuración del servidor.
2. Si es necesario restablecer los datos, consulta [Restablecer datos de Microsoft Edge en la nube](edge-learnmore-reset-data-in-cloud.md).

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a>Problema: "Tu administrador ha desactivado la sincronización."

Asegúrese de que las [Directiva SyncDisabled](./microsoft-edge-policies.md#syncdisabled)  no esté establecida.

## <a name="see-also"></a>Vea también

- [Sincronización de Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)