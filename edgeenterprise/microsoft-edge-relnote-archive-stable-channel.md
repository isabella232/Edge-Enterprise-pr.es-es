---
title: Notas de la versión archivadas para el canal estable de Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas de la versión archivadas para el canal estable de Microsoft Edge
ms.openlocfilehash: d50da924c3c78e38eb55b30cf219145d19fe9816
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11980162"
---
# <a name="archived-release-notes-for-microsoft-edge-stable-channel"></a>Notas de la versión archivadas para el canal estable de Microsoft Edge

Estas notas de versión proporcionan información sobre las nuevas características y las actualizaciones no relacionadas con la seguridad que se incluyen en el canal estable de Microsoft Edge. Todas las actualizaciones de seguridad se muestran [aquí](microsoft-edge-relnotes-security.md).

## <a name="version-88070581-february-25"></a>Versión 88.0.705.81: 25 de febrero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070574-february-17"></a>Versión 88.0.705.74: 17 de febrero

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#february-17-2021).

## <a name="version-88070568-february-11"></a>Versión 88.0.705.68: 11 de febrero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070563-february-5"></a>Versión 88.0.705.63: 5 de febrero

> [!IMPORTANT]
> Esta actualización contiene [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148), que ha sido reportado por el equipo de Chromium como una vulnerabilidad de seguridad.

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#february-5-2021).

## <a name="version-88070562-february-4"></a>Versión 88.0.705.62: 4 de febrero

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#february-4-2021).

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070556-january-28"></a>Versión 88.0.705.56: 28 de enero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070553-january-26"></a>Versión 88.0.705.53: 26 de enero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070550-january-21"></a>Versión 88.0.705.50: 21 de enero

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#january-21-2021).

<!--- begin major 88  --->
### <a name="feature-updates"></a>Actualizaciones de características

