---
title: Notas de la versión de Microsoft Edge para el canal estable
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de la versión de Microsoft Edge para el canal estable
ms.openlocfilehash: cb30da25581653b33c9529178b40a8de7161a7d1
ms.sourcegitcommit: e5980a7a36c252e8a04315b3d4c64a161027324e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297053"
---
# Notas de la versión para el canal estable de Microsoft Edge

Estas notas de versión proporcionan información sobre las nuevas características y las actualizaciones no relacionadas con la seguridad que se incluyen en el canal estable de Microsoft Edge.

- Todas las actualizaciones de seguridad se muestran [aquí](microsoft-edge-relnotes-security.md).
- Las notas de la versión archivadas para el Canal estable de Microsoft Edge se encuentran [aquí](microsoft-edge-relnote-archive-stable-channel.md).

 Para entender los canales de Microsoft Edge, vea la [Información general sobre los canales de Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Para el Canal estable, las actualizaciones se implementarán de manera progresiva en uno o más días. Para obtener más información, consulte [Progressive rollouts for Microsoft Edge updates (Implementaciones progresivas de actualizaciones de Microsoft Edge)](microsoft-edge-update-progressive-rollout.md).

## Versión 88.0.705.50: 21 de enero

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-21-2021).

<!--- begin major 88  --->
### Actualizaciones de características

