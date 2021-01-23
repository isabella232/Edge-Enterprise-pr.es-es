---
title: Configurar y solucionar problemas de sincronización de Microsoft Edge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 01/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar y solucionar problemas de sincronización de Microsoft Edge
ms.openlocfilehash: 36912d2fd1c33a227ce1d4b7c912f6ef1dfdcc00
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297465"
---
# Configurar y solucionar problemas de sincronización de Microsoft Edge

En este artículo se explica cómo configurar y usar Microsoft Edge para sincronizar los favoritos, contraseñas y otros datos del explorador en todos los dispositivos que han iniciado sesión a la cuenta. En este artículo también se proporcionan pasos de solución de problemas para los problemas de sincronización más comunes. También incluye las herramientas recomendadas para recopilar los registros necesarios para solucionar problemas.

> [!NOTE]
> Aplica a La versión 77 de Microsoft Edge o posterior, a menos que se indique lo contrario.

## Introducción

La sincronización de Microsoft Edge permite a los usuarios acceder a sus datos de exploración en todos sus dispositivos que hayan iniciado sesión. Los datos admitidos por la sincronización incluyen:

- Favoritos
- Contraseñas
- Direcciones y más (relleno de formularios)
- Colecciones
- Configuración
- Extensión
- Pestañas abiertas (disponibles en la versión 88 de Microsoft Edge)
- Historial (disponible en la versión 88 de Microsoft Edge)

La funcionalidad de sincronización está habilitada mediante el consentimiento del usuario, y los usuarios pueden activar o desactivar la sincronización para cada uno de los tipos de datos que se muestran anteriormente.

> [!NOTE]
> Los datos de configuración y conectividad de dispositivo adicionales (como el nombre del dispositivo, la marca y el modelo) se cargan para admitir la funcionalidad de sincronización.

## Requisitos previos

La sincronización de Microsoft Edge para las cuentas de Azure Active Directory (Azure AD) está disponible para cualquiera de las siguientes suscripciones:

- Azure AD Premium (P1 o P2)
- M365 Empresa Premium
- Office 365 E1 y posteriores
- Azure Information Protection (AIP) (P1 o P2)
- Todas las suscripciones de EDU (Microsoft Apps para estudiantes o profesores, Exchange Online para estudiantes o profesores, O365 A1 o superior, M365 A1 o superior, o Azure Information Protection P1 o P2 para estudiantes o profesores)

## Directivas de grupo de sincronización

Puedes usar las siguientes directivas de grupo para configurar y administrar la sincronización de Microsoft Edge:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): deshabilita la sincronización por completo.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): deshabilita el almacenamiento del historial de exploración y la sincronización. Esta directiva también deshabilita la sincronización de pestañas abiertas.
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): cuando esta directiva está deshabilitada, la sincronización del historial también se deshabilitará.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configurar la lista de tipos que se excluyen de la sincronización.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permitir que los perfiles de Active Directory (AD) usen almacenamiento local. Para más información, consulte [Sincronización local para usuarios de Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): activa la sincronización de forma predeterminada y no requiere el consentimiento del usuario para sincronizar.  

## Configurar la sincronización de Microsoft Edge

Las opciones de configuración para la sincronización de Microsoft Edge están disponibles a través del servicio de Azure Information Protection (AIP). Cuando AIP está habilitado para un espacio empresarial, todos los usuarios pueden sincronizar los datos de Microsoft Edge, independientemente de la licencia. Las instrucciones para habilitar AIP pueden encontrarse [aquí](https://docs.microsoft.com/azure/information-protection/activate-office365).

Para restringir la sincronización a un conjunto específico de usuarios, puedes habilitar la [directiva de control de incorporación AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) para estos usuarios. Si la sincronización aún no está disponible después de asegurarte de que todos los usuarios necesarios estén incorporados, asegúrate de que IPCv3Service está habilitado con el cmdlet de PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true).

> [!CAUTION]
> La activación de Azure Information Protection también permitirá el acceso a otras aplicaciones, como Microsoft Word o Microsoft Outlook, para proteger el contenido con AIP. Además, las directivas de control de incorporación que se usan para restringir la sincronización de Microsoft Edge también evitarán que otras aplicaciones protejan el contenido con AIP.

## Microsoft Edge y Enterprise State Roaming (ESR)

