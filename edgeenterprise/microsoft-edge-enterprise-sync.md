---
title: Configurar la sincronización de Microsoft Edge Enterprise
ms.author: collw
author: AndreaLBarr
manager: silvanam
ms.date: 09/07/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Opciones de administrador y usuario para configurar Microsoft Edge para sincronizar favoritos, contraseñas y otros datos del explorador.
ms.openlocfilehash: 5caec237eebcd18a83b8f32d638ace2fa2914e38
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11980272"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a>Configurar la sincronización de Microsoft Edge Enterprise

En este artículo se explica cómo los administradores pueden configurar Microsoft Edge para sincronizar los favoritos del usuario, las contraseñas y otros datos del navegador en todos los dispositivos en los que se ha iniciado la sesión. Si no eres un administrador, visita este artículo para saber cómo iniciar la sesión y sincronizar Microsoft Edge en todos los dispositivos. 
            [Inicie sesión para sincronizar Microsoft Edge en todos los dispositivos](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674).

> [!NOTE]
> Se aplica a la versión 77 o posterior de Microsoft Edge, a menos que se indique lo contrario.

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
- Microsoft 365 Empresa Premium, Estándar o Básico
- Office 365 E1 y posteriores
- Azure Information Protection (AIP) (P1 o P2)
- Todas las suscripciones de EDU (Microsoft Apps para estudiantes o profesores, Exchange Online para estudiantes o profesores, O365 A1 o superior, M365 A1 o superior, o Azure Information Protection P1 o P2 para estudiantes o profesores)

## <a name="sync-group-policies"></a>Directivas de grupo de sincronización

Los administradores pueden usar las siguientes directivas de grupo para configurar y administrar la sincronización de Microsoft Edge:

- 
            [SyncDisabled](./microsoft-edge-policies.md#syncdisabled): deshabilita la sincronización por completo.
- 
            [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): deshabilita el almacenamiento del historial de exploración y la sincronización. Esta directiva también deshabilita la sincronización de pestañas abiertas.
- 
            [AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): cuando esta directiva está deshabilitada, la sincronización del historial también se deshabilitará.
- 
            [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): configurar la lista de tipos que se excluyen de la sincronización.
- 
            [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): permitir que los perfiles de Active Directory (AD) usen almacenamiento local. Para más información, consulte [Sincronización local para usuarios de Active Directory (AD)](./microsoft-edge-on-premises-sync.md).
- 
            [ForceSync](/deployedge/microsoft-edge-policies#forcesync): activa la sincronización de forma predeterminada y no requiere el consentimiento del usuario para sincronizar.  

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