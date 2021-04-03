---
title: Notas de la versión de Microsoft Edge para el canal beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 04/02/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de la versión de Microsoft Edge para el canal beta
ms.openlocfilehash: da33ab8a97ede1691a5b3ba3172169613504626b
ms.sourcegitcommit: c09ad05d137103604bf7bd7c8d06901e9d15f76c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "11474943"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de la versión para el canal beta de Microsoft Edge

Estas notas de versión proporcionan información sobre las nuevas características y las actualizaciones no relacionadas con la seguridad que se incluyen en el canal beta de Microsoft Edge. Las versiones archivadas de estas notas de la versión están [aquí](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Hemos actualizado la nota de la [versión 89.0.774.18: 3 de febrero](#version-89077418-february-3) de Microsoft Edge Beta para reflejar las características que han llegado.

## <a name="version-90081827-april-2"></a>Versión 90.0.818.27: 2 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081822-march-29"></a>Versión 90.0.818.22: 29 de marzo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081814-march-22"></a>Versión 90.0.818.14: 22 de marzo

Se han corregido varios errores y problemas de rendimiento.
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>Versión 90.0.818.8: 16 de marzo

### <a name="feature-updates"></a>Actualizaciones de características

- **El inicio de sesión único (SSO) ya está disponible para las cuentas de Azure Active Directory (AzureAD) y las cuentas de Microsoft (MSA) en macOS.** Un usuario que haya iniciado sesión en MicrosoftEdge en macOS ahora tendrá la sesión iniciada de manera automática en los sitios web que estén configurados para permitir el inicio de sesión único con cuentas profesionales y de Microsoft (por ejemplo, bing.com, office.com, msn.com y outlook.com).

- **Impresión:**

  - **Modo de rasterización de impresión nuevo para las impresoras que no son PostScript**. A partir de la versión 90 de Microsoft Edge, los administradores pueden usar una nueva directiva para definir el modo de rasterización de impresión para sus usuarios. Esta directiva controla la forma en que Microsoft Edge imprime en impresoras que no sean PostScript en Windows.  En ocasiones, es necesario rasterizar los trabajos de impresión de impresoras que no sean PostScript para que se impriman correctamente. Las opciones de impresión son Completa y Rápida.

  - **Opciones de escala de página adicionales para la impresión**. Los usuarios ahora pueden personalizar el ajuste de escala al imprimir páginas web y documentos PDF con opciones adicionales. La opción "Ajustar a la página" garantiza que la página web o el documento se ajusta al espacio disponible en el "Tamaño de papel" seleccionado para la impresión. La opción "Tamaño real" garantiza que no se imprima ningún cambio en el tamaño del contenido, independientemente de la opción "Tamaño de papel" seleccionada.

- **Productividad:**

  - **Las sugerencias de Autorrellenar se extienden para incluir contenido de campos de dirección del portapapeles**. El contenido del Portapapeles se analiza cuando hace clic en un campo de perfil o dirección (por ejemplo, teléfono, correo electrónico, código postal, ciudad, estado, etc.) para mostrarlo como sugerencias de autorrelleno.

  - **Los usuarios pueden buscar sugerencias de autorrellenar incluso si no se detecta un formulario o campo**. Ahora, si tiene guardada la información en Microsoft Edge, las sugerencias de autorrelleno aparecerán automáticamente y le ayudarán a ahorrar tiempo al rellenar formularios. En casos en los que autorrellenar no encuentra un formulario, o si quiere capturar datos en formularios que normalmente no tienen autorrellenar (como formularios temporales), puede buscar la información con autorrellenar.

- **Descarga de Access desde un control flotante de la barra de menús**. Las descargas se mostrarán en la esquina superior derecha con todas las descargas activas en un solo lugar. Este menú se puede descartar fácilmente para que los usuarios puedan continuar explorando sin interrupciones y pueden supervisar el progreso de descarga general directamente desde la barra de herramientas. [Más información](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

- **Mejoras en la representación de fuentes**. Empezando por la versión 90 de Microsoft Edge, hemos realizado mejoras en la representación de texto para mejorar la claridad y reducir el efecto borroso. Parte de las mejoras en la representación de fuentes llegarán en la versión beta 90, pero están deshabilitadas de forma predeterminada.


### <a name="policy-updates"></a>Actualizaciones de directiva

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado siete directivas nuevas. Descargue las Plantillas administrativas actualizadas desde la [página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se agregaron las siguientes directivas nuevas:

- [ApplicationGuardFavoritesSyncEnabled](./microsoft-edge-policies.md#applicationguardfavoritessyncenabled): sincronización de favoritos de Protección de aplicaciones habilitada
- [ManagedConfigurationPerOrigin](./microsoft-edge-policies.md#managedconfigurationperorigin): establece valores de configuración administrados para sitios web de orígenes específicos.
- [PrintRasterizationMode](./microsoft-edge-policies.md#printrasterizationmode): modo de rasterización de impresión
- [QuickViewOfficeFilesEnabled](./microsoft-edge-policies.md#quickviewofficefilesenabled): administrar la funcionalidad de archivos de Office QuickView en Microsoft Edge
- [SSLErrorOverrideAllowedForOrigins](./microsoft-edge-policies.md#sslerroroverrideallowedfororigins): permitir a los usuarios continuar desde la página de advertencia HTTPS de orígenes específicos
- [WindowOcclusionEnabled](./microsoft-edge-policies.md#windowocclusionenabled): habilitar la ocultación de ventanas
- [WindowsHelloForHTTPAuthEnabled](./microsoft-edge-policies.md#windowshelloforhttpauthenabled): Windows Hello para autenticación HTTP habilitado

#### <a name="deprecated-policies"></a>Directivas en desuso

- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled): habilitar la ocultación de ventanas nativas
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin): versión mínima de TLS habilitada
<!-- end major 90 -->

## <a name="version-89077454-march-13"></a>Versión 89.0.774.54: 13 de marzo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077450-march-10"></a>Versión 89.0.774.50: 10 de marzo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077448-march-8"></a>Versión 89.0.774.48: 8 de marzo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077445-march-3"></a>Versión 89.0.774.45: 3 de marzo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077439-february-26"></a>Versión 89.0.774.39: 26 de febrero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077434-february-22"></a>Versión 89.0.774.34: 22 de febrero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077427-february-12"></a>Versión 89.0.774.27: 12 de febrero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077423-february-8"></a>Versión 89.0.774.23: 8 de febrero

Se han corregido varios errores y problemas de rendimiento.

<!-- begin major 89 -->
## <a name="version-89077418-february-3"></a>Versión 89.0.774.18: 3 de febrero

### <a name="feature-updates"></a>Actualizaciones de características

- **El modo de pantalla completa habilita funcionalidades de bloqueo adicionales**. Empezando por la versión 89 de Microsoft Edge, hemos agregado funcionalidades de bloqueo adicionales en el modo de pantalla completa para que los clientes puedan hacer el trabajo con una experiencia más productiva y segura. [Más información](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **La herramienta Enterprise Mode Site List Manager estará disponible en el explorador a través de la página *edge://compat***. Puede usar esta herramienta para crear, editar y exportar el XML de lista de sitios para el modo de Internet Explorer en Microsoft Edge. Puede habilitar el acceso a esta herramienta según sea necesario con la directiva de grupo. [Más información](./edge-ie-mode-site-list-manager.md).

- **Mejorar el rendimiento del explorador con pestañas en suspensión**. Las pestañas en suspensión mejoran el rendimiento del explorador al poner pestañas inactivas en reposo para liberar recursos del sistema, como la memoria y la CPU, de modo que las pestañas activas u otras aplicaciones puedan usarlos. Los usuarios pueden impedir que los sitios entren en suspensión y configurar el período de tiempo antes de que la pestaña inactiva se suspenda. Para mantener a los usuarios en su flujo, también se utiliza la [heurística](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) para evitar que determinados sitios pasen al modo suspensión, como los sitios de intranet. Esta característica se puede administrar con directivas de grupo.

  > [!NOTE]
  > "Mejorar el rendimiento del explorador con pestañas en suspensión" es una actualización de las notas de la versión del 3 de febrero para la versión principal 89.0.774.18.

- **Restablecer manualmente los datos de sincronización de Microsoft Edge en la nube**. Estamos incorporando un método para restablecer los datos de sincronización de Microsoft Edge desde el producto. Esto garantiza que los datos se eliminen de los servicios Microsoft, así como también resuelve ciertos problemas del producto que anteriormente requerían un vale de soporte técnico.

- **Mejoras en la experiencia de selección de texto en documentos PDF**. Los usuarios obtendrán una experiencia de selección de texto coherente y más fluida en todos los documentos PDF abiertos en Microsoft Edge a partir de la versión 89.

- **El campo Fecha de nacimiento ahora es compatible con la función Autorrellenar.** Actualmente, Microsoft Edge le ayuda a ahorrar tiempo y esfuerzo al rellenar formularios y crear cuentas en línea rellenando automáticamente los datos como direcciones, nombres, números de teléfono, etc. Empezando por la versión 89 de Microsoft Edge, agregamos compatibilidad con otro campo que puede guardar y rellenar automáticamente: la fecha de nacimiento. Puede ver, editar y eliminar esta información en cualquier momento en la configuración de su perfil.

- **Compatibilidad con la búsqueda en lenguaje natural en la barra de direcciones, la página de búsqueda de historial y el centro del historial**. Comenzando por la versión 89 de Microsoft Edge, la búsqueda de un artículo o sitio web le será más fácil con la búsqueda en lenguaje natural en la barra de direcciones, la página de historial y el centro del historial. Los usuarios pueden buscar contenido, descripción e intervalos de tiempo de páginas visualizadas previamente (por ejemplo, "receta de pastel de la semana pasada") además de coincidencias de palabras clave del título o la URL. Esta característica se limita a un grupo de usuarios seleccionados al azar que han permitido la experimentación. Estos usuarios proporcionan comentarios al equipo de características.

### <a name="policy-updates"></a>Actualizaciones de directiva

#### <a name="new-policies"></a>Nuevas directivas

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime): configuración de la duración de los datos de exploración
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled): administración de aplicaciones móviles habilitada
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages): define una lista ordenada de idiomas preferidos que los sitios web deben mostrar si el sitio admite el idioma
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled): permite las recomendaciones y notificaciones promocionales de Microsoft Edge
- [PrintingAllowedBackgroundsModesModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes): restringe el modo de impresión de gráficos de fondo
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault): modo de impresión de gráficos de fondo predeterminados
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist): bloquea acciones inteligentes de una lista de servicios

#### <a name="obsoleted-policies"></a>Directivas obsoletas

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): usa una directiva de referrer predeterminada de no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled): habilita el uso y los informes de datos relacionados con bloqueos
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices): envía información de sitios para mejorar los servicios Microsoft
<!-- end major 89 -->

## <a name="version-88070556-january-29"></a>Versión 88.0.705.56: 29 de enero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070549-january-20"></a>Versión 88.0.705.49: 20 de enero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070545-january-15"></a>Versión 88.0.705.45: 15 de enero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070541-january-11"></a>Versión 88.0.705.41: 11 de enero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070529-december-21"></a>Versión 88.0.705.29: 21 de diciembre

Se han corregido varios errores y problemas de rendimiento.

<!-- begin major 88 -->
## <a name="version-88070518-december-9"></a>Versión 88.0.705.18: 9 de diciembre

### <a name="feature-updates"></a>Actualizaciones de características

- **Desusos:**

  - Desusar la compatibilidad con el protocolo FTP. Se ha quitado la compatibilidad con el protocolo FTP heredado de MicrosoftEdge. Si se intenta navegar a un vínculo FTP, el explorador dirigirá el sistema operativo para que abra una aplicación externa para controlar el vínculo FTP. Como alternativa, los administradores de TI pueden configurar MicrosoftEdge para usar el modo IE para los sitios que dependen del protocolo FTP.
  - La compatibilidad con AdobeFlash se eliminará. A partir de la versión88 de Microsoft Edge Beta, se eliminarán la funcionalidad y la compatibilidad con Adobe Flash. Más información: [actualización sobre la finalización del soporte en Adobe Flash Player: blog de MicrosoftEdge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Autenticación:**

  - El inicio de sesión único (SSO) ya está disponible para las cuentas de Azure Active Directory (Azure AD) y las cuentas de Microsoft (MSA) en macOS y versiones de Windows de nivel inferior. Un usuario que haya iniciado sesión en Microsoft Edge en una versión de Microsoft Windows de nivel inferior (versiones 7 y 8.1) ahora tendrá la sesión iniciada automáticamente en los sitios web que estén configurados para permitir el inicio de sesión único con cuentas profesionales y Microsoft (por ejemplo, bing.com, office.com, msn.com, outlook.com).<br>Nota: es posible que un usuario tenga que cerrar sesión y volver a iniciarla si ha iniciado sesión en Microsoft Edge en una versión anterior a Microsoft Edge 88 para poder aprovechar esta característica.
  - Cambie automáticamente los usuarios en macOS a su perfil de trabajo para los sitios que se autentican con su cuenta profesional. A partir de la versión 88 de Microsoft Edge, ofrecemos la posibilidad de cambiar los sitios que se autentican con el perfil de trabajo de un usuario en macOS.<br>Nota: es posible que un usuario tenga que cerrar sesión y volver a iniciarla si ha iniciado sesión en Microsoft Edge en una versión anterior a Microsoft Edge 88 para poder aprovechar esta característica.

- **Opción de modo de pantalla completa para finalizar la sesión**. El botón "Finalizar sesión" ahora está disponible en una experiencia de navegación pública en modo de pantalla completa. Esta característica garantiza que los datos y la configuración del explorador se eliminen cuando se cierra Microsoft Edge. Más información sobre las características y la guía básica del modo de pantalla completa, [Configurar el modo de pantalla completa de Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md).

- **Seguridad y privacidad:**

  - Se generan alertas si se encuentra la contraseña de un usuario en una filtración en línea. Las contraseñas de usuario se comprueban con un repositorio de credenciales infringidas y se envía una alerta al usuario si se encuentra una coincidencia. Para garantizar la seguridad y la privacidad, las contraseñas de los usuarios se dividen y cifran cuando se comparan con la base de datos de credenciales filtradas.
  - Actualice automáticamente el contenido mixto. Las páginas seguras que se proporcionan a través de HTTPS pueden contener imágenes de referencias que se sirven a través de HTTP no seguro. Para mejorar la privacidad y la seguridad en Microsoft Edge 88, esas imágenes se recuperarán a través de HTTPS. Si la imagen no está disponible a través de HTTPS, no se cargará.
  - Vea permisos de sitio por sitio y por actividad reciente. A partir de Microsoft Edge 88, los usuarios podrán administrar los permisos de los sitios más fácilmente. Podrán ver los permisos por sitio web en lugar de solo por tipo de permiso. Además, hemos agregado una sección de actividades recientes que le mostrará al usuario todos los cambios recientes en los permisos de su sitio.
  - Más controles para las cookies del explorador. A partir de Microsoft Edge 88, los usuarios pueden eliminar cookies de terceros sin que esto afecte a las cookies principales. Además, los usuarios podrán filtrar las cookies según si son principales o de terceros y ordenar por nombre, número de cookies y la cantidad de datos almacenados y modificados por última vez.

- **Rendimiento:**

  - Mejore el rendimiento del explorador con pestañas en suspensión. Las pestañas en suspensión mejoran el rendimiento del explorador al poner pestañas inactivas en reposo para liberar recursos del sistema, como la memoria y la CPU, de modo que las pestañas activas u otras aplicaciones puedan usarlos. Los usuarios pueden impedir que los sitios entren en suspensión y configurar el período de tiempo antes de que la pestaña inactiva se suspenda. Para mantener a los usuarios en su flujo, también se utiliza la heurística para evitar que determinados sitios pasen al modo de suspensión, como los sitios de la intranet. Esta característica se limita a un grupo de usuarios seleccionados al azar que han permitido la experimentación. Planeamos tener la función de pestañas flotantes activada de forma predeterminada en Microsoft Edge versión 89. Esta característica se puede administrar con directivas de grupo.
  - Mejore la velocidad de inicio de Microsoft Edge con el aumento de inicio. Para mejorar la velocidad de inicio de Microsoft Edge, hemos desarrollado una característica denominada aumento de inicio. El aumento de inicio hace que Microsoft Edge se inicie más rápido al habilitar Microsoft Edge para que se ejecute en segundo plano. Nota: esta característica está limitada a un grupo de usuarios seleccionado aleatoriamente que han habilitado la experimentación. Estos usuarios proporcionan comentarios al equipo de características.

- **Productividad:**

  - Mejorar la productividad y la multitarea con pestañas verticales. A medida que el número de pestañas horizontales crece, los títulos de sitios comienzan a cortarse y los controles de pestaña se pierden a medida que se reducen las pestañas. Esto interrumpe el flujo de trabajo del usuario, ya que dedica más tiempo a buscar, cambiar y administrar sus pestañas, y menos tiempo a la tarea. Las pestañas verticales permiten a los usuarios mover sus pestañas al costado, donde los iconos alineados verticalmente y los títulos de sitio más largos hacen que sea más fácil digitalizar, identificar y cambiar a la pestaña que quiera abrir rápidamente.
  - Rellene automáticamente el campo de fecha de nacimiento. Microsoft Edge ya ayuda a ahorrar tiempo y esfuerzo mientras rellenas formularios y crea cuentas en línea mediante el rellenado automático de datos de usuario, como direcciones, nombres, números de teléfono, etc. Microsoft Edge ahora es compatible con el campo de fecha de nacimiento que los usuarios pueden guardar y rellenar automáticamente. Un usuario puede ver, editar y eliminar esta información en cualquier momento en la configuración de su perfil.
  - Mejoras en el historial de Cerrados recientemente. Cerrados recientemente ahora mantiene las últimas 25pestañas y ventanas de cualquier sesión de exploración pasada en lugar de solo la sesión anterior. Los usuarios pueden seleccionar Cerrados recientemente en la nueva experiencia de historial para ver todas las pestañas que estaban abiertas.
  - La función "Tu día de un vistazo" está activada de forma predeterminada. A partir de la versión 88 de Microsoft Edge, los trabajadores de la información pueden beneficiarse de las características de productividad inteligente en su nueva página de pestañas (NTP). Ofrecemos a los usuarios que han iniciado sesión con su cuenta profesional o educativa, contenido personalizado y relevante por medio de su M365 Graph. Los usuarios pueden examinar rápidamente sus módulos "Tu día de un vistazo" para realizar un seguimiento sencillo de las reuniones y del trabajo reciente, así como iniciar rápidamente las aplicaciones que quiera usar.

- **PDF:**

  - Presentación de documentos PDF en la vista de libro (dos páginas). A partir de la versión 88 de Microsoft Edge, los usuarios pueden ver documentos PDF en una sola página o en la vista de libro de dos páginas. Para cambiar la vista, haga clic en el botón **Vista de página** de la barra de herramientas.
  - Compatibilidad con notas de texto anclado para archivos PDF. A partir de la versión 87 de Microsoft Edge, los usuarios pueden agregar notas de texto escrito a cualquier parte del texto en archivos PDF.
  - Experiencia de selección de texto más fluida en documentos PDF. Los usuarios obtendrán una experiencia de selección de texto coherente y más fluida en todos los documentos PDF abiertos en Microsoft Edge.
  - Vea las páginas web guardadas como archivos PDF en la barra de Descargas. Ahora los usuarios pueden ver los archivos PDF generados configurando "Guardar como PDF" como el destino de la impresora para las páginas web en la barra de Descargas.

- **Fuentes:**

  - Los iconos del explorador se actualizan en el sistema de diseño Fluent. Como parte de nuestro trabajo constante en torno a Fluent Design en el explorador, hemos realizado cambios para alinear los iconos con el nuevo sistema de iconos de Microsoft. Estos cambios afectarán a numerosas interfaces de usuario con un alto nivel de función táctil, como pestañas, barra de direcciones, iconos de navegación y orientación, que se encuentran en los distintos menús.
  - Representación de fuentes mejorada. La representación de texto se ha mejorado para mejorar la claridad y para reducir el efecto borroso.

### <a name="policy-updates"></a>Actualizaciones de directivas

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado dieciséis directivas nuevas. Descargue las Plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se han agregado las siguientes directivas nuevas.

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
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled): habilita el aumento de inicio.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride): especifica cómo Microsoft Edge Update controla las actualizaciones disponibles de Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed): configura la disponibilidad de un diseño vertical para pestañas en el lateral del explorador.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols): permite la degradación de TLS/DTLS heredada en WebRTC.