- **Desusos:**

  - Desusar la compatibilidad con el protocolo FTP. Se ha quitado la compatibilidad con el protocolo FTP heredado de Microsoft Edge. Si se intenta navegar a un vínculo FTP, el explorador dirigirá el sistema operativo para que abra una aplicación externa para controlar el vínculo FTP. Como alternativa, los administradores de TI pueden configurar Microsoft Edge para usar el modo IE para los sitios que dependen del protocolo FTP.
  - La compatibilidad con Adobe Flash se eliminará. A partir de la versión 88 de Microsoft Edge Beta, se eliminarán la funcionalidad y la compatibilidad con Adobe Flash. Más información: [actualización sobre la finalización del soporte en Adobe Flash Player: blog de Microsoft Edge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Autenticación:**

  - El inicio de sesión único (SSO) ya está disponible para las cuentas de Azure Active Directory (Azure AD) y las cuentas de Microsoft (MSA) en versiones de Windows de nivel inferior. Un usuario que haya iniciado sesión en Microsoft Edge en una versión de Microsoft Windows de nivel inferior (versiones 7 y 8.1) ahora tendrá la sesión iniciada de manera automática en los sitios web que estén configurados para permitir el inicio de sesión único con cuentas profesionales y de Microsoft (por ejemplo, bing.com, office.com, msn.com, outlook.com).<br>Nota: es posible que un usuario tenga que cerrar sesión y volver a iniciarla si ha iniciado sesión en Microsoft Edge en una versión anterior a Microsoft Edge 88 para poder aprovechar esta característica.
  
  - Inicio de sesión único (SSO) para trabajar en sitios con cualquier cuenta de Windows Azure Active Directory (Azure AD) que esté en el sistema en perfiles de Microsoft Edge que no sean de Azure AD. Esta característica se puede habilitar para cualquier perfil que no haya iniciado sesión con una cuenta de trabajo o escuela y que no sea invitado o privado, y permite el uso de cualquier cuenta de trabajo o escuela que haya iniciado sesión en el sistema operativo con ese perfil. Esta característica se puede definir en **Configuración** > **Perfiles** > **Preferencias de perfil** > **Permitir el inicio de sesión único en sitios profesionales o educativos con este perfil o**.
  
    > [!NOTE]
    > "Inicio de sesión único (SSO) para todas las cuentas de Windows que usan el perfil de Microsoft Edge" es una actualización de las notas de la versión del 21 de enero.

- **Opción de modo de pantalla completa para finalizar la sesión**. El botón "Finalizar sesión" ahora está disponible en una experiencia de navegación pública en modo de pantalla completa. Esta característica garantiza que los datos y la configuración del explorador se eliminen cuando se cierra Microsoft Edge. Más información sobre las características y la guía básica del modo de pantalla completa, [Configurar el modo de pantalla completa de Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md).

- **Seguridad y privacidad:**

  - Se generan alertas si se encuentra la contraseña de un usuario en una filtración en línea. Las contraseñas de usuario se comprueban con un repositorio de credenciales infringidas y se envía una alerta al usuario si se encuentra una coincidencia. Para garantizar la seguridad y la privacidad, las contraseñas de los usuarios se dividen y cifran cuando se comparan con la base de datos de credenciales filtradas.
  - Actualice automáticamente el contenido mixto. Las páginas seguras que se proporcionan a través de HTTPS pueden contener imágenes de referencias que se sirven a través de HTTP no seguro. Para mejorar la privacidad y la seguridad en Microsoft Edge 88, esas imágenes se recuperarán a través de HTTPS. Si la imagen no está disponible a través de HTTPS, no se cargará.
  - Vea permisos de sitio por sitio y por actividad reciente. A partir de Microsoft Edge 88, los usuarios podrán administrar los permisos de los sitios más fácilmente. Podrán ver los permisos por sitio web en lugar de solo por tipo de permiso. Además, hemos agregado una sección de actividades recientes que le mostrará al usuario todos los cambios recientes en los permisos de su sitio.
  - Más controles para las cookies del explorador. A partir de Microsoft Edge 88, los usuarios pueden eliminar cookies de terceros sin que esto afecte a las cookies principales. Además, los usuarios podrán filtrar las cookies según si son principales o de terceros y ordenar por nombre, número de cookies y la cantidad de datos almacenados y modificados por última vez.

- **Contraseñas:**

  - Generador de contraseñas. Microsoft Edge ofrece un generador de contraseñas seguras integrado que puede usar al registrarse para obtener una nueva cuenta o al cambiar una contraseña existente. Solo tiene que buscar la lista desplegable de contraseñas sugeridas del explorador en el campo de contraseña y, cuando se seleccione, se guardará automáticamente en el explorador y se sincronizará en todos los dispositivos para facilitar su uso en el futuro.
  - Monitor de contraseñas. Cuando cualquiera de las contraseñas guardadas en el explorador coincida con las que se ven en la lista de credenciales filtradas, Microsoft Edge le notificará y le pedirá que actualice la contraseña. El Monitor de contraseñas busca coincidencias por usted y está activado de forma predeterminada.
  - Editar contraseña. Ahora puede editar las contraseñas guardadas directamente en la configuración de Microsoft Edge. Reemplazar una contraseña anterior guardada por una nueva cada vez que se actualice la contraseña fuera de Microsoft Edge es sencillo. Solo debe editar la contraseña guardada en Configuración. 

- **Mejorar la velocidad de inicio de Microsoft Edge con el inicio rápido.** Para mejorar la velocidad de inicio de Microsoft Edge, hemos desarrollado una característica denominada inicio rápido. El inicio rápido hace que Microsoft Edge se inicie más rápido al habilitar Microsoft Edge para que se ejecute en segundo plano. Nota: esta característica está limitada a un grupo de usuarios seleccionado aleatoriamente que han habilitado la experimentación. Estos usuarios proporcionan comentarios al equipo de características.

- **Productividad:**

  - Mejorar la productividad y la multitarea con pestañas verticales. A medida que el número de pestañas horizontales crece, los títulos de sitios comienzan a cortarse y los controles de pestaña se pierden a medida que se reducen las pestañas. Esto interrumpe el flujo de trabajo del usuario, ya que dedica más tiempo a buscar, cambiar y administrar sus pestañas, y menos tiempo a la tarea. Las pestañas verticales permiten a los usuarios mover sus pestañas al costado, donde los iconos alineados verticalmente y los títulos de sitio más largos hacen que sea más fácil digitalizar, identificar y cambiar a la pestaña que quiera abrir rápidamente.
  - Rellene automáticamente el campo de fecha de nacimiento. Microsoft Edge ya ayuda a ahorrar tiempo y esfuerzo mientras rellenas formularios y crea cuentas en línea mediante el rellenado automático de datos de usuario, como direcciones, nombres, números de teléfono, etc. Microsoft Edge ahora es compatible con el campo de fecha de nacimiento que los usuarios pueden guardar y rellenar automáticamente. Un usuario puede ver, editar y eliminar esta información en cualquier momento en la configuración de su perfil.
  - Mejoras en el historial de Cerrados recientemente. Cerrados recientemente ahora mantiene las últimas 25 pestañas y ventanas de cualquier sesión de exploración pasada en lugar de solo la sesión anterior. Los usuarios pueden seleccionar Cerrados recientemente en la nueva experiencia de historial para ver todas las pestañas que estaban abiertas.
  - La función "Tu día de un vistazo" está activada de forma predeterminada. A partir de la versión 88 de Microsoft Edge, los trabajadores de la información pueden beneficiarse de las características de productividad inteligentes en su página de Nueva pestaña. Los usuarios de Microsoft Edge 87 también experimentarán estas características en un plazo de 2 semanas después del lanzamiento de la versión 88 de Microsoft Edge. Ofrecemos contenido personalizado y relevante a los usuarios que hayan iniciado sesión con su cuenta profesional o educativa, con tecnología de M365 Graph. Los usuarios pueden examinar rápidamente sus módulos "Tu día de un vistazo" para realizar un seguimiento sencillo de las reuniones y del trabajo reciente, así como iniciar rápidamente las aplicaciones que quiera usar.

- **Sincronización del historial y las pestañas abiertas.** Para el deleite de nuestros usuarios, ahora el historial y pestañas abiertas se pueden sincronizar. Habilitar estas características ayudará a los usuarios a continuar su sesión anterior. El historial de exploración y las pestañas abiertas estarán disponibles en todos sus dispositivos de sincronización. Hemos actualizado las directivas de sincronización y del historial de exploradores, por lo que ahora los usuarios están conectados y son productivos en todos los dispositivos mediante Microsoft Edge. [Más información](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/).

- **PDF:**

  - Presentación de documentos PDF en la vista de libro (dos páginas). A partir de la versión 88 de Microsoft Edge, los usuarios pueden ver documentos PDF en una sola página o en la vista de libro de dos páginas. Para cambiar la vista, haga clic en el botón **Vista de página** de la barra de herramientas.
  - Compatibilidad con notas de texto anclado para archivos PDF. A partir de la versión 87 de Microsoft Edge, los usuarios pueden agregar notas de texto escrito en cualquier parte del texto en archivos PDF.

- **Fuentes:**

  - Los iconos del explorador se actualizan en el sistema de diseño Fluent. Como parte de nuestro trabajo constante en torno a Fluent Design en el explorador, hemos realizado cambios para alinear los iconos con el nuevo sistema de iconos de Microsoft. Estos cambios afectarán a numerosas interfaces de usuario con un alto nivel de función táctil, como pestañas, barra de direcciones, iconos de navegación y orientación, que se encuentran en los distintos menús.
  - Representación de fuentes mejorada. La representación de texto se ha mejorado para mejorar la claridad y para reducir el efecto borroso.

### <a name="policy-updates"></a>Actualizaciones de directivas

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado dieciocho directivas nuevas. Descargue las Plantillas administrativas actualizadas desde la [página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se han agregado las siguientes directivas nuevas.

- [BasicAuthOverHttpEnabled](./microsoft-edge-policies.md#basicauthoverhttpenabled): permite la autenticación básica para HTTP.
- [BlockExternalExtensions](./microsoft-edge-policies.md#blockexternalextensions): bloquea las extensiones externas para que no se instalen.
- [InternetExplorerIntegrationLocalFileAllowed](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileallowed): permite el inicio de archivos locales en el modo de Internet Explorer.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist): abre archivos locales en la lista de permiso de extensión de archivos en el modo de Internet Explorer.
- [InternetExplorerIntegrationLocalFileShowContextMenu](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileshowcontextmenu): muestra el menú contextual para abrir un vínculo en el modo de Internet Explorer.
- [IntranetRedirectBehavior](./microsoft-edge-policies.md#intranetredirectbehavior): comportamiento de redirección de intranet.
- [PrinterTypeDenyList](./microsoft-edge-policies.md#printertypedenylist): deshabilita los tipos de impresora en la lista de denegación.
- [ShowMicrosoftRewards](./microsoft-edge-policies.md#showmicrosoftrewards): muestra las experiencias de Microsoft Rewards.
- [SleepingTabsEnabled](./microsoft-edge-policies.md#sleepingtabsenabled): configura las pestañas en suspensión.
- [SleepingTabsTimeout](./microsoft-edge-policies.md#sleepingtabstimeout): establece el tiempo de suspensión de la pestaña en segundo plano para las pestañas en suspensión.
- [SleepingTabsBlockedForUrls](./microsoft-edge-policies.md#sleepingtabsblockedforurls): bloquea las pestañas en suspensión en sitios específicos.
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled): habilita el inicio rápido.
- [TargetBlankImpliesNoOpener:](./microsoft-edge-policies.md#targetblankimpliesnoopener) evita establecer window.opener para vínculos destinados a _blank.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride): especifica cómo Microsoft Edge Update controla las actualizaciones disponibles de Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed): configura la disponibilidad de un diseño vertical para pestañas en el lateral del explorador.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols): permite la degradación de TLS/DTLS heredada en WebRTC.
- [WebWidgetAllowed](./microsoft-edge-policies.md#webwidgetallowed): habilita el widget Web.
- [WebWidgetIsEnabledOnStartup](./microsoft-edge-policies.md#webwidgetisenabledonstartup): permite el widget web en el inicio de Windows.

#### <a name="deprecated-policies"></a>Directivas obsoletas

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled): habilita la autenticación proactiva.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist): configura las reglas de omisión de proxy.
- [ProxyMode](./microsoft-edge-policies.md#proxymode): configura la configuración del servidor proxy.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl): establece la dirección URL del archivo proxy .pac.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver): configura la dirección o URL del servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies): permite que WebDriver reemplace las directivas incompatibles.

### <a name="obsoleted-policies"></a>Directivas obsoletas

- [AllowPopupsDuringPageUnload:](./microsoft-edge-policies.md#allowpopupsduringpageunload) permite que una página muestre elementos emergentes durante su descarga.
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting): configuración predeterminada de Adobe Flash.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls): permite el complemento Adobe Flash en sitios específicos.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls): bloquea el complemento Adobe Flash en sitios específicos.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode): amplía la configuración de contenido de Adobe Flash a todo el contenido.
<!--- end major 88  --->
## <a name="version-87066475-january-7"></a>Versión 87.0.664.75: 7 de enero

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#january-7-2021).

## <a name="version-87066466-december-17"></a>Versión 87.0.664.66: 17 de diciembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066460-december-10"></a>Version 87.0.664.60: 10 de diciembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066457-december-7"></a>Versión 87.0.664.57: 7 de diciembre

Se han corregido varios errores y problemas de rendimiento. Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#december-7-2020).

## <a name="version-87066455-december-3"></a>Versión 87.0.664.55: 3 de diciembre

Se han corregido varios errores y problemas de rendimiento. La siguiente característica se actualizó para esta versión.

- La **opción compras está habilitada de forma predeterminada**. A partir de la versión 87 de Microsoft Edge, los usuarios empresariales pueden beneficiarse de la compra en Microsoft Edge. Con las características de compra, Microsoft Edge ayuda a los usuarios a buscar cupones y mejores precios mientras compras en Internet. (La experiencia del cupón se presentó con la versión estable de 87.0.664.41). La experiencia de comparación de precios ahora está disponible con esta actualización. Esta característica se puede configurar con la directiva [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled). Consulte nuestro [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) y [Obtenga más información](/microsoft-edge/privacy-whitepaper#shopping) sobre Compras de Microsoft.

## <a name="version-87066452-november-30"></a>Versión 87.0.664.52: 30 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066447-november-23"></a>Versión 87.0.664.47: 23 de noviembre

Se han corregido varios errores y problemas de rendimiento.

<!-- begin major 87 --->
## <a name="version-87066441-november-19"></a>Versión 87.0.664.41: 19 de noviembre

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#november-19-2020).

### <a name="feature-updates"></a>Actualizaciones de características

- **Redireccionamiento automático para sitios incompatibles de Internet Explorer a Microsoft Edge**. A partir de la actualización estable de Microsoft Edge 87, los sitios web públicos que muestren un mensaje de incompatibilidad en Internet Explorer se redirigirán automáticamente a Microsoft Edge de forma predeterminada. Para más información y configurar esta experiencia, vea [Redirigir sitios incompatibles](./edge-learnmore-neededge.md).

- **Las características de privacidad del modo de pantalla completa están habilitadas**. A partir de la versión 87 de Microsoft Edge, se habilitarán las características del modo de pantalla completa que puedan ayudar a las empresas relacionadas a mantener la privacidad de los datos del usuario. Estas características permiten habilitar experiencias como borrar los datos del usuario al salir, eliminar los archivos descargados y restablecer la experiencia de inicio configurada después de un período de inactividad especificado. Más información sobre cómo [Configurar el modo de pantalla completa de Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md)

- **Características de la compra habilitadas de forma predeterminada**. A partir de la versión 87 de Microsoft Edge, los usuarios empresariales también pueden beneficiarse de las compras en Edge. Con las características de compra, Microsoft Edge ayuda a los usuarios a buscar cupones y mejores precios mientras compran en línea. La experiencia de cupones está disponible con esta actualización y la comparación de precios se publicará en próximas actualizaciones de Microsoft Edge 87. Esta característica se puede configurar mediante la directiva [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled). Consulte nuestro [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) y [Obtenga más información](/microsoft-edge/privacy-whitepaper#shopping) sobre Compras de Microsoft.

- **Implementación de ClickOnce habilitada de manera predeterminada**. ClickOnce está habilitado de manera predeterminada en Microsoft Edge 87, lo cual reduce las barreras para que las empresas puedan implementar software y alinearse mejor con el comportamiento del explorador Microsoft Edge (versión anterior). A partir de Microsoft Edge 87, el estado "No se configuró" de la directiva ClickOnceEnabled reflejará el nuevo estado predeterminado de ClickOnce Habilitado (en comparación con el estado predeterminado anterior de Deshabilitado).

- **La página de pestaña nueva (NTP) de la empresa ahora integra la productividad al ofrecer un contenido de fuente que se puede personalizar y es relevante para el trabajo**. La NTP de la empresa combina la página de productividad de Office 365 que ofrecemos a los usuarios que hayan iniciado sesión con su cuenta profesional o educativa con fuentes personalizadas relevantes para el trabajo y el sector, que ahora están organizadas en una sola página. Los usuarios reconocerán el contenido de Office 365 con el que están familiarizados, así como la Búsqueda de Microsoft para la Empresa con tecnología de Bing. Además, pueden personalizar "Mi fuente" fácilmente eligiendo el contenido más relevante para ellos entre el contenido y los módulos disponibles para su organización. Los administradores de sistemas de información pueden controlar la configuración de la fuente de Noticias de su organización, incluido el sector seleccionado en la página de la nueva pestaña de Microsoft Edge desde el Centro de administración de Microsoft 365. [Más información](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Privacidad y seguridad:**

  - Enlace del token TLS de soporte para sitios configurados con directiva. El enlace del token TLS ayuda a evitar ataques de intento de robo del token y garantiza que las cookies no puedan volver a usarse desde un dispositivo distinto de aquel desde el que se establecieron inicialmente. El uso de un enlace de token TLS requiere establecer la directiva de [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) y requiere que los sitios que aparecen en la lista sean compatibles con esta característica.

- **Compatibilidad del teclado con el marcador de resaltado en archivos PDF**. Los usuarios pueden usar las teclas del teclado para resaltar cualquier texto en un archivo PDF.

- **Impresión:**

  - Elija el lado por el cual quiere que se voltee la página al imprimir en ambas caras. Los usuarios pueden optar por voltear la página por el lado largo o por el lado corto de la hoja al imprimir en ambas caras.
  - Elija el modo imprimir rasterización para la empresa. Controle la forma en que Microsoft Edge imprime en una impresora que no sea PostScript en Windows. En ocasiones, es necesario rasterizar los trabajos de impresión de impresoras que no sean PostScript para que se impriman correctamente. Las opciones de impresión son "Completa" y "Rápida".

### <a name="policy-updates"></a>Actualizaciones de directivas

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado diez directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se han agregado las siguientes directivas nuevas.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat): configura el formato de pegado predeterminado de las direcciones URL copiadas desde Microsoft Edge y determina si los formatos adicionales estarán disponibles para los usuarios.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled): Compras de Microsoft Edge está habilitado.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled): oculta el cuadro de diálogo de redirección que aparece una sola vez y el banner en Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled): Configura la edición de la barra de direcciones para la experiencia de navegación pública en modo de pantalla completa.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit): elimina los archivos descargados como parte de la sesión de pantalla completa al cerrar Microsoft Edge.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled): habilita el botón Mostrar contraseña.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall): evita la instalación del objeto auxiliar de explorador (BHO) para redirigir los sitios incompatibles desde Internet Explorer a Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode): redirige los sitios incompatibles desde Internet Explorer a Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled): configura el reconocimiento de voz.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled): habilita la característica de captura web en Microsoft Edge.

