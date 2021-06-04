---
title: Implementación progresiva para actualizaciones del canal estable de Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 05/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Implementación progresiva para actualizaciones del canal estable de Microsoft Edge
ms.openlocfilehash: 5b0d2f58318b10538d0470b644d346b5b9b9489b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981160"
---
# Implementación progresiva para actualizaciones del canal estable de Microsoft Edge

A partir de la versión 83 de Microsoft Edge, realizaremos implementaciones graduales de las actualizaciones principales en el canal estable de Microsoft Edge en un lapso de pocos días. Este lanzamiento progresivo nos permite supervisar las actualizaciones y actualizar el explorador de forma segura en toda la organización.

> [!NOTE]
> Esto aplica a la versión 83 o posterior del canal estable de Microsoft Edge.

##  <a name="why-do-we-need-progressive-rollout"></a>¿Por qué necesitamos la implementación progresiva?

Al supervisar el estado de nuestras actualizaciones de manera cercana y llevar a cabo las actualizaciones a lo largo de varios días, podemos limitar el impacto de los problemas que se pueden producir en la nueva actualización. Con la versión 83 de Microsoft Edge, las implementaciones progresivas se habilitarán para todas las versiones de Microsoft Edge para Windows 7, Windows 8 y 8.1, y Windows 10. Ofreceremos soporte técnico de Microsoft Edge en Mac tan pronto como esté listo.

##  <a name="how-will-the-updates-work"></a>¿Cómo funcionan las actualizaciones?

Cada instalación de Microsoft Edge se asigna a un valor de actualización. Cuando comencemos con las implementaciones, verá la actualización cuando el valor de su dispositivo se encuentre dentro del intervalo de valores de actualización. A medida que progresa la implementación (en pocos días), todos los usuarios obtendrán la actualización. Las actualizaciones del explorador con correcciones de seguridad críticas tendrán una cadencia de lanzamiento más rápida que las actualizaciones que no tengan correcciones de seguridad importantes. Esto se lleva a cabo para asegurar la protección inmediata frente a las vulnerabilidades.

##  <a name="how-does-this-affect-enterprises"></a>¿Cómo afecta esto a las empresas?

Los artefactos de Microsoft Edge se distribuyen a las empresas a través de varios mecanismos, como Microsoft Intune, Windows Server Update Services (WSUS) y Administrador de configuración. Estas herramientas de implementación se comportan de manera diferente en lo que respecta al lanzamiento progresivo:

- Las empresas que administran la distribución mediante Microsoft Intune se registran para actualizaciones automáticas. Se usa la implementación progresiva y todos los usuarios verán una actualización en unos días.
- Las empresas que administran la distribución mediante WSUS (Windows Server Update Services) o Administrador de configuración no están registradas para las actualizaciones automáticas. Los administradores pueden administrar y aplicar las actualizaciones que estarán disponibles desde el principio. El lanzamiento progresivo no afecta a este proceso.

Comparta sus valiosos comentarios a través de la opción de voz, el botón comentarios en la aplicación, o, sino, debajo de los comentarios, en caso de que tenga alguna duda o consulta.

##  <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
