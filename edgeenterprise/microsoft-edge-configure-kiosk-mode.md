---
title: Configurar la pantalla completa en Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 10/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar la pantalla completa en Microsoft Edge
ms.openlocfilehash: 799b3dd4b7fc96f0b8e5cb718bca98fd4f38ec15
ms.sourcegitcommit: 78905f66f4a6590a57c8f2bf808af92106b62996
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "11094867"
---
# Configurar la pantalla completa en Microsoft Edge

En este artículo se describe cómo configurar las opciones de pantalla completa de Microsoft Edge que puedes probar. También hay una guía básica de las características relevantes.

> [!NOTE]
> Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.

## Introducción

El modo de pantalla completa de Microsoft Edge ofrece dos experiencias de bloqueo del explorador para que las organizaciones puedan crear, administrar y proporcionar la mejor experiencia para sus clientes. Están disponibles las siguientes experiencias de bloqueo:  

- La experiencia de indicación digital/interactiva muestra un sitio específico en el modo de pantalla completa.
- La experiencia de explorador público ejecuta una versión multipestaña limitada de Microsoft Edge.

En ambas experiencias se ejecuta una sesión de Microsoft Edge InPrivate, que protege los datos de usuario.

## Configurar la pantalla completa de Microsoft Edge

Ya está disponible un conjunto inicial de características de modo de pantalla completa para probar el Canal Microsoft Edge Canary, versión 87. Puedes descargar Microsoft Edge Canary en la página [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download).

### Características del modo de pantalla completa

Las siguientes características están disponibles:

- La navegación de InPrivate protege los datos del usuario eliminando los datos y descargas del explorador cuando termina la sesión.
- Una directiva para configurar la eliminación de descargas al dejar la sesión.
- La opción de restablecer una sesión de usuario después de un determinado período de inactividad.
- Un conjunto inicial de funciones de bloqueo. Están disponibles las funciones siguientes:

  - Menú contextual del mouse
  - Herramientas de desarrollo con la tecla F12
  - Salir de la pantalla completa con la tecla F11 (si estás en el modo de pantalla completa)
  - Bloqueo del conjunto inicial de páginas *Edge://*

> [!NOTE]
> A medida que el modo de pantalla completa evolucione, habrá más características disponibles.

## Uso del modo de pantalla completa

Puedes invocar el modo de pantalla completa de Microsoft Edge con las siguientes opciones de línea de comandos de Windows 10:

- Indicación digital/interactiva de pantalla completa: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- Exploración pública de pantalla completa: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### Opciones de la línea de comandos adicionales

- `--no-first-run` : deshabilita la primera experiencia de ejecución de Microsoft Edge.
- `--kiosk-idle-timeout-minutes` : cambia el tiempo en minutos de la última actividad de usuario antes de que el modo de pantalla completa de Microsoft Edge restablezca la sesión del usuario. Se admiten los valores siguientes:

  - Valores predeterminados
    - Pantalla completa: desactivado
    - Navegación pública: 5 min
  - Valores permitidos
    - 0: desactiva el temporizador
    - 1-1440: número de minutos para restablecer el temporizador de inactividad

## Microsoft Edge con acceso asignado

### Quiosco multimedia de aplicación única

En la actualidad, Microsoft Edge es compatible con un subconjunto de los mismos tipos de pantalla completa que Microsoft Edge (versión anterior) para el acceso asignado a una sola aplicación con las siguientes experiencias de bloqueo, señalización digital e interactiva y navegación pública.  

