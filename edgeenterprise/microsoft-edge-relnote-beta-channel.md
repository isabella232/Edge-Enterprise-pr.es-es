---
title: Notas de la versión de Microsoft Edge para el canal beta
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 09/13/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas de la versión de Microsoft Edge para el canal beta
ms.openlocfilehash: 93fbb135befd1691220a1d9b4499d0713b1740f3
ms.sourcegitcommit: c3d63d913eb15e7dbeb9f45b5f28fc841b46bce1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2021
ms.locfileid: "12016469"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de la versión para el canal beta de Microsoft Edge

Estas notas de versión proporcionan información sobre las nuevas características y las actualizaciones no relacionadas con la seguridad que se incluyen en el canal beta de Microsoft Edge. Las versiones archivadas de estas notas de la versión están [aquí](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> La plataforma web de Microsoft Edge evoluciona constantemente para mejorar la experiencia del usuario, la seguridad y la privacidad. Para más información, vea [Cambios que afectan la compatibilidad del sitio próximamente en Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-94099219-september-13"></a>Versión 94.0.992.19: 13 de septiembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-94099214-september-7"></a>Versión 94.0.992.14: 7 de septiembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-9409929-september-2"></a>Versión 94.0.992.9: 2 de septiembre

### <a name="feature-updates"></a>Actualizaciones de características

- **Microsoft Edge a una cadencia de 4 semanas para actualizaciones en canales Beta y Estable.**  Adoptaremos un nuevo ciclo de lanzamiento de 4 semanas para las versiones principales. Puede leer más sobre la decisión aquí: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Nueva opción estable extendida que se ofrece.**  Ofrecemos una nueva opción extended stable a nuestros clientes Enterprise administrados. La opción Estable extendida se mantendrá en revisiones numeradas uniformes y se actualizará cada 8 semanas. Habrá una actualización de seguridad quincenal.  Información adicional aquí: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Mejoras en el comportamiento predeterminado de abrir archivos MHTML.**  Los archivos MHTML seguirán abiertos en modo IE si el modo IE está habilitado, a menos que el archivo MHTML se haya guardado desde Microsoft Edge (mediante las opciones Guardar como o Guardar página como en Microsoft Edge). Si el archivo se guardó Microsoft Edge, ahora se abrirá en Microsoft Edge.  Este cambio corregirá un problema de representación que se observó al abrir un archivo MHTML en modo IE cuando se guardaba desde Microsoft Edge.

- **Restringir las solicitudes de red privada a contextos seguros.** El acceso a recursos en redes locales (intranet) desde páginas en Internet requiere que esas páginas se entreguen a través de HTTPS. Este cambio se produce en el proyecto Chromium, en el que se basa Microsoft Edge. Para obtener más información, vaya a la entrada [Estado de la plataforma de Chrome](https://chromestatus.com/feature/5436853517811712). Hay dos directivas de compatibilidad disponibles para admitir escenarios que necesitan conservar la compatibilidad con páginas no seguras: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) e [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Bloquear descargas de contenido mixto.** Las páginas seguras solo descargarán archivos hospedados en otras páginas seguras y las descargas hospedadas en páginas no seguras (que no son HTTPS) se bloquearán si se inician desde una página segura. Este cambio se produce en el proyecto Chromium, en el que se basa Microsoft Edge. Para obtener más información, vaya a la entrada [del blog de seguridad de Google](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Habilitar el inicio de sesión implícito para cuentas locales.**   Al habilitar la directiva OnlyOnPremisesImplicitSigninEnabled, solo se habilitarán las cuentas locales para el inicio de sesión implícito.  Microsoft Edge no intentará iniciar sesión implícitamente en cuentas de MSA o AAD. También se detendrán las actualizaciones de cuentas locales a cuentas de AAD.

- **Cuadros de texto de formulario gratuitos agregados a documentos PDF.**  Ahora se admite la adición de cuadros de texto de formularios gratuitos a documentos PDF que puede usar para rellenar formularios y agregar notas visibles.

- **Actualice las contraseñas con facilidad.**  Ahora, el explorador te llevará directamente a la página Cambiar contraseña de un sitio web determinado que te ahorrará tiempo y clics evitando la necesidad de navegar a la página manualmente. Una vez que estés en esta página, el explorador también rellenará automáticamente la contraseña existente y sugerirá una nueva contraseña segura y única.  Tenga en cuenta que actualmente esta característica está disponible en un número limitado de sitios.  

- **Nueva página de configuración de accesibilidad.** Hemos unido la configuración relacionada con la accesibilidad en una sola página. Puede encontrar la nueva página edge://settings/accessibility en la lista de configuración principal. Aquí puedes encontrar la configuración para hacer que la página web sea más grande, mostrar un esquema de alta visibilidad alrededor del área de enfoque y otras configuraciones que pueden ayudar a mejorar la experiencia de navegación web. Seguiremos agregando nueva configuración aquí en versiones futuras de Microsoft Edge.

***Nuevas directivas***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Omitir la configuración de la lista de sitios de Application Guard y examinar Edge normalmente
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Solo cuenta local habilitada para el inicio de sesión implícito
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Habilitar la compatibilidad con Windows reglas de tabla de enrutamiento del sistema operativo al realizar conexiones punto a punto a través de WebRTC

***Directiva obsoleta***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) Habilitar la característica User-Agent sugerencias de cliente

## <a name="version-93096133-august-27"></a>Versión 93.0.961.33: 27 de agosto

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-93096127-august-20"></a>Versión 93.0.961.27: 20 de agosto

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-93096124-august-18"></a>Versión 93.0.961.24: 18 de agosto

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-93096111-august-3"></a>Versión 93.0.961.11: 3 de agosto

### <a name="feature-updates"></a>Actualizaciones de características

- **Preferencias iniciales en Microsoft Edge.**  A partir Microsoft Edge versión 93, la implementación de Microsoft Edge en su empresa será más fácil con la adición de [preferencias iniciales.](/deployedge/initial-preferences-support-on-microsoft-edge-browser)

- **El modo IE en Microsoft Edge admitirá el comportamiento "sin tiempo de respuesta".**  A partir Microsoft Edge versión 93, el modo IE en Microsoft Edge admitirá "no-merge". Para un usuario final, cuando se inicia una nueva ventana del explorador desde una aplicación de modo IE, estará en una sesión independiente, similar al comportamiento de IE11. Deberá ajustar la lista de sitios para configurar sitios que necesiten impedir el uso compartido de sesiones. En segundo plano, para cada ventana de Microsoft Edge, la primera vez que se visita una pestaña de modo IE dentro de esa ventana, si es uno de los sitios designados “sin tiempo de respuesta”, esa ventana se bloquea en una sesión de IE sin tiempo de respuesta diferente de todas las demás ventanas de Microsoft Edge al menos hasta que se cierre la última pestaña de “ modo ” IE en esa ventana. Obtenga más información [aquí](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--no-merge--option-that-was-supported-in-internet-explorer-11-).

- **Grupos de pestañas.**  La capacidad de clasificar las pestañas en grupos definidos por el usuario le ayuda a encontrar, cambiar y administrar pestañas de forma más eficaz en varias secuencias de trabajo. Para habilitar esto, estamos activando la agrupación de pestañas a partir Microsoft Edge versión 93.

- **Oculta la barra de título mientras usas pestañas verticales.**  Vuelve a obtener los píxeles adicionales ocultando la barra de título del explorador, en pestañas verticales. A partir Microsoft Edge versión 93, puedes ir a edge://settings/appearance y, en la sección Personalizar barra de herramientas, selecciona la opción para ocultar la barra de título mientras estás en modo pestaña vertical.

- **Imagen de vídeo en imagen (PiP) desde la barra de herramientas activable.**  A partir Microsoft Edge versión 93, será aún más fácil entrar en modo Imagen en imagen (PiP). Al mantener el mouse sobre un vídeo compatible, aparecerá una barra de herramientas que le permite ver ese vídeo en una ventana de PiP.  Nota: esta opción está disponible actualmente para Microsoft Edge usuarios en macOS.  Revierta en breve mientras continuamos nuestra implementación para Windows usuarios.

- **Eliminación de 3DES en TLS.**  A partir Microsoft Edge versión 93, se quitará la compatibilidad TLS_RSA_WITH_3DES_EDE_CBC_SHA conjunto de cifrado. Este cambio se produce en el proyecto Chromium, en el que se basa Microsoft Edge. Para obtener más información, vaya a la entrada [Estado de la plataforma de Chrome](https://chromestatus.com/feature/6678134168485888). Además, en Microsoft Edge versión 93, la directiva [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) estará disponible para admitir escenarios que necesitan conservar la compatibilidad con servidores obsoletos. Esta directiva de compatibilidad quedará obsoleta y dejará de funcionar en Microsoft Edge versión 95. Asegúrese de actualizar los servidores afectados antes de ese momento.

- **Directivas para omitir los avisos de ClickOnce y DirectInvoke.**  Hemos actualizado nuestras directivas para habilitar la omisión de los mensajes de ClickOnce y la aplicación de DirectInvoke para los tipos de archivo especificados, desde dominios especificados. Para ello, tendrá que:

  - Habilitar [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) o [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Habilitar la directiva [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) y establecer la lista de tipos de archivo específicos para los que ClickOnce y DirectInvoke deben estar deshabilitados.
  - Habilitar la [directiva AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) y establecer la lista de dominios específicos para los que ClickOnce y DirectInvoke se deshabilitarán

  Nota: AutoOpenAllowedForURLs es una directiva de apoyo para AutoOpenFileTypes. Si AutoOpenAllowedForURLs no está establecido y AutoOpenFileTypes está establecido, los tipos de archivo enumerados se abrirán automáticamente desde todas las direcciones URL.

### <a name="new-policies"></a>Nuevas directivas

- [AutoplayAllowlist](/DeployEdge/microsoft-edge-policies#autoplayallowlist) Permitir reproducción automática de medios en sitios específicos
- [CECPQ2Enabled](/DeployEdge/microsoft-edge-policies#cecpq2enabled) CECPQ2 post-quantum key-agreement enabled for TLS
- [ConfigureViewInFileExplorer](/DeployEdge/microsoft-edge-policies#configureviewinfileexplorer) Configurar la característica Ver en el Explorador de archivos para SharePoint páginas en Microsoft Edge
- [DefaultJavaScriptJitSetting](/DeployEdge/microsoft-edge-policies#defaultjavascriptjitsetting) Controlar el uso de JIT de JavaScript
- [ShowPDFDefaultRecommendationsEnabled](/DeployEdge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled) Permitir que las notificaciones establezcan Microsoft Edge como lector de PDF predeterminado
- [FeatureFlagOverridesControl](/DeployEdge/microsoft-edge-policies#featureflagoverridescontrol) Configurar la capacidad de los usuarios para invalidar las marcas de características
- [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled) Habilitar el inicio de sesión implícito
- [InternetExplorerIntegrationCloudSiteList](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) Configurar la lista Enterprise sitio en la nube del modo de almacenamiento
- [InternetExplorerIntegrationSiteListRefreshInterval](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) Configurar la frecuencia con la que se actualiza Enterprise lista de sitios de modo de actualización
- [JavaScriptJitAllowedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitallowedforsites) Permitir que JavaScript use JIT en estos sitios
- [JavaScriptJitBlockedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitblockedforsites) Impedir que JavaScript use JIT en estos sitios
- [LocalBrowserDataShareEnabled](/DeployEdge/microsoft-edge-policies#localbrowserdatashareenabled) Habilitar Windows buscar datos de exploración Microsoft Edge local
- [MAUEnabled](/DeployEdge/microsoft-edge-policies#mauenabled) Use siempre Microsoft AutoUpdate como actualizador para Microsoft Edge
- [MSAWebSiteSSOUsingThisProfileAllowed](/DeployEdge/microsoft-edge-policies#msawebsitessousingthisprofileallowed) Permitir el inicio de sesión único para sitios de Microsoft con este perfil
- [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) OneAuth Authentication Flow Se aplica para el inicio de sesión
- [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) Permitir a los usuarios obtener una sugerencia de contraseña segura siempre que creen una cuenta en línea
- [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) Configura una configuración que pide a los usuarios que escriban la contraseña del dispositivo mientras usan el autorrelleno de contraseñas
- [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) Establece el diseño para la impresión
- [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) Permitir depuración remota
- [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) Establecer el intervalo de tiempo para el relanzamiento
- [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) Habilitar asistencia para viajes
- [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) Habilitar conjuntos de cifrado 3DES en TLS

#### <a name="deprecated-policy"></a>Directivas en desuso

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Habilitar la configuración predeterminada del comportamiento de cookies samesite heredada

#### <a name="obsoleted-policy"></a>Directiva obsoleta

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Configurar la nueva Microsoft Edge página de pestañas

#### <a name="additional-change"></a>Cambio adicional

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Agregar compatibilidad con plataforma mac

## <a name="version-93096118-august-10"></a>Versión 93.0.961.18: 10 de agosto

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-92090262-july-29"></a>Versión 92.0.902.62: 29 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-92090255-july-21"></a>Versión 92.0.902.55: 21 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-92090245-july-12"></a>Versión 92.0.902.45: 12 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-92090240-july-6"></a>Versión 92.0.902.40: 6 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-92090222-june-21"></a>Versión 92.0.902.22: 21 de junio

### <a name="feature-updates"></a>Actualizaciones de características

- **Búsqueda de idioma natural para el historial del explorador en la barra de direcciones**. Encontrar el artículo o sitio web que está buscando ahora es más fácil gracias a la búsqueda de idioma natural directamente desde la barra de direcciones. Puedes encontrar resultados de búsqueda basados en el contenido/descripción/sincronización de la página (como "receta de pastel de la semana pasada") además de solo títulos/coincidencias de palabras clave url.
Tenga en cuenta que se trata de un lanzamiento de características controlado. Si no ve esta característica, vuelva a comprobar en breve, ya que continuaremos con el lanzamiento.

- **Los usuarios pueden obtener fácilmente el modo de Internet Explorer en Microsoft Edge**. A partir de Microsoft Edge versión 92, los usuarios pueden volver a cargar un sitio en el modo de Internet Explorer en Microsoft Edge en lugar de confiar en la aplicación independiente de IE 11 mientras esperan a que se configure un sitio en la lista de sitios del Modo de empresa. Se pedirá a los usuarios que agreguen el sitio a su lista de sitios locales, de modo que navegar a la misma página en Microsoft Edge se representará automáticamente en el modo IE durante los próximos 30 días. Puede usar la directiva *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* para configurar esta experiencia y permitir el acceso a los puntos de entrada del modo IE, así como la capacidad de agregar sitios a la lista de sitios locales. Puede usar la directiva *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* para ajustar el número de días para mantener los sitios en la lista de sitios locales.
Tenga en cuenta que es necesario KB5003698 o posterior para Windows 10, versión 1909; o es necesario KB5003690 o posterior para Windows 10, versión 2004, Windows 10, versión 20H2 o Windows 10, versión 21H1 para la experiencia de un extremo a otro.

- **Los archivos MHTML se abrirán de forma predeterminada en el modo de Internet Explorer**. A partir de Microsoft Edge versión 92 estable, los tipos de archivo MHTML se abrirán automáticamente en modo de Internet Explorer en Microsoft Edge en lugar de en la aplicación de Internet Explorer (IE11). Esto se observa con más frecuencia al intentar ver los correos electrónicos de Outlook en un explorador. Este cambio solo se producirá si IE11 es el controlador predeterminado para este tipo de archivo. Si prefiere cambiar esto, puede hacerlo antes de instalar la actualización de la versión 92 estable con [esta guía](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **Los instrumentos de pago ahora se sincronizan entre dispositivos**. A partir de Microsoft Edge versión 92, tiene la opción de sincronizar la información de pago entre los dispositivos en los que haya iniciado sesión.
Tenga en cuenta que se trata de un lanzamiento de características controlado. Si no ves esta característica, vuelve en breve mientras continuamos nuestra implementación.

- **La advertencia "Deshabilitar las extensiones del modo de desarrollador" puede descartarse permanentemente**. A partir de Microsoft Edge versión 92, puede deshabilitar la advertencia "Deshabilitar las extensiones del modo de desarrollador" haciendo clic en la opción "No volver a mostrar".
Tenga en cuenta que se trata de un lanzamiento de características controlado. Si no ves esta característica, vuelve en breve mientras continuamos nuestra implementación.

- **Administre las extensiones desde la barra de herramientas**. El nuevo menú de extensiones de la barra de herramientas le permite ocultar y anclar extensiones fácilmente. Los vínculos rápidos para administrar extensiones y buscar nuevas le permitirán encontrar fácilmente nuevas extensiones y administrar las existentes.
Tenga en cuenta que se trata de un lanzamiento de características controlado. Si no ves esta característica, vuelve en breve mientras continuamos nuestra implementación.

- **HTTPS automático**. Los usuarios tendrán la opción de actualizar la navegación de HTTP a HTTPS en dominios que probablemente admitan este protocolo más seguro. Esta compatibilidad también se puede configurar para intentar la entrega a través de HTTPS para todos los dominios.
Tenga en cuenta que estamos experimentando con esta característica y este comportamiento no se verá si ha optado por no participar en los experimentos.

- **Mejoras en la representación de fuentes**. Se han realizado mejoras en la representación del texto para mejorar la claridad y reducir el desenfoque.
Tenga en cuenta que se trata de un lanzamiento de características controlado. Si no ves esta característica, vuelve en breve mientras continuamos nuestra implementación.

### <a name="policy-updates"></a>Actualizaciones de directiva

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado ocho directivas nuevas. Descargue las Plantillas administrativas actualizadas desde la [página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se agregaron las siguientes directivas nuevas:

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) Inicio de sesión único para sitios profesionales o educativos con este perfil habilitado.
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configurar HTTPS automático
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Controlar el uso del modo de equipo sin periféricos
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Especificar si se permite que los sitios web inseguros realicen solicitudes a puntos de conexión de red más privados
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Permitir que los sitios enumerados realicen solicitudes a puntos de conexión de red más privados desde contextos inseguros
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Especificar el número de días que un sitio permanece en la lista de sitios del modo IE local
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Permitir que los sitios no configurados se vuelvan a cargar en el modo de Internet Explorer
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Especificar si SharedArrayBuffers se puede usar en un contexto no aislado entre orígenes

#### <a name="obsoleted-policy"></a>Directiva obsoleta

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Permite certificados firmados usando SHA-1 cuando sean emitidos por anclajes de veracidad locales.

## <a name="version-9209029-june-8"></a>Versión 92.0.902.9: 8 de junio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086441-june-3"></a>Versión 91.0.864.41: 3 de junio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086437-may-27"></a>Versión 91.0.864.37: 27 de mayo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086436-may-26"></a>Versión 91.0.864.36: 26 de mayo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086433-may-21"></a>Versión 91.0.864.33: 21 de mayo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086427-may-14"></a>Versión 91.0.864.27: 14 de mayo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086419-may-7"></a>Versión 91.0.864.19: 7 de mayo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086415-may-3"></a>Versión 91.0.864.15: 3 de mayo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086411-april-30"></a>Versión 91.0.864.11: 30 de abril

### <a name="feature-updates"></a>Actualizaciones de características

- **Identifique el tráfico de red que se origina en contenedores de Protección de aplicaciones de Microsoft Defender en el nivel de proxy**. A partir de Microsoft Edge versión 91, hay compatibilidad integrada para etiquetar el tráfico de red procedente de contenedores de Protección de aplicaciones, lo que permite a las empresas identificarlos y aplicar directivas específicas.

- **Opción de compatibilidad para permitir la sincronización de Favoritos desde el host al contenedor de Protección de aplicaciones de Edge**. A partir de Microsoft Edge versión 91, los usuarios tienen la opción de configurar Protección de aplicaciones para sincronizar sus favoritos desde el host al contenedor. Esto garantiza que los nuevos favoritos aparezcan también en el contenedor.

- **Compatibilidad con las API de reconocimiento de voz**. A partir de Microsoft Edge versión 91, se agregará compatibilidad de API para los comandos de reconocimiento de voz en Google.com y sitios similares. Esta característica se limita a un grupo de usuarios seleccionados al azar que han permitido la experimentación. Estos usuarios proporcionan comentarios al equipo de características.

- **Personalice el explorador con nuevos colores de tema**. Personalice Microsoft Edge con uno de los catorce nuevos colores de tema en Configuración -> Apariencia de la página. También puede instalar temas personalizados desde el sitio del complemento de Microsoft Edge. [Obtener más información](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- **Interrumpir descargas** A partir de Microsoft Edge versión 91, el explorador interrumpirá automáticamente las descargas de tipos que podrían dañar el equipo si esas descargas se inician sin una interacción del usuario y no son compatibles con la comprobación de Reputación de aplicación SmartScreen. Los usuarios pueden invalidar y seguir descargando haciendo clic con el botón secundario y seleccionando "Mantener" en el elemento de descarga.
Los administradores de empresa pueden optar por no participar en este comportamiento con una de estas dos directivas:
    - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) Deshabilita las advertencias basadas en la extensión del tipo de archivo de descarga para los tipos de archivo especificados en los dominios. Para obtener más información, consulte [Interrupciones de descargas de Seguridad de Microsoft Edge](/deployedge/microsoft-edge-security-downloads-interruptions)

### <a name="policy-updates"></a>Actualizaciones de directiva

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado seis directivas nuevas. Descargue las Plantillas administrativas actualizadas desde la [página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se agregaron las siguientes directivas nuevas:

- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled): identificación del tráfico de Protección de aplicaciones
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports): puertos de red permitidos explícitamente
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings): permitir la importación de la configuración de página de inicio
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled): permitir a los usuarios hacer un recorte de un problema matemático y obtener la solución con una explicación paso a paso en Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled): permitir contenido de Microsoft News en la página de nueva pestaña
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled): permitir vínculos rápidos en la página de nueva pestaña

#### <a name="obsoleted-policy"></a>Directiva obsoleta

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled): habilitar la autenticación proactiva
<!-- end major 91 -->

## <a name="version-90081846-april-22"></a>Versión 90.0.818.46: 22 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081842-april-20"></a>Versión 90.0.818.42: 20 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081841-april-16"></a>Versión 90.0.818.41: 16 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081838-april-14"></a>Versión 90.0.818.38: 14 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081836-april-12"></a>Versión 90.0.818.36: 12 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081827-april-2"></a>Versión 90.0.818.27: 2 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081822-march-29"></a>Versión 90.0.818.22: 29 de marzo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081814-march-22"></a>Versión 90.0.818.14: 22 de marzo

Se han corregido varios errores y problemas de rendimiento.
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>Versión 90.0.818.8: 16 de marzo

### <a name="feature-updates"></a>Actualizaciones de características

- **El inicio de sesión único (SSO) ya está disponible para las cuentas de Azure Active Directory (Azure AD) y las cuentas de Microsoft (MSA) en macOS.** Un usuario que haya iniciado sesión en Microsoft Edge en macOS ahora tendrá la sesión iniciada de manera automática en los sitios web que estén configurados para permitir el inicio de sesión único con cuentas profesionales y de Microsoft (por ejemplo, bing.com, office.com, msn.com y outlook.com).

- **Pantalla completa.** A partir de Microsoft Edge versión 90, hemos bloqueado la configuración de impresión de la interfaz de usuario para permitir solo las impresoras configuradas y las opciones "Imprimir en PDF". También hemos realizado mejoras en la pantalla completa de una sola aplicación de acceso asignado para restringir el inicio de otras aplicaciones desde el explorador. Para obtener más información sobre las características de pantalla completa, consulte [aquí](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Impresión:**

  - **Modo de rasterización de impresión nuevo para las impresoras que no son PostScript**. A partir de la versión 90 de Microsoft Edge, los administradores pueden usar una nueva directiva para definir el modo de rasterización de impresión para sus usuarios. Esta directiva controla la forma en que Microsoft Edge imprime en impresoras que no sean PostScript en Windows.  En ocasiones, es necesario rasterizar los trabajos de impresión de impresoras que no sean PostScript para que se impriman correctamente. Las opciones de impresión son Completa y Rápida.

  - **Opciones de escala de página adicionales para la impresión**. Los usuarios ahora pueden personalizar el ajuste de escala al imprimir páginas web y documentos PDF con opciones adicionales. La opción "Ajustar a la página" garantiza que la página web o el documento se ajusta al espacio disponible en el "Tamaño de papel" seleccionado para la impresión. La opción "Tamaño real" garantiza que no se imprima ningún cambio en el tamaño del contenido, independientemente de la opción "Tamaño de papel" seleccionada.

- **Productividad:**

  - **Las sugerencias de Autorrellenar se extienden para incluir contenido de campos de dirección del portapapeles**. El contenido del Portapapeles se analiza cuando hace clic en un campo de perfil o dirección (por ejemplo, teléfono, correo electrónico, código postal, ciudad, estado, etc.) para mostrarlo como sugerencias de autorrelleno.

  - **Los usuarios pueden buscar sugerencias de autorrellenar incluso si no se detecta un formulario o campo**. Ahora, si tiene guardada la información en Microsoft Edge, las sugerencias de autorrelleno aparecerán automáticamente y le ayudarán a ahorrar tiempo al rellenar formularios. En casos en los que autorrellenar no encuentra un formulario, o si quiere capturar datos en formularios que normalmente no tienen autorrellenar (como formularios temporales), puede buscar la información con autorrellenar.

- **Acceda a las descargas desde un control flotante de la barra de menús**. Las descargas se mostrarán en la esquina superior derecha con todas las descargas activas en un solo lugar. Este menú se puede descartar fácilmente para que los usuarios puedan continuar explorando sin interrupciones y pueden supervisar el progreso de descarga general directamente desde la barra de herramientas. [Obtenga más información](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).


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

<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
