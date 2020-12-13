---
title: Notas de la versión de Microsoft Edge para el canal estable
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 12/10/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de la versión de Microsoft Edge para el canal estable
ms.openlocfilehash: dd3ff3a37b2df1cf4ad8a9d9e83e0a21edeeba9d
ms.sourcegitcommit: 827eca46dd767f3c4509259974e1383fdf506d7e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "11205835"
---
# Notas de la versión para el canal estable de Microsoft Edge

Estas notas de versión proporcionan información sobre las nuevas características y las actualizaciones no relacionadas con la seguridad que se incluyen en el canal estable de Microsoft Edge. Para entender los canales de Microsoft Edge, consulte la [Información general sobre los canales de Microsoft Edge](microsoft-edge-channels.md). Todas las actualizaciones de seguridad se muestran [aquí](microsoft-edge-relnotes-security.md).

> [!NOTE]
> Para el canal estable, las actualizaciones se implementarán de manera progresiva en uno o más días. Para obtener más información, consulte [Progressive rollouts for Microsoft Edge updates (Implementaciones progresivas de actualizaciones de Microsoft Edge)](microsoft-edge-update-progressive-rollout.md).

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

<!-- begin 84 -->
## Versión 84.0.522.40: 16 de julio

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#july-16-2020)

### Actualizaciones de características

- Esta versión de Microsoft Edge proporciona tiempos mejorados de descarga de la lista de sitios en el modo Internet Explorer. Hemos reducido el tiempo de retraso de la descarga de la lista de sitios en modo Internet Explorer de 60 segundos a 0 segundos, en ausencia de una lista de sitios en caché. También hemos agregado compatibilidad con la directiva de grupo para casos en los que es necesario retrasar la navegación de la página principal en modo Internet Explorer hasta que finaliza la descarga de la lista de sitios. Para más información, consulte la directiva [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

- Microsoft Edge permite ahora a los usuarios iniciar sesión en el explorador cuando se "ejecuta como administrador" en Windows 10. Esto ayudará a los clientes que ejecuten Microsoft Edge en Windows server o en escenarios de escritorio remoto y de espacio aislado.

- Microsoft Edge ofrece ahora compatibilidad total con el mouse en el modo de pantalla completa. Ahora puede usar el mouse para acceder a las pestañas, la barra de direcciones y otros elementos sin tener que salir del modo de pantalla completa.

- Mejoras en la compra online. Agregue alias personalizados a la tarjeta de crédito o débito guardada. Ahora podrá distinguir y diferenciar las tarjetas de crédito cuando realice compras en línea. Escribir un alias para las tarjetas de crédito o débito le facilitará elegir la tarjeta adecuada al usar la opción de Autorrellenar para seleccionar un método de pago.

- De forma predeterminada, se deshabilitan TLS/1.0 y TLS/1.1.  La directiva [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) permite volver a habilitar TLS/1.0 y TLS/1.1. Esta directiva estará disponible como mínimo hasta la versión 88 de Microsoft Edge. Para más información, consulte [Cambios que se van a producir en Microsoft Edge que afectan a la compatibilidad de los sitios](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

- Mejoras en las colecciones:

  - Se ha agregado una funcionalidad de notas que le permite añadir una nota o comentario a un elemento de una colección. Las notas se agrupan y se mantienen adjuntadas a un elemento incluso si se ordenan los elementos de una colección. Para probar esta característica nueva, haga clic con el botón derecho en un elemento y seleccione "Agregar nota".
  - Puede cambiar el color de fondo de las notas en las colecciones. Puede usar la codificación por colores para ayudarle a organizar información y a incrementar la productividad.
  - Se han realizado mejoras notables en el rendimiento que le permiten exportar las colecciones a Excel en un tiempo menor que en las versiones anteriores de Microsoft Edge.

- Compatibilidad adicional con la API de Microsoft Edge:

  - La API de acceso de almacenamiento está habilitada para experimentación. Esta característica está habilitada para usuarios domésticos y usuarios de empresa con la directiva [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/deployedge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) establecida en "Completo". De forma predeterminada, esta característica estará habilitada para todos los usuarios de la versión 85 de canal estable de Microsoft Edge.
  
    Dado que la privacidad es cada vez más importante para los usuarios, van en aumento las solicitudes de configuraciones opcionales de usuario y de valores predeterminados del explorador más estrictos, como el bloqueo de todos los accesos al almacenamiento de terceros. Si bien estas configuraciones contribuyen a mejorar la privacidad y a bloquear los accesos no deseados de partes desconocidas o que no son de confianza, pueden tener consecuencias no deseadas, como el bloqueo del acceso a contenido que el usuario podría querer ver (por ejemplo, contenido de redes sociales y contenido multimedia incrustado).

    Esta API permite acceder al almacenamiento de origen en un contexto de terceros en el que un usuario proporcione una forma directa para permitir el almacenamiento que, de otro modo, quedaría bloqueado por la configuración actual del explorador. Para obtener más información, consulte [API de acceso al almacenamiento](https://www.chromestatus.com/feature/5612590694662144).

  - La API del sistema de archivos nativo quiere decir que usted puede conceder permisos a los sitios para editar archivos o carpetas mediante la API del sistema de archivos nativo.

- Mejoras de PDF:

  - Leer en voz alta para PDF permite a los usuarios escuchar contenido PDF mientras llevan a cabo otras tareas que pueden ser importantes. Además, ayuda a las personas que reciben educación audiovisual a centrarse en la lectura del contenido, lo que facilita el aprendizaje.
  - Se ha mejorado la edición de archivos PDF. Ahora puede guardar en el mismo archivo las modificaciones realizadas a un archivo PDF, en lugar de tener que guardar una copia cada vez que edita un PDF.

- Microsoft Edge permite ahora traducir en el Lector inmersivo. Cuando un usuario abre la vista de Lector inmersivo, obtiene la opción de traducir la página al idioma que desee.

- Varias actualizaciones de DevTools, como la compatibilidad con la personalización de los métodos abreviados de teclado para que coincidan con los de VS Code, y la visualización de DevTools en contraste alto.  Para obtener más información, consulte [Novedades en DevTools (Microsoft Edge 84)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### Actualizaciones de directiva

#### Nuevas directivas

Se han agregado siete directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled): permite volver a habilitar la característica AppCache, incluso si está desactivada de forma predeterminada.
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy): configurar las opciones del contenedor proxy de Protección de aplicaciones.
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload): Requerir que la lista de sitios modo empresarial esté disponible antes que la navegación por la tabulación.
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled): utilizar el solucionador de proxy de Windows.
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection): configurar la detección de bloqueos mejorada para el modo de Internet Explorer.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Para disminuir el consumo de energía y de la CPU, Microsoft Edge detectará cuándo una ventana está cubierta por otra ventana y suspenderá el trabajo pintando píxeles.
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout): Establecer un tiempo de espera de retardo en la navegación mediante tabulación para la lista de sitios de modo empresarial.