- **Desusos:**

  - Desusar la compatibilidad con el protocolo FTP. Se ha quitado la compatibilidad con el protocolo FTP heredado de MicrosoftEdge. Si se intenta navegar a un vínculo FTP, el explorador dirigirá el sistema operativo para que abra una aplicación externa para controlar el vínculo FTP. Como alternativa, los administradores de TI pueden configurar MicrosoftEdge para usar el modo IE para los sitios que dependen del protocolo FTP.
  - La compatibilidad con AdobeFlash se eliminará. A partir de la versión88 de Microsoft Edge Beta, se eliminarán la funcionalidad y la compatibilidad con Adobe Flash. Más información: [actualización sobre la finalización del soporte en Adobe Flash Player: blog de MicrosoftEdge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Autenticación:**

  - El inicio de sesión único (SSO) ya está disponible para las cuentas de Azure Active Directory (Azure AD) y las cuentas de Microsoft (MSA) en versiones de Windows de nivel inferior. Un usuario que haya iniciado sesión en Microsoft Edge en una versión de Microsoft Windows de nivel inferior (versiones 7 y 8.1) ahora tendrá la sesión iniciada de manera automática en los sitios web que estén configurados para permitir el inicio de sesión único con cuentas profesionales y de Microsoft (por ejemplo, bing.com, office.com, msn.com, outlook.com).<br>Nota: es posible que un usuario tenga que cerrar sesión y volver a iniciarla si ha iniciado sesión en Microsoft Edge en una versión anterior a Microsoft Edge 88 para poder aprovechar esta característica.

- **Opción de modo de pantalla completa para finalizar la sesión**. El botón "Finalizar sesión" ahora está disponible en una experiencia de navegación pública en modo de pantalla completa. Esta característica garantiza que los datos y la configuración del explorador se eliminen cuando se cierra Microsoft Edge. Más información sobre las características y la guía básica del modo de pantalla completa, [Configurar el modo de pantalla completa de Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

- **Seguridad y privacidad:**

  - Se generan alertas si se encuentra la contraseña de un usuario en una filtración en línea. Las contraseñas de usuario se comprueban con un repositorio de credenciales infringidas y se envía una alerta al usuario si se encuentra una coincidencia. Para garantizar la seguridad y la privacidad, las contraseñas de los usuarios se dividen y cifran cuando se comparan con la base de datos de credenciales filtradas.
  - Actualice automáticamente el contenido mixto. Las páginas seguras que se proporcionan a través de HTTPS pueden contener imágenes de referencias que se sirven a través de HTTP no seguro. Para mejorar la privacidad y la seguridad en Microsoft Edge 88, esas imágenes se recuperarán a través de HTTPS. Si la imagen no está disponible a través de HTTPS, no se cargará.
  - Vea permisos de sitio por sitio y por actividad reciente. A partir de Microsoft Edge 88, los usuarios podrán administrar los permisos de los sitios más fácilmente. Podrán ver los permisos por sitio web en lugar de solo por tipo de permiso. Además, hemos agregado una sección de actividades recientes que le mostrará al usuario todos los cambios recientes en los permisos de su sitio.
  - Más controles para las cookies del explorador. A partir de Microsoft Edge 88, los usuarios pueden eliminar cookies de terceros sin que esto afecte a las cookies principales. Además, los usuarios podrán filtrar las cookies según si son principales o de terceros y ordenar por nombre, número de cookies y la cantidad de datos almacenados y modificados por última vez.

- **Contraseñas:**

  - Generador de contraseñas. Microsoft Edge ofrece un generador de contraseñas seguras integrado que puede usar al registrarse para obtener una nueva cuenta o al cambiar una contraseña existente. Solo tiene que buscar la lista desplegable de contraseñas sugeridas del explorador en el campo de contraseña y, cuando se seleccione, se guardará automáticamente en el explorador y se sincronizará en todos los dispositivos para facilitar su uso en el futuro.
  - Monitor de contraseñas. Cuando cualquiera de las contraseñas guardadas en el explorador coincida con las que se ven en la lista de credenciales filtradas, Microsoft Edge le notificará y le pedirá que actualice la contraseña. El Monitor de contraseñas busca coincidencias por usted y está activado de forma predeterminada.
  - Editar contraseña. Ahora puede editar las contraseñas guardadas directamente en la configuración de Microsoft Edge. Reemplazar una contraseña anterior guardada por una nueva cada vez que se actualice la contraseña fuera de Microsoft Edge es sencillo. Solo debe editar la contraseña guardada en Configuración. 

- **Rendimiento:**

  - Mejore el rendimiento del explorador con pestañas en suspensión. Las pestañas en suspensión mejoran el rendimiento del explorador al poner pestañas inactivas en reposo para liberar recursos del sistema, como la memoria y la CPU, de modo que las pestañas activas u otras aplicaciones puedan usarlos. Los usuarios pueden impedir que los sitios entren en suspensión y configurar el período de tiempo antes de que la pestaña inactiva se suspenda. Para mantener a los usuarios en su flujo, también se utiliza la heurística para evitar que determinados sitios pasen al modo de suspensión, como los sitios de la intranet. Esta característica se limita a un grupo de usuarios seleccionados al azar que han permitido la experimentación. Planeamos tener la función de pestañas flotantes activada de forma predeterminada en Microsoft Edge versión 89. Esta característica se puede administrar con directivas de grupo.
  - Mejore la velocidad de inicio de Microsoft Edge con el aumento de inicio. Para mejorar la velocidad de inicio de Microsoft Edge, hemos desarrollado una característica denominada aumento de inicio. El aumento de inicio hace que Microsoft Edge se inicie más rápido al habilitar Microsoft Edge para que se ejecute en segundo plano. Nota: esta característica está limitada a un grupo de usuarios seleccionado aleatoriamente que han habilitado la experimentación. Estos usuarios proporcionan comentarios al equipo de características.

- **Productividad:**

  - Mejorar la productividad y la multitarea con pestañas verticales. A medida que el número de pestañas horizontales crece, los títulos de sitios comienzan a cortarse y los controles de pestaña se pierden a medida que se reducen las pestañas. Esto interrumpe el flujo de trabajo del usuario, ya que dedica más tiempo a buscar, cambiar y administrar sus pestañas, y menos tiempo a la tarea. Las pestañas verticales permiten a los usuarios mover sus pestañas al costado, donde los iconos alineados verticalmente y los títulos de sitio más largos hacen que sea más fácil digitalizar, identificar y cambiar a la pestaña que quiera abrir rápidamente.
  - Rellene automáticamente el campo de fecha de nacimiento. Microsoft Edge ya ayuda a ahorrar tiempo y esfuerzo mientras rellenas formularios y crea cuentas en línea mediante el rellenado automático de datos de usuario, como direcciones, nombres, números de teléfono, etc. Microsoft Edge ahora es compatible con el campo de fecha de nacimiento que los usuarios pueden guardar y rellenar automáticamente. Un usuario puede ver, editar y eliminar esta información en cualquier momento en la configuración de su perfil.
  - Mejoras en el historial de Cerrados recientemente. Cerrados recientemente ahora mantiene las últimas 25pestañas y ventanas de cualquier sesión de exploración pasada en lugar de solo la sesión anterior. Los usuarios pueden seleccionar Cerrados recientemente en la nueva experiencia de historial para ver todas las pestañas que estaban abiertas.
  - La función "Tu día de un vistazo" está activada de forma predeterminada. A partir de la versión 88 de Microsoft Edge, los trabajadores de la información pueden beneficiarse de las características de productividad inteligentes en su página de Nueva pestaña. Los usuarios de Microsoft Edge 87 también experimentarán estas características en un plazo de 2 semanas después del lanzamiento de la versión 88 de Microsoft Edge. Ofrecemos contenido personalizado y relevante a los usuarios que hayan iniciado sesión con su cuenta profesional o educativa, con tecnología de M365 Graph. Los usuarios pueden examinar rápidamente sus módulos "Tu día de un vistazo" para realizar un seguimiento sencillo de las reuniones y del trabajo reciente, así como iniciar rápidamente las aplicaciones que quiera usar.

- **El Historial y las pestañas abiertas se sincronizan.** Se han actualizado las directivas existentes de sincronización e historial del explorador, y los usuarios pueden configurar estas directivas para habilitar la sincronización para el historial del explorador y las pestañas abiertas.

- **PDF:**

  - Presentación de documentos PDF en la vista de libro (dos páginas). A partir de la versión 88 de Microsoft Edge, los usuarios pueden ver documentos PDF en una sola página o en la vista de libro de dos páginas. Para cambiar la vista, haga clic en el botón **Vista de página** de la barra de herramientas.
  - Compatibilidad con notas de texto anclado para archivos PDF. A partir de la versión 87 de Microsoft Edge, los usuarios pueden agregar notas de texto escrito en cualquier parte del texto en archivos PDF.

- **Fuentes:**

  - Los iconos del explorador se actualizan en el sistema de diseño Fluent. Como parte de nuestro trabajo constante en torno a Fluent Design en el explorador, hemos realizado cambios para alinear los iconos con el nuevo sistema de iconos de Microsoft. Estos cambios afectarán a numerosas interfaces de usuario con un alto nivel de función táctil, como pestañas, barra de direcciones, iconos de navegación y orientación, que se encuentran en los distintos menús.
  - Representación de fuentes mejorada. La representación de texto se ha mejorado para mejorar la claridad y para reducir el efecto borroso.

### Actualizaciones de directivas

#### Nuevas directivas

Se han agregado dieciocho directivas nuevas. Descargue las Plantillas administrativas actualizadas desde la [página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se han agregado las siguientes directivas nuevas.

- [BasicAuthOverHttpEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#basicauthoverhttpenabled): permite la autenticación básica para HTTP.
- [BlockExternalExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#blockexternalextensions): bloquea las extensiones externas para que no se instalen.
- [InternetExplorerIntegrationLocalFileAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileallowed): permite el inicio de archivos locales en el modo de Internet Explorer.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist): abre archivos locales en la lista de permiso de extensión de archivos en el modo de Internet Explorer.
- [InternetExplorerIntegrationLocalFileShowContextMenu](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileshowcontextmenu): muestra el menú contextual para abrir un vínculo en el modo de Internet Explorer.
- [IntranetRedirectBehavior](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intranetredirectbehavior): comportamiento de redirección de intranet.
- [PrinterTypeDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printertypedenylist): deshabilita los tipos de impresora en la lista de denegación.
- [ShowMicrosoftRewards](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showmicrosoftrewards): muestra las experiencias de Microsoft Rewards.
- [SleepingTabsEnabled](https://docs.microsoft.com/DeployEdge/.microsoft-edge-policies#sleepingtabsenabled): configura las pestañas en suspensión.
- [SleepingTabsTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabstimeout): establece el tiempo de suspensión de la pestaña en segundo plano para las pestañas en suspensión.
- [SleepingTabsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsblockedforurls): bloquea las pestañas en suspensión en sitios específicos.
- [StartupBoostEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#startupboostenabled): habilita el aumento de inicio.
- [TargetBlankImpliesNoOpener:](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#targetblankimpliesnoopener) evita establecer window.opener para vínculos destinados a _blank.
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride): especifica cómo Microsoft Edge Update controla las actualizaciones disponibles de Microsoft Edge.
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed): configura la disponibilidad de un diseño vertical para pestañas en el lateral del explorador.
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols): permite la degradación de TLS/DTLS heredada en WebRTC.
- [WebWidgetAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetallowed): habilita el widget Web.
- [WebWidgetIsEnabledOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetisenabledonstartup): permite el widget web en el inicio de Windows.

#### Directivas obsoletas

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled): habilita la autenticación proactiva.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist): configura las reglas de omisión de proxy.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode): configura la configuración del servidor proxy.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl): establece la dirección URL del archivo proxy .pac.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver): configura la dirección o URL del servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): permite que WebDriver reemplace las directivas incompatibles.

