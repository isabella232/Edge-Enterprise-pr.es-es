---
title: Notas de la versión archivadas para el canal de Microsoft Edge Beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 02/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de la versión archivadas para el canal de Microsoft Edge Beta
ms.openlocfilehash: d15b1e9596f97ae5f88d0ed473e0abb0b37f3612
ms.sourcegitcommit: 231727b0f42bc0b7af49cb3290692aa7e420502a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "11312900"
---
# Notas de la versión archivadas para el canal de Microsoft Edge Beta

Estas notas de versión proporcionan información sobre las nuevas características y las actualizaciones no relacionadas con la seguridad que se incluyen en el canal de Microsoft Edge Beta. Para entender los canales de Microsoft Edge, vea la [Información general sobre los canales de Microsoft Edge](microsoft-edge-channels.md). Todas las actualizaciones de seguridad se muestran [aquí](microsoft-edge-relnotes-security.md).

<!-- major 86 -->
## Versión 86.0.622.11: 9 de septiembre

### Actualizaciones de características

* **Modo Internet Explorer:**

   * Permite que los usuarios usen la interfaz de usuario (UI) de Microsoft Edge para probar los sitios en el modo Internet Explorer. A partir de la versión 86 de Microsoft Edge, los administradores pueden habilitar la opción de interfaz de usuario para cargar una pestaña en el modo de Internet Explorer con propósitos de prueba o como medida provisional, hasta que los sitios se agreguen al XML de la lista de sitios.

* **Elimine las descargas en el disco con el administrador de descargas.** Ahora los usuarios pueden eliminar los archivos descargados en su disco sin salir del explorador. La nueva funcionalidad Eliminar descargas se encuentra en el menú emergente del estante de descargas o de la página de descargas.

* **Volver a la versión anterior de Microsoft Edge.** La característica de restauración permite a los administradores volver a una versión en buen estado y conocida de Microsoft Edge si hay algún problema en la versión más reciente de Microsoft Edge.
[Más información](edge-learnmore-rollback.md).

* **Ejecutar la habilitación de Sincronización de forma predeterminada en toda la empresa.**  Los administradores pueden habilitar la sincronización para cuentas de Azure Active Directory (Azure AD) de forma predeterminada con la directiva [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync).

* **Actualizaciones para PDF:**

  * Tabla de contenido para documentos PDF. A partir de la versión 86, Microsoft Edge ha agregado soporte con la tabla de contenidos, que permite a los usuarios desplazarse de manera sencilla por los documentos PDF.
  * Acceso a todas las funciones PDF en pantallas pequeñas. Obtenga acceso a todas las funciones del lector de PDF para Microsoft Edge en los dispositivos con tamaños de pantalla reducidos.
  * Compatibilidad con el lápiz para resaltar en archivos PDF. Con esta actualización, los usuarios pueden usar el lápiz digital para resaltar texto directamente en archivos PDF, de la misma forma que lo harían con un subrayador o resaltador y una hoja en físico.
  * Se ha mejorado el desplazamiento de PDF. Ahora podrá experimentar un desplazamiento sin interrupciones mientras navega por documentos largos en PDF.

