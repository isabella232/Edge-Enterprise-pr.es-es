---
title: Configurar Microsoft Edge para macOS con un .plist
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar las opciones de directiva de Microsoft Edge en macOS con un .plist
ms.openlocfilehash: 84469a4f84deeee0e47b6d8899426fa36cf345aa
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981042"
---
# Configurar las opciones de directiva de Microsoft Edge en macOS con un .plist

En este artículo se describe cómo configurar Microsoft Edge en macOS con un archivo de lista de propiedades (.plist). Obtendrá información sobre cómo crear este archivo e implementarlo en Microsoft Intune.

Para obtener más información, consulta [Acerca de los archivos de lista de propiedades de información](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (sitio web de Apple) y [Configuración de carga personalizada](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## Configurar las directivas de Microsoft Edge en macOS

El primer paso es crear el archivo plist. Puedes crear el archivo plist con cualquier editor de texto o puedes usar [Terminal para crear el perfil de configuración](#create-a-configuration-profile-using-terminal). Sin embargo, es más fácil crear y editar un archivo plist con una herramienta que te dé formato al código XML. *Xcode* es un entorno de desarrollo integrado gratuito que puedes obtener desde una de las siguientes ubicaciones:

- [Sitio web de desarrolladores de Apple](https://developer.apple.com/xcode/)
- [Mac App Store](https://apps.apple.com/app/xcode/id497799835?mt=12)

Para obtener una lista de las directivas admitidas y sus nombres clave preferidos, consulta [Referencia de directivas del explorador de Microsoft Edge](microsoft-edge-policies.md). En el archivo de plantillas de directiva, que se puede descargar desde la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise), hay un ejemplo de archivo plist (*itadminexample.plist*) en la carpeta de **ejemplos**. El archivo de ejemplo contiene todos los tipos de datos admitidos que se pueden personalizar para definir la configuración de directiva. 

El siguiente paso después de crear el contenido del archivo plist, es asignarle un nombre usando el dominio de preferencia de Microsoft Edge, *com.microsoft.Edge*. El nombre distingue entre mayúsculas y minúsculas y no debe incluir el canal de destino porque se aplica a todos los canales de Microsoft Edge. El nombre de archivo plist debe ser **_com.microsoft.Edge.plist_**. 

> [!IMPORTANT]
> A partir de la compilación 78.0.249.2, todos los canales de Microsoft Edge en macOS se leen desde el dominio de preferencias **com.microsoft.Edge**. Todas las versiones anteriores se leían desde un dominio específico de canal, como **com.microsoft.Edge.Dev** para el canal Dev.

El último paso es implementar el archivo plist en los dispositivos Mac de los usuarios con el proveedor de MDM que prefieras, como Microsoft Intune. Para obtener instrucciones, consulta [Implementar el archivo plist](#deploy-your-plist).

### Crear un perfil de configuración con Terminal

1. En Terminal, usa el siguiente comando para crear un archivo plist para Microsoft Edge en el escritorio, con la configuración que prefieras:

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. Convierte el archivo plist de formato binario a texto sin formato:

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```
Después de convertir el archivo, comprueba que los datos de la directiva sean correctos y contengan la configuración que quieras para tu perfil de configuración.

> [!NOTE]
> Solo los pares de clave y valor deben encontrarse en el contenido del archivo plist o xml. Antes de cargar el archivo en Intune, elimine todos los valores de \<plist> y \<dict> los encabezados XML del archivo. El archivo solo debe contener pares de clave y valor.

## Implementar el archivo plist

Para Microsoft Intune, crea un nuevo perfil de configuración de dispositivo destinado a la plataforma macOS y selecciona el tipo de perfil del *Archivo de preferencias*. Elige como destino **com.microsoft.Edge** como nombre de dominio preferente y carga el plist. Para obtener más información, consulta [Agregar un archivo de lista de propiedades a dispositivos macOS con Microsoft Intune](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos).

Para Jamf, carga el archivo .plist como una carga de *Configuración personalizada*.

## Preguntas más frecuentes

### ¿Se puede configurar Microsoft Edge para usar las preferencias maestras?

Si, puedes configurar Microsoft Edge para usar un archivo de preferencias maestras.

Un archivo de preferencias maestras permite configurar las opciones predeterminadas para un perfil de usuario de explorador cuando se implementa Microsoft Edge. También puedes usar un archivo de preferencias maestras para aplicar la configuración en equipos que no están administrados por un sistema de administración de dispositivos. Esta configuración se aplica al perfil del usuario la primera vez que el usuario ejecuta el explorador. Cuando el usuario ejecute el explorador, no se aplicarán los cambios realizados en el archivo de preferencias maestras. Un usuario puede cambiar la configuración de las preferencias maestras del explorador. Si quieres que una configuración sea obligatoria o cambiar una configuración después de la primera ejecución del explorador, debes usar una directiva.

Un archivo de preferencias principales permite personalizar muchas opciones de configuración y preferencias diferentes del explorador, incluidas las que se comparten con otros exploradores basados en Chromium y las específicas de Microsoft Edge.  Las preferencias relacionadas con la directiva pueden configurarse mediante el archivo de preferencias maestras. En los casos en los que se establece una directiva y hay un conjunto de preferencias maestro correspondiente, la configuración de directiva tiene prioridad.

> [!IMPORTANT]
> Es posible que todas las preferencias disponibles no sean coherentes con la terminología Microsoft Edge y las convenciones de nomenclatura.  No hay ninguna garantía de que estas preferencias sigan funcionando según lo previsto en futuras versiones. Las preferencias se pueden cambiar u omitir en versiones posteriores.

Un archivo de preferencias maestras es un archivo de texto que se ha formateado usando marcado JSON. Este archivo debe agregarse al mismo directorio que el ejecutable msedge.exe. Para las implementaciones de sistema para toda la organización en el Mac, esto suele ser: "*~/Library/Application Support/Microsoft/Microsoft Edge general Preferences*" o "*/Library/Application Support/Microsoft/Microsoft Edge general Preferences*".

## Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar para macOS con Jamf](configure-microsoft-edge-on-mac-jamf.md)
- [Configurar para Windows](configure-microsoft-edge.md)
- [Configurar para Windows con Intune](configure-edge-with-intune.md)