#### Directivas obsoletas

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal): Permitir que las páginas envíen solicitudes sincrónicas de XHR durante el descarte de página.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled): determina si el comprobador de certificados integrado se usará para comprobar certificados de servidor.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled): habilitar el tratamiento más estricto para contenido mixto.

#### Directiva obsoleta

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess): Forzar el código de red para que se ejecute en el proceso del explorador.

<!-- End 84 -->
## Versión 83.0.478.64: 13 de julio

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.61: 7 de julio

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.58: 30 de junio

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.56: 24 de junio

Se han corregido varios errores y problemas de rendimiento.

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-24-2020)

## Versión 83.0.478.54: 17 de junio

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-17-2020)

## Versión 83.0.478.50: 15 de junio

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.45: 4 de junio

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-4-2020)

## Versión 83.0.478.44: 1 de junio

Se han corregido varios errores y problemas de rendimiento.

## Versión 83.0.478.37: 21 de mayo

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#may-21-2020)

### Actualizaciones de características

- Las actualizaciones de Microsoft Edge ahora se implementarán gradualmente. En el futuro, las actualizaciones de Microsoft Edge se implementarán para nuestros usuarios en un período de unos días. Esto nos permite proteger a más usuarios de actualizaciones con errores accidentales, lo que mejora la experiencia de actualización. Como usuario, seguirá obteniendo actualizaciones automáticas sin problemas. Si su organización no se inscribe para las actualizaciones automáticas, no le afectará este cambio. Para obtener más información, consulte el artículo sobre implementaciones progresivas [Progressive rollouts for Microsoft Edge Stable channel updates (Implementaciones progresivas de actualizaciones de canal estables de Microsoft Edge)](microsoft-edge-update-progressive-rollout.md).
- Mejoras de SmartScreen de Microsoft Defender: se han realizado varias mejoras en el servicio de SmartScreen de Microsoft Defender, como la protección mejorada frente a sitios malintencionados que redirigen al cargar, y el bloqueo de marco de nivel superior que reemplaza completamente sitios malintencionados con la página de seguridad de SmartScreen de Microsoft Defender. El bloqueo del marco de nivel superior impide que el audio y otros elementos multimedia del sitio malintencionado se reproduzcan, lo que ofrece una experiencia más fácil y menos confusa.