* **Cambio de perfil automático en Windows 7, 8 y 8.1.** El cambio de perfil automático que está disponible actualmente en Microsoft Edge en Windows 10 se amplía a otros Windows con versiones anteriores (Windows 7, 8 y 8.1). Para obtener más información, consulte la publicación en el blog [cambio de perfil automático](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Los usuarios verán sugerencias de autocompletar al empezar a escribir una consulta de búsqueda en el sitio web de complementos de Microsoft Edge.** Autocompletar ayudará a los usuarios a realizar de manera rápida sus búsquedas sin tener que escribir el nombre completo del elemento que estén buscando. Esto puede ser útil, ya que los usuarios no tendrán que recordar la escritura correcta y podrán elegir entre las opciones disponibles que se muestran.

* **Quitar la API de caché de aplicaciones HTML5.**  A partir de la versión 86 de Microsoft Edge, la API de caché de aplicaciones heredada que permite el uso sin conexión de páginas web se quita de Microsoft Edge. Los desarrolladores web deben revisar la documentación [WebDev](https://web.dev/appcache-removal/) para obtener información sobre cómo reemplazar la API de caché de aplicaciones con trabajos de servicio.  Importante: Puede solicitar un [token de AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) que permite a los sitios seguir usando la API de caché de aplicaciones obsoleta hasta la versión 90 de Microsoft Edge.

* **Seguridad:**

  * Soporte de DNS seguro (DNS a través de HTTPS).  A partir de la versión 86 de Microsoft Edge, está disponible la configuración para controlar el DNS seguro en los dispositivos no administrados. Estas opciones de configuración no son accesibles para los usuarios de dispositivos administrados, pero los administradores de TI pueden habilitar o deshabilitar el DNS seguro con la directiva de grupo [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode).


* **Agregar una imagen personalizada a la página de nueva pestaña (NTP) con una directiva de grupo.** A partir de la versión 86 de Microsoft Edge, la NTP tiene la opción de reemplazar la imagen predeterminada por una imagen personalizada proporcionada por el usuario. La directiva de grupo admite también la capacidad para administrar las propiedades de esta imagen.

* **Hacer coincidir los métodos abreviados de teclado personalizados con el VS Code.** Ahora las DevTools de Microsoft Edge permiten personalizar los métodos abreviados de teclado en las DevTools para que coincidan con su editor/IDE. (En Microsoft Edge 84, agregamos la capacidad de hacer coincidir los métodos abreviados del teclado de las DevTools con el VS Code).

* **Reemplazar las directivas [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) y [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) para las versiones anteriores de Windows y macOS.** Estas directivas están en desuso en la versión 86 de Microsoft Edge y quedarán obsoletas en Microsoft Edge versión 89.<br>
Estas directivas se reemplazarán por [Permitir telemetría](https://go.microsoft.com/fwlink/?linkid=2099569) en Windows 10 y la nueva directiva [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) para las demás plataformas. Esto permitirá que los usuarios administren los datos de diagnóstico que se envían a Microsoft para Windows 7, 8, 8.1 y macOS.

* **Cookies con SameSite=Lax de manera predeterminada**. Para mejorar la seguridad y la privacidad Web, las cookies usarán ahora [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) de manera predeterminada. Esto significa que las cookies se enviarán solo como cookies de origen y se omitirán para las solicitudes que se envíen a terceros. Este cambio puede provocar un impacto en la compatibilidad en aquellos sitios web que necesitan cookies para recursos de terceros para funcionar correctamente. Para permitir el envío de cookies, los desarrolladores web pueden marcar cookies que deberían establecerse y recibirse en contextos de terceros agregando atributos `SameSite=none` y `Secure` explícitos al establecer la cookie. Las empresas que quieran excluir determinados sitios de este cambio pueden usar la directiva [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) y las que quieran que ningún sitio sufra el cambio, pueden valerse de la directiva [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled).

### Actualizaciones de directiva

#### Nuevas directivas

Se han agregado diecinueve directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist): Bloquear el acceso a una lista especificada de servicios y destinos de exportación en Colecciones.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting): Configuración predeterminada de sensores.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting): Controlar el uso de la API de serie.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata): Enviar datos de diagnóstico necesarios y opcionales sobre el uso del explorador.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed): Permitir el acceso a la herramienta Enterprise Mode Site List Manager
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
- [URLBlocklist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlblocklist): Bloquear el acceso a una lista de direcciones URL.
- [URLAllowlist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlallowlist): Definir una lista de direcciones URL permitidas.
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled): Habilitar la característica User-Agent Client Hints (en desuso).
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit): Limitar el número de instantáneas de datos de usuario que se conservan para su uso en caso de reversión de emergencia.

#### Directivas obsoletas

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): habilitar el uso y los informes de datos relacionados con bloqueos.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): enviar información de sitios para mejorar los servicios Microsoft.

