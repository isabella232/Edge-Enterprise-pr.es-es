---
title: Planear transición al modo quiosco
ms.author: aguta
author: aguta
manager: srugh
ms.date: 02/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Planear transición al modo quiosco
ms.openlocfilehash: b563f7ac773fb295d42e2b27b1259af321ce5f70
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617749"
---
# <a name="plan-your-kiosk-mode-transition"></a>Planear transición al modo quiosco

Este artículo ofrece orientación sobre cómo realizar la transición tu quiosco de Microsoft Edge Legacy a Microsoft Edge.  

> [!NOTE]
> Este artículo se aplica a los canales estables, beta y de desarrollo de Microsoft Edge, versión 87 o posterior.

> [!IMPORTANT]
> Cuando el soporte de Microsoft Edge Legacy finalice el 9 de marzo de 2021, será eliminado y sustituido por Microsoft Edge en Chromium como parte de la actualización de Windows en abril. Para más detalles, ve a [esta entrada del blog](https://aka.ms/EdgeLegacyEOS). Para seguir usando los escenarios del quiosco basados en el navegador, debes instalar Microsoft Edge en Chromium y configurar el modo de pantalla completa antes de la publicación de Windows Update de abril en tu dispositivo.

## <a name="kiosk-setup-steps"></a>Pasos para configurar el modo quiosco

Usa los siguientes pasos como guía para configurar un quiosco en Microsoft Edge.

**Paso 1: evaluar las necesidades con respecto a la funcionalidad del modo quiosco que se ha lanzado (y que se lanzará).** La siguiente tabla enumera las características compatibles con el modo quiosco en Microsoft Edge en Chromium y Microsoft Edge Legacy. Utiliza esta tabla como guía para la transición a Microsoft Edge comparando cómo estas características son compatibles en ambas versiones de Microsoft Edge.

|Característica|Señalización interactiva\digital|Navegación pública|Disponible con la versión de Microsoft Edge (y versiones posteriores)|Disponible con Microsoft Edge Legacy|
|-|-|-|-|-|
|Navegación de InPrivate|esté|esté|89|esté|
|Restablecer por inactividad|esté|esté|89|Y|
|[Barra de direcciones de solo lectura](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (directiva) |N|esté |89|N|
|[Eliminar descargas al salir](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (directiva)  | esté|esté |89|N|
|F11 bloqueado (entrada y salida en pantalla completa) | esté | esté | 89 |esté|
|F12 bloqueado (Iniciar Herramientas de desarrollo) | esté | esté | 89 |Y|
| Soporte con varias pestañas | N| esté| 89|Y|
|[Permitir compatibilidad con direcciones URL](./microsoft-edge-policies.md#urlallowlist) (directiva)|esté|esté|89|N|
|[Bloquear compatibilidad con direcciones URL](./microsoft-edge-policies.md#urlblocklist) (directiva)|Y|esté|89|N|
|[Mostrar el botón Inicio](./microsoft-edge-policies.md#showhomebutton) (directiva)|N|esté|89|Y|
|[Administrar favoritos](./microsoft-edge-policies.md#managedfavorites) (directiva)|N|esté|89|Y|
|[Habilitar impresora](./microsoft-edge-policies.md#printingenabled) (directiva)|Y|esté|89|Y|
|[Configurar la nueva dirección URL de la página de pestaña](./microsoft-edge-policies.md#newtabpagelocation) (directiva)|N|esté|89|Y|
|Botón Finalizar sesión | N| esté| 89|Y|
|Todas las direcciones URL internas de Microsoft Edge están bloqueadas, excepto *edge://downloads* y *edge://print* |N|esté|89|esté|
| CTRL+N bloqueado (abrir una nueva ventana) | esté | esté | 89 |Y|
| CTRL+T bloqueado (abrir nueva pestaña) |Y | esté | 89 |Y|
|La configuración y más (...) mostrará solo las opciones necesarias  |esté |esté |89 |esté|
|Restringir el inicio de otras aplicaciones desde el explorador|Y|Y|90|Y|
|Bloqueo de la configuración de impresión de la interfaz de usuario|Y|Y|90|Y|
|[Establecer la página de la nueva pestaña como página principal](./microsoft-edge-policies.md#homepageisnewtabpage) (directiva)|N|Y|90|Y|

> [!NOTE]
> Para obtener información sobre el calendario de lanzamientos de Microsoft Edge, consulta [ Calendario de lanzamientos de Microsoft Edge](microsoft-edge-release-schedule.md).

**Paso 2: probar el nuevo quiosco en Microsoft Edge.** Recomendamos que pruebes a configurar el modo quiosco en Microsoft Edge. Una forma rápida y sencilla de probar el modo pantalla completa es configurar una aplicación única de acceso asignado mediante la Configuración de Windows, como se describe a continuación.

1. Las actualizaciones mínimas del sistema para los sistemas operativos enumerados en la siguiente tabla.

|Sistema operativo|Versión|Actualizaciones|
|--|--|--|
|Windows 10 | 2004 o posterior|[KB4601382 o posterior](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 o posterior](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. Para probar las últimas funciones, puedes descargar el último [Canal estable de Microsoft Edge](https://www.microsoftedgeinsider.com/download), versión 89 o superior.

   > [!IMPORTANT]
   > Debido a que se requiere una instalación a nivel de dispositivo, el canal Canary no es compatible.

3. En el ordenador del quiosco, abre la configuración de Windows y escribe "quiosco" en el campo de búsqueda. Selecciona  **Configurar un quiosco (acceso asignado)**, como se muestra en la siguiente captura de pantalla, para abrir el cuadro de diálogo de creación del quiosco.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar el quiosco con el acceso asignado":::

4. En la página **Configurar un quiosco** , haz clic en  **Empezar**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Página de quiosco: introducción":::

5. Escribe un nombre para crear una nueva cuenta de quiosco o elije una cuenta existente de la lista rellenada y haz clic en  **Siguiente**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Modo de pantalla completa: crear cuenta":::

6. En la página **Elegir una aplicación de modo pantalla completa** , seleccione **Microsoft Edge** y haga clic en  **Siguiente**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Elegir un modo de pantalla completa: signo digital de pantalla completa":::

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

## <a name="additional-scenarios-that-require-you-to-recreate-an-existing-kiosk-mode"></a>Escenarios adicionales que requieren recrear un modo de quiosco existente

Si actualizas a Windows 10, versión 20H2, se instalará Microsoft Edge en Chromium y se ocultará Microsoft Edge Legacy. En este caso, tendrás que volver a configurar el modo quiosco en Microsoft Edge en Chromium.

## <a name="how-to-get-help"></a>Cómo obtener ayuda

El modo quiosco puede ser una parte importante de tu trabajo diario, por lo que queremos ayudar a que esta transición sea lo más fácil posible y te ayude a evitar interrupciones. Si tu empresa necesita ayuda para la transición a Microsoft Edge en Chromium:

- [El](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=a77ee9b7-b6b6-aa08-d7b9-887ebe228207) soporte técnico está disponible en Microsoft. 
- [El soporte técnico](https://www.microsoft.com/fasttrack/microsoft-365/microsoft-edge?rtc=1) de FastTrack también está disponible sin coste adicional para los clientes con 150 o más puestos de pago de Windows 10 Enterprise.
- [La asesoría de aplicaciones ](https://www.microsoft.com/en-us/fasttrack/microsoft-365/app-assure) está disponible si experimentas problemas de compatibilidad de sitios o aplicaciones.

## <a name="see-also"></a>Consulta también

- [Página de inicio de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [El nuevo Microsoft Edge sustituirá a Microsoft Edge Legacy con el lanzamiento del martes de abril de Windows 10 Update](https://techcommunity.microsoft.com/t5/microsoft-365-blog/new-microsoft-edge-to-replace-microsoft-edge-legacy-with-april-s/ba-p/2114224)