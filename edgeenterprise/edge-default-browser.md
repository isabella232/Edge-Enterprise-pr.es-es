---
title: Establecer Microsoft Edge como explorador predeterminado en Windows y macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 1/15/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Aprende a establecer Microsoft Edge como explorador predeterminado
ms.openlocfilehash: c8cc45e0fe42dcbbd828dd81ae568f141cda2985
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981092"
---
# Establecer Microsoft Edge como explorador predeterminado

En este artículo se explica como puedes establecer Microsoft Edge como explorador predeterminado en Windows y macOS.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior, en Windows 8 y Windows 10. Para Windows 7 y macOS, consulta la directiva [Establecer Microsoft Edge como explorador predeterminado](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled).

## Introducción

Puedes usar la directiva de grupo **Establecer un archivo de configuración de asociaciones predeterminadas**, o la configuración de Administración de dispositivos móviles [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) para establecer Microsoft Edge como explorador predeterminado para la organización.

Para establecer el canal estable de Microsoft Edge como explorador predeterminado para los archivos html, los vínculos http/https y los archivos PDF, usa el siguiente ejemplo de archivo de asociación de aplicaciones:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations> 
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> Para establecer Microsoft Edge Beta como explorador predeterminado, establece **ApplicationName** en "Microsoft Edge Beta" y **ProgId** en "MSEdgeBHTML". Para establecer Microsoft Edge Dev como explorador predeterminado, establece **ApplicationName** en "Microsoft Edge Dev" y **ProgId** en "MSEdgeDHTML".


> [!NOTE]
> Las asociaciones de archivo predeterminadas no se aplican si Microsoft Edge no está instalado en el dispositivo de destino. En este escenario, se pide al usuario que seleccione su aplicación predeterminada cuando abre un vínculo o un archivo htm/html.

## Establecer Microsoft Edge como explorador predeterminado en dispositivos unidos al dominio

Puedes establecer Microsoft Edge como explorador predeterminado en dispositivos unidos al dominio configurando la directiva de grupo **Establecer un archivo de configuración de asociaciones predeterminado**. Activar esta directiva de grupo requiere crear y almacenar un archivo de configuración de asociaciones predeterminado. Este archivo se almacena localmente o en un recurso compartido de red. Para obtener más información sobre cómo crear este archivo, consulta [Exportar o importar asociaciones de aplicaciones predeterminadas](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).

### Para configurar la directiva de grupo para un archivo de configuración de asociaciones de protocolos y tipos de archivo predeterminados:

1. Abre el editor de directiva de grupo y ve a **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.
2. Selecciona **Definir un archivo de configuración de asociaciones predeterminadas**.
3. Haz clic en **Configuración de directiva** y, después, en **Habilitada**.
4. En **Opciones**, escribe la ubicación en el archivo de configuración de asociaciones predeterminadas.
5. Haz clic en **Aceptar** para guardar la configuración de directiva.

En el ejemplo de la siguiente captura de pantalla se muestra un archivo de asociaciones denominado *appassoc.xml* en un recurso compartido de red al que se puede acceder desde el dispositivo de destino.

   ![Habilitar la asociación de archivos en la directiva de grupo](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > Si esta opción está habilitada y el dispositivo del usuario está unido a un dominio, el archivo de configuración de asociaciones se procesará la próxima vez que el usuario inicie sesión.

## Establecer Microsoft Edge como explorador predeterminado en dispositivos unidos a Azure Active Directory

Para establecer Microsoft Edge como explorador predeterminado en dispositivos unidos a Azure Active Directory, sigue los pasos de configuración de Administración de dispositivos móviles [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) usando el siguiente archivo de asociación de aplicaciones como ejemplo.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> Para establecer Microsoft Edge Beta como explorador predeterminado, establece **ApplicationName** en "Microsoft Edge Beta" y **ProgId** en "MSEdgeBHTML". Para establecer Microsoft Edge Dev como explorador predeterminado, establece **ApplicationName** en "Microsoft Edge Dev" y **ProgId** en "MSEdgeDHTML".

## Establecer Microsoft Edge como explorador predeterminado en macOS

Intentar establecer mediante programación el explorador predeterminado en macOS hace que aparezca un aviso al usuario final. Este aviso es una característica de seguridad de macOS que puede quitarse de manera automatizada únicamente mediante AppleScript.

Debido a esta limitación, existen dos métodos principales para establecer Microsoft Edge como explorador predeterminado en macOS. La primera opción es reinstalar en el dispositivo una imagen de macOS donde Microsoft Edge ya se haya establecido como explorador predeterminado. La otra opción es usar la directiva [Establecer Microsoft Edge como explorador predeterminado](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled) , que pide al usuario establecer Microsoft Edge como explorador predeterminado.

Al usar cualquiera de estos métodos, el usuario sigue pudiendo cambiar el explorador predeterminado. Esto se debe a motivos de seguridad, la preferencia de explorador predeterminado no se puede bloquear mediante programación. Por este motivo, se recomienda implementar la directiva **Establecer Microsoft Edge como explorador predeterminado** incluso si crea una imagen como Microsoft Edge como explorador predeterminado. Si la directiva se establece, y un usuario cambia el explorador predeterminado de Microsoft Edge, la próxima vez que abra Microsoft Edge se le pedirá que lo establezca como predeterminado.

## Consulta también

- [Planear tu implementación de Microsoft Edge](https://docs.microsoft.com/DeployEdge/deploy-edge-plan-deployment)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Establecer Microsoft Edge como explorador predeterminado (Windows 7 y macOS)](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled)
- [Windows 10: ¿Cómo configurar asociaciones de archivos para profesionales de TI?](https://docs.microsoft.com/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [Exportar o importar asociaciones de aplicaciones predeterminadas](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [Introducción a DISM](https://docs.microsoft.com/windows-hardware/manufacture/desktop/what-is-dism)
  - [DISM: Administración y mantenimiento de imágenes de implementación](https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)