#### Directiva obsoleta

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled): habilitar una característica de seguridad TLS 1.3 para anclajes de veracidad locales.

#### Título de directiva modificado

[NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled): Habilitar ocultar ventanas nativas.

#### Descripción de la directiva modificado

- [AdsSettingForIntrusiveAdsSites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun)
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes)
- [BrowserSignin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsersignin)
- [ClearBrowsingDataOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearbrowsingdataonexit) 
- [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare)
- [CookiesAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#cookiesallowedforurls)
- [CustomHelpLink](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#customhelplink)
- [DefaultCookiesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultcookiessetting)
- [DefaultGeolocationSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultgeolocationsetting)
- [DefaultImagesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultimagessetting)
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultjavascriptsetting)
- [DefaultNotificationsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultnotificationssetting)
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)
- [DefaultPopupsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpopupssetting)
- [DefaultSearchProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#developertoolsavailability)
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors)
- [DownloadRestrictions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ForceBingSafeSearch](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcebingsafesearch)
- [ForceYouTubeRestrict](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forceyoutuberestrict)
- [HomepageIsNewTabPage](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepageisnewtabpage)
- [HomepageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepagelocation)
- [InPrivateModeAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#networkpredictionoptions)
- [NewTabPageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation)
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox)
- [NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls)
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [RegisteredProtocolHandlers](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#registeredprotocolhandlers)
- [RelaunchNotification](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#relaunchnotification)
- [RestoreOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartup)
- [RestoreOnStartupURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartupurls)
- [RestrictSigninToPattern](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restrictsignintopattern)
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)
- [SmartScreenAllowListDomains](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenallowlistdomains)
- [SmartScreenEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)
- [TrackingPrevention](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#trackingprevention)
- [WebRtcLocalhostIpHandling](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalhostiphandling)

<!-- end 86 -->

## Versión 85.0.564.41:25 de agosto

Se han corregido varios errores y problemas de rendimiento.

## Versión 85.0.564.40: 21 de agosto

Se han corregido varios errores y problemas de rendimiento.

## Versión 85.0.564.36: 17 de agosto

Se han corregido varios errores y problemas de rendimiento.

## Versión 85.0.564.30: 10 de agosto

Se han corregido varios errores y problemas de rendimiento.

## Versión 85.0.564.23:3 de agosto

Se han corregido varios errores y problemas de rendimiento.
<!-- major 85 -->
## Versión 85.0.564.18: 28 de julio

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
- [TLSCipherSuiteDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tlsciphersuitedenylist): especificar los conjuntos de cifrado TLS para deshabilitarlos.

#### Directivas obsoletas

- [EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload): habilitar la descarga de las acciones del dominio desde Microsoft.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled): volver a habilitar la API de componentes web v0 hasta M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): permitir al controlador web invalidar las directivas obsoletas.

<!--- END ---->

## Versión 84.0.522.35: 9 de julio

Se han corregido varios errores y problemas de rendimiento.

## Versión 84.0.522.28: 26 de junio

Se han corregido varios errores y problemas de rendimiento.

## Versión 84.0.522.26: 24 de junio

Se han corregido varios errores y problemas de rendimiento.

## Versión 84.0.522.20: 15 de junio

Se han corregido varios errores y problemas de rendimiento.

## Versión 84.0.522.15: 8 de junio

Se han corregido varios errores y problemas de rendimiento.

## Versión 84.0.522.11: 2 de junio

### Actualizaciones de características

