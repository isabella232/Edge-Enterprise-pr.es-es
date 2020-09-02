---
title: Pantalla completa de Microsoft Edge
ms.author: brianalt
author: brianalt
manager: seanlynd
ms.date: 01/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Pantalla completa de Microsoft Edge
ms.openlocfilehash: 7a690820752b5361349bf394055a737bd8175215
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981210"
---
# Pantalla completa de Microsoft Edge

En este artículo se ofrece una introducción de las opciones de pantalla completa de Microsoft Edge (versión 77 o posterior). También abarca lo que se necesita para seguir usando la pantalla completa de Microsoft Edge (versión heredada) (versión 45 y anteriores).

Para obtener información sobre la pantalla completa de Microsoft Edge (versión heredada) (versión 45 y anteriores), consulta [Implementar pantalla completa de Microsoft Edge](https://aka.ms/edgekioskmode).

## Microsoft Edge con acceso asignado

Microsoft Edge se puede ejecutar con [acceso asignado a varias aplicaciones](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) en Windows 10, que es el equivalente del tipo de pantalla completa de "exploración normal" de Microsoft Edge (versión heredada). Para configurar Microsoft Edge con acceso asignado a varias aplicaciones, sigue las instrucciones acerca de cómo [Configurar un quiosco multimedia de varias aplicaciones](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). El AUMID para el canal estable de Microsoft Edge es **MSEdge**.

Al usar Microsoft Edge con acceso asignado de varias aplicaciones, puedes usar las [directivas del explorador Microsoft Edge](microsoft-edge-policies.md) para configurar la experiencia de exploración de manera que cumpla con tus requisitos únicos.

En la actualidad, Microsoft Edge no es compatible con los mismos tipos de pantalla completa de Microsoft Edge (versión heredada) para acceso asignado de aplicación única y el tipo de pantalla completa de "Exploración pública" en el acceso asignado de varias aplicaciones. Si necesitas un explorador para un dispositivo de pantalla completa con acceso asignado de aplicación única, recomendamos el uso de la [pantalla completa de Microsoft Edge (versión heredada)](https://aka.ms/edgekioskmode) o la aplicación [Microsoft Kiosk Browser](https://www.microsoft.com/p/kiosk-browser/9ngb5s5xg2kp?activetab=pivot:overviewtab). 

## Parámetro de la línea de comandos “--kiosk” de Microsoft Edge

Puedes iniciar Microsoft Edge en pantalla completa con el parámetro de la línea de comandos "`--kiosk`". Esta acción abre el explorador en pantalla completa con el método abreviado de teclado de pantalla completa deshabilitado (F11). Para ello, crea un acceso directo con el destino establecido en:<br>
*`"<local path>\msedge.exe" --kiosk http://bing.com`*

> [!NOTE]
> El parámetro "`--kiosk`" no impedirá que el usuario obtenga acceso a los métodos abreviados de teclado de Windows y no impedirá que se ejecuten otras aplicaciones. Para lograr este tipo de control, considera la posibilidad de usar [AppLocker para crear un quiosco de Windows 10](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) y un [filtro de teclado](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter).

Para salir del modo de pantalla completa y cerrar el explorador, usa Alt+F4.

## Compatibilidad con la pantalla completa de Microsoft Edge (versión heredada)

Cuando se instala la nueva versión del canal estable de Microsoft Edge, Microsoft Edge (versión heredada) está oculto y todos los intentos de iniciar Microsoft Edge (versión heredada) se redirigen a la nueva versión. Para obtener información acerca de:

- Requisitos de Windows Update, consulta [Actualizaciones de Windows para admitir la próxima versión de Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md) 
- Acceso a Microsoft Edge (versión heredada) tras la instalación de Microsoft Edge, consulta [Acceso a Microsoft Edge (versión heredada tras la instalación de la nueva versión de Microsoft Edge](microsoft-edge-sysupdate-access-old-edge.md)
 
Para seguir usando la pantalla completa de Microsoft Edge (versión heredada) en tus dispositivos de pantalla completa, realiza una de las siguientes acciones: 

- Si tienes previsto instalar el canal estable de Microsoft Edge, quieres permitir que se instale o si ya está instalado en el dispositivo de pantalla completa, implementa la directiva de Microsoft Edge [Permitir la experiencia de exploradores Microsoft Edge en paralelo](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs).
- Para impedir que el canal estable de Microsoft Edge se instale en los dispositivos de quiosco multimedia, implemente la directiva [Valor predeterminado de Permitir instalación](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allow-installation-default) para el canal estable o considere la posibilidad de usar el [kit de herramientas de bloqueo para deshabilitar la entrega automática de Microsoft Edge](microsoft-edge-blocker-toolkit.md). 

## Consulta también

- [Configurar quioscos multimedia y señales digitales en las ediciones de escritorio de Windows](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Implementar la pantalla completa de Microsoft Edge (versión heredada)](https://aka.ms/edgekioskmode) 
- [Planear tu implementación de Microsoft Edge](deploy-edge-plan-deployment.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
