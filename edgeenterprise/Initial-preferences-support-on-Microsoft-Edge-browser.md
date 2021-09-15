---
title: Compatibilidad con preferencias iniciales en Microsoft Edge explorador
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 07/27/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Compatibilidad con preferencias iniciales en Microsoft Edge explorador.
ms.openlocfilehash: 7a497fd2f3305b0c027a396936ef86bacbcb5b20
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979821"
---
# <a name="configure-microsoft-edge-using-initial-preferences-settings-for-the-first-run"></a>Configurar Microsoft Edge con las preferencias iniciales para la primera ejecución

Usa la siguiente información para configurar la configuración Microsoft Edge preferencias iniciales en los Windows dispositivos.

> [!Note]
> Este artículo se aplica a Microsoft Edge versión 93 o posterior.

## <a name="configure-policy-settings-on-windows"></a>Configurar las opciones de directiva en Windows

A Microsoft Edge versión 93, Microsoft admite un número limitado de preferencias iniciales, anteriormente denominadas "Preferencias maestras", para ayudar a los administradores a configurar exploradores para la primera ejecución; vea la lista de la configuración admitida a continuación.  

Cuando se implementa, las preferencias iniciales actúan como la configuración predeterminada del explorador en dispositivos administrados; estas son las opciones preferidas por los administradores para que se utilicen de forma predeterminada, pero que los usuarios pueden cambiar o no están disponibles para algunos dispositivos, ya que no están unidas a un dominio de Active Directory®.

Algunos ejemplos de la configuración de preferencias intiales incluyen la configuración inicial de una página principal predeterminada o pestañas con direcciones URL específicas.

Las preferencias se copian initial_preferences archivo solo una vez y los cambios realizados en este archivo después de la configuración no se respetarán. Si una directiva de configuración administra una [Microsoft Edge y](/deployedge/microsoft-edge-policies) se configura en el archivo initial_preferences, la directiva siempre tiene prioridad.

A continuación se muestra la lista de opciones de preferencias que admite actualmente Microsoft Edge:

| Categoría Preferencias | Configuración |
| - | - |
| Bookmark_bar | show_apps_shortcut<br>show_managed_bookmarks<br>show_on_all_tabs |
| Marcadores | editing_enabled |
| Explorador /clear_data | browsing_history<br>browsing_history_basic"<br>caché<br>cache_basic<br>cookies<br>download_history<br>form_data<br>contraseñas |
| Historial | browsing_history<br>caché<br>cookies<br>download_history<br>form_data<br>hosted_apps_data<br>contraseñas<br>site_settings |
| Explorador | first_run_tabs<br>dark_theme<br>show_toolbar_bookmarks_button<br>show_toolbar_collections_butto<br>show_toolbar_downloads_button<br>show_home_button<br>show_prompt_before_closing_tabs<br>show_toolbar_history_button |
| default_search_provider | [default_search_provider] habilitado |
| Pantalla completa | Se permite |
| página principal | Homepage_url |
| homepage_is_newtabpage | homepage_is_newtabpage |
| Sesión | restore_on_startup<br>startup_urls |
| Extensions | Extensiones : configuración |

## <a name="1-download-an-example-initial_preferences-file"></a>1: Descargar un archivo de initial_preferences ejemplo

Para empezar, descargue el archivo "Directiva" desde la [Microsoft Edge Enterprise de aterrizaje](https://www.microsoft.com/edge/business/download). Extraiga los archivos y abra el `initial_preferences` archivo dentro de la `examples` carpeta.

## <a name="2-customize-and-validate-the-initial_preferences-file"></a>2: Personalizar y validar el initial_preferences archivo

Personalice la configuración de preferencias en el archivo *initial_preferences* descargado y valide los cambios para asegurarse de que no haya errores en el código JSON. Si encuentra errores, compruebe la sintaxis y la estructura del *archivo initial_preferences,* realice correcciones y vuelva a validarlo. Pocas herramientas de ejemplo para validar JSON, Herramientas [JSON](https://jsonformatter.org/) en línea o [edición JSON en Visual Studio Code](https://code.visualstudio.com/docs/languages/json).

## <a name="3-deploy-preferences-to-users-computer"></a>3: Implementar preferencias en el equipo de los usuarios

Implemente *el archivo initial_preferences* en los dispositivos de los usuarios al mismo tiempo que se implementa Microsoft Edge Browser y coloque el archivo en la siguiente ubicación en el dispositivo.

### <a name="windows-amd64-and-arm64"></a>Windows (AMD64 y ARM64)

| Canal | Ubicación |
| - | - |
| Estable | `"C:\Program Files (x86)\Microsoft\Edge\Application"` |
| Beta | `"C:\Program Files (x86)\Microsoft\Edge Beta\Application"` |
|Canary | `"%LOCALAPPDATA%\Microsoft\Edge SxS\Application"` |
| Dev | `"C:\Program Files (x86)\Microsoft\Edge Dev\Application"` |

**Nota:** *el initial_preferences* debe implementarse en la misma carpeta que el archivo msedge.exe en los equipos Windows usuarios.  

### <a name="macos"></a>macOS

| Canal | Ubicación |
| - | - |
| Estable | `"~/Library/Application Support/Microsoft Edge/Microsoft Edge Initial Preferences"` |
| Beta | `“~/Library/Application Support/Microsoft Edge Beta/Microsoft Edge Initial Preferences"` |
| Canary | `“~/Library/Application Support/Microsoft Edge Canary/Microsoft Edge Initial Preferences"` |
| Dev | `"~/Library/Application Support/Microsoft Edge Dev/Microsoft Edge Initial Preferences"` |

## <a name="important-notes-msi--pkg-deployment-and-initial_preferences-interaction"></a>Notas importantes: Implementación de MSI /Pkg *e initial_preferences* interacción

Las preferencias iniciales solo tendrán efecto cuando el archivo initial_preferences se implemente antes de que los usuarios finales ejecuten por primera vez el explorador.  

## <a name="see-also"></a>Vea también

- [El *initial_prefrences* de plantilla de ejemplo](https://www.microsoft.com/edge/business/download)