### Directivas obsoletas

- [AllowPopupsDuringPageUnload:](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowpopupsduringpageunload) permite que una página muestre elementos emergentes durante su descarga.
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting): configuración predeterminada de Adobe Flash.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls): permite el complemento Adobe Flash en sitios específicos.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls): bloquea el complemento Adobe Flash en sitios específicos.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode): amplía la configuración de contenido de Adobe Flash a todo el contenido.
<!--- end major 88  --->
## Versión 87.0.664.75: 7 de enero

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-7-2021).

## Versión 87.0.664.66: 17 de diciembre

Se han corregido varios errores y problemas de rendimiento.

## Version 87.0.664.60: 10 de diciembre

Se han corregido varios errores y problemas de rendimiento.

## Versión 87.0.664.57: 7 de diciembre

Se han corregido varios errores y problemas de rendimiento. Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#december-7-2020).

## Versión 87.0.664.55: 3 de diciembre

Se han corregido varios errores y problemas de rendimiento. La siguiente característica se actualizó para esta versión.

- La **opción compras está habilitada de forma predeterminada**. A partir de la versión 87 de Microsoft Edge, los usuarios empresariales pueden beneficiarse de la compra en Microsoft Edge. Con las características de compra, Microsoft Edge ayuda a los usuarios a buscar cupones y mejores precios mientras compras en Internet. (La experiencia del cupón se presentó con la versión estable de 87.0.664.41). La experiencia de comparación de precios ahora está disponible con esta actualización. Esta característica se puede configurar con la directiva [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled). Consulte nuestro [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) y [Obtenga más información](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) sobre Compras de Microsoft.

