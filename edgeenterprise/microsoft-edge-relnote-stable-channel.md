---
title: Notas de la versión de Microsoft Edge para el canal estable
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de la versión de Microsoft Edge para el canal estable
ms.openlocfilehash: 96525327c75231974e2e2976c1b811dee3a6b03e
ms.sourcegitcommit: 86e0de9b27ad4297a6d5a57c866d7ef4fc7bb0cd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400173"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Notas de la versión para el canal estable de Microsoft Edge

Estas notas de versión proporcionan información sobre las nuevas características y las actualizaciones no relacionadas con la seguridad que se incluyen en el canal estable de Microsoft Edge.

- Todas las actualizaciones de seguridad se muestran [aquí](microsoft-edge-relnotes-security.md).
- Las notas de la versión archivadas para el Canal estable de Microsoft Edge se encuentran [aquí](microsoft-edge-relnote-archive-stable-channel.md).

 Para entender los canales de Microsoft Edge, vea la [Información general sobre los canales de Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Para el Canal estable, las actualizaciones se implementarán de manera progresiva en uno o más días. Para más información, consulte [Implementaciones progresivas de actualizaciones de Microsoft Edge](microsoft-edge-update-progressive-rollout.md).

## <a name="version-89077448-march-8"></a>Versión 89.0.774.48: 8 de marzo

Se han corregido varios errores y problemas de rendimiento.

<!-- begin major 89 -->
## <a name="version-89077445-march-4"></a>Versión 89.0.774.45: 4 de marzo

> [!IMPORTANT]
> Esta actualización contiene [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166), que ha sido reportado por el equipo de Chromium como una vulnerabilidad de seguridad. Para más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide).

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-4-2021).

### <a name="resolved-issues"></a>Problemas resueltos

- **Correcciones y actualizaciones de los métodos abreviados del menú Inicio y la barra de tareas:**
  - Al hacer clic con el botón derecho en el acceso directo de Microsoft Edge en el menú Inicio, se mostrará correctamente la opción de desanclar Microsoft Edge de la barra de tareas cuando esté anclado.
  - Los diseños de inicio que incluyen una [configuración de barra de tareas](https://docs.microsoft.com/windows/configuration/configure-windows-10-taskbar) para anclar Microsoft Edge a la barra de tareas ya no crearán un segundo acceso directo de Microsoft Edge anclado a la barra de tareas.
  - Las organizaciones que usen perfiles de itinerancia de Windows ya no verán un icono en blanco en lugar del icono de Microsoft Edge en la barra de tareas cuando sus usuarios inicien sesión en Windows.

### <a name="feature-updates"></a>Actualizaciones de características

- **El modo de pantalla completa habilita funcionalidades de bloqueo adicionales**. Empezando por la versión 89 de Microsoft Edge, hemos agregado funcionalidades de bloqueo adicionales en el modo de pantalla completa para que los clientes puedan hacer el trabajo con una experiencia más productiva y segura. [Más información](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **La herramienta Enterprise Mode Site List Manager estará disponible en el explorador a través de la página *edge://compat***. Puede usar esta herramienta para crear, editar y exportar el XML de lista de sitios para el modo de Internet Explorer en Microsoft Edge. Puede habilitar el acceso a esta herramienta según sea necesario con la directiva de grupo. [Más información](https://docs.microsoft.com/deployedge/edge-ie-mode-site-list-manager).

- **Mejorar el rendimiento del explorador con pestañas en suspensión**. Las pestañas en suspensión mejoran el rendimiento del explorador al poner pestañas inactivas en reposo para liberar recursos del sistema, como la memoria y la CPU, de modo que las pestañas activas u otras aplicaciones puedan usarlos. Los usuarios pueden impedir que los sitios entren en suspensión y configurar el período de tiempo antes de que la pestaña inactiva se suspenda. Para mantener a los usuarios en su flujo, también se utiliza la [heurística](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) para evitar que determinados sitios pasen al modo suspensión, como los sitios de intranet. Esta característica se puede administrar con directivas de grupo.

- **Restablecer manualmente los datos de sincronización de Microsoft Edge en la nube**. Estamos incorporando un método para restablecer los datos de sincronización de Microsoft Edge desde el producto. Esto garantiza que los datos se eliminen de los servicios Microsoft, así como también resuelve ciertos problemas del producto que anteriormente requerían un vale de soporte técnico.

- **Habilitación inteligente del inicio de sesión único (SSO) para todas las cuentas Windows Azure Active Directory (Azure AD) para usuarios con un único perfil de Microsoft Edge que no sea de Azure AD**.  Activa automáticamente esta configuración para los usuarios que podrían beneficiarse más de esta característica. Si un usuario solo tiene un perfil de Microsoft Edge (y no es de Azure AD o el Modo Niños), la configuración se activa automáticamente cuando se inicie Microsoft Edge. Esta alternancia automática también se desactivará automáticamente si más adelante un usuario decide iniciar sesión en un perfil de Microsoft Edge diferente con una cuenta de Azure AD. Los usuarios pueden actualizar manualmente sus preferencias para esta característica en **Configuración > Perfiles >Preferencias de perfil > Permitir el inicio de sesión único para sitios profesionales o educativos con este perfil**.

- **Mejoras en la experiencia de selección de texto en documentos PDF**. Los usuarios obtendrán una experiencia de selección de texto coherente y más fluida en todos los documentos PDF abiertos en Microsoft Edge a partir de la versión 89.

- **El campo Fecha de nacimiento ahora es compatible con la función Autorrellenar.** Actualmente, Microsoft Edge le ayuda a ahorrar tiempo y esfuerzo al rellenar formularios y crear cuentas en línea rellenando automáticamente los datos como direcciones, nombres, números de teléfono, etc. Empezando por la versión 89 de Microsoft Edge, agregamos compatibilidad con otro campo que puede guardar y rellenar automáticamente: la fecha de nacimiento. Puede ver, editar y eliminar esta información en cualquier momento en la configuración de su perfil.

### <a name="policy-updates"></a>Actualizaciones de directiva

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado siete directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se han agregado las siguientes directivas nuevas.

- [BrowsingDataLifetime](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsingdatalifetime): configuración de la duración de los datos de exploración
- [MAMEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#mamenabled): administración de aplicaciones móviles habilitada
- [DefinePreferredLanguages](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#definepreferredlanguages): define una lista ordenada de idiomas preferidos que los sitios web deben mostrar si el sitio admite el idioma
- [ShowRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showrecommendationsenabled): permite las recomendaciones y notificaciones promocionales de Microsoft Edge
- [PrintingAllowedBackgroundsModesModes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingallowedbackgroundgraphicsmodes): restringe el modo de impresión de gráficos de fondo
- [PrintingBackgroundGraphicsDefault](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingbackgroundgraphicsdefault): modo de impresión de gráficos de fondo predeterminados
- [SmartActionsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartactionsblocklist): bloquea acciones inteligentes de una lista de servicios

#### <a name="obsoleted-policies"></a>Directivas obsoletas

Las siguientes directivas están obsoletas.

- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy): usa una directiva de referencia predeterminada de no-referrer-when-downgrade
- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): habilita el uso y los informes de datos relacionados con bloqueos
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): envía información de sitios para mejorar los servicios Microsoft
<!-- end major 89 -->
## <a name="version-88070581-february-25"></a>Versión 88.0.705.81: 25 de febrero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070574-february-17"></a>Versión 88.0.705.74: 17 de febrero

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-17-2021).