- Esta versión de Microsoft Edge proporciona tiempos mejorados de descarga de la lista de sitios en el modo Internet Explorer.  Hemos reducido el tiempo de retraso de la descarga de la lista de sitios en modo Internet Explorer de 60 segundos a 0 segundos, en ausencia de una lista de sitios en caché. También hemos agregado compatibilidad con la directiva de grupo para casos en los que es necesario retrasar la navegación de la página principal en modo Internet Explorer hasta que finaliza la descarga de la lista de sitios. Para más información, consulte la directiva [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

- Microsoft Edge permite ahora a los usuarios iniciar sesión en el explorador cuando se "ejecuta como administrador" en Windows 10. Esto ayudará a los clientes que ejecuten Microsoft Edge en Windows server o en escenarios de escritorio remoto y de espacio aislado.

- Microsoft Edge ofrece ahora compatibilidad total con el mouse en el modo de pantalla completa. Ahora puede usar el mouse para acceder a las pestañas, la barra de direcciones y otros elementos sin tener que salir del modo de pantalla completa.

- Mejoras en la compra online. Agregue alias personalizados a la tarjeta de crédito o débito guardada. Ahora podrá distinguir y diferenciar las tarjetas de crédito cuando realice compras en línea. Escribir un alias para las tarjetas de crédito o débito le facilitará elegir la tarjeta adecuada al usar la opción de Autorrellenar para seleccionar un método de pago.

- De forma predeterminada, se deshabilitan TLS/1.0 y TLS/1.1. Para facilitar la detección de los sitios afectados, puede establecer el indicador *edge://flags/#display-legacy-tls-warnings* para que Microsoft Edge muestre un aviso de no bloqueo de "no seguro" al cargar páginas que requieran protocolos TLS heredados. La directiva [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) permite volver a habilitar TLS/1.0 y TLS/1.1. Esta directiva estará disponible como mínimo hasta la versión 88 de Microsoft Edge. Para más información, consulte [Cambios que se van a producir en Microsoft Edge que afectan a la compatibilidad de los sitios](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

- Mejoras en las colecciones:

  - Se ha agregado una funcionalidad de notas que le permite añadir una nota o comentario a un elemento de una colección. Las notas se agrupan y se mantienen adjuntadas a un elemento incluso si se ordenan los elementos de una colección. Para probar esta característica nueva, haga clic con el botón derecho en un elemento y seleccione "Agregar nota".
  - Puede cambiar el color de fondo de las notas en las colecciones. Puede usar la codificación por colores para ayudarle a organizar información y a incrementar la productividad.
  - Se han realizado mejoras notables en el rendimiento que le permiten exportar las colecciones a Excel en un tiempo menor que en las versiones anteriores de Microsoft Edge.

- Compatibilidad adicional con la API de Microsoft Edge:

  - La API de acceso al almacenamiento. Esta API permite acceder al almacenamiento de origen en un contexto de terceros en el que un usuario proporcione una forma directa de permitir el almacenamiento que, de otro modo, quedaría bloqueada por la configuración actual del explorador.

    Dado que la privacidad es cada vez más importante para los usuarios, van en aumento las solicitudes de configuraciones opcionales de usuario y de valores predeterminados del explorador más estrictos, como el bloqueo de todos los accesos al almacenamiento de terceros. Si bien estas configuraciones contribuyen a mejorar la privacidad y a bloquear los accesos no deseados de partes desconocidas o que no son de confianza, pueden tener consecuencias no deseadas, como el bloqueo del acceso a contenido que el usuario podría querer ver (por ejemplo, contenido de redes sociales y contenido multimedia incrustado).

  - La API del sistema de archivos nativo quiere decir que usted puede conceder permisos a los sitios para editar archivos o carpetas mediante la API del sistema de archivos nativo.

- Mejoras de PDF:

  - Leer en voz alta para PDF permite a los usuarios escuchar contenido PDF mientras llevan a cabo otras tareas que pueden ser importantes. Además, ayuda a las personas que reciben educación audiovisual a centrarse en la lectura del contenido, lo que facilita el aprendizaje.
  - Se ha mejorado la edición de archivos PDF. Ahora puede guardar en el mismo archivo las modificaciones realizadas a un archivo PDF, en lugar de tener que guardar una copia cada vez que edita un PDF.

- Microsoft Edge permite ahora traducir en el Lector inmersivo. Cuando un usuario abre la vista de Lector inmersivo, obtiene la opción de traducir la página al idioma que desee.

- DevTools admite la personalización de los métodos abreviados de teclado para que coincidan con su editor/IDE, incluido VS Code.

### Actualizaciones de directiva

#### Nuevas directivas

Se han agregado cinco directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled): permite volver a habilitar la característica AppCache, incluso si está desactivada de forma predeterminada.
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy): contenedor proxy de Protección de aplicaciones.
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload): Requerir que la lista de sitios modo empresarial esté disponible antes que la navegación por la tabulación.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled): habilitar ocultar ventanas nativas.
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout): Establecer un tiempo de espera de retardo en la navegación mediante tabulación para la lista de sitios de modo empresarial.

