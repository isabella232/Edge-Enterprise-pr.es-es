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
# <a name="configure-microsoft-edge-enterprise-sync"></a>Configurar la sincronización de Microsoft Edge Enterprise

En este artículo se explica cómo los administradores pueden configurar Microsoft Edge para sincronizar los favoritos del usuario, las contraseñas y otros datos del explorador en todos los dispositivos que han iniciado sesión.

> [!NOTE]
> Se aplica a la versión 77 de Microsoft Edge o posteriores, a menos que se indique lo contrario.

## <a name="overview"></a>Introducción

La sincronización de Microsoft Edge permite a los usuarios acceder a sus datos de exploración en todos sus dispositivos que hayan iniciado sesión. Los datos admitidos por la sincronización incluyen:

- Favoritos
- Contraseñas
- Direcciones y más (relleno de formularios)
- Colecciones
- Configuración
- Extensión
- Pestañas abiertas (disponibles en la versión 88 de Microsoft Edge)
- Historial (disponible en la versión 88 de Microsoft Edge)

La funcionalidad de sincronización está habilitada mediante el consentimiento del usuario, y los usuarios pueden activar o desactivar la sincronización para cada uno de los tipos de datos enumerados anteriormente. Si un usuario está experimentando un problema de sincronización, es posible que deba restablecer la sincronización en **Configuración** > **Perfiles** > **Restablecer sincronización**.

> [!NOTE]
> Los datos de configuración y conectividad de dispositivos adicionales (como el nombre del dispositivo, la marca y el modelo) se cargan para admitir la funcionalidad de sincronización.

## <a name="prerequisites"></a>Requisitos previos

La sincronización de Microsoft Edge para las cuentas de Azure Active Directory (Azure AD) está disponible para cualquiera de las siguientes suscripciones:

- Azure AD Premium (P1 o P2)
- M365 Empresa Premium
- Office 365 E1 y posteriores
- Azure Information Protection (AIP) (P1 o P2)
- Todas las suscripciones de EDU (Microsoft Apps para estudiantes o profesores, Exchange Online para estudiantes o profesores, O365 A1 o superior, M365 A1 o superior, o Azure Information Protection P1 o P2 para estudiantes o profesores)

## <a name="sync-group-policies"></a>Directivas de grupo de sincronización

Los administradores pueden usar las siguientes directivas de grupo para configurar y administrar la sincronización de Microsoft Edge:

- [SyncDisabled](./microsoft-edge-policies.md#syncdisabled): deshabilita la sincronización por completo.
- [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): deshabilita el almacenamiento del historial de exploración y la sincronización. Esta directiva también deshabilita la sincronización de pestañas abiertas.
- [AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): cuando esta directiva está deshabilitada, la sincronización del historial también se deshabilitará.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): configurar la lista de tipos que se excluyen de la sincronización.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): permitir que los perfiles de Active Directory (AD) usen almacenamiento local. Para más información, consulte [Sincronización local para usuarios de Active Directory (AD)](./microsoft-edge-on-premises-sync.md).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): activa la sincronización de forma predeterminada y no requiere el consentimiento del usuario para sincronizar.  

## <a name="configure-microsoft-edge-sync"></a>Configurar la sincronización de Microsoft Edge

Las opciones de configuración para la sincronización de Microsoft Edge están disponibles a través del servicio de Azure Information Protection (AIP). Cuando AIP está habilitado para un espacio empresarial, todos los usuarios pueden sincronizar los datos de Microsoft Edge, independientemente de la licencia. Las instrucciones para habilitar AIP pueden encontrarse [aquí](/azure/information-protection/activate-office365).

Para restringir la sincronización a un conjunto específico de usuarios, puedes habilitar la [directiva de control de incorporación AIP](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) para estos usuarios. Si la sincronización aún no está disponible después de asegurarte de que todos los usuarios necesarios estén incorporados, asegúrate de que IPCv3Service está habilitado con el cmdlet de PowerShell [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps).

> [!CAUTION]
> La activación de Azure Information Protection también permitirá el acceso a otras aplicaciones, como Microsoft Word o Microsoft Outlook, para proteger el contenido con AIP. Además, las directivas de control de incorporación que se usan para restringir la sincronización de Microsoft Edge también evitarán que otras aplicaciones protejan el contenido con AIP.

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a>Microsoft Edge y Enterprise State Roaming (ESR)

Microsoft Edge es una aplicación multiplataforma con un ámbito expandido para sincronizar datos de usuario en todos sus dispositivos y ya no forma parte de Azure AD Enterprise State Roaming. Sin embargo, Microsoft Edge cumplirá las promesas de protección de datos de ESR, como la capacidad de crear su propia clave. Para obtener más información, consulta [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## <a name="see-also"></a>Vea también

- [Sincronización de Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Diagnosticar y corregir problemas de sincronización de Microsoft Edge](microsoft-edge-troubleshoot-enterprise-sync.md)
- [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)