#### <a name="deprecated-policy"></a>Directivas en desuso

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype): Configura la experiencia de la página de pestaña nueva de Microsoft Edge.

#### <a name="obsoleted-policy"></a>Directiva obsoleta

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures): vuelve a habilitar las características de la plataforma web en desuso por un tiempo limitado.

<!-- end major 87 -->

## <a name="version-86062269-november-13"></a>Versión 86.0.622.69: 13 de noviembre

> [!IMPORTANT]
> Esta actualización contiene [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) y [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), que han sido reportados por el equipo de Chromium como una vulnerabilidad de seguridad.

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#november-13-2020).

## <a name="version-86062268-november-11"></a>Versión 86.0.622.68: 11 de noviembre

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#november-11-2020).

## <a name="version-86062263-november-4"></a>Versión 86.0.622.63: 4 de noviembre

> [!IMPORTANT]
> Esta actualización contiene [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), que ha sido reportado por el equipo de Chromium como una vulnerabilidad de seguridad.

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#november-4-2020).

## <a name="version-86062261-november-2"></a>Versión 86.0.622.61: 2 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-86062258-october-29"></a>Versión 86.0.622.58: 29 de octubre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-86062256-october-27"></a>Versión 86.0.622.56: 27 de octubre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-86062251-october-22"></a>Versión 86.0.622.51: 22 de octubre

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#october-22-2020).

## <a name="version-86062248-october-20"></a>Versión 86.0.622.48: 20 de octubre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-86062243-october-15"></a>Versión 86.0.622.43: 15 de octubre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-86062238-october-9"></a>Versión 86.0.622.38: 9 de octubre

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#october-9-2020)

### <a name="feature-updates"></a>Actualizaciones de características

* **Volver a la versión anterior de Microsoft Edge.** La característica de restauración permite a los administradores volver a una versión en buen estado y conocida de Microsoft Edge si hay algún problema en la versión más reciente de Microsoft Edge. **Nota:** versión estable 86.0.622.38 es la primera versión a la que se puede revertir, lo que significa que la versión estable 87 es la primera versión preparada para la reversión. [Más información](edge-learnmore-rollback.md).