Microsoft Edge es una aplicación multiplataforma con un ámbito expandido para sincronizar datos de usuario en todos sus dispositivos y ya no forma parte de Azure AD Enterprise State Roaming. Sin embargo, Microsoft Edge cumplirá las promesas de protección de datos de ESR, como la capacidad de crear su propia clave. Para obtener más información, consulta [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Solucionar problemas de sincronización

En esta sección se proporcionan los pasos para la solución de problemas de sincronización más encontrados. También incluye las herramientas recomendadas para recopilar los registros necesarios para solucionar problemas.

### Problemas de identidad versus problemas de sincronización

Un caso de uso popular para mantener la identidad del usuario en el explorador es admitir la sincronización. Por este motivo, los problemas de identidad se confunden con frecuencia con los problemas de sincronización. Aprende la diferencia entre un problema de identidad y uno de sincronización antes de empezar a solucionar problemas de sincronización.

Antes de tratar un problema como un problema de sincronización, comprueba si el usuario ha iniciado sesión en el explorador con una cuenta válida.

La siguiente captura de pantalla muestra un ejemplo de un error de identidad. El error es "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea",** que se encuentra en *edge://sync-internals* en **Credenciales:**

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

### Problemas comunes de sincronización

#### Problema: no se puede acceder a la suscripción de M365 o Azure Information Protection

¿Tiene una suscripción anterior de M365 o Azure Information Protection (AIP) que expiró y se reemplazó por una nueva suscripción? En ese caso, la identificación del inquilino ha cambiado y es necesario restablecer los datos de servicio. Consulte las instrucciones para restablecer los datos en el problema del **error de Cryptographer encontrado**.

#### Problema: "La sincronización no está disponible para esta cuenta".

Si se produce este error en una cuenta de Azure Active Directory, o si aparece DISABLED_BY_ADMIN en *edge://sync-internals*, sigue los pasos del siguiente procedimiento de manera secuencial hasta que se solucione el problema.

> [!NOTE]
> Como el origen de este error suele ser un cambio de configuración en una cuenta empresarial de Azure Active Directory, estos pasos de solución de problemas solo los puede realizar un administrador de inquilinos y no los usuarios finales.

1. Comprueba que el inquilino empresarial tenga una suscripción compatible con M365. Aquí se proporciona la lista actual de los tipos de suscripción [aquí](https://docs.microsoft.com/azure/information-protection/activate-office365). Si el inquilino no tiene una suscripción compatible, puede comprar Azure Information Protection por separado o actualizar a una de las suscripciones compatibles.
2. Si hay disponible una suscripción compatible, compruebe que el inquilino tenga disponible Azure Information Protection (AIP). Las instrucciones para comprobar el estado de AIP y, si es necesario, activar AIP [aquí](https://docs.microsoft.com/azure/information-protection/activate-office365).
3. Si el paso 2 muestra que AIP está activo pero la sincronización sigue sin funcionar, activa la itinerancia de estado empresarial (ESR). [Aquí](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable) se indican las instrucciones para habilitar ESR. Ten en cuenta que ESR no necesita mantenerse activa. Puede desactivar ESR si este paso soluciona el problema.
4. Confirma que Azure Information Protection no esté limitado por una directiva de integración. Puedes usar el [applet Get-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps)  PowerShell para ver si está habilitado el ámbito. Los dos ejemplos siguientes muestran una configuración sin ámbito y un ámbito de configuración para un grupo de seguridad específico.

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


   Si el ámbito está habilitado, el usuario afectado debe agregarse al grupo de seguridad del ámbito o debería quitarse. En el ejemplo siguiente, la integración tiene ámbito AIP para el grupo de seguridad indicado y el ámbito debe quitarse con el sub applet set-AadrmOnboardingControlPolicy[](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell de [.](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps)

5. Confirma que IP DomainService esté activado en el espacio empresarial. El applet de PowerShell [Get-AadrmConfiguración](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) muestra el estado del servicio.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Comprueba si IPCv3Service está habilitado.":::

6. Si el problema no se solucionó, contacta el [soporte técnico de Microsoft Edge](https://www.microsoftedgeinsider.com/support).

#### Problema: Se atasca en "Configurando la sincronización..." o "No se pudo conectar al servidor de sincronización. Reintentar..."

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
   - [Puntos de conexión del Servicio de notificaciones de Windows](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. Si el problema aún no está arreglado, contacta el [soporte técnico de Microsoft Edge](https://www.microsoftedgeinsider.com/support).

### Problema: Se encontró un error de criptografía

Este error está visible en la parte inferior de **Escribir información** en *edge://sync-internals* y puede significar que es necesario restablecer los datos del lado del servicio del usuario. En el siguiente ejemplo se muestra un mensaje de error de criptografía:
<br>"Error:GenerateCryptoErrorsForTypes@.. /.. /components/sync/driver/data_type_manager_impl.cc:42, se encontró un error de criptografía".

1. Reinicia Microsoft Edge y navega hasta el *edge://sync-internals* y comprueba la sección "**Estado de la clave de cuenta de AAD**"
   - "Correcto" en "Último resultado de MIP": el error de criptografía significa que los datos del servidor pueden haber sido cifrados con una clave perdida. Es necesario restablecer los datos para reanudar la sincronización.
   - "Ningún permiso" en "Último resultado de MIP": es posible que se deba a un cambio de Azure AD o a cambios en la suscripción de inquilino. Es necesario restablecer los datos para reanudar la sincronización.
   - Otros errores pueden significar problemas de configuración del servidor.
2. Si es necesario restablecer los datos, consulta [Restablecer datos de Microsoft Edge en la nube](edge-learnmore-reset-data-in-cloud.md).

#### Problema: "Tu administrador ha desactivado la sincronización."

Asegúrate de que las [Directivas SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled) no estén establecidas.

## Preguntas más frecuentes

### CUMPLIMIENTO DE SEGURIDAD y SERVIDOR/DATOS

#### ¿Se cifran los datos sincronizados?

Los datos se cifran en el transporte con TLS 1.2 o superior. Todos los tipos de datos también se cifran en reposo en el servicio de Microsoft con AES128. Todos los tipos de datos, excepto los que se usan para la sincronización de pestañas abiertas e historial, también se cifran antes de salir del dispositivo del usuario con claves administradas a través de [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

#### ¿Por qué las pestañas abiertas y los datos del historial no tienen un cifrado adicional del lado del cliente?

Para reducir la utilización de recursos en los dispositivos de los usuarios finales, los datos del historial se generan del lado del servidor en función de los datos de itinerancia de las pestaña abiertas. Este proceso no sería posible con el cifrado de datos del lado del cliente. Para deshabilitar la sincronización de pestañas abiertas e historial, aplique las directivas [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) o [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled).

#### ¿Los administradores de espacios empresariales pueden poner su propia clave?

Sí, a través de [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

#### ¿Dónde se almacenan los datos de sincronización de Microsoft Edge?

Los datos sincronizados para las cuentas de Azure AD se almacenan en servidores seguros, en función del identificador de espacio empresarial. Por ejemplo, los datos de un espacio empresarial que está registrado en Estados Unidos se almacenan en los servidores localizados en una ubicación geográfica para esa región y usan la misma solución de almacenamiento que las aplicaciones de Office.

#### ¿Los datos salen de la nube en algún momento de Microsoft, aparte de sincronizarse con Microsoft Edge?

No.

#### ¿Qué términos de servicio se aplican a la sincronización empresarial?

Las condiciones de servicio para la sincronización de Microsoft Edge se incluyen en la licencia del software de Microsoft visible en Microsoft Edge en *edge://terms*. En última instancia, la suscripción y los términos de servicio de Azure AD se incluyen en los [Términos del servicio en línea](https://www.microsoft.com/licensing/product-licensing/products)de Microsoft.

#### ¿Microsoft Edge es compatible con el cumplimiento normativo de Government Community Cloud (GCC) High?

Actualmente, no. Para los clientes de la nube de GCC High, la sincronización de Microsoft Edge está deshabilitada.

### APLICAR LA SINCRONIZACIÓN

#### ¿Por qué la sincronización de Microsoft Edge no es compatible con todas las suscripciones de M365?

La sincronización empresarial depende de [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), que no está disponible en todas las suscripciones de M365.

#### ¿La sincronización de Microsoft Edge está basada en Enterprise State Roaming (ESR)?

No. ESR se puede usar para habilitar la sincronización, pero la sincronización de Microsoft Edge no forma parte de ESR. Para más información, consulte [Sincronización de Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) y [Microsoft Edge y Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).

#### ¿Microsoft Edge admitirá en algún momento la sincronización entre Microsoft Edge e IE?

No hay planes para admitir esta sincronización. Si aún necesita Internet Explorer (IE) en su entorno para usar aplicaciones heredadas, considere la posibilidad de usar el [nuevo modo de IE](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### ¿Microsoft Edge se sincronizará con Microsoft Edge (versión anterior)?

No lo hará. Creemos que la conexión de estos dos ecosistemas provocará un compromiso respecto de la confiabilidad de la sincronización en Microsoft Edge. Nos aseguraremos de que los datos existentes se migren a Microsoft Edge. Los usuarios también podrán importar datos desde el explorador de su elección, lo que también significa que Microsoft Edge no tendrá una forma de sincronizar con IE.

### ADMINISTRAR LA SINCRONIZACIÓN

#### ¿Es posible impedir que los usuarios sincronicen con un espacio empresarial personal?

No directamente, pero puede determinar qué perfiles pueden iniciar sesión en Microsoft Edge mediante la directiva [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## Consulta también

- [Sincronización de Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
