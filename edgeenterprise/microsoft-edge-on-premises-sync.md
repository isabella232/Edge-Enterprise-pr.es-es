---
title: Sincronización local para usuarios de Active Directory (AD)
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronización local para usuarios de Active Directory (AD)
ms.openlocfilehash: 89f061072fdaa748d317ca8dc0c290893cfdfd6c
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981212"
---
# Sincronización local para usuarios de Active Directory (AD)

En este artículo, se explica cómo los usuarios de Active Directory (AD) pueden desplazarse por los favoritos y las configuraciones de Microsoft Edge entre equipos sin una conexión a los servicios en la nube de Microsoft.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 85 o posterior.

## Introducción

Sincronizar los datos de usuario en Microsoft Edge requiere, de manera usual, una cuenta de Microsoft o una cuenta de Azure Active Directory (Azure AD), y una conexión a los servicios en la nube de Microsoft. Con la sincronización local, Microsoft Edge guarda los favoritos y la configuración de un usuario de Active Directory en un archivo que se puede mover entre diferentes equipos. La sincronización local no interfiere con la sincronización en la nube para los perfiles que admiten esta característica.

## Cómo funciona

Microsoft Edge permite asociar perfiles con cuentas de Active Directory (AD), los cuales no se pueden usar con la sincronización en la nube. Cuando está habilitada la sincronización local, los datos del perfil de AD se guardan en un archivo llamado profile.pb. De forma predeterminada, este archivo se almacena en *%APP_DATA%/Microsoft/Edge*. Después de escribir el archivo, este puede moverse entre distintos equipos, y los datos de usuario se leerán y se escribirán en cada uno de estos equipos.

## Usar la sincronización local

Para usar la sincronización local, tiene que habilitarla, asociar un perfil a una cuenta de AD y, de manera opcional, cambiar la ubicación de los datos de usuario.

### Habilitar la sincronización local

Para habilitar la sincronización local en Microsoft Edge, configure la directiva [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled).

### Asegúrese de que existe un perfil asociado a una cuenta de Active Directory

La sincronización local solo funciona con el perfil asociado a una cuenta de Active Directory (AD). Si no existe dicho perfil, la sincronización local no funcionará. Para asegurarse de que los usuarios inicien sesión con una cuenta de AD, configure la directiva [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin).

### Cambiar la ubicación de los datos de usuario (opcional)

De forma predeterminada, los datos del usuario se almacenan en un archivo con el nombre de**profile.pb** en *% APP_DATA%/Microsoft/Edge*. Para cambiar la ubicación de este archivo, configure la directiva [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation).

## Cambios en la experiencia de usuario cuando está habilitada la sincronización local

Cuando se habilita la sincronización local, no se le pedirá a los usuarios que habiliten la sincronización. Además, los usuarios no pueden desactivar la sincronización en la Configuración de sincronización, y tampoco pueden activar los tipos de sincronización que no son compatibles con la sincronización local.

## Notas de uso de sincronización local

### Ejecución de sincronización en la nube y sincronización local en el mismo equipo

La sincronización local no interfiere con la sincronización en la nube. Si Microsoft Edge tiene varias cuentas de Microsoft o perfiles de Azure Active Directory que se sincronizan con la nube, estos perfiles continuarán sincronizándose mientras la sincronización local esté habilitada.

### No se recomienda ejecutar Microsoft Edge en más de un equipo a la vez

Como la sincronización local funciona moviendo un archivo de datos de usuario entre equipos, esta no sincroniza los cambios entre sesiones simultáneas. Por este motivo, la sincronización local funciona mejor cuando se usa en un solo equipo a la vez. Si hay sesiones locales simultáneas en ejecución, es posible que los datos de otro equipo se sobrescriban de forma inesperada sobre los datos de cualquiera de los equipos la próxima vez que inicie sesión en un explorador.

> [!NOTE]
> Microsoft Edge bloquea el archivo **profile.pb** cuando está habilitada la sincronización local. Si se usa el redireccionamiento de carpetas para compartir un único archivo **profile.pb** entre equipos diferentes, solo se puede iniciar una sesión de Microsoft Edge que use ese archivo.

### Usar otras directivas de sincronización con la sincronización local

Se puede usar la directiva [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) para deshabilitar de forma selectiva la sincronización de la configuración o de los favoritos, si así lo desea. Si la directiva [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) está activa, se deshabilitará también la sincronización local.  

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge y Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Sincronización de Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
