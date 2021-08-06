---
title: Establecer Microsoft Edge como explorador predeterminado en Windows y macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Aprende a establecer Microsoft Edge como explorador predeterminado
ms.openlocfilehash: 31db8d2c5ebf256c5cc041a2716ddd954a3219106b5eb1b083cc71c062abec76
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724752"
---
# <a name="set-microsoft-edge-as-the-default-browser"></a>Establecer Microsoft Edge como explorador predeterminado

En este artículo se explica como puedes establecer Microsoft Edge como explorador predeterminado en Windows y macOS.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior, en Windows 8 y Windows 10. Para Windows 7 y macOS, consulta la directiva [Establecer Microsoft Edge como explorador predeterminado](./microsoft-edge-policies.md#defaultbrowsersettingenabled).

## <a name="introduction"></a>Introducción

Puedes usar la directiva de grupo **Establecer un archivo de configuración de asociaciones predeterminadas**, o la configuración de Administración de dispositivos móviles [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) para establecer Microsoft Edge como explorador predeterminado para la organización.

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

## <a name="set-microsoft-edge-as-the-default-browser-on-domain-joined-devices"></a>Establecer Microsoft Edge como explorador predeterminado en dispositivos unidos al dominio

Puedes establecer Microsoft Edge como explorador predeterminado en dispositivos unidos al dominio configurando la directiva de grupo **Establecer un archivo de configuración de asociaciones predeterminado**. Activar esta directiva de grupo requiere crear y almacenar un archivo de configuración de asociaciones predeterminado. Este archivo se almacena localmente o en un recurso compartido de red. Para obtener más información sobre cómo crear este archivo, consulta [Exportar o importar asociaciones de aplicaciones predeterminadas](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).

### <a name="to-configure-the-group-policy-for-a-default-file-type-and-protocol-associations-configuration-file"></a>Para configurar la directiva de grupo para un archivo de configuración de asociaciones de protocolos y tipos de archivo predeterminados:

1. Abre el editor de directiva de grupo y ve a **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.
2. Selecciona **Definir un archivo de configuración de asociaciones predeterminadas**.
3. Haz clic en **Configuración de directiva** y, después, en **Habilitada**.
4. En **Opciones**, escribe la ubicación en el archivo de configuración de asociaciones predeterminadas.
5. Haz clic en **Aceptar** para guardar la configuración de directiva.

En el ejemplo de la siguiente captura de pantalla se muestra un archivo de asociaciones denominado *appassoc.xml* en un recurso compartido de red al que se puede acceder desde el dispositivo de destino.

   ![Habilitar la asociación de archivos en la directiva de grupo](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > Si esta opción está habilitada y el dispositivo del usuario está unido a un dominio, el archivo de configuración de asociaciones se procesará la próxima vez que el usuario inicie sesión.

## <a name="set-microsoft-edge-as-the-default-browser-on-azure-active-directory-joined-devices"></a>Establecer Microsoft Edge como explorador predeterminado en dispositivos unidos a Azure Active Directory

Para establecer Microsoft Edge como explorador predeterminado en dispositivos unidos a Azure Active Directory, sigue los pasos de configuración de Administración de dispositivos móviles [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) usando el siguiente archivo de asociación de aplicaciones como ejemplo.

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

## <a name="set-microsoft-edge-as-the-default-browser-on-macos"></a>Establecer Microsoft Edge como explorador predeterminado en macOS

Intentar establecer mediante programación el explorador predeterminado en macOS hace que aparezca un aviso al usuario final. Este aviso es una característica de seguridad de macOS que puede quitarse de manera automatizada únicamente mediante AppleScript.

Debido a esta limitación, existen dos métodos principales para establecer Microsoft Edge como explorador predeterminado en macOS. La primera opción es reinstalar en el dispositivo una imagen de macOS donde Microsoft Edge ya se haya establecido como explorador predeterminado. La otra opción es usar la directiva [Establecer Microsoft Edge como explorador predeterminado](./microsoft-edge-policies.md#defaultbrowsersettingenabled) , que pide al usuario establecer Microsoft Edge como explorador predeterminado.

Al usar cualquiera de estos métodos, el usuario sigue pudiendo cambiar el explorador predeterminado. Esto se debe a motivos de seguridad, la preferencia de explorador predeterminado no se puede bloquear mediante programación. Por este motivo, se recomienda implementar la directiva **Establecer Microsoft Edge como explorador predeterminado** incluso si crea una imagen como Microsoft Edge como explorador predeterminado. Si la directiva se establece, y un usuario cambia el explorador predeterminado de Microsoft Edge, la próxima vez que abra Microsoft Edge se le pedirá que lo establezca como predeterminado.

## <a name="see-also"></a>Consulta también

- [Planear tu implementación de Microsoft Edge](./deploy-edge-plan-deployment.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Establecer Microsoft Edge como explorador predeterminado (Windows 7 y macOS)](./microsoft-edge-policies.md#defaultbrowsersettingenabled)
- [Windows 10: ¿Cómo configurar asociaciones de archivos para profesionales de TI?](/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [Exportar o importar asociaciones de aplicaciones predeterminadas](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [Introducción a DISM](/windows-hardware/manufacture/desktop/what-is-dism)
  - [DISM: Administración y mantenimiento de imágenes de implementación](/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)