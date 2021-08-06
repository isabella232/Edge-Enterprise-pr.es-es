---
title: 'Seguridad del administrador de contraseñas de Microsoft Edge '
ms.author: v-andreabarr
author: AndreaLBarr
manager: collw
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Seguridad del administrador de contraseñas de Microsoft Edge
ms.openlocfilehash: 41f1b269622e0053703af05f344a2d15e8a4b10e72e9507297b877f8047ccccb
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727063"
---
# <a name="microsoft-edge-password-manager-security"></a>Seguridad del administrador de contraseñas de Microsoft Edge 

Las preguntas más frecuentes incluidas en este artículo describen cómo el administrador de contraseñas integrado de Microsoft Edge proporciona seguridad para las contraseñas de usuarios.

> [!Note]
>Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="how-are-passwords-stored-in-microsoft-edge-and-how-safe-is-this-approach"></a>¿Cómo se almacenan las contraseñas en Microsoft Edge y qué tan seguro es este método?

Microsoft Edge almacena las contraseñas cifradas en el disco. Se cifran mediante AES256 y la clave de cifrado se guarda en un área de almacenamiento del sistema operativo (SO). Esta técnica se denomina cifrado de datos local. Aunque no todos los datos del explorador están cifrados, los datos confidenciales, como contraseñas, números de tarjeta de crédito y cookies, se cifran cuando se guardan.

El administrador de contraseñas de Microsoft Edge cifra las contraseñas para que solo se pueda acceder a ellas cuando un usuario haya iniciado sesión en el sistema operativo. Incluso si un atacante tiene derechos de administrador o acceso sin conexión y puede acceder a los datos almacenados localmente, el sistema está diseñado para impedir que el atacante obtenga las contraseñas de texto no cifrado de un usuario que no haya iniciado sesión.

La forma de descifrar las contraseñas de otro usuario es que ese usuario haya iniciado sesión y el atacante tuviera la contraseña del usuario o haya puesto en peligro el controlador de dominio.

### <a name="about-the-encryption-method"></a>Acerca del método de cifrado

La clave de cifrado del perfil está protegida con OSCrypt de Chromium y usa las siguientes ubicaciones de almacenamiento del sistema operativo específicas de la plataforma:

- En Windows, el área de almacenamiento es DPAPI

- En Mac, el área de almacenamiento es el Llavero

- En Linux, el área de almacenamiento es Gnome Keyring o KWallet

Todas estas áreas de almacenamiento cifran la clave AES256 con una clave accesible para algunos o todos los procesos que se ejecuten como usuario. Este vector de ataque a menudo se presenta en blogs como una posible "violación" o "vulnerabilidad", lo que es una comprensión incorrecta del modelo de amenazas del explorador y la posición de seguridad.

Sin embargo, los ataques físicamente locales y el malware están fuera del modelo de amenazas y, en estas condiciones, los datos cifrados serían vulnerables. Si el equipo está infectado con malware, un atacante puede obtener acceso descifrado a las áreas de almacenamiento del explorador. El código del atacante, que se ejecuta como su cuenta de usuario, puede hacer todo lo que usted puede hacer.

## <a name="why-encrypt-data-locally-why-not-store-the-encryption-key-elsewhere-or-make-it-harder-to-obtain"></a>¿Por qué cifrar los datos localmente? ¿Por qué no almacenar la clave de cifrado en otro lugar o dificultar la obtención?

Los exploradores de Internet (incluido Microsoft Edge) no están equipados con defensas para protegerse contra amenazas en las que todo el dispositivo está en peligro debido a que el malware se ejecuta como el usuario en el equipo. Sin embargo, programas como SmartScreen de Microsoft Defender y las protecciones de nivel de sistema operativo como Windows Defender están diseñados para garantizar que el dispositivo no esté en peligro para empezar.

A pesar de su incapacidad para proteger contra el malware de plena confianza, el Cifrado de datos local es útil en determinados escenarios. Por ejemplo, si un atacante encuentra una forma de robar archivos del disco sin la capacidad de ejecutar código o ha robado un portátil que no está protegido con el Cifrado de disco completo, el Cifrado de datos local dificultará al ladrón obtener los datos almacenados.

## <a name="do-you-recommend-storing-passwords-in-microsoft-edge"></a>¿Es recomendable almacenar contraseñas en Microsoft Edge?

