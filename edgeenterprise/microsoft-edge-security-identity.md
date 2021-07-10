---
title: Soporte y configuración de identidad de Microsoft Edge
ms.author: avvaid
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Soporte y configuración de identidad de Microsoft Edge
ms.openlocfilehash: 18b82c3f0c4af0e383dd50266c3d9184c76b23af
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641386"
---
# <a name="microsoft-edge-identity-support-and-configuration"></a>Soporte y configuración de identidad de Microsoft Edge

En este artículo se describe cómo Microsoft Edge usa la identidad para admitir funciones como la sincronización y el inicio de sesión único (SSO). Microsoft Edge admite el inicio de sesión con Active Directory Domain Services (AD DS), Azure Active Directory (Azure AD) y cuentas Microsoft (MSA). Actualmente, Microsoft Edge solo es compatible con cuentas de Azure Active Directory (Azure AD) que pertenecen a la nube global o a la nube independiente de GCC. Estamos trabajando para agregar compatibilidad con otras nubes independientes.

> [!NOTE]
> Esto se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="browser-sign-in-and-authenticated-features"></a>Funciones de inicio de sesión y autenticadas en el explorador

Microsoft Edge admite el inicio de sesión en un perfil de explorador con una cuenta de dominio, Azure AD o MSA. El tipo de cuenta que se usa para el inicio de sesión determina las funciones autenticadas que están disponibles para el usuario en Microsoft Edge. En la siguiente tabla se resume la compatibilidad de funciones para cada tipo de cuenta.

| Característica   | Azure AD Premium | Azure AD Free | AD DS local | MSA     |
|----|------------------|---------------|----------------|---------|
| Sincronización | Sí | No | No | Sí |
| SSO con token de actualización principal | Sí | Sí | No | Sí |
| SSO sin problemas | Sí | Sí | Sí | N/D |
| Autenticación de Windows integrada | Sí | Sí | Sí | N/D |
| Página Nueva pestaña de empresa | Requiere O365 |   Requiere O365 | No | N/D |
| Búsqueda de Microsoft | Requiere O365 | Requiere O365 | No | N/D |

## <a name="how-users-can-sign-into-microsoft-edge"></a>Cómo iniciar sesión en Microsoft Edge

### <a name="automatic-sign-in"></a>Inicio de sesión automático

Microsoft Edge usa la cuenta del SO predeterminada para iniciar sesión automáticamente en el explorador. En función de cómo esté configurado un dispositivo, los usuarios pueden iniciar sesión automáticamente en Microsoft Edge mediante uno de los siguientes métodos.

- **El dispositivo es híbrido/AAD-J:** disponible en Win10, Windows de nivel inferior y en las versiones de servidor correspondientes.
El usuario inicia sesión automáticamente con su cuenta de Azure AD.
- **El dispositivo se ha unido a un dominio:** disponible en Win10, Windows de nivel inferior y en las versiones de servidor correspondientes.
De forma predeterminada, el usuario no podrá iniciar sesión automáticamente. Si quiere que los usuarios inicien sesión con cuentas de dominios automáticamente, use la directiva [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin). Si quiere que los usuarios inicien sesión con cuentas de Azure AD automáticamente, tenga en cuenta la posibilidad de unir los dispositivos de forma híbrida.
- **La cuenta predeterminada del SO es MSA:** Win10 RS3 (versión 1709 y compilación 10.0.16299) y posterior. Este escenario es improbable en los dispositivos de empresa. Pero si la cuenta predeterminada del SO es MSA, Microsoft Edge inicia sesión automáticamente con la cuenta MSA.

### <a name="manual-sign-in"></a>Inicio de sesión manual

Si el usuario no inicia sesión automáticamente en Microsoft Edge, puede hacerlo manualmente durante la experiencia de primera ejecución, la configuración del explorador o abriendo el control flotante de identidad.

### <a name="managing-browser-sign-in"></a>Administrar el inicio de sesión del explorador

Si quiere administrar el inicio de sesión del explorador, puede usar las siguientes directivas:

- Asegúrese de que los usuarios siempre tengan un perfil de trabajo en Microsoft Edge. [Ver NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)
- Restrinja el inicio de sesión a un conjunto de cuentas de confianza. [Ver RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern)
- Deshabilite o fuerce el inicio de sesión del explorador. [Ver BrowserSignin](./microsoft-edge-policies.md#browsersignin)

## <a name="browser-to-web-single-sign-on-sso"></a>Inicio de sesión único (SSO) del explorador a la Web

En algunas plataformas, puede configurar Microsoft Edge para que inicie sesión automáticamente en los sitios web para los usuarios. Esta opción les ahorra el problema de volver a escribir sus credenciales para tener acceso a sus sitios web de trabajo y aumenta su productividad.

### <a name="sso-with-primary-refresh-token-prt"></a>SSO con Token de actualización principal (PRT)

Microsoft Edge tiene un soporte nativo para SSO basado en PRT y no necesita una extensión. En Windows 10 RS3 y versiones posteriores, si un usuario inicia sesión en su perfil de explorador, recibirá el SSO con el mecanismo de PRT en los sitios web compatibles.

Un token de actualización principal (PRT) es una clave de Azure AD que se usa para la autenticación en dispositivos con Windows 10, iOS y Android. Habilita el inicio de sesión único (SSO) entre las aplicaciones que se usan en estos dispositivos. Para obtener más información, consulta [¿Qué es un Token de actualización principal?](/azure/active-directory/devices/concept-primary-refresh-token).

### <a name="seamless-sso"></a>SSO sin problemas

Al igual que el SSO de PRT, Microsoft Edge tiene un soporte nativo para el SSO de conexión directa sin necesidad de una extensión. En Windows 10 RS3 y versiones posteriores, si un usuario inicia sesión en su perfil de explorador, recibirá el SSO con el mecanismo de PRT en los sitios web compatibles.

El inicio de sesión único de conexión directa hace que los usuario inicien sesión automáticamente cuando están en dispositivos corporativos conectados a una red corporativa. Cuando se habilita, los usuarios no tienen que escribir su contraseña para iniciar sesión en Azure AD. Por lo general, ni siquiera tienen que escribir sus nombres de usuario. Para obtener más información, consulta [Inicio de sesión único sin problemas de Active Directory](/azure/active-directory/hybrid/how-to-connect-sso).

### <a name="windows-integrated-authentication-wia"></a>Autenticación integrada de Windows (WIA)

Microsoft Edge también es compatible con la Autenticación integrada de Windows para las solicitudes dentro de la red interna de una organización para cualquier aplicación que use un explorador para su autenticación. Esto es compatible con todas las versiones de Windows 10 y Windows de nivel inferior. De forma predeterminada, Microsoft Edge usa la zona de intranet como una lista de permitidos para WIA. Como alternativa, puede personalizar la lista de servidores que estén habilitados para la Autenticación integrada a través de la directiva [AuthServerAllowlist](./microsoft-edge-policies.md#authserverallowlist). En macOS, esta directiva es necesaria para habilitar la Autenticación integrada.

Para admitir el SSO basado en WIA en Microsoft Edge (versión 77 y posteriores), puede que también deba realizar algunas tareas de configuración del servidor. Es probable que tenga que configurar la propiedad Active Directory Federation Services (AD FS) **WiaSupportedUserAgents** para agregar compatibilidad con la nueva cadena de agente de usuario de Microsoft Edge. Para obtener instrucciones sobre cómo realizar esta acción, vea la configuración [Ver WIASupportedUserAgent](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia#view-wiasupporteduseragent-settings) y [Cambiar WIASupportedUserAgent](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia#change-wiasupporteduseragent-settings). A continuación, se muestra un ejemplo de la cadena de agente de usuario de Microsoft Edge en Windows 10 y puede obtener más información sobre la [cadena de Microsoft Edge aquí](/microsoft-edge/web-platform/user-agent-string). 

El siguiente ejemplo de una cadena de agente de usuario es para la última compilación del canal para desarrolladores en el momento en que se publicó este artículo:<br> `"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3951.0 Safari/537.36 Edg/80.0.334.2"`

Para los servicios que requieren la delegación de credenciales de negociación, Microsoft Edge admite la delegación restringida a través de la directiva [AuthNegotiateDelegateAllowlist](./microsoft-edge-policies.md#authnegotiatedelegateallowlist).

## <a name="additional-authentication-concepts"></a>Conceptos de autenticación adicionales

### <a name="proactive-authentication"></a>Autenticación proactiva

La autenticación proactiva es una optimización del SSO del explorador al sitio web que carga por adelantado la autenticación en ciertos sitios web propios. Esto permite mejorar el rendimiento de la barra de direcciones si el usuario usa Bing como motor de búsqueda. Esto proporciona a los usuarios resultados de Búsqueda de Microsoft para empresas (MSB) y resultados personalizados. También permite la autenticación en servicios clave como la página de pestaña nueva de Office. Puede controlarla mediante la directiva [ProactiveAuthEnabled]( /deployedge/microsoft-edge-policies#proactiveauthenabled).

### <a name="windows-hello-credui-for-ntlm-authentication"></a>CredUI de Windows Hello para la autenticación NTLM

Cuando un sitio web intenta que los usuarios inicien sesión con los mecanismos de autenticación NTLM o Negotiate y el SSO no está disponible, les ofrecemos a una experiencia en la que podrán compartir sus credenciales del SO con el sitio web para cumplir el desafío de autenticación con CredUI de Windows Hello. Este flujo de inicio de sesión solo se mostrará a los usuarios de Windows 10 que no tengan inicio de sesión único durante el desafío de NTLM o Negotiate.

### <a name="sign-in-automatically-using-saved-passwords"></a>Iniciar sesión automáticamente con contraseñas guardadas

Si un usuario guarda las contraseñas en Microsoft Edge, puede habilitar una función para iniciar sesión automáticamente en los sitios web en los que se hayan guardado las credenciales. Para cambiar esta función, los usuarios pueden ir a *edge://settings/passwords*. Si quiere configurar esta característica, puede usar las directivas de [administrador de contraseñas](./microsoft-edge-policies.md#password-manager-and-protection).

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: Microsoft Edge y la identidad](microsoft-edge-video-identity.md)
- [Administración de identidades y acceso](https://www.microsoft.com/security/technology/identity-access-management)
- [Plataforma de identidad](https://developer.microsoft.com/identity)
- [Cuatro pasos para una sólida base de identidad con Azure Active Directory](/azure/active-directory/hybrid/four-steps)