## Versión 87.0.664.52: 30 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## Versión 87.0.664.47: 23 de noviembre

Se han corregido varios errores y problemas de rendimiento.

<!-- begin major 87 --->
## Versión 87.0.664.41: 19 de noviembre

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-19-2020).

### Actualizaciones de características

- **Redireccionamiento automático para sitios incompatibles de Internet Explorer a Microsoft Edge**. A partir de la actualización estable de Microsoft Edge 87, los sitios web públicos que muestren un mensaje de incompatibilidad en Internet Explorer se redirigirán automáticamente a Microsoft Edge de forma predeterminada. Para más información y configurar esta experiencia, vea [Redirigir sitios incompatibles](https://docs.microsoft.com/deployedge/edge-learnmore-neededge).

- **Las características de privacidad del modo de pantalla completa están habilitadas**. A partir de la versión 87 de Microsoft Edge, se habilitarán las características del modo de pantalla completa que puedan ayudar a las empresas relacionadas a mantener la privacidad de los datos del usuario. Estas características permiten habilitar experiencias como borrar los datos del usuario al salir, eliminar los archivos descargados y restablecer la experiencia de inicio configurada después de un período de inactividad especificado. Más información sobre cómo [Configurar el modo de pantalla completa de Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)

- **Características de la compra habilitadas de forma predeterminada**. A partir de la versión 87 de Microsoft Edge, los usuarios empresariales también pueden beneficiarse de las compras en Edge. Con las características de compra, Microsoft Edge ayuda a los usuarios a buscar cupones y mejores precios mientras compran en línea. La experiencia de cupones está disponible con esta actualización y la comparación de precios se publicará en próximas actualizaciones de Microsoft Edge 87. Esta característica se puede configurar mediante la directiva [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled). Consulte nuestro [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) y [Obtenga más información](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) sobre Compras de Microsoft.

- **Implementación de ClickOnce habilitada de manera predeterminada**. ClickOnce está habilitado de manera predeterminada en Microsoft Edge 87, lo cual reduce las barreras para que las empresas puedan implementar software y alinearse mejor con el comportamiento del explorador Microsoft Edge (versión anterior). A partir de Microsoft Edge 87, el estado "No se configuró" de la directiva ClickOnceEnabled reflejará el nuevo estado predeterminado de ClickOnce Habilitado (en comparación con el estado predeterminado anterior de Deshabilitado).

- **La página de pestaña nueva (NTP) de la empresa ahora integra la productividad al ofrecer un contenido de fuente que se puede personalizar y es relevante para el trabajo**. La NTP de la empresa combina la página de productividad de Office 365 que ofrecemos a los usuarios que hayan iniciado sesión con su cuenta profesional o educativa con fuentes personalizadas relevantes para el trabajo y el sector, que ahora están organizadas en una sola página. Los usuarios reconocerán el contenido de Office 365 con el que están familiarizados, así como la Búsqueda de Microsoft para la Empresa con tecnología de Bing. Además, pueden personalizar "Mi fuente" fácilmente eligiendo el contenido más relevante para ellos entre el contenido y los módulos disponibles para su organización. Los administradores de sistemas de información pueden controlar la configuración de la fuente de Noticias de su organización, incluido el sector seleccionado en la página de la nueva pestaña de Microsoft Edge desde el Centro de administración de Microsoft 365. [Más información](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Privacidad y seguridad:**

  - Enlace del token TLS de soporte para sitios configurados con directiva. El enlace del token TLS ayuda a evitar ataques de intento de robo del token y garantiza que las cookies no puedan volver a usarse desde un dispositivo distinto de aquel desde el que se establecieron inicialmente. El uso de un enlace de token TLS requiere establecer la directiva de [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) y requiere que los sitios que aparecen en la lista sean compatibles con esta característica.

- **Compatibilidad del teclado con el marcador de resaltado en archivos PDF**. Los usuarios pueden usar las teclas del teclado para resaltar cualquier texto en un archivo PDF.

- **Impresión:**

  - Elija el lado por el cual quiere que se voltee la página al imprimir en ambas caras. Los usuarios pueden optar por voltear la página por el lado largo o por el lado corto de la hoja al imprimir en ambas caras.
  - Elija el modo imprimir rasterización para la empresa. Controle la forma en que Microsoft Edge imprime en una impresora que no sea PostScript en Windows. En ocasiones, es necesario rasterizar los trabajos de impresión de impresoras que no sean PostScript para que se impriman correctamente. Las opciones de impresión son "Completa" y "Rápida".

### Actualizaciones de directivas

#### Nuevas directivas

Se han agregado diez directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se han agregado las siguientes directivas nuevas.

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat): configura el formato de pegado predeterminado de las direcciones URL copiadas desde Microsoft Edge y determina si los formatos adicionales estarán disponibles para los usuarios.
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled): Compras de Microsoft Edge está habilitado.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled): oculta el cuadro de diálogo de redirección que aparece una sola vez y el banner en Microsoft Edge.
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled): Configura la edición de la barra de direcciones para la experiencia de navegación pública en modo de pantalla completa.
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit): elimina los archivos descargados como parte de la sesión de pantalla completa al cerrar Microsoft Edge.
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled): habilita el botón Mostrar contraseña.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall): evita la instalación del objeto auxiliar de explorador (BHO) para redirigir los sitios incompatibles desde Internet Explorer a Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode): redirige los sitios incompatibles desde Internet Explorer a Microsoft Edge.
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled): configura el reconocimiento de voz.
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled): habilita la característica de captura web en Microsoft Edge.