Los usuarios que pueden confiar en el administrador de contraseñas integrado de Microsoft Edge pueden (y, de hecho, lo hacen) usan contraseñas más seguras y únicas porque no necesitan recordarlas todas y escribirlas con tanta frecuencia. Y como el administrador de contraseñas solo rellenará automáticamente las contraseñas en los sitios a los que pertenecen, es menos probable que los usuarios sufran un ataque de suplantación de identidad (phishing).

> [!Note]
>Los informes del sector muestran que el 80 % de los incidentes en línea están relacionados con la suplantación de identidad (phishing) y que más del 37 % de los usuarios no capacitados no superan las pruebas de phishing.

El administrador de contraseñas de Microsoft Edge es cómodo y fácil de distribuir, lo que contribuye a mejorar la seguridad. Cuando se combina con la sincronización, puede tener todas las contraseñas en todos sus dispositivos y es fácil usar una contraseña diferente para cada sitio web. Puede usar contraseñas largas y complejas que no tiene que recordar para cada sitio y evitar la molestia de escribir una cadena compleja de caracteres cada vez. La conveniencia del administrador de contraseñas implica que hay menos riesgo de sufrir un ataque de phishing.

Sin embargo, el uso de un administrador de contraseñas vinculado a la sesión de inicio de sesión del sistema operativo del usuario también implica que un atacante de esa sesión puede recuperar inmediatamente todas las contraseñas guardadas del usuario. Al no haber un administrador de contraseñas para robar, un adversario tendría que realizar un seguimiento de las pulsaciones de teclas o supervisar las contraseñas enviadas.

La decisión de usar un administrador de contraseñas se resume a evaluar las diversas ventajas que hemos descrito frente a la posibilidad de que todo el dispositivo se vea en peligro. Para la mayoría de los modelos de amenazas, el administrador de contraseñas de Microsoft Edge es la opción recomendada.