* **Ejecutar la habilitación de Sincronización de forma predeterminada en toda la empresa.**  Los administradores pueden habilitar la sincronización para cuentas de Azure Active Directory (Azure AD) de forma predeterminada con la directiva [ForceSync](./microsoft-edge-policies.md#forcesync).

* **Cambio de perfil automático en Windows 7 y 8.1.** El cambio de perfil automático que se encuentra disponible actualmente en Microsoft Edge en Windows 10 ha sido extendido a otros Windows de nivel inferior (Windows 7 y 8.1). Para obtener más información, consulte la publicación en el blog [cambio de perfil automático](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Cookies con SameSite=Lax de manera predeterminada**. Para mejorar la seguridad y la privacidad Web, las cookies usarán ahora [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) de manera predeterminada. Esto significa que las cookies se enviarán solo como cookies de origen y se omitirán para las solicitudes que se envíen a terceros. Este cambio puede provocar un impacto en la compatibilidad en aquellos sitios web que necesitan cookies para recursos de terceros para funcionar correctamente. Para permitir el envío de cookies, los desarrolladores web pueden marcar cookies que deberían establecerse y recibirse en contextos de terceros agregando atributos `SameSite=none` y `Secure` explícitos al establecer la cookie. Las empresas que quieran excluir determinados sitios de este cambio pueden usar la directiva [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) y las que quieran que ningún sitio sufra el cambio, pueden valerse de la directiva [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled).

* **Quitar la API de caché de aplicaciones HTML5.**  A partir de la versión 86 de Microsoft Edge, la API de caché de aplicaciones heredada que permite el uso sin conexión de páginas web se quita de Microsoft Edge. Los desarrolladores web deben revisar la documentación [WebDev](https://web.dev/appcache-removal/) para obtener información sobre cómo reemplazar la API de caché de aplicaciones con trabajos de servicio.  Importante: Puede solicitar un [token de AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) que permite a los sitios seguir usando la API de caché de aplicaciones obsoleta hasta la versión 90 de Microsoft Edge.

* **Privacidad y seguridad:**

  * Reemplazar las directivas [MetricsReportingEnabled](/DeployEdge/microsoft-edge-policies#metricsreportingenabled) y [SendSiteInformationToImproveServices](/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) para las versiones anteriores de Windows y macOS. Estas directivas están en desuso en la versión 86 de Microsoft Edge y quedarán obsoletas en Microsoft Edge versión 89.<br>
Estas directivas se reemplazarán por [Permitir telemetría](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) en Windows 10 y la nueva directiva [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) para las demás plataformas. Esto permitirá que los usuarios administren los datos de diagnóstico que se envían a Microsoft para Windows 7, 8, 8.1 y macOS.
  * Soporte de DNS seguro (DNS a través de HTTPS).  A partir de la versión 86 de Microsoft Edge, está disponible la configuración para controlar el DNS seguro en los dispositivos no administrados. Estas opciones de configuración no son accesibles para los usuarios de dispositivos administrados, pero los administradores de TI pueden habilitar o deshabilitar el DNS seguro con la directiva de grupo [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode).

* **modo de Internet Explorer:** permitir que los usuarios usen la interfaz de usuario (UI) de Microsoft Edge para probar los sitios en el modo de Internet Explorer. A partir de la versión 86 de Microsoft Edge, los administradores pueden habilitar la opción de interfaz de usuario para cargar una pestaña en el modo de Internet Explorer con propósitos de prueba o como medida provisional, hasta que los sitios se agreguen al XML de la lista de sitios.

* **Actualizaciones para PDF:**

  * Tabla de contenido para documentos PDF. A partir de la versión 86, Microsoft Edge ha agregado soporte con la tabla de contenidos, que permite a los usuarios desplazarse de manera sencilla por los documentos PDF.
  * Acceso a todas las funciones PDF en pantallas pequeñas. Obtenga acceso a todas las funciones del lector de PDF para Microsoft Edge en los dispositivos con tamaños de pantalla reducidos.
  * Compatibilidad con el lápiz para resaltar en archivos PDF. Con esta actualización, los usuarios pueden usar el lápiz digital para resaltar texto directamente en archivos PDF, de la misma forma que lo harían con un subrayador o resaltador y una hoja en físico.
  * Se ha mejorado el desplazamiento de PDF. Ahora podrá experimentar un desplazamiento sin interrupciones mientras navega por documentos largos en PDF.

* **Los usuarios verán sugerencias de autocompletar al empezar a escribir una consulta de búsqueda en el sitio web de complementos de Microsoft Edge.** Autocompletar ayudará a los usuarios a realizar de manera rápida sus búsquedas sin tener que escribir el nombre completo del elemento que estén buscando. Esto puede ser útil, ya que los usuarios no tendrán que recordar la escritura correcta y podrán elegir entre las opciones disponibles que se muestran.

* **Agregar una imagen personalizada a la página de nueva pestaña (NTP) con una directiva de grupo.** A partir de la versión 86 de Microsoft Edge, la NTP tiene la opción de reemplazar la imagen predeterminada por una imagen personalizada proporcionada por el usuario. La directiva de grupo admite también la capacidad para administrar las propiedades de esta imagen.

* **Hacer coincidir los métodos abreviados de teclado personalizados con el VS Code.** Ahora las DevTools de Microsoft Edge permiten personalizar los métodos abreviados de teclado en las DevTools para que coincidan con su editor/IDE. (En Microsoft Edge 84, agregamos la capacidad de hacer coincidir los métodos abreviados del teclado de las DevTools con el VS Code).

* **Elimine las descargas en el disco con el administrador de descargas.** Ahora los usuarios pueden eliminar los archivos descargados en su disco sin salir del explorador. La nueva funcionalidad Eliminar descargas se encuentra en el menú emergente del estante de descargas o de la página de descargas.

### <a name="policy-updates"></a>Actualizaciones de directiva

#### <a name="new-policies"></a>Nuevas directivas

Ha sido agregado veinticuatro directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist): Bloquear el acceso a una lista especificada de servicios y destinos de exportación en Colecciones.
- [DefaultFileSystemReadGuardSetting](./microsoft-edge-policies.md#defaultfilesystemreadguardsetting) controle el uso de la API del sistema de archivos para su lectura.
- [DefaultFileSystemWriteGuardSetting](./microsoft-edge-policies.md#defaultfilesystemwriteguardsetting) controle el uso de la API del sistema de archivos para su escritura.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting): Configuración predeterminada de sensores.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting): Controlar el uso de la API de serie.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata): enviar datos de diagnóstico necesarios y opcionales sobre el uso del explorador.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed): Permitir el acceso a la herramienta Enterprise Mode Site List Manager
- [FileSystemReadAskForUrls](./microsoft-edge-policies.md#filesystemreadaskforurls): permitir el acceso de lectura a través de la API del sistema de archivos en estos sitios.
- [FileSystemReadBlockedForUrls](./microsoft-edge-policies.md#filesystemreadblockedforurls) -bloquear el acceso de lectura a través de la API del sistema de archivos en estos sitios.
- [FileSystemWriteAskForUrls](./microsoft-edge-policies.md#filesystemwriteaskforurls) : permitir el acceso de escritura a los archivos y directorios en estos sitios.
- [FileSystemWriteBlockedForUrls](./microsoft-edge-policies.md#filesystemwriteblockedforurls) : bloquear el acceso de escritura a los archivos y directorios en estos sitios.
- [ForceSync](./microsoft-edge-policies.md#forcesync): Forzar la sincronización de los datos del explorador y no mostrar la solicitud de consentimiento de sincronización.
- [InsecureFormsWarningsEnabled](./microsoft-edge-policies.md#insecureformswarningsenabled) : Habilitar advertencias para formularios no seguros.
- [InternetExplorerIntegrationTestingAllowed](./microsoft-edge-policies.md#internetexplorerintegrationtestingallowed): Permitir probar el modo de Internet Explorer.
- [SpotlightExperiencesAndRecommendationsEnabled](./microsoft-edge-policies.md#spotlightexperiencesandrecommendationsenabled): Decidir si los usuarios pueden recibir imágenes de fondo y texto personalizados, sugerencias, notificaciones y recomendaciones para los servicios de Microsoft.
- [NewTabPageAllowedBackgroundTypes](./microsoft-edge-policies.md#newtabpageallowedbackgroundtypes): Configurar los tipos de fondo permitidos para el diseño de página de nueva pestaña.
- [SaveCookiesOnExit](./microsoft-edge-policies.md#savecookiesonexit): Guardar cookies cuando se cierra Microsoft Edge.
- [SensorsAllowedForUrls](./microsoft-edge-policies.md#sensorsallowedforurls): Permitir el acceso a sensores en sitios específicos.
- [SensorsBlockedForUrls](./microsoft-edge-policies.md#sensorsblockedforurls): Bloquear el acceso a sensores en sitios específicos.
- [SerialAskForUrls](./microsoft-edge-policies.md#serialaskforurls): Permitir la API de serie en sitios específicos.
- [SerialBlockedForUrls](./microsoft-edge-policies.md#serialblockedforurls): Bloquear la API de serie en sitios específicos.
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled): Habilitar la característica User-Agent Client Hints (en desuso).
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit): Limitar el número de instantáneas de datos de usuario que se conservan para su uso en caso de reversión de emergencia.

#### <a name="deprecated-policies"></a>Directivas obsoletas

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled): habilitar el uso y los informes de datos relacionados con bloqueos.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices): enviar información de sitios para mejorar los servicios Microsoft.

#### <a name="obsoleted-policy"></a>Directiva obsoleta

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled): habilitar una característica de seguridad TLS 1.3 para anclajes de veracidad locales.

## <a name="version-85056470-october-6"></a>Versión 85.0.564.70: 6 de octubre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-85056468-october-1"></a>Versión 85.0.564.68: 1 de octubre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-85056463-september-23"></a>Versión 85.0.564.63: 23 de septiembre

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#september-23-2020)

## <a name="version-85056451-september-9"></a>Versión 85.0.564.51: 9 de septiembre

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#september-9-2020)

## <a name="version-85056444-august-31"></a>Versión 85.0.564.44: 31 de agosto

Se han corregido varios errores y problemas de rendimiento.

<!-- 85.0.564.41: August 27 -->

## <a name="version-85056441-august-27"></a>Versión 85.0.564.41: 27 de agosto

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#august-27-2020)

### <a name="feature-updates"></a>Actualizaciones de características

- **Sincronización local de los Favoritos y las Configuraciones**. Ahora puede sincronizar los favoritos y la configuración del explorador entre los perfiles de Active Directory dentro de su propio entorno sin necesidad de sincronización en la nube.

- **Soporte de la directiva del grupo de Microsoft Edge para los sitios confiables y combinaciones de aplicaciones para iniciar sin aviso de confirmación.** El soporte añadido a la directiva del grupo permite a los administradores agregar combinaciones de sitios y aplicaciones de confianza para iniciar sin el aviso de confirmación. Esto agrega la capacidad de que los administradores configuren las combinaciones de protocolo de confianza/origen (como las aplicaciones de Microsoft 365) para que sus usuarios finales puedan suprimir el aviso de confirmación al navegar en una dirección URL que contenga un protocolo de aplicación.

- **Herramienta de resaltado para PDF**. Se puede agregar esta herramienta a la barra de herramientas para poder resaltar fácilmente el texto importante en los archivos PDF.

- **La API de acceso al almacenamiento está disponible**. Esta API permite acceder al almacenamiento de origen en un contexto de terceros en el que un usuario proporcione una forma directa para permitir el almacenamiento que, de otro modo, quedaría bloqueado por la configuración actual del explorador. Para obtener más información, consulte [API de acceso al almacenamiento](https://www.chromestatus.com/feature/5612590694662144).

- **El envío a OneNote está disponible para las Colecciones de Microsoft Edge**. Los usuarios están complacidos de poder enviar la información que hayan reunido en las Colecciones a OneNote, en donde pueden anexarla a un proyecto mayor y colaborar con otras personas. Y lo que es más importante, en Microsoft Edge 85, podrá enviar contenido a los productos de *Office para Mac* (Word, Excel y OneNote), tanto en la cuenta de Microsoft como en Azure Active Directory.

- **Actualizaciones de DevTools** Para obtener más información sobre las siguientes actualizaciones, consulte las [Novedades en DevTools (Microsoft Edge 85)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - Microsoft Edge DevTools admite la emulación de Surface Duo. Las DevTools de Microsoft Edge pueden emular Surface Duo para que pueda probar el aspecto que tendrá el contenido web en los dispositivos de pantalla doble. Para activar este experimento en DevTools, ingrese al Modo de dispositivo presionando Ctrl+Mayús+M en Windows o Comando+Mayús+M en macOS y seleccionando, a continuación, Surface Duo en la lista desplegable del dispositivo.
   - Microsoft Edge DevTools le permite hacer coincidir los métodos abreviados de teclado con el VS Code. Las DevTools de Microsoft Edge permiten personalizar los métodos abreviados de teclado en las DevTools para que coincidan con su editor/IDE. En Microsoft Edge 85, estamos agregando la capacidad de hacer coincidir los métodos abreviados del teclado de las DevTools con el VS Code. Este cambio ayudará a aumentar la productividad en VS Code y DevTools.

### <a name="policy-updates"></a>Actualizaciones de directivas

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado trece directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AutoLaunchProtocolsFromOrigins](./microsoft-edge-policies.md#autolaunchprotocolsfromorigins): definir una lista de protocolos que puedan iniciar una aplicación externa desde los orígenes listados sin avisar al usuario.
- [AutoOpenAllowedForURLs](./microsoft-edge-policies.md#autoopenallowedforurls): URL en donde AutoOpenFileTypes aplique.
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes): lista los tipos de archivo que se abrirán automáticamente al descargarse.
- [DefaultSearchProviderContextMenuAccessAllowed](./microsoft-edge-policies.md#defaultsearchprovidercontextmenuaccessallowed): permitir el acceso a la búsqueda del menú emergente del proveedor de búsquedas predeterminado.
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors): permitir certificados firmados usando SHA-1 cuando sean emitidos por anclajes de veracidad locales.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings): deshabilitar las advertencias basadas en la extensión del tipo de archivo de descarga para tipos de archivo especificados en los dominios.
- [IntensiveWakeUpThrottlingEnabled](./microsoft-edge-policies.md#intensivewakeupthrottlingenabled): controlar la característica IntensiveWakeUpThrottling.
- [NewTabPagePrerenderEnabled](./microsoft-edge-policies.md#newtabpageprerenderenabled): habilitar la carga previa de la nueva pestaña de la página para una representación más rápida.
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox): configurar la experiencia del cuadro de búsqueda de la nueva pestaña de la página.
- [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed): permitir que se alerte a los usuarios si se detecta que sus contraseñas no son seguras.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): habilitar el uso de copias itinerantes para los datos del perfil de Microsoft Edge.
- [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation): establecer el directorio del perfil móvil.
- [TLSCsipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist): especificar los conjuntos de cifrado TLS para deshabilitarlos.

#### <a name="obsoleted-policies"></a>Directivas obsoletas

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload): habilitar la descarga de las acciones del dominio desde Microsoft.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled): volver a habilitar la API de componentes web v0 hasta M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies): permitir al controlador web invalidar las directivas obsoletas.

## <a name="version-84052263-august-20"></a>Versión 84.0.522.63: 20 de agosto

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#august-20-2020).

## <a name="version-84052261-august-17"></a>Versión 84.0.522.61: 17 de agosto

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-84052259-august-11"></a>Versión 84.0.522.59: 11 de agosto

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#august-11-2020)

## <a name="version-84052258-august-10"></a>Versión 84.0.522.58: 10 de agosto

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-84052252-august-1"></a>Versión 84.0.522.52: 1 de agosto

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-84052250-july-31"></a>Versión 84.0.522.50: 31 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-84052249-july-29"></a>Versión 84.0.522.49: 29 de julio

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#july-29-2020)

## <a name="version-84052248-july-28"></a>Versión 84.0.522.48: 28 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-84052244-july-23"></a>Versión 84.0.522.44: 23 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-84052240-july-16"></a>Versión 84.0.522.40: 16 de julio

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#july-16-2020)

### <a name="feature-updates"></a>Actualizaciones de características

- Esta versión de Microsoft Edge proporciona tiempos mejorados de descarga de la lista de sitios en el modo Internet Explorer. Hemos reducido el tiempo de retraso de la descarga de la lista de sitios en modo Internet Explorer de 60 segundos a 0 segundos, en ausencia de una lista de sitios en caché. También hemos agregado compatibilidad con la directiva de grupo para casos en los que es necesario retrasar la navegación de la página principal en modo Internet Explorer hasta que finaliza la descarga de la lista de sitios. Para más información, consulte la directiva [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload).

- Microsoft Edge permite ahora a los usuarios iniciar sesión en el explorador cuando se "ejecuta como administrador" en Windows 10. Esto ayudará a los clientes que ejecuten Microsoft Edge en Windows server o en escenarios de escritorio remoto y de espacio aislado.

- Microsoft Edge ofrece ahora compatibilidad total con el mouse en el modo de pantalla completa. Ahora puede usar el mouse para acceder a las pestañas, la barra de direcciones y otros elementos sin tener que salir del modo de pantalla completa.

- Mejoras en la compra online. Agregue alias personalizados a la tarjeta de crédito o débito guardada. Ahora podrá distinguir y diferenciar las tarjetas de crédito cuando realice compras en línea. Escribir un alias para las tarjetas de crédito o débito le facilitará elegir la tarjeta adecuada al usar la opción de Autorrellenar para seleccionar un método de pago.

- De forma predeterminada, se deshabilitan TLS/1.0 y TLS/1.1.  La directiva [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) permite volver a habilitar TLS/1.0 y TLS/1.1. Esta directiva estará disponible como mínimo hasta la versión 88 de Microsoft Edge. Para más información, consulte [Cambios que se van a producir en Microsoft Edge que afectan a la compatibilidad de los sitios](/microsoft-edge/web-platform/site-impacting-changes).

- Mejoras en las colecciones:

  - Se ha agregado una funcionalidad de notas que le permite añadir una nota o comentario a un elemento de una colección. Las notas se agrupan y se mantienen adjuntadas a un elemento incluso si se ordenan los elementos de una colección. Para probar esta característica nueva, haga clic con el botón derecho en un elemento y seleccione "Agregar nota".
  - Puede cambiar el color de fondo de las notas en las colecciones. Puede usar la codificación por colores para ayudarle a organizar información y a incrementar la productividad.
  - Se han realizado mejoras notables en el rendimiento que le permiten exportar las colecciones a Excel en un tiempo menor que en las versiones anteriores de Microsoft Edge.

- Compatibilidad adicional con la API de Microsoft Edge:

  - La API de acceso de almacenamiento está habilitada para experimentación. Esta característica está habilitada para usuarios domésticos y usuarios de empresa con la directiva [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) establecida en "Completo". De forma predeterminada, esta característica estará habilitada para todos los usuarios de la versión 85 de canal estable de Microsoft Edge.
  
    Dado que la privacidad es cada vez más importante para los usuarios, van en aumento las solicitudes de configuraciones opcionales de usuario y de valores predeterminados del explorador más estrictos, como el bloqueo de todos los accesos al almacenamiento de terceros. Si bien estas configuraciones contribuyen a mejorar la privacidad y a bloquear los accesos no deseados de partes desconocidas o que no son de confianza, pueden tener consecuencias no deseadas, como el bloqueo del acceso a contenido que el usuario podría querer ver (por ejemplo, contenido de redes sociales y contenido multimedia incrustado).

    Esta API permite acceder al almacenamiento de origen en un contexto de terceros en el que un usuario proporcione una forma directa para permitir el almacenamiento que, de otro modo, quedaría bloqueado por la configuración actual del explorador. Para obtener más información, consulte [API de acceso al almacenamiento](https://www.chromestatus.com/feature/5612590694662144).

  - La API del sistema de archivos nativo quiere decir que usted puede conceder permisos a los sitios para editar archivos o carpetas mediante la API del sistema de archivos nativo.

- Mejoras de PDF:

  - Leer en voz alta para PDF permite a los usuarios escuchar contenido PDF mientras llevan a cabo otras tareas que pueden ser importantes. Además, ayuda a las personas que reciben educación audiovisual a centrarse en la lectura del contenido, lo que facilita el aprendizaje.
  - Se ha mejorado la edición de archivos PDF. Ahora puede guardar en el mismo archivo las modificaciones realizadas a un archivo PDF, en lugar de tener que guardar una copia cada vez que edita un PDF.

- Microsoft Edge permite ahora traducir en el Lector inmersivo. Cuando un usuario abre la vista de Lector inmersivo, obtiene la opción de traducir la página al idioma que desee.

- Varias actualizaciones de DevTools, como la compatibilidad con la personalización de los métodos abreviados de teclado para que coincidan con los de VS Code, y la visualización de DevTools en contraste alto.  Para obtener más información, consulte [Novedades en DevTools (Microsoft Edge 84)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### <a name="policy-updates"></a>Actualizaciones de directiva

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado siete directivas nuevas. Descargue las Plantillas administrativas actualizadas desde la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled): permite volver a habilitar la característica AppCache, incluso si está desactivada de forma predeterminada.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy): configurar las opciones del contenedor proxy de Protección de aplicaciones.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload): Requerir que la lista de sitios modo empresarial esté disponible antes que la navegación por la tabulación.
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled): utilizar el solucionador de proxy de Windows.
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection): configurar la detección de bloqueos mejorada para el modo de Internet Explorer.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Para disminuir el consumo de energía y de la CPU, Microsoft Edge detectará cuándo una ventana está cubierta por otra ventana y suspenderá el trabajo pintando píxeles.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout): Establecer un tiempo de espera de retardo en la navegación mediante tabulación para la lista de sitios de modo empresarial.

#### <a name="deprecated-policies"></a>Directivas obsoletas

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal): Permitir que las páginas envíen solicitudes sincrónicas de XHR durante el descarte de página.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled): determina si el comprobador de certificados integrado se usará para comprobar certificados de servidor.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled): habilitar el tratamiento más estricto para contenido mixto.

#### <a name="obsoleted-policy"></a>Directiva obsoleta

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess): Forzar el código de red para que se ejecute en el proceso del explorador.

<!-- End 84 -->
## <a name="version-83047864-july-13"></a>Versión 83.0.478.64: 13 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-83047861-july-7"></a>Versión 83.0.478.61: 7 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-83047858-june-30"></a>Versión 83.0.478.58: 30 de junio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-83047856-june-24"></a>Versión 83.0.478.56: 24 de junio

Se han corregido varios errores y problemas de rendimiento.

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#june-24-2020)

## <a name="version-83047854-june-17"></a>Versión 83.0.478.54: 17 de junio

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#june-17-2020)

## <a name="version-83047850-june-15"></a>Versión 83.0.478.50: 15 de junio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-83047845-june-4"></a>Versión 83.0.478.45: 4 de junio

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#june-4-2020)

## <a name="version-83047844-june-1"></a>Versión 83.0.478.44: 1 de junio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-83047837-may-21"></a>Versión 83.0.478.37: 21 de mayo

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#may-21-2020)

### <a name="feature-updates"></a>Actualizaciones de características

- Las actualizaciones de Microsoft Edge ahora se implementarán gradualmente. En el futuro, las actualizaciones de Microsoft Edge se implementarán para nuestros usuarios en un período de unos días. Esto nos permite proteger a más usuarios de actualizaciones con errores accidentales, lo que mejora la experiencia de actualización. Como usuario, seguirá obteniendo actualizaciones automáticas sin problemas. Si su organización no se inscribe para las actualizaciones automáticas, no le afectará este cambio. Para obtener más información, consulte el artículo sobre implementaciones progresivas [Progressive rollouts for Microsoft Edge Stable channel updates (Implementaciones progresivas de actualizaciones de canal estables de Microsoft Edge)](microsoft-edge-update-progressive-rollout.md).
- Mejoras de SmartScreen de Microsoft Defender: se han realizado varias mejoras en el servicio de SmartScreen de Microsoft Defender, como la protección mejorada frente a sitios malintencionados que redirigen al cargar, y el bloqueo de marco de nivel superior que reemplaza completamente sitios malintencionados con la página de seguridad de SmartScreen de Microsoft Defender. El bloqueo del marco de nivel superior impide que el audio y otros elementos multimedia del sitio malintencionado se reproduzcan, lo que ofrece una experiencia más fácil y menos confusa.

- En respuesta a los comentarios de los usuarios, ahora se pueden eximir algunas cookies del borrado automático cuando se cierre el explorador. Esta opción es útil si hay un sitio en el que los usuarios no quieren cerrar la sesión, pero quieren que todas las demás cookies se eliminen cuando se cierre el explorador. Para usar esta característica, ve a *edge://settings/clearBrowsingDataOnClose* y habilita el interruptor "Cookies y otros datos de sitio".

- El cambio de perfil automático ya está disponible para ayudarte a obtener el contenido del trabajo más fácilmente entre perfiles. Si usas varios perfiles en el trabajo, puedes probarlo en un sitio que requiera autenticación de tu cuenta profesional o educativa mientras estás en tu perfil personal. Cuando se detecta esto, se te pedirá que cambies a su perfil de trabajo para tener acceso a ese sitio sin tener que autenticarte. Cuando elijas el perfil de trabajo al que quieres cambiar, el sitio web simplemente se abrirá en tu perfil de trabajo. Esta función de cambio de perfil te ayudará a mantener tus datos personales y de trabajo separados y a obtener el contenido de trabajo con mayor esfuerzo. Si no quieres que la característica te solicite cambiar perfiles, puedes elegir la opción no volver a preguntar y se quitará.

- Mejoras de la característica de Colecciones:
  - Puedes usar arrastrar y soltar para agregar un elemento a una colección sin abrir la colección. Durante el proceso de arrastrar y soltar también puedes elegir una ubicación en la lista de colecciones en la que quieras colocar el elemento.
  - Puedes agregar varios elementos a una colección en lugar de agregar un elemento a la vez. Para agregar varios elementos, selecciona los elementos y arrástralos hasta una colección. También puedes seleccionarlos, hacer clic con el botón derecho y elegir la colección en la que quieres que aparezcan los elementos.

- Puedes agregar todas las pestañas de una ventana de Microsoft Edge a una colección nueva sin agregarlas individualmente. Para ello, haz clic con el botón derecho en cualquier pestaña y elige "Agregar todas las pestañas a una nueva colección".

- La sincronización de extensiones ya está disponible. Ahora, puedes sincronizar tus extensiones de en todos tus dispositivos. Las extensiones de las tiendas de Microsoft y Chrome se sincronizarán con Microsoft Edge. Para usar esta característica: haz clic en el signo de puntos suspensivos (**...**) en la barra de menús, selecciona **Configuración**. En Tu perfil, haz clic en **Sincronización** para ver las opciones de sincronización. En **Perfiles / Sincronizar** usa el botón de alternancia para habilitar Extensiones. Puedes usar la directiva de grupo [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) para deshabilitar la sincronización de extensiones.

- Se ha mejorado el mensaje en la página de Administración de descargas para las descargas no seguras que se han bloqueado.

- Mejoras en el Lector inmersivo:
  - Se ha agregado soporte para Adverbios en la experiencia de Elementos de la oración que tenemos en el Lector inmersivo. Mientras lee un artículo en el Lector inmersivo, abra las Herramientas gramaticales y active los Adverbios en las Elementos de la oración para resaltar todos los adverbios de la página.
  - Se ha agregado la posibilidad de seleccionar cualquier contenido de una página web y abrirla en el Lector inmersivo. Esta capacidad permite a los usuarios utilizar el Lector inmersivo y todas las herramientas de aprendizaje, como Foco de línea y Lectura en voz alta, en todos los sitios web.

- Link doctor proporciona correcciones de host y una consulta de búsqueda a los usuarios cuando escriben errores en una dirección URL. Por ejemplo: <br>
Un usuario escribe "powerbi" como "powerbbi".com. Link doctor propondrá "powerbi".com como corrección y creará un vínculo para buscar "powerbbi" en caso de que el usuario busque algo diferente.

- Permitir que los usuarios guarden su decisión de lanzar un protocolo externo para un sitio específico. Los usuarios pueden configurar la directiva [ExternalProtocolDialogShowAlwaysOpenCheckbox](/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) para habilitar o deshabilitar esta característica.

- Los usuarios pueden establecer Microsoft Edge como su explorador predeterminado directamente desde la **Configuración** de Microsoft Edge. Esto hace que sea más fácil para los usuarios cambiar el explorador predeterminado, dentro del contexto del explorador, en lugar de tener que buscar en la configuración del sistema operativo. Para usar esta característica, ve a *edge://settings/defaultBrowser* y haz clic en **Establecer como predeterminado**.

- Varias actualizaciones de DevTools, incluido el nuevo soporte de depuración remota, mejoras en la interfaz de usuario y más. Para más información, consulta [Novedades en DevTools (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- El escenario de advertencia MCAS (seguridad de acceso a la nube de Microsoft). Esto permite que los administradores configuren advertir, una nueva categoría de bloqueos de MCAS que permite al usuario invalidar una página de bloqueo de MCAS. Los bloqueos MDATP E5 están integrados de forma nativa en los bloqueos de SmartScreen para ofrecer una experiencia perfecta. Esta experiencia permite la apariencia de un bloqueo en rojo de página completa con el mensaje "Su organización ha bloqueado este sitio web", en lugar de solo una notificación del sistema.

- No permitir XmlHttpRequest sincrónico en el descarte de página. Se eliminará el envío de XmlHttpRequests sincrónicos durante la carga de una página web. Este cambio mejora el rendimiento y la confiabilidad del explorador, pero puede afectar a las aplicaciones web que aún no se han actualizado para usar API web más modernas, como sendBeacon y Fetch. La directiva de grupo para deshabilitar este cambio y permitir la XHR sincrónica durante el descarte de la página estará disponible hasta Microsoft Edge 88. Para más información, consulte [Cambios que se van a producir en Microsoft Edge que afectan a la compatibilidad de los sitios](/microsoft-edge/web-platform/site-impacting-changes).

### <a name="policy-updates"></a>Actualizaciones de directiva

#### <a name="new-policies"></a>Nuevas directivas

Se agregaron 15 nuevas directivas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AllowSurfGame](./microsoft-edge-policies.md#allowsurfgame): permitir juego de navegación.
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls): configurar la lista de sitios con los que Microsoft Edge intentará establecer un enlace de tokens.
- [BingAdsSuppression](./microsoft-edge-policies.md#bingadssuppression): bloquear todos los anuncios en los resultados de búsqueda de Bing.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled): determina si el comprobador de certificados integrado se usará para comprobar certificados de servidor.
- [ClearCachedImagesAndFilesOnExit](./microsoft-edge-policies.md#clearcachedimagesandfilesonexit): limpiar las imágenes y los archivos almacenados en caché cuando se cierra Microsoft Edge.
- [ConfigureShare](./microsoft-edge-policies.md#configureshare): configurar la experiencia de uso compartido.
- [DeleteDataOnMigration](./microsoft-edge-policies.md#deletedataonmigration): eliminar datos antiguos del explorador en la migración.
- [DnsOverHttpsMode](./microsoft-edge-policies.md#dnsoverhttpsmode): controlar el modo de DNS a través de HTTPS.
- [DnsOverHttpsTemplates](./microsoft-edge-policies.md#dnsoverhttpstemplates): especificar la plantilla URI de la resolución de DNS a través de HTTPS deseada.
- [FamilySafetySettingsEnabled](./microsoft-edge-policies.md#familysafetysettingsenabled): permitir que los usuarios configuren la seguridad familiar.
- [LocalProvidersEnabled](./microsoft-edge-policies.md#localprovidersenabled): permitir sugerencias de proveedores locales.
- [ScrollToTextFragmentEnabled](./microsoft-edge-policies.md#scrolltotextfragmentenabled): habilitar el desplazamiento al texto especificado en fragmentos de URL.
- [ScreenCaptureAllowed](./microsoft-edge-policies.md#screencaptureallowed): permitir o denegar capturas de pantalla.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): configurar la lista de tipos que se excluyen de la sincronización.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled): habilitar ocultar ventanas nativas.

#### <a name="deprecated-policy"></a>Directivas en desuso

Las siguientes directivas seguirán funcionando en esta versión. Pasarán a estar "en desuso" en una versión futura.

[EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) habilitar descarga de acciones de dominio de Microsoft

<!-- end 83 -->

## <a name="version-81041677-may-18"></a>Versión 81.0.416.77: 18 de mayo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-81041672-may-7"></a>Versión 81.0.416.72: 7 de mayo

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#may-7-2020)

## <a name="version-81041668-april-29"></a>Versión 81.0.416.68: 29 de abril

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#april-29-2020)

## <a name="version-81041664-april-23"></a>Versión 81.0.416.64: 23 de abril

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#april-23-2020)

## <a name="version-81041658-april-17"></a>Versión 81.0.416.58: 17 de abril

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#april-17-2020)

## <a name="version-81041653-april-13"></a>Versión 81.0.416.53: 13 de abril

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#april-13-2020)

### <a name="feature-updates"></a>Actualizaciones de características

- Se agregó la compatibilidad con Windows Information Protection (WIP), que ayuda a las empresas a proteger los datos confidenciales de una divulgación no autorizada. [Más información](./microsoft-edge-security-windows-information-protection.md).

- Colecciones ya está disponible. Para empezar, haga clic en el icono Colecciones que encontrará junto a la barra de direcciones. Esta acción abre el panel Colecciones, donde podrá crear, editar y ver las colecciones. Diseñamos Colecciones en función de lo que los usuarios hacen en la web. Sin importar si es comprador, viajero, profesor o alumno, las colecciones pueden ser de ayuda. [Más información](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Permita la eliminación (ocultar de la barra de herramientas) del botón Colecciones de la barra de herramientas de Microsoft Edge para lograr coherencia.

- El inicio de sesión automático en cuentas de Active Directory locales solo se dirigirá a las organizaciones que lo activen.  Si los usuarios ya han iniciado sesión con una cuenta de AD local, podrán salir de la sesión. Los usuarios solo iniciarán sesión automáticamente con la cuenta principal en su sistema operativo si es una cuenta de Microsoft o una cuenta de Active Directory. Los administradores pueden habilitar el inicio de sesión automático con una cuenta de AD local con la directiva ConfigureOnPremisesAccountAutoSignIn.

- Protección de aplicaciones. La compatibilidad con las extensiones ahora está disponible en el contenedor.

- Se ha agregado un mensaje para informar a los usuarios de que Internet Explorer no se instala cuando un usuario navega a una página que está configurada para abrirse en modo de Internet Explorer.

- Se ha actualizado la herramienta vista 3D de Microsoft Edge DevTools con una nueva característica que ayuda a depurar el contexto de apilamiento de índice z. La vista 3D muestra una representación de la profundidad del modelo de objetos de documento (DOM) utilizando colores y apilamiento, y la vista de índice z le ayuda a aislar los distintos contextos de apilamiento de la página. [Más información](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Las herramientas de desarrollo F12 están localizadas en 10 idiomas nuevos, por lo que coincidirán con el idioma que se usa en el resto del explorador. [Más información](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Se ha agregado compatibilidad con la reproducción de Dolby Vision. En compilación 17134 de Windows 10 (actualización 2018 de abril) con Dolby Vision activado, los sitios web pueden mostrar el contenido de Dolby Vision. Vea cómo habilitar el contenido de Dolby Vision en [Netflix](https://help.netflix.com/en/node/42384).

- Microsoft Edge ahora puede identificar y quitar duplicados de favoritos y combinar carpetas que tienen el mismo nombre. Para acceder a la herramienta, haga clic en la estrella en la barra de herramientas del explorador y seleccione "Quitar favoritos duplicados".  Puede confirmar los cambios y las actualizaciones de sus favoritos se sincronizarán en todos los dispositivos.

- Los usuarios nos han indicado que puede resultar complicado distinguir una ventana de navegación normal en un tema oscuro de una ventana de InPrivate, ya que ambos marcos de ventana son oscuros. La nueva píldora azul de InPrivate en la esquina superior derecha ayuda a asegurar a los usuarios que están en InPrivate.

- Abra vínculos externos en el perfil de explorador correcto. Seleccione un perfil predeterminado para abrir los vínculos abiertos para aplicaciones externas en *edge://settings/multiProfileSettings*.

- Se ha agregado una advertencia que alerta a los usuarios que inician sesión en un perfil de explorador con una cuenta después de haber iniciado sesión con otra cuenta previamente. Esta advertencia ayudará a evitar la combinación de datos no intencionada.

- Si tiene tarjetas de pago guardadas en su cuenta de Microsoft, puede usarlas en Microsoft Edge mientras rellena formularios de pago. Las tarjetas de su cuenta de Microsoft se sincronizarán en los dispositivos de escritorio y todos los detalles se compartirán con el sitio web después de la autenticación de dos factores (código CVC y su identidad de Microsoft). Para más comodidad, puede elegir guardar una copia de la tarjeta en el dispositivo de forma segura durante la autenticación.

- El foco de línea está diseñado para los usuarios que deseen concentrarse en una parte limitada del contenido mientras leen. Permite que los usuarios mantengan el foco en una, tres o cinco líneas cada vez y atenúa el resto de la página para que los usuarios puedan leer sin distracciones. Los usuarios pueden desplazarse con las teclas táctiles o de dirección y el foco cambia en consecuencia.

- Microsoft Edge está ahora integrado con el corrector ortográfico de Windows en las plataformas Windows 8.1 y posteriores. Esta integración ofrece una mayor compatibilidad con idiomas, con acceso a más diccionarios de idiomas y la posibilidad de usar diccionarios personalizados de Windows. Los usuarios no necesitan realizar ninguna acción cuando se ha agregado un idioma en la configuración de idioma del sistema operativo. Además, el botón de alternancia de corrección ortográfica del idioma está habilitado en la configuración de Microsoft Edge

- Cuando se abren documentos PDF con Microsoft Edge, los usuarios ya podrán crear resaltados, cambiar el color y eliminar los resaltados. Esta característica ayuda a hacer referencia a partes importantes del documento más adelante y para la colaboración.

- Cuando cargue documentos PDF largos que se han optimizado para la web, las páginas que está viendo el usuario se cargarán más rápido, en paralelo, mientras el resto del documento se carga.

- Ahora es más fácil empezar a usar el lector inmersivo para un sitio web pulsando la tecla F9.

- Ahora es más fácil empezar la lectura en voz alta con un método abreviado de teclado (Ctrl + Mayús + U).

- Se ha agregado un parámetro de línea de comandos MSI que le permite suprimir la creación de iconos de escritorio al instalar Microsoft Edge. El siguiente ejemplo muestra cómo usar este nuevo parámetro: <br>
`MicrosoftEdgeEnterpriseX64.msi DONOTCREATEDESKTOPSHORTCUT=true`<br>
Habrá una directiva de grupo para dar soporte a esta funcionalidad en una versión futura.

### <a name="policy-updates"></a>Actualizaciones de directiva

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado 11 directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled): habilitar la autenticación de ambiente para los perfiles de InPrivate e invitado. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled): permitir ejecutar el espacio aislado de audio.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): usar una directiva de referrer predeterminada de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled): habilitar la memoria caché de autenticación HTTP de ámbito global.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions): permitir la importación de extensiones.
- [ImportCookies](./microsoft-edge-policies.md#importcookies): permitir la importación de cookies.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts): permitir la importación de métodos abreviados.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect) : especificar cómo se comportan las navegaciones "en la página" de los sitios no configurados al iniciarse en las páginas en modo Internet Explorer.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled): habilitar el tratamiento más estricto para contenido mixto.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled): habilitar una característica de seguridad TLS 1.3 para anclajes de veracidad locales.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin): configurar el inicio de sesión automático con una cuenta de dominio de Active Directory cuando no haya cuenta de dominio de Azure AD.

#### <a name="policy-name-and-caption-changes"></a>Cambios en el nombre y el título de directiva

La directiva `OmniboxMSBProviderEnabled` ha cambiado a [AddressBarMicrosoftSearchInBingProviderEnabled](//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled): el título de la directiva es "Habilitar sugerencias de Búsqueda de Microsoft en Bing en la barra de direcciones".

#### <a name="deprecated-policies"></a>Directivas obsoletas

Las siguientes directivas siguen funcionando en esta versión. Pasarán a ser "obsoletas" en una versión futura.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled): volver a habilitar la API de componentes web v0 hasta M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies): permitir que el controlador WebDriver reemplace Incompatible.

#### <a name="resolved-issues"></a>Problemas resueltos

- Se ha corregido un problema en el que el modo IE en Microsoft Edge provocaba que apareciese un cuadro de diálogo de descarga en curso, incluso después de descargar el archivo.
- Se ha corregido un problema que provocaba que Microsoft Edge quitara las cookies de sesión cuando una página que ya estaba en modo IE activaba la apertura de una nueva pestaña en modo IE.

## <a name="version-800361111-april-7"></a>Versión 80.0.361.111: 7 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-800361109-april-1"></a>Versión 80.0.361.109: 1 de abril

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#april-1-2020)

## <a name="version-80036169-march-19"></a>Versión 80.0.361.69: 19 de marzo

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#march-19-2020)

## <a name="version-80036166-march-4"></a>Versión 80.0.361.66: 4 de marzo

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#march-4-2020)

## <a name="version-80036162-february-25"></a>Versión 80.0.361.62: 25 de febrero

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#february-25-2020)

## <a name="version-80036157-february-20"></a>Versión 80.0.361.57: 20 de febrero

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#february-20-2020)

## <a name="version-80036156-february-19"></a>Versión 80.0.361.56: 19 de febrero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-80036154-february-14"></a>Versión 80.0.361.54: 14 de febrero

### <a name="resolved-issues"></a>Problemas resueltos

- Se ha corregido un problema por el que la contraseña, el pago y las cookies no se importaban en Microsoft Edge.

## <a name="version-80036150-february-11"></a>Versión 80.0.361.50: 11 de febrero

Se han solucionado varios errores y correcciones de rendimiento.

## <a name="version-80036148-february-7"></a>Versión 80.0.361.48: 7 de febrero

Las actualizaciones de seguridad se muestran [aquí](./microsoft-edge-relnotes-security.md#february-7-2020)

### <a name="feature-updates"></a>Actualizaciones de características

- Se ha agregado la protección de SmartScreen para descargar aplicaciones potencialmente no deseadas. [Obtén más información](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
- Se ha agregado compatibilidad con la reproducción de Dolby Vision.
- Se ha habilitado a los usuarios de Windows Mixed Reality para ver vídeos de 360 ° en auriculares con micrófono de VR.
- Se ha agregado una opción a la vista de lectura para aumentar el espaciado del texto.
- Se ha agregado compatibilidad para borrar el vínculo con el borrador del lápiz para Surface.
- Se ha agregado compatibilidad con las teclas de dirección y la barra espaciadora para dibujar en las capturas de comentarios en modo Editor.
- Se ha mejorado la confiabilidad de las capturas de pantallas para que dejen de aparecer en negro al enviar comentarios.
- Se ha agregado compatibilidad con temas oscuros en la página de nueva pestaña local que se muestra cuando el dispositivo no está conectado a Internet.
- Se ha agregado la capacidad de restaurar sitios web instalados como aplicaciones cuando se restaura una sesión del explorador después de una actualización, bloqueo, etc.
- Se agregó compatibilidad con temas oscuros en la interfaz de usuario de PDF cuando el explorador está administrado por una directiva de grupo.
- Se ha actualizado Adobe Flash a la versión 32.0.0.321. [Obtén más información](https://helpx.adobe.com/flash-player/release-note/fp_32_air_32_release_notes.html)

### <a name="policy-updates"></a>Actualizaciones de directivas

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado 16 directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AlternateErrorPagesEnabled](./microsoft-edge-policies.md#alternateerrorpagesenabled): Sugiere páginas similares cuando no se puede encontrar una página web.
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting): controlar el uso de excepciones de contenido no seguro.
- [DNSInterceptionChecksEnabled](./microsoft-edge-policies.md#dnsinterceptionchecksenabled): comprobaciones de interceptación de DNS habilitadas.
- [HideFirstRunExperience](./microsoft-edge-policies.md#hidefirstrunexperience): ocultar la experiencia de primera ejecución y la pantalla de presentación.
- [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls): permitir el contenido no seguro en sitios especificados.
- [InsecureContentBlockedForUrls](./microsoft-edge-policies.md#insecurecontentblockedforurls): bloquear contenido no seguro en sitios especificados.
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled): habilitar la configuración de comportamiento de cookies de SameSite heredado predeterminado.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist): revertir al comportamiento de SameSite heredado para las cookies en sitios especificados.
- [PaymentMethodQueryEnabled](./microsoft-edge-policies.md#paymentmethodqueryenabled): permitir que los sitios web consulten las formas de pago disponibles.
- [PersonalizationReportingEnabled](./microsoft-edge-policies.md#personalizationreportingenabled): permitir la personalización de anuncios, búsquedas y noticias enviando historial de exploración a Microsoft.
- [PinningWizardAllowed](./microsoft-edge-policies.md#pinningwizardallowed): permitir el Asistente para Anclar a la barra de tareas.
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled): configurar Microsoft Defender SmartScreen para bloquear aplicaciones potencialmente no deseadas.
- [TotalMemoryLimitMb](./microsoft-edge-policies.md#totalmemorylimitmb): establecer el límite en megabytes de memoria que puede usar una única instancia de Microsoft Edge.
- [WebAppInstallForceList](./microsoft-edge-policies.md#webappinstallforcelist): configurar la lista de aplicaciones web instaladas por la fuerza.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled): volver a habilitar la API de componentes web v0 hasta M84.
- [WebRtcLocalIpsAllowedUrls](./microsoft-edge-policies.md#webrtclocalipsallowedurls): administrar la exposición de direcciones IP locales por WebRTC.

#### <a name="deprecated-policies"></a>Directivas obsoletas

La siguiente directiva ha quedado obsoleta.

- [NewTabPageCompanyLogo](./microsoft-edge-policies.md#newtabpagecompanylogo): establecer el logotipo de la página de nueva pestaña.

### <a name="resolved-issues"></a>Problemas resueltos

- Se ha corregido un problema que hacía que el audio no funcionase en el entorno de Citrix.
- Se ha corregido un problema por el que la experiencia en paralelo de Microsoft Edge y Microsoft Edge heredado producía bloqueos y vínculos heredados fallidos.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)