#### Directivas en desuso

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype): Configura la experiencia de la página de pestaña nueva de Microsoft Edge.

#### Directiva obsoleta

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures): vuelve a habilitar las características de la plataforma web en desuso por un tiempo limitado.

<!-- end major 87 -->

## Versión 86.0.622.69: 13 de noviembre

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-13-2020). Esta actualización contiene [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) y [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), que han sido reportados por el equipo de Chromium como si fueran una vulnerabilidad de seguridad.

## Versión 86.0.622.68: 11 de noviembre

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-11-2020)

## Versión 86.0.622.63: 4 de noviembre

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-4-2020). Esta actualización contiene [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), que ha sido reportado por el equipo de Chromium como una vulnerabilidad de seguridad.

## Versión 86.0.622.61: 2 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## Versión 86.0.622.58: 29 de octubre

Se han corregido varios errores y problemas de rendimiento.

## Versión 86.0.622.56: 27 de octubre

Se han corregido varios errores y problemas de rendimiento.

## Versión 86.0.622.51: 22 de octubre

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-22-2020)

## Versión 86.0.622.48: 20 de octubre

Se han corregido varios errores y problemas de rendimiento.

## Versión 86.0.622.43: 15 de octubre

Se han corregido varios errores y problemas de rendimiento.

