---
title: Notas de la versión de Microsoft Edge para el canal beta
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 07/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas de la versión de Microsoft Edge para el canal beta
ms.openlocfilehash: d5e4a4807a12cfd50cd0efaeab672361c68a1508
ms.sourcegitcommit: e3a30351b02226aa042153f17636d64a12c4518b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/12/2021
ms.locfileid: "11643946"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de la versión para el canal beta de Microsoft Edge

Estas notas de versión proporcionan información sobre las nuevas características y las actualizaciones no relacionadas con la seguridad que se incluyen en el canal beta de Microsoft Edge. Las versiones archivadas de estas notas de la versión están [aquí](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> La plataforma web de Microsoft Edge evoluciona constantemente para mejorar la experiencia del usuario, la seguridad y la privacidad. Para más información, vea [Cambios que afectan a la compatibilidad del sitio que llegan a Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-92090245-july-12"></a>Versión 92.0.902.45: 12 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-92090240-july-6"></a>Versión 92.0.902.40: 6 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-92090222-june-21"></a>Versión 92.0.902.22: 21 de junio

### <a name="feature-updates"></a>Actualizaciones de características

- **Búsqueda de idioma natural para el historial del explorador en la barra de direcciones**. Encontrar el artículo o sitio web que está buscando ahora es más fácil gracias a la búsqueda de idioma natural directamente desde la barra de direcciones. Puedes encontrar resultados de búsqueda basados en el contenido/descripción/sincronización de la página (como "receta de pastel de la semana pasada") además de solo títulos/coincidencias de palabras clave url.
Tenga en cuenta: se trata de una implementación de características controladas. Si no ve esta característica, vuelva a comprobar en breve, ya que continuaremos con el lanzamiento.

- **Los usuarios pueden obtener fácilmente el modo de Internet Explorer en Microsoft Edge**. A partir de Microsoft Edge versión 92, los usuarios pueden volver a cargar un sitio en el modo de Internet Explorer en Microsoft Edge en lugar de confiar en la aplicación independiente de IE 11 mientras esperan a que se configure un sitio en la lista de sitios del Modo de empresa. Se pedirá a los usuarios que agreguen el sitio a su lista de sitios locales, de modo que navegar a la misma página en Microsoft Edge se representará automáticamente en el modo IE durante los próximos 30 días. Puede usar la directiva *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* para configurar esta experiencia y permitir el acceso a los puntos de entrada del modo IE, así como la capacidad de agregar sitios a la lista de sitios locales. Puede usar la directiva *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* para ajustar el número de días para mantener los sitios en la lista de sitios locales.
Tenga en cuenta que es necesario KB5003698 o posterior para Windows 10, versión 1909; o es necesario KB5003690 o posterior para Windows 10, versión 2004, Windows 10, versión 20H2 o Windows 10, versión 21H1 para la experiencia de un extremo a otro.

- **Los archivos MHTML se abrirán de forma predeterminada en el modo de Internet Explorer**. A partir de Microsoft Edge versión 92 estable, los tipos de archivo MHTML se abrirán automáticamente en modo de Internet Explorer en Microsoft Edge en lugar de en la aplicación de Internet Explorer (IE11). Esto se observa con más frecuencia al intentar ver los correos electrónicos de Outlook en un explorador. Este cambio solo se producirá si IE11 es el controlador predeterminado para este tipo de archivo. Si prefiere cambiar esto, puede hacerlo antes de instalar la actualización de la versión 92 estable con [esta guía](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **Los instrumentos de pago ahora se sincronizan entre dispositivos**. A partir de Microsoft Edge versión 92, tiene la opción de sincronizar la información de pago entre los dispositivos en los que haya iniciado sesión.
Tenga en cuenta: se trata de una implementación de características controladas. Si no ve esta característica, vuelva a comprobar en breve, ya que continuaremos con el lanzamiento.

- **La advertencia "Deshabilitar las extensiones del modo de desarrollador" puede descartarse permanentemente**. A partir de Microsoft Edge versión 92, puede deshabilitar la advertencia "Deshabilitar las extensiones del modo de desarrollador" haciendo clic en la opción "No volver a mostrar".
Tenga en cuenta: se trata de una implementación de características controladas. Si no ve esta característica, vuelva a comprobar en breve, ya que continuaremos con el lanzamiento.

- **Administre las extensiones desde la barra de herramientas**. El nuevo menú de extensiones de la barra de herramientas le permite ocultar y anclar extensiones fácilmente. Los vínculos rápidos para administrar extensiones y buscar nuevas le permitirán encontrar fácilmente nuevas extensiones y administrar las existentes.
Tenga en cuenta: se trata de una implementación de características controladas. Si no ve esta característica, vuelva a comprobar en breve, ya que continuaremos con el lanzamiento.

- **HTTPS automático**. Los usuarios tendrán la opción de actualizar la navegación de HTTP a HTTPS en dominios que probablemente admitan este protocolo más seguro. Esta compatibilidad también se puede configurar para intentar la entrega a través de HTTPS para todos los dominios.
Tenga en cuenta que estamos experimentando con esta característica y este comportamiento no se verá si ha optado por no participar en los experimentos.

- **Mejoras en la representación de fuentes**. Se han realizado mejoras en la representación del texto para mejorar la claridad y reducir el desenfoque.
Tenga en cuenta: se trata de una implementación de características controladas. Si no ve esta característica, vuelva a comprobar en breve, ya que continuaremos con el lanzamiento.

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

- **Compatibilidad con las API de reconocimiento de voz**. A partir de Microsoft Edge versión 91, se agregará compatibilidad de API para los comandos de reconocimiento de voz en Google.com y sitios similares. Esta característica se limita a un grupo de usuarios seleccionados al azar que han habilitado la experimentación. Estos usuarios proporcionan comentarios al equipo de características.

- **Personalice el explorador con nuevos colores de tema**. Personalice Microsoft Edge con uno de los catorce nuevos colores de tema en Configuración -> Apariencia de la página. También puede instalar temas personalizados desde el sitio del complemento de Microsoft Edge. [Obtener más información](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- **Interrumpir descargas** A partir de Microsoft Edge versión 91, el explorador interrumpirá automáticamente las descargas de tipos que podrían dañar el equipo si esas descargas se inician sin una interacción del usuario y no son compatibles con la comprobación de Reputación de aplicación SmartScreen. Los usuarios pueden invalidar y continuar con la descarga haciendo clic con el botón derecho y eligiendo "Mantener" en el elemento de descarga.
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
