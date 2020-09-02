---
title: Sincronización de Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronización de Microsoft Edge Enterprise
ms.openlocfilehash: a6d01356db478871a7c6b386bbb731b32dc4739a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981197"
---
# Sincronización de Microsoft Edge Enterprise

Este artículo explica cómo usar Microsoft Edge para sincronizar los favoritos, las contraseñas y otros datos del explorador en todos los dispositivos que hayan iniciado sesión.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## Introducción

La sincronización de Microsoft Edge permite a los usuarios acceder a sus datos de exploración en todos sus dispositivos que hayan iniciado sesión. Los datos admitidos por la sincronización incluyen:

- Favoritos
- Contraseñas
- Direcciones y más (relleno de formularios)
- Colecciones
- Configuración

La funcionalidad de sincronización está habilitada a través del consentimiento del usuario y los usuarios pueden activar o desactivar la sincronización para cada uno de los tipos de datos enumerados anteriormente.

> [!NOTE]
> Los datos de configuración y conectividad de dispositivo adicionales (como el nombre del dispositivo, la marca y el modelo) se cargan para admitir la funcionalidad de sincronización.

## Requisitos previos

Actualmente, la sincronización de Microsoft Edge para las cuentas de Azure Active Directory (Azure AD) está disponible para las siguientes suscripciones:

- Azure AD Premium (P1 y P2)
- M365 Empresa Premium
- Office 365 E3 y superiores
- Azure Information Protection (AIP) (P1 y P2)
- Todas las suscripciones de EDU (O365 A1 o superior, M365 A1 o superior, o bien Azure Information Protection P1 o P2 para estudiantes o profesores)

> [!NOTE]
> La sincronización tiene una dependencia en el servicio de protección que ofrece Azure Information Protection (AIP) para proteger los datos de sincronización. Este servicio está disponible actualmente para las suscripciones anteriores. Para ver la lista completa de SKU con AIP, consulta [Precios de protección de la información](https://azure.microsoft.com/pricing/details/information-protection/).

## Opciones de configuración de sincronización de Microsoft Edge

Están disponibles las siguientes opciones de configuración para habilitar la sincronización de Microsoft Edge:

- Azure Information Protection (AIP)
- Azure AD Enterprise State Roaming (ESR)

Si se deshabilitan tanto AIP como ESR, los usuarios verán un mensaje de error que indicará que la sincronización no está disponible para su cuenta.

### Azure Information Protection (AIP)

Si el servicio de Azure Information Protection (AIP) está habilitado para un inquilino, todos los usuarios pueden sincronizar datos de Microsoft Edge, independientemente de las licencias. Las instrucciones para habilitar AIP pueden encontrarse [aquí](https://docs.microsoft.com/azure/information-protection/activate-office365).

Para restringir la sincronización a un conjunto específico de usuarios, puede habilitar la [directiva de control de incorporación AADRM](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) para estos usuarios. Si la sincronización aún no está disponible después de asegurarse de que todos los usuarios necesarios estén incorporados, asegúrese de que la IPCv3Service está habilitada con el cmdlet de PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps).

> [!CAUTION]
> La activación de Azure Information Protection también restringirá el acceso para otras aplicaciones con AIP, como Microsoft Word o Microsoft Outlook.

### Azure AD Enterprise State Roaming (ESR)

Si la función Azure Active Directory [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) está habilitada para cualquier usuario o inquilino, estos podrán usar la función de sincronización de Microsoft Edge, independientemente de la configuración de directiva de control de incorporación.

## Microsoft Edge y Enterprise State Roaming

El nuevo Microsoft Edge es una aplicación multiplataforma con un ámbito expandido para sincronización de los datos de usuarios en todos sus dispositivos y ya no forma parte de Azure AD Enterprise State Roaming. Sin embargo, el nuevo Microsoft Edge cumplirá las promesas de protección de datos de ESR, como la capacidad de llevar la propia clave. Para obtener más información, consulta [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Directivas de grupo de sincronización

Las siguientes directivas de grupo afectan a la sincronización de Microsoft Edge:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): deshabilita la sincronización por completo.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): deshabilita el almacenamiento y la sincronización del historial de exploración. Esto también deshabilita la sincronización de pestañas abiertas.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configurar la lista de tipos que se excluyen de la sincronización.

## Preguntas más frecuentes

### CUMPLIMIENTO DE SEGURIDAD y SERVIDOR/DATOS

#### ¿Se cifran los datos sincronizados? 

Los datos están cifrados en el transporte con TLS 1.2 o posterior y además, permanece en reposo en el servicio de Microsoft con AES256.

#### ¿Dónde se almacenan los datos de sincronización de Microsoft Edge?

Los datos sincronizados para las cuentas de Azure AD se almacenan en servidores seguros, en función del identificador de espacio empresarial. Por ejemplo, los datos de un espacio empresarial que está registrado en Estados Unidos se almacenan en los servidores localizados en una ubicación geográfica para esa región y usan la misma solución de almacenamiento que las aplicaciones de Office.

#### ¿Los datos salen de la nube en algún momento de Microsoft, aparte de sincronizarse con Microsoft Edge?

No.

#### ¿Los administradores de espacios empresariales pueden llevar su propia clave?

Sí, mediante [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

#### ¿Qué términos de servicio se aplican a la sincronización empresarial?

Los términos de servicio son los mismas que para la suscripción de Azure AD. Todos los términos de servicio de Azure AD, en última instancia, corresponden a los [Términos del servicio en línea](https://www.microsoft.com/licensing/product-licensing/products) de Microsoft.

#### ¿Es compatible Microsoft Edge con el cumplimiento normativo de Government Community Cloud (GCC) High?

Actualmente, no. GCC High es de nivel D, mientras que Microsoft Edge admite hasta el nivel C.

### APLICAR LA SINCRONIZACIÓN

#### ¿Qué sucede con los clientes de empresa y del sector educativo que deciden mantener Microsoft Edge heredado?

La versión actual del explorador Microsoft Edge seguirá participando en la oferta de ESR.

#### ¿Por qué necesito una suscripción de Azure AD Premium para sincronizar?

La sincronización de empresa depende de Azure Information Protection, que no está disponible en todos los niveles de Azure AD.

#### ¿La sincronización de Microsoft Edge está basada en Enterprise State Roaming?

No. ESR se puede usar para habilitar la sincronización, pero la sincronización de Microsoft Edge no forma parte de ESR. Para más información, consulte [Sincronización de Microsoft Edge](microsoft-edge-enterprise-sync.md) y [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

#### ¿Microsoft Edge admitirá en algún momento la sincronización entre Microsoft Edge e IE?

No hay planes para admitir esta sincronización. Si aún necesita Internet Explorer en su entorno para usar aplicaciones heredadas, considere la posibilidad de usar el [nuevo modo de IE](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### ¿El nuevo explorador de Microsoft Edge se sincronizará con Microsoft Edge Legacy?

No, no lo hará. Creemos que la conexión de estos dos ecosistemas dará lugar a compromisos en la confiabilidad de la sincronización del nuevo Microsoft Edge. Se garantizará que los datos existentes se migren al nuevo Microsoft Edge. Además, los usuarios podrán importar datos desde el explorador de su elección. Esto también significa que el nuevo explorador Microsoft Edge no tendrá una forma de sincronizarse con IE.

### ADMINISTRAR LA SINCRONIZACIÓN

#### ¿Es posible impedir que los usuarios sincronicen con un espacio empresarial personal?

No directamente, pero puede determinar qué perfiles pueden iniciar sesión en Microsoft Edge mediante la directiva [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
