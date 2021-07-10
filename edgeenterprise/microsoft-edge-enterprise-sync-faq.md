---
title: Preguntas frecuentes sobre sincronización empresarial de Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Preguntas más frecuentes sobre la sincronización empresarial de Microsoft Edge.
ms.openlocfilehash: a13e1f02f6e871004d45f81159d5cf0a3397b6ad
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643146"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a>Preguntas frecuentes sobre sincronización empresarial de Microsoft Edge

Este artículo responde a las preguntas más frecuentes acerca de la sincronización empresarial para Microsoft Edge versión 77 o posterior.

## <a name="security-and-serverdata-compliance"></a>Seguridad y cumplimiento de datos/servidor

### <a name="is-the-synced-data-encrypted"></a>¿Se cifran los datos sincronizados?

Los datos se cifran en el transporte con TLS 1.2 o superior. Todos los tipos de datos también se cifran en reposo en el servicio de Microsoft con AES128. Todos los tipos de datos, excepto los que se usan para la sincronización de pestañas abiertas e historial, también se cifran antes de salir del dispositivo del usuario con claves administradas a través de [Azure Information Protection](./microsoft-edge-policies.md#restrictsignintopattern).

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a>¿Por qué las pestañas abiertas y los datos del historial no tienen un cifrado adicional del lado del cliente?

Para reducir la utilización de recursos en los dispositivos de los usuarios finales, los datos del historial se generan del lado del servidor en función de los datos de itinerancia de las pestaña abiertas. Este proceso no sería posible con el cifrado de datos del lado del cliente. Para deshabilitar la sincronización de pestañas abiertas e historial, aplique las directivas [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) o [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled).

### <a name="can-tenant-admins-bring-their-own-key"></a>¿Los administradores de espacios empresariales pueden poner su propia clave?

Sí, a través de [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

### <a name="where-is-microsoft-edge-sync-data-stored"></a>¿Dónde se almacenan los datos de sincronización de Microsoft Edge?

Los datos sincronizados para las cuentas de Azure AD se almacenan en servidores seguros, en función del identificador de espacio empresarial. Por ejemplo, los datos de un espacio empresarial que está registrado en Estados Unidos se almacenan en los servidores localizados en una ubicación geográfica para esa región y usan la misma solución de almacenamiento que las aplicaciones de Office.

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a>¿Los datos salen de la nube en algún momento de Microsoft, aparte de sincronizarse con Microsoft Edge?

No.

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a>¿Qué términos de servicio se aplican a la sincronización empresarial?

Las condiciones de servicio para la sincronización de Microsoft Edge se incluyen en la licencia del software de Microsoft visible en Microsoft Edge en *edge://terms*. En última instancia, la suscripción y los términos de servicio de Azure AD se incluyen en los [Términos del servicio en línea](https://www.microsoft.com/licensing/product-licensing/products)de Microsoft.

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a>¿Microsoft Edge es compatible con el cumplimiento normativo de Government Community Cloud (GCC) High?

Actualmente, no. Para los clientes de la nube de GCC High, la sincronización de Microsoft Edge está deshabilitada.

## <a name="applying-sync"></a>Aplicación de sincronización

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a>¿Por qué la sincronización de Microsoft Edge no es compatible con todas las suscripciones de M365?

La sincronización empresarial depende de [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), que no está disponible en todas las suscripciones de M365.

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a>¿La sincronización de Microsoft Edge está basada en Enterprise State Roaming (ESR)?

No. ESR se puede usar para habilitar la sincronización, pero la sincronización de Microsoft Edge no forma parte de ESR. Para más información, consulte [Sincronización de Microsoft Edge](/DeployEdge/microsoft-edge-enterprise-sync) y [Microsoft Edge y Enterprise State Roaming](/DeployEdge/microsoft-edge-enterprise-state-roaming).

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a>¿Microsoft Edge admitirá en algún momento la sincronización entre Microsoft Edge e IE?

No hay planes para admitir esta sincronización. Si aún necesita Internet Explorer (IE) en su entorno para usar aplicaciones heredadas, considere la posibilidad de usar el [nuevo modo de IE](./edge-ie-mode.md).

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a>¿Microsoft Edge se sincronizará con Microsoft Edge (versión anterior)?

No lo hará. Creemos que la conexión de estos dos ecosistemas provocará un compromiso respecto de la confiabilidad de la sincronización en Microsoft Edge. Nos aseguraremos de que los datos existentes se migren a Microsoft Edge. Los usuarios también podrán importar datos desde el explorador de su elección, lo que también significa que Microsoft Edge no tendrá una forma de sincronizar con IE.

## <a name="managing-sync"></a>Administración de sincronización

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a>¿Es posible impedir que los usuarios sincronicen con un espacio empresarial personal?

No directamente, pero puede determinar qué perfiles pueden iniciar sesión en Microsoft Edge mediante la directiva [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern).

## <a name="see-also"></a>Consulta también

- [Sincronización de Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)