#### Directivas obsoletas

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal): Permitir que las páginas envíen solicitudes sincrónicas de XHR durante el descarte de página.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled): determina si el comprobador de certificados integrado se usará para comprobar certificados de servidor.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled): habilitar el tratamiento más estricto para contenido mixto.

#### Directiva obsoleta

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess): Forzar el código de red para que se ejecute en el proceso del explorador.

<!-- end 84 -->

## Versión 83.0.478.44: 1 de junio

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.37: 20 de mayo

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.33: 15 de mayo

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.28: 7 de mayo

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.25: 4 de mayo

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.18: 27 de abril

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.13: 22 de abril

### Actualizaciones de características

- Mejoras de SmartScreen de Microsoft Defender: se han realizado varias mejoras en el servicio de SmartScreen de Microsoft Defender, como la protección mejorada frente a sitios malintencionados que redirigen al cargar, y el bloqueo de marco de nivel superior que reemplaza completamente sitios malintencionados con la página de seguridad de SmartScreen de Microsoft Defender. El bloqueo del marco de nivel superior impide que el audio y otros elementos multimedia del sitio malintencionado se reproduzcan, lo que ofrece una experiencia más fácil y menos confusa.

- En respuesta a los comentarios de los usuarios, ahora se pueden eximir algunas cookies del borrado automático cuando se cierre el explorador. Esta opción es útil si hay un sitio en el que los usuarios no quieren cerrar la sesión, pero quieren que todas las demás cookies se eliminen cuando se cierre el explorador. Para usar esta característica, ve a *edge://settings/clearBrowsingDataOnClose* y habilita el interruptor "Cookies y otros datos de sitio".

- El cambio de perfil automático ya está disponible para ayudarte a obtener el contenido del trabajo más fácilmente entre perfiles. Si usas varios perfiles en el trabajo, puedes probarlo en un sitio que requiera autenticación de tu cuenta profesional o educativa mientras estás en tu perfil personal. Si detectamos un cambio, se te pedirá cambiar a tu perfil de trabajo para poder acceder a ese sitio sin tener que autenticarte. Cuando selecciones el perfil de trabajo al que quieres cambiar, el sitio web se abrirá en tu perfil de trabajo. Esta función de cambio de perfil te ayudará a mantener tus datos personales y de trabajo separados y a obtener el contenido de trabajo con mayor esfuerzo. Si no quieres que la característica te solicite cambiar perfiles, puedes elegir la opción no volver a preguntar y se quitará.

- Mejoras de la característica de Colecciones:
  - Puedes usar arrastrar y soltar para agregar un elemento a una colección sin abrir la colección. Durante el proceso de arrastrar y soltar también puedes elegir una ubicación en la lista de colecciones en la que quieras colocar el elemento.
  - Puedes agregar varios elementos a una colección en lugar de agregar un elemento a la vez. Para agregar varios elementos, selecciona los elementos y arrástralos hasta una colección. También puedes seleccionarlos, hacer clic con el botón derecho y elegir la colección en la que quieres que aparezcan los elementos.

- Puedes agregar todas las pestañas de una ventana de Microsoft Edge a una colección nueva sin agregarlas individualmente. Para agregar todas las pestañas, haz clic con el botón derecho en cualquier pestaña y selecciona "Agregar todas las pestañas a una nueva colección".

