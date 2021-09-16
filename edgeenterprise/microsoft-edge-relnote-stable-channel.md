---
title: Notas de la versión de Microsoft Edge para el canal estable
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 09/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de la versión de Microsoft Edge para el canal estable
ms.openlocfilehash: e13778ee9a93a4621ad77a00da1d85def3f97225
ms.sourcegitcommit: 6eefb7cb134f25a1e2d1f515a3a8600524a4b6e3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2021
ms.locfileid: "12017974"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Notas de la versión para el canal estable de Microsoft Edge

Estas notas de versión proporcionan información sobre las nuevas características y las actualizaciones no relacionadas con la seguridad que se incluyen en el canal estable de Microsoft Edge.

- Todas las actualizaciones de seguridad se muestran [aquí](microsoft-edge-relnotes-security.md).
- Las notas de la versión archivadas para el Canal estable de Microsoft Edge se encuentran [aquí](microsoft-edge-relnote-archive-stable-channel.md).

 Para entender los canales de Microsoft Edge, vea la [Información general sobre los canales de Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Para el Canal estable, las actualizaciones se implementarán de manera progresiva en uno o más días. Para más información, consulte [Implementaciones progresivas de actualizaciones de Microsoft Edge](microsoft-edge-update-progressive-rollout.md).
>
> Microsoft Edge La plataforma web evoluciona constantemente para mejorar la experiencia del usuario, la seguridad y la privacidad. Para más información, vea [Cambios que afectan a la compatibilidad del sitio que llegan a Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-93096147-september-11"></a>Versión 93.0.961.47: 11 de septiembre

> [!Important]
> Esta actualización contiene una corrección para [CVE-2021-30632](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632), que el equipo de Chromium ha notificado como una vulnerabilidad de seguridad. Para más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide).

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#september-11-2021).

## <a name="version-93096144-september-9"></a>Versión 93.0.961.44: 9 de septiembre

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#september-09-2021).

## <a name="version-93096138-september-2"></a>Versión 93.0.961.38: 2 de septiembre

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#september-02-2021).

### <a name="feature-updates"></a>Actualizaciones de características

- **Preferencias iniciales en Microsoft Edge.**  Microsoft Edge ahora admite un número limitado de preferencias iniciales (anteriormente Preferencias maestras). Los administradores de TI pueden implementar esta configuración como predeterminada antes de que los usuarios ejecuten el explorador por primera vez. Información adicional aquí: configure Microsoft Edge con las [preferencias iniciales para la primera ejecución.](/deployedge/initial-preferences-support-on-microsoft-edge-browser)

- **El modo IE en Microsoft Edge admitirá el comportamiento "sin tiempo de respuesta".**  Para un usuario final, cuando se inicia una nueva ventana del explorador desde una aplicación en modo IE, estará en una sesión independiente, similar al comportamiento de tiempo de respuesta en IE11. Tendrá que ajustar la lista de sitios para configurar los sitios que necesitan evitar el uso compartido de sesiones como "sin tiempo de respuesta". En segundo plano, para cada ventana de Microsoft Edge, la primera vez que se visita una pestaña de modo IE dentro de esa ventana, si es uno de los sitios designados “sin tiempo de respuesta”, esa ventana se bloquea en una sesión de IE sin tiempo de respuesta diferente de todas las demás ventanas de Microsoft Edge al menos hasta que se cierre la última pestaña de “ modo ” IE en esa ventana. Esto se debe al comportamiento anterior en el que los usuarios podían iniciar IE sin tiempo de respuesta y también podían iniciar Microsoft Edge sin tiempo de respuesta a través de otros mecanismos.  Información adicional aquí: [solución de problemas del modo IE y preguntas más frecuentes | Microsoft Docs](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--nomerge--option-that-was-supported-in-internet-explorer-11-)

- **Nueva directiva para detener el inicio de sesión implícito.**  La directiva [ImplicitSignInEnabled](/deployedge/microsoft-edge-policies#implicitsigninenabled) permite a los administradores del sistema deshabilitar el inicio de sesión implícito en Microsoft Edge exploradores.

- **Directivas para omitir los avisos de ClickOnce y DirectInvoke.** Hemos actualizado nuestras directivas para habilitar la omisión de los mensajes de ClickOnce y la aplicación de DirectInvoke para los tipos de archivo especificados, desde dominios especificados. Para ello, tendrá que:

  - Habilitar [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) o [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Habilitar la directiva [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) y establecer la lista de tipos de archivo específicos para los que ClickOnce y DirectInvoke deben estar deshabilitados.
  - Habilitar la directiva [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) y establecer la lista de dominios específicos para los que se deshabilitarán ClickOnce y DirectInvoke.

  Nota: AutoOpenAllowedForURLs es una directiva de apoyo para AutoOpenFileTypes. Si AutoOpenAllowedForURLs no está establecido y AutoOpenFileTypes está establecido, los tipos de archivo enumerados se abrirán automáticamente desde todas las direcciones URL.

- **Grupos de pestañas.**  Estamos activando la agrupación de pestañas, que proporciona la capacidad de clasificar las pestañas en grupos definidos por el usuario y le ayuda a encontrar, cambiar y administrar pestañas de forma más eficaz en varias secuencias de trabajo.  

- **Oculta la barra de título mientras usas pestañas verticales.**  Vuelve a obtener los píxeles adicionales ocultando la barra de título del explorador, en pestañas verticales. Ahora puede ir a edge://settings/appearance y, en la sección Personalizar barra de herramientas, seleccione la opción para ocultar la barra de título en el modo de tabulación vertical.

- **Imagen de vídeo en imagen (PiP) desde la barra de herramientas activable.**  Al mantener el mouse sobre un vídeo compatible, aparecerá una barra de herramientas que le permite ver ese vídeo en una ventana de PiP.  Tenga en cuenta que actualmente está disponible para los usuarios de Microsoft Edge en macOS.  

- **Eliminación de 3DES en TLS. Se quitará la compatibilidad con el conjunto de cifrado TLS_RSA_WITH_3DES_EDE_CBC_SHA.** Este cambio se produce en el proyecto Chromium, en el que se basa Microsoft Edge. Para obtener más información, vaya a la entrada [Estado de la plataforma de Chrome](https://chromestatus.com/feature/6678134168485888). Además, en Microsoft Edge versión 93, la directiva [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) estará disponible para admitir escenarios que necesitan conservar la compatibilidad con servidores obsoletos. Esta directiva de compatibilidad quedará obsoleta y dejará de funcionar en Microsoft Edge versión 95. Asegúrese de actualizar los servidores afectados antes de ese momento.

***Nuevas directivas***

- 
            [AutoplayAllowlist](/DeployEdge/microsoft-edge-policies#autoplayallowlist) Permitir reproducción automática multimedia en sitios específicos
- 
            [CECPQ2Enabled](/DeployEdge/microsoft-edge-policies#cecpq2enabled) Contrato de clave posterior a Quantum de CECPQ2 habilitado para TLS
- 
            [ConfigureViewInFileExplorer](/DeployEdge/microsoft-edge-policies#configureviewinfileexplorer) Configurar la característica Ver en Explorador de archivos para páginas de SharePoint en Microsoft Edge
- 
            [DefaultJavaScriptJitSetting](/DeployEdge/microsoft-edge-policies#defaultjavascriptjitsetting) Controlar el uso de JIT de JavaScript
- 
            [ShowPDFDefaultRecommendationsEnabled](/DeployEdge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled) Permitir que las notificaciones establezcan Microsoft Edge como lector de PDF predeterminado
- 
            [FeatureFlagOverridesControl](/DeployEdge/microsoft-edge-policies#featureflagoverridescontrol) Configurar la capacidad de los usuarios para invalidar las marcas de características
- 
            [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled) Habilitar inicio de sesión implícito
- 
            [InternetExplorerIntegrationCloudSiteList](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) Configurar la lista de sitios en la nube de modo de empresa
- 
            [InternetExplorerIntegrationSiteListRefreshInterval](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) Configurar la frecuencia con la que se actualiza la lista de sitios de modo de empresa
- 
            [JavaScriptJitAllowedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitallowedforsites) Permitir que JavaScript use JIT en estos sitios
- 
            [JavaScriptJitBlockedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitblockedforsites) Impedir que JavaScript use JIT en estos sitios
- 
            [LocalBrowserDataShareEnabled](/DeployEdge/microsoft-edge-policies#localbrowserdatashareenabled) Habilitar Windows para buscar datos de exploración de Microsoft Edge locales
- 
            [MAUEnabled](/DeployEdge/microsoft-edge-policies#mauenabled) Usar siempre Microsoft AutoUpdate como actualizador para Microsoft Edge
- 
            [MSAWebSiteSSOUsingThisProfileAllowed](/DeployEdge/microsoft-edge-policies#msawebsitessousingthisprofileallowed) Permitir el inicio de sesión único para sitios de Microsoft con este perfil
- 
            [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) Flujo de autenticación de OneAuth aplicado para el inicio de sesión
- 
            [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) Permitir a los usuarios obtener una sugerencia de contraseña segura siempre que creen una cuenta en línea
- 
            [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) Configura un ajuste que pide a los usuarios que introduzcan la contraseña de su dispositivo mientras se utiliza el relleno automático de la contraseña
- 
            [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) Establece el diseño para imprimir
- 
            [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) Permitir depuración remota
- 
            [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) Establecer el intervalo de tiempo para reiniciar
- 
            [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) Habilitar asistencia para viajes
- 
            [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) Habilitar conjuntos de cifrado 3DES en TLS
- 
            [WAMAuthBelowWin10RS3Enabled](/DeployEdge/microsoft-edge-policies#wamauthbelowwin10rs3enabled) WAM para la autenticación posterior a Windows 10 RS3 habilitado

***Directivas en desuso***

- 
            [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Habilitar la configuración de comportamiento de cookies de SameSite heredado predeterminado

***Directiva obsoleta***

- 
            [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Configurar la experiencia de la página de pestaña nueva de Microsoft Edge

***Cambio adicional***

- 
            [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Agregar compatibilidad con la plataforma mac
- 
            [PasswordMonitorAllowed](/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) Agregar compatibilidad con la plataforma mac


## <a name="version-92090284-august-26"></a>Versión 92.0.902.84: 26 de agosto

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-92090278-august-19"></a>Versión 92.0.902.78: 19 de agosto

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#august-19-2021).

## <a name="version-92090273-august-12"></a>Versión 92.0.902.73: 12 de agosto

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-92090267-august-5"></a>Versión 92.0.902.67: 5 de agosto

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#august-05-2021).

## <a name="version-92090262-july-29"></a>Versión 92.0.902.62: 29 de julio

Se han corregido varios errores y problemas de rendimiento.

### <a name="modified-policy"></a>Directiva modificada

- AutoplayAllowed: configuración en "Deshabilitado" ahora establece la reproducción automática de medios en "Límite"

## <a name="version-92090255-july-22"></a>Versión 92.0.902.55: 22 de julio

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#july-22-2021).

### <a name="feature-updates"></a>Actualizaciones de características


            **Los usuarios pueden obtener fácilmente el modo de Internet Explorer en Microsoft Edge**. A partir de Microsoft Edge versión 92, los usuarios pueden volver a cargar un sitio en el modo de Internet Explorer en Microsoft Edge en lugar de confiar en la aplicación independiente de IE 11 mientras esperan a que se configure un sitio en la lista de sitios del Modo de empresa. Se pedirá a los usuarios que agreguen el sitio a su lista de sitios locales, de modo que navegar a la misma página en Microsoft Edge se representará automáticamente en el modo IE durante los próximos 30 días. Puede usar la directiva [InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) para configurar esta experiencia y permitir el acceso a los puntos de entrada del modo IE, así como la capacidad de agregar sitios a la lista de sitios locales. Puede usar la directiva [InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) para ajustar el número de días para mantener los sitios en la lista de sitios locales. Tenga en cuenta que es necesario KB5003698 o posterior para Windows 10, versión 1909; o es necesario KB5003690 o posterior para Windows 10, versión 2004, Windows 10, versión 20H2 o Windows 10, versión 21H1 para la experiencia de un extremo a otro. Para más información, vea [Lista de sitios locales en modo IE](/deployedge/edge-ie-mode-local-site-list).


            **Los archivos MHTML se abrirán de forma predeterminada en el modo de Internet Explorer**. A partir de Microsoft Edge versión 92 estable, los tipos de archivo MHTML se abrirán automáticamente en modo de Internet Explorer en Microsoft Edge en lugar de en la aplicación de Internet Explorer (IE11). Esto se observa con más frecuencia al intentar ver los correos electrónicos de Outlook en un explorador. Este cambio solo se producirá si IE11 es el controlador predeterminado para este tipo de archivo. Si prefiere cambiar esto, puede hacerlo antes de instalar la actualización de la versión estable 92 mediante [esta guía](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).


            **La advertencia «Deshabilitar extensiones de modo de desarrollador» puede descartarse durante 2 semanas.** 
           A partir de Microsoft Edge versión 92 puede desactivar la advertencia «Deshabilitar extensiones de modo de desarrollador» durante 2 semanas seleccionando la opción en el desplegable del cuadro de diálogo de la advertencia.


            **Administre las extensiones desde la barra de herramientas**. El nuevo menú de extensiones de la barra de herramientas le permite ocultar y anclar extensiones fácilmente. Los vínculos rápidos para administrar extensiones y buscar nuevas le permitirán encontrar fácilmente nuevas extensiones y administrar las existentes.


            **El valor predeterminado de reproducción automática se establecerá en "Limite"**.  Para ayudarle a concentrase en línea, hemos cambiado el valor predeterminado para la reproducción automática de medios de Limitar a Permitir, empezando por Microsoft Edge versión 92.


            **Los instrumentos de pago ahora se sincronizan entre dispositivos**. A partir de Microsoft Edge versión 92, tiene la opción de sincronizar la información de pago entre los dispositivos en los que haya iniciado sesión. Tenga en cuenta que se trata de un lanzamiento de características controlado. Si no ve esta característica, vuelva a comprobar en breve, ya que continuaremos con el lanzamiento.
Actualmente, esta característica solo está disponible en Estados Unidos y solo para usuarios de MSA (no para AAD)


            **Mejoras en la representación de fuentes**. Se han realizado mejoras en la representación del texto para mejorar la claridad y reducir el desenfoque. Tenga en cuenta que se trata de un lanzamiento de características controlado. Si no ve esta característica, vuelva a comprobar en breve, ya que continuaremos con el lanzamiento.


            **Las características del botón de la barra de herramientas, como Favoritos y Colecciones, recordarán la elección del usuario para anclarlas al lado de la ventana**. Ahora habilitado de forma predeterminada, si el usuario decide anclar un botón de la barra de herramientas, siempre se abrirá en estado anclado hasta que decida desanclar.


            **Los usuarios ahora pueden administrar la opción "Permitir el inicio de sesión único para sitios de trabajo o escuela con este perfil" a través de la directiva de grupo**.  "Permitir el inicio de sesión único para sitios profesionales o educativos con este perfil" permite que los perfiles que no son de AAD puedan usar el inicio de sesión único para sitios profesionales o educativos con credenciales profesionales o educativas presentes en el equipo. Esta opción se muestra para los usuarios finales como un botón de alternancia en Configuración -> Perfiles -> Preferencias de perfil solo para perfiles que no son de AAD.  Puede usar la directiva [AADWebSiteSSOUsingThisProfileEnabled](/deployedge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) para configurar el comportamiento.  


            **Estado de la contraseña** Es importante usar contraseñas seguras y únicas en diferentes cuentas para mantener la seguridad en línea. Sin embargo, esto es más fácil en la teoría que en la práctica y la mayoría de los usuarios muestran hábitos de contraseña deficientes, como usar contraseñas débiles que son fáciles de adivinar, o reutilizar las mismas contraseñas seguras entre cuentas.

Con esta última versión de Microsoft Edge, la tarea de usar contraseñas seguras y únicas se vuelve un poco más fácil. Microsoft Edge le indicará si las contraseñas guardadas son lo suficientemente seguras y si las ha usado en varios sitios, lo que le ayudará a mantenerse más seguro en línea. Puede encontrar la información de estado de la contraseña en la lista de contraseñas guardadas en la página edge://settings/passwords.
  

            **Se agregó privacidad para las contraseñas guardadas** Si usa un dispositivo que comparte con otros usuarios o ha dejado el equipo desbloqueado por cualquier motivo, ahora puede realizar una segunda comprobación con la contraseña del dispositivo para evitar que otros usuarios obtengan acceso a las contraseñas de su sitio web. ¡Es muy simple!


            **Extensión de Outlook**.  Manténgase al corriente de la bandeja Outlook de Microsoft, el calendario, las tareas y mucho más sin tener que abrir una nueva ventana del explorador.  Puede obtener la nueva extensión de Outlook aquí [Microsoft Outlook: complementos de Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/microsoft-outlook/kkpalkknhlklpbflpcpkepmmbnmfailf?hl=en-US)


            **En consonancia con el proyecto de código abierto Chromium, Microsoft Edge está actualizando la forma en que representa tablas en páginas web**. Este cambio corrige problemas conocidos y acerca Microsoft Edge a la manera especificada en que las tablas están diseñadas para representarse en la Web u otros exploradores. Se recomienda probar los flujos de trabajo importantes en su entorno en busca de problemas inesperados. Hay disponible una explicación completa [aquí](https://docs.google.com/document/d/16PFD1GtMI9Zgwu0jtPaKZJ75Q2wyZ9EZnVbBacOfiNA/edit).

### <a name="new-policies"></a>Nuevas directivas

- Inicio de sesión único [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) para sitios de trabajo o escuela con este perfil habilitado
- 
            [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configurar HTTPS automático
- 
            [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Controlar el uso del modo de equipo sin periféricos
- 
            [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Especifica si se permite que los sitios web inseguros realicen solicitudes a puntos de conexión de red más privados.
- 
            [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Permitir que los sitios enumerados realicen solicitudes a puntos de conexión de red más privados desde contextos inseguros
- 
            [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Especificar el número de días que un sitio permanece en la lista de sitios del modo IE local
- 
            [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Permitir que los sitios no configurados se vuelvan a cargar en el modo de Internet Explorer
- 
            [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Especificar si SharedArrayBuffers se puede usar en un contexto no aislado entre orígenes

### <a name="deprecated-policy"></a>Directivas en desuso

- 
            [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) Permitir pruebas de modo de Internet Explorer

### <a name="obsoleted-policy"></a>Directiva obsoleta

- 
            [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Permite certificados firmados usando SHA-1 cuando sean emitidos por anclajes de veracidad locales.

## <a name="version-91086471-july-19"></a>Versión 91.0.864.71: 19 de julio

> [!Important]
>Esta actualización contiene [CVE-2021-30563](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563) que el equipo de Chromium ha notificado que tiene una vulnerabilidad que puede afectar a los usuarios normales. Para más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#july-19-2021).

## <a name="version-91086467-july-8"></a>Versión 91.0.864.67: 8 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086464-july-2"></a>Versión 91.0.864.64: 2 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086459-june-24"></a>Versión 91.0.864.59: 24 de junio

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#june-24-2021).

## <a name="version-91086454-june-18"></a>Versión 91.0.864.54: 18 de junio

> [!Important]
> Esta actualización contiene [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554) que el equipo de Chromium ha notificado que tiene una vulnerabilidad ampliamente conocida. Para más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#june-18-2021).

## <a name="version-91086448-june-11"></a>Versión 91.0.864.48: 11 de junio

> [!Important]
>Esta actualización contiene [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551) que el equipo de Chromium ha notificado que tiene una vulnerabilidad ampliamente conocida. Para más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#june-11-2021).

## <a name="version-91086441-june-3"></a>Versión 91.0.864.41: 3 de junio

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#june-3-2021).

## <a name="version-91086437-may-27"></a>Versión 91.0.864.37: 27 de mayo

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#may-27-2021).

### <a name="feature-updates"></a>Actualizaciones de características

- 
            **Identifique el tráfico de red que se origina en contenedores de Protección de aplicaciones de Microsoft Defender en el nivel de proxy**. A partir de Microsoft Edge versión 91, hay compatibilidad integrada para etiquetar el tráfico de red procedente de contenedores de Protección de aplicaciones, lo que permite a las empresas identificarlos y aplicar directivas específicas.

- 
            **Opción de compatibilidad para permitir la sincronización de Favoritos desde el host al contenedor de Protección de aplicaciones de Edge**. A partir de Microsoft Edge versión 91, los usuarios tienen la opción de configurar Protección de aplicaciones para sincronizar sus favoritos desde el host al contenedor. Esto garantiza que también aparezcan nuevos favoritos en el contenedor.

- 
            **A partir de Microsoft Edge versión 91, el explorador interrumpirá automáticamente las descargas de tipos que podrían dañar el equipo si dichas descargas se inician sin interacción del usuario y no son compatibles con la comprobación de Reputación de aplicación SmartScreen**. Los usuarios pueden invalidar y seguir descargando haciendo clic con el botón secundario y seleccionando "Mantener" en el elemento de descarga. Enterprise administradores pueden optar por no participar en este comportamiento mediante la configuración de la siguiente directiva:
  - 
            [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings:](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md) deshabilitar las advertencias basadas en extensión de tipo de archivo de descarga para tipos de archivo especificados en dominios

    Para obtener más información, [vea Microsoft Edge Security downloads interruptions](microsoft-edge-security-downloads-interruptions.md).

- 
            **Compatibilidad con API de reconocimiento de voz**. A partir de Microsoft Edge versión 91, se agregará compatibilidad de API para los comandos de reconocimiento de voz en Google.com y sitios similares. Esta característica se limita a un grupo de usuarios seleccionados al azar que han permitido la experimentación. Estos usuarios proporcionan comentarios al equipo de características.

- 
            **Personalice el explorador con nuevos colores de tema**. Personalice Microsoft Edge con uno de los catorce nuevos colores de tema en Configuración -> Apariencia de la página. También puede instalar temas personalizados desde el sitio del complemento de Microsoft Edge. [Obtén más información](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

### <a name="policy-updates"></a>Actualizaciones de directivas

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado seis directivas nuevas. Descargue las Plantillas administrativas actualizadas desde la [página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se agregaron las siguientes directivas nuevas:

- 
            [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled): identificación del tráfico de Protección de aplicaciones
- 
            [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports): puertos de red permitidos explícitamente
- 
            [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings): permitir la importación de la configuración de página de inicio
- 
            [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled): permitir a los usuarios hacer un recorte de un problema matemático y obtener la solución con una explicación paso a paso en Microsoft Edge
- 
            [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled): permitir contenido de Microsoft News en la página de nueva pestaña
- 
            [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled): permitir vínculos rápidos en la página de nueva pestaña

#### <a name="obsoleted-policy"></a>Directiva obsoleta

- 
            [ProactiveAuthEnabled:](./microsoft-edge-policies.md#proactiveauthenabled) habilitar la autenticación proactiva
<!-- end major 91 -->

## <a name="version-90081866-may-20"></a>Versión 90.0.818.66: 20 de mayo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081862-may-13"></a>Versión 90.0.818.62: 13 de mayo

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#may-13-2021).

## <a name="version-90081856-may-6"></a>Versión 90.0.818.56: 6 de mayo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081851-april-29"></a>Versión 90.0.818.51: 29 de abril

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#april-29-2021).

## <a name="version-90081849-april-26"></a>Versión 90.0.818.49: 26 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081846-april-22"></a>Versión 90.0.818.46: 22 de abril ##

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#april-22-2021).

## <a name="version-90081842-april-19"></a>Versión 90.0.818.42: 19 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-90081841-april-16"></a>Versión 90.0.818.41: 16 de abril ##

> [!Important]
>Esta actualización contiene [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224) que el equipo de Chromium ha notificado que tiene una vulnerabilidad en estado de desasose. Para más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide).

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#april-16-2021).

## <a name="version-90081839-april-15"></a>Versión 90.0.818.39: 15 de abril ##

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#april-15-2021).

## <a name="feature-updates"></a>Actualizaciones de características ##

-    **El inicio de sesión único (SSO) ya está disponible para las cuentas de Azure Active Directory (Azure AD) y las cuentas de Microsoft (MSA) en macOS.** Un usuario que haya iniciado sesión en Microsoft Edge en macOS ahora tendrá la sesión iniciada de manera automática en los sitios web que estén configurados para permitir el inicio de sesión único con cuentas profesionales y de Microsoft (por ejemplo, bing.com, office.com, msn.com y outlook.com).

- **Pantalla completa.** A partir de Microsoft Edge versión 90, hemos bloqueado la configuración de impresión de la interfaz de usuario para permitir solo las impresoras configuradas y las opciones "Imprimir en PDF". También hemos realizado mejoras en la pantalla completa de una sola aplicación de acceso asignado para restringir el inicio de otras aplicaciones desde el explorador. Para obtener más información acerca de las características del modo quiosco, vaya [aquí](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- 
            **Interrumpir descargas** A partir de Microsoft Edge versión 91, el explorador interrumpirá automáticamente las descargas de tipos que podrían dañar el equipo si dichas descargas se inician sin interacción del usuario y no son compatibles con la comprobación de reputación de la aplicación SmartScreen. Los usuarios pueden invalidar y continuar con la descarga haciendo clic con el botón derecho y eligiendo "Mantener" en el elemento de descarga.
Los administradores de empresa pueden optar por no participar en este comportamiento con una de estas dos directivas:
- 
            [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings:](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) deshabilitar las advertencias basadas en extensiones de tipo de archivo de descarga para tipos de archivo especificados en dominios Para obtener más información, vea [Interrupciones de descargas de Seguridad de Microsoft Edge](/deployedge/microsoft-edge-security-downloads-interruptions)

- 
            **Impresión**:

    - **Modo de rasterización de impresión nuevo para las impresoras que no son PostScript.** A partir de la versión 90 de Microsoft Edge, los administradores pueden usar una nueva directiva para definir el modo de rasterización de impresión para sus usuarios. Esta directiva controla cómo Microsoft Edge se imprime en impresoras que no PostScript en Windows. A veces, los trabajos de impresión en impresoras que no son PostScript deben rasterizarse para imprimirse correctamente. Las opciones de impresión son Completa y Rápida.
    
  - **Opciones de escala de página adicionales para la impresión.** Los usuarios ahora pueden personalizar el ajuste de escala al imprimir páginas web y documentos PDF con opciones adicionales. La opción "Ajustar a la página" garantiza que la página web o el documento se ajusta al espacio disponible en el "Tamaño de papel" seleccionado para la impresión. La opción "Tamaño real" garantiza que no se imprima ningún cambio en el tamaño del contenido, independientemente de la opción "Tamaño de papel" seleccionada.

-   **Productividad:**

    -   **Las sugerencias de Autorrellenar se extienden para incluir contenido de campos de dirección del portapapeles.** El contenido del Portapapeles se analiza cuando hace clic en un campo de perfil o dirección (por ejemplo, teléfono, correo electrónico, código postal, ciudad, estado, etc.) para mostrarlo como sugerencias de autorrelleno.

    -   **Los usuarios pueden buscar sugerencias de autorrellenar incluso si no se detecta un formulario o campo.** Ahora, si tiene guardada la información en Microsoft Edge, las sugerencias de autorrelleno aparecerán automáticamente y le ayudarán a ahorrar tiempo al rellenar formularios. En casos en los que autorrellenar no encuentra un formulario, o si quiere capturar datos en formularios que normalmente no tienen autorrellenar (como formularios temporales), puede buscar la información con autorrellenar.

-   **Descarga de Access desde un control flotante de la barra de menús.** Las descargas se mostrarán en la esquina superior derecha con todas las descargas activas en un solo lugar. Este menú se puede descartar fácilmente para que los usuarios puedan continuar explorando sin interrupciones y pueden supervisar el progreso de descarga general directamente desde la barra de herramientas. 
            [Más información](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

-   **Mejoras en la representación de fuentes.** Empezando por la versión 90 de Microsoft Edge, hemos realizado mejoras en la representación de texto para mejorar la claridad y reducir el efecto borroso. Parte de las mejoras en la representación de fuentes llegarán en la versión beta 90, pero están deshabilitadas de forma predeterminada.

- **Modo niños.** Hemos actualizado la directiva para que, cuando la directiva esté habilitada, deshabilite la característica Modo de niño además de la seguridad de la familia. Más información sobre el modo de [niños aquí](https://go.microsoft.com/fwlink/?linkid=2146910)

## <a name="policy-updates"></a>Actualizaciones de directivas

## <a name="new-policies"></a>Nuevas directivas

Se han agregado ocho directivas nuevas. Descargue las Plantillas administrativas actualizadas desde la [página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se agregaron las siguientes directivas nuevas:
-   
            [ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled): sincronización de favoritos de Protección de aplicaciones habilitada
- 
            [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) Identificación de tráfico de Application Guard
- 
            [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) Puertos de red permitidos explícitamente
- 
            [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) Permitir la importación de la configuración de página de inicio
- 
            [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) Permitir que los usuarios snip un problema de matemáticas y obtener la solución con una explicación paso a paso en Microsoft Edge
- 
            [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) Permitir Microsoft News contenido en la nueva página de pestaña
- 
            [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) Permitir vínculos rápidos en la nueva página de pestañas
-   
            [FetchKeepaliveDurationSecondsOnShutdown:](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown)duración de keepalive de fetch al cerrar
-   
            [ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin): establece valores de configuración administrados para sitios web de orígenes específicos.
-   
            [PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode): modo de rasterización de impresión
-   
            [QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled): administrar la funcionalidad de archivos de Office QuickView en Microsoft Edge
-   
            [SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins): permitir a los usuarios continuar desde la página de advertencia HTTPS de orígenes específicos
-   
            [WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled): habilitar la ocultación de ventanas
-   
            [WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled): Windows Hello para autenticación HTTP habilitado

## <a name="deprecated-policies"></a>Directivas en desuso

- 
            [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled) Habilitar la autenticación proactiva
-   
            [NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled): habilitar la ocultación de ventanas nativas
-   
            [SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin): versión mínima de TLS habilitada

## <a name="version-89077477-april-14"></a>Versión 89.0.774.77: 14 de abril

> [!Important]
>Esta actualización contiene [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) y [CVE-2021-21220,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220) que el equipo de Chromium ha notificado que tiene una vulnerabilidad ampliamente conocida.  Para más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide).

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#april-14-2021).

## <a name="version-89077476-april-12"></a>Versión 89.0.774.76: 12 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077475-april-8"></a>Versión 89.0.774.75: 8 de abril

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077468-april-1"></a>Versión 89.0.774.68: 1 de abril

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#april-1-2021).

## <a name="version-89077463-march-25"></a>Versión 89.0.774.63: 25 de marzo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077457-march-18"></a>Versión 89.0.774.57: 18 de marzo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077454-march-13"></a>Versión 89.0.774.54: 13 de marzo

> [!IMPORTANT]
> Esta actualización contiene [CVE-2021-21193](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193). El equipo de Chromium ha indicado que tiene una vulnerabilidad de seguridad ampliamente conocida. Para más información, vea la [Guía de actualización de Seguridad](https://msrc.microsoft.com/update-guide).

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#march-13-2021).

## <a name="version-89077450-march-10"></a>Versión 89.0.774.50: 10 de marzo

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-89077448-march-8"></a>Versión 89.0.774.48: 8 de marzo

Se han corregido varios errores y problemas de rendimiento.

<!-- begin major 89 -->
## <a name="version-89077445-march-4"></a>Versión 89.0.774.45: 4 de marzo

> [!IMPORTANT]
> Esta actualización contiene [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166), que ha sido reportado por el equipo de Chromium como una vulnerabilidad de seguridad. Para más información, vea la [Guía de actualización de Seguridad](https://msrc.microsoft.com/update-guide).

Las actualizaciones de seguridad del canal estable se muestran [aquí](./microsoft-edge-relnotes-security.md#march-4-2021).

### <a name="resolved-issues"></a>Problemas resueltos

- **Correcciones y actualizaciones de los métodos abreviados del menú Inicio y la barra de tareas:**
  - Al hacer clic con el botón derecho en el acceso directo de Microsoft Edge en el menú Inicio, se mostrará correctamente la opción de desanclar Microsoft Edge de la barra de tareas cuando esté anclado.
  - Los diseños de inicio que incluyen una [configuración de barra de tareas](/windows/configuration/configure-windows-10-taskbar) para anclar Microsoft Edge a la barra de tareas ya no crearán un segundo acceso directo de Microsoft Edge anclado a la barra de tareas.
  - Las organizaciones que usen perfiles de itinerancia de Windows ya no verán un icono en blanco en lugar del icono de Microsoft Edge en la barra de tareas cuando sus usuarios inicien sesión en Windows.

### <a name="feature-updates"></a>Actualizaciones de características

- 
            **El modo de pantalla completa habilita funcionalidades de bloqueo adicionales**. Empezando por la versión 89 de Microsoft Edge, hemos agregado funcionalidades de bloqueo adicionales en el modo de pantalla completa para que los clientes puedan hacer el trabajo con una experiencia más productiva y segura. 
            [Más información](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- 
            **La herramienta Enterprise Mode Site List Manager estará disponible en el explorador a través de la página *edge://compat***. Puede usar esta herramienta para crear, editar y exportar el XML de lista de sitios para el modo de Internet Explorer en Microsoft Edge. Puede habilitar el acceso a esta herramienta según sea necesario con la directiva de grupo. 
            [Más información](./edge-ie-mode-site-list-manager.md).

- 
            **Mejorar el rendimiento del explorador con pestañas en suspensión**. Las pestañas en suspensión mejoran el rendimiento del explorador al poner pestañas inactivas en reposo para liberar recursos del sistema, como la memoria y la CPU, de modo que las pestañas activas u otras aplicaciones puedan usarlos. Los usuarios pueden impedir que los sitios entren en suspensión y configurar el período de tiempo antes de que la pestaña inactiva se suspenda. Para mantener a los usuarios en su flujo, también se utiliza la [heurística](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) para evitar que determinados sitios pasen al modo suspensión, como los sitios de intranet. Esta característica se puede administrar con directivas de grupo.

- 
            **Restablecer manualmente los datos de sincronización de Microsoft Edge en la nube**. Estamos incorporando un método para restablecer los datos de sincronización de Microsoft Edge desde el producto. Esto garantiza que los datos se eliminen de los servicios Microsoft, así como también resuelve ciertos problemas del producto que anteriormente requerían un vale de soporte técnico.

- 
            **Habilitación inteligente del inicio de sesión único (SSO) para todas las cuentas Windows Azure Active Directory (Azure AD) para usuarios con un único perfil de Microsoft Edge que no sea de Azure AD**.  Activa automáticamente esta configuración para los usuarios que podrían beneficiarse más de esta característica. Si un usuario solo tiene un perfil de Microsoft Edge (y no es de Azure AD o el Modo Niños), la configuración se activa automáticamente cuando se inicie Microsoft Edge. Esta alternancia automática también se desactivará automáticamente si más adelante un usuario decide iniciar sesión en un perfil de Microsoft Edge diferente con una cuenta de Azure AD. Los usuarios pueden actualizar manualmente sus preferencias para esta característica en **Configuración > Perfiles >Preferencias de perfil > Permitir el inicio de sesión único para sitios profesionales o educativos con este perfil**.

- 
            **Mejoras en la experiencia de selección de texto en documentos PDF**. Los usuarios obtendrán una experiencia de selección de texto coherente y más fluida en todos los documentos PDF abiertos en Microsoft Edge a partir de la versión 89.

- 
            **El campo Fecha de nacimiento ahora es compatible con la función Autorrellenar.** 
           Actualmente, Microsoft Edge le ayuda a ahorrar tiempo y esfuerzo al rellenar formularios y crear cuentas en línea rellenando automáticamente los datos como direcciones, nombres, números de teléfono, etc. Empezando por la versión 89 de Microsoft Edge, agregamos compatibilidad con otro campo que puede guardar y rellenar automáticamente: la fecha de nacimiento. Puede ver, editar y eliminar esta información en cualquier momento en la configuración de su perfil.

### <a name="policy-updates"></a>Actualizaciones de directiva

#### <a name="new-policies"></a>Nuevas directivas

Se han agregado siete directivas nuevas. Descargue las Plantillas administrativas actualizadas desde la [página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Se han agregado las siguientes directivas nuevas.

- 
            [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime): configuración de la duración de los datos de exploración
- 
            [MAMEnabled](./microsoft-edge-policies.md#mamenabled): administración de aplicaciones móviles habilitada
- 
            [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages): define una lista ordenada de idiomas preferidos que los sitios web deben mostrar si el sitio admite el idioma
- 
            [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled): permite las recomendaciones y notificaciones promocionales de Microsoft Edge
- 
            [PrintingAllowedBackgroundsModesModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes): restringe el modo de impresión de gráficos de fondo
- 
            [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault): modo de impresión de gráficos de fondo predeterminados
- 
            [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist): bloquea acciones inteligentes de una lista de servicios

#### <a name="obsoleted-policies"></a>Directivas obsoletas

Las siguientes directivas están obsoletas.

- 
            [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): usa una directiva de referencia predeterminada de no-referrer-when-downgrade
- 
            [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled): habilita el uso y los informes de datos relacionados con bloqueos
- 
            [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices): envía información de sitios para mejorar los servicios Microsoft
<!-- end major 89 -->

<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Vea también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
