---
title: Configurar Microsoft Edge para macOS con un .plist
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configurar las opciones de directiva de Microsoft Edge en macOS con un .plist
ms.openlocfilehash: d2e604e13f0fb7f81b2fb492073eba0751407771
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979772"
---
# <a name="configure-microsoft-edge-policy-settings-for-macos-using-a-plist"></a>Configurar las opciones de directiva de Microsoft Edge en macOS con un .plist

En este artículo se describe cómo configurar Microsoft Edge en macOS con un archivo de lista de propiedades (.plist). Obtendrá información sobre cómo crear este archivo e implementarlo en Microsoft Intune.

Para obtener más información, consulta [Acerca de los archivos de lista de propiedades de información](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (sitio web de Apple) y [Configuración de carga personalizada](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="configure-microsoft-edge-policies-on-macos"></a>Configurar las directivas de Microsoft Edge en macOS

El primer paso es crear el archivo plist. Puedes crear el archivo plist con cualquier editor de texto o puedes usar [Terminal para crear el perfil de configuración](#create-a-configuration-profile-using-terminal). Sin embargo, es más fácil crear y editar un archivo plist con una herramienta que te dé formato al código XML. *Xcode* es un entorno de desarrollo integrado gratuito que puedes obtener desde una de las siguientes ubicaciones:

- [Sitio web de desarrolladores de Apple](https://developer.apple.com/xcode/)
- [Mac App Store](https://apps.apple.com/app/xcode/id497799835?mt=12)

Para obtener una lista de las directivas admitidas y sus nombres clave preferidos, consulta [Referencia de directivas del explorador de Microsoft Edge](microsoft-edge-policies.md). En el archivo de plantillas de directiva, que se puede descargar desde la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise), hay un ejemplo de archivo plist (*itadminexample.plist*) en la carpeta de **ejemplos**. El archivo de ejemplo contiene todos los tipos de datos admitidos que se pueden personalizar para definir la configuración de directiva. 

El siguiente paso después de crear el contenido del archivo plist, es asignarle un nombre usando el dominio de preferencia de Microsoft Edge, *com.microsoft.Edge*. El nombre distingue entre mayúsculas y minúsculas y no debe incluir el canal de destino porque se aplica a todos los canales de Microsoft Edge. El nombre de archivo plist debe ser **_com.microsoft.Edge.plist_**.

> [!IMPORTANT]
> A partir de la compilación 78.0.249.2, todos los canales de Microsoft Edge en macOS se leen desde el dominio de preferencias **com.microsoft.Edge**. Todas las versiones anteriores se leían desde un dominio específico de canal, como **com.microsoft.Edge.Dev** para el canal Dev.

El último paso es implementar el archivo plist en los dispositivos Mac de los usuarios con el proveedor de MDM que prefieras, como Microsoft Intune. Para obtener instrucciones, consulta [Implementar el archivo plist](#deploy-your-plist).

### <a name="create-a-configuration-profile-using-terminal"></a>Crear un perfil de configuración con Terminal

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

## <a name="deploy-your-plist"></a>Implementar el archivo plist

Para Microsoft Intune, crea un nuevo perfil de configuración de dispositivo destinado a la plataforma macOS y selecciona el tipo de perfil del *Archivo de preferencias*. Elige como destino **com.microsoft.Edge** como nombre de dominio preferente y carga el plist. Para obtener más información, consulta [Agregar un archivo de lista de propiedades a dispositivos macOS con Microsoft Intune](/intune/configuration/preference-file-settings-macos).

Para Jamf, carga el archivo .plist como una carga de *Configuración personalizada*.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar para macOS con Jamf](configure-microsoft-edge-on-mac-jamf.md)
- [Configurar para Windows](configure-microsoft-edge.md)
- [Configurar para Windows con Intune](configure-edge-with-intune.md)