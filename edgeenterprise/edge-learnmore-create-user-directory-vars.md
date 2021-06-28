---
title: Crear variables de directorio de datos de usuario de Microsoft Edge
ms.author: brianalt
author: AndreaLBarr
manager: srugh
ms.date: 04/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Aprende a crear variables de directorio de datos de usuario de Microsoft Edge
ms.openlocfilehash: 5ec78f16c7e5cd43f01845f35b8473494cd0c4bf
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618262"
---
# <a name="create-microsoft-edge-user-data-directory-variables"></a>Crear variables de directorio de datos de usuario de Microsoft Edge

En este artículo se explica cómo puedes usar variables de directorio de datos en lugar de usar rutas codificadas de forma rígida al modificar Microsoft Edge.

>[!NOTE]
>Este artículo se aplica a Microsoft Edge, versión 77 o posterior.
## <a name="path-variables"></a>Variables de ruta

Directivas para modificar las rutas del directorio de datos (por ejemplo, configurar las variables de soporte [UserDataDir](microsoft-edge-policies.md#userdatadir) o [DownloadDirectory](microsoft-edge-policies.md#downloaddirectory). Al configurar estas directivas puedes usar variables en lugar de rutas de acceso codificadas. Por ejemplo, para almacenar tus datos de perfil en datos de aplicación local de usuario en Windows en lugar de en la ubicación predeterminada. Establece la directiva [UserDataDir](microsoft-edge-policies.md#userdatadir) en **${local_app_data}\Edge\Perfil**. En la mayoría de las instalaciones de Windows 10, esta ruta da por resultado *C:\Usuarios\\&lt;Usuario actual&gt;\AppData\Local\Microsoft\Edge\Perfil*.

>[!NOTE]
>Para ver la  **ruta de perfil** actual, abra la página **Acerca de la versión** (escriba "edge://version"). La **ruta de perfil** sigue este formato: *C:\Usuarios\\&lt;Usuario actual&gt;\AppData\Local\Microsoft\Edge\Datos de usuario\Predeterminado*.

### <a name="guidance-for-using-path-variables"></a>Instrucciones para usar variables de ruta

Revisa las siguientes instrucciones antes de usar variables para las rutas.

- Todas las directivas que implican rutas en las que Microsoft Edge almacena datos diferentes dependen de la plataforma. Algunas de estas directivas están disponibles únicamente en plataformas específicas, pero otras se pueden usar en todas las plataformas.
- Para evitar errores causados por las aplicaciones que se inician en diferentes ubicaciones en diferentes ocasiones, asegúrate de que las rutas sean absolutas.
- Cada variable puede aparecer una sola vez en una ruta. Para la mayoría de ellas, esta es la única forma significativa de usar variables, ya que se resuelven en rutas absolutas.
- Casi todas las directivas crearán la ruta de acceso si no existe (si es posible en las circunstancias existentes).
- El uso de ubicaciones de red para algunas directivas puede generar resultados inesperados debido a las diferencias en el modo en que las diferentes versiones/canales de Microsoft Edge tratan la estructura de carpetas.

### <a name="supported-path-variables"></a>Variables de ruta soportadas

Microsoft Edge admite las siguientes variables de ruta.

#### <a name="all-platforms"></a>Todas las plataformas

| Variable | Descripción |
| --- | --- |
| **${user_name}** | El usuario que está usando Microsoft Edge. Microsoft Edge respeta los SUID (Establecer el Id. de usuario del propietario en ejecución) Ejemplo: *audreysmall* |
| **${machine_name}** | Nombre del equipo, incluido posiblemente el nombre del dominio. Ejemplo: *audreysmall* o *audrey.ex.contoso.com* |

#### <a name="windows-only"></a>Solo Windows

| Variable | Descripción |
| --- | --- |
| **${documents}** | Carpeta de documentos para el usuario actual. Ejemplo: *C:\Usuarios\Administrador\Documentos* |
|**${local_app_data}** | Carpeta de datos de aplicaciones para el usuario actual. Ejemplo: *C:\Usuarios\Administrador\AppData\Local* |
|**${roaming_app_data}** | Carpeta de datos de aplicaciones movidos para el usuario actual. Ejemplo: *C:\Usuarios\Administrador\AppData\Roaming* |
| **${profile}** | Carpeta particular para el usuario actual. Ejemplo: *C:\Usuarios\Administrador* |
| **${global_app_data}** | Carpeta de datos de la aplicación en todo el sistema. Ejemplo: *C:\AppData* |
| **${program_files}** | Carpeta de archivos de programa para el proceso actual. Esta carpeta depende de si se trata de un proceso de 32 bits o de 64 bits. Solución de ejemplo: *C:\Archivos de programa (x86)* |
| **${windows}** | Carpeta de Windows. Ejemplo: *C:\Windows* |
| **${client_name)** | El nombre del PC cliente conectado a una sesión de RDP o Citrix. Esta variable está vacía si se usa desde una sesión local. Si se usa en una ruta, aplica un prefijo que garantice que no esté vacía. Ejemplo: *C:\edge_profiles\session_${client_name}* da por resultado *C:\edge_profiles\session_&lt;ForlocalSessions&gt;* y *C:\edge_profiles\session_&lt;SomePCname&gt;* para sesiones remotas. |
| **${session_name}** | Nombre descriptivo de la sesión activa. Usa este nombre para distinguir entre varias sesiones remotas conectadas simultáneamente que usan un perfil de usuario único. Ejemplo: *WinSta0 para sesiones de escritorio local* |

#### <a name="macos-only"></a>Solo MacOS

| Variable | Descripción |
| --- | --- |
| **${users}** | Carpeta donde se almacenan los perfiles de usuario. Ejemplo: */Usuarios* |
| **${documents}** | Carpeta de documentos para el usuario actual. Ejemplo: */Usuarios/audreysmall/Documentos* |

## <a name="content-license"></a>Licencia de contenido

>[!NOTE]
>Algunas partes de esta página son modificaciones que se basan en trabajo creado y compartido por Chromium.org y que se usan de acuerdo con los términos descritos en la [Licencia internacional de Creative Commons Atribution 4.0](http://creativecommons.org/licenses/by/4.0/). La página original se puede encontrar [aquí](https://www.chromium.org/administrators/policy-list-3/user-data-directory-variables).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br/>Este trabajo dispone de licencia conforme a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licencia internacional de Creative Commons Attribution 4.0</a>.
## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)