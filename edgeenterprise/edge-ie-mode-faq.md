---
title: Solución de problemas del modo IE y preguntas frecuentes
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/15/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Solución de problemas y preguntas frecuentes para el modo Internet Explorer de Microsoft Edge
ms.openlocfilehash: 77b31362bd7d28598ead7f0a3b33a69f2f4cb264
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470208"
---
# <a name="ie-mode-troubleshooting-and-faq"></a>Solución de problemas del modo IE y preguntas frecuentes

En este artículo se ofrecen consejos para la solución de problemas y una lista de preguntas frecuentes para Microsoft Edge versión 77 o posterior.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.


## <a name="troubleshoot-ie-mode"></a>Solucionar problemas del modo IE

Usa la información de esta sección para diagnosticar y corregir problemas del modo IE.

### <a name="internet-explorer-mode-diagnostic-information"></a>Información de diagnóstico del modo Internet Explorer

Puede obtener información de diagnóstico del modo Internet Explorer en la pestaña Compatibilidad de Microsoft Edge. Para abrir esta pestaña y ver la página de diagnósticos del modo de Internet Explorer, vaya a *edge://compat/iediagnostic*. Es probable que se muestren mensajes de diagnóstico en esta página. En esta página también incluye información de configuración para las siguientes categorías:

- **Comprobación de claves del Registro**. (Solo se muestra si se produce un error en la comprobación). Realiza una comprobación para ver si la integración de Internet Explorer está configurada correctamente en el registro. De no ser así, el usuario puede hacer clic en **Corregir** para solucionar el problema.
- **Modo Internet Explorer**. Muestra la versión de API que se usa, en función de la configuración y del sistema operativo. Si hay un problema, es posible que se le pida al usuario que ejecute **Windows Update** e instale las actualizaciones necesarias.
- **Configuración del modo Internet Explorer**. Muestra si está habilitado el modo de Internet Explorer y cómo se configura.
- **Línea de comandos**. Muestra la cadena de línea de comandos y los modificadores que se usan para iniciar Microsoft Edge.
- **Configuración de directiva de grupo**. Muestra si el modo IE se configura con directivas de grupo y las directivas que se aplican.

### <a name="error-message-to-open-this-page-in-internet-explorer-mode-reinstall-microsoft-edge-with-administrator-privileges"></a>Mensaje de error: "Para abrir esta página en modo Internet Explorer, vuelve a instalar Microsoft Edge con privilegios de administrador".

Es posible que vea este error si no tiene todas las actualizaciones de Windows necesarias. Consulte los requisitos previos listados en [acerca del modo de IE](./edge-ie-mode.md) para las versiones requeridas de Windows y Microsoft Edge.

Si ya ha instalado todas las actualizaciones de Windows necesarias, es posible que vea este error si:

- Está usando el canal Canary, que se instala en el nivel de usuario de manera predeterminada.
- Está utilizando el canal Estable, Beta o Dev, pero cuando se le solicitó la elevación al instalar, la elevación se canceló. Si cancela la solicitud de elevación, la instalación continuará en el nivel de usuario.
- Se ha deshabilitado Internet Explorer 11 en Características de Windows.

Soluciones posibles:

- Ejecuta el instalador de cualquier canal en el nivel del sistema: `installer.exe --system-level`.
- Habilita Internet Explorer 11 en Características de Windows.

Para comprobar que Microsoft Edge está instalado en el nivel del sistema, escriba "edge://version" en la barra de direcciones de Microsoft Edge. La ruta de acceso del archivo ejecutable mostrará una ruta de acceso que comenzará por *C:\Archivos de programa*, lo que indica una instalación del sistema. Si la ruta del archivo ejecutable comienza por "C:\Usuarios", desinstale y vuelva a instalar Microsoft Edge con privilegios de administrador.

### <a name="error-message-to-open-this-page-in-ie-mode-try-restarting-microsoft-edge"></a>Mensaje de error: "Para abrir esta página en modo IE, prueba a reiniciar Microsoft Edge".

Es posible que vea este error si se ha producido un error inesperado en Internet Explorer. Por lo general, el reinicio de Microsoft Edge soluciona este error.

### <a name="error-message-turn-off-remote-debugging-to-open-this-site-in-ie-mode-otherwise-it-might-not-work-as-expected"></a>Mensaje de error: "Desactive la depuración remota para abrir este sitio en modo IE, o si no, probablemente no funcionará según lo esperado".

