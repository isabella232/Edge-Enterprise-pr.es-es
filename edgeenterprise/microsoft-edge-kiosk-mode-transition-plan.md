---
title: Planear transición al modo quiosco
ms.author: aguta
author: aguta
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Planear transición al modo quiosco
ms.openlocfilehash: 3a438c6dd71d9e1f0e644d24e3b1d1d60b099e8e
ms.sourcegitcommit: b1d49b229c47dc1d99e1b677d75aad38b3334ed6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "11314240"
---
# Planear transición al modo quiosco

Este artículo ofrece orientación sobre cómo realizar la transición tu quiosco de Microsoft Edge Legacy a Microsoft Edge.  

> [!NOTE]
> Este artículo se aplica a los canales estables, beta y de desarrollo de Microsoft Edge, versión 87 o posterior.

> [!IMPORTANT]
> Cuando el soporte de Microsoft Edge Legacy finalice el 9 de marzo de 2021, será eliminado y sustituido por Microsoft Edge en Chromium como parte de la actualización de Windows en abril. Para más detalles, ve a [esta entrada del blog](https://aka.ms/EdgeLegacyEOS). Para seguir usando los escenarios del quiosco basados en el navegador, debes instalar Microsoft Edge en Chromium y configurar el modo de pantalla completa antes de la publicación de Windows Update de abril en tu dispositivo.

## Pasos para configurar el modo quiosco

Usa los siguientes pasos como guía para configurar un quiosco en Microsoft Edge.

**Paso 1: evaluar las necesidades con respecto a la funcionalidad del modo quiosco que se ha lanzado (y que se lanzará).** La siguiente tabla enumera las características compatibles con el modo quiosco en Microsoft Edge en Chromium y Microsoft Edge Legacy. Utiliza esta tabla como guía para la transición a Microsoft Edge comparando cómo estas características son compatibles en ambas versiones de Microsoft Edge.

|Característica|Señalización interactiva\digital|Navegación pública|Disponible con la versión de Microsoft Edge (y versiones posteriores)|Disponible con Microsoft Edge Legacy|
|-|-|-|-|-|
|Navegación de InPrivate|esté|esté|89|Esté|
|Restablecer por inactividad|esté|esté|89|Esté|
|[Barra de direcciones de solo lectura](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (directiva) |N|esté |89|N|
|[Eliminar descargas al salir](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (directiva)  | esté|esté |89|N|
|F11 bloqueado (entrada y salida en pantalla completa) | esté | esté | 89 |Esté|
|F12 bloqueado (iniciar Herramientas de desarrollo) | esté | esté | 89 |Esté|
| Soporte para pestañas múltiples | N| esté| 89|Esté|
|[Permitir soporte para las direcciones URL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) (directiva)|Esté|esté|89|N|
|[Bloquear soporte para direcciones URL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) (directiva)|Esté|esté|89|N|
|[Mostrar el botón Inicio](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showhomebutton) (directiva)|N|esté|89|Esté|
|[Administrar favoritos](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedfavorites) (directiva)|N|esté|89|Esté|
|[Habilitar impresora](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printingenabled) (directiva)|Esté|esté|89|Esté|
|[Configurar la URL de la nueva pestaña](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation) (directiva)|N|esté||Esté|
|Botón de finalizar sesión | N| esté| 89|Esté|
|Todas las direcciones URL internas de Microsoft Edge están bloqueadas, excepto *edge://downloads* y *edge://print* |N|esté|89|Esté|
| CTRL+N bloqueado (abrir una nueva ventana) | esté | esté | 89 |Esté|
| CTRL+T bloqueado (abrir nueva pestaña) |Esté | esté | 89 |Esté|
|Configuracióny más (...) mostrará solo las opciones necesarias  |Esté |esté |89 |Esté|
|Restringir el inicio de otras aplicaciones desde el navegador|Esté|Esté|90/91|Esté|
|Bloqueo de la configuración de impresión de la interfaz de usuario|Esté|Esté|90/91|Esté|
|[Establecer la página de nueva pestaña como página de inicio](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepageisnewtabpage) (directiva)|-|-|TBD|Esté|

> [!NOTE]
> Para obtener información sobre el calendario de lanzamientos de Microsoft Edge, consulta [ Calendario de lanzamientos de Microsoft Edge](microsoft-edge-release-schedule.md).

**Paso 2: probar el nuevo quiosco en Microsoft Edge.** Recomendamos que pruebes a configurar el modo quiosco en Microsoft Edge. Una forma rápida y sencilla de probar el modo quiosco es configurar una aplicación única de acceso asignado mediante la Configuración de Windows, como se describe a continuación.

1. Instala la última versión de Windows 10 Insider Preview, versión 20215 o superior. Sigue las instrucciones que se indican en [Introducción a las versiones preliminares de Windows 10](https://docs.microsoft.com/windows-insider/get-started).
2. Instala la versión más reciente del [canal estable de Microsoft Edge](https://www.microsoft.com/edge), versión 87 o posterior.  Para probar las últimas características, puedes descargar el último [canal Microsoft Edge Beta ](https://www.microsoftedgeinsider.com/download), versión 89 o superior.

   > [!IMPORTANT]
   > Debido a que se requiere una instalación a nivel de dispositivo, el canal Canary no es compatible.

3. En el ordenador del quiosco, abre la configuración de Windows y escribe "quiosco" en el campo de búsqueda. Selecciona  **Configurar un quiosco (acceso asignado)**, como se muestra en la siguiente captura de pantalla, para abrir el cuadro de diálogo de creación del quiosco.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar el quiosco con el acceso asignado":::

4. En la página **Configurar un quiosco** , haz clic en  **Empezar**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Página de quiosco: introducción":::

5. Escribe un nombre para crear una nueva cuenta de quiosco o elije una cuenta existente de la lista rellenada y haz clic en  **Siguiente**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Modo de pantalla completa: crear cuenta":::

6. En la página **Elegir una aplicación de quiosco** , selecciona **Microsoft Edge** y haz clic en  **Siguiente**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Modo quiosco: elegir una aplicación":::

7. Selecciona una de las siguientes opciones para la visualización de Microsoft Edge cuando se ejecuta en modo quiosco:

   - Señalización digital/interactiva: muestra un sitio específico en modo de pantalla completa, ejecutando Microsoft Edge.
   - Explorador público: ejecuta una versión multipestaña limitada de Microsoft Edge.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Pantalla completa: inicio de sesión digital en pantalla completa.":::

8. Selecciona  **Siguiente**.
9. Escribe la dirección URL que quieres cargar cuando se inicie la pantalla completa.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Modo de pantalla completa: escribir URL":::

10. Acepta el valor predeterminado de 5 minutos para el tiempo de inactividad o proporciona un valor.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Modo de pantalla completa: introducir el tiempo de inactividad":::

11. Haz clic en  **Siguiente**.
12. Cierra la ventana  **Configuración**  para guardar y aplicar las opciones.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Modo de pantalla completa: finalizar la configuración":::

13. Cierra sesión en el dispositivo de quiosco e inicia sesión con la cuenta de quiosco local para validar la configuración.

**Paso 3: desarrollar un plan de transición.** En función de las pruebas y necesidades organizativas, recomendamos desarrollar un plan de transición y pasar a Microsoft Edge en Chromium antes de que finalice el soporte para Microsoft Edge Legacy el 9 de marzo de 2021.

## Escenarios adicionales que requieren recrear un modo de quiosco existente

Si actualizas a Windows 10, versión 20H2, se instalará Microsoft Edge en Chromium y se ocultará Microsoft Edge Legacy. En este caso, tendrás que volver a configurar el modo quiosco en Microsoft Edge en Chromium.

## Cómo obtener ayuda

El modo quiosco puede ser una parte importante de tu trabajo diario, por lo que queremos ayudar a que esta transición sea lo más fácil posible y te ayude a evitar interrupciones. Si tu empresa necesita ayuda para la transición a Microsoft Edge en Chromium:

- [El](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=a77ee9b7-b6b6-aa08-d7b9-887ebe228207) soporte técnico está disponible en Microsoft. 
- [El soporte técnico](https://www.microsoft.com/fasttrack/microsoft-365/microsoft-edge?rtc=1) de FastTrack también está disponible sin coste adicional para los clientes con 150 o más puestos de pago de Windows 10 Enterprise.
- [La asesoría de aplicaciones ](https://www.microsoft.com/en-us/fasttrack/microsoft-365/app-assure) está disponible si experimentas problemas de compatibilidad de sitios o aplicaciones.

## Consulta también

- [Página de inicio de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [El nuevo Microsoft Edge sustituirá a Microsoft Edge Legacy con el lanzamiento del martes de abril de Windows 10 Update](https://techcommunity.microsoft.com/t5/microsoft-365-blog/new-microsoft-edge-to-replace-microsoft-edge-legacy-with-april-s/ba-p/2114224)