---
title: Monitor de contraseñas habilitado automáticamente para usuarios
ms.author: supalsul
author:
manager: tulasim
ms.date: 07/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Monitor de contraseñas habilitado automáticamente para usuarios
ms.openlocfilehash: bd1fe390b972c66cd9b4c20ab3a9fabde76c7e03
ms.sourcegitcommit: 65530c0bad3097a510f507503eae9c5c67db47a0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/12/2021
ms.locfileid: "11643887"
---
# <a name="password-monitor-auto-enabled-for-users"></a>Monitor de contraseñas habilitado automáticamente para usuarios

En este artículo se describe cómo se activará el Monitor de contraseñas en Microsoft Edge para los usuarios seleccionados y se ofrecen a los administradores los pasos para controlar cómo se habilita la monitorización.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 88 o posterior.

## <a name="introduction-benefits-and-availability"></a>Introducción, ventajas y disponibilidad

El Monitor de contraseñas ayuda a los usuarios de Microsoft Edge a proteger sus cuentas en línea informándoles si alguna de sus contraseñas ha sido encontrada en una filtración en línea. Las filtraciones en línea o las infracciones de datos ocurren cuando los usuarios malintencionados roban datos de sitios web o aplicaciones de terceros. Para más información, consulte el documento [Monitor de contraseñas: Proteger contraseñas en Microsoft Edge](https://www.microsoft.com/research/blog/password-monitor-safeguarding-passwords-in-microsoft-edge/)  en el blog de Microsoft Research.

### <a name="benefits"></a>Ventajas

Debido a la frecuencia y el ámbito de estos ataques en línea, tener este tipo de protección se ha vuelto algo necesario para todos los usuarios. Microsoft Edge tiene la capacidad integrada de comprobar de forma segura las contraseñas guardadas de los usuarios frente a contraseñas que se sabe que están en peligro y les avisa si se encuentra una coincidencia.  

## <a name="configure-group-policy-for-password-monitor"></a>Configurar la directiva de grupo para el Monitor de contraseñas

Esta característica se controla mediante la directiva de grupo [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed).

Una vez habilitada la directiva, los usuarios aún necesitan dar su consentimiento para activar la característica. El consentimiento es necesario porque la característica contiene los datos personales y confidenciales del usuario (contraseñas). Si la característica está deshabilitada mediante la directiva de grupo, los usuarios no podrán invalidar esta configuración.  

## <a name="enabling-password-monitor-for-users"></a>Habilitar el Monitor de contraseñas para los usuarios

Una vez habilitada la directiva de monitor de contraseñas, hay diferentes formas de que la característica esté disponible para los usuarios.

- Habilitación automática. Los usuarios que han iniciado sesión con su cuenta de trabajo (Active Directory o Azure Active Directory) y sincronizan sus contraseñas, se habilitarán automáticamente para usar esta característica. Verán la notificación en la siguiente captura de pantalla para informarles que la característica está activada.

  :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-enabled-notice.png" alt-text="Aviso de monitorización de contraseñas habilitado":::

-  Obtener consentimiento explícito. Se pedirá permiso a los usuarios que no tengan activada la Sincronización de contraseñas para activar el Monitor de contraseñas. Se realizarán solicitudes cuando ocurran las siguientes acciones:
   - Cuando un usuario guarda una contraseña nueva.
 
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-save-pw-prompt.png" alt-text="Solicitud para guardar la contraseña":::

   - Cuando un usuario ha iniciado sesión en el explorador con una contraseña guardada.
  
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-after-signin.png" alt-text="Solicitud de confirmación después del inicio de sesión":::
   
- Activación directa. Los usuarios pueden ir a **Configuración** > **Contraseñas** en cualquier momento y Activar o Desactivar la característica.

## <a name="user-scenarios-with-password-monitor-auto-enabled"></a>Escenarios de usuario con el Monitor de contraseña habilitado automáticamente

En la tabla siguiente se muestran escenarios en los que el Monitor de contraseñas está habilitado automáticamente y cómo funcionará en los dispositivos de usuarios.

| Escenario | Condiciones de base | Impacto |
|--|--|--|
| 1 con sincronización activada | Sincronización ACTIVADA<br>Característica habilitada anteriormente: No<br>Respuesta a la interfaz de usuario de consentimiento: ninguna | La característica se habilita de forma predeterminada y se muestra una burbuja de aviso 2 minutos después de que se inicia el explorador.<br>- Si la sincronización se desactiva después de eso, la característica se deshabilitará.<br>- Si la característica se desactiva antes de modificar la sincronización, la sincronización ya no afectará a la característica.   |
| 2 con sincronización activada | Sincronización ACTIVADA<br>Característica habilitada anteriormente: Sí<br>Respuesta a la interfaz de usuario de consentimiento: ninguna | La característica permanece igual que la elección del usuario.  La burbuja de aviso no se muestra y el cambio de sincronización no afecta el valor de la característica.|
| 3 con sincronización desactivada | Sincronización Desactivada<br>Característica habilitada anteriormente: No<br>Respuesta a la interfaz de usuario de consentimiento: ninguna | La sincronización estará desactivada y la característica permanecerá deshabilitada<br>- En cualquier momento después de eso, si el usuario activa la sincronización sin modificar la característica: la característica estará habilitada y la notificación de habilitación automática se mostrará 2 minutos después de activar la sincronización. <br> - Si la sincronización se desactiva de nuevo, la característica será deshabilitada. <br>- Si se cambia la característica antes de activar la sincronización, la sincronización ya no afectará al Monitor de contraseñas.  |  
| 4 con sincronización desactivada | Sincronización DESACTIVADA<br>Característica habilitada anteriormente: Sí<br>Respuesta a la interfaz de usuario de consentimiento: ninguna | La característica permanece igual que la elección del usuario, la burbuja de aviso no se muestra y el cambio de sincronización no afecta al valor de la característica.  |

Además, si los usuarios han iniciado sesión con una cuenta de trabajo restringida mediante directivas para cualquiera de las siguientes opciones, la característica NO se habilitará automáticamente para ellos:

- El Monitor de contraseñas está deshabilitado  
- La Sincronización de contraseñas está deshabilitada
- El uso compartido de datos con servidores de Microsoft está deshabilitado

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

### <a name="how-can-password-monitor-be-disabled-for-my-organization"></a>¿Cómo puedo deshabilitar el Monitor de contraseñas para mi organización?

Puede deshabilitar el Monitor de contraseñas de su organización mediante las siguientes acciones:
- Usar la directiva de grupo PasswordMonitorAllowed.
- Impedir que los datos se sincronicen y se envíen a los servidores de Microsoft.

  > [!NOTE]
  > El Monitor de contraseñas puede funcionar incluso si la Sincronización de contraseñas está deshabilitada, siempre y cuando el usuario haya dado su consentimiento explícito para activar la característica o la haya activado por sí mismo a través de Configuración.

### <a name="what-happens-if-a-user-for-whom-the-feature-has-been-auto-enabled-turns-password-monitor-off-via-settings"></a>¿Qué sucede si un usuario para el que se ha habilitado automáticamente la característica desactiva el Monitor de contraseñas a través de Configuración?

Se respeta la configuración del usuario y la característica permanecerá deshabilitada para ese usuario. Sin embargo, es posible que se le vuelva a mostrar un cuadro de diálogo de consentimiento en caso de que nunca antes haya respondido a la petición de consentimiento.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)