- En respuesta a los comentarios de los usuarios, ahora se pueden eximir algunas cookies del borrado automático cuando se cierre el explorador. Esta opción es útil si hay un sitio en el que los usuarios no quieren cerrar la sesión, pero quieren que todas las demás cookies se eliminen cuando se cierre el explorador. Para usar esta característica, ve a *edge://settings/clearBrowsingDataOnClose* y habilita el interruptor "Cookies y otros datos de sitio".

- El cambio de perfil automático ya está disponible para ayudarte a obtener el contenido del trabajo más fácilmente entre perfiles. Si usas varios perfiles en el trabajo, puedes probarlo en un sitio que requiera autenticación de tu cuenta profesional o educativa mientras estás en tu perfil personal. Cuando se detecta esto, se te pedirá que cambies a su perfil de trabajo para tener acceso a ese sitio sin tener que autenticarte. Cuando elijas el perfil de trabajo al que quieres cambiar, el sitio web simplemente se abrirá en tu perfil de trabajo. Esta función de cambio de perfil te ayudará a mantener tus datos personales y de trabajo separados y a obtener el contenido de trabajo con mayor esfuerzo. Si no quieres que la característica te solicite cambiar perfiles, puedes elegir la opción no volver a preguntar y se quitará.

- Mejoras de la característica de Colecciones:
  - Puedes usar arrastrar y soltar para agregar un elemento a una colección sin abrir la colección. Durante el proceso de arrastrar y soltar también puedes elegir una ubicación en la lista de colecciones en la que quieras colocar el elemento.
  - Puedes agregar varios elementos a una colección en lugar de agregar un elemento a la vez. Para agregar varios elementos, selecciona los elementos y arrástralos hasta una colección. También puedes seleccionarlos, hacer clic con el botón derecho y elegir la colección en la que quieres que aparezcan los elementos.

- Puedes agregar todas las pestañas de una ventana de Microsoft Edge a una colección nueva sin agregarlas individualmente. Para ello, haz clic con el botón derecho en cualquier pestaña y elige "Agregar todas las pestañas a una nueva colección".

- La sincronización de extensiones ya está disponible. Ahora, puedes sincronizar tus extensiones de en todos tus dispositivos. Las extensiones de las tiendas de Microsoft y Chrome se sincronizarán con Microsoft Edge. Para usar esta característica: haz clic en el signo de puntos suspensivos (**...**) en la barra de menús, selecciona **Configuración**. En Tu perfil, haz clic en **Sincronización** para ver las opciones de sincronización. En **Perfiles / Sincronizar** usa el botón de alternancia para habilitar Extensiones. Puedes usar la directiva de grupo [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) para deshabilitar la sincronización de extensiones.

- Se ha mejorado el mensaje en la página de Administración de descargas para las descargas no seguras que se han bloqueado.

- Mejoras en el Lector inmersivo:
  - Se ha agregado soporte para Adverbios en la experiencia de Elementos de la oración que tenemos en el Lector inmersivo. Mientras lee un artículo en el Lector inmersivo, abra las Herramientas gramaticales y active los Adverbios en las Elementos de la oración para resaltar todos los adverbios de la página.
  - Se ha agregado la posibilidad de seleccionar cualquier contenido de una página web y abrirla en el Lector inmersivo. Esta capacidad permite a los usuarios utilizar el Lector inmersivo y todas las herramientas de aprendizaje, como Foco de línea y Lectura en voz alta, en todos los sitios web.

