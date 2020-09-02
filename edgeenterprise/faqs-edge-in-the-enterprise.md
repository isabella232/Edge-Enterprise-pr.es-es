---
title: Preguntas frecuentes sobre Edge en la empresa
ms.author: jwhit
author: jwhit-MSFT
manager: laurawi
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Preguntas frecuentes sobre la implementación de Microsoft Edge en la empresa
ms.openlocfilehash: 0f6891f4f7187b23f6e3d4e7880fdafa49def351
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981125"
---
# Preguntas frecuentes sobre Microsoft Edge en la empresa

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## ¿Cómo puedo saber qué versión de MicrosoftEdge tengo?

En la esquina superior derecha de Microsoft Edge, haz clic en el icono de puntos suspensivos (**...**) y, después, haz clic en **Configuración**. Selecciona **Acerca de Microsoft Edge** para ver la versión de Microsoft Edge.

## ¿Seguirá recibiendo actualizaciones InternetExplorer11?

Nos comprometemos a conservar Internet Explorer como un explorador con soporte, confiable y seguro. Internet Explorer sigue siendo un componente de Windows y sigue el ciclo de vida de soporte técnico del SO en el que está instalado. Para obtener más información, consulta [Preguntas frecuentes del ciclo de vida: Internet Explorer](https://support.microsoft.com/help/17454/). Si bien continuamos ofreciendo soporte y actualizando Internet Explorer, las últimas funciones y actualizaciones de la plataforma solo estarán disponibles en Microsoft Edge.

## ¿Puedo ejecutar la versión actual de Microsoft Edge (versión heredada) en paralelo al probar la nueva versión?

Sí, no hay ningún problema. A partir del 15 de enero de 2020, la nueva versión de Microsoft Edge (basadas en Chromium) se distribuirá a los dispositivos de las ediciones Home y Pro que ejecuten Windows 10, versión 1803 o posterior. Los dispositivos unidos a un dominio están excluidos de esta actualización. Para más información, consulta [Introducción a las actualizaciones de Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-blocker-toolkit#overview). Puedes tener una instalación en paralelo de Microsoft Edge (versión heredada) cuando evalúes la próxima versión de Microsoft Edge. Para obtener más información, consulta [Cómo obtener acceso a la versión anterior de Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge). Además, cada uno de los nuevos canales de Microsoft Edge también admite instalaciones en paralelo. Para más información, consulta [Introducción a los canales de Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## ¿MicrosoftEdge (basado en Chromium) admite los controles ActiveX y BHO como Silverlight o Java?

No. Microsoft Edge no es compatible con los controles ActiveX y BHO como Silverlight o Java. Sin embargo, si está ejecutando aplicaciones web que usen controles ActiveX, BHO o modos de documentos heredados en Internet Explorer 11, puede configurarlos para que se ejecuten en modo IE en el nuevo Microsoft Edge. Para obtener más información, consulte [Configurar el modo IE en Microsoft Edge](https://docs.microsoft.com/DeployEdge/edge-ie-mode).

## ¿Se migrarán los favoritos desde la versión actual de Microsoft Edge o tendré que volver a agregarlos?

Actualmente, Microsoft Edge admite importar desde instalaciones existentes de Microsoft Edge, Chrome, Internet Explorer y Firefox (en Win10). Las siguientes opciones de configuración son compatibles con la importación: Marcadores, Historial, Contraseñas y Autorrelleno (pagos, direcciones y formularios genéricos). Puedes elegir importar desde la experiencia de primera ejecución o desde la configuración del explorador.  

## ¿Cuál es la diferencia entre los canales/compilaciones estable, Beta, Dev y Canary?

El canal estable de la próxima versión de Microsoft Edge es el canal más estable que ofrecemos, con las funciones orientadas a empresas preparadas para [ejecutar proyectos piloto y evaluar](https://aka.ms/EdgeEnterprise) en toda la organización. El canal beta te permite validar la próxima versión estable con un conjunto representativo de usuarios. Los canales estable y beta se actualizarán cada seis semanas, aproximadamente. Los canales Dev y Canary se seguirán actualizando semanalmente y diariamente, respectivamente. Los instaladores sin conexión (archivos MSI y PKG) solo están disponibles para los canales Stable, Beta y Dev. Para más información, consulta [Introducción a los canales de Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## ¿Qué tipo de compatibilidad con extensiones tengo con la nueva versión de Microsoft Edge?

Microsoft Edge admite extensiones de [Complementos de Microsoft Edge Insider](https://go.microsoft.com/fwlink/?linkid=2081222) y [Chrome Web Store](https://go.microsoft.com/fwlink/?linkid=2072338).

## ¿Se admite Administración de dispositivos móviles (MDM) y Microsoft Intune?

Sí. Ya se admite la configuración de Microsoft Edge en Windows 10 con Microsoft Intune y Administración de dispositivos móviles (MDM). Para obtener más información, consulta [Configurar Microsoft Edge con Microsoft Intune](configure-edge-with-intune.md) y [Configurar Microsoft Edge con Administración de dispositivos móviles](configure-edge-with-mdm.md).

## ¿Admite WSUS la implementación inicial del nuevo Microsoft Edge?

No. WSUS es compatible con la actualización de instalaciones de MSI existentes de Microsoft Edge, pero no se puede usar para la implementación inicial. Si el propósito es administrar actualizaciones en última instancia por medio de WSUS, la implementación inicial se puede realizar mediante una herramienta de administración, como [ConfigMgr](https://docs.microsoft.com/configmgr/apps/deploy-use/deploy-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json).

## Consulte también

- [Página de aterrizaje de documentación de Microsoft Edge](https://docs.microsoft.com/DeployEdge/)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