<!-- begin major 86 -->
## Versión 86.0.622.38: 9 de octubre

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-9-2020)

### Actualizaciones de características

* **Volver a la versión anterior de Microsoft Edge.** La característica de restauración permite a los administradores volver a una versión en buen estado y conocida de Microsoft Edge si hay algún problema en la versión más reciente de Microsoft Edge. **Nota:** versión estable 86.0.622.38 es la primera versión a la que se puede revertir, lo que significa que la versión estable 87 es la primera versión preparada para la reversión. [Más información](edge-learnmore-rollback.md).

* **Ejecutar la habilitación de Sincronización de forma predeterminada en toda la empresa.**  Los administradores pueden habilitar la sincronización para cuentas de Azure Active Directory (Azure AD) de forma predeterminada con la directiva [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync).

* **Cambio de perfil automático en Windows 7 y 8.1.** El cambio de perfil automático que se encuentra disponible actualmente en Microsoft Edge en Windows 10 ha sido extendido a otros Windows de nivel inferior (Windows 7 y 8.1). Para obtener más información, consulte la publicación en el blog [cambio de perfil automático](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Cookies con SameSite=Lax de manera predeterminada**. Para mejorar la seguridad y la privacidad Web, las cookies usarán ahora [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) de manera predeterminada. Esto significa que las cookies se enviarán solo como cookies de origen y se omitirán para las solicitudes que se envíen a terceros. Este cambio puede provocar un impacto en la compatibilidad en aquellos sitios web que necesitan cookies para recursos de terceros para funcionar correctamente. Para permitir el envío de cookies, los desarrolladores web pueden marcar cookies que deberían establecerse y recibirse en contextos de terceros agregando atributos `SameSite=none` y `Secure` explícitos al establecer la cookie. Las empresas que quieran excluir determinados sitios de este cambio pueden usar la directiva [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) y las que quieran que ningún sitio sufra el cambio, pueden valerse de la directiva [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled).

* **Quitar la API de caché de aplicaciones HTML5.**  A partir de la versión 86 de Microsoft Edge, la API de caché de aplicaciones heredada que permite el uso sin conexión de páginas web se quita de Microsoft Edge. Los desarrolladores web deben revisar la documentación [WebDev](https://web.dev/appcache-removal/) para obtener información sobre cómo reemplazar la API de caché de aplicaciones con trabajos de servicio.  Importante: Puede solicitar un [token de AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) que permite a los sitios seguir usando la API de caché de aplicaciones obsoleta hasta la versión 90 de Microsoft Edge.

* **Privacidad y seguridad:**

  * **Reemplazar las directivas [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) y [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) para las versiones anteriores de Windows y macOS.** Estas directivas están en desuso en la versión 86 de Microsoft Edge y quedarán obsoletas en Microsoft Edge versión 89.<br>
Estas directivas se reemplazarán por [Permitir telemetría](https://go.microsoft.com/fwlink/?linkid=2099569) en Windows 10 y la nueva directiva [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) para las demás plataformas. Esto permitirá que los usuarios administren los datos de diagnóstico que se envían a Microsoft para Windows 7, 8, 8.1 y macOS.
  * Soporte de DNS seguro (DNS a través de HTTPS).  A partir de la versión 86 de Microsoft Edge, está disponible la configuración para controlar el DNS seguro en los dispositivos no administrados. Estas opciones de configuración no son accesibles para los usuarios de dispositivos administrados, pero los administradores de TI pueden habilitar o deshabilitar el DNS seguro con la directiva de grupo [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode).

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

### Actualizaciones de directiva

#### Nuevas directivas

Ha sido agregado veinticuatro directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist): Bloquear el acceso a una lista especificada de servicios y destinos de exportación en Colecciones.
- [DefaultFileSystemReadGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultfilesystemreadguardsetting) controle el uso de la API del sistema de archivos para su lectura.
- [DefaultFileSystemWriteGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultfilesystemwriteguardsetting) controle el uso de la API del sistema de archivos para su escritura.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting): Configuración predeterminada de sensores.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting): Controlar el uso de la API de serie.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata): enviar datos de diagnóstico necesarios y opcionales sobre el uso del explorador.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed): Permitir el acceso a la herramienta Enterprise Mode Site List Manager
- [FileSystemReadAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemreadaskforurls): permitir el acceso de lectura a través de la API del sistema de archivos en estos sitios.
- [FileSystemReadBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemreadblockedforurls) -bloquear el acceso de lectura a través de la API del sistema de archivos en estos sitios.
- [FileSystemWriteAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemwriteaskforurls) : permitir el acceso de escritura a los archivos y directorios en estos sitios.
- [FileSystemWriteBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemwriteblockedforurls) : bloquear el acceso de escritura a los archivos y directorios en estos sitios.
- [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync): Forzar la sincronización de los datos del explorador y no mostrar la solicitud de consentimiento de sincronización.
- [InsecureFormsWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecureformswarningsenabled) : Habilitar advertencias para formularios no seguros.
- [InternetExplorerIntegrationTestingAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed): Permitir probar el modo de Internet Explorer.
- [SpotlightExperiencesAndRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#spotlightexperiencesandrecommendationsenabled): Decidir si los usuarios pueden recibir imágenes de fondo y texto personalizados, sugerencias, notificaciones y recomendaciones para los servicios de Microsoft.
- [NewTabPageAllowedBackgroundTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageallowedbackgroundtypes): Configurar los tipos de fondo permitidos para el diseño de página de nueva pestaña.
- [SaveCookiesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savecookiesonexit): Guardar cookies cuando se cierra Microsoft Edge.
- [SensorsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsallowedforurls): Permitir el acceso a sensores en sitios específicos.
- [SensorsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsblockedforurls): Bloquear el acceso a sensores en sitios específicos.
- [SerialAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialaskforurls): Permitir la API de serie en sitios específicos.
- [SerialBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialblockedforurls): Bloquear la API de serie en sitios específicos.
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled): Habilitar la característica User-Agent Client Hints (en desuso).
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit): Limitar el número de instantáneas de datos de usuario que se conservan para su uso en caso de reversión de emergencia.

