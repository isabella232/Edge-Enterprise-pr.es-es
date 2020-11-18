---
title: Asociar extensiones de archivo con el modo Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Asociar extensiones de archivo con el modo Internet Explorer
ms.openlocfilehash: c80732239b911f7cd3d615e9ce1e480db2749f17
ms.sourcegitcommit: fc0ac6bb6655d1f6e2de7c838f275779cd7a5de6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "11175183"
---
# Asociar extensiones de archivo con el modo Internet Explorer

En este artículo explica cómo asociar Microsoft Edge con el modo Internet Explorer con extensiones para aplicaciones de escritorio.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 86 o posterior.

## Instrucciones para la asociación de extensiones de archivo con el modo Internet Explorer

Las instrucciones siguientes muestran una entrada que asocia Microsoft Edge con el modo IE con el tipo de archivo .mht. Use los pasos siguientes como guía para configurar una asociación de archivos.

> [!NOTE]
> Se pueden establecer extensiones de archivos específicos para abrirlos en el modo Internet Explorer de forma predeterminada usando la directiva para **definir un archivo de configuración de asociaciones predeterminadas**. Para obtener más información, consulte [Directiva CSP: ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

1. Defina un nuevo ProgID con el canal de Microsoft Edge para usarlo para abrirlo con el modo Internet Explorer. El ProgID incluye el nombre y el icono de la aplicación, así como la ruta de acceso completa a msedge.exe.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""
```

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"
```

2. Configure las actualizaciones del shell para pasar la línea de comandos necesaria para abrir con el modo IE.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. Por último, asocie la extensión de archivo .mht a un ProgID nuevo. Agregue su ProgID como nombre de valor con el tipo de valor de REG_SZ.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

Después de asignar las claves descritas en el ejemplo anterior, los usuarios verán una opción adicional en el menú **Abrir con** para abrir un archivo .mht usando \<channel\> el modo IE de Microsoft Edge.

## Registro de ejemplo

Puede guardar el fragmento siguiente de código como un archivo .reg e importarlo en el registro.

```markdown
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""

```

## Recursos adicionales

- [Acerca del modo IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Información de sitios configurables](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [Información adicional del modo de empresa](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Configuración de asociaciones de tipo de archivo](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