#### <a name="deprecated-policies"></a>Directivas en desuso

Las siguientes directivas están en desuso.

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled): habilita la autenticación proactiva.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist): configura las reglas de omisión de proxy.
- [ProxyMode](./microsoft-edge-policies.md#proxymode): configura la configuración del servidor proxy.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl): establece la dirección URL del archivo proxy .pac.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver): configura la dirección o URL del servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies): permite a WebDriver reemplazar las directivas incompatibles.

#### <a name="obsoleted-policies"></a>Directivas obsoletas

Las siguientes directivas están obsoletas.

- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting): configuración predeterminada de Adobe Flash.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls): permite el complemento Adobe Flash en sitios específicos.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls): bloquea el complemento Adobe Flash en sitios específicos.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode): amplía la configuración de contenido de Adobe Flash a todo el contenido.

<!-- end major 88 -->

## <a name="version-87066455-december-3"></a>Versión 87.0.664.55: 3 de diciembre

Se han corregido varios errores y problemas de rendimiento. La siguiente característica nueva es compatible con esta versión.

- **Se generan alertas si se encuentra la contraseña de un usuario en una filtración en línea**. Las contraseñas de usuario se comprueban con un repositorio de credenciales infringidas y se envía una alerta al usuario si se encuentra una coincidencia. Para garantizar la seguridad y la privacidad, las contraseñas de los usuarios se dividen y cifran cuando se comparan con la base de datos de credenciales filtradas.

## <a name="version-87066452-november-30"></a>Versión 87.0.664.52: 30 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066440-november-18"></a>Versión87.0.664.40: 18 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066436-november-16"></a>Versión87.0.664.36: 16 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066430-november-9"></a>Versión 87.0.664.30: 9 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066424-november-2"></a>Versión 87.0.664.24: 2 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066418-october-26"></a>Versión 87.0.664.18: 26 de octubre

Se han corregido varios errores y problemas de rendimiento.

<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)