> [!Note]
>Si una empresa está preocupada por el robo de una contraseña específica o que un sitio se vea en peligro a causa de una contraseña robada, se deben tomar precauciones adicionales. Algunas soluciones eficaces que ayudan a mitigar este tipo de incidentes es el Inicio de sesión único (SSO) a través de Active Directory, Azure Active Directory o un tercero. Otras soluciones incluyen la autenticación 2FA (como [MS Authenticator](/azure/active-directory/user-help/user-help-auth-app-download-install)) o [WebAuthN](https://webauthn.guide/).

## <a name="should-a-password-manager-be-enabled-by-an-organization"></a>¿Una organización debe habilitar un administrador de contraseñas?

La respuesta simple y sencilla es: Sí, use el administrador de contraseñas del explorador.

Una respuesta más completa implica tener un conocimiento detallado del modelo de amenazas, porque las opciones y decisiones de seguridad varían en función de los distintos modelos de amenazas. Algunas preguntas relevantes que debe tener en cuenta al pensar si debe habilitar el administrador de contraseñas para su organización son:

- ¿Qué tipos de atacantes le preocupan?

- ¿En qué tipo de sitios web inician sesión sus usuarios?

- ¿Los usuarios seleccionan contraseñas seguras y únicas?

- ¿Las cuentas de sus usuarios están protegidas con 2FA?

- ¿Qué tipo de ataques son más probables?

- ¿Cómo se protegen los dispositivos de la empresa frente al malware?

- ¿Cuál es la tolerancia personal de los usuarios a los inconvenientes?

- Tenga en cuenta el impacto de la sincronización de datos.

Es importante considerar la seguridad de los datos de usuario, ya que se sincronizan con varios dispositivos de usuario, así como el grado de control que tiene la organización en la sincronización de datos de autorrelleno.

Sincronización de datos y Microsoft Edge:

- La sincronización de datos se puede habilitar o deshabilitar según lo desee en toda la organización.

- Seguridad de datos en tránsito y en reposo en la nube: todos los datos sincronizados se cifran en tránsito a través de HTTPS cuando se transfieren entre el explorador y los servidores de Microsoft. Los datos sincronizados también se almacenan en un estado cifrado en los servidores de Microsoft. Los tipos de datos confidenciales, como direcciones y contraseñas, se cifran aún más en el dispositivo antes de sincronizarse. Si usa una cuenta de trabajo o escuela, todos los tipos de datos se cifran aún más antes de sincronizarse con Microsoft Information Protection.

## <a name="why-do-microsoft-security-baselines-recommend-disabling-the-password-manager"></a>¿Por qué las líneas base de seguridad de Microsoft recomiendan deshabilitar el administrador de contraseñas?

Actualmente, el equipo de seguridad de Microsoft ha calificado el impacto de un gusano que comprometa una red de PCS de la empresa (lo que provoca la pérdida de todas las credenciales en los administradores de contraseñas de todos los dispositivos) como más grave que el riesgo (más probable pero de menor impacto) de ataques de suplantación de identidad dirigidos que comprometan una única credencial especificada por el usuario.

Esta evaluación se encuentra en discusión y está sujeta a cambios con la adición de nuevas características de mejora de la seguridad en Microsoft Edge.

## <a name="can-malicious-extensions-gain-access-to-passwords"></a>¿Pueden las extensiones malintencionadas obtener acceso a las contraseñas?

Una extensión con permiso para interactuar con una página es inherentemente capaz de tener acceso a cualquier cosa desde esa página, incluida una contraseña rellenada automáticamente. Del mismo modo, una extensión malintencionada puede modificar el contenido de los campos de un formulario y las solicitudes/respuestas de red para hacer mal uso de la autoridad del contexto de inicio de sesión del usuario actual.

Sin embargo, Microsoft Edge proporciona un amplio conjunto de directivas que permiten un control preciso sobre las extensiones instaladas. El uso de las directivas incluidas en la tabla siguiente es necesario para proteger los datos corporativos.

| Directiva | Título |
|-|-|
|[BlockExternalExtensions](/deployedge/microsoft-edge-policies#blockexternalextensions)|Bloquear la instalación de extensiones externas|
|[ExtensionAllowedTypes](/deployedge/microsoft-edge-policies#extensionallowedtypes)|Configurar los tipos de extensión permitidos|
|[ExtensionInstallAllowlist](/deployedge/microsoft-edge-policies#extensioninstallallowlist)|Permitir que se instalen extensiones específicas|
|[ExtensionInstallBlocklist](/deployedge/microsoft-edge-policies#extensioninstallblocklist)|Controlar qué extensiones no se pueden instalar|
|[ExtensionInstallForcelist](/deployedge/microsoft-edge-policies#extensioninstallforcelist)|Controlar qué extensiones se instalan de forma silenciosa|
|[ExtensionInstallSources](/deployedge/microsoft-edge-policies#extensioninstallsources)|Configurar la extensión y los orígenes de instalación de los scripts de usuario|
| [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) |Configurar las opciones de administración de extensiones |

## <a name="how-does-the-microsoft-edge-password-manager-compare-with-a-third-party-product"></a>¿Cómo se compara el administrador de contraseñas de Microsoft Edge con un producto de terceros?

En la tabla siguiente se muestra cómo se compara el administrador de contraseñas de Microsoft Edge con administradores de contraseñas de terceros.

| Administrador de contraseñas de terceros | Administrador de contraseñas de Microsoft Edge|
|-|-|
| *Sincronización del servidor*. Algunos productos almacenan contraseñas en la nube para sincronizar todos los dispositivos. Esta característica es útil, pero existe un riesgo si el servicio en la nube se pone en peligro y se exponen los datos. **Observaciones:**   El riesgo se mitiga al tener contraseñas cifradas en la nube y almacenar la clave de cifrado en los dispositivos para que los atacantes no puedan acceder a la clave ni a las contraseñas.| Existe un riesgo de exposición a la nube porque las contraseñas se sincronizan entre dispositivos Windows que tienen Microsoft Edge instalado. **Observaciones:**   Este riesgo se mitiga mediante los pasos de seguridad de datos descritos en este artículo.|
| *Confianza*. Es necesario confiar en que el tercero no está haciendo nada malintencionado, como enviar sus contraseñas a otro usuario. **Observaciones:**   Este riesgo puede mitigarse revisando el código fuente (en el caso de los productos de código abierto) o pensando que el proveedor se preocupa por su reputación e ingresos. | **Observaciones:** Microsoft es un proveedor conocido y de confianza con décadas de historia en proporcionar seguridad y productividad de nivel empresarial, con recursos diseñados para proteger sus contraseñas en todo el mundo. |
| *Seguridad de cadena de suministro*. Es difícil comprobar que el proveedor tiene procesos seguros de cadena de suministro, compilación y versión para el código fuente. |**Observaciones:**  Microsoft tiene procesos internos sólidos para garantizar un riesgo mínimo para el código fuente. |
| *Cliente o cuenta en peligro*.Si un dispositivo cliente o una cuenta de usuario están en peligro, un atacante puede obtener las contraseñas. **Notas:** Este riesgo se mitiga para algunos administradores de contraseñas que requieren que el usuario escriba una Contraseña maestra que no esté almacenada localmente para descifrar las contraseñas.Una Contraseña maestra es solo una mitigación parcial porque un atacante podría leer pulsaciones de teclas y obtener la contraseña maestra a medida que se escribe o leer contraseñas de la memoria del proceso al rellenar un campo de formulario. | **Notas:** Microsoft ofrece protecciones de nivel de sistema operativo como Windows Defender, diseñadas para garantizar que el dispositivo no se vea en peligro para empezar. Sin embargo, si un dispositivo cliente está en peligro, es posible que un atacante pueda descifrar las contraseñas. |

> [!Note]
> Los productos de terceros pueden proporcionar protección contra modelos de amenazas adicionales, pero esto es a expensas de la complejidad o la facilidad de uso. El administrador de contraseñas de Microsoft Edge está diseñado para proporcionar una administración de contraseñas cómoda y fácil de usar que los administradores de TI pueden controlar completamente mediante directiva de grupo y sin la necesidad de confiar en un tercero.

## <a name="why-doesnt-microsoft-offer-a-master-password-to-protect-the-data"></a>¿Por qué Microsoft no ofrece una Contraseña maestra para proteger los datos?

Cuando las contraseñas del explorador se cifran en el disco, la clave de cifrado está disponible para cualquier proceso del dispositivo, lo que incluye cualquier malware que se ejecute localmente. Incluso si las contraseñas se cifran en un "almacén" mediante una clave maestra, se descifrarán cuando se carguen en el espacio de memoria del explorador y se pueden recopilar después de desbloquear el almacén.

Una característica de Contraseña maestra (que autentica al usuario antes de rellenar automáticamente sus datos) ofrece una ventaja en cuanto a comodidad, para una mitigación de amenazas más amplia. En concreto, ayuda a reducir la ventana de exposición de datos contra malware latente o atacantes físicamente locales. Sin embargo, una Contraseña maestra no es la solución perfecta, ya que los atacantes locales y el malware dedicado tienen diversas estrategias para eludir la protección de una Contraseña maestra.

> [!Note]
> Microsoft reconoce el valor de autenticar a los usuarios antes de autorrellenar y esta funcionalidad se agregará a Microsoft Edge en una versión futura.

## <a name="can-using-a-password-manager-impact-my-privacy"></a>¿El uso de un administrador de contraseñas puede afectar a mi privacidad?

No, no si se realizan pasos para proteger el acceso a las contraseñas guardadas.

Hay una vulnerabilidad conocida que usan algunos anunciantes, al emplear contraseñas almacenadas para identificar y realizar un seguimiento de los usuarios de forma exclusiva. Para obtener más información, consulte [Los anunciantes extraen datos del administrador de contraseñas de su explorador](https://www.theverge.com/2017/12/30/16829804/browser-password-manager-adthink-princeton-research). Los exploradores han tomado medidas para mitigar este  [problema de privacidad](https://bugs.chromium.org/p/chromium/issues/detail?id=798492).La clase PasswordValueGatekeeper se puede usar para limitar el acceso a los datos del campo de contraseña, incluso cuando el explorador está configurado para autorrellenar cuando se carga.

Esta amenaza de recopilación de información de usuario se puede mitigar fácilmente habilitando la característica opcional de edge://flags/#fill-on-account-select. Esta característica solo permite agregar contraseñas a un campo de formulario después de que el usuario elija explícitamente una credencial, lo que garantiza que los usuarios estén al tanto de quién recibe sus contraseñas.

## <a name="see-also"></a>Vea también

[Página de aterrizaje de Microsoft Edge para empresas](https://www.microsoft.com/edge/business/download)

[Cómo Microsoft Edge es más seguro que Chrome para empresas en Windows 10](/DeployEdge/ms-edge-security-for-business)
