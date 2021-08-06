---
title: Microsoft Edge y Enterprise State Roaming
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge y Enterprise State Roaming
ms.openlocfilehash: 664478f6c79d5710c4c0441fc33862d20cda0d1cfbcfefc7c944739cc7f539dd
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727453"
---
# <a name="microsoft-edge-and-enterprise-state-roaming"></a>Microsoft Edge y Enterprise State Roaming

Este artículo explica cómo está cambiando la participación de Microsoft Edge en Enterprise State Roaming (ESR) para una mejor compatibilidad con la sincronización entre plataformas y dispositivos.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="introduction"></a>Introducción

Con Windows 10, los usuarios de [Azure Active Directory (Azure AD)](/azure/active-directory/fundamentals/active-directory-whatis) obtuvieron la capacidad de sincronizar de forma segura su configuración de usuario y los datos de configuración de aplicaciones en la nube. [Enterprise State Roaming (ESR)](/azure/active-directory/devices/enterprise-state-roaming-overview) ofrece a los usuarios una experiencia unificada en todos sus dispositivos Windows y reduce el tiempo necesario para configurar un nuevo dispositivo.

Como parte de la adopción de la plataforma Chromium por parte de Microsoft Edge, su solución de sincronización está ahora desconectada del marco de sincronización de Windows. Esto afecta a la relación de Microsoft Edge con la oferta de ESR.

> [!IMPORTANT]
> El nuevo Microsoft Edge no participa en la oferta de ESR.

## <a name="whats-changing-with-microsoft-edge"></a>¿Qué cambia con Microsoft Edge?

Con el nuevo Microsoft Edge, la solución de sincronización no está vinculada al ecosistema de sincronización de Windows. Esto nos permite ofrecer Microsoft Edge en todas las plataformas, como Windows 7, Windows 8,1, iOS, Android y macOS. Esto también nos permite ofrecer la sincronización para cuentas no principales en Windows. Además, podemos enviar Microsoft Edge con una cadencia de distribución más frecuente y flexible que Windows. (Para obtener más información, consulte [Actualizaciones de Windows para admitir la próxima versión de Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md). Todos estos factores resaltaron la necesidad de reevaluar la participación de Microsoft Edge en la oferta de ESR.

ESR está enmarcado como una oferta de producto de Windows con promesas sobre cómo se controlan los datos de los dispositivos Windows, pero la sincronización de Microsoft Edge se extenderá más allá de los dispositivos Windows. Además, a medida que los datos se mueven entre estos dispositivos, se dificulta la definición de la oferta de sincronización de Microsoft Edge en el contexto de ESR. Para simplificar la forma en que funciona y se administra la sincronización, y para dar cabida a los cambios resaltados, se tomó la decisión de extraer Microsoft Edge de la oferta de ESR.

## <a name="does-this-mean-enterprises-will-lose-the-abilities-they-had-as-part-of-esr"></a>¿Significa esto que las empresas perderán las posibilidades que tenían como parte de ESR?

No. Microsoft Edge seguirá admitiendo la mayoría de las posibilidades proporcionadas en la oferta de ESR.

### <a name="unified-experience-across-devices-and-new-device-configuration-time"></a>Experiencia unificada entre dispositivos y nuevo tiempo de configuración de dispositivos

Cuando un usuario ha iniciado sesión en su dispositivo Windows con una cuenta de Azure Active Directory (cuenta de Azure AD), Microsoft Edge heredará implícitamente esa identidad la primera vez que se inicie el nuevo explorador.

Una vez que un usuario haya dado su consentimiento explícito para activar la sincronización en el nuevo Microsoft Edge, el explorador sincronizará todos los datos del explorador, como favoritos, contraseñas e historial. Esto garantiza una experiencia unificada entre dispositivos y reduce el tiempo necesario para personalizar el explorador.

### <a name="separation-of-corporate-and-consumer-data"></a>Separación de datos corporativos y de consumidores

Las organizaciones controlan sus datos y no se mezclan datos corporativos de cuentas de consumidores en la nube ni datos de consumidores en cuentas empresariales en la nube.

### <a name="enhanced-security"></a>Seguridad mejorada

Los datos se cifran automáticamente antes de abandonar el dispositivo con Windows 10 del usuario, usando Azure Information Protection, y los datos permanecen cifrados cuando quedan almacenados en la nube. Todo el contenido permanece cifrado al quedar almacenado en la nube, excepto los espacios de nombres, como los nombres de configuración.

### <a name="monitoring"></a>Monitorización

Proporcionaremos control y visibilidad sobre quién sincroniza la configuración de la organización y en qué dispositivos, mediante la integración con el Portal Azure AD. Esta funcionalidad se habilitará en una futura versión.

### <a name="management"></a>Administración

Los administradores podrán controlar qué miembros de la organización pueden habilitar la sincronización. Consulta [Configurar la sincronización de Microsoft Edge](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync) y las [Directivas de grupo de sincronización](microsoft-edge-enterprise-sync.md#sync-group-policies). Además, los usuarios pueden activar o desactivar la sincronización para cada uno de sus dispositivos, así como alternar cada atributo de datos individualmente para la sincronización.

### <a name="key-management"></a>Administración de claves

La función de sincronización aprovecha Azure Information Protection (AIP) para proteger los datos sincronizados solamente para el usuario y para los administradores de empresa. AIP admite claves de Microsoft administradas (valor predeterminado) y traer la propia clave para la administración de claves de nube. La estrategia de administración de claves de nube que usa la organización es transparente para Microsoft Edge y no tiene ninguna incidencia en la función de sincronización.

> [!IMPORTANT]
> [Conservar la propia clave ( HYOK)](/azure/information-protection/configure-adrms-restrictions) y Active Directory Rights Management Service no se admiten.

## <a name="summary-of-sync-attributes"></a>Resumen de atributos de sincronización

Los siguientes atributos de datos se sincronizarán en la nueva versión de Microsoft Edge en el primer inicio:

- Favoritos
- Contraseñas
- Rellenado de formularios
- Historial
- Pestañas abiertas (sesiones)
- Configuración (preferencias)
- Extensiones

La lista anterior de atributos es diferente de los atributos que se podían sincronizar en la versión heredada de Microsoft Edge. (Para obtener información detallada sobre la configuración heredada de Microsoft Edge, consulta [Configuración de itinerancia de Windows 10](/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference)). Los usuarios pueden habilitar o deshabilitar selectivamente estos atributos con la configuración Microsoft Edge. Dada la diferencia de atributos entre las dos versiones (por ejemplo, el historial), es posible que se pida a los usuarios que vuelvan a conceder el consentimiento de sincronización.

> [!NOTE]
> A diferencia de Microsoft Edge heredado, el nuevo Microsoft Edge no usa el Administrador de credenciales de Windows para las contraseñas y, como resultado, no sincronizará las contraseñas con Internet Explorer ni con otras aplicaciones que usen el Administrador de credenciales de Windows.

## <a name="terms-of-service"></a>Términos de servicio

Los términos de servicio de la sincronización de Microsoft Edge quedan bajo la licencia de software de Microsoft, que puede verse en Microsoft Edge, en *edge://terms*.

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sincronización de Microsoft Edge](microsoft-edge-enterprise-sync.md)