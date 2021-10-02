---
title: Notas de la versión de Microsoft Edge para el canal estable
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 10/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de la versión de Microsoft Edge para el canal estable
ms.openlocfilehash: f15c8e1d4dcd037b0948e7309387ba3baa5d1ffa
ms.sourcegitcommit: 2bf511511f131b8497b3e162c44286c217508885
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2021
ms.locfileid: "12057346"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Notas de la versión para el canal estable de Microsoft Edge

Estas notas de versión proporcionan información sobre las nuevas características y las actualizaciones no relacionadas con la seguridad que se incluyen en el canal estable de Microsoft Edge.

- Todas las actualizaciones de seguridad se muestran [aquí](microsoft-edge-relnotes-security.md).
- Las notas de la versión archivadas para el Canal estable de Microsoft Edge se encuentran [aquí](microsoft-edge-relnote-archive-stable-channel.md).

 Para entender los canales de Microsoft Edge, vea la [Información general sobre los canales de Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Para el Canal estable, las actualizaciones se implementarán de manera progresiva en uno o más días. Para más información, consulte [Implementaciones progresivas de actualizaciones de Microsoft Edge](microsoft-edge-update-progressive-rollout.md).
>
> Microsoft Edge La plataforma web evoluciona constantemente para mejorar la experiencia del usuario, la seguridad y la privacidad. Para más información, consulte [Cambios que afectan a la compatibilidad del sitio próximamente en Microsoft Edge](/ microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-94099238-october-1"></a>Versión 94.0.992.38: 1 de octubre

> [!Important]
> Esta actualización contiene una corrección para [CVE-2021-37975](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37975) y [CVE-2021-37976](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37976), que el equipo de Chromium ha notificado que contienen una vulnerabilidad de seguridad. Para obtener más información, vea la [Guía de actualizaciones de seguridad](https://msrc.microsoft.com/update-guide)

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#october-01-2021).

## <a name="version-94099237-september-30"></a>Versión 94.0.992.37: 30 de septiembre

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-94099231-september-24"></a>Versión 94.0.992.31: 24 de septiembre

> [!Important]
> Esta actualización contiene una corrección para [CVE-2021-37973](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37973) que el equipo de Chromium ha notificado que tiene una vulnerabilidad de seguridad. Para más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide).

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#september-24-2021).

### <a name="feature-updates"></a>Actualizaciones de características

- **Microsoft Edge ha completado el paso a una cadencia de 4 semanas para actualizaciones.**  Hemos adoptado un nuevo ciclo de lanzamiento de 4 semanas para las versiones principales. Más información aquí: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Nueva opción Estable extendida que se ofrece.**  Ofrecemos una nueva opción Estable extendida a nuestros clientes de empresa administrados. La opción Estable extendida se mantendrá en revisiones numeradas uniformes y se actualizará cada 8 semanas. Habrá una actualización de seguridad quincenal.  Información adicional aquí: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Mejoras en el comportamiento predeterminado de abrir archivos MHTML.**  Los archivos MHTML seguirán abriéndose en modo IE si el modo IE está habilitado, a menos que el archivo MHTML se haya guardado desde Microsoft Edge (mediante las opciones Guardar como o Guardar página como en Microsoft Edge). Si el archivo se guardó desde Microsoft Edge, ahora se abrirá en Microsoft Edge.  Este cambio corregirá un problema de representación observado al abrir un archivo MHTML en modo IE cuando se guarda desde Microsoft Edge.

- **Restringir las solicitudes de red privada a contextos seguros.** El acceso a recursos en redes locales (intranet) desde páginas de Internet requiere que esas páginas se entreguen a través de HTTPS. Este cambio se produce en el proyecto Chromium, en el que se basa Microsoft Edge. Para más información, vaya a la entrada [Estado de la plataforma de Chrome](https://chromestatus.com/feature/5436853517811712). Hay dos directivas de compatibilidad disponibles para admitir escenarios que necesitan conservar la compatibilidad con páginas no seguras: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) y [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Bloquear descargas de contenido mixto.** Las páginas seguras solo descargarán archivos hospedados en otras páginas seguras y las descargas hospedadas en páginas no seguras (que no son HTTPS) se bloquearán si se inician desde una página segura. Este cambio se produce en el proyecto Chromium, en el que se basa Microsoft Edge. Para más información, vaya a la [entrada del blog de seguridad de Google.](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html)

- **Habilitar el inicio de sesión implícito para cuentas locales.** Al habilitar la directiva [OnlyOnPremisesImplicitSigninEnabled](/deployedge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled), solo se habilitarán las cuentas locales para el inicio de sesión implícito.  Microsoft Edge no intentará iniciar sesión implícitamente en cuentas de MSA o AAD. También se detendrán las actualizaciones de cuentas locales a cuentas de AAD.

- **Nueva página de configuración de accesibilidad.**  Hemos unido la configuración relacionada con la accesibilidad en una sola página. Puede encontrar la nueva página edge://settings/accessibility en la lista de configuración principal. Aquí puede encontrar la configuración para aumentar el tamaño de la página web, mostrar un esquema de alta visibilidad en torno al área de enfoque y otras opciones de configuración que pueden ayudar a mejorar su experiencia de exploración web. Seguiremos agregando nuevas opciones de configuración aquí en versiones futuras de Microsoft Edge.

***Nuevas directivas***

- 
            [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Ignorar la configuración de la lista de sitios de Protección de aplicaciones y navegar en Microsoft Edge con normalidad
- 
            [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Solo cuenta local habilitada para el inicio de sesión implícito
- 
            [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Habilitar la compatibilidad con las reglas de tabla de enrutamiento del sistema operativo Windows al realizar conexiones punto a punto a través de WebRTC

***Directiva obsoleta***

- 
            [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) Habilitar la característica User-Agent Client Hints (en desuso).

## <a name="version-93096152-september-16"></a>Versión93.0.961.52: 16 de septiembre

>[!Important]
>Esta actualización contiene una corrección para [CVE-2021-30633](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632), que el equipo de Chromium ha notificado como una vulnerabilidad de seguridad. Para más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide).

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#september-16-2021).

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

## <a name="version-91086471-july-19"></a>Versión91.0.864.71: 19 de julio

> [!Important]
>Esta actualización contiene una corrección para [CVE-2021-30563](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563), que el equipo de Chromium ha notificado como una vulnerabilidad de seguridad. Para obtener más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#july-19-2021).

## <a name="version-91086467-july-8"></a>Versión 91.0.864.67: 8 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086464-july-2"></a>Versión 91.0.864.64: 2 de julio

Se han corregido varios errores y problemas de rendimiento.

## <a name="version-91086459-june-24"></a>Versión 91.0.864.59: 24 de junio

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#june-24-2021).

## <a name="version-91086454-june-18"></a>Versión91.0.864.54: 18 de junio

> [!Important]
> Esta actualización contiene una corrección para [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554), que el equipo de Chromium ha notificado como una vulnerabilidad de seguridad. Para obtener más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Las actualizaciones de seguridad del canal estable se muestran [aquí](/deployedge/microsoft-edge-relnotes-security#june-18-2021).

## <a name="version-91086448-june-11"></a>Versión91.0.864.48: 11 de junio

> [!Important]
>Esta actualización contiene una corrección para [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551), que el equipo de Chromium ha notificado como una vulnerabilidad de seguridad. Para obtener más información, consulte la [Guía de actualización de seguridad](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

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

<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