## <a name="version-88070568-february-11"></a>Versión 88.0.705.68: 11 de febrero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070563-february-5"></a>Versión 88.0.705.63: 5 de febrero

> [!IMPORTANT]
> Esta actualización contiene [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148), que ha sido reportado por el equipo de Chromium como una vulnerabilidad de seguridad.

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-5-2021).

## <a name="version-88070562-february-4"></a>Versión 88.0.705.62: 4 de febrero

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-4-2021).

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070556-january-28"></a>Versión 88.0.705.56: 28 de enero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070553-january-26"></a>Versión 88.0.705.53: 26 de enero

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-88070550-january-21"></a>Versión 88.0.705.50: 21 de enero

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-21-2021).

<!--- begin major 88  --->
### <a name="feature-updates"></a>Actualizaciones de características

- **Desusos:**

  - Desusar la compatibilidad con el protocolo FTP. Se ha quitado la compatibilidad con el protocolo FTP heredado de MicrosoftEdge. Si se intenta navegar a un vínculo FTP, el explorador dirigirá el sistema operativo para que abra una aplicación externa para controlar el vínculo FTP. Como alternativa, los administradores de TI pueden configurar MicrosoftEdge para usar el modo IE para los sitios que dependen del protocolo FTP.
  - La compatibilidad con AdobeFlash se eliminará. A partir de la versión88 de Microsoft Edge Beta, se eliminarán la funcionalidad y la compatibilidad con Adobe Flash. Más información: [actualización sobre la finalización del soporte en Adobe Flash Player: blog de MicrosoftEdge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Autenticación:**

  - El inicio de sesión único (SSO) ya está disponible para las cuentas de Azure Active Directory (Azure AD) y las cuentas de Microsoft (MSA) en versiones de Windows de nivel inferior. Un usuario que haya iniciado sesión en Microsoft Edge en una versión de Microsoft Windows de nivel inferior (versiones 7 y 8.1) ahora tendrá la sesión iniciada de manera automática en los sitios web que estén configurados para permitir el inicio de sesión único con cuentas profesionales y de Microsoft (por ejemplo, bing.com, office.com, msn.com, outlook.com).<br>Nota: es posible que un usuario tenga que cerrar sesión y volver a iniciarla si ha iniciado sesión en Microsoft Edge en una versión anterior a Microsoft Edge 88 para poder aprovechar esta característica.
  
  - Inicio de sesión único (SSO) para trabajar en sitios con cualquier cuenta de Windows Azure Active Directory (Azure AD) que esté en el sistema en perfiles de Microsoft Edge que no sean de Azure AD. Esta característica se puede habilitar para cualquier perfil que no haya iniciado sesión con una cuenta de trabajo o escuela y que no sea invitado o privado, y permite el uso de cualquier cuenta de trabajo o escuela que haya iniciado sesión en el sistema operativo con ese perfil. Esta característica se puede definir en **Configuración** > **Perfiles** > **Preferencias de perfil** > **Permitir el inicio de sesión único en sitios profesionales o educativos con este perfil o**.
  
    > [!NOTE]
    > "Inicio de sesión único (SSO) para todas las cuentas de Windows que usan el perfil de Microsoft Edge" es una actualización de las notas de la versión del 21 de enero.

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

- **Mejorar la velocidad de inicio de Microsoft Edge con el aumento de inicio.** Para mejorar la velocidad de inicio de Microsoft Edge, hemos desarrollado una característica denominada aumento de inicio. El aumento de inicio hace que Microsoft Edge se inicie más rápido al habilitar Microsoft Edge para que se ejecute en segundo plano. Nota: esta característica está limitada a un grupo de usuarios seleccionado aleatoriamente que han habilitado la experimentación. Estos usuarios proporcionan comentarios al equipo de características.

- **Productividad:**

  - Mejorar la productividad y la multitarea con pestañas verticales. A medida que el número de pestañas horizontales crece, los títulos de sitios comienzan a cortarse y los controles de pestaña se pierden a medida que se reducen las pestañas. Esto interrumpe el flujo de trabajo del usuario, ya que dedica más tiempo a buscar, cambiar y administrar sus pestañas, y menos tiempo a la tarea. Las pestañas verticales permiten a los usuarios mover sus pestañas al costado, donde los iconos alineados verticalmente y los títulos de sitio más largos hacen que sea más fácil digitalizar, identificar y cambiar a la pestaña que quiera abrir rápidamente.
  - Rellene automáticamente el campo de fecha de nacimiento. Microsoft Edge ya ayuda a ahorrar tiempo y esfuerzo mientras rellenas formularios y crea cuentas en línea mediante el rellenado automático de datos de usuario, como direcciones, nombres, números de teléfono, etc. Microsoft Edge ahora es compatible con el campo de fecha de nacimiento que los usuarios pueden guardar y rellenar automáticamente. Un usuario puede ver, editar y eliminar esta información en cualquier momento en la configuración de su perfil.
  - Mejoras en el historial de Cerrados recientemente. Cerrados recientemente ahora mantiene las últimas 25pestañas y ventanas de cualquier sesión de exploración pasada en lugar de solo la sesión anterior. Los usuarios pueden seleccionar Cerrados recientemente en la nueva experiencia de historial para ver todas las pestañas que estaban abiertas.
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

- [BasicAuthOverHttpEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#basicauthoverhttpenabled): permite la autenticación básica para HTTP.
- [BlockExternalExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#blockexternalextensions): bloquea las extensiones externas para que no se instalen.
- [InternetExplorerIntegrationLocalFileAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileallowed): permite el inicio de archivos locales en el modo de Internet Explorer.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist): abre archivos locales en la lista de permiso de extensión de archivos en el modo de Internet Explorer.
- [InternetExplorerIntegrationLocalFileShowContextMenu](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileshowcontextmenu): muestra el menú contextual para abrir un vínculo en el modo de Internet Explorer.
- [IntranetRedirectBehavior](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intranetredirectbehavior): comportamiento de redirección de intranet.
- [PrinterTypeDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printertypedenylist): deshabilita los tipos de impresora en la lista de denegación.
- [ShowMicrosoftRewards](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showmicrosoftrewards): muestra las experiencias de Microsoft Rewards.
- [SleepingTabsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsenabled): configura las pestañas en suspensión.
- [SleepingTabsTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabstimeout): establece el tiempo de suspensión de la pestaña en segundo plano para las pestañas en suspensión.
- [SleepingTabsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsblockedforurls): bloquea las pestañas en suspensión en sitios específicos.
- [StartupBoostEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#startupboostenabled): habilita el aumento de inicio.
- [TargetBlankImpliesNoOpener:](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#targetblankimpliesnoopener) evita establecer window.opener para vínculos destinados a _blank.
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride): especifica cómo Microsoft Edge Update controla las actualizaciones disponibles de Microsoft Edge.
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed): configura la disponibilidad de un diseño vertical para pestañas en el lateral del explorador.
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols): permite la degradación de TLS/DTLS heredada en WebRTC.
- [WebWidgetAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetallowed): habilita el widget Web.
- [WebWidgetIsEnabledOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetisenabledonstartup): permite el widget web en el inicio de Windows.

#### <a name="deprecated-policies"></a>Directivas obsoletas

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled): habilita la autenticación proactiva.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist): configura las reglas de omisión de proxy.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode): configura la configuración del servidor proxy.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl): establece la dirección URL del archivo proxy .pac.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver): configura la dirección o URL del servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): permite que WebDriver reemplace las directivas incompatibles.

