---
title: Documentación de directiva de explorador Microsoft Edge
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 10/22/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentación de Windows y Mac para todas las directivas admitidas por Explorador Microsoft Edge
ms.openlocfilehash: 982a171e1c4f55ab99db53a399c669fdf4798f53
ms.sourcegitcommit: 7d160257010f75b86b89c8802d0dd27f1f8761ef
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134469"
---
# Microsoft Edge: directivas

La versión más reciente de Microsoft Edge incluye las siguientes directivas. Puede usar estas directivas para configurar cómo se ejecuta Microsoft Edge en su organización.

Para obtener información sobre un conjunto adicional de directivas utilizadas para controlar cómo y cuándo se actualiza Microsoft Edge, vea la [referencia de directiva de actualización de Microsoft Edge](microsoft-edge-update-policies.md).

Puede descargar el [Kit Microsoft Security Compliance](https://www.microsoft.com/download/details.aspx?id=55319) para la configuración básica de seguridad recomendada para Microsoft Edge. Para más información, vea el [Blog de líneas base de seguridad de Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines).

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## Directivas disponibles

Estas tablas enumeran todas las directivas de grupo relacionadas con el explorador disponibles en esta versión de Microsoft Edge. Usa los vínculos de la tabla para obtener más detalles sobre directivas específicas.

|||
|-|-|
|[Configuración de Protección de aplicaciones](#application-guard-settings)|[Transmitir](#cast)|
|[Configuración del Contenido](#content-settings)|[Proveedor de búsquedas predeterminado](#default-search-provider)|
|[Extensions](#extensions)|[Autenticación HTTP](#http-authentication)|
|[Configuración de pantalla completa](#kiosk-mode-settings)|[Mensajería nativa](#native-messaging)|
|[Administrador de contraseñas y protección](#password-manager-and-protection)|[Impresión](#printing)|
|[Servidor proxy](#proxy-server)|[Configuración de SmartScreen](#smartscreen-settings)|
|[Inicio, página principal y página de pestaña nueva](#startup-home-page-and-new-tab-page)|[Adicional](#additional)|


### [*Configuración de Protección de aplicaciones*](#application-guard-settings-policies)

|Nombre de directiva|Título|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Contenedor proxy de la Protección de aplicaciones|
### [*Transmitir*](#cast-policies)

|Nombre de directiva|Título|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Habilitar Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Mostrar el icono transmitir en la barra de herramientas|
### [*Configuración del Contenido*](#content-settings-policies)

|Nombre de directiva|Título|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Seleccionar automáticamente certificados de cliente para estos sitios|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Permitir las cookies en determinados sitios|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Bloquear las cookies en determinados sitios|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Limitar las cookies de determinados sitios web en la sesión actual|
|[DefaultCookiesSetting](#defaultcookiessetting)|Configurar cookies|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|Controlar el uso de la API del sistema de archivos para leer|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|Controlar el uso de la API del sistema de archivos para escribir|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Configuración de geolocalización predeterminada|
|[DefaultImagesSetting](#defaultimagessetting)|Configuración predeterminada de imágenes|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Controlar el uso de excepciones de contenido inseguro|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Configuración predeterminada de JavaScript|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Configuración predeterminada de notificación|
|[DefaultPluginsSetting](#defaultpluginssetting)|Configuración predeterminada de Adobe Flash|
|[DefaultPopupsSetting](#defaultpopupssetting)|Configuración predeterminada de la ventana emergente|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Controlar el uso de la API de Bluetooth Web|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Controlar el uso de la API WebUSB|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|Permitir el acceso de lectura a través de la API del sistema de archivos en estos sitios|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|Bloquear el acceso de lectura a través de la API del sistema de archivos en estos sitios|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|Permitir el acceso de escritura a archivos y directorios en estos sitios|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|Bloquear el acceso de escritura a archivos y directorios en estos sitios|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Permitir imágenes en estos sitios|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Bloquear imágenes en determinados sitios|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Permitir el contenido inseguro en determinados sitios|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Bloquear contenidos inseguros en determinados sitios|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|Permitir JavaScript en determinados sitios|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|Bloquear JavaScript en determinados sitios|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Habilitar la configuración predeterminada del comportamiento de las cookies de SameSite|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Revertir a la conducta heredada de SameSite para las cookies en determinados sitios|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Permitir las notificaciones en determinados sitios|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Bloquear las notificaciones en determinados sitios|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Permitir el complemento Adobe Flash en determinados sitios|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Bloquear el complemento Adobe Flash en determinados sitios|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Permitir ventanas emergentes en determinados sitios|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Bloquear ventanas emergentes en determinados sitios|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Registrar controladores de protocolo|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Decida si los usuarios pueden recibir imágenes de fondo y texto personalizados, sugerencias, notificaciones
y sugerencias para los servicios Microsoft|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Conceder acceso a determinados sitios para conectarse a dispositivos USB determinados|
|[WebUsbAskForUrls](#webusbaskforurls)|Permitir WebUSB en determinados sitios|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Bloquear WebUSB en determinados sitios|
### [*Proveedor de búsquedas predeterminado*](#default-search-provider-policies)

|Nombre de directiva|Título|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Habilitar el proveedor de búsquedas predeterminado|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Codificaciones de proveedores de búsqueda predeterminadas|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Especifica la característica de búsqueda por imagen para el proveedor de búsquedas predeterminado.|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Parámetros para una URL de imagen que utiliza POST|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Proveedor de palabras clave predeterminado|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Nombre del proveedor de búsquedas predeterminado|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|URL de búsqueda del proveedor de búsqueda predeterminado|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|URL del proveedor de búsqueda predeterminado para sugerencias|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Configurar la nueva experiencia del cuadro de búsqueda de la página de pestañas|
### [*Extensions*](#extensions-policies)

|Nombre de directiva|Título|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Configurar los tipos de extensión permitidos|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Permitir que se instalen extensiones específicas|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Controlar qué extensiones no se pueden instalar|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Controlar qué extensiones se instalan de forma silenciosa|
|[ExtensionInstallSources](#extensioninstallsources)|Configurar la extensión y los orígenes de instalación de los scripts de usuario|
|[ExtensionSettings](#extensionsettings)|Configurar la administración de la extensión|
### [*Autenticación HTTP*](#http-authentication-policies)

|Nombre de directiva|Título|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Allow cross-origin HTTP Authentication prompts|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Especifica una lista de servidores en los que Microsoft Edge puede delegar credenciales de usuario|
|[AuthSchemes](#authschemes)|Esquemas de autenticación compatibles|
|[AuthServerAllowlist](#authserverallowlist)|Configurar la lista de servidores de autenticación permitidos|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Deshabilitar la búsqueda CNAME al negociar la autenticación Kerberos|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Incluir un puerto no estándar en Kerberos SPN|
|[NtlmV2Enabled](#ntlmv2enabled)|Controlar si la autenticación NTLMv2 está habilitada|
### [*Configuración de pantalla completa*](#kiosk-mode-settings-policies)

|Nombre de directiva|Título|
|-|-|
|[KioskAddressBarEditingEnabled](#kioskaddressbareditingenabled)|Configura la edición de la barra de direcciones para la experiencia de navegación pública en modo de pantalla completa.|
|[KioskDeleteDownloadsOnExit](#kioskdeletedownloadsonexit)|Eliminar archivos descargados como parte de la sesión de pantalla completa cuando se cierra Microsoft Edge|
### [*Mensajería nativa*](#native-messaging-policies)

|Nombre de directiva|Título|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Controlar cuáles hosts de mensajería nativo pueden utilizar los usuarios|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Configurar la lista de bloqueados de la mensajería nativa|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Permitir los hosts de mensajería nativo en el nivel de usuario (instalado sin permisos de administrador) |
### [*Administrador de contraseñas y protección*](#password-manager-and-protection-policies)

|Nombre de directiva|Título|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Habilitar el guardado de contraseñas en el administrador de contraseñas|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Permitir que los usuarios puedan recibir alertas si se detecta que las contraseñas no son seguras|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Configurar el cambio de contraseña URL|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Configurar la lista de URLs de acceso a la empresa donde el servicio de protección de contraseñas debe capturar los salted hashes de una contraseña|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Configurar el desencadenador de advertencia de protección con contraseña|
|[PasswordRevealEnabled](#passwordrevealenabled)|Habilitar el botón revelar contraseña|
### [*Impresión*](#printing-policies)

|Nombre de directiva|Título|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Reglas predeterminadas para seleccionar impresoras|
|[PrintHeaderFooter](#printheaderfooter)|Imprimir encabezados y pies de página|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Establecer la impresora predeterminada del sistema como la impresora predeterminada|
|[PrintingEnabled](#printingenabled)|Habilitar la impresión|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|Tamaño de página de impresión predeterminado|
|[UseSystemPrintDialog](#usesystemprintdialog)|Imprimir usando el diálogo de impresión del sistema|
### [*Servidor proxy*](#proxy-server-policies)

|Nombre de directiva|Título|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Configurar las reglas de omisión de proxy|
|[ProxyMode](#proxymode)|Configurar los ajustes del servidor proxy|
|[ProxyPacUrl](#proxypacurl)|Establecer la URL del archivo proxy .pac|
|[ProxyServer](#proxyserver)|Configurar la dirección o la dirección URL del servidor proxy|
|[ProxySettings](#proxysettings)|Configuración de proxy|
### [*Configuración de SmartScreen*](#smartscreen-settings-policies)

|Nombre de directiva|Título|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Impedir la omisión de los mensajes de SmartScreen de Microsoft Defender para los sitios|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Impedir que se ignoren las advertencias de SmartScreen de Microsoft Defender sobre las descargas|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Configurar la lista de dominios en los que SmartScreen de Microsoft Defender no desencadenará advertencias|
|[SmartScreenEnabled](#smartscreenenabled)|Configurar SmartScreen de Microsoft Defender|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Forzar a SmartScreen de Microsoft Defender a comprobar las descargas de origen confiable|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Configurar SmartScreen de Microsoft Defender para bloquear aplicaciones potencialmente no deseadas.|
### [*Inicio&comma; página principal y página de pestaña nueva*](#startup-home-page-and-new-tab-page-policies)

|Nombre de directiva|Título|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Establecer la nueva ficha como página principal|
|[HomepageLocation](#homepagelocation)|Configurar la dirección URL de la página principal|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Configurar los tipos de fondo permitidos para el diseño de página de nueva pestaña|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Establecer el logotipo de la compañía en la página de nueva pestaña (obsoleto)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Ocultar los sitios principales predeterminados de la nueva ficha|
|[NewTabPageLocation](#newtabpagelocation)|Configurar la dirección URL de la ficha|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Establecer una nueva ficha de vínculos rápidos|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Habilitar precarga de la página de nueva pestaña para procesamiento más rápido|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Configurar la experiencia de la nueva ficha de Microsoft Edge (en desuso)|
|[RestoreOnStartup](#restoreonstartup)|Acción que se realizará en el inicio|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Sitios que se abren cuando el explorador se inicia|
|[ShowHomeButton](#showhomebutton)|Mostrar el botón Inicio en la barra de herramientas|
### [*Adicional*](#additional-policies)

|Nombre de directiva|Título|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Habilitar las sugerencias de Búsqueda de Microsoft en Bing en la barra de direcciones|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Configuración de anuncios para sitios con anuncios intrusivos|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Habilitar la eliminación del explorador y el historial de descargas|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Permitir cuadros de diálogo de selección de archivos|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Permitir que una página muestre elementos emergentes durante su descarga|
|[AllowSurfGame](#allowsurfgame)|Permitir el juego surf|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Permitir que las páginas envíen solicitudes de XHR sincrónicas durante el descarte de página (en desuso)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Configurar la lista de sitios con los que Microsoft Edge intentará establecer un enlace de tokens.|
|[AllowTrackingForUrls](#allowtrackingforurls)|Configurar excepciones de prevención de seguimiento para determinados específicos|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Sugiere páginas similares cuando no se puede encontrar una página web.|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|Abrir siempre los archivos PDF externamente|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Habilitar la autenticación de ambiente para los perfiles InPrivate o Invitado|
|[AppCacheForceEnabled](#appcacheforceenabled)|Permite volver a habilitar la característica AppCache, incluso si está desactivada de forma predeterminada.|
|[ApplicationLocaleValue](#applicationlocalevalue)|Establecer la configuración regional de la aplicación|
|[AudioCaptureAllowed](#audiocaptureallowed)|Permitir o bloquear captura de audio|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Sitios que pueden acceder a dispositivos de captura de audio sin solicitar permiso|
|[AudioSandboxEnabled](#audiosandboxenabled)|Permitir ejecutar el espacio aislado de audio.|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Importar automáticamente los datos y la configuración desde otro explorador en la primera ejecución|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Definir una lista de protocolos para iniciar una aplicación externa desde orígenes de la lista sin pedir al usuario|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URL donde se pueden aplicar AutoOpenFileTypes|
|[AutoOpenFileTypes](#autoopenfiletypes)|Lista de tipos de archivo que se deben abrir automáticamente al descargarse|
|[AutofillAddressEnabled](#autofilladdressenabled)|Habilitar Autorrellenar para las direcciones|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|Habilitar Autorrellenar para las tarjetas de crédito|
|[AutoplayAllowed](#autoplayallowed)|Permitir la reproducción automática multimedia para sitios web|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Seguir ejecutando aplicaciones en segundo plano después de cerrar Microsoft Edge|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Permitir actualizaciones en segundo plano de la lista de plantillas disponibles para Colecciones y otras características que utilizan plantillas|
|[BingAdsSuppression](#bingadssuppression)|Bloquear todos los anuncios en los resultados de búsqueda de Bing.|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Bloquear cookies de terceros|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Permitir la creación de perfiles desde el menú desplegable identidad o la página Configuración|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Activar el modo invitado|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Permitir consultas a un servicio de tiempo de red del explorador|
|[BrowserSignin](#browsersignin)|Configuración de inicio de sesión del explorador|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Usar cliente DNS integrado|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Determina si el comprobador de certificados integrado se usará para comprobar certificados de servidor (en desuso)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Deshabilitar el certificado de transparencia para obtener una lista de hashes de PublicKeyInfo|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Deshabilitar el certificado Aplicación de la transparencia para una lista de autoridades de certificación de legado|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Deshabilitar la aplicación de la transparencia de certificados para dirección URL determinadas|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Borrar los datos de exploración cuando se cierra Microsoft Edge|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Limpie las imágenes y los archivos almacenados en caché cuando se cierra Microsoft Edge|
|[ClickOnceEnabled](#clickonceenabled)|Permitir que los usuarios abran archivos mediante el protocolo ClickOnce|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Bloquear el acceso a una lista especificada de servicios y destinos de exportación en Colecciones|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Habilitar advertencias de seguridad para indicadores de la línea de comandos|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Habilitar las actualizaciones de los componentes en Microsoft Edge|
|[ConfigureDoNotTrack](#configuredonottrack)|Configurar No realizar seguimiento|
|[ConfigureFriendlyURLFormat](#configurefriendlyurlformat)|Configura el formato de pegado predeterminado de las direcciones URL copiadas desde Microsoft Edge y determina si los formatos adicionales estarán disponibles para los usuarios.|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Configurar el inicio de sesión automático con una cuenta de dominio de Active Directory cuando no haya cuenta de dominio de Azure AD|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Configurar Texto a voz en línea|
|[ConfigureShare](#configureshare)|Configurar Compartir experiencia|
|[CustomHelpLink](#customhelplink)|Especificar el vínculo de ayuda personalizada|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Comprobaciones de interceptación de DNS habilitadas|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Establecer Microsoft Edge como explorador predeterminado|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Permitir el acceso de búsqueda al menú contextual del proveedor de búsquedas predeterminado|
|[DefaultSensorsSetting](#defaultsensorssetting)|Configuración predeterminada de sensores|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Controlar el uso de la API de serie|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Requerir que la lista de sitios modo empresarial esté disponible antes que la navegación por la tabulación|
|[DeleteDataOnMigration](#deletedataonmigration)|Eliminar datos antiguos del explorador en la migración.|
|[DeveloperToolsAvailability](#developertoolsavailability)|Controlar dónde se pueden usar las herramientas de desarrollo|
|[DiagnosticData](#diagnosticdata)|Enviar datos de diagnóstico necesarios y opcionales sobre el uso del explorador|
|[DirectInvokeEnabled](#directinvokeenabled)|Permitir que los usuarios abran archivos mediante el protocolo DirectInvoke|
|[Disable3DAPIs](#disable3dapis)|Deshabilitar la compatibilidad para las API gráficas 3D|
|[DisableScreenshots](#disablescreenshots)|Deshabilitar las capturas de pantalla|
|[DiskCacheDir](#diskcachedir)|Establecer directorio de caché de disco|
|[DiskCacheSize](#diskcachesize)|Configurar el tamaño de la caché de disco, en bytes|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Controlar el modo de DNS a través de HTTPS.|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Especificar la plantilla de URI de la resolución de DNS a través de HTTPS deseada|
|[DownloadDirectory](#downloaddirectory)|Establecer directorio de descarga|
|[DownloadRestrictions](#downloadrestrictions)|Permitir las restricciones de descarga|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Habilitar la característica colecciones|
|[EdgeShoppingAssistantEnabled](#edgeshoppingassistantenabled)|Comprar en Microsoft Edge activado|
|[EditFavoritesEnabled](#editfavoritesenabled)|Permitir que los usuarios editen los favoritos|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Re-enable deprecated web platform features for a limited time (obsolete)|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Habilitar la descarga de acciones de dominio de Microsoft (obsoleto)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Habilitar las comprobaciones de OCSP/CRL en línea|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Permitir certificados firmados mediante SHA-1 cuando sean emitidos por anclajes de veracidad locales (en desuso).|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Permitir que las extensiones administradas utilicen la API de la plataforma de hardware empresarial|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Permitir el acceso a la herramienta Enterprise Mode Site List Manager|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Deshabilitar el tipo de archivo de descarga advertencias basadas en la extensión para tipos de archivo especificados en dominios|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Controlar la comunicación con el servicio de experimentación y configuración|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Mostrar la casilla "abrir siempre" en el cuadro de diálogo de protocolo externo|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Permitir que los usuarios configuren la seguridad familiar|
|[FavoritesBarEnabled](#favoritesbarenabled)|Habilitar la barra de favoritos|
|[ForceBingSafeSearch](#forcebingsafesearch)|Forzar la búsqueda segura de Bing|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Configurar si Microsoft Edge debe seleccionar automáticamente un certificado cuando haya múltiples coincidencias de certificados para un sitio configurado con "AutoSelectCertificateForUrls"|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Permitir el uso de perfiles efímeros|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Forzar la búsqueda segura de Google|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Usar una directiva de referencia predeterminada de sin referencia cuando se cambia a una versión anterior (en desuso).|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Forzar el código de red para que se ejecute en el proceso del explorador|
|[ForceSync](#forcesync)|Forzar la sincronización de los datos del explorador y no mostrar la solicitud de consentimiento de sincronización|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Forzar el modo restringido de YouTube mínimo|
|[FullscreenAllowed](#fullscreenallowed)|Permitir el modo de pantalla completa|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Habilitar la caché de autenticación HTTP de ámbito global|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Forzar la navegación directa en el sitio de la intranet en lugar de buscar en las entradas de una sola palabra en la barra de direcciones|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Configurar la lista de nombres que se omitirán por alto la comprobación de la directiva de HSTS|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Usar la aceleración de hardware cuando esté disponible|
|[HideFirstRunExperience](#hidefirstrunexperience)|Ocultar la experiencia de primera ejecución y la pantalla de presentación.|
|[HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](#hideinternetexplorerredirectuxforincompatiblesitesenabled)|Ocultar el cuadro de diálogo redirección único y la pancarta en Microsoft Edge|
|[ImportAutofillFormData](#importautofillformdata)|Permitir la importación de los datos del formulario Autorrellenar|
|[ImportBrowserSettings](#importbrowsersettings)|Permitir la importación de la configuración del explorador|
|[ImportCookies](#importcookies)|Permitir la importación de cookies|
|[ImportExtensions](#importextensions)|Permitir la importación de extensiones|
|[ImportFavorites](#importfavorites)|Permitir la importación de favoritos|
|[ImportHistory](#importhistory)|Permitir la importación del historial de exploración|
|[ImportHomepage](#importhomepage)|Permitir la importación de la configuración de la página principal|
|[ImportOpenTabs](#importopentabs)|Permitir la importación de las pestañas abiertas|
|[ImportPaymentInfo](#importpaymentinfo)|Permitir la importación de información de pago|
|[ImportSavedPasswords](#importsavedpasswords)|Permitir la importación de las contraseñas guardadas|
|[ImportSearchEngine](#importsearchengine)|Permitir la importación de la configuración del motor de búsqueda|
|[ImportShortcuts](#importshortcuts)|Permitir la importación de accesos directos|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Configurar la disponibilidad del modo InPrivate|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Habilitar advertencias para formularios inseguros|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Controlar la característica IntensiveWakeUpThrottling|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Configurar la detección de bloqueos mejorada para el modo de Internet Explorer|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Configurar la integración de Internet Explorer|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Configurar la lista de sitios del Modo de empresa|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Especificar cómo se comportan las navegaciones "en la página" de los sitios no configurados al iniciarse en las páginas en modo Internet Explorer|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Permitir pruebas del modo Internet Explorer|
|[IsolateOrigins](#isolateorigins)|Habilitar el aislamiento de sitio para determinados orígenes|
|[LocalProvidersEnabled](#localprovidersenabled)|Permita sugerencias de proveedores locales.|
|[ManagedFavorites](#managedfavorites)|Configurar Favoritos|
|[ManagedSearchEngines](#managedsearchengines)|Administrar motores de búsqueda|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Número máximo de conexiones simultáneas al servidor proxy|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Permitir que Google Cast se conecte para transmitir dispositivos en todas las direcciones IP|
|[MetricsReportingEnabled](#metricsreportingenabled)|Habilitar el uso y los informes de datos relacionados con bloqueos (en desuso)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Habilitar oclusión de ventana nativa|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Establecer un tiempo de espera de retardo en la navegación por la etiqueta de la lista de sitios de modo empresarial|
|[NetworkPredictionOptions](#networkpredictionoptions)|Habilitar predicción de red|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Configurar si un usuario siempre tiene un perfil predeterminado que inicia sesión automáticamente con su cuenta profesional o educativa|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Controlar el lugar en el que se aplican restricciones de seguridad para orígenes inseguros|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Permita que los sitios web consulten los métodos de pago disponibles|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Permita la personalización de anuncios, búsquedas y noticias enviando el historial de exploración a Microsoft|
|[PinningWizardAllowed](#pinningwizardallowed)|Permita anclar al Asistente para tareas|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Permitir la autenticación proactiva|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Habilitar contenido promocional de pestañas completas|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Pregunte dónde guardar los archivos descargados|
|[QuicAllowed](#quicallowed)|Permitir protocolo QUIC|
|[RedirectSitesFromInternetExplorerPreventBHOInstall](#redirectsitesfrominternetexplorerpreventbhoinstall)|Evita la instalación del BHO para redirigir sitios incompatibles desde Internet Explorer a Microsoft Edge|
|[RedirectSitesFromInternetExplorerRedirectMode](#redirectsitesfrominternetexplorerredirectmode)|Redirigir los sitios incompatibles de Internet Explorer a Microsoft Edge.|
|[RelaunchNotification](#relaunchnotification)|Notifique a un usuario que es recomendable reiniciar el explorador, o es necesario para actualizaciones pendientes|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Establezca el período de tiempo de las notificaciones de actualización|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Habilitar integridad de código de representador|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Especifique si se necesitan comprobaciones OCSP/CRL en línea para los anclajes de veracidad local|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Habilite la resolución de errores de navegación con un servicio Web|
|[RestrictSigninToPattern](#restrictsignintopattern)|Restrinja las cuentas que se pueden usar como cuentas de Microsoft Edge principal|
|[RoamingProfileLocation](#roamingprofilelocation)|Configurar el directorio de perfiles móviles|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Permitir el uso de copias móviles para datos de Perfil de Microsoft Edge|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Extienda la configuración de contenido de Adobe Flash a todo el contenido|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Permita que los usuarios continúen desde la página de advertencia HTTPS|
|[SSLVersionMin](#sslversionmin)|Versión de TLS mínima activada|
|[SaveCookiesOnExit](#savecookiesonexit)|Guardar cookies cuando se cierra Microsoft Edge|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Deshabilitar la opción pada guardar el historial del explorador|
|[ScreenCaptureAllowed](#screencaptureallowed)|Permitir o denegar captura de pantalla|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Habilite el desplazamiento al texto especificado en fragmentos de URL|
|[SearchSuggestEnabled](#searchsuggestenabled)|Permitir sugerencias de búsqueda|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Sitios web o dominios que no necesitan permiso para usar la atestación de clave de seguridad directa|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Enviar todos los sitios de intranet a Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Enviar información de sitios para mejorar los servicios Microsoft (en desuso)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Permitir el acceso a sensores en sitios específicos|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Bloquear el acceso a sensores en sitios específicos|
|[SerialAskForUrls](#serialaskforurls)|Permitir la API de serie en sitios específicos|
|[SerialBlockedForUrls](#serialblockedforurls)|Bloquear la API de serie en sitios específicos|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Mostrar el acceso directo de Microsoft Office en la barra de favoritos (en desuso)|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Habilite la compatibilidad con el intercambio de HTTP firmado (SXG)|
|[SitePerProcess](#siteperprocess)|Habilite el aislamiento de sitio para cada sitio|
|[SpeechRecognitionEnabled](#speechrecognitionenabled)|Configure Speech Recognition|
|[SpellcheckEnabled](#spellcheckenabled)|Habilite corrección ortográfica|
|[SpellcheckLanguage](#spellchecklanguage)|Habilite idiomas de revisión ortográfica específicos|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Forzar deshabilitar idioma de revisión ortográfica|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Permitir el tratamiento más estricto de contenido mixto (en desuso)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Suprimir la advertencia de SO no compatible|
|[SyncDisabled](#syncdisabled)|Deshabilitar la sincronización de datos con servicios de sincronización de Microsoft|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Configurar la lista de tipos que se excluyen de la sincronización|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Habilitar una característica de seguridad TLS 1.3 para los anclajes de veracidad locales (en desuso)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Especificar los conjuntos de cifrado TLS para deshabilitarlos|
|[TabFreezingEnabled](#tabfreezingenabled)|Permitir el bloqueo de las pestañas en segundo plano|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Habilitar los procesos de finalización en el administrador de tareas del explorador|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Establecer el límite en megabytes de memoria que puede utilizar una única instancia de Microsoft Edge.|
|[TrackingPrevention](#trackingprevention)|Bloquear el seguimiento de la actividad de exploración de los usuarios en la web|
|[TranslateEnabled](#translateenabled)|Habilitar la traducción|
|[URLAllowlist](#urlallowlist)|Definir una lista de direcciones URL permitidas|
|[URLBlocklist](#urlblocklist)|Bloquear el acceso a una lista de direcciones URL|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Habilitar la característica User-Agent Client Hints (en desuso)|
|[UserDataDir](#userdatadir)|Establecer el directorio de datos del usuario|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Limita el número de instantáneas de datos de usuario que se conservan para su uso en caso de reversión de emergencia|
|[UserFeedbackAllowed](#userfeedbackallowed)|Permitir comentarios de los usuarios|
|[VideoCaptureAllowed](#videocaptureallowed)|Permitir o bloquear captura de vídeo|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Sitios que pueden acceder a dispositivos de captura de vídeo sin solicitar permiso|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|Establecer la optimización de WPAD|
|[WebAppInstallForceList](#webappinstallforcelist)|Configurar la lista de aplicaciones web instaladas por la fuerza.|
|[WebCaptureEnabled](#webcaptureenabled)|Habilitar la característica de captura Web en Microsoft Edge|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Nombre de GP: volver a habilitar la API de componentes web v0 hasta M84.|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Permitir que WebDriver reemplace las directivas incompatibles (en desuso)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Administrar la exposición de la dirección IP local por WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Restringir la exposición de la dirección IP local por WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Restringir el rango de puertos UDP locales usados por WebRTC|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Usar la resolución del proxy de Windows (en desuso)|




  ## Directivas de configuración de Protección de aplicaciones

  [Volver al principio](#microsoft-edge---policies)

  ### ApplicationGuardContainerProxy

  #### Contenedor proxy de la Protección de aplicaciones

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 84 o posterior

  #### Descripción

  Configure los parámetros del proxy para la Protección de aplicaciones de Microsoft Edge.
Si habilita esta directiva, la Protección de aplicaciones de Microsoft Edge ignora otras fuentes de configuraciones de proxy.

Si no configura esta directiva, la Protección de aplicaciones de Microsoft Edge utiliza la configuración del proxy del host.

Esta directiva no afecta a la configuración del proxy de Microsoft Edge fuera de la Protección de aplicaciones (en el host).

El campo ProxyMode permite especificar el servidor proxy utilizado por la Protección de aplicaciones Microsoft Edge.

El campo ProxyPacUrl es una dirección URL a un archivo proxy. PAC.

El campo ProxyServer es una URL para el servidor proxy.

Si elige el valor "directo" como "Modo Proxy", todos los demás campos son ignorados.

Si elige el valor "auto_detect" como "ProxyMode", se ignorará todos los demás campos.

Si elige el valor 'fixed_servers' como 'ProxyMode', se utiliza el campo 'ProxyServer'.

Si elige el valor 'pac_script' como 'ProxyMode', se utiliza el campo 'ProxyPacUrl'.

Para obtener más información acerca de cómo identificar el tráfico de Protección de aplicaciones mediante proxy doble, visite [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ApplicationGuardContainerProxy
  - Nombre GP: contenedor proxy de Protección de aplicaciones
  - Ruta GP (Obligatorio): plantillas administrativas/Microsoft Edge/Configuración de la Protección de aplicaciones
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ApplicationGuardContainerProxy
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {"ProxyMode": "direct", "ProxyPacUrl": "https://internal.site/example.pac", "ProxyServer": "123.123.123.123:8080"}
  ```
  

  

  [Volver al principio](#microsoft-edge---policies)

  ## Directivas de transmisión

  [Volver al principio](#microsoft-edge---policies)

  ### EnableMediaRouter

  #### Habilitar Google Cast

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilitar esta directiva para habilitar Google Cast. Los usuarios podrán iniciarlo desde el menú de aplicaciones, los menús contextuales de la página, los controles de medios en los sitios web habilitados para la transmisión y (si se muestra) el icono de la barra de herramientas de transmisión.

Deshabilitar esta directiva para deshabilitar Google Cast.

De forma predeterminada, Google Cast está activado.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EnableMediaRouter
  - Nombre de GP: habilitar Google Cast
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Transmitir
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: EnableMediaRouter
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: EnableMediaRouter
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ShowCastIconInToolbar

  #### Mostrar el icono transmitir en la barra de herramientas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Establecer esta directiva a verdadero para mostrar el icono de la barra de herramientas de Transmitir en la barra de herramientas o el menú de desbordamiento. Los usuarios no podrán eliminarlo.

Si no configura esta directiva o si la deshabilita, los usuarios pueden anclar o quitar el icono utilizando su menú contextual.

Si también ha configurado la directiva [EnableMediaRouter](#enablemediarouter) como falsa, entonces esta directiva se ignora y el icono de la barra de herramientas no se mostrará.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ShowCastIconInToolbar
  - Nombre de GP: mostrar el icono transmitir en la barra de herramientas
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Transmitir
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ShowCastIconInToolbar
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ShowCastIconInToolbar
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Directivas de configuración de contenidos

  [Volver al principio](#microsoft-edge---policies)

  ### AutoSelectCertificateForUrls

  #### Seleccionar automáticamente certificados de cliente para estos sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Setting the policy lets you make a list of URL patterns that specify sites for which Microsoft Edge can automatically select a client certificate. The value is an array of stringified JSON dictionaries, each with the form { "pattern": "$URL_PATTERN", "filter" : $FILTER }, where $URL_PATTERN is a content setting pattern. $FILTER restricts the client certificates the browser automatically selects from. Independent of the filter, only certificates that match the server's certificate request are selected.

Examples for the usage of the $FILTER section:

* When $FILTER is set to { "ISSUER": { "CN": "$ISSUER_CN" } }, only client certificates issued by a certificate with the CommonName $ISSUER_CN are selected.

* When $FILTER contains both the "ISSUER" and the "SUBJECT" sections, only client certificates that satisfy both conditions are selected.

* When $FILTER contains a "SUBJECT" section with the "O" value, a certificate needs at least one organization matching the specified value to be selected.

* When $FILTER contains a "SUBJECT" section with a "OU" value, a certificate needs at least one organizational unit matching the specified value to be selected.

* When $FILTER is set to {}, the selection of client certificates is not additionally restricted. Note that filters provided by the web server still apply.

If you leave the policy unset, there's no autoselection for any site.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AutoSelectCertificateForUrls
  - Nombre de GP: seleccionar automáticamente certificados de cliente para estos sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\AutoSelectCertificateForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AutoSelectCertificateForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### CookiesAllowedForUrls

  #### Permitir las cookies en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Defina una lista de sitios, basada en los patrones de dirección URL, a los que se les permite colocar cookies.

Si no se configura esta directiva se utiliza para todos los sitios el valor global predeterminado de la directiva [DefaultCookiesSetting](#defaultcookiessetting) (si está establecido) o la configuración personal del usuario.

Vea las directivas [CookiesBlockedForUrls](#cookiesblockedforurls) y [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) para más información.

Tenga en cuenta que no puede haber patrones de dirección URL conflictivos establecidos entre estas tres directivas:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Para impedir que se eliminen las cookies al salir, configure la directiva [SaveCookiesOnExit](#savecookiesonexit) .

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: CookiesAllowedForUrls
  - Nombre de GP: permitir las cookies en determinados sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\CookiesAllowedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: CookiesAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### CookiesBlockedForUrls

  #### Bloquear las cookies en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios, basada en los patrones de dirección URL, que no pueden establecer cookies.

Si no se configura esta directiva se utiliza para todos los sitios el valor global predeterminado de la directiva [DefaultCookiesSetting](#defaultcookiessetting) (si está establecido) o la configuración personal del usuario.

Vea las directivas de [CookiesAllowedForUrls](#cookiesallowedforurls) y [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) para más información.

Tenga en cuenta que no puede haber patrones de dirección URL conflictivos establecidos entre estas tres directivas:

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: CookiesBlockedForUrls
  - Nombre de GP: bloquear las cookies en determinados sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\CookiesBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: CookiesBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### CookiesSessionOnlyForUrls

  #### Limitar las cookies de determinados sitios web en la sesión actual

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Las cookies creadas por los sitios web que coinciden con un patrón de dirección URL definido por usted se eliminan cuando termina la sesión (cuando se cierra la ventana).

Las cookies creadas por los sitios web que no coinciden con el patrón son controladas por la directiva [DefaultCookiesSetting](#defaultcookiessetting) (si está establecida) o por la configuración personal del usuario. Este es también el comportamiento por defecto si no se configura esta directiva.

Si Microsoft Edge se ejecuta en segundo plano, es posible que la sesión no se cierre cuando se cierre la última ventana, lo que significa que las cookies no se borrarán cuando se cierre la ventana. Vea la directiva [BackgroundModeEnabled](#backgroundmodeenabled) para obtener información sobre la configuración de lo que sucede cuando Microsoft Edge se ejecuta en el modo segundo plano.

También puede utilizar las directivas [CookiesAllowedForUrls](#cookiesallowedforurls) y [CookiesBlockedForUrls](#cookiesblockedforurls) para controlar qué sitios web pueden crear cookies.

Tenga en cuenta que no puede haber patrones de dirección URL conflictivos establecidos entre estas tres directivas:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Si establece la directiva [RestoreOnStartup](#restoreonstartup) para restaurar las direcciones URL de sesiones anteriores, esta directiva se ignorará y las cookies se almacenarán de forma permanente para esos sitios.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: CookiesSessionOnlyForUrls
  - Nombre de GP: limitar las cookies de determinados sitios web en la sesión actual
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\CookiesSessionOnlyForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: CookiesSessionOnlyForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultCookiesSetting

  #### Configurar cookies

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Controlar si los sitios web pueden crear cookies en el dispositivo del usuario. Esta directiva es todo o nada: puede permitir que todos los sitios web creen cookies o que ningún sitio web cree cookies. No puede utilizar esta directiva para habilitar las cookies de determinados sitios web.

Establecer la directiva en "SessionOnly" para borrar las cookies cuando se cierre la sesión. Si Microsoft Edge se ejecuta en segundo plano, es posible que la sesión no se cierre cuando se cierre la última ventana, lo que significa que las cookies no se borrarán cuando se cierre la ventana. Vea la directiva [BackgroundModeEnabled](#backgroundmodeenabled) para obtener información sobre la configuración de lo que sucede cuando Microsoft Edge se ejecuta en el modo segundo plano.

Si no configura esta directiva, se usará la de "AllowCookies" predeterminada y los usuarios podrán cambiarla en la Configuración de Microsoft Edge. (Si no desea que los usuarios cambien esta configuración, establezca la directiva).

Asignación de opciones de directiva:

* AllowCookies (1) = permitir que todos los sitios creen cookies

* BlockCookies (2) = no permitir que ningún sitio cree cookies

* SessionOnly (4) = guardar las cookies durante toda la duración de la sesión, salvo las que se muestran en [SaveCookiesOnExit](#savecookiesonexit)

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultCookiesSetting
  - Nombre de GP: configurar cookies
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultCookiesSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultCookiesSetting
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultFileSystemReadGuardSetting

  #### Controlar el uso de la API del sistema de archivos para leer

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Si establece esta directiva en 3, los sitios web podrán pedir acceso de lectura al sistema de archivos del sistema operativo del host utilizando la API del sistema de archivos. Si establece esta directiva en 2, se deniega el acceso.

Si no establece esta directiva, los sitios web podrán pedir acceso. Los usuarios pueden cambiar esta configuración.

Asignación de opciones de directiva:

* BlockFileSystemRead (2) = No permitir que ningún sitio solicite acceso de lectura a archivos y directorios mediante la API del sistema de archivos

* AskFileSystemRead (3) = Permitir que los sitios pidan al usuario que otorgue acceso de lectura a archivos y directorios mediante la API del sistema de archivos

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultFileSystemReadGuardSetting
  - Nombre de GP: controla el uso de la API del sistema de archivos para lectura
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultFileSystemReadGuardSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: DefaultFileSystemReadGuardSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultFileSystemWriteGuardSetting

  #### Controlar el uso de la API del sistema de archivos para escribir

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Si establece esta directiva en 3, los sitios web podrán pedir acceso de escritura al sistema de archivos del sistema operativo del host mediante la API del sistema de archivos. Si establece esta directiva en 2, se deniega el acceso.

Si no establece esta directiva, los sitios web podrán pedir acceso. Los usuarios pueden cambiar esta configuración.

Asignación de opciones de directiva:

* BlockFileSystemWrite (2) = No permitir que cualquier sitio solicite acceso de escritura a archivos y directorios

* AskFileSystemWrite (3) = Permitir que los sitios pidan al usuario acceso de escritura a archivos y directorios

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultFileSystemWriteGuardSetting
  - Nombre de GP: controla el uso de la API del sistema de archivos para escribir
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultFileSystemWriteGuardSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: DefaultFileSystemWriteGuardSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultGeolocationSetting

  #### Configuración de geolocalización predeterminada

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Establecer si los sitios web pueden realizar un seguimiento de las ubicaciones físicas de los usuarios. Puede permitir que se realice un seguimiento de forma predeterminada ("AllowGeolocation"), rechazarlo de forma predeterminada ("BlockGeolocation") o preguntar a los usuarios cada vez que un sitio web solicite su ubicación ("AskGeolocation").

Si no configura esta directiva, se usará "AskGeolocation" y el usuario podrá cambiarla.

Asignación de opciones de directiva:

* AllowGeolocation (1) = permitir que los sitios realicen un seguimiento de la ubicación física de los usuarios

* BlockGeolocation (2) = no permitir que ningún sitio realice un seguimiento de la ubicación física de los usuarios

* AskGeolocation (3) = preguntar cuando un sitio quiera realizar un seguimiento de la ubicación física de los usuarios

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultGeolocationSetting
  - Nombre de GP: configuración de geolocalización predeterminada
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultGeolocationSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultGeolocationSetting
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultImagesSetting

  #### Configuración predeterminada de imágenes

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Establecer si los sitios web pueden mostrar imágenes. Puede permitir imágenes en todos los sitios ("AllowImages") o bloquearlas en todos los sitios ("BlockImages").

Si no configura esta directiva, las imágenes se permitirán de forma predeterminada, y el usuario podrá cambiar esta configuración.

Asignación de opciones de directiva:

* AllowImages (1) = permitir que todos los sitios muestren todas las imágenes

* BlockImages (2) = no permitir que ningún sitio muestre imágenes

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultImagesSetting
  - Nombre de GP: configuración predeterminada de imágenes
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultImagesSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultImagesSetting
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultInsecureContentSetting

  #### Controlar el uso de excepciones de contenido inseguro

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Permite establecer si los usuarios pueden agregar excepciones para permitir contenido mixto para sitios determinados.

Esta directiva puede ser anulada para patrones específicos de dirección URL usando las directivas [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) e [InsecureContentBlockedForUrls](#insecurecontentblockedforurls).

Si no se establece esta directiva, los usuarios podrán agregar excepciones para permitir el contenido mixto bloqueable y deshabilitar las actualizaciones automáticas para el contenido mixto bloqueable de forma opcional.

Asignación de opciones de directiva:

* BlockInsecureContent (2) = no permitir que ningún sitio cargue contenido mixto

* AllowExceptionsInsecureContent (3) = permitir que los usuarios agreguen excepciones para admitir contenido mixto

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultInsecureContentSetting
  - Nombre de GP: controlar el uso de excepciones de contenido inseguro
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultInsecureContentSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultInsecureContentSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultJavaScriptSetting

  #### Configuración predeterminada de JavaScript

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Establecer si los sitios web pueden ejecutar JavaScript. Puede permitir el acceso ("AllowJavaScript") o bloquearlo ("BlockJavaScript") para todos los sitios.

Si no configura esta directiva, todos los sitios pueden ejecutar JavaScript de forma predeterminada, y el usuario puede cambiar esta configuración.

Asignación de opciones de directiva:

* AllowJavaScript (1) = permitir que todos los sitios ejecuten JavaScript

* BlockJavaScript (2) = no permitir que ningún sitio ejecute JavaScript

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultJavaScriptSetting
  - Nombre de GP: configuración predeterminada de JavaScript
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultJavaScriptSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultJavaScriptSetting
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultNotificationsSetting

  #### Configuración predeterminada de notificación

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Establecer si los sitios web pueden mostrar notificaciones de escritorio. Puede permitirlas de forma predeterminada ("AllowNotifications"), denegarlas de forma predeterminada ("BlockNotifications") o hacer que se le pregunte al usuario cada vez que un sitio web quiera mostrar una notificación ("AskNotifications").

Si no configura esta directiva, las notificaciones se permitirán de forma predeterminada, y el usuario podrá cambiar esta configuración.

Asignación de opciones de directiva:

* AllowNotifications (1) = permitir que los sitios muestren notificaciones de escritorio

* BlockNotifications (2) = no permitir que ningún sitio muestre notificaciones de escritorio

* AskNotifications (3) = preguntar cada vez que un sitio quiera mostrar notificaciones de escritorio

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultNotificationsSetting
  - Nombre de GP: configuración predeterminada de notificación
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultNotificationsSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultNotificationsSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultPluginsSetting

  #### Configuración predeterminada de Adobe Flash

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  En primer lugar, se comprueban [PluginsAllowedForUrls](#pluginsallowedforurls) y [PluginsBlockedForUrls](#pluginsblockedforurls) y, a continuación, esta directiva. Las opciones son "ClickToPlay" y "BlockPlugins". Si establece esta directiva en "BlockPlugins", este complemento será denegado para todos los sitios web. "ClickToPlay" permite ejecutar el complemento Flash, pero los usuarios deben hacer clic en el marcador de posición para iniciarlo.

Si no configura esta directiva, el usuario puede cambiar esta configuración manualmente.

Nota: la reproducción automática es solo para los dominios que aparecen explícitamente en la directiva de [PluginsAllowedForUrls](#pluginsallowedforurls). Para activar la reproducción automática en todos los sitios, agregue http://* y https://* a la lista de direcciones URL permitidas.

Asignación de opciones de directiva:

* BlockPlugins (2) = bloquear el complemento de Adobe Flash

* ClickToPlay (3) = hacer clic para reproducir

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultPluginsSetting
  - Nombre de GP: configuración predeterminada de Adobe Flash
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultPluginsSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultPluginsSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultPopupsSetting

  #### Configuración predeterminada de la ventana emergente

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Establecer si los sitios web pueden mostrar ventanas emergentes. Puede permitirlas ("AllowPopups") o bloquearlas ("BlockPopups") en todos los sitios web.

Si no configura esta directiva, las ventanas emergentes se bloquearán de forma predeterminada y el usuario podrá cambiar esta configuración.

Asignación de opciones de directiva:

* AllowPopups (1) = permitir que todos los sitios muestren ventanas emergentes

* BlockPopups (2) = no permitir que ningún sitio muestre mensajes emergentes

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultPopupsSetting
  - Nombre de GP: configuración predeterminada de la ventana emergente
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultPopupsSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultPopupsSetting
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultWebBluetoothGuardSetting

  #### Controlar el uso de la API de Bluetooth Web

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Controla si los sitios web pueden acceder a los dispositivos Bluetooth cercanos. Puede bloquear completamente el acceso o requerir que el sitio le pregunte a los usuarios cada vez que deseen tener acceso a un dispositivo Bluetooth.

Si no configura esta directiva, se utilizará el valor predeterminado ("AskWebBluetooth", lo que significa que se preguntará a los usuarios cada vez) y los usuarios pueden cambiarlo.

Asignación de opciones de directiva:

* BlockWebBluetooth (2) = no permitir que ningún sitio solicite el acceso a dispositivos Bluetooth mediante la API de Bluetooth Web

* AskWebBluetooth (3) = permitir que los sitios soliciten al usuario que conceda acceso a un dispositivo Bluetooth cercano

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultWebBluetoothGuardSetting
  - Nombre de GP: controlar el uso de la API de Bluetooth Web
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultWebBluetoothGuardSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultWebBluetoothGuardSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultWebUsbGuardSetting

  #### Controlar el uso de la API WebUSB

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Establecer si los sitios web pueden acceder a dispositivos USB conectados. Puede bloquear completamente el acceso o preguntar al usuario cada vez que un sitio web quiera acceder a los dispositivos USB conectados.

Puede reemplazar esta directiva para patrones determinados de dirección URL utilizando las directivas [WebUsbAskForUrls](#webusbaskforurls) y [WebUsbBlockedForUrls](#webusbblockedforurls).

Si no configura esta directiva, los sitios pueden preguntar a los usuarios si pueden acceder a los dispositivos USB conectados ("AskWebUsb") de forma predeterminada, y los usuarios pueden cambiar esta configuración.

Asignación de opciones de directiva:

* BlockWebUsb (2) = no permitir que ningún sitio solicite el acceso a dispositivos USB mediante la API WebUSB

* AskWebUsb (3) = permitir que los sitios soliciten al usuario conceder acceso a un dispositivo USB conectado

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultWebUsbGuardSetting
  - Nombre de GP: Nombre de GP: controlar el uso de la API WebUSB
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultWebUsbGuardSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultWebUsbGuardSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### FileSystemReadAskForUrls

  #### Permitir el acceso de lectura a través de la API del sistema de archivos en estos sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  El establecimiento de la directiva permite indicar los patrones de dirección URL que especifican los sitios que pueden pedir a los usuarios acceso de lectura a archivos o directorios del sistema de archivos del sistema operativo del host mediante la API del sistema de archivos.

Dejar la directiva sin establecer significa que [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) se aplicará a todos los sitios, si está establecido. Si no es así, se aplica la configuración personal de los usuarios.

Los patrones de dirección URL no pueden entrar en conflicto con [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls). Ninguna de las directivas tiene prioridad si una dirección URL coincide con ambas.

Para información detallada sobre los patrones de dirección URL válidos, consulte https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: FileSystemReadAskForUrls
  - Nombre de GP: permitir el acceso de lectura a través de la API del sistema de archivos en estos sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: FileSystemReadAskForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### FileSystemReadBlockedForUrls

  #### Bloquear el acceso de lectura a través de la API del sistema de archivos en estos sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Si define esta directiva, puedes listar los patrones de dirección URL que especifican los sitios que no pueden pedir a los usuarios acceso de lectura a archivos o directorios del sistema de archivos del sistema operativo de host mediante la API del sistema de archivos.

Si no define esta directiva, [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) se aplicará a todos los sitios, si está establecido. Si no es así, se aplica la configuración personal de los usuarios.

Los patrones de dirección URL no pueden entrar en conflicto con [FileSystemReadAskForUrls](#filesystemreadaskforurls). Ninguna de las directivas tiene prioridad si una dirección URL coincide con ambas.

Para información detallada sobre los patrones de dirección URL válidos, consulte https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: FileSystemReadBlockedForUrls
  - Nombre de GP: bloquear el acceso de lectura a través de la API del sistema de archivos en estos sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: FileSystemReadBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### FileSystemWriteAskForUrls

  #### Permitir el acceso de escritura a archivos y directorios en estos sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Si define esta directiva, puede listar los patrones de dirección URL que especifican los sitios que pueden pedir a los usuarios acceso de escritura a archivos o directorios del sistema de archivos en el sistema operativo del host.

Si no define esta directiva, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) se aplicará a todos los sitios, si está establecido. Si no es así, se aplica la configuración personal de los usuarios.

Los patrones de dirección URL no pueden entrar en conflicto con [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls). Ninguna de las directivas tiene prioridad si una dirección URL coincide con ambas.

Para información detallada sobre los patrones de dirección URL válidos, consulte https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: FileSystemWriteAskForUrls
  - Nombre de GP: permitir el acceso de escritura a archivos y directorios en estos sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: FileSystemWriteAskForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### FileSystemWriteBlockedForUrls

  #### Bloquear el acceso de escritura a archivos y directorios en estos sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Si define esta directiva, puede listar los patrones de dirección URL que especifican los sitios que no pueden pedir a los usuarios acceso de escritura a archivos o directorios en el sistema de archivos del sistema operativo del host.

Si no define esta directiva, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) se aplicará a todos los sitios, si está establecido. Si no es así, se aplica la configuración personal de los usuarios.

Los patrones de dirección URL no pueden entrar en conflicto con [FileSystemWriteAskForUrls](#filesystemwriteaskforurls). Ninguna de las directivas tiene prioridad si una dirección URL coincide con ambas.

Para información detallada sobre los patrones de dirección URL válidos, consulte https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: FileSystemWriteBlockedForUrls
  - Nombre de GP: bloquear el acceso de escritura a archivos y directorios en estos sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: FileSystemWriteBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImagesAllowedForUrls

  #### Permitir imágenes en estos sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios, basada en los patrones de dirección URL que pueden mostrar imagenes.

Si no configura esta directiva, se utiliza el valor predeterminado global para todos los sitios, ya sea de la directiva [DefaultImagesSetting](#defaultimagessetting) (si está establecida) o de la configuración personal del usuario.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImagesAllowedForUrls
  - Nombre de GP: permitir imágenes en estos sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Microsoft Edge\ImagesAllowedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImagesAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImagesBlockedForUrls

  #### Bloquear imágenes en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios, basada en los patrones de dirección URL que pueden mostrar imagenes.

Si no se configura esta directiva, se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultImagesSetting](#defaultimagessetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImagesBlockedForUrls
  - Nombre de GP: Nombre de GP: bloquear imágenes en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Microsoft Edge\ImagesBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImagesBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### InsecureContentAllowedForUrls

  #### Permitir el contenido inseguro en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Crea una lista de patrones de dirección URL para especificar los sitios que pueden mostrar contenido mixto inseguro (es decir, contenido HTTP en sitios HTTPS).

Si no configura esta directiva, el contenido mixto bloqueable será bloqueado y opcionalmente el contenido mixto bloqueable será actualizado. Sin embargo, se permitirá a los usuarios establecer excepciones para permitir contenido mixto inseguro para determinados sitios.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: InsecureContentAllowedForUrls
  - Nombre de GP: permitir el contenido inseguro en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Microsoft Edge\InsecureContentAllowedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: InsecureContentAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### InsecureContentBlockedForUrls

  #### Bloquear contenidos inseguros en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Crea una lista de patrones de URL para especificar los sitios a los que no se les permite mostrar contenido mixto (es decir, contenido HTTP en sitios HTTPS) bloqueable (es decir, activo) y para los que se deshabilitarán opcionalmente las actualizaciones de contenido mixto bloqueable.

Si no configura esta directiva, el contenido mixto bloqueable será bloqueado y opcionalmente el contenido mixto bloqueable será actualizado. Sin embargo, se permitirá a los usuarios establecer excepciones para permitir contenido mixto inseguro para determinados sitios.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: InsecureContentBlockedForUrls
  - Nombre de GP: bloquear los contenidos inseguros en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Microsoft Edge\InsecureContentBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: InsecureContentBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### JavaScriptAllowedForUrls

  #### Permitir JavaScript en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios basada en los patrones de dirección URL a los que se les permite ejecutar JavaScript.

Si no configura esta directiva, se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultJavaScriptSetting](#defaultjavascriptsetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: JavaScriptAllowedForUrls
  - Nombre de GP: permitir JavaScript en determinados sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Microsoft Edge\JavaScriptAllowedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: JavaScriptAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### JavaScriptBlockedForUrls

  #### Bloquear JavaScript en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios basada en los patrones de dirección URL a los que se les permite ejecutar JavaScript.

Si no configura esta directiva, se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultJavaScriptSetting](#defaultjavascriptsetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: JavaScriptBlockedForUrls
  - Nombre de GP: bloquear JavaScript en determinados sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: JavaScriptBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabled

  #### Habilitar la configuración predeterminada del comportamiento de las cookies de SameSite

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Permite revertir todas las cookies al comportamiento de SameSite heredado. Reverting to legacy behavior causes cookies that don't specify a SameSite attribute to be treated as if they were "SameSite=None", removes the requirement for "SameSite=None" cookies to carry the "Secure" attribute, and skips the scheme comparison when evaluating if two sites are same-site.

If you don't set this policy, the default SameSite behavior for cookies will depend on other configuration sources for the SameSite-by-default feature, the Cookies-without-SameSite-must-be-secure feature, and the Schemeful Same-Site feature. These features can also be configured by a field trial or the same-site-by-default-cookies flag, the cookies-without-same-site-must-be-secure flag, or the schemeful-same-site flag in edge://flags.

Asignación de opciones de directiva:

* DefaultToLegacySameSiteCookieBehavior (1) = revertir al comportamiento de SameSite heredado para las cookies en todos los sitios.

* DefaultToSameSiteByDefaultCookieBehavior (2) = usar el comportamiento de SameSite predeterminado para las cookies en todos los sitios

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: LegacySameSiteCookieBehaviorEnabled
  - Nombre de GP: habilitar la configuración predeterminada del comportamiento heredado de las cookies de SameSite
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: LegacySameSiteCookieBehaviorEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: LegacySameSiteCookieBehaviorEnabled
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList

  #### Revertir a la conducta heredada de SameSite para las cookies en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Las cookies establecidas para los dominios que coincidan con los patrones determinados revertirán al comportamiento heredado de SameSite.

Reverting to legacy behavior causes cookies that don't specify a SameSite attribute to be treated as if they were "SameSite=None", removes the requirement for "SameSite=None" cookies to carry the "Secure" attribute, and skips the scheme comparison when evaluating if two sites are same-site.

Si no establece esta directiva, se usará el valor predeterminado global. El valor predeterminado global también se utilizará para las cookies de los dominios no cubiertos por los patrones especificados.

El valor predeterminado global puede ser configurado usando la directiva [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled). Si [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) no está establecido, el valor global predeterminado pasará a otras fuentes de configuración.

Tenga en cuenta que los patrones listados en esta directiva se tratan como dominios, no como dirección URL, por lo que no debe especificar un esquema o un puerto.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Nombre de GP: volver a la conducta heredada de SameSite para las cookies en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Valor de ejemplo:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NotificationsAllowedForUrls

  #### Permitir las notificaciones en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite crear una lista de patrones de url para especificar los sitios que están autorizados a mostrar notificaciones.

Si no establece esta directiva, se utilizará el valor predeterminado global para todos los sitios. Este valor predeterminado será de la directiva[DefaultNotificationsSetting](#defaultnotificationssetting)de configuración de notificaciones predeterminadas, si está establecida, o de la configuración personal del usuario. Para obtener información detallada sobre los patrones de url válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NotificationsAllowedForUrls
  - Nombre de GP: permitir las notificaciones en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\NotificationsAllowedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NotificationsAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NotificationsBlockedForUrls

  #### Bloquear las notificaciones en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite crear una lista de patrones de url para especificar los sitios que no están autorizados a mostrar notificaciones.

Si no establece esta directiva, se utilizará el valor predeterminado global para todos los sitios. Este valor predeterminado será de la directiva[DefaultNotificationsSetting](#defaultnotificationssetting)de configuración de notificaciones predeterminadas, si está establecida, o de la configuración personal del usuario. Para obtener información detallada sobre los patrones de url válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NotificationsBlockedForUrls
  - Nombre de GP: bloquear las notificaciones en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\NotificationsBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NotificationsBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PluginsAllowedForUrls

  #### Permitir el complemento Adobe Flash en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios, basada en los patrones de dirección URL que pueden ejecutar el complemento de Adobe Flash.

Si no configura esta directiva, se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultPluginsSetting](#defaultpluginssetting) (si está establecido) o la configuración personal del usuario.

Para obtener información detallada sobre los patrones de url válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Sin embargo, a partir de M85, los patrones con carácteres comodín de "*" y "[*.]" en el host ya no son compatibles con esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PluginsAllowedForUrls
  - Nombre de GP: permitir el complemento de Adobe Flash en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\PluginsAllowedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PluginsAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PluginsBlockedForUrls

  #### Bloquear el complemento Adobe Flash en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios basada en los patrones de dirección URL que están bloqueados para ejecutar Adobe Flash.

Si no configura esta directiva, se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultPluginsSetting](#defaultpluginssetting) (si está establecido) o la configuración personal del usuario.

Para obtener información detallada sobre los patrones de url válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Sin embargo, a partir de M85, los patrones con carácteres comodín de "*" y "[*.]" en el host ya no son compatibles con esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PluginsBlockedForUrls
  - Nombre de GP: bloquear el complemento Adobe Flash en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\PluginsBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PluginsBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PopupsAllowedForUrls

  #### Permitir ventanas emergentes en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios basada en los patrones de dirección URL que puedan abrir ventanas emergentes.

Si no configura esta directiva se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultPopupsSetting](#defaultpopupssetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PopupsAllowedForUrls
  - Nombre de GP: permitir las ventanas emergentes en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\PopupsAllowedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PopupsAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PopupsBlockedForUrls

  #### Bloquear ventanas emergentes en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios basada en los patrones de dirección URL que están bloqueados para abrir ventanas emergentes.

Si no configura esta directiva se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultPopupsSetting](#defaultpopupssetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PopupsBlockedForUrls
  - Nombre de GP: bloquear las ventanas emergentes en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\PopupsBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PopupsBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### RegisteredProtocolHandlers

  #### Registrar controladores de protocolo

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Establezca esta directiva (recomendado únicamente) para registrar una lista de controladores de protocolo. Esta lista se combina con las registradas por el usuario y ambas pueden usarse.

Para registrar un controlador de protocolo:

- Establezca la propiedad Protocol en el esquema (por ejemplo, "mailto").
- Establezca la propiedad URL en la propiedad URL de la aplicación que controla el esquema especificado en el campo "protocol". El patrón puede incluir un marcador de posición "%s", que será reemplazado por la dirección URL controlada.

Los usuarios no pueden quitar un controlador de protocolo registrado por esta directiva. Sin embargo, pueden instalar un controlador de protocolo predeterminado nuevo para reemplazar a los controladores de protocolo existentes.

  #### Características admitidas:

  - Puede ser obligatorio: no
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RegisteredProtocolHandlers
  - Nombre de GP: registrar controladores de protocolo
  - Ruta de acceso de GP (obligatorio): N/D
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Configuración de contenido
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatorio): N/D
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: RegisteredProtocolHandlers
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [{"default": true, "protocol": "mailto", "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"}]
  ```
  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: RegisteredProtocolHandlers
  - Valor de ejemplo:
``` xml
<key>RegisteredProtocolHandlers</key>
<array>
  <dict>
    <key>default</key>
    <true/>
    <key>protocol</key>
    <string>mailto</string>
    <key>url</key>
    <string>https://mail.contoso.com/mail/?extsrc=mailto&url=%s</string>
  </dict>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SpotlightExperiencesAndRecommendationsEnabled

  #### Decida si los usuarios pueden recibir imágenes de fondo y texto personalizados, sugerencias, notificaciones
y sugerencias para los servicios Microsoft

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 86 o posterior

  #### Descripción

  Decida si los usuarios pueden recibir imágenes de fondo y texto personalizados, sugerencias, notificaciones y sugerencias para los servicios Microsoft.

Si habilita o no configura esta opción, las experiencias destacadas y las recomendaciones se activarán.

Si deshabilita esta opción, las experiencias destacadas y las recomendaciones se desactivarán.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SpotlightExperiencesAndRecommendationsEnabled
  - Nombre de GP: decida si los usuarios pueden recibir imágenes de fondo y texto personalizados, sugerencias, notificaciones y sugerencias para los servicios Microsoft
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre de valor: SpotlightExperiencesAndRecommendationsEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### WebUsbAllowDevicesForUrls

  #### Conceder acceso a determinados sitios para conectarse a dispositivos USB determinados

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite establecer una lista de direcciones URL que especifican los sitios a los que se concederá automáticamente permiso de acceso a un dispositivo USB con el proveedor y los id. de producto dados. Cada elemento de la lista debe contener tanto dispositivos como direcciones url para que la directiva sea válida. Cada elemento de los dispositivos puede contener un id. de proveedor y un campo de id. de producto. Cualquier id. que se omite se trata como un comodín con una excepción, y esa excepción es que no se puede especificar una id. de producto sin que se especifique también una id. de proveedor. De lo contrario, la directiva no será válida y será ignorada.

El modelo de permiso de USB utiliza la dirección URL del sitio solicitante ("URL de solicitud") y la dirección URL del sitio de marco de nivel superior ("URL de incrustación") para conceder permiso a la dirección URL solicitante para acceder al dispositivo USB. La dirección URL de solicitud puede ser diferente de la URL de incrustación cuando el sitio que realiza la solicitud se carga en un iframe. Por lo tanto, el campo "direcciones URL" puede contener hasta dos cadenas de direcciones URL delimitadas por una coma para especificar la dirección URL de solicitud y de incrustación respectivamente. Si se especifica solo una dirección URL, el acceso a los dispositivos USB correspondientes se concederá cuando la dirección URL del sitio que realiza la solicitud coincida con esta URL, independientemente del estado de incrustación. Las direcciones URL en "direcciones URL" deben ser direcciones URL válidas, de lo contrario, se omitirá la directiva.

Si no establece esta directiva se utilizará el valor global predeterminado para todos los sitios, ya sea de la directiva [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) si está establecida o en caso contrario de la configuración personal del usuario.

Los patrones de URL en esta directiva no deben entrar en conflicto con los configurados a través de [WebUsbBlockedForUrls](#webusbblockedforurls). Si hay un conflicto, esta directiva tendrá prioridad sobre [WebUsbBlockedForUrls](#webusbblockedforurls) y [WebUsbAskForUrls](#webusbaskforurls).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WebUsbAllowDevicesForUrls
  - Nombre de GP: conceder acceso a sitios determinados para conectarse a dispositivos USB específicos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: WebUsbAllowDevicesForUrls
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [
  {
    "devices": [
      {
        "product_id": 5678, 
        "vendor_id": 1234
      }
    ], 
    "urls": [
      "https://contoso.com", 
      "https://fabrikam.com"
    ]
  }
]
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [{"devices": [{"product_id": 5678, "vendor_id": 1234}], "urls": ["https://contoso.com", "https://fabrikam.com"]}]
  ```
  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: WebUsbAllowDevicesForUrls
  - Valor de ejemplo:
``` xml
<key>WebUsbAllowDevicesForUrls</key>
<array>
  <dict>
    <key>devices</key>
    <array>
      <dict>
        <key>product_id</key>
        <integer>5678</integer>
        <key>vendor_id</key>
        <integer>1234</integer>
      </dict>
    </array>
    <key>urls</key>
    <array>
      <string>https://contoso.com</string>
      <string>https://fabrikam.com</string>
    </array>
  </dict>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WebUsbAskForUrls

  #### Permitir WebUSB en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios basada en patrones de dirección URL que pueden pedir al usuario acceso a un dispositivo USB.

Si no configura esta directiva se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

Los patrones de dirección URL definidos en esta directiva no pueden entrar en conflicto con los configurados en la directiva [WebUsbBlockedForUrls](#webusbblockedforurls), no se puede permitir ni bloquear una dirección URL. Para información detallada sobre los patrones de url válidos, consulte[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WebUsbAskForUrls
  - Nombre de GP: permitir WebUSB en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\WebUsbAskForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: WebUsbAskForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WebUsbBlockedForUrls

  #### Bloquear WebUSB en determinados sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios basada en patrones de dirección URL que no pueden pedir al usuario que les conceda acceso a un dispositivo USB.

Si no configura esta directiva se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

Los patrones de dirección URL en esta directiva no pueden entrar en conflicto con los configurados en la directiva [WebUsbAskForUrls](#webusbaskforurls). No puede permitir y bloquear una dirección URL.  Para obtener información detallada sobre los patrones de url válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WebUsbBlockedForUrls
  - Nombre de GP: bloquear WebUSB en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\WebUsbBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: WebUsbBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Directivas del proveedor de búsqueda predeterminado

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSearchProviderEnabled

  #### Habilitar el proveedor de búsquedas predeterminado

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilita la posibilidad de utilizar un proveedor de búsqueda predeterminado.

Si habilita esta directiva un usuario puede buscar un término escribiendo en la barra de direcciones (siempre y cuando lo que escriba no sea una URL).

Puede especificar el proveedor de búsqueda predeterminado que se utilizará habilitando el resto de las directivas de búsqueda predeterminadas. Si éstos se dejan vacíos (no configurados) o se configuran incorrectamente, el usuario podrá elegir el proveedor predeterminado.

Si se deshabilita esta directiva, el usuario no podrá buscar desde la barra de direcciones.

Si habilita o deshabilita esta directiva, los usuarios no podrán cambiarla ni reemplazarla.

Si no configura esta política se habilita el proveedor de búsqueda predeterminado y el usuario puede elegir el proveedor de búsqueda predeterminado además de configurar la lista de proveedores de búsqueda.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

A partir de Microsoft Edge 84, puede establecer esta directiva como Directiva recomendada.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSearchProviderEnabled
  - Nombre de GP: habilitar el proveedor de búsquedas predeterminado
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge/Proveedor de búsqueda predeterminado
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Proveedor de búsquedas predeterminado
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: DefaultSearchProviderEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSearchProviderEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSearchProviderEncodings

  #### Codificaciones de proveedores de búsqueda predeterminadas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifique las codificaciones de caracteres admitidas por el proveedor de búsquedas. Las codificaciones son nombres de página de códigos como UTF-8, GB2312 e ISO-8859-1. Se prueban en el orden indicado.

Esta directiva es opcional. Si no se configura, se utilizará el valor predeterminado UTF-8.

Esta directiva solo se aplica si habilita las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, puede establecer esta directiva como Directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsquedas predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que puede elegir el usuario. Si este es el comportamiento deseado, utilice la Directiva de [ ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSearchProviderEncodings
  - Nombre de GP: codificaciones de proveedores de búsqueda por defecto
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge/Proveedor de búsqueda predeterminado
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Proveedor de búsquedas predeterminado
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\DefaultSearchProviderEncodings
  - Ruta de acceso (recomendada): SOFTWARE\Policies\Microsoft\Edge\Recommended\DefaultSearchProviderEncodings
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSearchProviderEncodings
  - Valor de ejemplo:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURL

  #### Especifica la característica de búsqueda por imagen para el proveedor de búsquedas predeterminado.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica la dirección URL del motor de búsqueda utilizado para la búsqueda de imágenes. Las solicitudes de búsqueda se envían mediante el método GET.

Esta directiva es opcional. Si no la configura, la búsqueda de imágenes no estará disponible.

Especifique la dirección URL de la búsqueda de imágenes de Bing como: '{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'.

Especifique la dirección URL de la búsqueda de imágenes de Google como: '{google:baseURL}searchbyimage/upload'.

Vea la directiva [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) para terminar de configurar la búsqueda de imágenes.

Esta directiva solo se aplica si habilita las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, puede establecer esta directiva como Directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsquedas predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que puede elegir el usuario. Si este es el comportamiento deseado, utilice la Directiva de [ ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSearchProviderImageURL
  - Nombre de GP: especifica la característica de búsqueda por imagen para el proveedor de búsquedas predeterminado
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge/Proveedor de búsqueda predeterminado
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Proveedor de búsquedas predeterminado
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: DefaultSearchProviderImageURL
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSearchProviderImageURL
  - Valor de ejemplo:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURLPostParams

  #### Parámetros para una URL de imagen que utiliza POST

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Si habilita esta directiva, especificará los parámetros que se utilizan cuando se realiza una búsqueda de imágenes que utiliza POST. La directiva consiste en pares nombre/valor separados por comas. Si un valor es un parámetro de plantilla como {imageThumbnail} en el ejemplo anterior, se reemplaza con datos de miniaturas de imágenes reales. Esta directiva solo se aplica si habilita las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Especifica la dirección URL de búsqueda de imágenes desde los parámetros post de Bing como: 'imageBin={google:imageThumbnailBase64}'.

Especifica la dirección URL de búsqueda de imágenes de los parámetros post de Google como: 'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'.

Si no establece esta directiva, las solicitudes de búsqueda de imágenes se envían mediante el método GET.

A partir de Microsoft Edge 84, puede establecer esta directiva como Directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsquedas predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que puede elegir el usuario. Si este es el comportamiento deseado, utilice la Directiva de [ ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSearchProviderImageURLPostParams
  - Nombre de GP: parámetros para una dirección URL de imagen que utiliza POST
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge/Proveedor de búsqueda predeterminado
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Proveedor de búsquedas predeterminado
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: DefaultSearchProviderImageURLPostParams
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSearchProviderImageURLPostParams
  - Valor de ejemplo:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSearchProviderKeyword

  #### Proveedor de palabras clave predeterminado

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica la palabra clave, que es el método abreviado que se usa en la barra de direcciones para desencadenar la búsqueda de este proveedor.

Esta directiva es opcional. Si no lo configura, ninguna palabra clave activará el proveedor de búsquedas.

Esta directiva solo se aplica si habilita las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, puede establecer esta directiva como Directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsquedas predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que puede elegir el usuario. Si este es el comportamiento deseado, utilice la Directiva de [ ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSearchProviderKeyword
  - Nombre de GP: palabra clave del proveedor de búsquedas predeterminado
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge/Proveedor de búsqueda predeterminado
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Proveedor de búsquedas predeterminado
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: DefaultSearchProviderKeyword
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"mis"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSearchProviderKeyword
  - Valor de ejemplo:
``` xml
<string>mis</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSearchProviderName

  #### Nombre del proveedor de búsquedas predeterminado

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica el nombre del proveedor de búsquedas predeterminado.

Si habilita esta directiva, establece el nombre del proveedor de búsqueda predeterminado.

Si no habilita esta directiva o la deja vacía, se utilizará el nombre del servidor especificado por la dirección URL de búsqueda.

"DefaultSearchProviderName" debe establecerse en un proveedor de búsqueda cifradas aprobado por la organización que se corresponda con el proveedor de búsquedas cifradas definido en DTBC-0008. Esta directiva solo se aplica si habilita las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, puede establecer esta directiva como Directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsquedas predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que puede elegir el usuario. Si este es el comportamiento deseado, utilice la Directiva de [ ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSearchProviderName
  - Nombre de GP: nombre del proveedor de búsquedas predeterminado
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge/Proveedor de búsqueda predeterminado
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Proveedor de búsquedas predeterminado
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: DefaultSearchProviderName
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"My Intranet Search"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSearchProviderName
  - Valor de ejemplo:
``` xml
<string>My Intranet Search</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSearchProviderSearchURL

  #### URL de búsqueda del proveedor de búsqueda predeterminado

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica la dirección URL del motor de búsqueda utilizado para la búsqueda predeterminado. La dirección URL contiene la cadena "{searchTerms}", que se reemplaza en el momento de la consulta por los términos que está buscando el usuario.

Especifica la dirección URL de búsqueda de Bing como:

'{bing:baseURL}search?q={searchTerms}'.

Especifique la dirección URL de la búsqueda de Google como: '{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'.

Esta directiva es necesaria cuando se habilita la directiva de [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) si no habilita esta última directiva, se omitirá.

A partir de Microsoft Edge 84, puede establecer esta directiva como Directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsquedas predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que puede elegir el usuario. Si este es el comportamiento deseado, utilice la Directiva de [ ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSearchProviderSearchURL
  - Nombre de GP: dirección URL de búsqueda para el proveedor de búsqueda predeterminado
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge/Proveedor de búsqueda predeterminado
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Proveedor de búsquedas predeterminado
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: DefaultSearchProviderSearchURL
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSearchProviderSearchURL
  - Valor de ejemplo:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSearchProviderSuggestURL

  #### URL del proveedor de búsqueda predeterminado para sugerencias

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica la dirección URL del motor de búsqueda utilizado para ofrecer sugerencias de búsqueda. La dirección URL contiene la cadena "{searchTerms}", que se reemplaza en el momento de la consulta por el texto que el usuario ha introducido de momento.

Esta directiva es opcional. Si no lo configuras, los usuarios no verán sugerencias de búsqueda; verán sugerencias de su historial de exploración y de sus favoritos.

La dirección URL sugerida por Bing puede ser especificada como:

'{bing:baseURL}qbox?query={searchTerms}'.

La dirección URL sugerida por Google se puede especificar como: '{google:baseURL}complete/search?output=chrome&q={searchTerms}'.

Esta directiva solo se aplica si habilita las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, puede establecer esta directiva como Directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsquedas predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que puede elegir el usuario. Si este es el comportamiento deseado, utilice la Directiva de [ ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSearchProviderSuggestURL
  - Nombre de GP: dirección URL del proveedor de búsqueda predeterminado para sugerencias
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge/Proveedor de búsqueda predeterminado
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Proveedor de búsquedas predeterminado
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: DefaultSearchProviderSuggestURL
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSearchProviderSuggestURL
  - Valor de ejemplo:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NewTabPageSearchBox

  #### Configurar la nueva experiencia del cuadro de búsqueda de la página de pestañas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 85 o posterior

  #### Descripción

  Puede configurar el cuadro de búsqueda de la página de la nueva pestaña para que use "cuadro de búsqueda (recomendado)" o "barra de direcciones" para buscar en nuevas pestañas. Esta directiva solo funciona si configura el motor de búsqueda en un valor distinto de Bing al establecer las dos directivas siguientes: [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

 Si deshabilita o no configura esta directiva:

- Si el motor de búsqueda predeterminado de la barra de direcciones es Bing, en la página de la nueva pestaña se usa el cuadro de búsqueda para buscar en nuevas pestañas.
- Si el motor de búsqueda predeterminado de la barra de direcciones no es de Bing, se ofrece a los usuarios una opción adicional (use "barra de direcciones") al buscar en nuevas pestañas.


Si habilita esta directiva y la configura como:

- "Cuadro de búsqueda (recomendado)" (' Bing '), en la página de la nueva pestaña se usa el cuadro de búsqueda para buscar en nuevas pestañas.
- "Barra de direcciones" ("redirigir"), el cuadro de búsqueda de la página de la nueva pestaña usa la barra de direcciones para buscar en nuevas pestañas.

Asignación de opciones de directiva:

* Bing (bing) = cuadro de búsqueda (recomendado)

* redirigir (redirigir) = barra de direcciones

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NewTabPageSetFeedType
  - Nombre GP: configurar la nueva página de la pestaña buscar en el cuadro de búsqueda
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge/Proveedor de búsqueda predeterminado
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Proveedor de búsquedas predeterminado
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: NewTabPageSearchBox
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"bing"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NewTabPageSetFeedType
  - Valor de ejemplo:
``` xml
<string>bing</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Extensiones de las directivas

  [Volver al principio](#microsoft-edge---policies)

  ### ExtensionAllowedTypes

  #### Configurar los tipos de extensión permitidos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Controla qué tipos de extensión se pueden instalar y limita el acceso en tiempo de ejecución.

Esta configuración define los tipos de extensiones permitidas y los hosts con los que pueden interactuar. El valor es una lista de cadenas, cada una de las cuales debe ser una de las siguientes: "extension", "theme", "user_script", y "hosted_app". Vea la documentación de las extensiones de Microsoft Edge para obtener más información sobre estos tipos.

Tenga en cuenta que esta directiva también afecta a las extensiones que se instalen a la fuerza mediante el uso de la directiva [ExtensionInstallForcelist](#extensioninstallforcelist).

Si habilita esta directiva, solo se instalarán las extensiones que coincidan con un tipo de la lista.

Si no configura esta directiva, no se aplicarán restricciones a los tipos de extensión aceptables.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ExtensionAllowedTypes
  - Nombre de GP: configurar los tipos de extensiones permitidas
  - Ruta de acceso de GP: (obligatoria): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\ExtensionAllowedTypes
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ExtensionAllowedTypes
  - Valor de ejemplo:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ExtensionInstallAllowlist

  #### Permitir que se instalen extensiones específicas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Se permiten todas las extensiones de forma predeterminada. Sin embargo, si bloquea todas las extensiones configurando la directiva "ExtensionInstallBlockList" en "*", los usuarios solo podrán instalar las extensiones definidas en esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ExtensionInstallAllowlist
  - Nombre de GP: permitir la instalación de extensiones específicas
  - Ruta de acceso de GP: (obligatoria): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\ExtensionInstallAllowlist
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ExtensionInstallAllowlist
  - Valor de ejemplo:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ExtensionInstallBlocklist

  #### Controlar qué extensiones no se pueden instalar

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Lista extensiones específicas que los usuarios no pueden instalar en Microsoft Edge. Al implementar esta directiva cualquier extensión de esta lista que haya sido instalada previamente será deshabilitada y el usuario no podrá habilitarla. Si elimina un elemento de la lista de extensiones bloqueadas, esa extensión se volverá a habilitar automáticamente en cualquier lugar en el que se haya instalado previamente.

Use "*" para bloquear todas las extensiones que no estén explícitamente listadas en la lista de permisos.

Si no configura esta directiva los usuarios podrán instalar cualquier extensión en Microsoft Edge.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ExtensionInstallBlocklist
  - Nombre de GP: controlar qué extensiones no pueden ser instaladas
  - Ruta de acceso de GP: (obligatoria): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\ExtensionInstallBlocklist
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ExtensionInstallBlocklist
  - Valor de ejemplo:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ExtensionInstallForcelist

  #### Controlar qué extensiones se instalan de forma silenciosa

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica las extensiones que se instalan silenciosamente, sin interacción del usuario, y que los usuarios no pueden desinstalar ni deshabilitar ("forzar instalación"). Todos los permisos solicitados por las extensiones se conceden de forma implícita, sin interacción del usuario, incluyendo todos los permisos adicionales solicitados por las futuras versiones de la extensión. Además, se conceden permisos para las API de extensión enterprise.deviceAttributes y enterprise.platformKeys. (Estas dos API sólo están disponibles para las extensiones que se instalan a la fuerza).

Esta directiva tiene prioridad sobre una directiva potencialmente conflictiva de [ExtensionInstallBlocklist](#extensioninstallblocklist). Cuando se quita una extensión de la lista forzar instalación, Microsoft Edge la desinstala automáticamente.

La instalación forzada está limitada a las aplicaciones y extensiones que aparecen en el sitio web de complementos de Microsoft Edge para aquellas instancias que no se cuentan entre ninguna de las siguientes: instancias de Windows que se unen a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise inscritas para la administración de dispositivos o instancias de macOS que se administran mediante MDM o que están unidas a un dominio a través de MCX.

Tenga en cuenta que los usuarios pueden modificar el código fuente de cualquier extensión mediante el uso de herramientas de desarrollo, lo que podría hacer que la extensión fuera disfuncional. Si esto le preocupa, establezca la directiva [DeveloperToolsAvailability](#developertoolsavailability).

Utilice el siguiente formato para agregar una extensión a la lista:

[extensionID];[updateURL]

- extensionID: es la cadena de 32 letras que se encuentra en edge://extensiones cuando está en modo de programador.

- updateURL (opcional) es la dirección del documento XML del manifiesto de actualización para la aplicación o extensión, como se describe en [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043). Si desea instalar una extensión desde el almacén Web de Chrome, proporcione la dirección URL de la actualización de almacenes Web de Chrome, https://clients2.google.com/service/update2/crx. Tenga en cuenta que la dirección URL de actualización establecida en esta directiva sólo se utiliza para la instalación inicial; las actualizaciones posteriores de la extensión utilizan la dirección URL de actualización indicada en el manifiesto de la extensión. Si no define el updateURL, se presupone que la extensión está hospedada en Microsoft Store y se usa la siguiente URL de actualización (https://edge.microsoft.com/extensionwebstorebase/v1/crx).

Por ejemplo, gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx instala la aplicación Microsoft Online desde la dirección URL de "actualización" de Microsoft Store. Para obtener más información sobre las extensiones de hospedaje vea: [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044).

Si no configura esta directiva, no se instalarán extensiones automáticamente y los usuarios podrán desinstalar cualquier extensión en Microsoft Edge.

Tenga en cuenta que esta directiva no se aplica al modo InPrivate.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ExtensionInstallForcelist
  - Nombre de GP: Controlar qué extensiones se instalan de forma silenciosa
  - Ruta de acceso de GP: (obligatoria): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\ExtensionInstallForcelist
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ExtensionInstallForcelist
  - Valor de ejemplo:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ExtensionInstallSources

  #### Configurar la extensión y los orígenes de instalación de los scripts de usuario

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Defina las direcciones URL que pueden instalar extensiones y temas.

De forma predeterminada, los usuarios tienen que descargar un archivo *.crx para cada extensión o script que quieran instalar, y luego arrastrarlo hasta la página de configuración de Microsoft Edge. Esta directiva permite que las direcciones URL específicas que se utilizan instalen la extensión o el script para el usuario.

Cada elemento de esta lista es un patrón de coincidencia de estilo de extensión (vea [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Los usuarios pueden instalar fácilmente elementos desde cualquier dirección URL que coincida con un elemento de esta lista. Tanto la ubicación del archivo *.crx como la página desde la que se inicia la descarga (en otras palabras, la de referencia) deben estar permitidas por estos patrones.

La directiva [ExtensionInstallBlocklist](#extensioninstallblocklist) tiene prioridad sobre esta directiva. Las extensiones que se encuentren en la lista de bloqueados no se instalarán, incluso si proviene de un sitio de esta lista.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ExtensionInstallSources
  - Nombre de GP: configurar la extensión y los orígenes de instalación de los scripts del usuario
  - Ruta de acceso de GP: (obligatoria): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\ExtensionInstallSources
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ExtensionInstallSources
  - Valor de ejemplo:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ExtensionSettings

  #### Configurar la administración de la extensión

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura los parámetros de la administración de extensiones para Microsoft Edge.

Esta directiva controla múltiples parámetros, incluyendo los parámetros controlados por cualquier directiva existente relacionada con las extensiones. Esta directiva reemplaza las directivas heredadas si ambas están establecidas.

Esta directiva asigna un id. de extensión o una dirección URL de actualización a su configuración. Con un id. de extensión, la configuración se aplica solo a la extensión especificada. Establezca una configuración predeterminada para el id. especial "*" para que se aplique a todas las extensiones que no estén específicamente enumeradas en esta política. Con una dirección URL de actualización, la configuración se aplica a todas las extensiones con la dirección URL de actualización exacta indicada en el manifiesto de esta extensión, como se describe en [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ExtensionSettings
  - Nombre de GP: configurar los ajustes de administración de la extensión
  - Ruta de acceso de GP: (obligatoria): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ExtensionSettings
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {
  "*": {
    "allowed_types": [
      "hosted_app"
    ], 
    "blocked_install_message": "Custom error message.", 
    "blocked_permissions": [
      "downloads", 
      "bookmarks"
    ], 
    "install_sources": [
      "https://company-intranet/apps"
    ], 
    "installation_mode": "blocked", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ]
  }, 
  "abcdefghijklmnopabcdefghijklmnop": {
    "blocked_permissions": [
      "history"
    ], 
    "installation_mode": "allowed", 
    "minimum_version_required": "1.0.1"
  }, 
  "bcdefghijklmnopabcdefghijklmnopa": {
    "allowed_permissions": [
      "downloads"
    ], 
    "installation_mode": "force_installed", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ], 
    "update_url": "https://contoso.com/update_url"
  }, 
  "cdefghijklmnopabcdefghijklmnopab": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "fghijklmnopabcdefghijklmnopabcde": {
    "blocked_install_message": "Custom removal message.", 
    "installation_mode": "removed"
  }, 
  "update_url:https://www.contoso.com/update.xml": {
    "allowed_permissions": [
      "downloads"
    ], 
    "blocked_permissions": [
      "wallpaper"
    ], 
    "installation_mode": "allowed"
  }
}
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {"*": {"allowed_types": ["hosted_app"], "blocked_install_message": "Custom error message.", "blocked_permissions": ["downloads", "bookmarks"], "install_sources": ["https://company-intranet/apps"], "installation_mode": "blocked", "runtime_allowed_hosts": ["*://good.contoso.com"], "runtime_blocked_hosts": ["*://*.contoso.com"]}, "abcdefghijklmnopabcdefghijklmnop": {"blocked_permissions": ["history"], "installation_mode": "allowed", "minimum_version_required": "1.0.1"}, "bcdefghijklmnopabcdefghijklmnopa": {"allowed_permissions": ["downloads"], "installation_mode": "force_installed", "runtime_allowed_hosts": ["*://good.contoso.com"], "runtime_blocked_hosts": ["*://*.contoso.com"], "update_url": "https://contoso.com/update_url"}, "cdefghijklmnopabcdefghijklmnopab": {"blocked_install_message": "Custom error message.", "installation_mode": "blocked"}, "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {"blocked_install_message": "Custom error message.", "installation_mode": "blocked"}, "fghijklmnopabcdefghijklmnopabcde": {"blocked_install_message": "Custom removal message.", "installation_mode": "removed"}, "update_url:https://www.contoso.com/update.xml": {"allowed_permissions": ["downloads"], "blocked_permissions": ["wallpaper"], "installation_mode": "allowed"}}
  ```
  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ExtensionSettings
  - Valor de ejemplo:
``` xml
<key>ExtensionSettings</key>
<dict>
  <key>*</key>
  <dict>
    <key>allowed_types</key>
    <array>
      <string>hosted_app</string>
    </array>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>blocked_permissions</key>
    <array>
      <string>downloads</string>
      <string>bookmarks</string>
    </array>
    <key>install_sources</key>
    <array>
      <string>https://company-intranet/apps</string>
    </array>
    <key>installation_mode</key>
    <string>blocked</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
  </dict>
  <key>abcdefghijklmnopabcdefghijklmnop</key>
  <dict>
    <key>blocked_permissions</key>
    <array>
      <string>history</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
    <key>minimum_version_required</key>
    <string>1.0.1</string>
  </dict>
  <key>bcdefghijklmnopabcdefghijklmnopa</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>installation_mode</key>
    <string>force_installed</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
    <key>update_url</key>
    <string>https://contoso.com/update_url</string>
  </dict>
  <key>cdefghijklmnopabcdefghijklmnopab</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>fghijklmnopabcdefghijklmnopabcde</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom removal message.</string>
    <key>installation_mode</key>
    <string>removed</string>
  </dict>
  <key>update_url:https://www.contoso.com/update.xml</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>blocked_permissions</key>
    <array>
      <string>wallpaper</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
  </dict>
</dict>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Directivas de autenticación HTTP

  [Volver al principio](#microsoft-edge---policies)

  ### AllowCrossOriginAuthPrompt

  #### Allow cross-origin HTTP Authentication prompts

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Controls whether third-party images on a page can show an authentication prompt.

Generalmente, esto está deshabilitado como defensa contra la suplantación de identidad (phishing). If you don't configure this policy, it's disabled and third-party images can't show an authentication prompt.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AllowCrossOriginAuthPrompt
  - Nombre de GP: Permitir solicitudes de autenticación HTTP de origen cruzado
  - Ruta de acceso GP (obligatoria): Plantillas administrativas/Microsoft Edge/autenticación HTTP
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AllowCrossOriginAuthPrompt
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AllowCrossOriginAuthPrompt
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AuthNegotiateDelegateAllowlist

  #### Especifica una lista de servidores en los que Microsoft Edge puede delegar credenciales de usuario

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura la lista de servidores en los que Microsoft Edge puede delegar.

Separa los nombres de los servidores con comas. Se permiten los comodines (*).

Si no configura esta directiva, Microsoft Edge no delegará las credenciales de usuario aunque se detecte un servidor como intranet.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AuthNegotiateDelegateAllowlist
  - Nombre de GP: especificar una lista de servidores en los que Microsoft Edge puede delegar credenciales de usuario
  - Ruta de acceso GP (obligatoria): Plantillas administrativas/Microsoft Edge/autenticación HTTP
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AuthNegotiateDelegateAllowlist
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"contoso.com"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AuthNegotiateDelegateAllowlist
  - Valor de ejemplo:
``` xml
<string>contoso.com</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AuthSchemes

  #### Esquemas de autenticación compatibles

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica qué esquemas de autenticación HTTP son compatibles.

Puede configurar la directiva usando estos valores: "básico", "implícito", "NTLM" y "negociar". Separa los valores múltiples con comas.

Si no configura esta directiva se utilizarán los cuatro esquemas.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AuthSchemes
  - Nombre de GP: esquemas de autenticación admitidos
  - Ruta de acceso GP (obligatoria): Plantillas administrativas/Microsoft Edge/autenticación HTTP
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AuthSchemes
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"basic,digest,ntlm,negotiate"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AuthSchemes
  - Valor de ejemplo:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AuthServerAllowlist

  #### Configurar la lista de servidores de autenticación permitidos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica qué servidores habilitar para la autenticación integrada. La autenticación integrada solo está habilitada cuando Microsoft Edge recibe un desafío de autenticación de un proxy o de un servidor de esta lista.

Separa los nombres de los servidores con comas. Se permiten los comodines (*).

Si no configura esta directiva, Microsoft Edge intentará detectar si un servidor está en la intranet, solo entonces responderá a las solicitudes de IWA. Si el servidor se encuentra en Internet, Microsoft Edge ignorará las solicitudes de IWA.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AuthServerAllowlist
  - Nombre de GP: configurar la lista de servidores de autenticación permitidos
  - Ruta de acceso GP (obligatoria): Plantillas administrativas/Microsoft Edge/autenticación HTTP
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AuthServerAllowlist
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"*contoso.com,contoso.com"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AuthServerAllowlist
  - Valor de ejemplo:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DisableAuthNegotiateCnameLookup

  #### Deshabilitar la búsqueda CNAME al negociar la autenticación Kerberos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Determina si el SPN de Kerberos generado se basa en el nombre DNS canónico (CNAME) o en el nombre original introducido.

Si habilita esta directiva, se omitirá la búsqueda del CNAME y se utilizará el nombre del servidor (tal y como se ha introducido).

Si deshabilita esta directiva o no la configura, se utilizará el nombre canónico del servidor.  Esto se determina a través de la búsqueda del CNAME.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DisableAuthNegotiateCnameLookup
  - Nombre de GP: deshabilitar la búsqueda de CNAME al negociar la autenticación Kerberos
  - Ruta de acceso GP (obligatoria): Plantillas administrativas/Microsoft Edge/autenticación HTTP
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DisableAuthNegotiateCnameLookup
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DisableAuthNegotiateCnameLookup
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### EnableAuthNegotiatePort

  #### Incluir un puerto no estándar en Kerberos SPN

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica si el SPN de Kerberos generado debe incluir un puerto no estándar.

Si habilita esta directiva y un usuario incluye un puerto no estándar (un puerto distinto al 80 o al 443) en una dirección URL, ese puerto se incluye en el SPN de Kerberos generado.

Si no configura o desactiva esta directiva, el SPN de Kerberos generado no incluirá un puerto en ningún caso.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EnableAuthNegotiatePort
  - Nombre de GP: incluir un puerto que no sea estándar en Kerberos SPN
  - Ruta de acceso GP (obligatoria): Plantillas administrativas/Microsoft Edge/autenticación HTTP
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: EnableAuthNegotiatePort
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: EnableAuthNegotiatePort
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NtlmV2Enabled

  #### Controlar si la autenticación NTLMv2 está habilitada

  
  
  #### Versiones compatibles:

  - En MacOS desde la versión 77 o posterior

  #### Descripción

  Controla si NTLMv2 está habilitado.

Todas las versiones recientes de samba y los servidores de Windows son compatibles con NTLMv2. Sólo debe deshabilitar NTLMv2 para resolver problemas de compatibilidad con versiones anteriores, ya que reduce la seguridad de la autenticación.

Si no configura esta directiva, NTLMv2 se habilitará de forma predeterminada.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NtlmV2Enabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Directivas de configuración de pantalla completa

  [Volver al principio](#microsoft-edge---policies)

  ### KioskAddressBarEditingEnabled

  #### Configura la edición de la barra de direcciones para la experiencia de navegación pública en modo de pantalla completa.

  
  
  #### Versiones compatibles:

  - On Windows and macOS since 87 or later

  #### Descripción

  Esta directiva solo se aplica en el modo de pantalla completa de Microsoft Edge al usar la experiencia de examen público.

Si habilita esta Directiva, impedirá que los usuarios puedan cambiar la dirección URL en la barra de direcciones.

Si deshabilita esta Directiva o no la configura, los usuarios podrán cambiar la dirección URL en la barra de direcciones.

Para obtener información detallada sobre cómo configurar la pantalla completa, consulta [https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: KioskAddressBarEditingEnabled
  - Nombre de GP: Configura la edición de la barra de direcciones para la experiencia de navegación pública en modo de pantalla completa.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Configuración de pantalla completa
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: KioskAddressBarEditingEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```

  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: KioskAddressBarEditingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### KioskDeleteDownloadsOnExit

  #### Eliminar archivos descargados como parte de la sesión de pantalla completa cuando se cierra Microsoft Edge

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 87 o posterior

  #### Descripción
                                                                                              

  Esta directiva solo se aplica a la modalidad de exposición de Microsoft Edge.

Si habilitas esta directiva, los archivos descargados como parte de la sesión de pantalla completa se eliminan cada vez que se cierra Microsoft Edge.

Si deshabilitas esta directiva o no la configuras, los archivos descargados como parte de la sesión de pantalla completa no se eliminan cuando se cierra Microsoft Edge.

Para obtener información detallada sobre cómo configurar la pantalla completa, consulta [https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: KioskDeleteDownloadsOnExit
  - Nombre de GP: Eliminar archivos descargados como parte de la sesión de pantalla completa cuando se cierra Microsoft Edge
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Configuración de pantalla completa
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: KioskDeleteDownloadsOnExit
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ## Directivas de mensajería nativa

  [Volver al principio](#microsoft-edge---policies)

  ### NativeMessagingAllowlist

  #### Controlar cuáles hosts de mensajería nativo pueden utilizar los usuarios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Enumera los hosts de mensajería nativos específicos que los usuarios pueden utilizar en Microsoft Edge.

De forma predeterminada, se permiten todos los hosts de mensajería nativa. Si establece la directiva [NativeMessagingBlocklist](#nativemessagingblocklist) en *, todos los hosts de mensajería nativa se bloquearán y solo se cargarán los hosts de mensajería nativa que figuran en esta lista.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NativeMessagingAllowlist
  - Nombre de GP: controlar cuáles son los servidores de mensajería nativos que pueden usar los usuarios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Mensajería nativa
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\NativeMessagingAllowlist
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NativeMessagingAllowlist
  - Valor de ejemplo:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NativeMessagingBlocklist

  #### Configurar la lista de bloqueados de la mensajería nativa

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica los hosts de mensajería nativa que no se deben usar.

Use "*" para bloquear todos los hosts de mensajería nativa, excepto si aparecen explícitamente en la lista de permitidos.

Si no configura esta directiva Microsoft Edge cargará todos los hosts de mensajería nativa instalados.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NativeMessagingBlocklist
  - Nombre de GP: configurar la lista de elementos bloqueados de la mensajería nativa
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Mensajería nativa
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\NativeMessagingBlocklist
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NativeMessagingBlocklist
  - Valor de ejemplo:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NativeMessagingUserLevelHosts

  #### Permitir los hosts de mensajería nativo en el nivel de usuario (instalado sin permisos de administrador) 

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite la instalación a nivel de usuario de hosts de mensajería nativa.

Si deshabilita esta directiva, Microsoft Edge solo usará hosts de mensajería nativa instalados en el nivel de sistema.

De forma predeterminada, si no configura esta directiva, Microsoft Edge permitirá el uso de hosts de mensajería nativa a nivel de usuario.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NativeMessagingUserLevelHosts
  - Nombre de GP: permitir el servidor de mensajería nativo en el nivel de usuario (instalado sin permisos de administrador) 
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Mensajería nativa
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: NativeMessagingUserLevelHosts
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NativeMessagingUserLevelHosts
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Administrador de contraseñas y directivas de protección

  [Volver al principio](#microsoft-edge---policies)

  ### PasswordManagerEnabled

  #### Habilitar el guardado de contraseñas en el administrador de contraseñas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilitar Microsoft Edge para guardar las contraseñas de los usuarios.

Si habilita esta directiva, los usuarios podrán guardar sus contraseñas en Microsoft Edge. La próxima vez que visiten el sitio Microsoft Edge introducirá la contraseña automáticamente.

Si deshabilita esta directiva, los usuarios no podrán guardar nuevas contraseñas, pero podrán seguir utilizando las contraseñas guardadas previamente.

Si habilita o deshabilita esta directiva, los usuarios no podrán cambiarla o reemplazarla en Microsoft Edge. Si no la configura, los usuarios podrán guardar las contraseñas, así como desactivar esta característica.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PasswordManagerEnabled
  - Nombre de GP: habilitar la posibilidad de guardar contraseñas en el administrador de contraseñas
  - Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge/Administrador de contraseñas y protección 
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Administrador de contraseñas y protección 
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: PasswordManagerEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PasswordManagerEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PasswordMonitorAllowed

  #### Permitir que los usuarios puedan recibir alertas si se detecta que las contraseñas no son seguras

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 85 o posterior

  #### Descripción

  Permitir que Microsoft Edge supervise las contraseñas de usuario.

Si habilita esta directiva y un usuario conviene que habilite la Directiva, se le notificará al usuario si alguna de las contraseñas almacenadas en Microsoft Edge no es segura. Microsoft Edge mostrará una alerta y esta información también estará disponible en Configuración > Contraseñas > Monitor de contraseña.

Si deshabilita esta Directiva, no se pedirá permiso a los usuarios para habilitar esta característica. Las contraseñas no se analizarán y no recibirán ninguna alerta.

Si habilita o no configura la Directiva, los usuarios pueden activar o desactivar esta característica.

Para obtener más información sobre cómo encuentra Microsoft Edge las contraseñas no seguras, vea [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

Instrucciones adicionales:

Esta Directiva puede configurarse como Recomendada así como Obligatoria, pero con un llamado importante.

Obligatoria habilitada: dado que el consentimiento por parte del usuario individual es una condición previa para habilitar esta característica para un usuario determinado, esta Directiva no tiene una configuración habilitada obligatoria. Si la Directiva está establecida en Obligatoria, la interfaz de usuario de configuración no cambiará y se mostrará el mensaje de error siguiente en edge://policy

Ejemplo de mensaje de estado de error: "Este valor de Directiva no se tiene en cuenta porque el Monitor de contraseña requiere el consentimiento del usuario individual para ser activado. Puede pedir a los usuarios de su organización que tengan acceso a la configuración > Perfil > contraseña y a activar la característica ".

Directiva en modo Recomendada: Si la Directiva está establecida en Recomendada, la interfaz de usuario de configuración permanecerá en estado "desactivado", pero se le mostrará un icono de maletín junto a esta descripción al pasar el puntero por encima: "Su organización recomienda un valor específico para esta configuración y usted ha elegido un valor distinto"

Obligatorio y Recomendado desactivados: Estos estados funcionarán de la forma habitual y se mostrarán los títulos usuales a los usuarios.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PasswordMonitorAllowed
  - Nombre de directiva de usuario: permitir que los usuarios se avisen si se detecta que las contraseñas no son seguras
  - Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge/Administrador de contraseñas y protección 
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Administrador de contraseñas y protección 
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: PasswordMonitorAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### PasswordProtectionChangePasswordURL

  #### Configurar el cambio de contraseña URL

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura la dirección URL de cambio de contraseña (solo esquemas HTTP y HTTPS).

El servicio de protección de contraseñas enviará a los usuarios a esta dirección URL para que cambien su contraseña después de ver una advertencia en el explorador.

Si habilita esta directiva, el servicio de protección de contraseñas enviará a los usuarios a esta dirección URL para que cambien su contraseña.

Si deshabilita esta directiva o no la configura, el servicio de protección de contraseñas no redirigirá a los usuarios a una dirección URL de cambio de contraseña.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PasswordProtectionChangePasswordURL
  - Nombre de GP: configurar el cambio de dirección URL de la contraseña
  - Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge/Administrador de contraseñas y protección 
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: PasswordProtectionChangePasswordURL
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://contoso.com/change_password.html"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PasswordProtectionChangePasswordURL
  - Valor de ejemplo:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PasswordProtectionLoginURLs

  #### Configurar la lista de URLs de acceso a la empresa donde el servicio de protección de contraseñas debe capturar los salted hashes de una contraseña

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configurar la lista de URL de inicio de sesión de la empresa (sólo esquemas HTTP y HTTPS) en la que Microsoft Edge debe capturar los salted hashes de las contraseñas y utilizarlos para la detección para volver a utilizar las mismas.

Si habilita esta directiva, el servicio de protección con contraseña capturará las huellas digitales de las contraseñas en las direcciones URL definidas.

Si deshabilita esta directiva o no la configura, no se capturarán las huellas digitales de la contraseña.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PasswordProtectionLoginURLs
  - GP name: configurar la lista de URLs de acceso a la empresa donde el servicio de protección de contraseñas debe capturar los salted hashes de una contraseña
  - Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge/Administrador de contraseñas y protección 
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\PasswordProtectionLoginURLs
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PasswordProtectionLoginURLs
  - Valor de ejemplo:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PasswordProtectionWarningTrigger

  #### Configurar el desencadenador de advertencia de protección con contraseña

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Le permite controlar cuándo activar la advertencia de protección de contraseña. La protección de la contraseña alerta a los usuarios cuando reutilizan su contraseña protegida en sitios potencialmente sospechosos.

Puede utilizar las directivas [PasswordProtectionLoginURLs](#passwordprotectionloginurls) y [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) para configurar qué contraseñas desea proteger.

Exenciones: las contraseñas de los sitios enumerados en [PasswordProtectionLoginURLs](#passwordprotectionloginurls) y [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl), así como de los sitios enumerados en [SmartScreenAllowListDomains](#smartscreenallowlistdomains), no activarán una advertencia de protección de contraseña.

Establezca en "PasswordProtectionWarningOff" para no mostrar las advertencias de protección de contraseña.

Establezca en "PasswordProtectionWarningOnPasswordReuse" para mostrar advertencias de protección de contraseña cuando el usuario reutiliza su contraseña protegida en un sitio no permitido.

Si desactiva o no configura esta directiva, entonces el desencadenador de advertencia no se muestra.

Asignación de opciones de directiva:

* PasswordProtectionWarningOff (0) = la advertencia de protección de contraseña está desactivada

* PasswordProtectionWarningOnPasswordReuse (1) = la advertencia de protección de contraseña se activa por la reutilización de contraseñas

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PasswordProtectionWarningTrigger
  - Nombre de GP: configurar el indicador de advertencia para la protección de contraseñas
  - Ruta de acceso de GP (obligatorio): Plantillas administrativas/Microsoft Edge/Administrador de contraseñas y protección 
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: PasswordProtectionWarningTrigger
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PasswordProtectionWarningTrigger
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PasswordRevealEnabled

  #### Habilitar el botón revelar contraseña

  
  
  #### Versiones compatibles:

  - On Windows and macOS since 87 or later

  #### Descripción

  Le permite configurar la visualización predeterminada del botón revelar contraseña del explorador para los campos de entrada de contraseña en los sitios Web.

Si habilita o no configura esta Directiva, la configuración de usuario del explorador usa de forma predeterminada el botón Mostrar contraseña.

Si deshabilita esta Directiva, la configuración de usuario del explorador no mostrará el botón Mostrar contraseña.

Por accesibilidad, los usuarios pueden cambiar la configuración del explorador de la directiva predeterminada.

Esta directiva solo afecta al botón revelar contraseña del explorador, no afecta a los botones de revelar personalizados de los sitios Web.

  #### Características admitidas:

  - Puede ser obligatorio: no
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PasswordRevealEnabled
  - Nombre GP: habilitar el botón revelar contraseña
  - Ruta de acceso de GP (obligatorio): N/D
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Administrador de contraseñas y protección 
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatorio): N/D
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: PasswordRevealEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```

  #### Información y configuración de Mac
  
  - Nombre clave de preferencias: PasswordRevealEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Directivas de impresión

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultPrinterSelection

  #### Reglas predeterminadas para seleccionar impresoras

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Reemplaza las reglas de selección de impresoras predeterminadas de Microsoft Edge. Esta directiva determina las reglas para seleccionar la impresora predeterminada en Microsoft Edge, que ocurre la primera vez que un usuario intenta imprimir una página.

Cuando se establece esta directiva, Microsoft Edge intenta encontrar una impresora que coincida con todos los atributos especificados y la utiliza como impresora predeterminada. Si hay varias impresoras que cumplen los criterios, se utiliza la primera que coincida.

Si no configura esta directiva o no se encuentran impresoras que coincidan con la misma dentro del tiempo de espera, la impresora se configurará de forma predeterminada con la impresora PDF incorporada o sin impresora, si la impresora PDF no está disponible.

El valor se analiza como un objeto JSON, de acuerdo con el siguiente esquema: { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

Omitir un campo significará que todos los valores coinciden; por ejemplo, si no se especifica la conectividad, la vista previa de impresión empezará a descubrir todo tipo de impresoras locales. Los patrones de expresión regulares deben seguir la sintaxis de JavaScript RegExp y las coincidencias se distinguen mayúsculas de minúsculas

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultPrinterSelection
  - Nombre de GP: reglas predeterminadas para seleccionar impresoras
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Impresión
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultPrinterSelection
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultPrinterSelection
  - Valor de ejemplo:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PrintHeaderFooter

  #### Imprimir encabezados y pies de página

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Forzar a los "encabezados y pies de página" a que estén activados o desactivados en el diálogo de impresión.

Si no configura esta directiva, los usuarios podrán decidir si imprimir los encabezados y los pies de página.

Si deshabilita esta directiva, los usuarios no podrán imprimir los encabezados y los pies de página.

Si habilita esta directiva, los usuarios siempre imprimirán los encabezados y los pies de página.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PrintHeaderFooter
  - Nombre de GP: imprimir encabezados y pies de página
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Impresión
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Impresión
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: PrintHeaderFooter
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PrintHeaderFooter
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PrintPreviewUseSystemDefaultPrinter

  #### Establecer la impresora predeterminada del sistema como la impresora predeterminada

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Indica a Microsoft Edge que utilice la impresora predeterminada del sistema como opción predeterminada en la vista previa de impresión en lugar de la impresora utilizada recientemente.

Si deshabilita esta directiva o no la configura, la vista previa de impresión utilizará la impresora más reciente como opción de destino predeterminada.

Si habilita esta directiva, la vista previa de impresión utilizará la impresora predeterminada del sistema operativo como opción de destino predeterminada.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PrintPreviewUseSystemDefaultPrinter
  - Nombre de GP: establecer la impresora del sistema como la impresora predeterminada
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Impresión
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Impresión
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: PrintPreviewUseSystemDefaultPrinter
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PrintPreviewUseSystemDefaultPrinter
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PrintingEnabled

  #### Habilitar la impresión

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilita la impresión en Microsoft Edge y evita que los usuarios cambien esta configuración.

Si habilita esta directiva o no la configura los usuarios podrán imprimir.

Si deshabilita esta política, los usuarios no podrán imprimir desde Microsoft Edge. Si deshabilita esta directiva, los usuarios no podrán imprimir desde Microsoft Edge. Los usuarios pueden seguir imprimiendo desde los complementos que omiten Microsoft Edge mientras imprimen. Por ejemplo, ciertas aplicaciones de Adobe Flash tienen la opción de imprimir en su menú contextual, lo cual no está cubierto en esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PrintingEnabled
  - Nombre de GP: habilitar la impresión
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Impresión
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: PrintingEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PrintingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PrintingPaperSizeDefault

  #### Tamaño de página de impresión predeterminado

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Reemplaza el tamaño de página de impresión predeterminado.

El nombre debe contener uno de los formatos listados o "personalizado" si el tamaño de papel requerido no se encuentra en la lista. Si se proporciona un valor "personalizado", la propiedad custom_size debe especificarse. Describe el alto y el ancho que se quiere en micras. En caso contrario, no se debe especificar la propiedad custom_size. Se ignora la directiva que infringe estas reglas.

Si el tamaño de la página no está disponible en la impresora elegida por el usuario, se ignora esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PrintingPaperSizeDefault
  - Nombre de GP: tamaño de página de impresión predeterminado
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Impresión
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: PrintingPaperSizeDefault
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {"custom_size": {"height": 297000, "width": 210000}, "name": "custom"}
  ```
  

  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: PrintingPaperSizeDefault
  - Valor de ejemplo:
``` xml
<key>PrintingPaperSizeDefault</key>
<dict>
  <key>custom_size</key>
  <dict>
    <key>height</key>
    <integer>297000</integer>
    <key>width</key>
    <integer>210000</integer>
  </dict>
  <key>name</key>
  <string>custom</string>
</dict>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### UseSystemPrintDialog

  #### Imprimir usando el diálogo de impresión del sistema

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Muestra el diálogo de impresión del sistema en lugar de la vista previa de impresión.

Si habilita esta directiva, Microsoft Edge abrirá el diálogo de impresión del sistema en lugar de la vista previa de impresión integrada cuando un usuario imprima una página.

Si no configura o deshabilita esta directiva, los comandos de impresión activarán la pantalla de vista previa de impresión de Microsoft Edge.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: UseSystemPrintDialog
  - Nombre de GP: imprimir usando el diálogo de impresión del sistema
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/Microsoft Edge/Impresión
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: UseSystemPrintDialog
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: UseSystemPrintDialog
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Directivas de servidor proxy

  [Volver al principio](#microsoft-edge---policies)

  ### ProxyBypassList

  #### Configurar las reglas de omisión de proxy

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de hosts para los que Microsoft Edge omite cualquier proxy.

Esta directiva se aplica solo si ha seleccionado "Usar servidores proxy fijos" en la directiva de [ProxyMode](#proxymode). Si seleccionó cualquier otro modo para configurar directivas de proxy, no habilite ni configure esta directiva.

Si habilita esta directiva, podrá crear una lista de hosts para los que Microsoft Edge no utiliza un proxy.

Si no configura esta directiva, no se crea ninguna lista de hosts para los que Microsoft Edge omite un proxy. Deje esta directiva sin configurar si especificó algún otro método para configurar las directivas de proxy.

Para obtener ejemplos más detallados, vaya a [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ProxyBypassList
  - Nombre de GP: configurar las reglas de omisión de proxy
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ProxyBypassList
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ProxyBypassList
  - Valor de ejemplo:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ProxyMode

  #### Configurar los ajustes del servidor proxy

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica la configuración del servidor proxy que usa Microsoft Edge. Si habilita esta directiva, los usuarios no podrán cambiar la configuración de proxy.

Si elige no usar nunca un servidor proxy y conectarse siempre directamente, se ignorarán todas las demás opciones.

Si elige utilizar la configuración de proxy del sistema, se ignorarán todas las demás opciones.

Si elige la detección automática del servidor proxy, se ignorarán todas las demás opciones.

Si elige el modo de servidor proxy fijo, puede especificar más opciones en [ProxyServer](#proxyserver) y en 'Lista de reglas de omisión de proxy separadas por comas'.

Si escoge utilizar un script de proxy .pac, deberá especificar la dirección URL del script en "dirección URL de un archivo proxy .pac".

Para obtener ejemplos más detallados, vaya a [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Si habilita esta directiva, Microsoft Edge ignorará todas las opciones relacionadas con el proxy especificadas desde la línea de comandos.

Si no configura esta directiva, los usuarios podrán elegir su propia configuración de proxy.

Asignación de opciones de directiva:

* ProxyDisabled (direct) = nunca usar un servidor proxy

* ProxyAutoDetect (auto_detect) = detectar automáticamente la configuración del proxy

* ProxyPacScript (pac_script) = usar un script de proxy .pac

* ProxyFixedServers (fixed_servers) = usar servidores proxy fijos

* ProxyUseSystem (system) = usar la configuración de proxy del sistema

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ProxyMode
  - Nombre de GP: configurar los ajustes del servidor proxy
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ProxyMode
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"direct"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ProxyMode
  - Valor de ejemplo:
``` xml
<string>direct</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ProxyPacUrl

  #### Establecer la URL del archivo proxy .pac

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica la dirección URL de un archivo de autoconfiguración de proxy (PAC).

Esta directiva se aplica sólo si seleccionaste "Usar un script de proxy .pac" en la directiva de [ProxyMode](#proxymode). Si seleccionó cualquier otro modo para configurar directivas de proxy, no habilite ni configure esta directiva.

Si habilita esta directiva, puede especificar la dirección URL de un archivo PAC, que define cómo el navegador elige automáticamente el servidor proxy apropiado para buscar un sitio web en particular.

Si deshabilita o no configura esta directiva, no se especificará ningún archivo PAC. Deje esta directiva sin configurar si especificó algún otro método para configurar las directivas de proxy.

Para obtener ejemplos más detallados, vea [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ProxyPacUrl
  - Nombre de GP: establecer la dirección URL del proxy del archivo .pac
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ProxyPacUrl
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://internal.contoso.com/example.pac"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ProxyPacUrl
  - Valor de ejemplo:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ProxyServer

  #### Configurar la dirección o la dirección URL del servidor proxy

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica la dirección URL del servidor proxy.

Esta directiva se aplica solo si ha seleccionado "Usar servidores proxy fijos" en la directiva de [ProxyMode](#proxymode). Si seleccionó cualquier otro modo para configurar directivas de proxy, no habilite ni configure esta directiva.

Si habilita esta directiva, el servidor proxy configurado por la misma se utilizará para todas las direcciones URL.

Si deshabilita o no configura esta directiva, los usuarios pueden elegir su propia configuración de proxy mientras se encuentran en este modo de proxy. Deje esta directiva sin configurar si especificó algún otro método para configurar las directivas de proxy.

Para obtener más opciones y ejemplos detallados, vea [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ProxyServer
  - Nombre de GP: dirección o la URL del servidor proxy
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ProxyServer
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"123.123.123.123:8080"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ProxyServer
  - Valor de ejemplo:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ProxySettings

  #### Configuración de proxy

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura la configuración del proxy para Microsoft Edge.

Si habilita esta directiva, Microsoft Edge ignorará todas las opciones relacionadas con el proxy especificadas desde la línea de comandos.

Si no configura esta directiva, los usuarios podrán elegir su propia configuración de proxy.

Esta directiva reemplaza las siguientes directivas individuales:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

El campo ProxyMode permite especificar el servidor proxy utilizado por Microsoft Edge y evita que los usuarios cambien la configuración del proxy.

El campo ProxyPacUrl es una dirección URL a un archivo proxy. PAC.

El campo ProxyServer es una URL para el servidor proxy.

El campo ProxyBypassList es una lista de hosts proxy que Microsoft Edge omite.

Si elige el valor "Direct" como "ProxyMode", nunca se utilizará un proxy y se ignorarán todos los demás campos.

Si elige el valor "Direct" como "ProxyMode", nunca se utilizará un proxy y se ignorarán todos los demás campos.

Si elige el valor "auto_detect" como "ProxyMode", se ignorará todos los demás campos.

Si elige el valor "fixed_server" como "ProxyMode", se usarán los campos "ProxyServer" y "ProxyBypassList".

Si elige el valor "pac_script" como "ProxyMode", se usarán los campos "ProxyPacUrl" y "ProxyBypassList".

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ProxySettings
  - Nombre de GP: configurar parámetros proxy
  - Ruta de acceso GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ProxySettings
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {"ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", "ProxyMode": "direct", "ProxyPacUrl": "https://internal.site/example.pac", "ProxyServer": "123.123.123.123:8080"}
  ```
  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ProxySettings
  - Valor de ejemplo:
``` xml
<key>ProxySettings</key>
<dict>
  <key>ProxyBypassList</key>
  <string>https://www.example1.com,https://www.example2.com,https://internalsite/</string>
  <key>ProxyMode</key>
  <string>direct</string>
  <key>ProxyPacUrl</key>
  <string>https://internal.site/example.pac</string>
  <key>ProxyServer</key>
  <string>123.123.123.123:8080</string>
</dict>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Configuración de directivas de SmartScreen

  [Volver al principio](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverride

  #### Impedir la omisión de los mensajes de SmartScreen de Microsoft Defender para los sitios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Esta configuración de directiva le permite decidir si los usuarios pueden reemplazar las advertencias de SmartScreen de Microsoft Defender sobre sitios web potencialmente malintencionados.

Si habilita esta configuración, los usuarios no podrán ignorar las advertencias de SmartScreen de Microsoft Defender y se les bloqueará el acceso al sitio.

Si deshabilita o no establece esta configuración, los usuarios podrán ignorar las advertencias de SmartScreen de Microsoft Defender y continuar en el sitio.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PreventSmartScreenPromptOverride
  - Nombre de GP: Impedir la omisión de los avisos de SmartScreen de Microsoft Defender para los sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Value Name: PreventSmartScreenPromptOverride
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia:PreventSmartScreenPromptOverride
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverrideForFiles

  #### Impedir que se ignoren las advertencias de SmartScreen de Microsoft Defender sobre las descargas

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 77 o posterior
  - En MacOS desde la versión 79 o posterior

  #### Descripción

  Esta directiva le permite determinar si los usuarios pueden anular las advertencias de SmartScreen de Microsoft Defender sobre las descargas sin comprobar.

Si habilita esta directiva, los usuarios de su organización no podrán ignorar las advertencias de SmartScreen de Microsoft Defender y se les impedirá completar las descargas sin comprobar.

Si deshabilita o no configura esta directiva, los usuarios podrán ignorar las advertencias de SmartScreen de Microsoft Defender y completar las descargas sin comprobar.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PreventSmartScreenPromptOverrideForFiles
  - Nombre de GP: impedir la omisión de las advertencias sobre las descargas de SmartScreen de Microsoft Defender 
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Value Name: PreventSmartScreenPromptOverrideForFiles
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PreventSmartScreenPromptOverrideForFiles
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SmartScreenAllowListDomains

  #### Configurar la lista de dominios en los que SmartScreen de Microsoft Defender no desencadenará advertencias

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura la lista de dominios de confianza de SmartScreen de Microsoft Defender. Esto significa que: SmartScreen de Microsoft Defender no comprobará la existencia de recursos potencialmente malintencionados como software de suplantación de identidad (phishing) y otro malware si las direcciones URL de origen coinciden con estos dominios.
El servicio de protección de descargas de SmartScreen de Microsoft Defender no comprueba las descargas hospedadas en estos dominios.

Si habilita esta directiva, SmartScreen de Microsoft Defender confiará en estos dominios.
Si deshabilita o no establece esta directiva, la protección predeterminada de SmartScreen de Microsoft Defender se aplicará a todos los recursos.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.
Tenga en cuenta también que esta directiva no se aplicará si su organización habilitó la Protección contra amenazas avanzada de Microsoft Defender. En su lugar, debe configurar las listas de permitidos y bloqueados en el Centro de seguridad de Microsoft Defender.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SmartScreenAllowListDomains
  - Nombre de GP: configurar la lista de dominios en los que SmartScreen de Microsoft Defender no desencadenará advertencias
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\SmartScreenAllowListDomains
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SmartScreenAllowListDomains
  - Valor de ejemplo:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SmartScreenEnabled

  #### Configurar SmartScreen de Microsoft Defender

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Esta configuración de directiva permite configurar si se activa SmartScreen de Microsoft Defender. SmartScreen de Microsoft Defender muestra mensajes de advertencia para ayudar a proteger a los usuarios de posibles estafas de suplantación de identidad (phishing) y software malintencionado. De manera predeterminada, SmartScreen de Microsoft Defender está activado.

Si habilita esta configuración, SmartScreen de Microsoft Defender estará activado.

Si deshabilita esta configuración, SmartScreen de Microsoft Defender estará deshabilitado.

Si no establece esta configuración, los usuarios podrán elegir si quieren usar SmartScreen de Microsoft Defender.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SmartScreenEnabled
  - Nombre de GP: configurar SmartScreen de Microsoft Defender
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Configuración de SmartScreen
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: SmartScreenEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SmartScreenEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SmartScreenForTrustedDownloadsEnabled

  #### Forzar a SmartScreen de Microsoft Defender a comprobar las descargas de origen confiable

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 78 o posterior

  #### Descripción

  Esta configuración de directiva le permite configurar si SmartScreen de Microsoft Defender comprueba la reputación de las descargas de una fuente de confianza.

Si habilita o no configura esta opción, SmartScreen de Microsoft Defender comprobará la reputación de la descarga independientemente de la fuente.

Si deshabilita esta configuración, SmartScreen de Microsoft Defender no comprobará la reputación de la descarga cuando ésta se realice desde una fuente de confianza.

Esta directiva solo está disponible en las instancias de Windows que están unidas a un dominio de Microsoft Active Directory o en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SmartScreenForTrustedDownloadsEnabled
  - Nombre de GP: forzar a SmartScreen de Microsoft Defender a que compruebe las descargas de orígenes de confianza
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Configuración de SmartScreen
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: SmartScreenForTrustedDownloadsEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### SmartScreenPuaEnabled

  #### Configurar SmartScreen de Microsoft Defender para bloquear aplicaciones potencialmente no deseadas.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Esta configuración de directiva le permite configurar si activar o no el bloqueo de aplicaciones potencialmente no deseadas de SmartScreen de Microsoft Defender. El bloqueo de aplicaciones potencialmente no deseadas de SmartScreen de Microsoft Defender proporciona mensajes de advertencia para ayudar a proteger a los usuarios del adware, los mineros de monedas, el bundleware y otras aplicaciones de baja reputación que están hospedadas en sitios web. El bloqueo de aplicaciones potencialmente no deseadas de SmartScreen de Microsoft Defender está desactivado por defecto.

Si habilita esta configuración, se activará el bloqueo de aplicaciones potencialmente no deseadas de SmartScreen de Microsoft Defender.

Si deshabilitas esta configuración, se desactivará el bloqueo de aplicaciones potencialmente no deseadas de SmartScreen de Microsoft Defender.

Si no configura esta opción, los usuarios podrán elegir si desean utilizar el bloqueo de aplicaciones potencialmente no deseadas de SmartScreen de Microsoft Defender.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SmartScreenPuaEnabled
  - Nombre de GP: configurar SmartScreen de Microsoft Defender para bloquear aplicaciones potencialmente no deseadas.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge / Configuración de contenido
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)/Configuración de SmartScreen
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: SmartScreenPuaEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SmartScreenPuaEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Directivas de Inicio&comma; página principal y página de pestaña nueva

  [Volver al principio](#microsoft-edge---policies)

  ### HomepageIsNewTabPage

  #### Establecer la nueva ficha como página principal

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura la página principal predeterminada en Microsoft Edge. Puede establecer la página principal en una dirección URL que especifique o en la página de la nueva pestaña.

Si habilita esta directiva, la nueva pestaña se utilizará siempre como página de inicio y se ignorará la ubicación de la dirección URL de la página de inicio.

Si deshabilita esta directiva, la página de inicio del usuario no podrá ser la nueva página de pestañas, a menos que la URL esté configurada como "edge://newtab".

Si no está configurado, los usuarios pueden elegir si la nueva pestaña es su página de inicio.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: HomepageIsNewTabPage
  - Nombre de GP: establecer la página de la nueva pestaña como página principal
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazar)/Startup, página principal y página de la pestaña nueva
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: HomepageIsNewTabPage
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: HomepageIsNewTabPage
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### HomepageLocation

  #### Configurar la dirección URL de la página principal

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura la dirección URL de la página principal predeterminada en Microsoft Edge.

La página de inicio es la página que se abre con el botón Inicio. Las páginas que se abren en el inicio están controladas por las directivas [RestoreOnStartup](#restoreonstartup).

Puede establecer una dirección URL aquí o establecer la página de inicio para abrir la página de la nueva pestaña. Si selecciona abrir la página de la nueva pestaña, entonces esta directiva no tendrá efecto.

Si habilita esta directiva, los usuarios no podrán cambiar la URL de su página de inicio, pero podrán elegir utilizar la página de la nueva pestaña como su página de inicio.

Si deshabilita o no configura esta directiva, los usuarios podrán elegir su propia página de inicio, siempre y cuando la directiva [HomepageIsNewTabPage](#homepageisnewtabpage) no esté habilitada.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: HomepageLocation
  - Nombre de GP: configurar la dirección URL de la página principal
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazar)/Startup, página principal y página de la pestaña nueva
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: HomepageLocation
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://www.contoso.com"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: HomepageLocation
  - Valor de ejemplo:
``` xml
<string>https://www.contoso.com</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NewTabPageAllowedBackgroundTypes

  #### Configurar los tipos de fondo permitidos para el diseño de página de nueva pestaña

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Puede configurar qué tipos de imagen de fondo se permiten en el diseño de página de nueva pestaña en Microsoft Edge.

Si no configura esta directiva, se habilitarán todos los tipos de imagen de fondo en la página de nueva pestaña.

Asignación de opciones de directiva:

* DisableImageOfTheDay (1) = deshabilitar el tipo de imagen de fondo diaria

* DisableCustomImage (2) = deshabilitar el tipo de imagen de fondo personalizada

* DisableAll (3) = deshabilitar todos los tipos de imagen de fondo

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NewTabPageAllowedBackgroundTypes
  - Nombre de GP: configurar los tipos de fondo permitidos para el diseño de página de nueva pestaña
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: NewTabPageAllowedBackgroundTypes
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NewTabPageAllowedBackgroundTypes
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NewTabPageCompanyLogo

  #### Establecer el logotipo de la compañía en la página de nueva pestaña (obsoleto)

  
  >OBSOLETA: Esta directiva está obsoleta y no funciona después de Microsoft Edge 85.
  #### Versiones compatibles:

  - En Windows y MacOS, desde el 79 hasta el 85

  #### Descripción

  Esta directiva no funcionaba como se esperaba debido a cambios en los requisitos operativos. Por lo que está obsoleto y no se debe usar.

Especifica el logotipo de la empresa que se utilizará en la página de la nueva pestaña de Microsoft Edge.

La directiva debe ser configurada como una cadena que exprese el o los logotipos en formato JSON. Por ejemplo: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

Esta directiva se configura especificando la dirección URL desde la que Microsoft Edge puede descargar el logotipo y su hash criptográfico (SHA-256), que se utiliza para comprobar la integridad de la descarga. El logotipo debe estar en formato PNG o SVG, y su tamaño de archivo no debe exceder los 16 MB. El logo se descarga y se almacena en caché, y se volverá a descargar cada vez que cambie la dirección URL o el hash. La dirección URL debe ser accesible sin ninguna autenticación.

"default_logo" es necesario y se usará cuando no haya imagen de fondo. Si "light_logo" es proporcionado, se usará cuando la nueva página de la pestaña del usuario tenga una imagen de fondo. Recomendamos un logotipo horizontal con un fondo transparente que esté alineado a la izquierda y centrado verticalmente. El logotipo debe tener una altura mínima de 32 píxeles y una relación de aspecto de 1:1 a 4:1. El "default_logo" debe tener un contraste adecuado contra un fondo blanco/negro, mientras que la "light_logo" debe tener un contraste adecuado contra una imagen de fondo.

Si habilita esta directiva, Microsoft Edge descargará y mostrará los logotipos especificados en la página de la nueva pestaña. Los usuarios no pueden reemplazar u ocultar el o los logotipo(s).

Si deshabilita o no configura esta directiva, Microsoft Edge no mostrará ningún logotipo de la compañía o un logotipo de Microsoft en la página de la nueva pestaña.

Para obtener ayuda para determinar el algoritmo hash SHA-256, vea https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NewTabPageCompanyLogo
  - Nombre de GP: establecer logotipo de la empresa en la página de nueva pestaña (obsoleto)
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: NewTabPageCompanyLogo
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {
  "default_logo": {
    "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29", 
    "url": "https://www.contoso.com/logo.png"
  }, 
  "light_logo": {
    "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737", 
    "url": "https://www.contoso.com/light_logo.png"
  }
}
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {"default_logo": {"hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29", "url": "https://www.contoso.com/logo.png"}, "light_logo": {"hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737", "url": "https://www.contoso.com/light_logo.png"}}
  ```
  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NewTabPageCompanyLogo
  - Valor de ejemplo:
``` xml
<key>NewTabPageCompanyLogo</key>
<dict>
  <key>default_logo</key>
  <dict>
    <key>hash</key>
    <string>cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29</string>
    <key>url</key>
    <string>https://www.contoso.com/logo.png</string>
  </dict>
  <key>light_logo</key>
  <dict>
    <key>hash</key>
    <string>517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737</string>
    <key>url</key>
    <string>https://www.contoso.com/light_logo.png</string>
  </dict>
</dict>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NewTabPageHideDefaultTopSites

  #### Ocultar los sitios principales predeterminados de la nueva ficha

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Oculta los sitios principales predeterminados de la página de la nueva pestaña de Microsoft Edge.

Si establece esta directiva en true, los iconos del sitio superior predeterminado estarán ocultos.

Si establece esta directiva como falsa o no la configura, los iconos del sitio superior predeterminados permanecerán visibles.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NewTabPageHideDefaultTopSites
  - Nombre de GP: Ocultar los principales sitios predeterminados de la nueva página de la pestaña
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: NewTabPageHideDefaultTopSites
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NewTabPageHideDefaultTopSites
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NewTabPageLocation

  #### Configurar la dirección URL de la ficha

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura la dirección URL predeterminada de la página de la nueva pestaña.

Esta directiva determina la página que se abre cuando se crean nuevas pestañas (incluso cuando se abren nuevas ventanas). También afecta a la página de inicio si está configurada para abrirse en la página de la nueva pestaña.

Esta directiva no determina qué página se abre al inicio; esto lo controla la directiva [RestoreOnStartup](#restoreonstartup). También afecta a la página de inicio si está configurada para abrirse en la página de la nueva pestaña.

Si no configura esta directiva, se utiliza la página de la nueva pestaña predeterminada.

Si configura esta directiva*y* la directiva [NewTabPageSetFeedType](#newtabpagesetfeedtype), esta directiva tendrá prioridad.

Si se proporciona una dirección URL incorrecta, se abrirán nuevas pestañas about://blank.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NewTabPageLocation
  - Nombre de GP: configurar página de la nueva pestaña de dirección URL
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazar)/Startup, página principal y página de la pestaña nueva
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: NewTabPageLocation
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://www.fabrikam.com"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NewTabPageLocation
  - Valor de ejemplo:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NewTabPageManagedQuickLinks

  #### Establecer una nueva ficha de vínculos rápidos

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 79 o posterior

  #### Descripción

  De forma predeterminada, Microsoft Edge muestra vínculos rápidos en la página de la nueva pestaña de los accesos directos agregados por el usuario y los sitios principales en función del historial de exploración. Con esta directiva, puede configurar hasta tres iconos de vínculos rápidos en la página de la nueva pestaña, expresados como objeto JSON:

[{"URL": "https://www.contoso.com", "Título": "portal de Contoso", "fijo": true/false},...]

El campo "URL" es obligatorio. las "Título" y "anclód" son opcionales. Si no se proporciona "Título", la dirección URL se usa como título predeterminado. Si no se especifica "fijo", el valor predeterminado es false.

Microsoft Edge los presenta en el orden de listado, de izquierda a derecha, con todos los mosaicos anclados mostrándose por delante de los no anclados.

Si la directiva está establecida como obligatoria, el campo " anclado " será ignorada y todos los mosaicos se anclarán. Los mosaicos no pueden ser eliminados por el usuario y siempre aparecen en la parte delantera de la lista de vínculos rápidos.

Si la Directiva está establecida como se recomienda, los mosaicos anclados permanecerán en la lista, pero el usuario podrá editarlos y eliminarlos. Los iconos de vínculos rápidos sin fijar se comportan como sitios principales predeterminados y se resaltan en la lista si se visitan otros sitios web con más frecuencia. Al aplicar vínculos no anclados a través de esta directiva a un perfil de explorador existente, es posible que los vínculos no aparezcan en absoluto, en función de cómo se encuentren en comparación con el historial de exploración del usuario.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NewTabPageManagedQuickLinks
  - Nombre de GP: establecer una nueva pestaña de vínculos rápidos
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazar)/Startup, página principal y página de la pestaña nueva
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: NewTabPageManagedQuickLinks
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [
  {
    "pinned": true, 
    "title": "Contoso Portal", 
    "url": "https://contoso.com"
  }, 
  {
    "title": "Fabrikam", 
    "url": "https://fabrikam.com"
  }
]
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [{"pinned": true, "title": "Contoso Portal", "url": "https://contoso.com"}, {"title": "Fabrikam", "url": "https://fabrikam.com"}]
  ```
  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NewTabPageManagedQuickLinks
  - Valor de ejemplo:
``` xml
<key>NewTabPageManagedQuickLinks</key>
<array>
  <dict>
    <key>pinned</key>
    <true/>
    <key>title</key>
    <string>Contoso Portal</string>
    <key>url</key>
    <string>https://contoso.com</string>
  </dict>
  <dict>
    <key>title</key>
    <string>Fabrikam</string>
    <key>url</key>
    <string>https://fabrikam.com</string>
  </dict>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NewTabPagePrerenderEnabled

  #### Habilitar precarga de la página de nueva pestaña para procesamiento más rápido

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 85 o posterior

  #### Descripción

  Si configura esta Directiva, se habilitará la carga previa de la página de la pestaña nueva y los usuarios no podrán cambiar esta configuración. Si no configura esta Directiva, se habilita la carga previa y un usuario puede cambiar esta configuración.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NewTabPagePrerenderEnabled
  - Nombre de GP: Habilitar precarga de la página de nueva pestaña para procesamiento más rápido
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazar)/Startup, página principal y página de la pestaña nueva
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: NewTabPagePrerenderEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: NewTabPagePrerenderEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NewTabPageSetFeedType

  #### Configurar la experiencia de la nueva ficha de Microsoft Edge (en desuso)

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En Windows y macOS desde 79 o posterior

  #### Descripción

  Estamos dejando de usar esta Directiva, ya que la nueva versión de la página de la nueva pestaña de Enterprise ya no requiere escoger entre los diferentes tipos de contenido. En su lugar, el contenido que se presenta al usuario se puede controlar mediante el Centro de administración de Microsoft 365. Para ir al Centro de administración de Microsoft 365, inicie sesión en https://admin.microsoft.com con su cuenta de administrador. La Directiva quedará obsoleta después de la versión 90 de Microsoft Edge.

Le permite elegir la experiencia de Microsoft News u Office 365 fuente para la página de la nueva pestaña.

Al establecer esta directiva en "News", los usuarios verán la experiencia de actividad de Microsoft News en la página de nueva pestaña.

Al establecer esta directiva en "Office", los usuarios con un inicio de sesión en el explorador de Active Directory Azure verán la experiencia de actividad de Office 365 en la página de nueva pestaña.

Si deshabilita o no configura esta directiva:

- A los usuarios que inicien sesión en el explorador Azure Active Directory se les ofrece la experiencia de actividad de la página de la nueva pestaña de Office 365, así como la experiencia de actividad estándar de la página de la nueva pestaña.

- Los usuarios que no inicien sesión en el explorador de Active Directory Azure verán la experiencia estándar de la página de la nueva pestaña.

Si configura esta directiva*y* la directiva [NewTabPageLocation](#newtabpagelocation), entonces la directiva [NewTabPageLocation](#newtabpagelocation) tendrá prioridad.

Configuración predeterminada:  deshabilitado o no configurado

Asignación de opciones de directiva:

* News (0) = experiencia de actividad de Microsoft News

* Office (1) = experiencia de actividad de Office 365

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NewTabPageSetFeedType
  - Nombre de GP: Configurar la experiencia de la página de la nueva pestaña de Microsoft Edge (en desuso)
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazar)/Startup, página principal y página de la pestaña nueva
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: NewTabPageSetFeedType
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NewTabPageSetFeedType
  - Valor de ejemplo:
``` xml
<integer>0</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### RestoreOnStartup

  #### Acción que se realizará en el inicio

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica cómo se comporta Microsoft Edge cuando se inicia.

Si desea que siempre se abra una nueva pestaña al iniciar, elija "RestoreOnStartupIsNewTabPage".

Si desea volver a abrir las direcciones URL abiertas la última vez que se cerró Microsoft Edge, elija "RestoreOnStartupIsLastSession". La sesión del explorador se restaurará tal como estaba. Tenga en cuenta que esta opción deshabilita algunas configuraciones que dependen de las sesiones o que realizan acciones al salir (como Borrar datos de exploración al salir o las cookies de sólo sesión).

Si desea abrir un conjunto específico de direcciones URL, elija "RestoreOnStartupIsURLs".

Deshabilitar esta configuración equivale a dejarla sin configurar. Los usuarios podrán cambiarla en Microsoft Edge.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

Asignación de opciones de directiva:

* RestoreOnStartupIsNewTabPage (5) = abrir una nueva pestaña

* RestoreOnStartupIsLastSession (1) = restaurar la última sesión

* RestoreOnStartupIsURLs (4) = abrir una lista de direcciones URL

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RestoreOnStartup
  - Nombre de GP: acciones necesarias para realizar el inicio
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazar)/Startup, página principal y página de la pestaña nueva
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: RestoreOnStartup
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000004
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: RestoreOnStartup
  - Valor de ejemplo:
``` xml
<integer>4</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### RestoreOnStartupURLs

  #### Sitios que se abren cuando el explorador se inicia

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especificar una lista de sitios web para que se abran automáticamente cuando se inicie el explorador. Si no configura esta directiva, no se abrirá ningún sitio al iniciar.

Esta directiva solo funciona si también establece la directiva [RestoreOnStartup](#restoreonstartup) en 'Abrir una lista de direcciones URL' (4).

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RestoreOnStartupURLs
  - Nombre de GP: sitios que se abren al iniciar el explorador
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazar)/Startup, página principal y página de la pestaña nueva
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\RestoreOnStartupURLs
  - Ruta de acceso (recomendada): SOFTWARE\Policies\Microsoft\Microsoft Edge\Recommended\RestoreOnStartupURLs
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: RestoreOnStartupURLs
  - Valor de ejemplo:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ShowHomeButton

  #### Mostrar el botón Inicio en la barra de herramientas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Muestra el botón Inicio en la barra de herramientas de Microsoft Edge.

Habilite esta directiva para mostrar siempre el botón Inicio. Deshabilítelo de forma que nunca se muestre el botón.

Si no configura la directiva, los usuarios pueden elegir si se muestra el botón Inicio.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ShowHomeButton
  - Nombre de GP: mostrar el botón de inicio en la barra de herramientas
  - Ruta de acceso de GP: Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de pestaña nueva
  - Ruta de acceso de GP (recomendado): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazar)/Startup, página principal y página de la pestaña nueva
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ShowHomeButton
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ShowHomeButton
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ## Otras directivas

  [Volver al principio](#microsoft-edge---policies)

  ### AddressBarMicrosoftSearchInBingProviderEnabled

  #### Habilitar las sugerencias de Búsqueda de Microsoft en Bing en la barra de direcciones

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 81 o posterior

  #### Descripción

  Habilita la visualización de las sugerencias relevantes de Búsqueda de Microsoft en Bing en la lista de sugerencias de la barra de direcciones cuando el usuario escribe una cadena de búsqueda en la barra de direcciones. Si habilita o no configura esta directiva, los usuarios podrán ver los resultados internos con tecnología de Búsqueda de Microsoft en Bing en la lista de sugerencias de la barra de direcciones de Microsoft Edge. Para ver los resultados de la Búsqueda de Microsoft en Bing, el usuario debe iniciar sesión en Microsoft Edge con su cuenta de Azure AD de esa organización.
Si deshabilita esta directiva, los usuarios no podrán ver los resultados internos en la lista de sugerencias de la barra de direcciones de Microsoft Edge.
Si habilitó el conjunto de directivas que fuerza a un proveedor de búsqueda predeterminado ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) and [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)), y el proveedor de búsqueda especificado no es Bing, entonces esta directiva no se aplicará y no habrá sugerencias de Búsqueda de Microsoft en Bing en la lista de sugerencias de la barra de direcciones.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AddressBarMicrosoftSearchInBingProviderEnabled
  - Nombre de GP: habilitar las sugerencias en la barra de direcciones de la Búsqueda de Microsoft en Bing
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AddressBarMicrosoftSearchInBingProviderEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AddressBarMicrosoftSearchInBingProviderEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AdsSettingForIntrusiveAdsSites

  #### Configuración de anuncios para sitios con anuncios intrusivos

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Controla si se bloquean anuncios en sitios con anuncios intrusivos.

Asignación de opciones de directiva:

* AllowAds (1) = permitir anuncios en todos los sitios.

* BlockAds (2) = bloquear anuncios en sitios con anuncios intrusivos. (Valor predeterminado)

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AdsSettingForIntrusiveAdsSites
  - Nombre de GP: configuración de anuncios para los sitios con anuncios intrusivos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AdsSettingForIntrusiveAdsSites
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AdsSettingForIntrusiveAdsSites
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AllowDeletingBrowserHistory

  #### Habilitar la eliminación del explorador y el historial de descargas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilita la eliminación del historial del navegador y del historial de descargas y evita que los usuarios cambien esta configuración.

Tenga en cuenta que incluso con esta directiva deshabilitada, no se garantiza la conservación del historial de exploración y descarga: los usuarios pueden editar o eliminar los archivos de la base de datos del historial directamente, y el propio explorador puede eliminar (en función del período de caducidad) o archivar cualquiera o todos los elementos del historial en cualquier momento.

Si habilita esta directiva o no la configura, los usuarios podrán eliminar el historial de exploración y descarga.

Si deshabilita esta directiva, los usuarios no podrán eliminar el historial de exploración y descarga.

Si deshabilita esta directiva, no habilite la directiva de [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), porque ambas se ocupan de la eliminación de datos. Si habilita ambas directivas, la directiva [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) tendrá prioridad y eliminará todos los datos cuando se cierre Microsoft Edge, independientemente de cómo haya configurado esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AllowDeletingBrowserHistory
  - Nombre de GP: habilitar la eliminación del buscador y el historial de descargas
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AllowDeletingBrowserHistory
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AllowDeletingBrowserHistory
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AllowFileSelectionDialogs

  #### Permitir cuadros de diálogo de selección de archivos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite el acceso a los archivos locales permitiendo que Microsoft Edge muestre los cuadro de diálogo de selección de archivos.

Si habilita o no configura esta directiva, los usuarios podrán abrir los cuadro de diálogo de selección de archivos como siempre.

Si se deshabilita esta directiva, siempre que el usuario realice una acción que active un cuadro de diálogo de selección de archivos (como importar favoritos, cargar archivos o guardar enlaces), se mostrará un mensaje en su lugar y se supondrá que el usuario ha hecho clic en Cancelar en el cuadro de diálogo de selección de archivos.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AllowFileSelectionDialogs
  - Nombre de GP: permitir cuadros de diálogo en la selección de archivos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AllowFileSelectionDialogs
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AllowFileSelectionDialogs
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AllowPopupsDuringPageUnload

  #### Permitir que una página muestre elementos emergentes durante su descarga

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Esta directiva permite a un administrador especificar que una página puede mostrar mensajes emergentes durante su descarga.

Cuando la Directiva está configurada en habilitada, se permite que las páginas muestren mensajes emergentes mientras se descargan.

Cuando la Directiva está configurada en habilitada o deshabilitada, se permite que las páginas muestren mensajes emergentes mientras se descargan. Esto es lo que se contempla en SPEC:https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name)

En el futuro se eliminará esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AllowPopupsDuringPageUnload
  - Nombre de GP: permitir que la página muestre los elementos emergentes durante su descarga
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AllowPopupsDuringPageUnload
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AllowPopupsDuringPageUnload
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AllowSurfGame

  #### Permitir el juego surf

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 83 o posterior

  #### Descripción

  Si deshabilita esta directiva, los usuarios no podrán jugar al juego de surf cuando el dispositivo esté desconectado o si el usuario navega a edge://surf.

Si habilita o no configura esta directiva, los usuarios podrán jugar al juego de surf.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AllowSurfGame
  - Nombre de GP: permitir el juego de surf
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AllowSurfGame
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AllowSurfGame
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AllowSyncXHRInPageDismissal

  #### Permitir que las páginas envíen solicitudes de XHR sincrónicas durante el descarte de página (en desuso)

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En Windows y macOS desde 79 o posterior

  #### Descripción

  Esta directiva está en desuso porque solo pretende ser un mecanismo a corto plazo para dar a las empresas más tiempo para actualizar su contenido web cuando se ha comprobado que es incompatible con el cambio para no permitir solicitudes de XHR sincrónicas durante el descarte de la página. No funciona en la versión 88 de Microsoft Edge.

Esta directiva le permite especificar que una página puede enviar solicitudes de XHR sincrónico durante el descarte de la página.

Si habilita esta directiva, las páginas podrán enviar solicitudes de XHR sincronizadas durante el descarte de la página.

Si deshabilita esta directiva o no la configura, las páginas no podrán enviar solicitudes de XHR sincronizadas durante el descarte de la página.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AllowSyncXHRInPageDismissal
  - Nombre de DG: permitir que las páginas envíen solicitudes sincrónicas de XHR durante el descarte de página (en desuso)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AllowSyncXHRInPageDismissal
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AllowSyncXHRInPageDismissal
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AllowTokenBindingForUrls

  #### Configurar la lista de sitios con los que Microsoft Edge intentará establecer un enlace de tokens.

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 83 o posterior

  #### Descripción

  Configura la lista de patrones de dirección URL para los sitios con los que el navegador intentará realizar el protocolo de enlace de tokens.
Para los dominios de esta lista, el explorador enviará el enlace de tokens ClientHello en el protocolo de enlace TLS (Ver https://tools.ietf.org/html/rfc8472).
Si el servidor responde con una respuesta válida de ServerHello, el explorador creará y enviará mensajes de enlace de token en las siguientes solicitudes https. Vea https://tools.ietf.org/html/rfc8471 para obtener más información.

Si esta lista está vacía, se deshabilitará el enlace de token.

Esta directiva solo está disponible en los dispositivos Windows 10 con capacidad de Modo seguro virtual.

A partir de Microsoft Edge 86, esta directiva ya no es compatible con la actualización dinámica.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AllowTokenBindingForUrls
  - Nombre de GP: configurar la lista de sitios con los que Microsoft Edge intentará establecer un enlace de tokens.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\AllowTokenBindingForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [Volver al principio](#microsoft-edge---policies)

  ### AllowTrackingForUrls

  #### Configurar excepciones de prevención de seguimiento para determinados específicos

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Configura la lista de patrones de dirección URL que están excluidos de la prevención de seguimiento.

Si configura esta directiva, la lista de patrones de dirección URL configurados se excluirán de la prevención de seguimiento.

Si no configura esta directiva se utilizará para todos los sitios el valor global predeterminado de la directiva "Bloquear el seguimiento de la actividad de exploración de la web de los usuarios" (si está establecido) o la configuración personal del usuario para todos los sitios.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AllowTrackingForUrls
  - Nombre de GP: configurar las excepciones para la prevención de seguimiento en sitios determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\AllowTrackingForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AllowTrackingForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AlternateErrorPagesEnabled

  #### Sugiere páginas similares cuando no se puede encontrar una página web.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Permite que Microsoft Edge emita una conexión a un servicio web para generar dirección URL y buscar sugerencias para problemas de conectividad como errores de DNS.

Si habilita esta directiva, se utilizará un servicio web para gener una dirección URL y buscar sugerencias de errores en la red.

Si deshabilita esta directiva, no se realizarán llamadas al servicio web y se mostrará una página de error estándar.

Si no configura esta directiva, Microsoft Edge respetará la preferencia de usuario establecida en Servicios en Edge://configuración/privacidad.
En concreto, hay una **sugerir páginas similares cuando no se puede encontrar una página web** conmutar, en la que el usuario puede activar o desactivar la opción. Tenga en cuenta que si habilitó esta directiva (AlternateErrorPagesEnabled), la opción Sugerir páginas similares cuando no se puede encontrar una página web estará activada, pero el usuario no podrá cambiar la configuración con la tecla de alternancia. Si deshabilita esta directiva, la opción Sugerir páginas similares cuando no se puede encontrar una página web estará desactivada, y el usuario no podrá cambiar la configuración con la tecla de alternancia.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AlternateErrorPagesEnabled
  - Nombre de GP: Sugerir páginas similares cuando no se pueda encontrar una página web
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: AlternateErrorPagesEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AlternateErrorPagesEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AlwaysOpenPdfExternally

  #### Abrir siempre los archivos PDF externamente

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Deshabilita el visor de PDF interno en Microsoft Edge.

Si habilita esta directiva, Microsoft Edge tratará los archivos PDF como descargas y permitirá a los usuarios abrirlos con la aplicación predeterminada.

Si no configura esta directiva o la deshabilita, Microsoft Edge abrirá archivos PDF (a menos que el usuario la deshabilite).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AlwaysOpenPdfExternally
  - Nombre de GP: siempre abrir los archivos en formato PDF de forma externa
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AlwaysOpenPdfExternally
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AlwaysOpenPdfExternally
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AmbientAuthenticationInPrivateModesEnabled

  #### Habilitar la autenticación de ambiente para los perfiles InPrivate o Invitado

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 81 o posterior

  #### Descripción

  Configura esta directiva para permitir o desactivar la autenticación del entorno para los perfiles de InPrivate e Invitado en Microsoft Edge.

La autenticación del entorno es la autenticación http con credenciales predeterminadas cuando no se proporcionan credenciales explícitas mediante los esquemas de desafío/respuesta de NTLM/Kerberos/Negociar.

Si establece la directiva en "RegularOnly", solo se permitirá la autenticación del entorno para las sesiones Regulares. Las sesiones de InPrivate e Invitado no se les permitirá autenticarse con el entorno.

Si establece la Directiva en "InPrivateAndRegular", se permite la autenticación de ambiente para las sesiones InPrivate y Regular. A las sesiones de Invitado no se les permitirá autenticarse con el entorno.

Si establece la Directiva en "GuestAndRegular", permitirá la autenticación del entorno para las sesiones Invitado y Regular. Las sesiones de InPrivate no se les permitirá autenticarse en el entorno

Si establece la Directiva en "Todas", permitirá la autenticación del entorno para todas las sesiones.

Tenga en cuenta que la autenticación del entorno siempre está permitida en los perfiles regulares.

En la versión 81 y posteriores de Microsoft Edge, si no se establece la directiva, la autenticación del entorno se habilitará solo en las sesiones regulares.

Asignación de opciones de directiva:

* RegularOnly (0) = habilitar la autenticación del entorno solo en las sesiones regulares

* InPrivateAndRegular (1) = habilitar la autenticación del entorno en las sesiones InPrivate y regulares

* GuestAndRegular (2) = habilitar la autenticación del entorno en las sesiones de invitado y regulares

* Todas (3) = habilitar la autenticación del entorno en las sesiones regulares, InPrivate y de invitado

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AmbientAuthenticationInPrivateModesEnabled
  - Nombre de GP: habilitar la autenticación de ambiente para los perfiles InPrivate o de invitado
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AmbientAuthenticationInPrivateModesEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AmbientAuthenticationInPrivateModesEnabled
  - Valor de ejemplo:
``` xml
<integer>0</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AppCacheForceEnabled

  #### Permite volver a habilitar la característica AppCache, incluso si está desactivada de forma predeterminada.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 84 o posterior

  #### Descripción

  Si establece esta directiva en "true", la AppCache está habilitada, aunque AppCache en Microsoft Edge no esté disponible de forma predeterminada.

Si establece esta directiva en falso, o no la establece, AppCache seguirá las opciones predeterminadas de Microsoft Edge.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AppCacheForceEnabled
  - Nombre de GP: permite volver a habilitar la característica AppCache, incluso si está desactivada de forma predeterminada.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AppCacheForceEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: AppCacheForceEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ApplicationLocaleValue

  #### Establecer la configuración regional de la aplicación

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 77 o posterior

  #### Descripción

  Configura la configuración regional de la aplicación en Microsoft Edge y evita que los usuarios cambien la localización.

Si habilita esta Directiva, Microsoft Edge use la configuración regional indicada. Si no es compatible con la configuración regional configurada, se usa en su lugar "en-US".

Si deshabilita o no configura esta opción, Microsoft Edge usa la configuración regional preferida especificada por el usuario (si está configurada) o la configuración regional de suplencia "en-US".

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ApplicationLocaleValue
  - Nombre de GP: establecer la configuración regional de la aplicación
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ApplicationLocaleValue
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"en"
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### AudioCaptureAllowed

  #### Permitir o bloquear captura de audio

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite definir si se pide a un usuario que conceda a un sitio web acceso al dispositivo de captura de audio. Esta directiva se aplica a todas las direcciones URL excepto aquellas configuradas en la lista [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Si habilita esta directiva o no la configura (la configuración predeterminada), se le pedirá al usuario el acceso de captura de audio excepto de las direcciones URL en la lista [AudioCaptureAllowedUrls](#audiocaptureallowedurls). A estas URL de la lista se les concede acceso sin pedir confirmación.

Si deshabilita esta directiva, no se le pedirá al usuario y solo se podrá obtener acceso a la captura de audio para las direcciones URL configuradas en [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Esta directiva afecta a todos los tipos de entradas de audio, no solo al micrófono integrado.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AudioCaptureAllowed
  - Nombre de GP: permitir o bloquear la captura de audio
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AudioCaptureAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AudioCaptureAllowed
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AudioCaptureAllowedUrls

  #### Sitios que pueden acceder a dispositivos de captura de audio sin solicitar permiso

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especificar sitios web basándose en modelos URL que pueden usar dispositivos de captura de audio sin pedir permiso al usuario. Los patrones en esta lista se hacen coincidir con el origen de seguridad de la dirección URL que realiza la solicitud. Si son coincidentes, el sitio tiene acceso automático a los dispositivos de captura de audio.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AudioCaptureAllowedUrls
  - Nombre de GP: sitios que pueden acceder a los dispositivos de captura de audio sin solicitar permiso
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\AudioCaptureAllowedUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AudioCaptureAllowedUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AudioSandboxEnabled

  #### Permitir ejecutar el espacio aislado de audio.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 81 o posterior

  #### Descripción

  Esta directiva controla el espacio aislado del proceso de audio.

Si habilita esta directiva, el proceso de audio se ejecutará en espacio aislado.

Si deshabilita esta directiva, el proceso de audio se ejecutará sin recinto y el módulo de procesamiento de audio WebRTC se ejecutará en el proceso de representación.
Esto deja a los usuarios vulnerables a los riesgos de seguridad relacionados con la ejecución del subsistema de audio no aislado..

Si no configura esta directiva, se usará la configuración predeterminada para el espacio aislado de audio, lo que puede variar en función de la plataforma.

Esta directiva está pensada para ofrecer a las empresas la flexibilidad necesaria para deshabilitar el espacio aislado de audio si usan configuraciones de software de seguridad que interfieren con el espacio aislado.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AudioSandboxEnabled
  - Nombre de GP: permitir la ejecución del espacio aislado de audio
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AudioSandboxEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AudioSandboxEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AutoImportAtFirstRun

  #### Importar automáticamente los datos y la configuración desde otro explorador en la primera ejecución

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Si habilita esta directiva, todas las configuraciones y tipos de datos admitidos del explorador especificado se importarán de forma silenciosa y automática en la primera ejecución. Durante la primera experiencia de ejecución, también se omitirá la sección de importación.

Los datos del explorador de Microsoft Edge (versión anterior) siempre se migrarán de forma silenciosa en la primera ejecución, independientemente del valor de esta directiva.

Si se establece esta directiva en "FromDefaultBrowser", se importarán los tipos de datos correspondientes al explorador predeterminado del dispositivo administrado.

Si el explorador especificado como valor de esta directiva no está presente en el dispositivo administrado, Microsoft Edge simplemente omitirá la importación sin notificar al usuario.

Si establece esta directiva en "DisabledAutoImport", la sección de importación de la primera ejecución se omitirá por completo y Microsoft Edge no importará los datos y la configuración del explorador automáticamente.

Si se establece esta directiva en el valor "FromInternetExplorer", se importarán los siguientes tipos de datos de Internet Explorer:
1. Favoritos o marcadores
2. Contraseñas guardadas
3. Motores de búsqueda
4. Historial de exploración
5. Página principal

Si se establece esta directiva en el valor "FromGoogleChrome", se importarán los siguientes tipos de datos de Google Chrome:
1. Favoritos
2. Contraseñas guardadas
3. Direcciones y mucho más
4. Información de pago
5. Historial de exploración
6. Configuración
7. Pestañas ancladas y abiertas
8. Extensions
9. Cookies

Nota: para obtener más información sobre lo que se importa en Google Chrome, vea [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

Si se establece esta directiva en el valor "FromSafari", los datos de usuario ya no se importarán en Microsoft Edge. Esto se debe a la forma en que el acceso total al disco funciona en Mac.
Ya no es posible tener una importación automatizada y desatendida de datos de Safari en Microsoft Edge en macOS Mojave y versiones posteriores.

A partir de la versión 83 de Microsoft Edge, si se establece esta directiva en el valor "FromMozillaFirefox", se importarán los siguientes tipos de datos de Mozilla Firefox:
1. Favoritos o marcadores
2. Contraseñas guardadas
3. Direcciones y mucho más
4. Historial de Exploración

Si desea restringir los tipos de datos específicos para que no se importen en los dispositivos administrados, puede usar esta directiva con otras directivas, como [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites), etc.

Asignación de opciones de directiva:

* FromDefaultBrowser (0) = importa automáticamente todos los tipos de datos y configuraciones compatibles con el explorador predeterminado.

* FromInternetExplorer (1) = importa automáticamente todos los tipos de datos y configuraciones compatibles desde Internet Explorer

* FromGoogleChrome (2) = importa automáticamente todos los tipos de datos y configuraciones compatibles desde Google Chrome

* FromSafari (3) = importa automáticamente todos los tipos de datos y configuraciones compatibles desde Safari

* DisabledAutoImport (4) = deshabilita la importación automática, y se omite la sección de importación de la experiencia de primera ejecución

* FromMozillaFirefox (5) = importa automáticamente todos los tipos de datos y configuraciones compatibles desde Mozilla Firefox

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AutoImportAtFirstRun
  - Nombre de GP: importar los datos y la configuración de otro navegador automáticamente durante la primera ejecución
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AutoImportAtFirstRun
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AutoImportAtFirstRun
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AutoLaunchProtocolsFromOrigins

  #### Definir una lista de protocolos para iniciar una aplicación externa desde orígenes de la lista sin pedir al usuario

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 85 o posterior

  #### Descripción

  Permite configurar una lista de protocolos y, para cada protocolo, una lista asociada de patrones de origen permitidos que pueden iniciar una aplicación externa sin tener que preguntar al usuario. El separador final no se debe incluir cuando se enumera el protocolo. Por ejemplo, Enumera "skype" en lugar de "skype:" o "skype://".

Si configura esta Directiva, solo se permitirá que un protocolo inicie una aplicación externa sin tener que preguntar por la Directiva si:

- se mostrará el protocolo

- el origen del sitio que intenta iniciar el protocolo coincide con uno de los patrones de origen en la lista allowed_origins del protocolo.

Si alguna de las condiciones es false, el mensaje de inicio del protocolo externo no se omitirá por directiva.

Si no configura esta Directiva, no se puede iniciar ningún protocolo sin una indicación. Los usuarios pueden optar por no recibir mensajes para cada protocolo o por sitio, salvo que la Directiva [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) se configure como deshabilitada. Esta directiva no afecta a las exenciones de mensaje por protocolo/por sitio establecidas por los usuarios.

Los modelos de coincidencia de origen usan un formato similar al de la Directiva de [ URLBlocklist](#urlblocklist), que se explican en [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Sin embargo, los patrones de coincidencia de origen para esta Directiva no pueden contener elementos "/path" o "@query". Cualquier patrón que contenga un elemento "/path" o "@query" se pasará por alto.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AutoLaunchProtocolsFromOrigins
  - Nombre de directiva de usuario: definir una lista de protocolos que pueden iniciar una aplicación externa desde orígenes de la lista sin preguntar
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AutoLaunchProtocolsFromOrigins
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [
  {
    "allowed_origins": [
      "example.com", 
      "http://www.example.com:8080"
    ], 
    "protocol": "spotify"
  }, 
  {
    "allowed_origins": [
      "https://example.com", 
      "https://.mail.example.com"
    ], 
    "protocol": "teams"
  }, 
  {
    "allowed_origins": [
      "*"
    ], 
    "protocol": "outlook"
  }
]
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [{"allowed_origins": ["example.com", "http://www.example.com:8080"], "protocol": "spotify"}, {"allowed_origins": ["https://example.com", "https://.mail.example.com"], "protocol": "teams"}, {"allowed_origins": ["*"], "protocol": "outlook"}]
  ```
  

  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: AutoLaunchProtocolsFromOrigins
  - Valor de ejemplo:
``` xml
<key>AutoLaunchProtocolsFromOrigins</key>
<array>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>example.com</string>
      <string>http://www.example.com:8080</string>
    </array>
    <key>protocol</key>
    <string>spotify</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>https://example.com</string>
      <string>https://.mail.example.com</string>
    </array>
    <key>protocol</key>
    <string>teams</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>*</string>
    </array>
    <key>protocol</key>
    <string>outlook</string>
  </dict>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AutoOpenAllowedForURLs

  #### URL donde se pueden aplicar AutoOpenFileTypes

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 85 o posterior

  #### Descripción

  Lista de direcciones URL a las que se aplicará [AutoOpenFileTypes](#autoopenfiletypes). Esta Directiva no tiene ningún impacto en los valores abiertos automáticamente establecidos por los usuarios a través de la estante de descarga... > Entrada de menú "abrir archivos siempre para este tipo".

Si configura direcciones URL en esta Directiva, los archivos solo se abrirán automáticamente por Directiva si la dirección URL forma parte de este conjunto y el tipo de archivo se muestra en [AutoOpenFileTypes](#autoopenfiletypes). Si alguna de las condiciones es falsa, la descarga no se abrirá automáticamente por la Directiva.

Si no define esta Directiva, todas las descargas en las que el tipo de archivo está en [AutoOpenFileTypes](#autoopenfiletypes) se abrirán automáticamente.

Se tiene que dar formato a un modelo de dirección URL con el [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AutoOpenAllowedForURLs
  - Nombre GP: direcciones URL donde se puede aplicar AutoOpenFileTypes
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\PopupsAllowedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: AutoOpenAllowedForURLs
  - Valor de ejemplo:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AutoOpenFileTypes

  #### Lista de tipos de archivo que se deben abrir automáticamente al descargarse

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 85 o posterior

  #### Descripción

  Esta Directiva establece una lista de los tipos de archivo que se abrirán automáticamente en la descarga. Nota: no es necesario incluir el separador inicial cuando se indica el tipo de archivo, por lo que debe indicar "txt" en lugar de ". txt".

De forma predeterminada, estos tipos de archivo se abrirán automáticamente en todas las direcciones URL. Puede usar la Directiva [AutoOpenAllowedForURLs](#autoopenallowedforurls) para restringir las direcciones URL para las que se abrirán automáticamente estos tipos de archivo.

Los archivos con tipos que se deben abrir de forma automática seguirán sujetos a las comprobaciones de SmartScreen de Microsoft defender habilitadas y no se abrirán si se producen errores en esas comprobaciones.

Los tipos de archivos que el usuario ya especificó para que se abran automáticamente seguirán haciéndolos cuando se descarguen. El usuario seguirá pudiendo especificar que se abran automáticamente otros tipos de archivo.

Si no define esta Directiva, solo los tipos de archivo que el usuario ya especificó que se abriera automáticamente lo hará cuando se descargue.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AutoOpenFileTypes
  - Nombre GP: lista de los tipos de archivo que se abrirán automáticamente al descargarse
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\URLBlocklist
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: AutoOpenFileTypes
  - Valor de ejemplo:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AutofillAddressEnabled

  #### Habilitar Autorrellenar para las direcciones

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilita la característica Autorrellenar y permite a los usuarios completar automáticamente la información de dirección en formularios web con información almacenada anteriormente.

Si deshabilita esta directiva, Autorrellenar nunca sugiere o rellena la información de la dirección, ni tampoco guarda información adicional de la dirección que pueda enviar el usuario mientras está explorando la Web.

Si habilita esta directiva o no la configura, los usuarios podrán controlar la función de Autorellenar para direcciones en la interfaz de usuario.

Tenga en cuenta que si deshabilita esta directiva, también detendrá toda la actividad de todos los formularios web, excepto los formularios de pago y contraseña. No se guardan más entradas, y Microsoft Edge no sugiere ni autorellena ninguna entrada anterior.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AutofillAddressEnabled
  - Nombre de GP: habilitar el autorrelleno para las direcciones
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: AutofillAddressEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AutofillAddressEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AutofillCreditCardEnabled

  #### Habilitar Autorrellenar para las tarjetas de crédito

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilita la función de Autorrelleno de Microsoft Edge y permite a los usuarios autocompletar la información de la tarjeta de crédito en formularios web utilizando la información almacenada anteriormente.

Si deshabilita esta directiva, la función de Autorrellenar nunca sugerirá ni rellenará información de tarjetas de crédito, ni guardará información adicional de tarjetas de crédito que los usuarios puedan enviar mientras exploran la web.

Si habilita esta directiva o no la configura, los usuarios podrán controlar la función de Autorrellenar para las tarjetas de crédito.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AutofillCreditCardEnabled
  - Nombre de GP: habilitar el autorrelleno para las tarjetas de crédito
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: AutofillCreditCardEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AutofillCreditCardEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### AutoplayAllowed

  #### Permitir la reproducción automática multimedia para sitios web

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Esta directiva establece la directiva de reproducción automática multimedia para los sitios web.

La configuración predeterminada, "No configurada", respeta la configuración actual de reproducción automática multimedia y permite a los usuarios establecer su configuración de reproducción automática.

La configuración de "Habilitado" establece la reproducción automática multimedia en "Permitir".  Se permite que todos los sitio web puedan reproducir automáticamente multimedia. Los usuarios no pueden invalidar esta Directiva.

Si está en "Deshabilitado", la reproducción automática multimedia estará en "Bloquear".  No se permite a los sitios web la reproducción automática multimedia. Los usuarios no pueden invalidar esta Directiva.

Será necesario cerrar y volver a abrir una cuenta para que esta directiva tenga efecto.


  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: AutoplayAllowed
  - Nombre de GP: permitir la reproducción automática de multimedia en los sitios web
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: AutoplayAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: AutoplayAllowed
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### BackgroundModeEnabled

  #### Seguir ejecutando aplicaciones en segundo plano después de cerrar Microsoft Edge

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 77 o posterior

  #### Descripción

  Permite que los procesos de Microsoft Edge se inicien en el inicio de sesión del sistema operativo y sigan funcionando después de cerrar la última ventana del explorador. En este escenario, las aplicaciones en segundo plano y la sesión de exploración actual siguen activas, incluyendo las cookies de la sesión. Un proceso abierto en segundo plano muestra un icono en la bandeja del sistema y siempre se puede cerrar desde ahí.

Si se habilita esta directiva, se activará el modo en segundo plano.

Si deshabilita esta directiva, se desactivará el modo en segundo plano.

Si no configura esta directiva, el modo en segundo plano se desactivará inicialmente, y el usuario podrá configurar su comportamiento en edge://configuración/sistema.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: BackgroundModeEnabled
  - Nombre de GP: seguir ejecutando las aplicaciones en segundo plano después de cerrar Microsoft Edge
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: BackgroundModeEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### BackgroundTemplateListUpdatesEnabled

  #### Permitir actualizaciones en segundo plano de la lista de plantillas disponibles para Colecciones y otras características que utilizan plantillas

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 79 o posterior

  #### Descripción

  Le permite activar o desactivar las actualizaciones en segundo plano de la lista de plantillas disponibles para las colecciones y otras funciones que utilizan plantillas.  Las plantillas se usan para extraer metadatos enriquecidos de una página web cuando la página se guarda en una colección.

Si habilita esta configuración o la configuración no está configurada, la lista de plantillas disponibles se descargará en segundo plano desde un servicio de Microsoft cada 24 horas.

Si deshabilita esta configuración, la lista de plantillas disponibles se descargará a petición. Este tipo de descarga puede dar lugar a pequeñas sanciones de rendimiento para las colecciones y otras funciones.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: BackgroundTemplateListUpdatesEnabled
  - Nombre de GP: permitir las actualizaciones en segundo plano de la lista de plantillas disponibles para las colecciones y otras características que utilicen plantillas
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: BackgroundTemplateListUpdatesEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: BackgroundTemplateListUpdatesEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### BingAdsSuppression

  #### Bloquear todos los anuncios en los resultados de búsqueda de Bing.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 83 o posterior

  #### Descripción

  Habilita una experiencia de búsqueda sin anuncios en Bing.com

Si se habilita esta directiva, el usuario podrá realizar búsquedas en bing.com y tener una experiencia de búsqueda sin anuncios. Al mismo tiempo, la configuración de la Búsqueda Segura se establecerá en "Estricto" y no podrá ser cambiada por el usuario.

Si no configura esta directiva, la experiencia predeterminada tendrá anuncios en los resultados de búsqueda de bing.com. La búsqueda segura se establecerá en "Moderado" por defecto y podrá ser cambiada por el usuario.

Esta directiva solo está disponible para los SKUs K-12 identificados como inquilinos de EDU por Microsoft.

Por favor, vea[https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711) para obtener más información sobre esta directiva, o si se aplican las siguientes situaciones:

* Tiene un inquilino de la UDE, pero la directiva no funciona.

* En la lista blanca de direcciones IP se disponía de una experiencia de búsqueda gratis en anuncios.

* Estaba experimentando una experiencia de búsqueda sin anuncios en Microsoft Edge (versión anterior) y desea actualizarse a la nueva versión de Microsoft Edge.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: BingAdsSuppression
  - Nombre de GP: bloquear todos los anuncios en los resultados de búsqueda de Bing
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: BingAdsSuppression
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: BingAdsSuppression
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### BlockThirdPartyCookies

  #### Bloquear cookies de terceros

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Bloquee los elementos de la página web que no estén en el dominio de la barra de direcciones y configuren cookies.

Si habilita esta directiva, los elementos de la página web que no son del dominio que está en la barra de direcciones no pueden establecer cookies

Si deshabilita esta directiva, los elementos de la Página Web de dominios que no sean en la barra de direcciones podrán establecer cookies.

Si no configura esta directiva, las cookies de terceros se habilitan, pero los usuarios pueden cambiar esta opción.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: BlockThirdPartyCookies
  - Nombre de GP: bloquear las cookies de terceros
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: BlockThirdPartyCookies
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: BlockThirdPartyCookies
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### BrowserAddProfileEnabled

  #### Permitir la creación de perfiles desde el menú desplegable identidad o la página Configuración

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite a los usuarios crear nuevos perfiles, con la opción **agregar perfil**.
Si habilita esta Directiva o no la configura, Microsoft Edge permite a los usuarios usar **agregar perfiles** en el menú desplegable identidad o en la página Configuración para crear nuevos perfiles.

Si desactiva esta directiva, los usuarios no podrán agregar nuevos perfiles desde el menú desplegable Identidad o desde la página Configuración.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: BrowserAddProfileEnabled
  - Nombre de GP: habilitar la creación de perfiles en el menú desplegable de identidad o en la página de configuración
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: BrowserAddProfileEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: BrowserAddProfileEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### BrowserGuestModeEnabled

  #### Activar el modo invitado

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilita la opción para permitir el uso de perfiles de invitado en Microsoft Edge. Cuando se trata de un perfil de invitado, el navegador no puede importar los datos de navegación de los perfiles existentes y los elimina cuando se cierran todos los perfiles de invitado.

Si habilita esta Directiva o no la configura, Microsoft Edge le permite a los usuarios buscar en perfiles de invitado.

Si deshabilita esta directiva, Microsoft Edge no permite a los usuarios explorar los perfiles de invitado.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: BrowserGuestModeEnabled
  - Nombre de GP: habilitar el modo de invitado
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: BrowserGuestModeEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: BrowserGuestModeEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### BrowserNetworkTimeQueriesEnabled

  #### Permitir consultas a un servicio de tiempo de red del explorador

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Impide que Microsoft Edge envíe ocasionalmente consultas a un servicio de tiempo de la red del explorador para recuperar una marca de tiempo exacta.

Si deshabilita esta directiva, Microsoft Edge dejará de enviar consultas a un servicio de tiempo de la red del explorador.

Si habilita o no configura esta directiva, Microsoft Edge enviará ocasionalmente consultas a un servicio de tiempo de red del explorador.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: BrowserNetworkTimeQueriesEnabled
  - Nombre de GP: permitir las consultas al servicio de tiempo en la red del explorador
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: BrowserNetworkTimeQueriesEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: BrowserNetworkTimeQueriesEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### BrowserSignin

  #### Configuración de inicio de sesión del explorador

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica si un usuario puede iniciar sesión en Microsoft Edge con su cuenta y usar los servicios relacionados con la cuenta, como la sincronización y el inicio de sesión único. Para controlar la disponibilidad de la sincronización, use la directiva de [SyncDisabled](#syncdisabled) en su lugar.

Si establece esta directiva en "Deshabilitar", asegúrese de que también haya establecido la directiva [NonRemovableProfileEnabled](#nonremovableprofileenabled) como deshabilitada, ya que [NonRemovableProfileEnabled](#nonremovableprofileenabled) deshabilita la creación de un perfil para iniciar sesión automáticamente en el explorador. Si se establecen ambas directivas, Microsoft Edge usará la directiva "desactivar el inicio de sesión del navegador" y se comportará como si la directiva [NonRemovableProfileEnabled](#nonremovableprofileenabled) hubiese sido deshabilitada.

Si establece esta directiva en "Habilitar", los usuarios pueden iniciar sesión en el explorador. Iniciar sesión en el explorador no garantiza que la sincronización esté activada de forma predeterminada. El usuario deberá habilitarla por separado para poder usar esta característica.

Si establece esta directiva en "Forzar", los usuarios tendrán que iniciar sesión en un perfil para usar el explorador. De forma predeterminada, esto permite que el usuario elija si desea sincronizar con su cuenta, a menos que la sincronización esté deshabilitada por el administrador del dominio o con la directiva [SyncDisabled](#syncdisabled). El valor predeterminado de la directiva [BrowserGuestModeEnabled](#browserguestmodeenabled) está establecido como falso.

Si no configura esta directiva, los usuarios podrán decidir si desean habilitar la opción de inicio de sesión del explorador y usarla según les parezca adecuado.

Asignación de opciones de directiva:

* Deshabilitar (0) = deshabilitar el inicio de sesión del explorador

* Habilitar (1) = habilitar el inicio de sesión del explorador

* Forzar (2) = exigir a los usuarios iniciar sesión para usar el explorador

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: BrowserSignin
  - Nombre de GP: configuración del inicio de sesión en el explorador
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: BrowserSignin
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: BrowserSignin
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### BuiltInDnsClientEnabled

  #### Usar cliente DNS integrado

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Controla si se debe usar el cliente DNS integrado.

Esto no afecta a los servidores DNS que se usan; sino la pila de software que se utiliza para comunicarse con ellos. Por ejemplo, si el sistema operativo se configura para usar un servidor DNS empresarial, el cliente DNS integrado usaría ese mismo servidor. Sin embargo, es posible que el cliente DNS integrado se dirigirá a los servidores en diferentes formas al usar protocolos más modernos relacionados con DNS, como DNS a través de TLS.

Si habilita esta Directiva, el cliente DNS integrado se usa, si está disponible.

Si deshabilita esta Directiva, el cliente no se usa nunca.

Si no configura esta Directiva, el cliente DNS integrado está habilitado de forma predeterminada en el MacOS, y los usuarios pueden cambiar si lo usan para usar el cliente DNS integrado Si edita edge://flags o especifique el marcador de la línea de comandos.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: BuiltInDnsClientEnabled
  - Nombre de GP: usar el cliente integrado de DNS
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: BuiltInDnsClientEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: BuiltInDnsClientEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### BuiltinCertificateVerifierEnabled

  #### Determina si el comprobador de certificados integrado se usará para comprobar certificados de servidor (en desuso)

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En macOS desde 83 o posterior

  #### Descripción

  Esta directiva es obsoleta porque tiene por objeto servir únicamente como mecanismo a corto plazo para que las empresas dispongan de más tiempo para actualizar sus entornos e informar de los problemas si se comprueba que son incompatibles con el verificador de certificados incorporado.

No funcionará en la versión 87 de Microsoft Edge cuando se planee la eliminación del soporte técnico para el comprobador de certificados heredado en Mac OS X.


  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: BuiltinCertificateVerifierEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForCas

  #### Deshabilitar el certificado de transparencia para obtener una lista de hashes de PublicKeyInfo

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Deshabilita la aplicación de los requisitos de transparencia de certificados para una lista de hashes de subjectPublicKeyInfo.

Esta directiva permite deshabilitar los requisitos de divulgación sobre la transparencia de los certificados para las cadenas de certificados que contengan certificados con algunos de los hash de la asignatura especificadaPublicKeyInfo. Esto permite que los certificados que, de otra forma, no serían de confianza porque no se divulgaron públicamente de manera adecuada puedan seguir siendo usados por los servidores corporativos.

Para deshabilitar el cumplimiento de la transparencia de certificados al establecer esta directiva, se debe cumplir uno de los siguientes conjuntos de condiciones:
1. El hash corresponde al certificado del servidor subjectPublicKeyInfo.
2. El hash que corresponde a subjectPublicKeyInfo aparece en un certificado de CA en la cadena de certificados y está restringido a través de la extensión X.509v3 nameConstraints, uno o más directoryName nameConstraints están presentes en los permittedSubtrees, y el directoryName contiene un atributo organizationName.
3. El hash que corresponde a subjectPublicKeyInfo aparece en un certificado de CA en la cadena de certificados, el certificado de CA tiene uno o varios atributos organizationName en el asunto del certificado, además de que, el certificado del servidor contiene el mismo número de atributos organizationName en el mismo orden y con valores idénticos byte por byte.

Un algoritmo hash subjectPublicKeyInfo se especifica al concatenar el nombre del algoritmo hash, el carácter "/" y la codificación base64 del algoritmo hash que se aplicará al subjectPublicKeyInfo codificado en DER del certificado especificado. Esta codificación Base64 tiene el mismo formato que una huella digital SPKI, como se define en la sección 2,4 de RFC 7469. Se omiten los algoritmos hash no reconocidos. En este momento, el único algoritmo hash compatible es "SHA256".

Si deshabilita o no configura esta directiva, cualquier certificado que deba divulgarse a través de la transparencia de certificados se considerará de poca confianza si no se divulga de acuerdo con la directiva de transparencia de certificados

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: CertificateTransparencyEnforcementDisabledForCas
  - Nombre de GP: deshabilitar el certificado de transparencia para obtener una lista de hashes de PublicKeyInfo
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\CertificateTransparencyEnforcementDisabledForCa
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: CertificateTransparencyEnforcementDisabledForCas
  - Valor de ejemplo:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas

  #### Deshabilitar el certificado Aplicación de la transparencia para una lista de autoridades de certificación de legado

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Deshabilita la aplicación de los requisitos de transparencia de los certificados para obtener una lista de las entidades de certificación (CAS) heredadas.

Esta directiva permite deshabilitar los requisitos de divulgación sobre la transparencia de los certificados para las cadenas de certificados que contengan certificados con algunos de los hash de la asignatura especificadaPublicKeyInfo. Esto permite que los certificados que, de otra forma, no serían de confianza porque no se divulgaron públicamente de manera adecuada sigan usándose para los servidores corporativos.

Para que se deshabilite la aplicación de transparencia de certificados, debe establecerse el valor de hash en un subjectPublicKeyInfo que aparezca en un certificado de CA reconocido como entidad de certificación (CA) heredada. Una entidad de certificación heredada (CA), es una CA que ha sido reconocida públicamente como predeterminada por uno o más sistemas operativos compatibles con Microsoft Edge.

Se especifica un hash de subjectPublicKeyInfo concatenando el nombre del algoritmo hash, el carácter "/" y la codificación base64 del algoritmo hash que se aplicará al subjectPublicKeyInfo codificado en DER del certificado especificado. Esta codificación Base64 tiene el mismo formato que una huella digital SPKI, como se define en la sección 2,4 de RFC 7469. Se omiten los algoritmos hash no reconocidos. En este momento, el único algoritmo hash compatible es "SHA256".

Si no configura esta directiva, cualquier certificado que deba divulgarse a través de la transparencia de certificados se considerará de poca confianza si no se divulga de acuerdo con la directiva de transparencia de certificados

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Nombre de GP: deshabilitar el certificado de transparencia para obtener una lista de las entidades de certificación heredadas
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Valor de ejemplo:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForUrls

  #### Deshabilitar la aplicación de la transparencia de certificados para dirección URL determinadas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Deshabilita la aplicación de los requisitos de transparencia de los certificados en las direcciones URL indicadas.

Esta directiva le permite no divulgar los certificados de los nombres de host en las direcciones URL especificadas por la transparencia de certificados. Esto le permite usar certificados que de otro modo no serían de confianza, ya que no fueron divulgados públicamente de forma correcta, lo que dificulta la detección de los certificados que fueron emitidos de forma errónea en estos servidores.

Forme el modelo de URL de acuerdo con [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Dado que los certificados son válidos para un nombre de host determinado, independientemente del esquema, puerto o ruta de acceso, sólo se considerará una parte del nombre de host de la dirección URL. Los hosts comodín no son compatibles.

Al no configurar esta directiva, cualquier certificado que deba divulgarse a través de la transparencia de certificados es considerado como no confiable si no es revelado.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: CertificateTransparencyEnforcementDisabledForUrls
  - Nombre de GP: deshabilitar la aplicación de transparencia de certificados para direcciones de URL determinadas
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: CertificateTransparencyEnforcementDisabledForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ClearBrowsingDataOnExit

  #### Borrar los datos de exploración cuando se cierra Microsoft Edge

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Microsoft Edge no desactiva los datos de examen de manera predeterminada cuando se cierra. La búsqueda de datos incluye la información que se especifica en los formularios, las contraseñas e incluso los sitios web que se visitan.

Si habilita esta Directiva, todos los datos de examen se eliminan cada vez que se cierra Microsoft Edge. Tenga en cuenta que, si habilita esta Directiva, tiene prioridad sobre la configuración [DefaultCookiesSetting](#defaultcookiessetting)

Si deshabilita o no configura esta directiva, los usuarios pueden configurar la opción Borrar datos de navegación en Configuración.

Si habilita esta directiva, no configure la [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) o el [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) directiva, ya que todos tratan sobre cómo eliminar datos de exploración. Si configura las directivas anteriores y esta directiva, todos los datos de navegación se eliminan al cerrar Microsoft Edge, independientemente de cómo haya configurado [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) o [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

Para impedir que se eliminen las cookies al salir, configure la directiva [SaveCookiesOnExit](#savecookiesonexit) .

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ClearBrowsingDataOnExit
  - Nombre de GP: borrar los datos de exploración al cerrar Microsoft Edge
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ClearBrowsingDataOnExit
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ClearBrowsingDataOnExit
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ClearCachedImagesAndFilesOnExit

  #### Limpie las imágenes y los archivos almacenados en caché cuando se cierra Microsoft Edge

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 83 o posterior

  #### Descripción

  De forma predeterminada, Microsoft Edge no borra las imágenes y los archivos almacenados en caché cuando se cierra.

Si habilita esta Directiva, los archivos y las imágenes que están almacenadas en la caché se eliminarán cada vez que se cierre Microsoft Edge.

Si deshabilita esta Directiva, los usuarios no podrán configurar la opción de archivos e imágenes en caché en edge://settings/clearBrowsingDataOnClose.

Si no configura esta Directiva, los usuarios pueden elegir si las imágenes y los archivos almacenados en caché son eliminados al salir de.

Si deshabilita esta Directiva, no habilite la Directiva de [ ClearBrowsingDataOnExit](#clearbrowsingdataonexit), ya que ambos tratan sobre la eliminación de datos. Si configura ambas opciones, la Directiva [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) tendrá prioridad y eliminará todos los datos cuando se cierre Microsoft Edge, independientemente de cómo haya configurado [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ClearCachedImagesAndFilesOnExit
  - Nombre de GP: limpiar las imágenes y los archivos almacenados en el caché al cerrar Microsoft Edge
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ClearCachedImagesAndFilesOnExit
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ClearCachedImagesAndFilesOnExit
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ClickOnceEnabled

  #### Permitir que los usuarios abran archivos mediante el protocolo ClickOnce

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 78 o posterior

  #### Descripción

  Permita que los usuarios abran los archivos mediante el protocolo ClickOnce El protocolo ClickOnce permite que los sitios web soliciten que el explorador abra archivos de una dirección URL específica mediante el controlador de archivos de ClickOnce en el equipo o dispositivo del usuario.

Si habilita esta Directiva, los usuarios pueden abrir archivos mediante el protocolo ClickOnce. Esta directiva reemplaza la configuración de ClickOnce del usuario en la página edge://flags/.

Si deshabilita esta Directiva, los usuarios no podrán abrir archivos con el protocolo ClickOnce. En su lugar, el archivo se guardará en el sistema de archivos usando el explorador. Esta directiva reemplaza la configuración de ClickOnce del usuario en la página edge://flags/.

Si no configura esta Directiva, los usuarios con versiones de Microsoft Edge anteriores a Microsoft Edge 87 no podrán abrir archivos mediante el protocolo ClickOnce de forma predeterminada. Sin embargo, los usuarios tienen la opción de habilitar el uso del protocolo ClickOnce con la página edge://flags/. Los usuarios con las versiones 87 y posteriores de Microsoft Edge pueden abrir archivos con el protocolo ClickOnce de forma predeterminada, pero tienen la opción de deshabilitarlo mediante la página edge://flags/.

Deshabilitar ClickOnce puede impedir que las aplicaciones ClickOnce (archivos. Application) se inicien correctamente.

Para obtener más información sobre ClickOnce, vea [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) y [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ClickOnceEnabled
  - Nombre de GP: permitir que los usuarios abran los archivos mediante el protocolo ClickOnce
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ClickOnceEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### CollectionsServicesAndExportsBlockList

  #### Bloquear el acceso a una lista especificada de servicios y destinos de exportación en Colecciones

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Enumera los servicios y destinos de exportación específicos a los que los usuarios no pueden obtener acceso en la característica Colecciones de Microsoft Edge. Esto incluye mostrar datos adicionales de Bing y exportar colecciones a asociados externos o productos de Microsoft.

Si habilita esta directiva, los servicios y destinos de exportación que coincidan con la lista determinada estarán bloqueados.

Si no configura esta Directiva, no se aplicarán restricciones sobre los servicios y destinos de exportación aceptables.

Asignación de opciones de directiva:

* pinterest_suggestions (pinterest_suggestions) = sugerencias de Pinterest

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: CollectionsServicesAndExportsBlockList
  - Nombre de GP: bloquear el acceso a una lista especificada de servicios y destinos de exportación en Colecciones
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: CollectionsServicesAndExportsBlockList
  - Valor de ejemplo:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### CommandLineFlagSecurityWarningsEnabled

  #### Habilitar advertencias de seguridad para indicadores de la línea de comandos

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Si se deshabilita, esta directiva evita que las advertencias de seguridad aparezcan cuando se inicia Microsoft Edge el marcador de la línea de comandos potencialmente peligrosas.

Aun si está habilitado o no, las advertencias de seguridad se mostrarán cuando estos marcadores de línea de comandos se utilicen para iniciar Microsoft Edge.

Por ejemplo, el marcador de --disable-gpu-sandbox genera esta advertencia:  Estás usando un marcador de línea de comandos que no es compatible: --disable-gpu-sandbox. Esto constituye un riesgo para la estabilidad y la seguridad.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: CommandLineFlagSecurityWarningsEnabled
  - Nombre de GP: habilitar las advertencias de seguridad para los indicadores de la línea de comandos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: CommandLineFlagSecurityWarningsEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: CommandLineFlagSecurityWarningsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ComponentUpdatesEnabled

  #### Habilitar las actualizaciones de los componentes en Microsoft Edge

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Si habilita o no configura esta directiva, se habilitarán las actualizaciones de componentes en Microsoft Edge.

Si deshabilita esta directiva o se establece como falsa, se deshabilitarán las actualizaciones de componentes para todos los componentes de Microsoft Edge.

Sin embargo, en esta directiva se omiten algunos componentes. Esto incluye cualquier componente que no contenga un código ejecutable, que no cambie significativamente el comportamiento del explorador, o que sea crítico para la seguridad. Es decir, las actualizaciones que se consideran "críticas para la seguridad" y se seguirán aplicando incluso si deshabilita esta directiva

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ComponentUpdatesEnabled
  - Nombre de GP: habilitar las actualizaciones de los componentes en Microsoft Edge
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ComponentUpdatesEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ComponentUpdatesEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ConfigureDoNotTrack

  #### Configurar No realizar seguimiento

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifique si se enviarán solicitudes de No realizar seguimiento a sitios web que soliciten información de seguimiento. No realizar un seguimiento de las solicitudes permite que los sitios web que visite sepan que no desea que se realice un seguimiento de su actividad de navegación. De forma predeterminada, Microsoft Edge no envía solicitudes de No seguimiento, pero los usuarios pueden activar esta característica para enviarlas.

Si habilita esta directiva, las solicitudes de no realizar seguimiento siempre se enviarán a sitios web que soliciten información de seguimiento.

Si deshabilita esta directiva, las solicitudes nunca se enviarán.

Si no configura esta directiva, los usuarios podrán elegir si enviar estas solicitudes.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ConfigureDoNotTrack
  - Nombre de GP: configurar No realizar seguimiento
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ConfigureDoNotTrack
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ConfigureDoNotTrack
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ConfigureFriendlyURLFormat

  #### Configura el formato de pegado predeterminado de las direcciones URL copiadas desde Microsoft Edge y determina si los formatos adicionales estarán disponibles para los usuarios.

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 87 o posterior

  #### Descripción

  Si FriendlyURLs están habilitadas, Microsoft Edge calculará representaciones adicionales de la dirección URL y las colocará en el portapapeles.

Esta directiva configura el formato que se pegará cuando el usuario pegue en aplicaciones externas o dentro de Microsoft Edge sin el elemento de menú contextual "pegar como".

Si se configura, esta directiva hace una elección en lugar del usuario. Las opciones de edge://settings/shareCopyPaste aparecerán atenuadas y las opciones del menú contextual "Pegar como" no estarán disponibles.

* Sin configurar = el usuario podrá elegir el formato de pegado que prefiera. De forma predeterminada, se establece en el formato descriptivo de la dirección URL. El menú "pegar como" estará disponible en Microsoft Edge.

* 1 = no se almacenarán formatos adicionales en el portapapeles. No habrá ningún elemento de menú contextual de "pegar como" en Microsoft Edge y el único formato disponible para pegar será el formato de la dirección URL en texto sin formato. La característica URL descriptiva se deshabilitará de forma eficaz.

* 3 = el usuario recibirá una dirección URL descriptiva cada vez que las copie en superficies que acepten texto enriquecido. La dirección URL sin formato aún estará disponible para las superficies sin riqueza. No se mostrará el menú "pegar como" en Microsoft Edge.

* 4 = (no se usa actualmente)

Es posible que los formatos más ricos no sean muy compatibles en algunos destinos de pegado o en sitios Web. Por lo tanto, si se configura esta Directiva, se recomienda usar la opción URL normal.

Asignación de opciones de directiva:

* PlainText (1) = la dirección URL normal sin ninguna información adicional, como el título de la página. Esta es la opción recomendada cuando se configura esta Directiva. Para obtener más información, consulte:

* TitledHyperlink (3) = Hipervículo titulado: Un hipervínculo que señala a la dirección URL copiada, pero cuyo texto visible corresponde al título de la página de destino. Este es el formato descriptivo de la dirección URL.

* WebView (4): próximamente. Si se establece, se comporta igual que "dirección URL sin formato".

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ConfigureFriendlyURLFormat
  - Nombre de GP: Configura el formato de pegado predeterminado de las direcciones URL copiadas desde Microsoft Edge y determina si los formatos adicionales estarán disponibles para los usuarios.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ConfigureFriendlyURLFormat
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000003
```

  

  [Volver al principio](#microsoft-edge---policies)

  ### ConfigureOnPremisesAccountAutoSignIn

  #### Configurar el inicio de sesión automático con una cuenta de dominio de Active Directory cuando no haya cuenta de dominio de Azure AD

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 81 o posterior

  #### Descripción

  Habilita el uso de cuentas de Active Directory para el inicio de sesión automático en caso de que los equipos de los usuarios se unan a un dominio y el entorno no se haya unido de forma híbrida. Si desea que los usuarios inicien sesión automáticamente con sus cuentas de Azure Active Directory, en su lugar, llame a Azure AD join (vea[https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197) para obtener más información) o a una combinación híbrida (vea[https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) para obtener más información) en su entorno.

Si ha configurado la directiva[BrowserSignin](#browsersignin) como deshabilitada, esta directiva no tendrá ningún efecto.

Si habilita esta directiva y la establece en "SignInAndMakeDomainAccountNonRemovable", Microsoft Edge iniciará automáticamente la sesión de los usuarios que estén en equipos unidos a un dominio mediante sus cuentas de Active Directory.

Si establece esta directiva como "Deshabilitada" o no la establece, Microsoft Edge no iniciará sesión automáticamente a los usuarios que se encuentren en equipos unidos a un dominio con cuentas de Active Directory.

Asignación de opciones de directiva:

* Deshabilitado (0) = deshabilitado

* SignInAndMakeDomainAccountNonRemovable (1) = iniciar sesión y convertir la cuenta de dominio en no extraíble

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ConfigureOnPremisesAccountAutoSignIn
  - Nombre de GP: configurar el inicio de sesión automático con una cuenta de dominio de Active Directory cuando no tenga una cuenta de dominio de Azure AD
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ConfigureOnPremisesAccountAutoSignIn
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### ConfigureOnlineTextToSpeech

  #### Configurar Texto a voz en línea

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configure si el explorador puede usar el texto en línea para la característica fuentes de voz, como parte de los servicios de Azure Cognitive. Estas fuentes de voz son de mayor calidad que las preinstaladas en el sistema.

Si habilita o no configura esta directiva, las aplicaciones basadas en web que usan la API SpeechSynthesis podrán usar texto en línea para la característica fuentes de voz.

Si deshabilita esta directiva, la característica fuentes de voz no estará disponible.

Obtenga más información sobre esta característica aquí: API SpeechSynthesis: [ https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038) servicios cognitivos: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ConfigureOnlineTextToSpeech
  - Nombre de GP: configurar el texto a voz en línea
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ConfigureOnlineTextToSpeech
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ConfigureOnlineTextToSpeech
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ConfigureShare

  #### Configurar Compartir experiencia

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 83 o posterior

  #### Descripción

  Si establece esta directiva en "ShareAllowed" (el valor predeterminado), los usuarios podrán acceder a la experiencia de Uso compartido de Windows 10 desde el Menú Configuración y Más en Microsoft Edge para compartir con otras aplicaciones del sistema.

Si establece esta directiva en "ShareDisallowed", los usuarios no podrán acceder a la experiencia de Uso compartido de Windows 10. Si el botón compartir se encuentra en la barra de herramientas, también estará oculto.

Asignación de opciones de directiva:

* ShareAllowed (0) = permitir el acceso a la experiencia de Uso compartido

* ShareDisallowed (1) = no permitir el acceso a la experiencia de Uso compartido

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ConfigureShare
  - Nombre de GP: configurar la experiencia de uso compartido
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ConfigureShare
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### CustomHelpLink

  #### Especificar el vínculo de ayuda personalizada

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 79 o posterior

  #### Descripción

  Especifique un vínculo para el menú de ayuda o la tecla F1.

Si habilita esta directiva, un administrador podrá especificar un vínculo para el menú de ayuda o la tecla F1.

Si deshabilita o no configura esta directiva, se usará el enlace predeterminado para el menú de ayuda o la tecla F1.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: CustomHelpLink
  - Nombre de GP: especificar el vínculo de ayuda personalizada
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: CustomHelpLink
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: CustomHelpLink
  - Valor de ejemplo:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DNSInterceptionChecksEnabled

  #### Comprobaciones de interceptación de DNS habilitadas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Esta directiva configura un conmutador local que puede usarse para deshabilitar las comprobaciones de interceptación de DNS. Estas comprobaciones intentan detectar si el explorador se encuentra detrás de un proxy que redirige nombres de host desconocidos.

Es posible que esta detección no sea necesaria para un entorno empresarial en el que se conozca la configuración de la red. Se puede deshabilitar para evitar el tráfico adicional de DNS y HTTP durante el inicio y en cada uno de los cambios de configuración DNS.

Si habilita o no establece esta directiva, se realizarán las comprobaciones de interceptación de DNS.

Si deshabilita esta directiva, no se llevarán a cabo las comprobaciones de interceptación de DNS.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DNSInterceptionChecksEnabled
  - Nombre de GP: comprobaciones de interceptación de DNS habilitadas
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DNSInterceptionChecksEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DNSInterceptionChecksEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultBrowserSettingEnabled

  #### Establecer Microsoft Edge como explorador predeterminado

  
  
  #### Versiones compatibles:

  - En Windows 7 y macOS desde la versión 77 o posterior

  #### Descripción

  Si establece esta directiva en "true", Microsoft Edge siempre comprueba si es el navegador predeterminado en el inicio y, si es posible, se registra automáticamente.

Si establece esta directiva en false, Microsoft Edge deja de comprobar si es el valor predeterminado y desactiva los controles de usuario para esta opción.

Si no define esta Directiva, Microsoft Edge permite a los usuarios controlar si son las predeterminadas y, en caso contrario, si las notificaciones de usuario deben aparecer.

Nota para los administradores de Windows: esta directiva solo funciona en los ordenadores que ejecuten Windows 7. Para las versiones posteriores de Windows, hay que implementar un archivo de "asociaciones de aplicación predeterminadas" que hace de Microsoft Edge el controlador de los protocolos https y http (y, opcionalmente, del protocolo ftp y formatos de archivo como .html, .htm, .pdf, .svg, .webp). Vea [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932) para obtener más información.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultBrowserSettingEnabled
  - Nombre de GP: establecer Microsoft Edge como explorador predeterminado
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultBrowserSettingEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultBrowserSettingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSearchProviderContextMenuAccessAllowed

  #### Permitir el acceso de búsqueda al menú contextual del proveedor de búsquedas predeterminado

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 85 o posterior

  #### Descripción

  Permite el uso de un proveedor de búsquedas predeterminado en el menú contextual.

Si establece esta directiva en deshabilitado, el elemento de menú contextual de búsqueda, que depende del proveedor de búsquedas predeterminado y la búsqueda en la barra lateral, no estará disponible.

Si establece esta directiva en habilitada o no la establece, el elemento de menú contextual para el proveedor de búsquedas predeterminado y la búsqueda en la barra lateral estará disponible.

El valor de la directiva solo se aplica cuando la directiva [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) está habilitada, y no se aplica en caso contrario.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSearchProviderContextMenuAccessAllowed
  - Nombre de GP: permitir el acceso de búsqueda al menú contextual del proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DefaultSearchProviderContextMenuAccessAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSearchProviderContextMenuAccessAllowed
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSensorsSetting

  #### Configuración predeterminada de sensores

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Establecer si los sitios web pueden acceder y usar sensores, tales como sensores de luz y de movimiento. Puede bloquear o permitir por completo el acceso de los sitios web a los sensores.

Establecer la directiva en 1 permite a los sitios web tener acceso a sensores y usarlos. Establecer la directiva en 2 impide a los sitios web tener acceso a sensores.

Puede reemplazar esta directiva para patrones determinados de dirección URL mediante las directivas [SensorsAllowedForUrls](#sensorsallowedforurls) y [SensorsBlockedForUrls](#sensorsblockedforurls).

Si no configura esta directiva, los sitios web podrán tener acceso a sensores y usarlos, y el usuario podrá cambiar esta configuración. Este es el valor predeterminado global para [SensorsAllowedForUrls](#sensorsallowedforurls) y [SensorsBlockedForUrls](#sensorsblockedforurls).

Asignación de opciones de directiva:

* AllowSensors (1) = Permitir a los sitios acceder a los sensores

* BlockSensors (2) = No permitir a ningún sitio acceder a los sensores

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSensorsSetting
  - Nombre de GP: Configuración predeterminada de sensores
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre de valor: DefaultSensorsSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSensorsSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DefaultSerialGuardSetting

  #### Controlar el uso de la API de serie

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Establecer si los sitios web pueden acceder a los puertos serie. Puede bloquear completamente el acceso o preguntar al usuario cada vez que un sitio web quiera acceder a un puerto serie.

Establecer la directiva en 3 permite a los sitios web solicitar acceso a los puertos serie. Establecer la directiva en 2 impide a los sitios web tener acceso a puertos serie.

Puede reemplazar esta directiva para patrones determinados de dirección URL utilizando las directivas [SerialAskForUrls](#serialaskforurls) y [SerialBlockedForUrls](#serialblockedforurls)

Si no configura esta directiva, de manera predeterminada, los sitios web podrán preguntar a los usuarios si pueden acceder a un puerto serie, y los usuarios pueden cambiar esta configuración.

Asignación de opciones de directiva:

* BlockSerial (2) = No permitir a un sitio solicitar acceso a puertos serie mediante la API de serie

* AskSerial (3) = Permitir a los sitios solicitar permisos de usuario para tener acceso a un puerto serie

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DefaultSerialGuardSetting
  - Nombre de GP: Controlar el uso de la API de serie
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre de valor: DefaultSerialGuardSetting
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DefaultSerialGuardSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DelayNavigationsForInitialSiteListDownload

  #### Requerir que la lista de sitios modo empresarial esté disponible antes que la navegación por la tabulación

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 84 o posterior

  #### Descripción

  Le permite especificar si las pestañas de Microsoft Edge esperan para navegar hasta que el explorador ha descargado la lista de sitios de modo empresarial inicial. Esta configuración está pensada para el escenario en el que la Página principal del explorador se debe cargar en el modo de Internet Explorer y es importante que se realice en la primera ejecución del explorador después de habilitar el modo IE. Si este escenario no existe, le recomendamos que no habilite esta opción, ya que puede afectar negativamente al rendimiento de carga de la Página principal. La configuración solo se aplica cuando Microsoft Edge no tiene una lista de sitios en el modo de empresa en caché, como en ejecutar por primera vez el explorador después de habilitar el modo IE.

Esta configuración funciona conjuntamente con: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) establecida en "IEMode" y la directiva [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) donde la lista tiene al menos una entrada.

El comportamiento del tiempo de espera de esta Directiva se puede configurar con la Directiva [NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout).

Si establece esta directiva en "Todos", cuando Microsoft Edge no tenga una versión en caché de la lista de sitios del modo de empresa, las pestañas retrasarán la navegación hasta que el explorador descargue la lista de sitios. Los sitios configurados para abrirse en modo de Internet Explorer por la lista de sitios se cargarán en el modo de Internet Explorer, incluso durante la navegación inicial del explorador. Los sitios que no pueden configurarse para abrirse en Internet Explorer, como cualquier sitio con un esquema distinto de http:, https:, archivo: o FTP: no retrasa la navegación y carga inmediatamente en el modo de borde.

Si establece esta directiva en "Ninguno" o no la configura, cuando Microsoft Edge no tenga una versión en caché de la lista de sitios del modo de empresa, las pestañas se navegarán inmediatamente y no esperarán a que el explorador descargue Enterprise Mode Site List. Los sitios configurados para abrirse en el modo de Internet Explorer por la lista de sitios se abrirán en el modo de Microsoft Edge hasta que el explorador termine de descargar la lista de sitios de modo empresarial.

Asignación de opciones de directiva:

* None (0) = ninguno

* All (1) = Todas las navegaciones aptas

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DelayNavigationsForInitialSiteListDownload
  - Nombre de la Directiva de Grupo: necesita que la lista de sitios modo empresarial esté disponible antes que la navegación por la tabulación
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DelayNavigationsForInitialSiteListDownload
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### DeleteDataOnMigration

  #### Eliminar datos antiguos del explorador en la migración.

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 83 o posterior

  #### Descripción

  Esta directiva determina si se eliminarán los datos de navegación del usuario de Microsoft Edge (versión anterior) después de migrar a la versión 81 o posterior de Microsoft Edge.

Si establece esta directiva como "habilitada", todos los datos de navegación de Microsoft Edge (versión anterior) después de migrar a la versión 81 de Microsoft Edge o posterior serán eliminados. Esta política debe establecerse antes de migrar a la versión 81 o posterior de Microsoft Edge para que tenga algún efecto en los datos de exploración existentes.

Si establece esta directiva como "deshabilitada", o si no está configurada, los datos de navegación del usuario no se eliminarán después de migrar a la versión 83 o posterior de Microsoft Edge.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DeleteDataOnMigration
  - Nombre de GP: eliminar los datos antiguos del explorador durante la migración
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DeleteDataOnMigration
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### DeveloperToolsAvailability

  #### Controlar dónde se pueden usar las herramientas de desarrollo

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Controla dónde se pueden usar las herramientas de desarrollo.

Si establece esta directiva en "DeveloperToolsDisallowedForForceInstalledExtensions" (el valor predeterminado), los usuarios podrán acceder a las herramientas de desarrollo y a la consola de JavaScript en general, pero no en el contexto de las extensiones instaladas por la directiva empresarial.

Si establece esta directiva en "DeveloperToolsAllowed" (el valor predeterminado), los usuarios podrán acceder a las herramientas de desarrollo y a la consola de JavaScript en todos los contextos, incluyendo el contexto de las extensiones instaladas por la directiva empresarial.

Si establece esta directiva en "DeveloperToolsDisallowed", los usuarios no podrán acceder a las herramientas de desarrollo o inspeccionar los elementos del sitio web. Se deshabilitarán los métodos abreviados de teclado y las entradas de los menús contextuales y del menú que abren las herramientas para desarrolladores o la consola JavaScript.

Asignación de opciones de directiva:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = bloquear las herramientas para desarrolladores en extensiones instaladas por la directiva empresarial, y permitirlas en otros contextos

* DeveloperToolsAllowed (1) = permitir el uso de las herramientas de desarrollo

* DeveloperToolsDisallowed (2) = no permitir el uso de las herramientas de desarrollo

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DeveloperToolsAvailability
  - Nombre de GP: controlar dónde se pueden usar las herramientas de desarrollo
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DeveloperToolsAvailability
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DeveloperToolsAvailability
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DiagnosticData

  #### Enviar datos de diagnóstico necesarios y opcionales sobre el uso del explorador

  
  
  #### Versiones compatibles:

  - En Windows 7 y macOS desde la versión 86 o posterior

  #### Descripción

  Esta directiva controla el envío a Microsoft de datos de diagnóstico necesarios y opcionales sobre el uso del explorador.

Los datos de diagnóstico se recopilan para proteger, actualizar y mejorar el rendimiento de Microsoft Edge.

Algunos de los datos de diagnóstico opcionales están relacionados con el uso del explorador, los sitios web que visita y los informes de bloqueos, que ayudan a Microsoft a mejorar el producto y el servicio.

Esta Directiva no es compatible con dispositivos Windows 10. Para controlar esta colección de datos en Windows 10, los administradores de TI tienen que usar la directiva de grupo de datos de diagnóstico de Windows. Esta directiva será "Permitir telemetría" o "Permitir datos de diagnóstico", en función de la versión de Windows. Más información sobre la colección de datos de diagnóstico de Windows 10: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Use una de las opciones siguientes para configurar esta directiva:

"Desactivado" desactiva la recopilación de datos de diagnóstico necesarios y opcionales. No se recomienda esta opción.

"RequiredData" envía los datos de diagnóstico necesarios y desactiva la recopilación de datos de diagnóstico opcionales. Microsoft Edge enviará los datos de diagnóstico necesarios para que Microsoft Edge esté protegido y actualizado, y para que funcione como se espera de él.

"OptionalData" envía datos de diagnóstico opcionales y contiene datos sobre el uso del explorador, los sitios web que se visitan y los informes de bloqueos enviados a Microsoft para mejorar el producto y el servicio.

En Windows 7 y macOS, esta directiva controla el envío de datos necesarios y opcionales a Microsoft.

Si no configura esta directiva o la deshabilita, Microsoft Edge se ajustará de forma predeterminada a las preferencias del usuario.

Asignación de opciones de directiva:

* Desactivado (0) = desactivado (no recomendado)

* RequiredData (1) = datos necesarios

* OptionalData (2) = datos opcionales

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DiagnosticData
  - Nombre GP: enviar datos de diagnóstico necesarios y opcionales sobre el uso del explorador
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre de valor: DiagnosticData
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: DiagnosticData
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DirectInvokeEnabled

  #### Permitir que los usuarios abran archivos mediante el protocolo DirectInvoke

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 78 o posterior

  #### Descripción

  Permitir que los usuarios abran archivos mediante el protocolo DirectInvoke. El protocolo ClickOnce permite que los sitios web soliciten que el explorador abra los archivos desde una dirección URL determinada mediante un controlador de archivos específico en el equipo o dispositivo del usuario.

Si habilita esta directiva, los usuarios podrán abrir archivos mediante el protocolo DirectInvoke.

Si deshabilita esta directiva, los usuarios no podrán abrir archivos mediante el protocolo DirectInvoke. En su lugar, el archivo se guardará en el sistema de archivos.

Nota: si deshabilita DirectInvoke, es posible que algunas características de Microsoft SharePoint Online no funcionen correctamente.

Para obtener más información acerca de DirectInvoke, vea [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) y [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DirectInvokeEnabled
  - Nombre de GP: permitir que los usuarios abran los archivos mediante el protocolo DirectInvoke
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DirectInvokeEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### Disable3DAPIs

  #### Deshabilitar la compatibilidad para las API gráficas 3D

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Evita que las páginas web puedan acceder a la unidad de procesamiento de gráficos (GPU). Específicamente, las páginas web no pueden acceder a la API de WebGL y los complementos no pueden usar la API de Pepper 3D.

Si no configura o deshabilita esta directiva, las páginas web podrán usar la API de WebGL y los complementos para usar la API de Pepper 3D. De forma predeterminada, Microsoft Edge necesita aún requiere de los argumentos de la línea de comandos para poder usar estas API.

Si establece la directiva [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) como falsa, la configuración de la directiva "Disable3DAPIs" se omitirá, lo que equivaldría a establecer la directiva "Disable3DAPIs" como verdadera.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: Disable3DAPIs
  - Nombre de GP: deshabilitar la compatibilidad con las API de gráficos 3D
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: Disable3DAPIs
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: Disable3DAPIs
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DisableScreenshots

  #### Deshabilitar las capturas de pantalla

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Controla si los usuarios pueden tomar capturas de pantalla de la página del explorador.

Si esta opción está habilitada, el usuario no podrá realizar capturas de pantalla con métodos abreviados de teclado o las API de extensión.

Si esta directiva está deshabilitada o no es configurada, los usuarios podrán hacer capturas de pantalla.

Tenga en cuenta que esta directiva controla las capturas de pantalla tomadas desde el propio explorador. Aunque habilite esta directiva, los usuarios podrán seguir realizando capturas de pantalla mediante algún método ajeno al explorador (como usar una característica del sistema operativo u otra aplicación).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DisableScreenshots
  - Nombre de GP: deshabilitar las capturas de pantalla
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DisableScreenshots
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DisableScreenshots
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DiskCacheDir

  #### Establecer directorio de caché de disco

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura el directorio que se usará para almacenar los archivos en caché.

Si habilita esta directiva, Microsoft Edge usará el directorio proporcionado independientemente de si el usuario ha especificado el marcador "--disk-cache-dir". Para evitar la pérdida de datos u otros errores inesperados, no configure esta directiva en un directorio raíz de volumen o en un directorio que se use para otros propósitos, ya que Microsoft Edge administra su contenido.

Vea [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obtener una lista de variables que puede usar para especificar directorios y rutas de acceso.

Si no configura esta directiva, se usará el directorio de caché predeterminado, y los usuarios podrán anularlo con el marcador de la línea de comandos "--disk-cache-dir".

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DiskCacheDir
  - Nombre de GP: establecer directorio de caché de disco
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DiskCacheDir
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"${user_home}/Edge_cache"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DiskCacheDir
  - Valor de ejemplo:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DiskCacheSize

  #### Configurar el tamaño de la caché de disco, en bytes

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configure el tamaño de la caché, en bytes, que se usa para almacenar archivos en el disco.

Si habilita esta directiva, Microsoft Edge usa el tamaño de caché proporcionado, independientemente de si el usuario ha especificado el marcador "--cache-tamaño". El valor especificado en esta Directiva no es un límite duro, sino una sugerencia al sistema de almacenamiento en caché. cualquier valor por debajo de unos pocos megabytes es demasiado pequeño y se redondeará hacia arriba a un mínimo razonable.

Si establece el valor de esta directiva en 0, se usará el tamaño de caché predeterminado y los usuarios no podrán cambiarlo.

Si no configura esta Directiva, se usará el tamaño predeterminado, pero los usuarios podrán anularla con el marcador "--almacenamiento de caché en disco".

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DiskCacheSize
  - Nombre de GP: configurar el tamaño de la caché de disco en bytes
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DiskCacheSize
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x06400000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DiskCacheSize
  - Valor de ejemplo:
``` xml
<integer>104857600</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DnsOverHttpsMode

  #### Controlar el modo de DNS a través de HTTPS.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 83 o posterior

  #### Descripción

  Controla el modo de DNS a través de HTTPS Tenga en cuenta que esta directiva solo establecerá el modo predeterminado en cada consulta. Este modo puede ser anulado en tipos especiales de consultas, como las solicitudes para solucionar el nombre de host de un servidor de DNS a través de HTTPS.

El modo "desactivado" deshabilita los DNS a través de HTTPS.

El modo "automático" enviará primero las consultas DNS a través de HTTPS si se encuentra disponible un servidor DNS a través de HTTPS y puede reservar el envío de consultas poco seguras por error.

El modo "seguro" solo enviará consultas de DNS a través de HTTPS y no podrá solucionar el error.

Si no configura esta directiva, es posible que el explorador envíe solicitudes DNS sobre HTTPS a un solucionador que esté asociado con la solución del sistema configurado por el usuario.

Asignación de opciones de directiva:

* off (deshabilitado) = deshabilitar DNS sobre HTTPS

* automatic (automático) = habilitar DNS a través de HTTPS con reserva no segura

* secure (seguro) = habilitar DNS a través de HTTPS sin reserva no segura

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DnsOverHttpsMode
  - Nombre de GP: controlar el modo de DNS a través de HTTPS
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DnsOverHttpsMode
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"off"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DnsOverHttpsMode
  - Valor de ejemplo:
``` xml
<string>off</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DnsOverHttpsTemplates

  #### Especificar la plantilla de URI de la resolución de DNS a través de HTTPS deseada

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 83 o posterior

  #### Descripción

  La plantilla de URI del solucionador de DNS a través de HTTPS deseada. Para especificar varias soluciones DNS a través de HTTPS, separe las plantillas URI correspondientes con espacios.

Si establece [DnsOverHttpsMode](#dnsoverhttpsmode) como "seguro", entonces esta directiva deberá ser establecida y no podrá dejarse vacía.

Si establece [DnsOverHttpsMode](#dnsoverhttpsmode) en "automático" y esta directiva está establecida, entonces se usarán las plantillas URI especificadas. Si no establece esta directiva, se usarán las asignaciones codificadas para intentar actualizar el solucionador de DNS actual del usuario a un solucionador de DoH operado por el mismo proveedor.

Si la plantilla URI contiene una variable DNS, las solicitudes al solucionador usarán GET; en caso contrario, las solicitudes usarán POST.

Las plantillas con un formato incorrecto serán omitidas.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DnsOverHttpsTemplates
  - Nombre de GP: especificar la plantilla URI de la resolución deseada de DNS a través de HTTPS
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: DnsOverHttpsTemplates
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://dns.example.net/dns-query{?dns}"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DnsOverHttpsTemplates
  - Valor de ejemplo:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DownloadDirectory

  #### Establecer directorio de descarga

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura el directorio que se usará al descargar archivos.

Si habilita esta directiva, Microsoft Edge usará el directorio proporcionado independientemente de si el usuario ha especificado uno o ha elegido que se le solicite la ubicación cada vez que realice una descarga. Vea [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obtener una lista de las variables que se pueden usar.

Si deshabilita o no configura esta directiva, se usará el directorio de descargas predeterminado y éste podría ser cambiado por el usuario.

Si establece una ruta de acceso no válida, Microsoft Edge usará de forma predeterminada el directorio de descargas predeterminado del usuario.

Si no existe la carpeta especificada por la ruta de acceso, la descarga activará un mensaje de solicitud que preguntará al usuario dónde quiere guardar su descarga.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DownloadDirectory
  - Nombre de GP: establecer el directorio de descarga
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: DownloadDirectory
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DownloadDirectory
  - Valor de ejemplo:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### DownloadRestrictions

  #### Permitir las restricciones de descarga

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura el tipo de descargas que Microsoft Edge bloquea completamente, sin dejar que los usuarios anulen la decisión de seguridad.

Establezca "BlockDangerousDownloads" para permitir todas las descargas excepto aquellas que llevan advertencias de SmartScreen de Microsoft Defender.

Establezca "BlockPotentiallyDangerousDownloads" para permitir todas las descargas excepto aquellas que llevan advertencias de SmartScreen de Microsoft Defender sobre descargas potencialmente peligrosas o no deseadas.

Establezca "BlockAllDownloads" para bloquear todas las descargas.

Si no configura esta directiva o establece la opción "DefaultDownloadSecurity", se aplicarán a las descargas las restricciones de seguridad habituales, basándose en los resultados del análisis de SmartScreen de Microsoft Defender.

Tenga en cuenta que estas restricciones se aplican a las descargas desde el contenido de la página web, así como el "vínculo de descarga..." en la opción del menú contextual. Estas restricciones no se aplican a la hora de guardar o descargar la página que se muestra en ese momento, ni tampoco se aplican a la opción Guardar como PDF de las opciones de impresión.

Vea [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934) para obtener más información sobre SmartScreen de Microsoft Defender.

Asignación de opciones de directiva:

* DefaultDownloadSecurity (0) = ninguna restricción especial

* BlockDangerousDownloads (1) = bloquear descargas peligrosas

* BlockPotentiallyDangerousDownloads (2) = bloquear descargas potencialmente peligrosas o no deseadas

* BlockAllDownloads (3) = bloquear todas las descargas

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: DownloadRestrictions
  - Nombre de GP: permitir las restricciones de descarga
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: DownloadRestrictions
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: DownloadRestrictions
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### EdgeCollectionsEnabled

  #### Habilitar la característica colecciones

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Permite que los usuarios accedan a la característica de colecciones, donde pueden recopilar, organizar, compartir y exportar contenido de forma más eficaz y con la integración de Office.

Si habilita o no configura esta directiva, los usuarios podrán obtener acceso y usar la característica de colecciones de Microsoft Edge.

Si deshabilita esta directiva, los usuarios no podrán acceder ni usar las colecciones de Microsoft Edge.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EdgeCollectionsEnabled
  - Nombre de GP: habilitar la característica de colecciones
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: EdgeCollectionsEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: EdgeCollectionsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### EdgeShoppingAssistantEnabled

  #### Comprar en Microsoft Edge activado

  
  
  #### Versiones compatibles:

  - On Windows and macOS since 87 or later

  #### Descripción

  Esta directiva permite a los usuarios comparar los precios de un producto que estén buscando, obtener cupones en el sitio web en el que se encuentren y aplicar cupones automáticamente durante la compra.

Si habilita o no configura esta Directiva, las características de compra, como la comparación de precios y los cupones, se aplicarán automáticamente para los dominios comerciales. Los cupones para el minorista actual y los precios de otros minoristas se obtendrán de un servidor.

Si deshabilita esta Directiva, las características de compra, como la comparación de precios y los cupones, no se encontrarán automáticamente para los dominios comerciales.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EdgeShoppingAssistantEnabled
  - Nombre GP: Compra en Microsoft Edge activada
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: EdgeShoppingAssistantEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```

  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: EdgeShoppingAssistantEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### EditFavoritesEnabled

  #### Permitir que los usuarios editen los favoritos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilite esta directiva para permitir que los usuarios puedan agregar, quitar o modificar los favoritos. Si no se configura esta directiva, este será el comportamiento por defecto.

Deshabilite esta directiva para evitar que los usuarios puedan agregar, quitar o modificar los favoritos. Aún podrán usar los favoritos existentes.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EditFavoritesEnabled
  - Nombre de GP: permitir que los usuarios editen los favoritos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: EditFavoritesEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: EditFavoritesEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### EnableDeprecatedWebPlatformFeatures

  #### Re-enable deprecated web platform features for a limited time (obsolete)

  
  >OBSOLETE: This policy is obsolete and doesn't work after Microsoft Edge 86.
  #### Versiones compatibles:
            

  - On Windows and macOS since 77, until 86

  #### Descripción

  This policy is obsolete because dedicated web platform policies are now used to manage individual web platform feature deprecations.

Especifica una lista de características obsoletas de la plataforma web para volver a habilitar temporalmente.

Esta directiva le permite volver a habilitar las características en desuso de la plataforma web durante un período de tiempo limitado. Las características se identifican con una etiqueta de cadena.

Si no configura esta política, si la lista está vacía o si una característica no coincide con una de las etiquetas de cadena admitidas, todas las características en desuso de la plataforma web permanecerán deshabilitadas.

Aunque la directiva en sí es compatible con las plataformas anteriores, es posible que la característica que habilita no esté disponible en todas las plataformas. No todas las características en desuso de plataforma web pueden volver a habilitarse Solo se pueden volver a habilitar las que se enumeran explícitamente a continuación, y solo por un período de tiempo limitado, que puede ser distinto para cada característica. Puede revisar el propósito detrás de los cambios realizados en la característica de la plataforma web en https://bit.ly/blinkintents.

El formato general de la etiqueta de la cadena es [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd].

Asignación de opciones de directiva:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = Habilitar la API de ExampleDeprecatedFeature mediante 2008/09/02

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EnableDeprecatedWebPlatformFeatures
  - GP name: Re-enable deprecated web platform features for a limited time (obsolete)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: EnableDeprecatedWebPlatformFeatures
  - Valor de ejemplo:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### EnableDomainActionsDownload

  #### Habilitar la descarga de acciones de dominio de Microsoft (obsoleto)

  
  >OBSOLETA: Esta directiva está obsoleta y no funciona después de Microsoft Edge 84.
  #### Versiones compatibles:

  - En Windows y MacOS desde el 77 hasta el 84

  #### Descripción

  Esta Directiva no funciona porque deben evitarse Estados en conflicto. Aunque esta directiva se usa para habilitar o deshabilitar la descarga de la lista de acciones del dominio, no siempre alcanza el estado deseado. El servicio de experimentación y configuración, que controla la descarga, tiene su propia directiva de grupo para configurar las descargas realizadas desde el servicio. En su lugar, use la directiva [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)

En Microsoft Edge, las acciones de dominio representan una serie de características de compatibilidad que ayudan al explorador a funcionar correctamente a través de la web.

Por motivos de compatibilidad, Microsoft mantiene una lista de acciones que se deben llevar en a cabo en ciertos dominios. Por ejemplo, es posible que el explorador invalide la cadena de agente de usuario en un sitio web cuando se rompe el sitio, debido a la nueva cadena agente de usuario en Microsoft Edge. Todas estas acciones están pensadas para ser temporales mientras Microsoft intenta resolver el problema con el propietario del sitio.

Al iniciar el explorador y, después, el explorador se pondrá en contacto de forma periódica con el servicio de experimentación y configuración que contenga la lista más actualizada de las acciones de compatibilidad que se deben realizar. Esta lista se guarda de forma local después de ser recuperada por primera vez para que las siguientes solicitudes solo actualicen la lista si la copia del servidor ha cambiado.

Si habilita esta directiva, la lista de acciones del dominio se seguirá descargando desde el servicio de experimentación y configuración.

Si deshabilita esta directiva, la lista de acciones del dominio no se seguirá descargando desde el servicio de experimentación y configuración.

Si no configura esta directiva, la lista de acciones del dominio se seguirá descargando desde el servicio de experimentación y configuración.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EnableDomainActionsDownload
  - Nombre de GP: habilitar la descarga de acciones de dominio de Microsoft (en desuso)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: EnableDomainActionsDownload
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: EnableDomainActionsDownload
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### EnableOnlineRevocationChecks

  #### Habilitar las comprobaciones de OCSP/CRL en línea

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Las comprobaciones de la revocación en línea no proporcionan una ventaja de seguridad considerable y están deshabilitadas de forma predeterminada.

Si habilita esta directiva, Microsoft Edge realizará comprobaciones OCSP/CRL en línea de errores recuperables. "Error recuperable" significa que si no se puede tener acceso al servidor de revocación, el certificado se considerará válido.

Si deshabilita la directiva o no la configura, Microsoft Edge no realizará comprobaciones de la revocación en línea.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EnableOnlineRevocationChecks
  - Nombre de GP: habilitar las comprobaciones de OCSP/CRL en línea
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: EnableOnlineRevocationChecks
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: EnableOnlineRevocationChecks
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### EnableSha1ForLocalAnchors

  #### Permitir certificados firmados mediante SHA-1 cuando sean emitidos por anclajes de veracidad locales (en desuso).

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 85 o posterior

  #### Descripción

  Cuando esta configuración está habilitada, Microsoft Edge permite conexiones protegidas por certificados firmados con SHA-1 siempre y cuando el certificado se encadene a un certificado raíz instalado de forma local y, por lo tanto, sea válido.

Tenga en cuenta que esta directiva depende de la pila de comprobación de certificados del sistema operativo (SO) que permite firmas SHA-1. Si una actualización del sistema operativo cambia el tratamiento de éste para los certificados SHA-1, puede que esta directiva ya no tenga efecto.  Además, esta directiva está pensada como una solución temporal para dar más tiempo a las empresas para dejar de usar SHA-1. Esta directiva se eliminará en Microsoft Edge 92, cuyo lanzamiento será a mediados de 2021.

Si no establece esta directiva o la establece en falso, o si el certificado SHA-1 se encadena a una raíz de certificado de confianza pública, Microsoft Edge no permitirá certificados firmados por SHA-1.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EnableSha1ForLocalAnchors
  - Nombre de GP: permitir certificados firmados mediante SHA-1 cuando sean emitidos por anclajes de veracidad locales (en desuso).
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: EnableSha1ForLocalAnchors
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: EnableSha1ForLocalAnchors
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### EnterpriseHardwarePlatformAPIEnabled

  #### Permitir que las extensiones administradas utilicen la API de la plataforma de hardware empresarial

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Cuando esta directiva se establece como habilitada, las extensiones instaladas por la directiva de empresa pueden usar la API de la plataforma del hardware de empresa.
Cuando esta directiva se establece como deshabilitada o no establecida, las extensiones instaladas por la directiva de empresa no pueden usar la API de la plataforma del hardware de empresa.
Esta directiva también se aplica a las extensiones de los componentes.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EnterpriseHardwarePlatformAPIEnabled
  - Nombre de GP: permitir que las extensiones administradas utilicen la API de la plataforma de hardware empresarial
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: EnterpriseHardwarePlatformAPIEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: EnterpriseHardwarePlatformAPIEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### EnterpriseModeSiteListManagerAllowed

  #### Permitir el acceso a la herramienta Enterprise Mode Site List Manager

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 86 o posterior

  #### Descripción

  Permite establecer si Enterprise Mode Site List Manager está disponible para los usuarios.

Si habilita esta directiva, los usuarios pueden ver el botón de navegación de Enterprise Mode Site List Manager en la página edge://compat, ir a la herramienta y usarla.

Si deshabilita o no configura esta directiva, los usuarios no verán el botón de navegación de Enterprise Mode Site List Manager y no podrán usar la herramienta.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: EnterpriseModeSiteListManagerAllowed
  - Nombre de GP: permitir el acceso a la herramienta Enterprise Mode Site List Manager
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: EnterpriseModeSiteListManagerAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings

  #### Deshabilitar el tipo de archivo de descarga advertencias basadas en la extensión para tipos de archivo especificados en dominios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 85 o posterior

  #### Descripción

  Puede habilitar esta directiva para crear un diccionario de extensiones de tipo de archivo con una lista de dominios correspondiente que se excluirá de las advertencias de descarga basada en la extensión de tipo de archivo. Esto permite a los administradores de la empresa bloquear las advertencias de descarga basada en la extensión de tipo de archivo para los archivos que están asociados a un dominio de la lista. Por ejemplo, si la extensión "JNLP" está asociada a "website1.com", los usuarios no verán ninguna advertencia al descargar los archivos "JNLP" de "website1.com", pero verán una advertencia de descarga al descargar archivos "JNLP" de "website2.com".

Los archivos con las extensiones de tipo de archivo especificados para los dominios identificados por esta directiva seguirán sujetos a advertencias de seguridad basadas en la extensión que no sean de tipo de archivo, como advertencias de descarga de contenido mixto y advertencias de SmartScreen de Microsoft defender.

Si deshabilita esta Directiva o no la configura, los tipos de archivo que desencadenen advertencias de descarga basadas en extensión mostrarán advertencias al usuario.

Si habilita esta directiva:

* El patrón de dirección URL debe tener un formato acorde con [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).
* La extensión de tipo de archivo escrita tiene que ser ASCII en minúsculas. El separador inicial no se debe incluir cuando se indica la extensión de tipo de archivo, por lo que se debe usar "jnlp" en lugar de ".jnlp".

Por ejemplo:

El siguiente valor de ejemplo impide las advertencias de descarga basada en la extensión de tipo de archivo que se basan en extensiones SWF, exe y JNLP para los dominios *. contoso.com. Se mostrará al usuario una advertencia de descarga basada en la extensión de un tipo de archivo en cualquier otro dominio para los archivos exe y JNLP, pero no para los archivos SWF.

[{"file_extension": "JNLP", "Domains": ["contoso.com"]}, {"file_extension": "exe", "Domains": ["contoso.com"]}, {"file_extension": "SWF", "Domains": ["*"]}]

Tenga en cuenta que, mientras que en el ejemplo anterior se muestra una advertencia de descarga basada en la extensión de tipo de archivo para los archivos "SWF" para todos los dominios, no se recomienda la eliminación de estas advertencias para todos los dominios por cualquier extensión peligrosa, por motivos de seguridad. Solo se muestra en el ejemplo para mostrar la posibilidad de hacerlo.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Nombre de GP: deshabilitar el tipo de archivo de descarga advertencias basadas en extensión para tipos de archivo especificados en dominios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Valor de ejemplo:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ExperimentationAndConfigurationServiceControl

  #### Controlar la comunicación con el servicio de experimentación y configuración

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  En Microsoft Edge, el servicio de experimentación y configuración se usa para implementar la carga de experimentación y configuración.

La carga útil de experimentación consiste en una lista de características de las primeras fases de desarrollo que Microsoft ha habilitado para realizar pruebas y obtener comentarios.

La carga útil de la configuración consiste en una lista de configuraciones que Microsoft quiere implementar en Microsoft Edge para optimizar la experiencia del usuario. Por ejemplo, la carga útil de la configuración puede especificar la frecuencia con la que Microsoft Edge envía solicitudes al servicio de experimentación y configuración para recuperar la carga útil más reciente.

Adicionalmente, la carga útil de la configuración también puede contener una lista de acciones que se deben llevar a cabo en determinados dominios por motivos de compatibilidad. Por ejemplo, es posible que el explorador invalide la cadena de agente de usuario en un sitio web cuando se rompe el sitio, debido a la nueva cadena agente de usuario en Microsoft Edge. Todas estas acciones están pensadas para ser temporales mientras Microsoft intenta resolver el problema con el propietario del sitio.

Si establece esta directiva en "FullMode", se descargará la carga útil completa del Servicio de experimentación y configuración. Esto incluye las cargas útiles de experimentación y configuración.

Si establece esta directiva en "ConfigurationsOnlyMode", solo se entregará la carga útil de la configuración.

Si establece esta directiva en "RestrictedMode", la comunicación con el Servicio de experimentación y configuración se detendrá completamente.

Si no configura esta directiva, el comportamiento de un dispositivo administrado en los canales Estable y Beta será el mismo que cuando se usa "ConfigurationsOnlyMode".

Si no configura esta directiva, el comportamiento de un dispositivo no administrado será el mismo que cuando se usa "FullMode".

Asignación de opciones de directiva:

* FullMode (2) = recuperar configuraciones y experimentos

* ConfigurationsOnlyMode (1) = solo recuperar configuraciones

* RestrictedMode (0) = deshabilitar la comunicación con el servicio de experimentación y configuración

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ExperimentationAndConfigurationServiceControl
  - Nombre de GP: controlar la comunicación con el servicio de experimentación y configuración
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ExperimentationAndConfigurationServiceControl
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ExperimentationAndConfigurationServiceControl
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox

  #### Mostrar la casilla "abrir siempre" en el cuadro de diálogo de protocolo externo

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 79 o posterior

  #### Descripción

  Esta directiva controla si la casilla de verificación "permitir siempre que este sitio abra vínculos de este tipo" se muestra en los avisos de confirmación al iniciar el protocolo externo. Esta directiva solo se aplica a los vínculos https://.

Si se habilita esta directiva, cuando se muestre un aviso de confirmación de un protocolo externo, el usuario podrá seleccionar "Permitir siempre" para omitir todos los avisos de confirmación futuros del protocolo en este sitio.

Si desactiva esta directiva, la casilla de verificación "Permitir siempre" no se mostrará. Se solicitará confirmación al usuario cada vez que se invoque un protocolo externo.

Antes de Microsoft Edge 83, si no configura esta directiva, la casilla "Permitir siempre" no se muestra. Se solicitará confirmación al usuario cada vez que se invoque un protocolo externo.

En Microsoft Edge 83, si no configura esta directiva, la visibilidad de la casilla de verificación se controla con el indicador "Habilitar recordatorio de las preferencias de lanzamiento de protocolos" en edge://flags

A partir de Microsoft Edge 84, si no configura esta directiva, cuando se muestre un aviso de confirmación de un protocolo externo, el usuario podrá seleccionar "Permitir siempre" para omitir todos los avisos de confirmación futuros del protocolo en este sitio.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Nombre de GP: mostrar la casilla "abrir siempre" en el cuadro de diálogo de protocolo externo
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### FamilySafetySettingsEnabled

  #### Permitir que los usuarios configuren la seguridad familiar

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 83 o posterior

  #### Descripción

  Esta directiva deshabilita y oculta completamente la página de seguridad familiar en la configuración. También se bloqueará la navegación a edge://settings/familysafety. La página seguridad familiar describe las características que están disponibles para los grupos de familia y cómo unirse a un grupo de familia. Obtenga más información sobre la seguridad familiar aquí: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Si habilita o no configura esta directiva, se mostrará la página de seguridad familiar.

Si deshabilita esta directiva, no se mostrará la página de seguridad familiar.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: FamilySafetySettingsEnabled
  - Nombre de GP: permitir que los usuarios configuren la Protección infantil de Microsoft
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: FamilySafetySettingsEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: FamilySafetySettingsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### FavoritesBarEnabled

  #### Habilitar la barra de favoritos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilita o deshabilita la barra de favoritos.

Si habilita esta directiva, los usuarios verán la barra de favoritos.

Si deshabilita esta directiva, los usuarios no verán la barra de favoritos.

Si no se configura esta directiva, el usuario podrá optar por usar la barra de favoritos.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: FavoritesBarEnabled
  - Nombre de GP: habilitar la barra de favoritos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: FavoritesBarEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: FavoritesBarEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ForceBingSafeSearch

  #### Forzar la búsqueda segura de Bing

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Asegúrese de que las consultas que se realizan en la búsqueda web de Bing se hagan con la búsqueda segura establecida en el valor especificado. Los usuarios no pueden cambiar esta configuración.

Si configura esta directiva como "BingSafeSearchNoRestrictionsMode", la búsqueda segura en Bing volverá al valor de bing.com.

Si configura esta directiva como "BingSafeSearchModerateMode", se usará la configuración moderada para la búsqueda segura. La configuración moderada filtra los vídeos e imágenes para adultos, pero no el texto de los resultados en la búsqueda.

Si configura esta directiva como "BingSafeSearchStrictMode", se usará la configuración del valor estricto para la búsqueda segura. La configuración estricta filtra el texto, las imágenes y los vídeos para adultos.

Si deshabilita esta directiva o no la configura, no se aplicará la búsqueda segura en Bing y los usuarios podrán establecer el valor que deseen en bing.com.

Asignación de opciones de directiva:

* BingSafeSearchNoRestrictionsMode (0) = no configurar restricciones de búsqueda en Bing

* BingSafeSearchModerateMode (1) = configurar restricciones de búsqueda moderadas en Bing

* BingSafeSearchStrictMode (2) = configurar restricciones de búsqueda estrictas en Bing

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ForceBingSafeSearch
  - Nombre de GP: forzar la búsqueda segura de Bing
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ForceBingSafeSearch
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ForceBingSafeSearch
  - Valor de ejemplo:
``` xml
<integer>0</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ForceCertificatePromptsOnMultipleMatches

  #### Configurar si Microsoft Edge debe seleccionar automáticamente un certificado cuando haya múltiples coincidencias de certificados para un sitio configurado con "AutoSelectCertificateForUrls"

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 81 o posterior

  #### Descripción

  Se alterna la opción entre la selección de un certificado si hay varios certificados disponibles y la configuración de un sitio con [AutoSelectCertificateForUrls](#autoselectcertificateforurls). Si no se configura [AutoSelectCertificateForUrls](#autoselectcertificateforurls) en un sitio, siempre se le solicitará al usuario que seleccione un certificado.

Si establece esta directiva como verdadera, Microsoft Edge le solicitará al usuario que seleccione un certificado para los sitios de la lista definida en [AutoSelectCertificateForUrls](#autoselectcertificateforurls) si y solo si hay más de un certificado.

Si establece esta directiva como falsa o no la configura, Microsoft Edge seleccionará un certificado automáticamente, aunque hayan varias coincidencias para un certificado. No se solicitará al usuario que seleccione un certificado para los sitios de la lista definida en [AutoSelectCertificateForUrls](#autoselectcertificateforurls).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ForceCertificatePromptsOnMultipleMatches
  - Nombre de GP: configurar la selección automática de un certificado por parte de Microsoft Edge cuando haya múltiples coincidencias de certificados para un sitio configurado con "AutoSelectCertificateForUrls"
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ForceCertificatePromptsOnMultipleMatches
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ForceCertificatePromptsOnMultipleMatches
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ForceEphemeralProfiles

  #### Permitir el uso de perfiles efímeros

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Controla el cambio de los perfiles de usuario al modo efímero. Un perfil efímero se crea al iniciar una sesión, se elimina al finalizar la misma y se asocia al perfil original del usuario.

Si habilita esta directiva, los perfiles se ejecutan en modo efímero. Esto permite que los usuarios trabajen desde sus propios dispositivos sin guardar los datos de exploración en los mismos. Si habilita esta directiva como una directiva del sistema operativo (por ejemplo, al usar GPO en Windows), se aplicará a todos los perfiles del sistema.

Si deshabilita esta directiva o no la configura, los usuarios verán sus perfiles normales al iniciar sesión en el explorador.

En el modo efímero, los datos del perfil solo se guardarán en el disco mientras la sesión del usuario se mantenga activa. Las características como el historial del explorador, las extensiones, sus datos, datos Web como las cookies y las bases de datos web no se guardan después de cerrar el explorador. Esto no impedirá que los usuarios descarguen los datos manualmente en el disco, o que no puedan imprimirlos o guardar las páginas. Si el usuario ha habilitado la sincronización, todos los datos se conservarán en sus cuentas de sincronización al igual que ocurre en los perfiles normales. Los usuarios también pueden usar la exploración InPrivate en modo efímero, a menos que lo desactive explícitamente.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ForceEphemeralProfiles
  - Nombre de GP: permitir el uso de perfiles efímeros
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ForceEphemeralProfiles
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ForceEphemeralProfiles
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ForceGoogleSafeSearch

  #### Forzar la búsqueda segura de Google

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Obliga a que las consultas de la Búsqueda web de Google se realicen con la opción de búsqueda segura habilitada y evita que los usuarios cambien esta configuración.

Al habilitar esta directiva, la función de búsqueda segura siempre estará habilitada en la búsqueda de Google.

Si deshabilita esta directiva o no la configura, no se aplicará la búsqueda segura en Google.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ForceGoogleSafeSearch
  - Nombre de GP: forzar la búsqueda segura de Google
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ForceGoogleSafeSearch
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ForceGoogleSafeSearch
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ForceLegacyDefaultReferrerPolicy

  #### Usar una directiva de referencia predeterminada de sin referencia cuando se cambia a una versión anterior (en desuso).

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 81 o posterior

  #### Descripción

  Esta directiva está en desuso porque solo pretende ser un mecanismo a corto plazo para dar a las empresas más tiempo para actualizar su contenido web cuando se ha comprobado que es incompatible con la directiva de referencia predeterminada actual. No funciona en la versión 88 de Microsoft Edge.

La directiva de referencia predeterminada de Microsoft Edge se está reforzando a partir de su valor actual de no-referrer-when-downgrade, con strict-origin-when-cross-origin (más seguro), a través de una implementación gradual.

Antes del lanzamiento, esta directiva de la empresa no tendrá ningún efecto. Después de que se haya implementado y habilitado esta directiva de empresa, la directiva de referencia predeterminada de Microsoft Edge se establecerá en su valor anterior de no-referrer-when-downgrade.

Esta directiva de empresa está deshabilitada de forma predeterminada.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ForceLegacyDefaultReferrerPolicy
  - Nombre de GP: usar de forma predeterminada la directiva sin referencia cuando se cambia a una versión anterior.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ForceLegacyDefaultReferrerPolicy
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ForceLegacyDefaultReferrerPolicy
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ForceNetworkInProcess

  #### Forzar el código de red para que se ejecute en el proceso del explorador

  
  >OBSOLETA: Esta directiva está obsoleta y no funciona después de Microsoft Edge 83.
  #### Versiones compatibles:

  - En Windows desde 78, hasta 83

  #### Descripción

  Esta directiva está en desuso, ya que solo pretende ser un mecanismo a corto plazo para dar a las empresas más tiempo para migrar a software de terceros que no dependa del enlace de las API de red. Se recomienda el uso de servidores proxy sobre los LSP y el parcheo de la API de Win32.

Esta directiva fuerza el código de red para que se ejecute en el proceso del explorador.

Esta directiva está deshabilitada forma predeterminada Al habilitarla, los usuarios quedarán expuestos a problemas de seguridad cuando el proceso de red se realice en un espacio aislado

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ForceNetworkInProcess
  - Nombre GP: obligar a ejecutar el código de red en el proceso del explorador (obsoleto)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ForceNetworkInProcess
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### ForceSync

  #### Forzar la sincronización de los datos del explorador y no mostrar la solicitud de consentimiento de sincronización

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Fuerza la sincronización de datos en Microsoft Edge. Asimismo, esta directiva impide al usuario desactivar la sincronización.

Si no configura esta directiva, los usuarios podrán activar o desactivar la sincronización. Si habilita esta directiva, los usuarios no podrán desactivar la sincronización.

Para que esta directiva funcione correctamente, la directiva [BrowserSignin](#browsersignin) no debe estar configurada, o bien debe establecerse como habilitada. Si [BrowserSignin](#browsersignin) está establecido como deshabilitado, [ForceSync](#forcesync) no tendrá efecto.

[SyncDisabled](#syncdisabled) no debe estar configurado o debe establecerse como "Falso". Si se establece como "Verdadero", [ForceSync](#forcesync) no tendrá efecto.

0 = No iniciar automáticamente la sincronización y mostrar el consentimiento de sincronización (predeterminado) 1 = Forzar la activación de la sincronización para el perfil de usuario de Azure AD o Azure AD degradado y no mostrar la solicitud de consentimiento de sincronización

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ForceSync
  - Nombre de GP: Forzar la sincronización de los datos del explorador y no mostrar la solicitud de consentimiento de sincronización
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre de valor: ForceSync
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ForceSync
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ForceYouTubeRestrict

  #### Forzar el modo restringido de YouTube mínimo

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Exige un modo de limitación mínimo en YouTube y evita que los usuarios puedan seleccionar un modo menos restringido.

Establézcalo en "Estricto" para aplicar el Modo Estricto Restringido en YouTube.

Establézcalo en "Moderado" para exigir al usuario que solo use el Modo Moderado Restringido y el Modo Restringido Estricto en YouTube. Los usuarios no pueden deshabilitar el modo restringido.

No configure esta directiva o establézcala en "Off" para no aplicar el Modo Restringido en YouTube. Tanto las directivas externas, como las directivas de YouTube, aún podrían exigir el modo restringido.

Asignación de opciones de directiva:

* Off (0) = no aplicar el Modo Restringido en YouTube

* Moderate (1) = exigir al menos un Modo Restringido Moderado en YouTube

* Strict (2) = aplicar el Modo Restringido Estricto para YouTube

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ForceYouTubeRestrict
  - Nombre de GP: forzar el mínimo del modo restringido de YouTube
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ForceYouTubeRestrict
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ForceYouTubeRestrict
  - Valor de ejemplo:
``` xml
<integer>0</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### FullscreenAllowed

  #### Permitir el modo de pantalla completa

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 77 o posterior

  #### Descripción

  Establece la disponibilidad del modo de pantalla completa: toda la interfaz de usuario de Microsoft Edge está oculta y solo el contenido web es visible.

Si habilita esta directiva o no la configura, el usuario, las aplicaciones y las extensiones con los permisos adecuados podrán activar el modo de pantalla completa.

Si deshabilita esta directiva, los usuarios, las aplicaciones y las extensiones no podrán entrar en el modo de pantalla completa.

No se puede abrir Microsoft Edge en el modo de pantalla completa usando la línea de comandos cuando el modo de pantalla completa está deshabilitado.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: FullscreenAllowed
  - Nombre de GP: permitir el modo de pantalla completa
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: FullscreenAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### GloballyScopeHTTPAuthCacheEnabled

  #### Habilitar la caché de autenticación HTTP de ámbito global

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 81 o posterior

  #### Descripción

  Esta directiva configura una caché por perfil global con las credenciales de autenticación del servidor HTTP.

Si deshabilita o no establece esta directiva, el explorador usará el comportamiento predeterminado de la autenticación entre sitios, que a partir de la versión 80, estará en el ámbito de las credenciales de autenticación del servidor HTTP por el sitio de primer nivel. Así pues, si dos sitios utilizan recursos del mismo dominio de autenticación, las credenciales tendrán que proporcionarse de forma independiente según el contexto de cada uno de ellos. Las credenciales en caché de proxy almacenadas se reutilizarán en todos los sitios.

Si habilita esta directiva, las credenciales de autenticación HTTP especificadas en el contexto de un sitio se usarán automáticamente en el contexto de otro sitio.

Al habilitar esta directiva los sitios quedan vulnerables a algunos tipos de ataques entre sitios, y permite que los usuarios sean rastreados entre los mismos, incluso sin cookies, añadiendo entradas al caché de autorización HTTP mediante credenciales incrustadas en las direcciones URL.

Esta directiva está pensada para que las empresas que dependen del comportamiento heredado tengan la posibilidad de actualizar los procedimientos de inicio de sesión, que luego serán eliminados.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: GloballyScopeHTTPAuthCacheEnabled
  - Nombre de GP: habilitar la caché de autenticación HTTP de ámbito global
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: GloballyScopeHTTPAuthCacheEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: GloballyScopeHTTPAuthCacheEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar

  #### Forzar la navegación directa en el sitio de la intranet en lugar de buscar en las entradas de una sola palabra en la barra de direcciones

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Si habilita esta directiva, el resultado principal de la sugerencia de la barra de direcciones navegará a los sitios de la intranet si el texto introducido en la barra de direcciones es una sola palabra sin signos de puntuación.

La navegación predeterminada llevará a cabo una navegación en un sitio de la intranet que coincida con el texto escrito, cuando en éste se escriba una sola palabra sin signos de puntuación.

Si habilita esta directiva, el segundo resultado de la sugerencia de la barra de direcciones realizará una búsqueda en la web tal como se ha escrito, siempre que este texto sea de una sola palabra y sin signos de puntuación. Se usará el proveedor de búsquedas predeterminado, a menos que también se habilite una directiva para evitar la búsqueda web.

Dos efectos de la habilitación de esta directiva son:

La navegación por los sitios en busca de respuestas para las consultas de una sola palabra que normalmente podrían resolverse con un elemento del historial ya no se producirá. En su lugar, el explorador intentará navegar a través de sitios internos que pueden no existir en la intranet de una organización. Se producirá un error 404.

Los términos de búsqueda populares de una sola palabra requerirán de la selección manual de sugerencias de búsqueda para realizar una búsqueda adecuada.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Nombre de GP: forzar la navegación directa en el sitio de intranet en lugar de buscar por la introducción de una sola palabra en la barra de direcciones
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### HSTSPolicyBypassList

  #### Configurar la lista de nombres que se omitirán por alto la comprobación de la directiva de HSTS

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 79 o posterior

  #### Descripción

  Los nombres de host que se especifiquen en esta lista estarán exentos de la comprobación de directivas de HSTS, que podrían actualizar las solicitudes de "http://" a "https://". En esta directiva solo se permiten nombres de host de una sola etiqueta. Los nombres de host deben tener un nombre canónico. Todos los IDN deben ser convertidos a su formato de etiqueta A, y todas las letras ASCII deben estar en minúsculas. Esta directiva solo se aplicará a los nombres de host mencionados específicamente; sin embargo, no se aplicará a los subdominios nombrados en la lista.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: HSTSPolicyBypassList
  - Nombre de GP: configurar la lista de nombres que se omitirán en la comprobación de la directiva de HSTS
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\HSTSPolicyBypassList
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: HSTSPolicyBypassList
  - Valor de ejemplo:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### HardwareAccelerationModeEnabled

  #### Usar la aceleración de hardware cuando esté disponible

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica si está disponible el uso de la aceleración de hardware. Si habilita esta directiva o no la configura, se habilitará la aceleración de hardware, a menos que bloquee de manera explícita una función de GPU.

Si deshabilita esta directiva, también se deshabilitará la aceleración de hardware.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: HardwareAccelerationModeEnabled
  - Nombre de GP: usar la aceleración de hardware cuando esté disponible
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: HardwareAccelerationModeEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: HardwareAccelerationModeEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### HideFirstRunExperience

  #### Ocultar la experiencia de primera ejecución y la pantalla de presentación.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Si habilita esta directiva, la primera vista de Windows y la pantalla de presentación no se mostrarán a los usuarios cuando ejecuten Microsoft Edge por primera vez.

En las opciones de configuración que se muestran en la primera vista de Windows, el explorador usará de forma predeterminada lo siguiente:

-En la página de la nueva pestaña, el tipo de fuente estará establecido en las noticias de MSN, y el diseño en Inspiradores.

-El usuario seguirá iniciando sesión automáticamente en Microsoft Edge si la cuenta de Windows es del tipo Azure AD o MSA.

-La sincronización no se habilitará de forma predeterminada y se pedirá a los usuarios que elijan si quieren sincronizar al iniciar el explorador. Para configurar la sincronización y la solicitud de consentimiento de sincronización, puede usar la directiva [ForceSync](#forcesync) o [SyncDisabled](#syncdisabled).

Si deshabilita o no configura esta directiva, se mostrará la primera vista de Windows y la pantalla de presentación.

Nota: Las opciones específicas de configuración que se muestran al usuario en la primera vista de Windows, también se pueden administrar mediante el uso de otras directivas específicas. Puede usar la directiva HideFirstRunExperience junto a estas directivas para configurar una experiencia de navegación específica en sus dispositivos administrados. Entre estas directivas se encuentran:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[ForceSync](#forcesync)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: HideFirstRunExperience
  - Nombre de GP: Ocultar la experiencia de primera ejecución y la pantalla de presentación
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: HideFirstRunExperience
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: HideFirstRunExperience
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

  #### Ocultar el cuadro de diálogo redirección único y la pancarta en Microsoft Edge

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 87 o posterior

  #### Descripción

  Esta Directiva ofrece la opción de deshabilitar el cuadro de diálogo redirección único y el anuncio de banner. Cuando esta directiva está habilitada, los usuarios no verán tanto el cuadro de diálogo único como el banner.
Los usuarios seguirán siendo redirigidos a Microsoft Edge cuando encuentren un sitio web no compatible en Internet Explorer, pero no se importarán los datos de examen.

- Si habilita esta Directiva, el cuadro de diálogo de redirección y la pancarta nunca se mostrarán a los usuarios. Los datos de examen de los usuarios no se importarán cuando se produzca una redirección.

- Si deshabilita o no configura esta Directiva, el cuadro de diálogo de redirección se mostrará en la primera redirección y se mostrará el encabezado de redirección persistente para las sesiones que comiencen con una redirección. Los datos de examen de los usuarios se importarán cada vez que el usuario se encuentre en la redirección (solo si el usuario lo reenvía a él en el cuadro de diálogo de una sola vez).


  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled
  - Nombre GP: ocultar el cuadro de diálogo redirección único y la pancarta en Microsoft Edge
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```

  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportAutofillFormData

  #### Permitir la importación de los datos del formulario Autorrellenar

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite que los usuarios importen datos de los formularios de autorrelleno desde otro navegador a Microsoft Edge.

Si habilita esta directiva, la opción de importar manualmente los datos de autorrelleno se seleccionará automáticamente.

Si deshabilita esta directiva, los datos del formulario de autorelleno no se importarán en la primera ejecución, y los usuarios no podrán importarlos manualmente.

Si no se configura esta directiva, se importarán los datos de autorrelleno durante la primera ejecución, y los usuarios podrán elegir si desean importar estos datos manualmente en las sesiones de exploración posteriores.

Puede establecer esta directiva como una recomendación. Esto significa que Microsoft Edge importará los datos de autorelleno durante la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción de **datos de autorelleno** en la importación manual.

**Nota**: actualmente, esta directiva administra la importación desde los exploradores Google Chrome (en Windows 7, 8 y 10 y en macOS) y Mozilla Firefox (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportAutofillFormData
  - Nombre de GP: permitir la importación de los datos del formulario autorrellenado
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportAutofillFormData
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportAutofillFormData
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportBrowserSettings

  #### Permitir la importación de la configuración del explorador

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Permite que los usuarios importen la configuración desde otro explorador a Microsoft Edge.

Si habilita esta directiva, la casilla de verificación de la **Configuración del explorador** se seleccionará automáticamente en el cuadro de diálogo **Importar datos del explorador**.

Si deshabilita esta directiva, la configuración del explorador no se importará en la primera ejecución, y los usuarios no podrán importarlos manualmente.

Si no configura esta directiva, se importará la configuración del explorador durante la primera ejecución, y los usuarios podrán elegir si desean importar esta configuración manualmente en las sesiones de exploración posteriores.

También puede establecer esta directiva como una recomendación. Esto significa que Microsoft Edge importará la configuración durante la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción de la **configuración del explorador** en la importación manual.

**Nota**: actualmente, esta directiva administra la importación desde Google Chrome (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportBrowserSettings
  - Nombre de GP: permitir la importación de la configuración del explorador
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportBrowserSettings
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportBrowserSettings
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportCookies

  #### Permitir la importación de cookies

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 81 o posterior

  #### Descripción

  Permite que los usuarios importen las cookies desde otro explorador a Microsoft Edge.

Si deshabilita esta directiva, las cookies no se importarán durante la primera ejecución.

Si no configura esta directiva, las cookies no importarán durante la primera ejecución.

También puede establecer esta directiva como una recomendación. Esto quiere decir que Microsoft Edge importará las cookies durante la primera ejecución.

**Nota**: actualmente, esta directiva administra la importación desde Google Chrome (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportCookies
  - Nombre de GP: permitir la importación de cookies
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportCookies
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportCookies
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportExtensions

  #### Permitir la importación de extensiones

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 81 o posterior

  #### Descripción

  Permite que los usuarios importen las extensiones desde otro explorador a Microsoft Edge.

Si habilita esta directiva, la casilla de verificación de las **Extensiones** se seleccionará automáticamente en el cuadro de diálogo **Importar datos del explorador**.

Si deshabilita esta directiva, las extensiones no se importarán en la primera ejecución, y los usuarios no podrán importarlos manualmente.

Si no configura esta directiva, se importarán las extensiones durante la primera ejecución, y los usuarios podrán elegir si desean importarlas manualmente en las sesiones de exploración posteriores.

También puede establecer esta directiva como una recomendación. Esto significa que Microsoft Edge importará las extensiones durante la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción de los**favoritos** en la importación manual.

**Nota**: actualmente, esta directiva solo admite la importación de Google Chrome (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportExtensions
  - Nombre de GP: permitir la importación de extensiones
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportExtensions
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportExtensions
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportFavorites

  #### Permitir la importación de favoritos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite que los usuarios importen los favoritos desde otro explorador a Microsoft Edge.

Si habilita esta directiva, la casilla de verificación de los **favoritos** se seleccionará automáticamente en el cuadro de diálogo **Importar datos del explorador**.

Si deshabilita esta directiva, los favoritos no se importarán durante la primera ejecución, y los usuarios no podrán importarlos manualmente.

Si no configura esta directiva, se importarán los favoritos durante la primera ejecución, y los usuarios podrán elegir si desean importarlas manualmente en las sesiones de exploración posteriores.

También puede establecer esta directiva como una recomendación. Esto significa que Microsoft Edge importará los favoritos durante la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción de los**favoritos** en la importación manual.

**Nota**: actualmente, esta directiva administra la importación desde los exploradores Internet Explorer (en Windows 7, 8 y 10), Google Chrome (en Windows, 7, 8, 10 y en macOS), Mozilla Firefox (en Windows 7, 8 y 10 y en macOS) y Apple Safari (en macOs).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportFavorites
  - Nombre de GP: permitir la importación de favoritos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportFavorites
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportFavorites
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportHistory

  #### Permitir la importación del historial de exploración

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite que los usuarios importen su historial de exploración desde otro explorador a Microsoft Edge.

Si habilita esta directiva, la casilla de verificación del **historial de exploración** se seleccionará automáticamente en el cuadro de diálogo **Importar datos del explorador**.

Si deshabilita esta directiva, el historial de exploración no se importará durante la primera ejecución, y los usuarios no podrán importarlo manualmente.

Si no se configura esta directiva, se importará el historial de exploración durante la primera ejecución, y los usuarios podrán elegir si desean importarlo manualmente en las sesiones de exploración posteriores.

También puede establecer esta directiva como una recomendación. Esto significa que Microsoft Edge importará el historial de exploración durante la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción del **historial de exploración** en la importación manual.

**Nota**: actualmente, esta directiva administra la importación desde los exploradores Internet Explorer (en Windows 7, 8 y 10), Google Chrome (en Windows, 7, 8, 10 y en macOS), Mozilla Firefox (en Windows 7, 8 y 10 y en macOS) y Apple Safari (macOs).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportHistory
  - Nombre de GP: permitir la importación del historial de exploración
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportHistory
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportHistory
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportHomepage

  #### Permitir la importación de la configuración de la página principal

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite que los usuarios importen la configuración de su página principal desde otro explorador a Microsoft Edge.

Si habilita esta directiva, la opción de importar manualmente la configuración de su página principal se seleccionará automáticamente.

Si deshabilita esta directiva, la configuración de su página principal no se importará durante la primera ejecución, y los usuarios no podrán importarlos manualmente.

Si no se configura esta directiva, se importará la configuración de su página principal durante la primera ejecución, y los usuarios podrán elegir si desean importar estos datos manualmente en las sesiones de exploración posteriores.

Puede establecer esta directiva como una recomendación. Esto significa que Microsoft Edge importará la configuración de su página principal durante la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción de la **página principal** en la importación manual.

**Nota**: actualmente, esta directiva administra la importación desde Internet Explorer (en Windows 7, 8 y 10).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportHomepage
  - Nombre de GP: permitir la importación de la configuración de la página principal
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ImportHomepage
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportHomepage
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportOpenTabs

  #### Permitir la importación de las pestañas abiertas

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 79 o posterior

  #### Descripción

  Permite que los usuarios importen las pestañas ancladas desde otro explorador a Microsoft Edge.

Si habilita esta directiva, la casilla de verificación de las **pestañas abiertas** se seleccionará automáticamente en el cuadro de diálogo **Importar datos del explorador**.

Si deshabilita esta directiva, no se importarán las pestañas abiertas durante la primera ejecución, y los usuarios no podrán importarlas manualmente.

Si no configura esta directiva, se importarán las pestañas abiertas durante la primera ejecución, y los usuarios podrán elegir si desean importarlas manualmente en las sesiones de exploración posteriores.

También puede establecer esta directiva como una recomendación. Esto significa que Microsoft Edge importará las pestañas abiertas durante la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción de las **pestañas abiertas** en la importación manual.

**Nota**: actualmente, esta directiva solo admite la importación de Google Chrome (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportOpenTabs
  - Nombre de GP: permitir la importación de las pestañas abiertas
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportOpenTabs
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportOpenTabs
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportPaymentInfo

  #### Permitir la importación de información de pago

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite que los usuarios importen la información de pago desde otro explorador a Microsoft Edge.

Si habilita esta directiva, la casilla de verificación de la **información de pago** se seleccionará automáticamente en el cuadro de diálogo **Importar datos del explorador**.

Si deshabilita esta directiva, no se importará la información de pago en la primera ejecución, y los usuarios no podrán importarlos manualmente.

Si no se configura esta directiva, se importará la información de pago durante la primera ejecución, y los usuarios podrán elegir si desean importarla manualmente en las sesiones de exploración posteriores.

También puede establecer esta directiva como una recomendación. Esto significa que Microsoft Edge importará la información de pago durante la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción de la **información de pago** en la importación manual.

**Nota:** actualmente, esta directiva administra la importación desde Google Chrome (en Windows 7, 8, 10 y en macOS).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportPaymentInfo
  - Nombre de GP: permitir la importación de la información de pago
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportPaymentInfo
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportPaymentInfo
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportSavedPasswords

  #### Permitir la importación de las contraseñas guardadas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite que los usuarios importen las contraseñas guardadas desde otro explorador a Microsoft Edge.

Si habilita esta directiva, la opción de importar manualmente las contraseñas guardadas se seleccionará automáticamente.

Si deshabilita esta directiva, no se importarán las contraseñas guardadas durante la primera ejecución, y los usuarios no podrán importarlas manualmente.

Si no configura esta directiva, se importarán las contraseñas durante la primera ejecución, y los usuarios podrán elegir si desean importarlas manualmente en las sesiones de exploración posteriores.

Puede establecer esta directiva como una recomendación. Esto significa que Microsoft Edge importará las contraseñas durante la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción de las **contraseñas** en la importación manual.

**Nota**: actualmente, esta directiva administra la importación desde los exploradores Internet Explorer (en Windows 7, 8 y 10), Google Chrome (en Windows, 7, 8, 10 y en macOS) y Mozilla Firefox (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportSavedPasswords
  - Nombre de GP: permitir la importación de las contraseñas guardadas
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportSavedPasswords
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportSavedPasswords
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportSearchEngine

  #### Permitir la importación de la configuración del motor de búsqueda

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite que los usuarios importen la configuración del motor de búsqueda desde otro explorador a Microsoft Edge.

Si habilita esta directiva, la opción de importar manualmente la configuración del motor de búsqueda se seleccionará automáticamente.

Si deshabilita esta directiva, no se importará la configuración del motor de búsqueda durante la primera ejecución, y los usuarios no podrán importarlos manualmente.

Si no se configura esta directiva, se importará la configuración del motor de búsqueda durante la primera ejecución, y los usuarios podrán elegir si desean importar estos datos manualmente en las sesiones de exploración posteriores.

Puede establecer esta directiva como una recomendación. Esto significa que Microsoft Edge importará la configuración del motor de búsqueda durante la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción del **motor de búsqueda** en la importación manual.

**Nota**: actualmente, esta directiva administra la importación desde Internet Explorer (en Windows 7, 8 y 10).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportSearchEngine
  - Nombre de GP: permitir la importación de la configuración del motor de búsqueda
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportSearchEngine
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportSearchEngine
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ImportShortcuts

  #### Permitir la importación de accesos directos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 81 o posterior

  #### Descripción

  Permite que los usuarios importen los accesos directos desde otro explorador a Microsoft Edge.

Si deshabilita esta directiva, los accesos directos no se importarán durante la primera ejecución.

Si no configura esta directiva, los accesos directos se importarán durante la primera ejecución.

También puede establecer esta directiva como una recomendación. Esto quiere decir que Microsoft Edge importará los accesos directos durante la primera ejecución.

**Nota**: actualmente, esta directiva administra la importación desde Google Chrome (en Windows 7, 8, 10 y en macOS).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ImportShortcuts
  - Nombre de GP: permitir la importación de accesos directos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ImportShortcuts
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ImportShortcuts
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### InPrivateModeAvailability

  #### Configurar la disponibilidad del modo InPrivate

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica si el usuario puede abrir páginas en modo InPrivate en Microsoft Edge.

Si no configura esta directiva o la configura en "Habilitada", los usuarios podrán abrir las páginas en modo InPrivate.

Establezca esta directiva en "Deshabilitada" para evitar que los usuarios usen el modo InPrivate.

Establezca esta directiva en "Forzado" para usar siempre el modo InPrivate.

Asignación de opciones de directiva:

* Habilitado (0) = modo InPrivate disponible

* Deshabilitado (1) = modo InPrivate deshabilitado

* Forzado (2) = modo InPrivate forzado

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: InPrivateModeAvailability
  - Nombre de GP: configurar la disponibilidad del modo InPrivate
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: InPrivateModeAvailability
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: InPrivateModeAvailability
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### InsecureFormsWarningsEnabled

  #### Habilitar advertencias para formularios inseguros

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Esta directiva controla el tratamiento de formularios inseguros (formularios enviados a través de HTTP) incrustados en sitios seguros (HTTPS) en el explorador.
Si habilita esta directiva o no la establece, se mostrará una advertencia de página completa cuando se envíe un formulario inseguro. Además, se mostrará una advertencia junto a los campos de formulario cuando estén centrados y se deshabilitará el autorrelleno para estos formularios.
Si deshabilita esta directiva, no se mostrarán advertencias para formularios no seguros y el autorrelleno funcionará con normalidad.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: InsecureFormsWarningsEnabled
  - Nombre de GP: Habilitar advertencias para formularios inseguros
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre de valor: InsecureFormsWarningsEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: InsecureFormsWarningsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### IntensiveWakeUpThrottlingEnabled

  #### Controlar la característica IntensiveWakeUpThrottling

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 85 o posterior

  #### Descripción

  Cuando se habilita la característica IntensiveWakeUpThrottling, los temporizadores de JavaScript de las pestañas de fondo se aceleran y se separan de forma agresiva, y no más de una vez por minuto después de que se haya conectado una página durante 5 minutos o más.

Esta es una característica compatible con estándares web, pero puede romper la funcionalidad en algunos sitios web, lo que provoca que algunas acciones se retrasen hasta un minuto. Sin embargo, si se habilita, se producen ahorros significativos de CPU y batería. Consulte https://bit.ly/30b1XR4 para obtener más detalles.

Si habilita esta Directiva, la característica se habilitará y los usuarios no podrán invalidar esta configuración.
Si deshabilita esta Directiva, la característica se deshabilitará y los usuarios no podrán invalidar esta configuración.
Si no configura esta Directiva, la característica se controlará con su propia lógica interna. Los usuarios pueden configurar manualmente esta opción.

Tenga en cuenta que la Directiva se aplica por cada proceso del representador, con el valor más reciente de la configuración de Directiva vigente cuando se inicia el proceso de un representador. Se debe reiniciar completamente para asegurar que todas las pestañas cargadas reciban una configuración de directiva coherente. Es inocuo tener procesos que se ejecuten con diferentes valores de esta Directiva.


  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: IntensiveWakeUpThrottlingEnabled
  - Nombre de GP: controle la característica IntensiveWakeUpThrottling
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: IntensiveWakeUpThrottlingEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: IntensiveWakeUpThrottlingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### InternetExplorerIntegrationEnhancedHangDetection

  #### Configurar la detección de bloqueos mejorada para el modo de Internet Explorer

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 84 o posterior

  #### Descripción

  La detección de bloqueos mejorada es un enfoque más específico para detectar páginas web bloqueadas en el modo de Internet Explorer que la que usa Internet Explorer independiente. Cuando se detecta una página web que se ha bloqueado, el explorador aplica una mitigación para evitar el bloqueo del resto del explorador.

Esta configuración le permite configurar el uso de la detección de bloqueos mejorada en caso de que se realicen problemas incompatibles con cualquiera de los sitios Web. Se recomienda deshabilitar esta directiva solo si aparecen notificaciones como "(el sitio web) no responde" en el modo de Internet Explorer, pero no en Internet Explorer independiente.

Esta configuración funciona conjuntamente con: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) establecida en "IEMode" y la directiva [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) donde la lista tiene al menos una entrada.

Si establece esta directiva en "Habilitada" o no la configura, los sitios web que se ejecuten en modo de Internet Explorer usarán la detección de bloqueos mejorada.

Si establece esta directiva en "Deshabilitada", la detección de bloqueos mejorada se deshabilita, y los usuarios recibirán el comportamiento de la detección de bloqueos de Internet Explorer básica.

Para obtener más información sobre el modo Internet Explorer, vea [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Asignación de opciones de directiva:

* Deshabilitada (0) = detección de bloqueos mejorada deshabilitada

* Habilitada (1) = detección de bloqueos mejorada habilitada

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: InternetExplorerIntegrationEnhancedHangDetection
  - Nombre GP: configurar la detección mejorada de bloqueo para el modo de Internet Explorer
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: InternetExplorerIntegrationEnhancedHangDetection
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### InternetExplorerIntegrationLevel

  #### Configurar la integración de Internet Explorer

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 77 o posterior

  #### Descripción

  Para obtener instrucciones sobre cómo configurar la experiencia óptima en el modo de Internet Explorer, vea [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Asignación de opciones de directiva:

* None (0) = ninguno

* IEMode (1) = modo de Internet Explorer

* NeedIE (2) = Internet Explorer 11

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: InternetExplorerIntegrationLevel
  - Nombre de GP: configurar la integración de Internet Explorer
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: InternetExplorerIntegrationLevel
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteList

  #### Configurar la lista de sitios del Modo de empresa

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 78 o posterior

  #### Descripción

  Para obtener instrucciones sobre cómo configurar la experiencia óptima en el modo de Internet Explorer, vea [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: InternetExplorerIntegrationSiteList
  - Nombre de GP: configurar la lista de sitios del modo de empresa
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: InternetExplorerIntegrationSiteList
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://internal.contoso.com/sitelist.xml"
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteRedirect

  #### Especificar cómo se comportan las navegaciones "en la página" de los sitios no configurados al iniciarse en las páginas en modo Internet Explorer

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 81 o posterior

  #### Descripción

  Una navegación "en la página" se inicia desde un vínculo, un script o un formulario en la página actual. También puede ser un redireccionamiento de servidor de un intento de navegación "en la página" anterior. Por otra parte, un usuario puede iniciar una navegación que no sea "en la página", y que sea independiente de la página actual, de varias formas con los controles del explorador. Por ejemplo, con la barra de direcciones, el botón Atrás o un vínculo favorito.

Esta configuración le permite determinar si las navegaciones desde las páginas cargadas en el modo Internet Explorer a los sitios sin configurar (que no están configurados en la lista de sitios del modo de empresa) vuelven a Microsoft Edge o permanecen en el modo Internet Explorer.

Esta configuración funciona conjuntamente con: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) establecida en "IEMode" y la directiva [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) donde la lista tiene al menos una entrada.

Si deshabilita o no configura esta directiva, solo podrán abrirse los sitios que fueron configurados para el modo Internet Explorer. Cualquier sitio que no esté configurado para abrirse en el modo Internet Explorer se redirigirá a Microsoft Edge.

Si configura esta directiva como "Predeterminada", solo podrán abrirse los sitios que fueron configurados para el modo de Internet Explorer. Cualquier sitio que no esté configurado para abrirse en el modo Internet Explorer se redirigirá a Microsoft Edge.

Si establece esta directiva en "AutomaticNavigationsOnly", obtendrá la experiencia predeterminada, aunque todas las navegaciones automáticas (como los redireccionamientos 302) a sitios sin configurar se mantendrán en el modo de Internet Explorer.

Si establece esta directiva en "AllInPageNavigations", todas las navegaciones realizadas desde páginas cargadas en modo IE hasta los sitios sin configurar se mantendrán en el modo de Internet Explorer (opción menos recomendada).

Para obtener más información sobre el modo Internet Explorer, vea [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Asignación de opciones de directiva:

* Predeterminado (0) = predeterminado

* AutomaticNavigationsOnly (1) = mantener solo la navegación automática en el modo de Internet Explorer

* AllInPageNavigations (2) = mantener todas las navegaciones en la página en el modo de Internet Explorer

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: InternetExplorerIntegrationSiteRedirect
  - Nombre de GP: especificar el comportamiento de las navegaciones "en la página" de los sitios no configurados cuando se inician desde las páginas en modo Internet Explorer
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: InternetExplorerIntegrationSiteRedirect
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### InternetExplorerIntegrationTestingAllowed

  #### Permitir pruebas del modo Internet Explorer

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 86 o posterior

  #### Descripción

  Esta directiva es un sustituto de la directiva de marca de pruebas del modo IE. Permite a los usuarios abrir una pestaña en modo IE desde la opción del menú de la interfaz de usuario.

Esta configuración funciona conjuntamente con: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) establecida en "IEMode" y la directiva [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) donde la lista tiene al menos una entrada.

Si habilita esta directiva, los usuarios podrán abrir la pestaña en modo IE desde la opción de la interfaz de usuario y desplazarse por el sitio actual hasta un sitio en modo IE.

Si deshabilita esta directiva, los usuarios no podrán ver la opción de la interfaz de usuario directamente en el menú.

Si no configura esta directiva, podrá configurar la marca de pruebas del modo IE de forma manual.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: InternetExplorerIntegrationTestingAllowed
  - Nombre de GP: Permitir pruebas del modo Internet Explorer
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre de valor: InternetExplorerIntegrationTestingAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### IsolateOrigins

  #### Habilitar el aislamiento de sitio para determinados orígenes

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica los orígenes para que se ejecuten de forma aislada, en su propio proceso.

Esta directiva también aísla los orígenes nombrados por los subdominios, por ejemplo, al especificar https://contoso.com/ que se https://foo.contoso.com/ aislarán como parte del https://contoso.com/ sitio.

Si se habilita esta directiva, cada uno de los orígenes nombrados en una lista separada por comas se ejecutará en su propio proceso.

Si deshabilita esta directiva, las funciones "IsolateOrigins" y "SitePerProcess" también se deshabilitarán. Los usuarios aún podrán habilitar la directiva ''IsolateOrigins'' manualmente, a través de los indicadores de la línea de comandos.

Si no configura esta directiva, el usuario podrá cambiar esta configuración manualmente.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: IsolateOrigins
  - Nombre de GP: habilitar el aislamiento de sitio para orígenes determinados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: IsolateOrigins
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: IsolateOrigins
  - Valor de ejemplo:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### LocalProvidersEnabled

  #### Permita sugerencias de proveedores locales.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 83 o posterior

  #### Descripción

  Permitir sugerencias por parte de los proveedores de sugerencias en el dispositivo (proveedores locales), como por ejemplo, los favoritos y el historial de navegación, en la barra de direcciones de Microsoft Edge y en la lista de autosugerencias.

Si habilita esta directiva, se usarán las sugerencias de proveedores locales.

Si deshabilita esta directiva, las sugerencias de proveedores locales jamás se utilizarán. No se mostrarán sugerencias para el historial y los favoritos locales.

Si no configura esta Directiva, se mostrarán sugerencias para los proveedores locales, aunque el usuario podrá cambiar esta opción con la configuración de alternancia.

Tenga en cuenta que es posible que algunas funciones no estén disponibles si se ha aplicado una directiva para deshabilitar esta función. Por ejemplo, las sugerencias del historial de navegación no estarán disponibles si habilita la directiva [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled).

Para finalizar la aplicación de esta directiva, es necesario que se reinicie el explorador.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: LocalProvidersEnabled
  - Nombre de GP: permitir las sugerencias de los proveedores locales
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: LocalProvidersEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: LocalProvidersEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ManagedFavorites

  #### Configurar Favoritos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configura una lista de los favoritos administrados.

La directiva crea una lista de favoritos. Cada favorito tiene las claves "nombre" y "URL", que contienen el nombre del favorito y su objetivo. Puede configurar una subcarpeta definiendo un favorito sin la clave "URL" pero con la clave adicional "secundarios", la cual contiene una lista de favoritos definida anteriormente (algunos de los cuales pueden volver a ser carpetas). Microsoft Edge modifica las URL incompletas como si fueran enviadas a través de la barra de direcciones, por ejemplo "microsoft.com" pasa a ser "https://microsoft.com/".

Estos favoritos se ubican en una carpeta que no puede ser modificada por el usuario (pero el usuario puede elegir si quiere ocultarla en la barra de favoritos). De forma predeterminada, el nombre de la carpeta es "favoritos administrados", pero puede cambiarlo si agrega a la lista de favoritos un diccionario que contenga la clave "toplevel_name" con el nombre de la carpeta que desee usar como valor.

Los favoritos administrados no se sincronizan con la cuenta del usuario y no pueden ser modificados por las extensiones.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ManagedFavorites
  - Nombre de GP: configurar Favoritos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ManagedFavorites
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [
  {
    "toplevel_name": "My managed favorites folder"
  }, 
  {
    "name": "Microsoft", 
    "url": "microsoft.com"
  }, 
  {
    "name": "Bing", 
    "url": "bing.com"
  }, 
  {
    "children": [
      {
        "name": "Microsoft Edge Insiders", 
        "url": "www.microsoftedgeinsider.com"
      }, 
      {
        "name": "Microsoft Edge", 
        "url": "www.microsoft.com/windows/microsoft-edge"
      }
    ], 
    "name": "Microsoft Edge links"
  }
]
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [{"toplevel_name": "My managed favorites folder"}, {"name": "Microsoft", "url": "microsoft.com"}, {"name": "Bing", "url": "bing.com"}, {"children": [{"name": "Microsoft Edge Insiders", "url": "www.microsoftedgeinsider.com"}, {"name": "Microsoft Edge", "url": "www.microsoft.com/windows/microsoft-edge"}], "name": "Microsoft Edge links"}]
  ```
  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ManagedFavorites
  - Valor de ejemplo:
``` xml
<key>ManagedFavorites</key>
<array>
  <dict>
    <key>toplevel_name</key>
    <string>My managed favorites folder</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Microsoft</string>
    <key>url</key>
    <string>microsoft.com</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Bing</string>
    <key>url</key>
    <string>bing.com</string>
  </dict>
  <dict>
    <key>children</key>
    <array>
      <dict>
        <key>name</key>
        <string>Microsoft Edge Insiders</string>
        <key>url</key>
        <string>www.microsoftedgeinsider.com</string>
      </dict>
      <dict>
        <key>name</key>
        <string>Microsoft Edge</string>
        <key>url</key>
        <string>www.microsoft.com/windows/microsoft-edge</string>
      </dict>
    </array>
    <key>name</key>
    <string>Microsoft Edge links</string>
  </dict>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ManagedSearchEngines

  #### Administrar motores de búsqueda

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Le permite configurar una lista de hasta 10 motores de búsqueda, de entre los cuales uno debe estar marcado como motor de búsqueda predeterminado.
No es necesario que especifique la codificación. A partir de Microsoft Edge 80, los parámetros suggest_url y image_search_url son opcionales. El parámetro opcional, image_search_post_params (que consiste en pares de nombres y valores separados por comas), está disponible a partir de Microsoft Edge 80.

A partir de Microsoft Edge 83, puedes habilitar la detección del motor de búsqueda con el parámetro opcional allow_search_engine_discovery. Este parámetro debe ser el primer elemento en la lista. Si no se especifica allow_search_engine_discovery, se deshabilitará la detección del motor de búsqueda de forma predeterminada. A partir de Microsoft Edge 84, puede establecer esta directiva como directiva recomendada para permitir la detección de proveedores de búsqueda. No es necesario agregar el parámetro opcional allow_search_engine_discovery.

Si habilita esta directiva, los usuarios no podrán agregar, quitar ni cambiar ningún motor de búsqueda de la lista. Los usuarios pueden configurar cualquier motor de búsqueda de la lista como motor de búsqueda predeterminado.

Si deshabilita o no configura esta directiva, los usuarios podrán modificar la lista de motores de búsqueda libremente.

Si la directiva [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) está establecida, entonces se ignorará esta directiva (ManagedSearchEngines). El usuario debe reiniciar su explorador para finalizar la aplicación de esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ManagedSearchEngines
  - Nombre de GP: administrar los motores de búsqueda
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ManagedSearchEngines
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [
  {
    "allow_search_engine_discovery": true
  }, 
  {
    "is_default": true, 
    "keyword": "example1.com", 
    "name": "Example1", 
    "search_url": "https://www.example1.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"
  }, 
  {
    "image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}", 
    "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload", 
    "keyword": "example2.com", 
    "name": "Example2", 
    "search_url": "https://www.example2.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"
  }, 
  {
    "encoding": "UTF-8", 
    "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload", 
    "keyword": "example3.com", 
    "name": "Example3", 
    "search_url": "https://www.example3.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"
  }, 
  {
    "keyword": "example4.com", 
    "name": "Example4", 
    "search_url": "https://www.example4.com/search?q={searchTerms}"
  }
]
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [{"allow_search_engine_discovery": true}, {"is_default": true, "keyword": "example1.com", "name": "Example1", "search_url": "https://www.example1.com/search?q={searchTerms}", "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"}, {"image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}", "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload", "keyword": "example2.com", "name": "Example2", "search_url": "https://www.example2.com/search?q={searchTerms}", "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"}, {"encoding": "UTF-8", "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload", "keyword": "example3.com", "name": "Example3", "search_url": "https://www.example3.com/search?q={searchTerms}", "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"}, {"keyword": "example4.com", "name": "Example4", "search_url": "https://www.example4.com/search?q={searchTerms}"}]
  ```
  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ManagedSearchEngines
  - Valor de ejemplo:
``` xml
<key>ManagedSearchEngines</key>
<array>
  <dict>
    <key>allow_search_engine_discovery</key>
    <true/>
  </dict>
  <dict>
    <key>is_default</key>
    <true/>
    <key>keyword</key>
    <string>example1.com</string>
    <key>name</key>
    <string>Example1</string>
    <key>search_url</key>
    <string>https://www.example1.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example1.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>image_search_post_params</key>
    <string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
    <key>image_search_url</key>
    <string>https://www.example2.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example2.com</string>
    <key>name</key>
    <string>Example2</string>
    <key>search_url</key>
    <string>https://www.example2.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example2.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>encoding</key>
    <string>UTF-8</string>
    <key>image_search_url</key>
    <string>https://www.example3.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example3.com</string>
    <key>name</key>
    <string>Example3</string>
    <key>search_url</key>
    <string>https://www.example3.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example3.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>keyword</key>
    <string>example4.com</string>
    <key>name</key>
    <string>Example4</string>
    <key>search_url</key>
    <string>https://www.example4.com/search?q={searchTerms}</string>
  </dict>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### MaxConnectionsPerProxy

  #### Número máximo de conexiones simultáneas al servidor proxy

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica el número máximo de conexiones simultáneas al servidor proxy.

Algunos servidores proxy no pueden administrar una gran cantidad de conexiones simultáneas por cliente, esto se puede solucionar estableciendo esta directiva en un valor inferior.

El valor de esta directiva debe ser inferior a 100 y superior a 6. El valor predeterminado es 32.

Se sabe que algunas aplicaciones web consumen muchas conexiones con GETs en espera, por lo que si se reducen las conexiones máximas a un nivel inferior a 32, las redes de los exploradores podrían colgarse al abrir una gran cantidad de estas aplicaciones web.

Si no configura esta directiva, se usará el valor predeterminado (32).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: MaxConnectionsPerProxy
  - Nombre de GP: número máximo de conexiones simultáneas al servidor proxy
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: MaxConnectionsPerProxy
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000020
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: MaxConnectionsPerProxy
  - Valor de ejemplo:
``` xml
<integer>32</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### MediaRouterCastAllowAllIPs

  #### Permitir que Google Cast se conecte para transmitir dispositivos en todas las direcciones IP

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilite esta directiva para permitir que Google Cast se conecte a los dispositivos Cast a través de todas las direcciones IP y no solo a través de las direcciones privadas RFC1918/RFC4193.

Deshabilite esta directiva para restringir Google Cast a los dispositivos Cast en las direcciones privadas RFC1918/RFC4193.

De no configurar esta directiva, Google Cast se conectará a los dispositivos de Cast en las direcciones privadas RFC1918/RFC4193 únicamente, a menos que habilite la característica CastAllowAllIPs.

Si la Directiva [EnableMediaRouter](#enablemediarouter) está deshabilitada, no se aplicará esta Directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: MediaRouterCastAllowAllIPs
  - Nombre de GP: permitir que Google Cast se conecte a los dispositivos de Cast a través de todas las direcciones IP
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: MediaRouterCastAllowAllIPs
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: MediaRouterCastAllowAllIPs
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### MetricsReportingEnabled

  #### Habilitar el uso y los informes de datos relacionados con bloqueos (en desuso)

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Esta directiva está en desuso. Actualmente, se admite pero quedará obsoleto en Microsoft Edge 89. Esta directiva se reemplaza por la nueva directiva: [DiagnosticData](#diagnosticdata)para Windows 7, Windows 8 y macOS. Esta directiva se ha reemplazado por Permitir telemetría en Windows 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Esta directiva permite los informes de datos de uso y relacionados con bloqueos acerca de Microsoft Edge para Microsoft.

Habilita esta directiva para enviar informes de datos de uso y relacionados con bloqueos a Microsoft. Deshabilita esta directiva para no enviar los datos a Microsoft. En ambos casos, los usuarios no pueden cambiar ni invalidar la configuración.

En Windows 10, si no se configura esta directiva, Microsoft Edge se ajustará por defecto a la configuración de datos de diagnóstico de Windows. Si habilita esta directiva, Microsoft Edge solo podrá enviar datos de uso si la configuración de los datos de diagnóstico de Windows está establecida en Mejorado o Completo. Si deshabilita esta directiva, Microsoft Edge no enviará los datos de uso. Los datos relacionados con bloqueos se envían en función de la configuración de datos de diagnóstico de Windows. Obtenga más información acerca de la configuración de datos de diagnóstico de Windows en [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569).

En Windows 7, Windows 8 y macOS, esta directiva controla el envío de datos de uso y de bloqueos. Si no configura esta directiva, Microsoft Edge se ajustará de forma predeterminada a las preferencias del usuario.

Para habilitar esta directiva, debe establecer[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) en habilitado. Si [MetricsReportingEnabled](#metricsreportingenabled) o [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) no se configura o se deshabilita, estos datos no se enviarán a Microsoft.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o en las instancias de macOS administradas por MDM o unidas a un dominio por MCX.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: MetricsReportingEnabled
  - Nombre de GP: habilitar el uso y los informes de datos relacionados con bloqueos (en desuso)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: MetricsReportingEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: MetricsReportingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NativeWindowOcclusionEnabled

  #### Habilitar oclusión de ventana nativa

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 84 o posterior

  #### Descripción

  Habilita la oclusión de ventana nativa en Microsoft Edge.

Si habilita esta configuración, para reducir el consumo de energía y de CPU, Microsoft Edge detectará cuando una ventana esté cubierta por otras ventanas, y suspenderá los píxeles de los trabajos de pintura.

Si deshabilita esta configuración, Microsoft Edge no detectará cuando una ventana esté cubierta por otras ventanas.

Si no se establece esta directiva, se habilitará la detección de ventanas ocultas.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NativeWindowOcclusionEnabled
  - Nombre GP: habilitar oclusión de ventana nativa
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: NativeWindowOcclusionEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### NavigationDelayForInitialSiteListDownloadTimeout

  #### Establecer un tiempo de espera de retardo en la navegación por la etiqueta de la lista de sitios de modo empresarial

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 84 o posterior

  #### Descripción

  Permite establecer un tiempo de espera, en segundos, en las pestañas de Microsoft Edge esperando para navegar hasta que el explorador Descargue la lista de sitios de modo empresarial inicial.

Esta configuración funciona conjuntamente con: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) establecida en "IEMode" y la directiva [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) donde la lista tiene al menos una entrada y [DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) se establece en "Todas las navegaciones aptas" (1).

Las pestañas no se verán más largas que este tiempo de espera de la lista de sitios de modo empresarial para descargar. Si el explorador no ha terminado de descargar la lista del sitio modo empresarial cuando se agote el tiempo de espera, las pestañas de Microsoft Edge seguirán navegando de todos modos. El valor del tiempo de espera no debe ser mayor que 20 segundos y no puede ser menor que 1 segundo.

Si define el tiempo de espera en esta directiva en un valor mayor que el predeterminado de 2 segundos, se mostrará una barra de información al usuario después de 2 segundos. La barra de información contiene un botón que permite que el usuario se deje esperando a que finalice la descarga de la lista de sitios en el modo de empresa.

Si no configura esta Directiva, se usará el tiempo de espera predeterminado de 2 segundos. Este valor predeterminado está sujeto a cambios en el futuro.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NavigationDelayForInitialSiteListDownloadTimeout
  - Nombre de la Directiva de Grupo: establecer un tiempo de espera para retrasar la navegación por la ficha de la lista de sitios de modo empresarial
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: NavigationDelayForInitialSiteListDownloadTimeout
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x0000000a
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### NetworkPredictionOptions

  #### Habilitar predicción de red

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite la predicción de red y evita que los usuarios cambien esta configuración.

Esto controla la captura previa del DNS, la preconexión del TCP y el SSL, y la representación previa de las páginas web.

Si no configura esta directiva, la predicción de red estará habilitada, pero el usuario podrá cambiarla.

Asignación de opciones de directiva:

* NetworkPredictionAlways (0) = predecir las acciones de red en cualquiera de sus conexiones

* NetworkPredictionWifiOnly (1) = no compatible. Si se usa este valor, se tratará como si se hubiera definido en "Predecir las acciones de red en cualquiera de sus conexiones" (0).

* NetworkPredictionNever (2) = no predecir las acciones de red en cualquiera de sus conexiones

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NetworkPredictionOptions
  - Nombre de GP: habilitar la predicción de red
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: NetworkPredictionOptions
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: NetworkPredictionOptions
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### NonRemovableProfileEnabled

  #### Configurar si un usuario siempre tiene un perfil predeterminado que inicia sesión automáticamente con su cuenta profesional o educativa

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 78 o posterior

  #### Descripción

  Esta directiva determina si un usuario puede quitar el perfil de Microsoft Edge que ha iniciado sesión automáticamente con la cuenta profesional o educativa de un usuario.

Si habilita esta directiva, se creará un perfil que no se pueda quitar con la cuenta profesional o escolar del usuario en Windows. No se podrá quitar este perfil o iniciar sesión.

Si deshabilita o no configura esta directiva, el perfil con el que se ha iniciado sesión automáticamente, ya sea con la cuenta profesional o educativa de un usuario en Windows, no podrá cerrar sesión ni ser quitado por el usuario.

Si desea configurar el inicio de sesión del explorador, utilice la directiva [BrowserSignin](#browsersignin).

Esta directiva solo está disponible en las instancias de Windows que están unidas a un dominio de Microsoft Active Directory o en las instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: NonRemovableProfileEnabled
  - Nombre de GP: configurar qué usuario tiene un perfil predeterminado para iniciar sesión automáticamente con su cuenta profesional o educativa.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: NonRemovableProfileEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### OverrideSecurityRestrictionsOnInsecureOrigin

  #### Controlar el lugar en el que se aplican restricciones de seguridad para orígenes inseguros

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica una lista de orígenes (direcciones URL) o patrones de nombres de host (como "*.contoso.com") en los que no se aplican las restricciones de seguridad para orígenes inseguros.

Con esta directiva se pueden especificar los orígenes permitidos para aplicaciones heredadas que no puedan implementar TLS o configurar un servidor de ensayo para el desarrollo interno de la web, de modo que los desarrolladores puedan probar las características que requieran de contextos seguros sin tener que desplegar TLS en el servidor de ensayo. Esta directiva también evita que el origen sea etiquetado como "no seguro" en el omnibox.

Establecer una lista de direcciones URL en esta directiva tiene el mismo efecto que establecer el indicador de la línea de comandos "--unsafely-treat-insecure-origin-as-secure" en una lista separada por comas en las mismas direcciones URL. Al habilitar esta directiva, se anula el marcador de la línea de comandos

Para obtener más información sobre contextos seguros, vea https://www.w3.org/TR/secure-contexts/.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: OverrideSecurityRestrictionsOnInsecureOrigin
  - Nombre de GP: controlar el lugar donde se aplican las restricciones de seguridad para orígenes inseguros
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: OverrideSecurityRestrictionsOnInsecureOrigin
  - Valor de ejemplo:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PaymentMethodQueryEnabled

  #### Permita que los sitios web consulten los métodos de pago disponibles

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Permite establecer si los sitios web podrán comprobar si el usuario tiene métodos de pago guardados.

Si deshabilita esta directiva, se le informará a los sitios web que utilicen las API PaymentRequest.canMakePayment o PaymentRequest.hasEnrolledInstrument que no hay ningún método de pago disponible.

Si habilita o no establece esta directiva, los sitios web podrán comprobar si el usuario tiene métodos de pago guardados.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PaymentMethodQueryEnabled
  - Nombre de GP: permitir que los sitios web consulten los métodos de pago disponibles
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: PaymentMethodQueryEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PaymentMethodQueryEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PersonalizationReportingEnabled

  #### Permita la personalización de anuncios, búsquedas y noticias enviando el historial de exploración a Microsoft

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Esta directiva impide que Microsoft recopile el historial de exploración de un usuario de Microsoft Edge para utilizarlo en la personalización de la publicidad, búsquedas, noticias y otros servicios Microsoft.

Esta opción solo está disponible para los usuarios con una cuenta de Microsoft. Esta opción no está disponible para las cuentas de menores o de empresa.

Si deshabilita esta directiva, los usuarios no podrán cambiar ni reemplazar esta configuración. Si esta directiva está habilitada o no ha sido configurada, Microsoft Edge se establecerá de forma predeterminada en la preferencia del usuario.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PersonalizationReportingEnabled
  - Nombre de GP: permitir la personalización de anuncios, búsquedas y noticias al enviar el historial de exploración a Microsoft.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: PersonalizationReportingEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PersonalizationReportingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PinningWizardAllowed

  #### Permita anclar al Asistente para tareas

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 80 o posterior

  #### Descripción

  Microsoft Edge usa el asistente Anclar a la barra de tareas para ayudar a los usuarios a anclar los sitios sugeridos a la barra de tareas. La característica anclar a la barra de tareas está habilitada de forma predeterminada y el usuario podrá acceder a la misma desde el menú Configuración y más.

Si habilita o no configura esta directiva, los usuarios podrán llamar al asistente Anclar a la barra de tareas desde el menú Configuración y Más. También se puede llamar al asistente a través del inicio de un protocolo.

Si deshabilita esta directiva, el asistente para anclar a la barra de tareas se deshabilitará del menú y no podrá ser llamado a través del inicio de un protocolo.

Las opciones de configuración del usuario para habilitar o deshabilitar el asistente para anclar a la barra de tareas no están disponibles.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PinningWizardAllowed
  - Nombre de GP: permitir el anclaje del asistente a la barra de tareas
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: PinningWizardAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### ProactiveAuthEnabled

  #### Permitir la autenticación proactiva

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Le permite configurar si debe habilitar o no la autenticación proactiva.

Si habilita esta directiva, Microsoft Edge intentará autenticar con el modo proactivo al usuario que haya iniciado sesión con los servicios Microsoft. Microsoft Edge comprueba con regularidad la actualización del manifiesto que contiene la configuración que rige la ejecución de este proceso en un servicio en línea.

Si deshabilita esta directiva, Microsoft Edge no intentará autenticar con el modo proactivo al usuario que haya iniciado sesión con los servicios Microsoft. Microsoft Edge dejará de comprobar con regularidad la actualización del manifiesto que contiene la configuración que rige la ejecución de este proceso en un servicio en línea.

Si no configura esta directiva, se habilitará la autenticación proactiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ProactiveAuthEnabled
  - Nombre de GP: permitir la autenticación proactiva
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ProactiveAuthEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ProactiveAuthEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PromotionalTabsEnabled

  #### Habilitar contenido promocional de pestañas completas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Controla la presentación del contenido de promoción o educación en la pestaña completa. Esta configuración controla la presentación de las páginas de bienvenida que ayudan a los usuarios a iniciar sesión en Microsoft Edge, a elegir su explorador predeterminado o a conocer las características del producto.

Si habilita esta directiva (establecida como verdadera) o no la configura, Microsoft Edge podrá mostrar el contenido de las pestañas completas a los usuarios para proporcionarles información sobre el producto.

Si deshabilita (establecido como falso) esta directiva, Microsoft Edge no podrá mostrar a los usuarios el contenido de las pestañas completas.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PromotionalTabsEnabled
  - Nombre de GP: habilitar el contenido promocional de la pestaña completa
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: PromotionalTabsEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PromotionalTabsEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### PromptForDownloadLocation

  #### Pregunte dónde guardar los archivos descargados

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Establece la opción de preguntar dónde guardar un archivo antes de descargarlo.

Si habilita esta directiva, se le preguntará al usuario dónde guardar cada archivo antes de descargarlo; si no la configura, los archivos se guardarán automáticamente en la ubicación predeterminada, sin preguntarle al usuario.

Si no configura esta directiva, el usuario podrá cambiar su configuración.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: PromptForDownloadLocation
  - Nombre de GP: Preguntar dónde guardar los archivos descargados
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: PromptForDownloadLocation
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: PromptForDownloadLocation
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### QuicAllowed

  #### Permitir protocolo QUIC

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite el uso del protocolo QUIC en Microsoft Edge.

Si habilita o no configura esta directiva, se permitirá el protocolo QUIC.

Si deshabilita esta directiva, se bloqueará el protocolo QUIC.

QUIC es un protocolo red de la capa de transporte que puede mejorar el rendimiento de las aplicaciones web que usan actualmente el TCP.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: QuicAllowed
  - Nombre de GP: permitir el protocolo QUIC
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: QuicAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: QuicAllowed
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### RedirectSitesFromInternetExplorerPreventBHOInstall

  #### Evita la instalación del BHO para redirigir sitios incompatibles desde Internet Explorer a Microsoft Edge

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 87 o posterior

  #### Descripción

  Esta configuración le permite especificar si se debe bloquear la instalación del objeto auxiliar del navegador (BHO) que permite redirigir sitios incompatibles de Internet Explorer a Microsoft Edge para sitios que requieran un explorador moderno.

Si habilita esta Directiva, el BHO no se instalará. Si ya está instalado, se desinstalará en la próxima actualización de Microsoft Edge.

Si esta Directiva no se configura o se deshabilita, se instalará el BHO.

El BHO es necesario para que se produzca la redirección no compatible del sitio, pero el hecho de que se produzca el redireccionamiento también lo controla [RedirectSitesFromInternetExplorerRedirectMode](#redirectsitesfrominternetexplorerredirectmode).

Para obtener más información sobre esta Directiva, vea [https://go.microsoft.com/fwlink/?linkid=2141715](https://go.microsoft.com/fwlink/?linkid=2141715)

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RedirectSitesFromInternetExplorerPreventBHOInstall
  - Nombre de GP: Evite la instalación del BHO para redirigir sitios incompatibles de Internet Explorer a Microsoft Edge.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombrel del valor: RedirectSitesFromInternetExplorerPreventBHOInstall
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```

  

  [Volver al principio](#microsoft-edge---policies)

  ### RedirectSitesFromInternetExplorerRedirectMode

  #### Redirigir los sitios incompatibles de Internet Explorer a Microsoft Edge.

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 87 o posterior

  #### Descripción

  Esta configuración le permite especificar si Internet Explorer va a redirigir las navegaciones a los sitios que requieran un explorador moderno para Microsoft Edge.

Si no configura esta Directiva o la configura en "sitelist", comenzando en M87, Internet Explorer redirigirá los sitios que requieran un explorador moderno a Microsoft Edge.

Microsoft proporciona una lista de sitios públicos que requieren el redireccionamiento, como https://mail.yahoo.com.

Cuando se redirige un sitio de Internet Explorer a Microsoft Edge, la pestaña de Internet Explorer que comenzó a cargar el sitio se cierra si no tenía contenido anterior. En caso contrario, se desplazará hasta una página de ayuda de Microsoft en la que se explica por qué el sitio se redirigió a Microsoft Edge.

Cuando se inicia Microsoft Edge para cargar un sitio desde Internet Explorer, se muestra una barra de información en la que se explica que el sitio funciona mejor en un explorador moderno.

Si establece esta directiva en "Deshabilitar", Internet Explorer no redirige el tráfico a Microsoft Edge.

Para obtener más información sobre esta Directiva, vea  [https://go.microsoft.com/fwlink/?linkid=2141715](https://go.microsoft.com/fwlink/?linkid=2141715)

Asignación de opciones de directiva:

* Disable (0) = deshabilitar

* Sitelist (1) = redirigir sitios basados en los sitios no compatibles sitelist

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RedirectSitesFromInternetExplorerRedirectMode
  - Nombre de GP: Redirigir automáticamente los sitios incompatibles de Internet Explorer a Microsoft Edge.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre de valor: RedirectSitesFromInternetExplorerRedirectMode
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```

  

  [Volver al principio](#microsoft-edge---policies)

  ### RelaunchNotification

  #### Notifique a un usuario que es recomendable reiniciar el explorador, o es necesario para actualizaciones pendientes

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Notifica a los usuarios que deben reiniciar Microsoft Edge para aplicar una actualización pendiente.

Si no configura esta directiva, Microsoft Edge agregará un icono de reciclaje en la parte superior derecha de la barra de menús, para pedir a los usuarios que reinicien el explorador para aplicar la actualización.

Si habilita esta directiva y la establece como "Recomendada" (1), una advertencia recurrente indicará a los usuarios una recomendación de reinicio. Los usuarios pueden ignorar esta advertencia y posponer el reinicio.

Si se establece la directiva como "Requerida", una advertencia recurrente indicará a los usuarios que el navegador se reiniciará automáticamente tan pronto como transcurra un período de notificación. El período predeterminado es de siete días. Puede configurar este período con la directiva [RelaunchNotificationPeriod](#relaunchnotificationperiod).

La sesión del usuario se restaurará al reiniciar el explorador.

Asignación de opciones de directiva:

* Recomendada (1) = recomendada: mostrar un aviso recurrente al usuario en el que se recomienda realizar un reinicio.

* Requerida (2) = requerida: mostrar un aviso recurrente al usuario para indicar que es necesario reiniciar.

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RelaunchNotification
  - Nombre de GP: notificar al usuario que se recomienda o se requiere el reinicio del navegador para realizar las actualizaciones pendientes
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: RelaunchNotification
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: RelaunchNotification
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### RelaunchNotificationPeriod

  #### Establezca el período de tiempo de las notificaciones de actualización

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite establecer el período de tiempo, en milisegundos, en el que se notifica a los usuarios que Microsoft Edge debe ser relanzado para aplicar una actualización pendiente.

Durante este período de tiempo, se le informará repetidamente al usuario sobre la necesidad de una actualización. En el caso de Microsoft Edge, el menú de la aplicación cambia para indicar que es necesario realizar un reinicio cuando se supera un tercio del período de notificación. Esta notificación cambia de color una vez que se supera el período de notificación, y vuelve a ocurrir después de que transcurre el período de notificación completo. Las notificaciones adicionales habilitadas por la directiva [RelaunchNotification](#relaunchnotification) siguen la misma programación.

Si no se establece, se usa el período predeterminado de 604,8 millones de milisegundos (una semana).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RelaunchNotificationPeriod
  - Nombre de GP: establecer el período de tiempo de las notificaciones de actualización
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: RelaunchNotificationPeriod
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x240c8400
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: RelaunchNotificationPeriod
  - Valor de ejemplo:
``` xml
<integer>604800000</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### RendererCodeIntegrityEnabled

  #### Habilitar integridad de código de representador

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 78 o posterior

  #### Descripción

  Si esta directiva está habilitada o sin establecer, entonces la integridad del código de presentación estará habilitada. Esta directiva sólo debe desactivarse si se produce algún problema de compatibilidad con un software de terceros que deba ejecutarse dentro de los procesos de representación de Microsoft Edge.

Si se deshabilita esta directiva, la seguridad y la estabilidad de Microsoft Edge se verán perjudicadas, ya que se permitirá que se cargue código desconocido y potencialmente hostil en los procesos de representación de Microsoft Edge.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RendererCodeIntegrityEnabled
  - Nombre de GP: habilitar la integridad de código del representador
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: RendererCodeIntegrityEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### RequireOnlineRevocationChecksForLocalAnchors

  #### Especifique si se necesitan comprobaciones OCSP/CRL en línea para los anclajes de veracidad local

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 77 o posterior

  #### Descripción

  Controla la solicitud de las comprobaciones de revocación en línea (comprobaciones OCSP/CRL). Si Microsoft Edge no puede obtener información sobre el estado de la revocación, estos certificados se considerarán revocados ("error no recuperable").

Si habilita esta directiva, Microsoft Edge siempre realizará una comprobación de la revocación de los certificados del servidor que se hayan validado correctamente y estén firmados por certificados de CA instalados de forma local.

Si no configura o deshabilita esta directiva, entonces Microsoft Edge usará la configuración de comprobación de revocación en línea existente.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RequireOnlineRevocationChecksForLocalAnchors
  - Nombre de GP: especificar si se requieren comprobaciones OCSP/CRL en línea para los anclajes de veracidad locales
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: RequireOnlineRevocationChecksForLocalAnchors
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### ResolveNavigationErrorsUseWebService

  #### Habilite la resolución de errores de navegación con un servicio Web

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Permite que Microsoft Edge emita una conexión sin datos a un servicio web para sondear las redes en busca de conectividad que se encuentra en lugares como hoteles y aeropuertos con Wi-Fi.

Si habilita esta directiva, se utilizará un servicio web para las pruebas de conectividad de la red.

Si desactiva esta directiva, Microsoft Edge usará las API nativas para intentar resolver los problemas de navegación y conectividad de red.

**Nota**: A excepción de Windows 8 y las versiones posteriores de Windows, Microsoft Edge *siempre* usará las API nativas para resolver los problemas de conectividad.

Si no configura esta directiva, Microsoft Edge respetará la preferencia de usuario establecida en Servicios en Edge://configuración/privacidad.
Específicamente, hay un botón de alternancia **Usar un servicio web para ayudar a resolver errores de navegación**, que el usuario puede activar o desactivar. Tenga en cuenta que si ha habilitado esta directiva (ResolveNavigationErrorsUseWebService), la opción **Usar un servicio web para ayudar a resolver los errores de navegación** estará activada, pero el usuario no podrá cambiar la opción con el botón de alternancia. Si ha deshabilitado esta directiva, la configuración **Usar un servicio web para ayudar a resolver los errores de navegación** se desactivará y el usuario no podrá cambiar la configuración con el botón de alternancia.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ResolveNavigationErrorsUseWebService
  - Nombre de GP: habilitar la resolución de errores de navegación con un servicio Web
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: ResolveNavigationErrorsUseWebService
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ResolveNavigationErrorsUseWebService
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### RestrictSigninToPattern

  #### Restrinja las cuentas que se pueden usar como cuentas de Microsoft Edge principal

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Determina qué cuentas pueden establecerse como cuentas primarias del explorador en Microsoft Edge (es decir, la cuenta que se elige durante el flujo de confirmación de la sincronización).

Si un usuario intenta configurar una cuenta principal para el explorador con un nombre de usuario que no coincida con este patrón, se bloqueará y verá el mensaje de error correspondiente. Puede configurar esta directiva para que coincida con varias cuentas mediante una expresión regular de estilo Perl para el patrón. Tenga en cuenta que las coincidencias de patrón distinguen mayúsculas de minúsculas. Para obtener más información sobre las reglas de expresión regular que se usan, consulte https://go.microsoft.com/fwlink/p/?linkid=2133903.

Si no se configura esta directiva o la deja en blanco, los usuarios podrán configurar cualquier cuenta como la cuenta principal del explorador en Microsoft Edge.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RestrictSigninToPattern
  - Nombre de GP: restringir qué cuentas pueden ser usadas como cuentas principales de Microsoft Edge
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: RestrictSigninToPattern
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
".*@contoso.com"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: RestrictSigninToPattern
  - Valor de ejemplo:
``` xml
<string>.*@contoso.com</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### RoamingProfileLocation

  #### Configurar el directorio de perfiles móviles

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 85 o posterior

  #### Descripción

  Configura el directorio que se usará para almacenar la copia de perfiles móviles de.

Si habilita esta Directiva, Microsoft Edge usa el directorio proporcionado para almacenar una copia de los perfiles en itinerancia, siempre y cuando haya habilitado también la Directiva [RoamingProfileSupportEnabled](#roamingprofilesupportenabled). Si deshabilita la Directiva de [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) o no la configura, el valor almacenado en esta Directiva no se usa.

Para obtener una lista de las variables que puede usar, vea [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Si no configura esta Directiva, se usará la ruta de acceso del perfil móvil predeterminado.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RoamingProfileLocation
  - Nombre de la Directiva de Grupo: establecer el directorio del perfil móvil
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: RoamingProfileLocation
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"${roaming_app_data}\\edge-profile"
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### RoamingProfileSupportEnabled

  #### Permitir el uso de copias móviles para datos de Perfil de Microsoft Edge

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 85 o posterior

  #### Descripción

  Habilite esta directiva para usar perfiles móviles en Windows. La configuración almacenada en perfiles de Microsoft Edge (favoritos y preferencias) también se guarda en un archivo almacenado en la carpeta de Perfil de usuario móvil (o en la ubicación especificada por el administrador mediante la Directiva de [RoamingProfileLocation](#roamingprofilelocation)).

Si deshabilita esta Directiva o no la configura, solo se usarán los perfiles locales habituales.

La Directiva [SyncDisabled](#syncdisabled) deshabilita toda la sincronización de datos y suplanta la Directiva.

Consulte https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles para obtener más información sobre el uso de perfiles de usuario móviles.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RoamingProfileSupportEnabled
  - Nombre GP: habilitar el uso de copias móviles para datos de Perfil de Microsoft Edge
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: RoamingProfileSupportEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### RunAllFlashInAllowMode

  #### Extienda la configuración de contenido de Adobe Flash a todo el contenido

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Si habilita esta directiva, se ejecutará todo el contenido de Adobe Flash incrustado en los sitios web que estén configurados para permitir Adobe Flash en la configuración del contenido, ya sea por el usuario o por la directiva de la empresa. Esto incluye el contenido reducido o de otros orígenes.

Para controlar qué sitios web están autorizados para ejecutar Adobe Flash, vea las especificaciones en las directivas [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls) y [PluginsBlockedForUrls](#pluginsblockedforurls).

Si deshabilita o no configura esta directiva, es posible que el contenido de Adobe Flash, de otros orígenes (de sitios que no se especifican en las tres directivas mencionadas anteriormente) o el contenido reducido sea bloqueado.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: RunAllFlashInAllowMode
  - Nombre de GP: extender la configuración de contenido de Adobe Flash a todo el contenido
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: RunAllFlashInAllowMode
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: RunAllFlashInAllowMode
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SSLErrorOverrideAllowed

  #### Permita que los usuarios continúen desde la página de advertencia HTTPS

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Microsoft Edge muestra una página de advertencia cuando los usuarios visitan sitios con errores de SSL.

Si habilita o no configura (por defecto) esta directiva, los usuarios podrán hacer clic en estas páginas de advertencia.

Si deshabilita esta directiva, se bloqueará a los usuarios para que no puedan hacer clic en ninguna página de advertencia.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SSLErrorOverrideAllowed
  - Nombre de GP: permitir que los usuarios continúen desde la página de advertencia de HTTPS
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: SSLErrorOverrideAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SSLErrorOverrideAllowed
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SSLVersionMin

  #### Versión de TLS mínima activada

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Sets the minimum supported version of TLS. Si no configura esta directiva, Microsoft Edge usará una versión mínima predeterminada, TLS 1.0.

If you enable this policy, Microsoft Edge won't use any version of SSL/TLS lower than the specified version. Los valores no reconocidos serán ignorados.

Asignación de opciones de directiva:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SSLVersionMin
  - Nombre de GP: versión mínima de TLS activada
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: SSLVersionMin
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"tls1"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SSLVersionMin
  - Valor de ejemplo:
``` xml
<string>tls1</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SaveCookiesOnExit

  #### Guardar cookies cuando se cierra Microsoft Edge

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Cuando esta directiva está habilitada, el conjunto de cookies especificado no se eliminará cuando se cierre el explorador. Esta directiva solo surte efecto cuando:
- El botón de alternancia en Configuración/Privacidad "Cookies y otros datos de sitio" está configurado y servicios/Borrar datos de exploración está cerrado o
- La directiva [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) se habilita o
- La directiva [DefaultCookiesSetting](#defaultcookiessetting) se configura como "Mantener cookies durante toda la sesión".

Puede definir una lista de sitios, basándose en modelos URL en los que se conservarán sus cookies durante las sesiones.

Nota: los usuarios todavía podrán editar la lista de sitios de cookies para agregar o quitar las URL. Sin embargo, no podrán quitar las direcciones URL que haya agregado un administrador.

Si habilita esta directiva, la lista de cookies no se eliminará cuando se cierre el explorador.

Si deshabilita o no configura esta directiva, se usará la configuración personal del usuario.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SaveCookiesOnExit
  - Nombre GP: guardar cookies cuando se cierra Microsoft Edge
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta (obligatoria): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: SaveCookiesOnExit
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SavingBrowserHistoryDisabled

  #### Deshabilitar la opción pada guardar el historial del explorador

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Deshabilita la opción de guardar el historial del explorador y evita que los usuarios cambien esta configuración.

Si habilita esta directiva, el historial de exploración no se guardará. Esto también deshabilita la sincronización de las pestañas.

Si deshabilita o no configura esta directiva, se guardará el historial de exploración.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SavingBrowserHistoryDisabled
  - Nombre de GP: deshabilitar la opción para guardar el historial del explorador
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: SavingBrowserHistoryDisabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SavingBrowserHistoryDisabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ScreenCaptureAllowed

  #### Permitir o denegar captura de pantalla

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 83 o posterior

  #### Descripción

  Si habilita o no configura esta directiva, una página web podría utilizar las API de uso compartido de pantalla (por ejemplo, getDisplayMedia() o la API de la extensión Desktop Capture) para realizar una captura de pantalla.
Si deshabilita esta directiva, las llamadas a las API de uso compartido de pantalla fallarán. Por ejemplo, si está usando una reunión en línea basada en web, no funcionará el uso compartido de video o pantalla.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ScreenCaptureAllowed
  - Nombre de GP: permitir o denegar la captura de pantalla
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ScreenCaptureAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ScreenCaptureAllowed
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ScrollToTextFragmentEnabled

  #### Habilite el desplazamiento al texto especificado en fragmentos de URL

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 83 o posterior

  #### Descripción

  Esta característica permite que los hipervínculos y la navegación de la barra de direcciones URL se dirijan hacia un texto específico en una página web, al que se desplazará una vez que la página web termine de cargarse.

Si habilita o no configura esta directiva, se habilitará el desplazamiento de la página web hacia determinados fragmentos de texto a través de una dirección URL.

Si deshabilita esta directiva, también se deshabilitará el desplazamiento de la página web hacia determinados fragmentos de texto a través de una dirección URL.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ScrollToTextFragmentEnabled
  - Nombre de GP: habilitar el desplazamiento de texto especificado en los fragmentos de URL
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ScrollToTextFragmentEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ScrollToTextFragmentEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SearchSuggestEnabled

  #### Permitir sugerencias de búsqueda

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilita las sugerencias de búsqueda web en la barra de direcciones de Microsoft Edge y en la lista de auto-sugerencias e impide que los usuarios cambien esta directiva.

Si habilita esta directiva, se usarán las sugerencias de búsqueda web.

Si deshabilita esta directiva, las sugerencias de búsqueda web nunca se usarán, aunque el historial local y las sugerencias locales de los favoritos seguirán apareciendo. Si deshabilita esta directiva, no se incluirán en la telemetría de Microsoft ni los caracteres escritos ni las direcciones URL que visite.

Si no se establece esta directiva, se habilitarán las sugerencias de búsqueda, sin embargo, el usuario podrá cambiarlas.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SearchSuggestEnabled
  - Nombre de GP: permitir las sugerencias de búsqueda
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: SearchSuggestEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SearchSuggestEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SecurityKeyPermitAttestation

  #### Sitios web o dominios que no necesitan permiso para usar la atestación de clave de seguridad directa

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especifica los sitios web y los dominios que no necesitan un permiso explícito del usuario al solicitar los certificados de atestación de las claves de seguridad. Además, se envía una señal a la clave de seguridad para indicar que puede usar la atestación individual. Sin esto, se le pedirá a los usuarios cada vez que un sitio solicite una consulta para la atestación de las claves de seguridad.

Sitios (como https://contoso.com/some/path) solo coinciden con U2F appIDs. Los dominios (como contoso.com) solo coinciden como ID. de webauthn RP. Para cubrir tanto las API de U2F como de webauthn en un sitio determinado, es necesario enumerar tanto la dirección URL de la aplicación como el dominio.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SecurityKeyPermitAttestation
  - Nombre de GP: sitios web o dominios que no necesitan permiso para usar la atestación directa de la clave de seguridad
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\SecurityKeyPermitAttestation
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SecurityKeyPermitAttestation
  - Valor de ejemplo:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SendIntranetToInternetExplorer

  #### Enviar todos los sitios de intranet a Internet Explorer

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 77 o posterior

  #### Descripción

  Para obtener instrucciones sobre cómo configurar la experiencia óptima en el modo de Internet Explorer, vea [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SendIntranetToInternetExplorer
  - Nombre de GP: enviar todos los sitios de intranet a Internet Explorer
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: SendIntranetToInternetExplorer
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### SendSiteInfoToImproveServices

  #### Enviar información de sitios para mejorar los servicios Microsoft (en desuso)

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Esta directiva está en desuso. Actualmente, se admite pero quedará obsoleto en Microsoft Edge 89. Esta directiva se reemplaza por la nueva directiva: [DiagnosticData](#diagnosticdata)para Windows 7, Windows 8 y macOS. Esta directiva se ha reemplazado por Permitir telemetría en Windows 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Esta directiva permite enviar información a Microsoft acerca de los sitios web visitados en Microsoft Edge para mejorar servicios como la búsqueda.

Habilite esta directiva para enviar información a Microsoft acerca de los sitios web visitados en Microsoft Edge. Deshabilite esta directiva para no enviar información a Microsoft acerca de los sitios web visitados en Microsoft Edge. En ambos casos, los usuarios no pueden cambiar ni invalidar la configuración.

En Windows 10, si no se configura esta directiva, Microsoft Edge se ajustará por defecto a la configuración de datos de diagnóstico de Windows. Si esta directiva está habilitada, Microsoft Edge sólo enviará información sobre los sitios web visitados desde Microsoft Edge si la configuración de datos de diagnóstico de Windows está establecida como Completa Si esta directiva está deshabilitada, Microsoft Edge no enviará información acerca de los sitios web visitados. Obtenga más información acerca de la configuración de datos de diagnóstico de Windows en: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Esta directiva controla el envío de información sobre los sitios web visitados en Windows 7, Windows 8 y macOS. Si no configura esta directiva, Microsoft Edge se ajustará de forma predeterminada a las preferencias del usuario.

Para habilitar esta directiva, debe establecer [MetricsReportingEnabled](#metricsreportingenabled) como habilitado. Si [MetricsReportingEnabled](#sendsiteinfotoimproveservices) o [SendSiteInfoToImproveServices](#metricsreportingenabled) no se configura o se deshabilita, estos datos no se enviarán a Microsoft.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SendSiteInfoToImproveServices
  - Nombre GP: enviar información de sitios para mejorar los servicios Microsoft (en desuso)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: SendSiteInfoToImproveServices
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SendSiteInfoToImproveServices
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SensorsAllowedForUrls

  #### Permitir el acceso a sensores en sitios específicos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Definir una lista de sitios, basándose en patrones de dirección URL, que puedan acceder a sensores —como sensores de luz y de movimiento— y usarlos.

Si no configura esta directiva se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultSensorsSetting](#defaultsensorssetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

Para los patrones de dirección URL que no coincidan con esta directiva, se emplea el siguiente orden de prioridad: la directiva [SensorsBlockedForUrls](#sensorsblockedforurls) (si hay una coincidencia), la directiva [DefaultSensorsSetting](#defaultsensorssetting) (si se establece) o la configuración personal del usuario.

Los patrones de dirección URL definidos en esta directiva no pueden entrar en conflicto con aquellos configurados en la directiva [SensorsBlockedForUrls](#sensorsblockedforurls). No puede permitir y bloquear una dirección URL.

Para información detallada sobre los patrones de dirección URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SensorsAllowedForUrls
  - Nombre de GP: Permitir el acceso a sensores en sitios específicos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\SensorsAllowedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SensorsAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SensorsBlockedForUrls

  #### Bloquear el acceso a sensores en sitios específicos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Definir una lista de sitios, basándose en patrones de dirección URL, que no puedan acceder a sensores, tales como sensores de luz y de movimiento.

Si no configura esta directiva se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultSensorsSetting](#defaultsensorssetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

Para los patrones de dirección URL que no coincidan con esta directiva, se emplea el siguiente orden de prioridad: la directiva [SensorsAllowedForUrls](#sensorsallowedforurls) (si hay una coincidencia), la directiva [DefaultSensorsSetting](#defaultsensorssetting) (si se establece) o la configuración personal del usuario.

Los patrones de dirección URL definidos en esta directiva no pueden entrar en conflicto con aquellos configurados en la directiva [SensorsAllowedForUrls](#sensorsallowedforurls). No puede permitir y bloquear una dirección URL.

Para información detallada sobre los patrones de dirección URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SensorsBlockedForUrls
  - Nombre de GP: Bloquear el acceso a sensores en sitios específicos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\SensorsBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de las preferencias: SensorsBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SerialAskForUrls

  #### Permitir la API de serie en sitios específicos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Define una lista de sitios basada en patrones de dirección URL que pueden solicitar al usuario acceso a un puerto serie.

Si no configura esta directiva se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultSerialGuardSetting](#defaultserialguardsetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

Para los patrones de dirección URL que no coincidan con esta directiva, se emplea el siguiente orden de prioridad: la directiva [SerialBlockedForUrls](#serialblockedforurls) (si hay una coincidencia), la directiva [DefaultSerialGuardSetting](#defaultserialguardsetting) (si se establece) o la configuración personal del usuario.

Los patrones de dirección URL definidos en esta directiva no pueden entrar en conflicto con aquellos configurados en la directiva [SerialBlockedForUrls](#serialblockedforurls). No puede permitir y bloquear una dirección URL.

Para información detallada sobre los patrones de dirección URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SerialAskForUrls
  - Nombre de GP: Permitir la API de serie en sitios específicos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\SerialAskForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SerialAskForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SerialBlockedForUrls

  #### Bloquear la API de serie en sitios específicos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Define una lista de sitios basada en patrones de dirección URL que no pueden solicitar al usuario acceso a un puerto serie.

Si no configura esta directiva se utilizará para todos los sitios el valor global predeterminado de la directiva [DefaultSerialGuardSetting](#defaultserialguardsetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

Para los patrones de dirección URL que no coincidan con esta directiva, se emplea el siguiente orden de prioridad: la directiva [SerialAskForUrls](#serialaskforurls) (si hay una coincidencia), la directiva [DefaultSerialGuardSetting](#defaultserialguardsetting) (si se establece) o la configuración personal del usuario.

Los patrones de dirección URL en esta directiva no pueden entrar en conflicto con los configurados en la directiva [SerialAskForUrls](#serialaskforurls). No puede permitir y bloquear una dirección URL.

Para información detallada sobre los patrones de dirección URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SerialBlockedForUrls
  - Nombre de GP: Bloquear la API de serie en sitios específicos
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge\SerialBlockedForUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SerialBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### ShowOfficeShortcutInFavoritesBar

  #### Mostrar el acceso directo de Microsoft Office en la barra de favoritos (en desuso)

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Esta directiva no funcionaba como se esperaba debido a cambios en los requisitos operativos. Por lo tanto, está en desuso y no debería utilizarse.

Especifica si se va a incluir un método abreviado para Office.com en la barra de favoritos. Para los usuarios que iniciaron sesión en Microsoft Edge, el método abreviado lleva a los usuarios a sus aplicaciones y documentos de Microsoft Office. Si habilita o no configura esta directiva, los usuarios pueden elegir si ven el método abreviado de teclado cambiando el botón de alternancia en el menú contextual de la barra de favoritos.
Si deshabilita esta directiva, el método abreviado no se muestra.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: ShowOfficeShortcutInFavoritesBar
  - Nombre de GP: mostrar el acceso directo de Microsoft Office en la barra de favoritos (en desuso)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: ShowOfficeShortcutInFavoritesBar
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: ShowOfficeShortcutInFavoritesBar
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SignedHTTPExchangeEnabled

  #### Habilite la compatibilidad con el intercambio de HTTP firmado (SXG)

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Habilita la compatibilidad con el Intercambio firmado de HTTP (SXG).

Si no se establece o habilita esta directiva, Microsoft Edge aceptará el contenido web que sirva como intercambios firmados de HTTP.

Si esta directiva está deshabilitada, los intercambios firmados por HTTP no podrán ser cargados.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SignedHTTPExchangeEnabled
  - Nombre de GP: habilitar la compatibilidad con el intercambio firmado de HTTP (SXG)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: SignedHTTPExchangeEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SignedHTTPExchangeEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SitePerProcess

  #### Habilite el aislamiento de sitio para cada sitio

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  La directiva "SitePerProcess" puede ser usada para evitar que los usuarios opten por el comportamiento predeterminado de aislar todos los sitios. Tenga en cuenta que también puede usar la directiva [IsolateOrigins](#isolateorigins) para aislar orígenes adicionales más precisos.

Si habilita esta directiva, los usuarios no podrán optar por el comportamiento predeterminado donde cada sitio se ejecuta en su propio proceso.

Si deshabilita o no configura esta directiva, el usuario podrá optar por no recibir el aislamiento del sitio.  (Por ejemplo, con la entrada "deshabilitar aislamiento de sitio" en edge://flags.)  Si deshabilita o no configura la directiva, no se desactivará el aislamiento de sitio.


  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SitePerProcess
  - Nombre de GP: habilitar el aislamiento de sitio en cada uno de los sitios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: SitePerProcess
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SitePerProcess
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SpeechRecognitionEnabled

  #### Configure Speech Recognition

  
  
  #### Versiones compatibles:

  - On Windows and macOS since 87 or later

  #### Descripción

  Set whether websites can use the W3C Web Speech API to recognize speech from the user. The Microsoft Edge implementation of the Web Speech API uses Azure Cognitive Services, so voice data will leave the machine.

If you enable or don't configure this policy, web-based applications that use the Web Speech API can use Speech Recognition.

If you disable this policy, Speech Recognition is not available through the Web Speech API.

Read more about this feature here: SpeechRecognition API: [https://go.microsoft.com/fwlink/?linkid=2143388](https://go.microsoft.com/fwlink/?linkid=2143388) Cognitive Services: [https://go.microsoft.com/fwlink/?linkid=2143680](https://go.microsoft.com/fwlink/?linkid=2143680)

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - GP unique name: SpeechRecognitionEnabled
  - GP name: Configure Speech Recognition
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Value Name: SpeechRecognitionEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```

  #### Información y configuración de Mac
  
  - Preference Key Name: SpeechRecognitionEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SpellcheckEnabled

  #### Habilite corrección ortográfica

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Si habilita o no configura esta directiva, el usuario podrá usar la revisión ortográfica.

Si deshabilita esta directiva, el usuario no podrá usar la revisión ortográfica y las directivas [SpellcheckLanguage](#spellchecklanguage) y [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) también estarán deshabilitadas.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SpellcheckEnabled
  - Nombre de GP: habilitar la corrección ortográfica
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: SpellcheckEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SpellcheckEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SpellcheckLanguage

  #### Habilite idiomas de revisión ortográfica específicos

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 77 o posterior

  #### Descripción

  Habilita varios idiomas para la revisión ortográfica. Cualquier idioma especificado que no sea reconocido será omitido

Si habilita esta directiva, el corrector ortográfico estará habilitado para los idiomas especificados, así como para cualquier idioma que el usuario haya habilitado.

Si no configura o deshabilita esta política, no se realizarán los cambios necesarios en las preferencias de revisión ortográfica del usuario.

Si la directiva [SpellcheckEnabled](#spellcheckenabled) está deshabilitada, esta directiva no tendrá ningún efecto.

Si se incluye un idioma tanto en la directiva de "SpellcheckLanguage" como en la de [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist), se habilitará el idioma de revisión ortográfica.

Los idiomas admitidos son: af, bg, ca, cs, cy, da, de, el, en - AU, en - CA, en - GB, en - US, es, es - 419, es - AR, es - ES, es - MX, es - US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt - BR, pt - PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SpellcheckLanguage
  - Nombre de GP: habilitar los idiomas específicos de la revisión ortográfica
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [Volver al principio](#microsoft-edge---policies)

  ### SpellcheckLanguageBlocklist

  #### Forzar deshabilitar idioma de revisión ortográfica

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 78 o posterior

  #### Descripción

  Deshabilitar de forma forzada los lenguajes de revisión ortográfica. Los idiomas no reconocidos en la lista se omitirán.

Si habilita esta directiva, la revisión ortográfica se deshabilitará en los idiomas especificados. El usuario aún podrá habilitar o deshabilitar la revisión ortográfica para los idiomas que no estén en la lista.

Si deshabilita o no establece esta directiva, no se realizará ningún cambio en las preferencias de revisión ortográfica del usuario.

Si la directiva [SpellcheckEnabled](#spellcheckenabled) se establece como deshabilitada, esta directiva no tendrá ningún efecto.

Si se incluye un idioma en alguna de las directivas [SpellcheckLanguage](#spellchecklanguage) y "SpellcheckLanguageBlocklist", se habilitará el idioma de la revisión ortográfica.

Los idiomas admitidos son: af, bg, ca, cs, da, de, el, en - AU, en - CA, en - GB, en - US, es, es - 419, es - AR, es - ES, es - MX, es - US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt - BR, pt - PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SpellcheckLanguageBlocklist
  - Nombre de GP: Forzar la inhabilitación del idioma de revisión ortográfica
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [Volver al principio](#microsoft-edge---policies)

  ### StricterMixedContentTreatmentEnabled

  #### Permitir el tratamiento más estricto de contenido mixto (en desuso)

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 81 o posterior

  #### Descripción

  Esta directiva está en desuso porque solo pretende ser un mecanismo a corto plazo para dar a las empresas más tiempo para actualizar su contenido web cuando se ha comprobado que es incompatible con el tratamiento de contenido mixto más estricto. No funciona en la versión 85 de Microsoft Edge.

Esta directiva controla el tratamiento para contenido mixto (contenido HTTP en sitios HTTPS) en el explorador.

Si establece esta directiva como verdadera o no establecida, el contenido mixto de audio y vídeo se actualizará automáticamente a HTTPS (es decir, la dirección URL se reescribirá como HTTPS, sin una reserva cuando el recurso no esté disponible a través de HTTPS) y se mostrará una advertencia de "no seguro" en la barra de direcciones URL para el contenido mixto de imágenes.

Si establece la directiva como falsa, se deshabilitarán las actualizaciones automáticas para audio y vídeo, y no se mostrará ninguna advertencia sobre las imágenes.

Esta directiva no afecta otros tipos de contenido mixto que no sean audio, vídeo e imágenes.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: StricterMixedContentTreatmentEnabled
  - Nombre de DG: permitir el tratamiento más estricto de contenido mixto (en desuso)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: StricterMixedContentTreatmentEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: StricterMixedContentTreatmentEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SuppressUnsupportedOSWarning

  #### Suprimir la advertencia de SO no compatible

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Suprime la advertencia que aparece al ejecutar Microsoft Edge en un equipo o sistema operativo que ya no sea compatible.

Si esta directiva tiene un valor falso o no está establecido, las advertencias aparecerán en los equipos o sistemas operativos que no sean compatibles.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SuppressUnsupportedOSWarning
  - Nombre de GP: suprimir la advertencia de SO no compatible
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: SuppressUnsupportedOSWarning
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SuppressUnsupportedOSWarning
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SyncDisabled

  #### Deshabilitar la sincronización de datos con servicios de sincronización de Microsoft

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Deshabilita la sincronización de datos en Microsoft Edge. Esta directiva también evita que se muestren solicitudes de consentimiento de sincronización.

Si no establece o aplica esta directiva como se recomienda, los usuarios podrán activar o desactivar la sincronización. Si aplica esta directiva como obligatoria, los usuarios no podrán activar la sincronización.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SyncDisabled
  - Nombre de GP: deshabilitar la sincronización de datos con servicios de sincronización de Microsoft
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: SyncDisabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SyncDisabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### SyncTypesListDisabled

  #### Configurar la lista de tipos que se excluyen de la sincronización

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde la versión 83 o posterior

  #### Descripción

  Si habilita esta directiva, todos los tipos de datos especificados se excluirán de la sincronización. Esta directiva se puede usar para restringir el tipo de datos cargados en el servicio de sincronización de Microsoft Edge.

Puede proporcionar uno de los siguientes tipos de datos para esta directiva: "favoritos", "configuración", "contraseñas", "addressesAndMore", "extensiones", "historial", "openTabs" y "colecciones". Observe que los nombres de estos tipos de datos distinguen mayúsculas de minúsculas.

Los usuarios no podrán reemplazar los tipos de datos deshabilitados.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: SyncTypesListDisabled
  - Nombre de GP: configurar la lista de tipos que están excluidos de la sincronización.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\SyncTypesListDisabled
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: SyncTypesListDisabled
  - Valor de ejemplo:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### TLS13HardeningForLocalAnchorsEnabled

  #### Habilitar una característica de seguridad TLS 1.3 para los anclajes de veracidad locales (en desuso)

  
  >OBSOLETA: Esta directiva está obsoleta y no funciona después de Microsoft Edge 85.
  #### Versiones compatibles:

  - En Windows y MacOS, desde la versión 81 hasta la versión 85

  #### Descripción

  Esta directiva está en desuso, ya que solo pretende ser un mecanismo a corto plazo para dar a las empresas más tiempo para actualizar los proxis afectados.

Esta directiva controla una característica de seguridad de TLS 1,3 que protege las conexiones frente a ataques de degradación. Es compatible con las versiones anteriores y no afectará las conexiones a los servidores o proxies TLS 1,2 compatibles. Sin embargo, las versiones anteriores de algunos proxies que interceptan TLS tienen un error de implementación, lo que hace que sean incompatibles.

Si deshabilita esta directiva o no la configura, Microsoft Edge habilitará estas protecciones de seguridad en todas las conexiones.

Si deshabilita esta directiva, Microsoft Edge deshabilitará estas protecciones de seguridad en las conexiones autenticadas instaladas localmente con certificados de CA. Estas protecciones siempre están habilitadas en las conexiones autenticadas con certificados de entidad de confianza pública.

Se puede usar esta directiva para comprobar los proxis afectados y actualizarlos. Se espera que los servidores afectados den error en las conexiones con el código de error: ERR_TLS13_DOWNGRADE_DETECTED.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: TLS13HardeningForLocalAnchorsEnabled
  - Nombre GP: habilitar una característica de seguridad TLS 1.3 para los anclajes de veracidad locales (en desuso)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: TLS13HardeningForLocalAnchorsEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: TLS13HardeningForLocalAnchorsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### TLSCipherSuiteDenyList

  #### Especificar los conjuntos de cifrado TLS para deshabilitarlos

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 85 o posterior

  #### Descripción

  Configure la lista de conjuntos de cifrado que se deshabilitan en conexiones TLS.

Si configura esta Directiva, la lista de conjuntos de cifrado configurados no se usará al establecer conexiones TLS.

Si no configura esta Directiva, el explorador elegirá los conjuntos de cifrado TLS que se usarán.

Los valores del conjunto de cifrado que se van a deshabilitar se especifican como valores hexadecimales de 16 bits. Los valores los asigna el registro autoridad de números asignados de Internet (IANA).

La TLS_AES_128_GCM_SHA256 del conjunto de cifrado TLS 1,3 (0x1301) es necesaria para TLS 1,3 y no se puede deshabilitar por esta Directiva.

Esta Directiva no afecta a las conexiones basadas en QUIC. QUIC puede apagarse a través de la Directiva de [QuicAllowed](#quicallowed).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: TLSCipherSuiteDenyList
  - Nombre de GP: especifique los conjuntos de cifrado TLS para deshabilitarlos.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: TLSCipherSuiteDenyList
  - Valor de ejemplo:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### TabFreezingEnabled

  #### Permitir el bloqueo de las pestañas en segundo plano

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 79 o posterior

  #### Descripción

  Controla si Microsoft Edge puede congelar las pestañas que están en segundo plano durante al menos 5 minutos.

Al congelar la pestaña se reduce el uso de la CPU, batería y memoria. Microsoft Edge usa la heurística para evitar congelar las pestañas que funcionan correctamente en segundo plano, como las notificaciones de pantalla, la reproducción de sonido y la transmisión de vídeo.

Si habilita o no configura esta directiva, las pestañas que han estado en segundo plano durante un mínimo de 5 minutos podrían ser congeladas.

Si desactiva esta directiva, no se congelarán las pestañas.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: TabFreezingEnabled
  - Nombre de GP: permitir el bloqueo de las pestañas en segundo plano
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: TabFreezingEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: TabFreezingEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### TaskManagerEndProcessEnabled

  #### Habilitar los procesos de finalización en el administrador de tareas del explorador

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Si habilita o no configura esta directiva, los usuarios podrán detener los procesos en el administrador de tareas del explorador. Si la deshabilita, los usuarios no podrán detener los procesos y el botón Detener proceso estará deshabilitado en el administrador de tareas del explorador.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: TaskManagerEndProcessEnabled
  - Nombre GP: habilitar los procesos finales en el administrador de tareas del explorador
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: TaskManagerEndProcessEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: TaskManagerEndProcessEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### TotalMemoryLimitMb

  #### Establecer el límite en megabytes de memoria que puede utilizar una única instancia de Microsoft Edge.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Configure la cantidad de memoria que una sola instancia de Microsoft Edge puede usar antes de que las pestañas empiecen a ser descartadas para ahorrar memoria. La memoria usada por la pestaña se liberará y la pestaña tendrá que volver a cargarse cuando se cambie a.

Si habilita esta directiva, el navegador comenzará a descartar las pestañas para ahorrar memoria una vez que se supere el límite. Sin embargo, no hay garantía de que el navegador siempre se ejecute por debajo del límite. Cualquier valor por debajo de 1024 se redondeará a 1024.

Si no establece esta directiva, el explorador solo intentará ahorrar memoria cuando haya detectado que la cantidad de memoria física de su equipo es insuficiente.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: TotalMemoryLimitMb
  - Nombre de GP: establecer el límite de megabytes de memoria que puede usar una sola instancia de Microsoft Edge.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: TotalMemoryLimitMb
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000800
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: TotalMemoryLimitMb
  - Valor de ejemplo:
``` xml
<integer>2048</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### TrackingPrevention

  #### Bloquear el seguimiento de la actividad de exploración de los usuarios en la web

  
  
  #### Versiones compatibles:

  - En Windows y macOS desde 78 o posterior

  #### Descripción

  Le permite decidir si desea bloquear el acceso a los sitios web que quieran rastrear la actividad de los usuarios.

Si deshabilita esta directiva o no la configura, los usuarios podrán establecer su propio nivel de prevención de rastreo.

Asignación de opciones de directiva:

* TrackingPreventionOff (0) = desactivado (sin prevención de rastreo)

* TrackingPreventionBasic (1) = básico (bloquea rastreadores malintencionados; el contenido y los anuncios será personalizados)

* TrackingPreventionBalanced (2) = equilibrado (bloquea rastreadores malintencionados y de sitios que el usuario no ha visitado; el contenido y los anuncios serán menos personalizados)

* TrackingPreventionStrict (3) = estricto (bloquea rastreadores malintencionados y la mayoría de los rastreadores de todos los sitios; el contenido y los anuncios tendrán una personalización mínima. Es posible que algunas partes de los sitios no funcionen)

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: TrackingPrevention
  - Nombre de GP: bloquear el seguimiento de la actividad de exploración de los usuarios en la web
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: TrackingPrevention
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000002
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: TrackingPrevention
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### TranslateEnabled

  #### Habilitar la traducción

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Habilita el servicio de traducción integrada de Microsoft en Microsoft Edge.

Si habilita esta directiva, Microsoft Edge ofrecerá la funcionalidad de traducción al usuario mostrándole un menú flotante integrado de traducción cuando sea necesario, y una opción para traducir en el menú contextual del botón derecho del ratón.

Al deshabilitar esta directiva también se deshabilitarán todas las características de traducción integradas.

Si no configura la directiva, los usuarios podrán elegir si desean usar la funcionalidad de traducción o no.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: sí
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: TranslateEnabled
  - Nombre de GP: habilitar la traducción
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendada): Plantillas administrativas/Microsoft Edge: configuración predeterminada (los usuarios pueden reemplazarla)
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendada): SOFTWARE\Directivas\Microsoft\Microsoft Edge\Recomendado
  - Nombre del valor: TranslateEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: TranslateEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### URLAllowlist

  #### Definir una lista de direcciones URL permitidas

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción
                    

  El establecimiento de la Directiva permite tener acceso a las direcciones URL indicadas, como excepciones para [URLBlocklist](#urlblocklist).

Aplique formato al modelo de dirección URL en función de [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Puede usar esta directiva para abrir excepciones a las listas de bloqueo restrictivas. Por ejemplo, puede incluir "*" en la lista de bloqueados para bloquear todas las solicitudes y, a continuación, usar esta directiva para permitir el acceso a una lista limitada de direcciones URL. Puede usar esta directiva para abrir excepciones para determinados esquemas, subdominios de otros dominios, puertos o rutas de acceso específicas.

El filtro más específico determina si una dirección URL está bloqueada o es permitida. La lista de permitidos tiene prioridad sobre la lista de bloqueados.

Esta directiva está limitada a 1000 entradas; las siguientes entradas se omiten.

Esta directiva también permite al explorador invocar automáticamente aplicaciones externas registradas como controladores de protocolo para protocolos como "tel:" o "ssh:".

Si no configura esta Directiva, no hay ninguna excepción a la lista de bloqueados en la Directiva [URLBlocklist](#urlblocklist).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: URLAllowlist
  - Nombre de GP: definir una lista de direcciones URL permitidas
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\URLAllowlist
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: URLAllowlist
  - Valor de ejemplo:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### URLBlocklist

  #### Bloquear el acceso a una lista de direcciones URL

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Define una lista de sitios basada en los patrones de dirección URL que están bloqueados (sus usuarios no pueden cargarlos).

Aplique formato al modelo de dirección URL en función de [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Puede definir excepciones en la directiva [URLAllowlist](#urlallowlist). Estas directivas están limitadas a 1000 entradas; las siguientes entradas se omiten.

Tenga en cuenta que no se recomienda bloquear las direcciones URL "edge://*" internas, lo que puede provocar errores inesperados.

Esta Directiva no impide que la página se actualice dinámicamente a través de JavaScript. Por ejemplo, si bloquea "contoso.com/abc", es posible que los usuarios sigan pudiendo visitar "contoso.com" y hacer clic en un vínculo para visitar "contoso.com/abc", siempre que la página no se actualice.

Si no configura esta Directiva, no se bloquea ninguna dirección URL.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: URLBlocklist
  - Nombre de GP: bloquear el acceso a una lista de direcciones URL
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\URLBlocklist
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\3 = "hosting.com/bad_path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\5 = ".exact.hostname.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\6 = "file://*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\7 = "custom_scheme:*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\8 = "*"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: URLBlocklist
  - Valor de ejemplo:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/bad_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
  <string>file://*</string>
  <string>custom_scheme:*</string>
  <string>*</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### UserAgentClientHintsEnabled

  #### Habilitar la característica User-Agent Client Hints (en desuso)

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 86 o posterior

  #### Descripción

  Esta directiva está en desuso porque solo pretende ser un mecanismo a corto plazo para dar a las empresas más tiempo para actualizar su contenido web cuando se compruebe que es incompatible con característica User-Agent Client Hints. No funciona en la versión 89 de Microsoft Edge.

Cuando se habilita la característica User-Agent Client Hints se envían encabezados de solicitud granulares que ofrecen información sobre el explorador del usuario (por ejemplo, la versión del explorador) y el entorno (por ejemplo, la arquitectura del sistema).

Esta es una característica aditiva, pero los nuevos encabezados pueden romper algunos sitios web que restringen los caracteres que pueden contener las solicitudes.

Si habilita o no configura esta directiva, se habilitará la característica User-Agent Client Hints. Si deshabilita esta directiva, esta característica no estará disponible.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: UserAgentClientHintsEnabled
  - Nombre GP: habilitar la característica User-Agent Client Hints (en desuso)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: UserAgentClientHintsEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: UserAgentClientHintsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### UserDataDir

  #### Establecer el directorio de datos del usuario

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Configure el directorio que se usará para almacenar los datos del usuario.

Si habilita esta directiva, Microsoft Edge usará el directorio especificado independientemente de si el usuario ha establecido el marcador de línea de comandos "--user-data-dir".

Si no habilita esta directiva, se usará la ruta de acceso predeterminada del perfil, aunque el usuario podrá anularla con el marcador "--user-data-dir". Los usuarios pueden encontrar el directorio del perfil en edge://versión/en ruta de acceso del perfil.

Para evitar la pérdida de datos u otros errores, no configure esta directiva en un directorio raíz de volumen o en un directorio que se use para otros propósitos, ya que Microsoft Edge administra su contenido.

Vea [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obtener una lista de las variables que se pueden usar.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: Actualización
  - Nombre de GP: establecer el directorio de datos del usuario
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: UserDataDir
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"${users}/${user_name}/Edge"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: UserDataDir
  - Valor de ejemplo:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### UserDataSnapshotRetentionLimit

  #### Limita el número de instantáneas de datos de usuario que se conservan para su uso en caso de reversión de emergencia

  
  
  #### Versiones compatibles:

  - En Windows desde la versión 86 o posterior

  #### Descripción

  Después de cada actualización de la versión principal, Microsoft Edge creará una instantánea de las partes de los datos de exploración del usuario que se usarán en caso de una emergencia posterior que requiera la reversión temporal de la versión. Si se lleva a cabo una reversión temporal en una versión de la cual el usuario tenga la instantánea correspondiente, se restaurarán los datos de la instantánea. Así, los usuarios pueden conservar configuraciones tales como marcadores y datos del autorrelleno.

Si no establece esta directiva, se usará el valor predeterminado de 3 instantáneas.

Si define esta directiva, las instantáneas antiguas se eliminarán según sea necesario para respetar el límite que usted establezca. Si establece esta directiva en 0, no se realizará ninguna instantánea.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Integer

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: UserDataSnapshotRetentionLimit
  - Nombre de GP: Limita el número de instantáneas de datos de usuario que se conservan para su uso en caso de reversión de emergencia
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre de valor: UserDataSnapshotRetentionLimit
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000003
```


  

  [Volver al principio](#microsoft-edge---policies)

  ### UserFeedbackAllowed

  #### Permitir comentarios de los usuarios

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Microsoft Edge usa la característica de Comentarios de Edge (habilitada de forma predeterminada) para permitir que los usuarios envíen comentarios, sugerencias o encuestas a los clientes e informen sobre cualquier problema con el explorador. Asimismo, de forma predeterminada, los usuarios no pueden deshabilitar (desactivar) la característica de comentarios de Microsoft Edge.

Si habilita esta directiva o no la configura los usuarios podrán invocar la característica de comentarios de Microsoft Edge

Si deshabilita esta directiva, los usuarios no podrán invocar la característica de comentarios de Microsoft Edge

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: UserFeedbackAllowed
  - Nombre de GP: permitir comentarios de los usuarios
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: UserFeedbackAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: UserFeedbackAllowed
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### VideoCaptureAllowed

  #### Permitir o bloquear captura de vídeo

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Controla si los sitios pueden capturar vídeo.

Si se habilita o no se configura (valor predeterminado), se le solicitará al usuario el acceso para la captura de vídeo en todos los sitios, excepto en los que tengan direcciones URL configuradas en la lista de la directiva [VideoCaptureAllowedUrls](#videocaptureallowedurls), a los cuales se les concederá acceso sin solicitarlo.

Si deshabilita esta directiva, no se le harán solicitudes al usuario y la captura de vídeo solo estará disponible para las direcciones URL configuradas en la directiva [VideoCaptureAllowedUrls](#videocaptureallowedurls).

Esta directiva afecta todos los tipos de entradas de vídeo, no solo a la cámara integrada.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: VideoCaptureAllowed
  - Nombre de GP: permitir o bloquear captura de vídeo
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: VideoCaptureAllowed
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000000
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: VideoCaptureAllowed
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### VideoCaptureAllowedUrls

  #### Sitios que pueden acceder a dispositivos de captura de vídeo sin solicitar permiso

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Especificar sitios web basándose en modelos URL que pueden usar dispositivos de captura de vídeo sin pedir permiso al usuario. Los patrones en esta lista se hacen coincidir con el origen de seguridad de la dirección URL que realiza la solicitud. Si coinciden, el sitio recibe acceso automáticamente a los dispositivos de captura de vídeo.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: VideoCaptureAllowedUrls
  - Nombre de GP: sitios que pueden acceder a dispositivos de captura de vídeo sin solicitar permiso
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\VideoCaptureAllowedUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: VideoCaptureAllowedUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WPADQuickCheckEnabled

  #### Establecer la optimización de WPAD

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Le permite deshabilitar la optimización WPAD (detección automática de proxy web) en Microsoft Edge.

Si deshabilita esta directiva, la optimización de WPAD se deshabilitará, lo que hará que el explorador tenga que esperar más tiempo por los servidores WPAD basados en DNS.

Si habilita o no configura la directiva, la optimización de WPAD se habilitará.

Independientemente de si esta directiva está habilitada, los usuarios no podrán cambiar la configuración de la optimización de WPAD.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WPADQuickCheckEnabled
  - Nombre de GP: establecer optimización WPAD
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: WPADQuickCheckEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: WPADQuickCheckEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WebAppInstallForceList

  #### Configurar la lista de aplicaciones web instaladas por la fuerza.

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Configure esta directiva para especificar una lista de aplicaciones web que se instalan de forma silenciosa, sin interacción del usuario, y qué usuarios no pueden desinstalar o desactivar.

Cada elemento de la lista es un objeto con un miembro obligatorio: url (la dirección URL de la aplicación web que se va a instalar) y 2 miembros opcionales: default_launch_container (especifica el modo de ventana en el que se abre la aplicación web: una pestaña nueva es el valor predeterminado) y create_desktop_shortcut (True si quiere crear accesos directos del escritorio de Windows y Linux).

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Diccionario

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WebAppInstallForceList
  - Nombre de GP: configurar la lista de aplicaciones web instaladas a la fuerza.
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: WebAppInstallForceList
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [
  {
    "create_desktop_shortcut": true, 
    "default_launch_container": "window", 
    "url": "https://www.contoso.com/maps"
  }, 
  {
    "default_launch_container": "tab", 
    "url": "https://app.contoso.edu"
  }
]
```

  ##### Valor de ejemplo de Compact:

  ```
  SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [{"create_desktop_shortcut": true, "default_launch_container": "window", "url": "https://www.contoso.com/maps"}, {"default_launch_container": "tab", "url": "https://app.contoso.edu"}]
  ```
  

  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: WebAppInstallForceList
  - Valor de ejemplo:
``` xml
<key>WebAppInstallForceList</key>
<array>
  <dict>
    <key>create_desktop_shortcut</key>
    <true/>
    <key>default_launch_container</key>
    <string>window</string>
    <key>url</key>
    <string>https://www.contoso.com/maps</string>
  </dict>
  <dict>
    <key>default_launch_container</key>
    <string>tab</string>
    <key>url</key>
    <string>https://app.contoso.edu</string>
  </dict>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WebCaptureEnabled

  #### Habilitar la característica de captura Web en Microsoft Edge

  
  
  #### Versiones compatibles:

  - On Windows and macOS since 87 or later

  #### Descripción

  Habilita la característica de captura Web en Microsoft Edge que permite a los usuarios capturar contenido web y realizar anotaciones en la captura con las herramientas de entrada de lápiz.
Si habilita esta Directiva o no la configura, la opción de captura web aparece en el menú contextual, en la configuración y en el menú más y mediante el método abreviado de teclado, CTRL + MAYÚS + S.
Si deshabilita esta Directiva, los usuarios no podrán acceder a la característica de captura Web en Microsoft Edge.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: sí

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WebCaptureEnabled
  - Nombre GP: habilitar la característica de captura Web en Microsoft Edge
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: WebCaptureEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```

  #### Información y configuración de Mac
  
  - Nombre de clave de preferencias: WebCaptureEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WebComponentsV0Enabled

  #### Nombre de GP: volver a habilitar la API de componentes web v0 hasta M84.

  
  >OBSOLETA: Esta directiva está obsoleta y no funciona después de Microsoft Edge 84.
  #### Versiones compatibles:

  - En Windows y MacOS desde el 80 hasta el 84

  #### Descripción

  Esta Directiva no funciona porque esta directiva permitió que estas características se habiliten de forma selectiva hasta la versión 85 de Microsoft Edge. Las API de los componentes Web v0 (Shadow DOM v0, elementos personalizados v0, e importaciones de HTML) fueron deshabilitas en 2018, y han sido deshabilitas de forma predeterminada empezando por M80.

Si configura esta directiva como verdadera, se habilitarán las características de Web Components V0 para todos los sitios.

Si establece esta directiva como falsa o no la establece, las características de los componentes Web v0 se deshabilitarán de forma predeterminada, comenzando por M80.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WebComponentsV0Enabled
  - Nombre GP: vuelva a habilitar los componentes Web API V0 hasta M84 (obsoleto)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: WebComponentsV0Enabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: WebComponentsV0Enabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WebDriverOverridesIncompatiblePolicies

  #### Permitir que WebDriver reemplace las directivas incompatibles (en desuso)

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
                     
  #### Versiones compatibles:

  - En Windows y MacOS desde el 77 hasta el 84

  #### Descripción

  Esta Directiva no funciona porque Webdriver ya es compatible con todas las directivas existentes.

Esta directiva permite que los usuarios de la función WebDriver anulen las directivas que puedan interferir con su operación.

En este momento, esta directiva deshabilita las directivas de [SitePerProcess](#siteperprocess) e [IsolateOrigins](#isolateorigins).

Si la directiva está habilitada, WebDriver podrá anular las directivas de incompatibilidad.
Si la directiva está deshabilitada o no está configurada, WebDriver no podrá anular las directivas que no sean compatibles.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WebDriverOverridesIncompatiblePolicies
  - Nombre de GP: permitir que WebDriver reemplace las que no sean compatibles (en desuso)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: WebDriverOverridesIncompatiblePolicies
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  #### Información y configuración de Mac
  
  - Nombre de clave de la preferencia: WebDriverOverridesIncompatiblePolicies
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WebRtcLocalIpsAllowedUrls

  #### Administrar la exposición de la dirección IP local por WebRTC

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 80 o posterior

  #### Descripción

  Especifica una lista de orígenes (direcciones URL) o patrones de nombre de host (como "*contoso.com*") para que la dirección IP local pueda ser mostrada por WebRTC.

Si habilita esta directiva y establece una lista de orígenes (direcciones URL) o patrones de nombre de host, al habilitar edge://flags/#enable-webrtc-Hide-local-IPS-con-mDNS, WebRTC mostrará la dirección IP local a los casos que coincidan con los patrones en la lista.

Si deshabilita o no configura esta directiva, y edge://flags/#enable-webrtc-Hide-local-IPS-con-mDNS está habilitado, WebRTC no mostrará las direcciones IP locales. La dirección IP local está oculta con un nombre de host mDNS.

Si deshabilita o no configura esta directiva, y edge://flags/#enable-webrtc-hide-local-ips-with-mdns está habilitado, WebRTC no mostrará las direcciones IP locales.

Tenga en cuenta que esta directiva reduce la protección de las direcciones IP locales que los administradores podrían necesitar.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Lista de cadenas

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WebRtcLocalIpsAllowedUrls
  - Nombre de GP: administrar la exposición de la dirección IP local por WebRTC
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ

  ##### Valor de ejemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: WebRtcLocalIpsAllowedUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WebRtcLocalhostIpHandling

  #### Restringir la exposición de la dirección IP local por WebRTC

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Le permite establecer si WebRTC mostrará o no la dirección IP local del usuario.

Si establece esta directiva en "AllowAllInterfaces" o "AllowPublicAndPrivateInterfaces", WebRTC mostrará la dirección IP local.

Si establece esta directiva en "AllowPublicInterfaceOnly" o "DisableNonProxiedUdp", WebRTC no mostrará la dirección IP local.

Si deshabilita o no define esta directiva, WebRTC mostrará la dirección IP local.

Asignación de opciones de directiva:

* AllowAllInterfaces (valor predeterminado) = permitir todas las interfaces. Esto muestra la dirección IP local.

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = permitir las interfaces pública y privada a través de la ruta http predeterminada. Esto muestra la dirección IP local.

* AllowPublicInterfaceOnly (default_public_interface_only) = permitir la interfaz pública a través de la ruta predeterminada http. Esto no muestra la dirección IP local.

* DisableNonProxiedUdp (disable_non_proxied_udp) = usar TCP excepto si el servidor proxy es compatible con UDP. Esto no muestra la dirección IP local.

Use la información anterior al configurar esta directiva.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WebRtcLocalhostIpHandling
  - Nombre de GP: restringir la exposición de la dirección IP local de la WebRTC
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: WebRtcLocalhostIpHandling
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"default"
```


  #### Información y configuración de Mac
  
  - Nombre clave de la preferencia: WebRtcLocalhostIpHandling
  - Valor de ejemplo:
``` xml
<string>default</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WebRtcUdpPortRange

  #### Restringir el rango de puertos UDP locales usados por WebRTC

  
  
  #### Versiones compatibles:

  - En Windows y MacOS desde 77 o posterior

  #### Descripción

  Restringe el intervalo de puertos UDP usado por WebRTC a un intervalo de puertos específico (incluyendo los puntos de conexión).

Debe especificar el intervalo de puertos UDP locales que WebRTC puede usar al configurar esta directiva.

Si no configura esta directiva, o si la establece con una cadena vacía o un intervalo de puertos no válido, WebRTC podrá usar cualquier puerto UDP local disponible.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Cadena

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WebRtcUdpPortRange
  - Nombre de GP: restringir el rango de puertos locales UDP usados por WebRTC
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: WebRtcUdpPortRange
  - Tipo de valor: REG_SZ

  ##### Valor de ejemplo:

```
"10000-11999"
```


  #### Información y configuración de Mac
  
  - Nombre clave de preferencia: WebRtcUdpPortRange
  - Valor de ejemplo:
``` xml
<string>10000-11999</string>
```
  

  [Volver al principio](#microsoft-edge---policies)

  ### WinHttpProxyResolverEnabled

  #### Usar la resolución del proxy de Windows (en desuso)

  >En desuso: esta directiva está en desuso. Actualmente se admite pero quedará obsoleto en una versión futura.
  
  #### Versiones compatibles:

  - En Windows desde la versión 84 o posterior

  #### Descripción

  Esta directiva está en desuso, ya que se reemplazará por una característica similar en una versión futura; puede consultar https://crbug.com/1032820.

Use Windows para resolver los servidores proxy de todas las redes de exploradores en lugar de la resolución de proxy integrada en Microsoft Edge. El solucionador de proxy de Windows admite características de proxy de Windows como DirectAccess/NRPT.

Esta Directiva se proporciona con los problemas descritos por https://crbug.com/644030. Hace que el código de Windows recupere y ejecute archivos PAC, incluidos los archivos PAC configurados a través de la Directiva [ProxyPacUrl](#proxypacurl). Como las búsquedas en red para el archivo PAC ocurren por Windows en lugar de con el código de Microsoft Edge, las directivas de red como [DnsOverHttpsMode](#dnsoverhttpsmode) no se aplicarán a las búsquedas en red de un archivo PAC.

Si habilita esta Directiva, se usará la resolución del proxy de Windows.

Si deshabilita o no configura esta Directiva, se usará la resolución de proxy de Microsoft Edge.

  #### Características admitidas:

  - Puede ser obligatorio: sí
  - Puede ser recomendable: no
  - Actualización de directiva dinámica: no es necesario reiniciar el explorador

  #### Tipo de datos:

  - Booleano

  #### Información y configuración de Windows

  ##### Información de directiva de grupo (ADMX)

  - Nombre único de GP: WinHttpProxyResolverEnabled
  - Nombre GP: usar la resolución del proxy de Windows (en desuso)
  - Ruta de acceso de GP (obligatoria): Plantillas administrativas/ Microsoft Edge/
  - Ruta de acceso de GP (recomendado): N/D
  - Nombre de archivo de ADMX GP: MSEdge.admx

  ##### Configuración del Registro de Windows

  - Ruta de acceso (obligatoria): SOFTWARE\Directivas\Microsoft\Microsoft Edge
  - Ruta de acceso (recomendado): N/D
  - Nombre del valor: WinHttpProxyResolverEnabled
  - Tipo de valor: REG_DWORD

  ##### Valor de ejemplo:

```
0x00000001
```


  

  [Volver al principio](#microsoft-edge---policies)


## Consulte también

- [Configuración de Microsoft Edge](configure-microsoft-edge.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Blog de líneas de base de seguridad de Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)