- Link doctor proporciona correcciones de host y una consulta de búsqueda a los usuarios cuando escriben errores en una dirección URL. Por ejemplo: <br>
Un usuario escribe "powerbi" como "powerbbi".com. Link doctor propondrá "powerbi".com como corrección y creará un vínculo para buscar "powerbbi" en caso de que el usuario busque algo diferente.

- Permitir que los usuarios guarden su decisión de lanzar un protocolo externo para un sitio específico. Los usuarios pueden configurar la directiva [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) para habilitar o deshabilitar esta característica.

- Los usuarios pueden establecer Microsoft Edge como su explorador predeterminado directamente desde la **Configuración** de Microsoft Edge. Esto hace que sea más fácil para los usuarios cambiar el explorador predeterminado, dentro del contexto del explorador, en lugar de tener que buscar en la configuración del sistema operativo. Para usar esta característica, ve a *edge://settings/defaultBrowser* y haz clic en **Establecer como predeterminado**.

- Varias actualizaciones de DevTools, incluido el nuevo soporte de depuración remota, mejoras en la interfaz de usuario y más. Para más información, consulta [Novedades en DevTools (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- El escenario de advertencia MCAS (seguridad de acceso a la nube de Microsoft). Esto permite que los administradores configuren advertir, una nueva categoría de bloqueos de MCAS que permite al usuario invalidar una página de bloqueo de MCAS. Los bloqueos MDATP E5 están integrados de forma nativa en los bloqueos de SmartScreen para ofrecer una experiencia perfecta. Esta experiencia permite la apariencia de un bloqueo en rojo de página completa con el mensaje "Su organización ha bloqueado este sitio web", en lugar de solo una notificación del sistema.

- No permitir XmlHttpRequest sincrónico en el descarte de página. Se eliminará el envío de XmlHttpRequests sincrónicos durante la carga de una página web. Este cambio mejora el rendimiento y la confiabilidad del explorador, pero puede afectar a las aplicaciones web que aún no se han actualizado para usar API web más modernas, como sendBeacon y Fetch. La directiva de grupo para deshabilitar este cambio y permitir la XHR sincrónica durante el descarte de la página estará disponible hasta Microsoft Edge 88. Para más información, consulte [Cambios que se van a producir en Microsoft Edge que afectan a la compatibilidad de los sitios](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

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

<!-- end 83 -->

## Versión 81.0.416.77: 18 de mayo

Se han corregido varios errores y problemas de rendimiento.

## Versión 81.0.416.72: 7 de mayo

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#may-7-2020)

## Versión 81.0.416.68: 29 de abril

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-29-2020)

## Versión 81.0.416.64: 23 de abril

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-23-2020)

## Versión 81.0.416.58: 17 de abril

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-17-2020)

## Versión 81.0.416.53: 13 de abril

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-13-2020)

### Actualizaciones de características

- Se agregó la compatibilidad con Windows Information Protection (WIP), que ayuda a las empresas a proteger los datos confidenciales de una divulgación no autorizada. [Más información](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection).

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

### Actualizaciones de directiva

#### Nuevas directivas

Se han agregado 11 directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled): habilitar la autenticación de ambiente para los perfiles de InPrivate e invitado. 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled): permitir ejecutar el espacio aislado de audio.
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy): usar una directiva de referrer predeterminada de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled): habilitar la memoria caché de autenticación HTTP de ámbito global.
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions): permitir la importación de extensiones.
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies): permitir la importación de cookies.
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts): permitir la importación de métodos abreviados.
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect) : especificar cómo se comportan las navegaciones "en la página" de los sitios no configurados al iniciarse en las páginas en modo Internet Explorer.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled): habilitar el tratamiento más estricto para contenido mixto.
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled): habilitar una característica de seguridad TLS 1.3 para anclajes de veracidad locales.
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin): configurar el inicio de sesión automático con una cuenta de dominio de Active Directory cuando no haya cuenta de dominio de Azure AD.

#### Cambios en el nombre y el título de directiva

La directiva `OmniboxMSBProviderEnabled` ha cambiado a [AddressBarMicrosoftSearchInBingProviderEnabled](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled): el título de la directiva es "Habilitar sugerencias de Búsqueda de Microsoft en Bing en la barra de direcciones".

#### Directivas obsoletas