### <a name="obsoleted-policies"></a>Directivas obsoletas

- [AllowPopupsDuringPageUnload:](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowpopupsduringpageunload) permite que una página muestre elementos emergentes durante su descarga.
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting): configuración predeterminada de Adobe Flash.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls): permite el complemento Adobe Flash en sitios específicos.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls): bloquea el complemento Adobe Flash en sitios específicos.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode): amplía la configuración de contenido de Adobe Flash a todo el contenido.
<!--- end major 88  --->
## <a name="version-87066475-january-7"></a>Versión 87.0.664.75: 7 de enero

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-7-2021).

## <a name="version-87066466-december-17"></a>Versión 87.0.664.66: 17 de diciembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066460-december-10"></a>Version 87.0.664.60: 10 de diciembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066457-december-7"></a>Versión 87.0.664.57: 7 de diciembre

Se han corregido varios errores y problemas de rendimiento. Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#december-7-2020).

## <a name="version-87066455-december-3"></a>Versión 87.0.664.55: 3 de diciembre

Se han corregido varios errores y problemas de rendimiento. La siguiente característica se actualizó para esta versión.

- La **opción compras está habilitada de forma predeterminada**. A partir de la versión 87 de Microsoft Edge, los usuarios empresariales pueden beneficiarse de la compra en Microsoft Edge. Con las características de compra, Microsoft Edge ayuda a los usuarios a buscar cupones y mejores precios mientras compras en Internet. (La experiencia del cupón se presentó con la versión estable de 87.0.664.41). La experiencia de comparación de precios ahora está disponible con esta actualización. Esta característica se puede configurar con la directiva [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled). Consulte nuestro [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) y [Obtenga más información](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) sobre Compras de Microsoft.