#### Directivas obsoletas

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): habilitar el uso y los informes de datos relacionados con bloqueos.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): enviar información de sitios para mejorar los servicios Microsoft.

#### Directiva obsoleta

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled): habilitar una característica de seguridad TLS 1.3 para anclajes de veracidad locales.

<!-- end 86 -->
## Versión 85.0.564.70: 6 de octubre

Se han corregido varios errores y problemas de rendimiento.

## Versión 85.0.564.68: 1 de octubre

Se han corregido varios errores y problemas de rendimiento.

## Versión 85.0.564.63: 23 de septiembre

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-23-2020)

## Versión 85.0.564.51: 9 de septiembre

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-9-2020)

## Versión 85.0.564.44: 31 de agosto

Se han corregido varios errores y problemas de rendimiento.
<!-- begin 85 -->
## Versión 85.0.564.41: 27 de agosto

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-27-2020)

### Actualizaciones de características

- **Sincronización local de los Favoritos y las Configuraciones**. Ahora puede sincronizar los favoritos y la configuración del explorador entre los perfiles de Active Directory dentro de su propio entorno sin necesidad de sincronización en la nube.

- **Soporte de la directiva del grupo de Microsoft Edge para los sitios confiables y combinaciones de aplicaciones para iniciar sin aviso de confirmación.** El soporte añadido a la directiva del grupo permite a los administradores agregar combinaciones de sitios y aplicaciones de confianza para iniciar sin el aviso de confirmación. Esto agrega la capacidad de que los administradores configuren las combinaciones de protocolo de confianza/origen (como las aplicaciones de Microsoft 365) para que sus usuarios finales puedan suprimir el aviso de confirmación al navegar en una dirección URL que contenga un protocolo de aplicación.

- **Herramienta de resaltado para PDF**. Se puede agregar esta herramienta a la barra de herramientas para poder resaltar fácilmente el texto importante en los archivos PDF.