Las siguientes directivas siguen funcionando en esta versión. Pasarán a ser "obsoletas" en una versión futura.

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled): volver a habilitar la API de componentes web v0 hasta M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): permitir que el controlador WebDriver reemplace Incompatible.

#### Problemas resueltos

- Se ha corregido un problema en el que el modo IE en Microsoft Edge provocaba que apareciese un cuadro de diálogo de descarga en curso, incluso después de descargar el archivo.
- Se ha corregido un problema que provocaba que Microsoft Edge quitara las cookies de sesión cuando una página que ya estaba en modo IE activaba la apertura de una nueva pestaña en modo IE.

## Versión 80.0.361.111: 7 de abril

Se han corregido varios errores y problemas de rendimiento.

## Versión 80.0.361.109: 1 de abril

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-1-2020)

## Versión 80.0.361.69: 19 de marzo

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-19-2020)

## Versión 80.0.361.66: 4 de marzo

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-4-2020)

## Versión 80.0.361.62: 25 de febrero

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#february-25-2020)

## Versión 80.0.361.57: 20 de febrero

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#february-20-2020)

## Versión 80.0.361.56: 19 de febrero

Se han corregido varios errores y problemas de rendimiento.

## Versión 80.0.361.54: 14 de febrero

### Problemas resueltos

- Se ha corregido un problema por el que la contraseña, el pago y las cookies no se importaban en Microsoft Edge.

## Versión 80.0.361.50: 11 de febrero

Se han solucionado varios errores y correcciones de rendimiento.

## Versión 80.0.361.48: 7 de febrero

Las actualizaciones de seguridad se muestran [aquí](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#february-7-2020)

### Actualizaciones de características

- Se ha agregado la protección de SmartScreen para descargar aplicaciones potencialmente no deseadas. [Obtén más información](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
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

### Actualizaciones de directivas

#### Nuevas directivas

Se han agregado 16 directivas nuevas. Descargue las plantillas administrativas actualizadas desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Se han agregado las siguientes directivas nuevas.

- [AlternateErrorPagesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#alternateerrorpagesenabled): Sugiere páginas similares cuando no se puede encontrar una página web.
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting): controlar el uso de excepciones de contenido no seguro.
- [DNSInterceptionChecksEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsinterceptionchecksenabled): comprobaciones de interceptación de DNS habilitadas.
- [HideFirstRunExperience](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hidefirstrunexperience): ocultar la experiencia de primera ejecución y la pantalla de presentación.
- [InsecureContentAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecurecontentallowedforurls): permitir el contenido no seguro en sitios especificados.
- [InsecureContentBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecurecontentblockedforurls): bloquear contenido no seguro en sitios especificados.
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled): habilitar la configuración de comportamiento de cookies de SameSite heredado predeterminado.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist): revertir al comportamiento de SameSite heredado para las cookies en sitios especificados.
- [PaymentMethodQueryEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#paymentmethodqueryenabled): permitir que los sitios web consulten las formas de pago disponibles.
- [PersonalizationReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#personalizationreportingenabled): permitir la personalización de anuncios, búsquedas y noticias enviando historial de exploración a Microsoft.
- [PinningWizardAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pinningwizardallowed): permitir el Asistente para Anclar a la barra de tareas.
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled): configurar Microsoft Defender SmartScreen para bloquear aplicaciones potencialmente no deseadas.
- [TotalMemoryLimitMb](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#totalmemorylimitmb): establecer el límite en megabytes de memoria que puede usar una única instancia de Microsoft Edge.
- [WebAppInstallForceList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webappinstallforcelist): configurar la lista de aplicaciones web instaladas por la fuerza.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled): volver a habilitar la API de componentes web v0 hasta M84.
- [WebRtcLocalIpsAllowedUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalipsallowedurls): administrar la exposición de direcciones IP locales por WebRTC.

#### Directivas obsoletas

La siguiente directiva ha quedado obsoleta.

- [NewTabPageCompanyLogo](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagecompanylogo): establecer el logotipo de la página de nueva pestaña.

### Problemas resueltos

- Se ha corregido un problema que hacía que el audio no funcionase en el entorno de Citrix.
- Se ha corregido un problema por el que la experiencia en paralelo de Microsoft Edge y Microsoft Edge heredado producía bloqueos y vínculos heredados fallidos.

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