Actualmente, la pantalla completa de Microsoft Edge con acceso asignado está disponible para probar con la última  [versión preliminar de Windows 10 Insider](https://insider.windows.com/), versión 20215 o superiores, y con el  [Canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), versión 87.0.644.4 o superiores.

**¿Cómo puedo obtener la vista previa de Windows Insider?**

Para instalar una versión preliminar de Windows 10 Insider en un PC, sigue las instrucciones que se indican en  [Introducción a las versiones preliminares de Windows 10 Insider](https://docs.microsoft.com/windows-insider/get-started).

### Pantalla completa de varias aplicaciones

Microsoft Edge se puede ejecutar con [acceso asignado a varias aplicaciones](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) en Windows 10, que es el equivalente del tipo de pantalla completa de "Exploración normal" de Microsoft Edge (versión anterior). Para configurar Microsoft Edge con acceso asignado a varias aplicaciones, sigue las instrucciones acerca de cómo [Configurar un quiosco multimedia de varias aplicaciones](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). (El AUMID para el canal estable de Microsoft Edge es **MSEdge**).

Al configurar la pantalla completa de Microsoft Edge cuando usas Microsoft Edge con acceso asignado de varias aplicaciones, puedes usar las [directivas del explorador Microsoft Edge](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) para configurar la experiencia de exploración de manera que cumpla con tus requisitos únicos.

### Usar la configuración de Windows

La configuración de Windows es la manera más sencilla de configurar uno o dos dispositivos de quiosco de aplicación única. Usa los siguientes pasos para configurar un equipo de quiosco de una sola aplicación.

1. Instala la última versión preliminar de Windows 10 Insider, versiones 20215 o superiores. Sigue las instrucciones que se indican en [Introducción a las versiones preliminares de Windows 10](https://docs.microsoft.com/windows-insider/get-started).
2. Instala la última versión del [canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), 87.0.644.4 o superior.

   > [!IMPORTANT]
   > Dado que es necesario instalar a nivel de dispositivo, solo se admite un canal que no sea Canary.

3. En el equipo de quiosco, abre la configuración de Windows y escribe "quiosco" en el campo de búsqueda. Selecciona  **Configurar un quiosco (acceso asignado)**, como se muestra en la siguiente captura de pantalla, para abrir el cuadro de diálogo de creación del quiosco.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar el quiosco con el acceso asignado":::

4. En la página **Configurar un quiosco** , haz clic en  **Empezar**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Configurar el quiosco con el acceso asignado":::

5. Escribe un nombre para crear una nueva cuenta de quiosco o elije una cuenta existente de la lista rellenada y haz clic en  **Siguiente**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Configurar el quiosco con el acceso asignado":::

6. En la página **Elegir una aplicación de quiosco** , selecciona **Microsoft** Edge y haz clic en  **Siguiente**.

   > [!NOTE]
   > Esto solo se aplica a Microsoft Edge Dev, Beta y canales estables.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Configurar el quiosco con el acceso asignado":::

7. Elige una de las siguientes opciones para decidir cómo se muestra Microsoft Edge cuando se ejecuta en el modo de pantalla completa:

   - Señalización de indicación digital/interactiva: muestra un sitio específico en el modo de pantalla completa que ejecuta Microsoft Edge
   - Explorador público: ejecuta una versión multipestaña limitada de Microsoft Edge.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Configurar el quiosco con el acceso asignado":::

8. Selecciona  **Siguiente**.
9. Escribe la dirección URL que quieres cargar cuando se inicie la pantalla completa.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Configurar el quiosco con el acceso asignado":::

10. Acepta el valor predeterminado de 5 minutos para el tiempo de inactividad o proporciona un valor.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Configurar el quiosco con el acceso asignado":::

11. Haz clic en  **Siguiente**.
12. Cierra la ventana  **Configuración**  para guardar y aplicar las opciones.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Configurar el quiosco con el acceso asignado"  de configuración solo habilitará las opciones necesarias (por ejemplo, Imprimir, Ayuda, Comentarios y Leer en voz alta).
  - Bloqueo adicional de páginas *edge://* (por ejemplo, *edge://settings*)
  - Configurar la interfaz de usuario de opciones de impresión
  - Limitar el explorador de archivos a la carpeta de descargas.

### A principios de 2021

Agregaremos las siguientes características y soporte:

- Disponibilidad general del modo de pantalla completa de Microsoft Edge con el acceso asignado a una sola aplicación en Windows.
- Características adicionales de paridad con Microsoft Edge (versión anterior).
- Integración con Intune para configurar dispositivos con la experiencia de usuario del perfil de modo de pantalla completa.

## Consulte también

- [Configurar quioscos multimedia y señales digitales en las ediciones de escritorio de Windows](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Implementar la pantalla completa de Microsoft Edge (versión heredada)](https://aka.ms/edgekioskmode)
- [Planear tu implementación de Microsoft Edge](deploy-edge-plan-deployment.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