- La sincronización de extensiones ya está disponible. Ahora, puedes sincronizar tus extensiones de en todos tus dispositivos. Las extensiones de las tiendas de Microsoft y Chrome se sincronizarán con Microsoft Edge. Para usar esta característica: haz clic en el signo de puntos suspensivos (**...**) en la barra de menús, selecciona **Configuración**. En Tu perfil, haz clic en **Sincronización** para ver las opciones de sincronización. En **Perfiles / Sincronizar** usa el botón de alternancia para habilitar Extensiones. Puedes usar la directiva de grupo [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) para deshabilitar la sincronización de extensiones.

- Se ha mejorado el mensaje en la página de Administración de descargas para las descargas no seguras que se han bloqueado.

- Mejoras en el Lector inmersivo:
  - Se ha agregado soporte para Adverbios en la experiencia de Elementos de la oración que tenemos en el Lector inmersivo. Mientras lee un artículo en el Lector inmersivo, abra las Herramientas gramaticales y active los Adverbios en las Elementos de la oración para resaltar todos los adverbios de la página.
  - Se ha agregado la posibilidad de seleccionar cualquier contenido de una página web y abrirla en el Lector inmersivo. Esta capacidad permite a los usuarios utilizar el Lector inmersivo y todas las herramientas de aprendizaje, como Foco de línea y Lectura en voz alta, en todos los sitios web.

- Link doctor proporciona correcciones de host y una consulta de búsqueda a los usuarios cuando escriben errores en una dirección URL. Por ejemplo: <br>
Un usuario escribe "powerbi" como "powerbbi".com. Link doctor propondrá "powerbi".com como corrección y creará un vínculo para buscar "powerbbi" en caso de que el usuario busque algo diferente.

- Permitir que los usuarios guarden su decisión de lanzar un protocolo externo para un sitio específico. Los usuarios pueden configurar la directiva [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) para habilitar o deshabilitar esta característica.

- Los usuarios pueden establecer Microsoft Edge como su explorador predeterminado directamente desde la **Configuración** de Microsoft Edge. Esta funcionalidad facilita a los usuarios cambiar su explorador predeterminado, dentro del contexto del explorador, en lugar de tener que buscar en la configuración del sistema operativo. Para usar esta característica, ve a *edge://settings/defaultBrowser* y haz clic en **Establecer como predeterminado**.