Es probable que vea este error si realiza la depuración de forma remota y navega a una página web configurada para ejecutarse en modo IE. Puede continuar, pero la página se mostrará con Microsoft Edge.

### <a name="error-message-error-could-not-retrieve-emie-site-list"></a>Mensaje de error: "Error: no se pudo recuperar la lista de sitios de EMIE".

Es posible que veas este error en la página *edge://compat/enterprise* indicando que no se pudo descargar la lista de sitios. A partir de la versión 87 de Microsoft Edge, cuando las cookies se bloquean para solicitudes de terceros usando la directiva [BlockThirdPartyCookies](./microsoft-edge-policies.md#blockthirdpartycookies) la autenticación HTTP también está prohibida. Puedes permitir cookies para el dominio específico que hospeda la Lista de sitios del modo de empresa usando la directiva [CookiesAllowedForURls](./microsoft-edge-policies.md#cookiesallowedforurls) para asegurarte de que las descargas de listas de sitios son correctas.

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

### <a name="will-ie-mode-replace-internet-explorer-11"></a>¿Reemplazará el modo IE a Internet Explorer 11?

Nos comprometemos a conservar Internet Explorer como un explorador con soporte, confiable y seguro. Internet Explorer sigue siendo un componente de Windows y sigue el ciclo de vida de soporte técnico del SO en el que está instalado. Para obtener más detalles, consulta [Preguntas frecuentes del ciclo de vida: Internet Explorer](https://support.microsoft.com/help/17454/). Si bien Microsoft continúa ofreciendo soporte y actualizando Internet Explorer, las últimas funciones y actualizaciones de la plataforma solo estarán disponibles en Microsoft Edge.

### <a name="can-i-use-open-with-explorer-or-view-in-file-explorer-in-sharepoint-with-ie-mode"></a>¿Puedo usar "Abrir con el Explorador" o "Ver en el Explorador de archivos" en SharePoint con el modo IE?

Sí, si esto funciona en Internet Explorer 11 independiente, funcionará en el modo IE. Sin embargo, en lugar de usar la opción Abrir con el explorador, el enfoque recomendado para administrar archivos y carpetas por fuera de SharePoint es [sincronizar los archivos de SharePoint](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88) o [mover o copiar archivos en SharePoint](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc).

### <a name="does-ie-mode-on-microsoft-edge-support-the-nomerge-option-that-was-supported-in-internet-explorer-11"></a>¿Es compatible el modo IE en Microsoft Edge con la opción *no combinar* que era compatible con Internet Explorer 11?

No hay ninguna línea de comandos explícita en Microsoft Edge que refleje la opción *no combinar*, pero existen un par de alternativas que recomendamos para ofrecer esta funcionalidad.

1. Usar perfiles en Microsoft Edge: cada perfil se asigna a una sesión de IE diferente para las páginas en modo IE, por lo que se comporta de la misma forma que la opción *no combinar*.
2. Usa la línea de comandos `--user-data-dir=<path>`, pero con una ruta de acceso diferente para cada sesión. Si es necesario, puedes crear una utilidad que el usuario puede ejecutar y que inicia Microsoft Edge y cambia la ruta de acceso de la sesión.

Si las opciones anteriores no son adecuadas para el escenario en cuestión, puedes enviarnos un comentario en uno de nuestros canales: Soporte técnico de Microsoft o el [foro TechCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a>¿Puedo guardar vínculos como páginas web en el modo Internet Explorer?

Sí, puede habilitar la opción de Guardar destino como en el menú contextual del modo Internet Explorer en Microsoft Edge. Para hacerlo, configure la directiva de grupo *"Permitir la opción Guardar destino como en el modo Internet Explorer"* que se encuentra en *Configuración del equipo > Plantillas administrativas > Componentes de Windows > Internet Explorer*.
El mecanismo de guardado funciona de la misma manera que en Internet Explorer y, si el destino está guardado como archivo HTML, al volver a abrir el archivo se representará la página en Microsoft Edge.
 
Tenga en cuenta que esta funcionalidad requiere las siguientes actualizaciones mínimas del sistema operativo:
- Windows 10, versión 2004, Windows Server versión 2004, Windows 10, versión 20H2: [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10, versión 1903, Windows 10, versión 1909, Windows Server versión 1903: [KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)
- Windows 10, versión 1809, Windows Server versión 1809, Windows Server 2019: [KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)
- Windows 10, versión 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, versión 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, versión 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)


## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Acerca del modo IE](./edge-ie-mode.md)
- [Información adicional del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)