## <a name="version-87066452-november-30"></a>Versión 87.0.664.52: 30 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-87066447-november-23"></a>Versión 87.0.664.47: 23 de noviembre

Se han corregido varios errores y problemas de rendimiento.

<!-- begin major 87 --->
## <a name="version-87066441-november-19"></a>Versión 87.0.664.41: 19 de noviembre

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-19-2020).

### <a name="feature-updates"></a>Actualizaciones de características

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

### <a name="policy-updates"></a>Actualizaciones de directivas

#### <a name="new-policies"></a>Nuevas directivas

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

#### <a name="deprecated-policy"></a>Directivas en desuso

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype): Configura la experiencia de la página de pestaña nueva de Microsoft Edge.

#### <a name="obsoleted-policy"></a>Directiva obsoleta

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures): vuelve a habilitar las características de la plataforma web en desuso por un tiempo limitado.

<!-- end major 87 -->

## <a name="version-86062269-november-13"></a>Versión 86.0.622.69: 13 de noviembre

> [!IMPORTANT]
> Esta actualización contiene [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) y [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), que han sido reportados por el equipo de Chromium como una vulnerabilidad de seguridad.

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-13-2020).

## <a name="version-86062268-november-11"></a>Versión 86.0.622.68: 11 de noviembre

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-11-2020).

## <a name="version-86062263-november-4"></a>Versión 86.0.622.63: 4 de noviembre

> [!IMPORTANT]
> Esta actualización contiene [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), que ha sido reportado por el equipo de Chromium como una vulnerabilidad de seguridad.

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-4-2020).

## <a name="version-86062261-november-2"></a>Versión 86.0.622.61: 2 de noviembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-86062258-october-29"></a>Versión 86.0.622.58: 29 de octubre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-86062256-october-27"></a>Versión 86.0.622.56: 27 de octubre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-86062251-october-22"></a>Versión 86.0.622.51: 22 de octubre

Las actualizaciones de seguridad del canal estable se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-22-2020).

## <a name="version-86062248-october-20"></a>Versión 86.0.622.48: 20 de octubre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-86062243-october-15"></a>Versión 86.0.622.43: 15 de octubre

Se han corregido varios errores y problemas de rendimiento.

<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