- Varias actualizaciones de DevTools, incluido el nuevo soporte de depuración remota, mejoras en la interfaz de usuario y más. Para más información, consulta [Novedades en DevTools (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

### Actualizaciones de directiva

#### Nuevas directivas

Se agregaron 15 nuevas directivas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AllowSurfGame](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsurfgame): permitir juego de navegación.
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls): configurar la lista de sitios con los que Microsoft Edge intentará establecer un enlace de tokens.
- [BingAdsSuppression](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#bingadssuppression): bloquear todos los anuncios en los resultados de búsqueda de Bing.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled): determina si el comprobador de certificados integrado se usará para comprobar certificados de servidor.
- [ClearCachedImagesAndFilesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearcachedimagesandfilesonexit): limpiar las imágenes y los archivos almacenados en caché cuando se cierra Microsoft Edge.
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare): configurar la experiencia de uso compartido.
- [DeleteDataOnMigration](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#deletedataonmigration): eliminar datos antiguos del explorador en la migración.
- [DnsOverHttpsMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpsmode): controlar el modo de DNS a través de HTTPS.
- [DnsOverHttpsTemplates](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpstemplates): especificar la plantilla URI de la resolución de DNS a través de HTTPS deseada.
- [FamilySafetySettingsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#familysafetysettingsenabled): permitir que los usuarios configuren la seguridad familiar.
- [LocalProvidersEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#localprovidersenabled): permitir sugerencias de proveedores locales.
- [ScrollToTextFragmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#scrolltotextfragmentenabled): habilitar el desplazamiento al texto especificado en fragmentos de URL.
- [ScreenCaptureAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#screencaptureallowed): permitir o denegar capturas de pantalla.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configurar la lista de tipos que se excluyen de la sincronización.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled): habilitar ocultar ventanas nativas.

#### Directivas en desuso

Las siguientes directivas seguirán funcionando en esta versión. Pasarán a estar "en desuso" en una versión futura.

[EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) habilitar descarga de acciones de dominio de Microsoft

<!--  end 83 -->

## Versión 81.0.416.60: 20 de abril

Se han corregido varios errores y problemas de rendimiento.

## Versión 81.0.416.58: 17 de abril

Actualizaciones de seguridad.

## Versión 81.0.416.50: 10 de abril

Se han corregido varios errores y problemas de rendimiento.

## Versión 81.0.416.45: 3 de abril

Se han corregido varios errores y problemas de rendimiento.

## Versión 81.0.416.41: 30 de marzo

Se han corregido varios errores y problemas de rendimiento.

## Versión 81.0.416.34: 17 de marzo

Se han corregido varios errores y problemas de rendimiento.

## Versión 81.0.416.31: 12 de marzo

Se han corregido varios errores y problemas de rendimiento.

## Versión 81.0.416.28: 9 de marzo

Se han corregido varios errores y problemas de rendimiento.

## Versión 81.0.416.20: 28 de febrero

Se han corregido varios errores y problemas de rendimiento.

## Versión 81.0.416.12: 20 de febrero

### Actualizaciones de características

- Colecciones ya está disponible. Para empezar, haga clic en el icono Colecciones que encontrará junto a la barra de direcciones. Esta acción abre el panel Colecciones, donde podrá crear, editar y ver las colecciones. Diseñamos Colecciones en función de lo que los usuarios hacen en la web. Sin importar si es comprador, viajero, profesor o alumno, las colecciones pueden ser de ayuda. [Más información](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Permita la eliminación (ocultar de la barra de herramientas) del botón Colecciones de la barra de herramientas de Microsoft Edge para lograr coherencia.

- El inicio de sesión automático en cuentas de Active Directory locales solo se dirigirá a las organizaciones que lo activen. Si los usuarios ya han iniciado sesión con una cuenta de AD local, podrán salir de la sesión. Ahora, los usuarios solo iniciarán sesión automáticamente con la cuenta principal en su sistema operativo si es una cuenta de Microsoft o una cuenta de Active Directory. Los administradores pueden habilitar el inicio de sesión automático con una cuenta de AD local con la directiva ConfigureOnPremisesAccountAutoSignIn.

- Protección de aplicaciones. La compatibilidad con las extensiones ahora está disponible en el contenedor.

- Se ha agregado un mensaje para informar a los usuarios de que Internet Explorer no se instala cuando un usuario navega a una página que está configurada para abrirse en modo de Internet Explorer.

- Se ha actualizado la herramienta vista 3D de Microsoft Edge DevTools con una nueva característica que ayuda a depurar el contexto de apilamiento de índice z. La vista 3D muestra una representación de la profundidad del modelo de objetos de documento (DOM) utilizando colores y apilamiento, y la vista de índice z le ayuda a aislar los distintos contextos de apilamiento de la página. [Más información](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Las herramientas de desarrollo F12 se han localizado en 10 idiomas nuevos, por lo que coincidirán con el idioma que se usa en el resto del explorador. [Más información](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Se ha agregado compatibilidad con la reproducción de Dolby Vision. En compilación 17134 de Windows 10 (actualización 2018 de abril) con Dolby Vision activado, los sitios web pueden mostrar el contenido de Dolby Vision. Vea cómo habilitar el contenido de Dolby Vision en [Netflix](https://help.netflix.com/en/node/42384).

- Microsoft Edge ahora puede identificar y quitar duplicados de favoritos y combinar carpetas que tienen el mismo nombre. Para acceder a la herramienta, haga clic en la estrella en la barra de herramientas del explorador y seleccione "Quitar favoritos duplicados".  Podrá confirmar los cambios y las actualizaciones de sus favoritos se sincronizarán en todos los dispositivos.

- Los usuarios nos han indicado que puede resultar complicado distinguir una ventana de navegación normal en un tema oscuro de una ventana de InPrivate, ya que ambos marcos de ventana son oscuros. La nueva píldora azul de InPrivate en la esquina superior derecha ayuda a asegurar a los usuarios que están en InPrivate.

- Abra vínculos externos en el perfil de explorador correcto. Seleccione un perfil predeterminado para abrir los vínculos abiertos para aplicaciones externas en *edge://settings/multiProfileSettings*.

- Se ha agregado una advertencia para alertar a los usuarios que inician sesión en un perfil de explorador con una cuenta después de haber iniciado sesión con otra cuenta previamente. Esto ayudará a evitar la combinación de datos no intencionada.

- Si tiene tarjetas de pago guardadas en su cuenta de Microsoft, puede usarlas en Microsoft Edge mientras rellena formularios de pago. Las tarjetas de su cuenta de Microsoft se sincronizarán en los dispositivos de escritorio y todos los detalles se compartirán con el sitio web después de la autenticación de dos factores (código CVC y su identidad de Microsoft). Para más comodidad, puede elegir guardar una copia de la tarjeta en el dispositivo de forma segura durante la autenticación.

- El foco de línea está diseñado para los usuarios que deseen concentrarse en una parte limitada del contenido mientras leen. Permite que los usuarios mantengan el foco en 1, 3 o 5 líneas cada vez y atenúa el resto de la página para que los usuarios puedan leer sin distracciones. Los usuarios pueden desplazarse con las teclas táctiles o de dirección y el foco cambia en consecuencia.

- Microsoft Edge está ahora integrado con el corrector ortográfico de Windows en las plataformas Windows 8.1 y posteriores. Esta integración ofrece una mayor compatibilidad con idiomas, con acceso a más diccionarios de idiomas y la posibilidad de usar diccionarios personalizados de Windows. Los usuarios no necesitan realizar ninguna acción cuando se ha agregado un idioma en la configuración de idioma del sistema operativo y el botón de alternancia de corrección ortográfica del idioma está habilitado en la configuración de Microsoft Edge.

- Cuando se abren documentos PDF con Microsoft Edge, los usuarios ya podrán crear resaltados, cambiar el color y eliminar los resaltados. Esto sirve para hacer referencia a partes importantes del documento más adelante y para la colaboración.

- Cuando cargue documentos PDF largos que se han optimizado para la web, las páginas que está viendo el usuario se cargarán más rápido, en paralelo, mientras el resto del documento se carga.

- Ahora es más fácil empezar a usar el lector inmersivo para un sitio web pulsando la tecla F9.

- Ahora es más fácil empezar la lectura en voz alta con un método abreviado de teclado (Ctrl + Mayús + U).

### Actualizaciones de directiva

#### Nuevas directivas

Se han agregado 12 directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled): habilitar la autenticación de ambiente para los perfiles de InPrivate e invitado. 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled): permitir ejecutar el espacio aislado de audio.
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy): usar una directiva de referrer predeterminada de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled): habilitar la memoria caché de autenticación HTTP de ámbito global.
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions): permitir la importación de extensiones.
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies): permitir la importación de cookies.
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts): permitir la importación de métodos abreviados.
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect) : especificar cómo se comportan las navegaciones "en la página" de los sitios no configurados al iniciarse en las páginas en modo Internet Explorer.
- [OmniboxMSBProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#omniboxmsbproviderenabled): activar Búsqueda de Microsoft para proveedores de empresas en omnibox. 
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled): habilitar el tratamiento más estricto para contenido mixto.
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled): habilitar una característica de seguridad TLS 1.3 para anclajes de veracidad locales.
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin): configurar el inicio de sesión automático con una cuenta de dominio de Active Directory cuando no haya cuenta de dominio de Azure AD.

#### Directivas obsoletas

Las siguientes directivas siguen funcionando en esta versión. Pasarán a ser "obsoletas" en una versión futura.

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled): volver a habilitar la API de componentes web v0 hasta M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): permitir que el controlador WebDriver reemplace Incompatible.

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)