- **La API de acceso al almacenamiento está disponible**. Esta API permite acceder al almacenamiento de origen en un contexto de terceros en el que un usuario proporcione una forma directa para permitir el almacenamiento que, de otro modo, quedaría bloqueado por la configuración actual del explorador. Para obtener más información, consulte [API de acceso al almacenamiento](https://www.chromestatus.com/feature/5612590694662144).

- **El envío a OneNote está disponible para las Colecciones de Microsoft Edge**. Los usuarios están complacidos de poder enviar la información que hayan reunido en las Colecciones a OneNote, en donde pueden anexarla a un proyecto mayor y colaborar con otras personas. Y lo que es más importante, en Microsoft Edge 85, podrá enviar contenido a los productos de *Office para Mac* (Word, Excel y OneNote), tanto en la cuenta de Microsoft como en Azure Active Directory.

- **Actualizaciones de DevTools** Para obtener más información sobre las siguientes actualizaciones, consulte las [Novedades en DevTools (Microsoft Edge 85)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - Microsoft Edge DevTools admite la emulación de Surface Duo. Las DevTools de Microsoft Edge pueden emular Surface Duo para que pueda probar el aspecto que tendrá el contenido web en los dispositivos de pantalla doble. Para activar este experimento en DevTools, ingrese al Modo de dispositivo presionando Ctrl+Mayús+M en Windows o Comando+Mayús+M en macOS y seleccionando, a continuación, Surface Duo en la lista desplegable del dispositivo.
   - Microsoft Edge DevTools le permite hacer coincidir los métodos abreviados de teclado con el VS Code. Las DevTools de Microsoft Edge permiten personalizar los métodos abreviados de teclado en las DevTools para que coincidan con su editor/IDE. En Microsoft Edge 85, estamos agregando la capacidad de hacer coincidir los métodos abreviados del teclado de las DevTools con el VS Code. Este cambio ayudará a aumentar la productividad en VS Code y DevTools.

### Actualizaciones de directivas

#### Nuevas directivas

Se han agregado trece directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AutoLaunchProtocolsFromOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autolaunchprotocolsfromorigins): definir una lista de protocolos que puedan iniciar una aplicación externa desde los orígenes listados sin avisar al usuario.
- [AutoOpenAllowedForURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenallowedforurls): URL en donde AutoOpenFileTypes aplique.
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes): lista los tipos de archivo que se abrirán automáticamente al descargarse.
- [DefaultSearchProviderContextMenuAccessAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchprovidercontextmenuaccessallowed): permitir el acceso a la búsqueda del menú emergente del proveedor de búsquedas predeterminado.
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors): permitir certificados firmados usando SHA-1 cuando sean emitidos por anclajes de veracidad locales.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings): deshabilitar las advertencias basadas en la extensión del tipo de archivo de descarga para tipos de archivo especificados en los dominios.
- [IntensiveWakeUpThrottlingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intensivewakeupthrottlingenabled): controlar la característica IntensiveWakeUpThrottling.
- [NewTabPagePrerenderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageprerenderenabled): habilitar la carga previa de la nueva pestaña de la página para una representación más rápida.
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox): configurar la experiencia del cuadro de búsqueda de la nueva pestaña de la página.
- [PasswordMonitorAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordmonitorallowed): permitir que se alerte a los usuarios si se detecta que sus contraseñas no son seguras.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): habilitar el uso de copias itinerantes para los datos del perfil de Microsoft Edge.
- [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation): establecer el directorio del perfil móvil.
- [TLSCsipherSuiteDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tlsciphersuitedenylist): especificar los conjuntos de cifrado TLS para deshabilitarlos.

#### Directivas obsoletas

- [EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload): habilitar la descarga de las acciones del dominio desde Microsoft.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled): volver a habilitar la API de componentes web v0 hasta M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): permitir al controlador web invalidar las directivas obsoletas.

<!--- END 85 ---->

## Versión 84.0.522.63: 20 de agosto

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-20-2020).

## Versión 84.0.522.61: 17 de agosto

Se han corregido varios errores y problemas de rendimiento.

## Versión 84.0.522.59: 11 de agosto

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-11-2020)

## Versión 84.0.522.58: 10 de agosto

Se han corregido varios errores y problemas de rendimiento.

## Versión 84.0.522.52: 1 de agosto

Se han corregido varios errores y problemas de rendimiento.

## Versión 84.0.522.50: 31 de julio

Se han corregido varios errores y problemas de rendimiento.

## Versión 84.0.522.49: 29 de julio

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#july-29-2020)

## Versión 84.0.522.48: 28 de julio

Se han corregido varios errores y problemas de rendimiento.

## Versión 84.0.522.44: 23 de julio

Se han corregido varios errores y problemas de rendimiento.

<!-- Archived to version 84.0.522.40: July 16 -->

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
