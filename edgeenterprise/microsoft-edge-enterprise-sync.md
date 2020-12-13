---
title: Sincronización de Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 12/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronización de Microsoft Edge Enterprise
ms.openlocfilehash: 791188b5d28c867d6409a4d5373ea6c1ec7e49c7
ms.sourcegitcommit: 482b2e440a62cbf974dc45ac817f9d9d187ba1b9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "11205469"
---
# Sincronización de Microsoft Edge Enterprise

Este artículo explica cómo usar Microsoft Edge para sincronizar los favoritos, las contraseñas y otros datos del explorador en todos los dispositivos que hayan iniciado sesión.

> [!NOTE]
> Este artículo se aplica a la versión 77 de Microsoft Edge o posteriores, a menos que se indique lo contrario.

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

## Configuración de la sincronización de Microsoft Edge

Las opciones de configuración para la sincronización de Microsoft Edge están disponibles a través del servicio de Azure Information Protection (AIP). Cuando AIP está habilitado para un espacio empresarial, todos los usuarios pueden sincronizar los datos de Microsoft Edge, independientemente de la licencia. Las instrucciones para habilitar AIP pueden encontrarse [aquí](https://docs.microsoft.com/azure/information-protection/activate-office365).

Para restringir la sincronización a un conjunto específico de usuarios, puedes habilitar la [directiva de control de incorporación AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) para estos usuarios. Si la sincronización aún no está disponible después de asegurarte de que todos los usuarios necesarios estén incorporados, asegúrate de que IPCv3Service está habilitado con el cmdlet de PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true).

> [!CAUTION]
> La activación de Azure Information Protection también permitirá el acceso a otras aplicaciones, como Microsoft Word o Microsoft Outlook, para proteger el contenido con AIP. Además, las directivas de control de incorporación que se usan para restringir la sincronización de Microsoft Edge también evitarán que otras aplicaciones protejan el contenido con AIP.

## Microsoft Edge y Enterprise State Roaming

El nuevo Microsoft Edge es una aplicación multiplataforma con un ámbito expandido para sincronización de los datos de usuarios en todos sus dispositivos y ya no forma parte de Azure AD Enterprise State Roaming. Sin embargo, el nuevo Microsoft Edge cumplirá las promesas de protección de datos de ESR, como la capacidad de llevar la propia clave. Para obtener más información, consulta [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Directivas de grupo de sincronización

Las siguientes directivas de grupo afectan a la sincronización de Microsoft Edge:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): deshabilita la sincronización por completo.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): deshabilita el almacenamiento del historial de exploración y la sincronización. Esta directiva también deshabilita la sincronización de pestañas abiertas.
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): cuando esta directiva está deshabilitada, la sincronización del historial también se deshabilitará.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configurar la lista de tipos que se excluyen de la sincronización.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permitir que los perfiles de Active Directory (AD) usen almacenamiento local. Para más información, consulte [Sincronización local para usuarios de Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): activar la sincronización de forma predeterminada y no requerir el consentimiento del usuario para sincronizar.  

## Preguntas más frecuentes

### CUMPLIMIENTO DE SEGURIDAD y SERVIDOR/DATOS

#### ¿Se cifran los datos sincronizados?

Los datos se cifran en el transporte con TLS 1.2 o superior. Todos los tipos de datos también se cifran en reposo en el servicio de Microsoft con AES128. Todos los tipos de datos, excepto los que se usan para la sincronización de pestañas abiertas e historial, también se cifran antes de salir del dispositivo del usuario con claves administradas a través de [Azure Information Protection](https://docs.microsoft.com/azure/information-protection/).

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

La sincronización empresarial depende de Azure Information Protection, que no está disponible en todas las suscripciones de M365.

#### ¿La sincronización de Microsoft Edge está basada en Enterprise State Roaming (ESR)?

No. ESR se puede usar para habilitar la sincronización, pero la sincronización de Microsoft Edge no forma parte de ESR. Para más información, consulte [Sincronización de Microsoft Edge](microsoft-edge-enterprise-sync.md) y [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

#### ¿Microsoft Edge admitirá en algún momento la sincronización entre Microsoft Edge e IE?

No hay planes para admitir esta sincronización. Si aún necesita Internet Explorer (IE) en su entorno para usar aplicaciones heredadas, considere la posibilidad de usar el [nuevo modo de IE](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### ¿Microsoft Edge se sincronizará con Microsoft Edge (versión anterior)?

No lo hará. Creemos que la conexión de estos dos ecosistemas provocará un compromiso respecto de la confiabilidad de la sincronización en Microsoft Edge. Nos aseguraremos de que los datos existentes se migren a Microsoft Edge. Además, los usuarios podrán importar datos desde el explorador de su elección. Esto también significa que el nuevo explorador Microsoft Edge no tendrá una forma de sincronizarse con IE.

### ADMINISTRAR LA SINCRONIZACIÓN

#### ¿Es posible impedir que los usuarios sincronicen con un espacio empresarial personal?

No directamente, pero puede determinar qué perfiles pueden iniciar sesión en Microsoft Edge mediante la directiva [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
