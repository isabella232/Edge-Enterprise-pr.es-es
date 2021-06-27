---
title: Configurar el modo de pantalla completa en Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 04/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Obtenga información sobre las características del modo de pantalla completa y sobre cómo configurar las opciones del modo de pantalla completa de Microsoft Edge.
ms.openlocfilehash: 20cb32c0cd27ad6d7437ed8ae0440560f3ed71b2
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617860"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a>Configurar el modo de pantalla completa en Microsoft Edge

En este artículo se describe cómo configurar las opciones de pantalla completa de Microsoft Edge que puedes probar. También hay una guía básica de las características a las que nos dirigiremos.

> [!NOTE]
> Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.

> [!IMPORTANT]
> Invocar características de pantalla completa de Microsoft Edge en Windows 10 con los argumentos de línea de comandos proporcionados en [Usar características de pantalla completa](#use-kiosk-mode-features).

## <a name="overview"></a>Información general

El modo de pantalla completa de Microsoft Edge ofrece dos experiencias de bloqueo del explorador para que las organizaciones puedan crear, administrar y proporcionar la mejor experiencia para sus clientes. Están disponibles las siguientes experiencias de bloqueo:  

- Experiencia de **señalización digital/interactiva**: Muestra un sitio específico en modo de pantalla completa.
- Experiencia de **exploración pública**: Ejecuta una versión limitada de varias pestañas de Microsoft Edge.

En ambas experiencias se ejecuta una sesión de Microsoft Edge InPrivate, que protege los datos de usuario.

## <a name="set-up-microsoft-edge-kiosk-mode"></a>Configurar la pantalla completa de Microsoft Edge

Hay disponible un conjunto inicial de características de modo de pantalla completa para probar con el Canal estable de Microsoft Edge, versión 87. Puede descargar la versión más reciente de [Microsoft Edge (canal estable oficial).](https://www.microsoft.com/edge)

### <a name="kiosk-mode-supported-features"></a>Características compatibles con el modo de pantalla completa

En la tabla siguiente se enumeran las características compatibles con el modo de pantalla completa en Microsoft Edge y Microsoft Edge Legacy. Use esta tabla como guía para realizar la transición a Microsoft Edge comparando cómo se admiten estas características en ambas versiones de Microsoft Edge.

|Característica|Señalización interactiva\digital|Navegación pública|Disponible con la versión de Microsoft Edge (y versiones posteriores)|Disponible con Microsoft Edge Legacy|
|-|-|-|-|-|
|Navegación de InPrivate|esté|esté|89|esté|
|Restablecer por inactividad|esté|esté|89|Y|
|[Barra de direcciones de solo lectura](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (directiva) |N|esté |89|N|
|[Eliminar descargas al salir](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (directiva)  | esté|esté |89|N|
|F11 bloqueado (entrada y salida en pantalla completa) | esté | esté |89|esté|
|F12 bloqueado (Iniciar Herramientas de desarrollo) | esté | esté |89|Y|
| Soporte con varias pestañas | N| esté|89|Y|
|[Permitir compatibilidad con direcciones URL](./microsoft-edge-policies.md#urlallowlist) (directiva)|esté|esté|89|N|
|[Bloquear compatibilidad con direcciones URL](./microsoft-edge-policies.md#urlblocklist) (directiva)|Y|esté|89|N|
|[Mostrar el botón Inicio](./microsoft-edge-policies.md#showhomebutton) (directiva)|N|esté|89|Y|
|[Administrar favoritos](./microsoft-edge-policies.md#managedfavorites) (directiva)|N|esté|89|Y|
|[Habilitar impresora](./microsoft-edge-policies.md#printingenabled) (directiva)|Y|esté|89|Y|
|[Configurar la nueva dirección URL de la página de pestaña](./microsoft-edge-policies.md#newtabpagelocation) (directiva)|N|esté|89|S|
|Botón Finalizar sesión * | N| esté|89|Y|
|Todas las direcciones URL internas de Microsoft Edge están bloqueadas, excepto *edge://downloads* y *edge://print* |N|esté|89|S|
| CTRL+N bloqueado (abrir una nueva ventana) * | S | esté |89|Y|
| CTRL+T bloqueado (abrir nueva pestaña) |S | N |89|Y|
|La configuración y más (...) mostrará solo las opciones necesarias  |esté |esté |89|esté|
|Restringir el inicio de otras aplicaciones desde el explorador|Y|S|90|S|
|Bloqueo de la configuración de impresión de la interfaz de usuario|Y|S|90|S|
|[Establecer la nueva etiqueta como página de inicio](./microsoft-edge-policies.md#homepageisnewtabpage) (directiva)|N|S|90|S|

> [!NOTE]
> Las características seguidas de "*" solo están habilitadas en un escenario de aplicación única de acceso asignado.

## <a name="use-kiosk-mode-features"></a>Use las características del modo de pantalla completa

Las características del modo de pantalla completa de Microsoft Edge se pueden invocar con las siguientes opciones de línea de comandos de Windows 10 para señalización digital/interactiva y exploración pública.

### <a name="kiosk-mode-digitalinteractive-signage"></a>Señalización digital/interactiva en modo de pantalla completa
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a>Exploración pública en modo de pantalla completa

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="additional-command-line-options"></a>Opciones de la línea de comandos adicionales

- **--no-first-run**: deshabilita la primera experiencia de ejecución de Microsoft Edge.

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- **--kiosk-idle-timeout-minutes=**: cambia el tiempo (en minutos) de la última actividad de usuario antes de que el modo de pantalla completa de Microsoft Edge restablezca la sesión del usuario. Reemplace "valor" en el siguiente ejemplo por la cantidad de minutos.

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   Son admitidos los siguientes "valores":

     - Valores predeterminados (en minutos)
       - Pantalla completa: 0 (desactivado)
       - Exploración pública: 5 min
    - Valores permitidos
      - 0: desactiva el temporizador
      - 1-1440: número de minutos para restablecer el temporizador de inactividad


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## <a name="support-policies-for-kiosk-mode"></a>Directivas de soporte técnico para el modo de pantalla completa

Usa cualquiera de las directivas de Microsoft Edge que se enumeran en la tabla siguiente para mejorar la experiencia de pantalla completa del tipo de pantalla completa de Microsoft Edge que configures. Para más información sobre estas directivas, consulta [Microsoft Edge: referencia de directiva de explorador](./microsoft-edge-policies.md).

> [!NOTE]
> La configuración de directivas no está limitada a las directivas enumeradas en la tabla siguiente, pero se deben probar directivas adicionales para garantizar que la funcionalidad del modo de pantalla completa no se vea afectada negativamente.

|Directiva de grupo|Señalización digital\interactiva|Exploración pública de una sola aplicación|
|--|--|--|
|[Impresión](./microsoft-edge-policies.md#printing-policies) | esté|esté |
|[HomePageLocation](./microsoft-edge-policies.md#homepagelocation) |N | esté|
|[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton) |N | esté|
|[NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) |N |esté |
|[FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled) |N |esté |
|[URLAllowlist](./microsoft-edge-policies.md#urlallowlist) |esté |esté |
|[URLBlocklist](./microsoft-edge-policies.md#urlblocklist) |esté | esté|
|[ManagedSearchEngines](./microsoft-edge-policies.md#managedsearchengines) |N | esté|
|[UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed) |N | esté|
|[VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) | N|esté |
|[Configuración de SmartScreen](./microsoft-edge-policies.md#smartscreen-settings-policies) |esté |Y |
|[EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)|Y|esté|

## <a name="microsoft-edge-with-assigned-access"></a>Microsoft Edge con acceso asignado

### <a name="single-app-kiosk"></a>Pantalla completa de aplicación única

El modo pantalla completa de la versión 90 de Microsoft Edge ofrece una amplia lista de funciones. Consulte la sección de funciones compatibles con el modo Pantalla completa.
Con las siguientes actualizaciones de Windows se puede configurar Microsoft Edge a través de la aplicación única de acceso asignado.

|Sistema operativo|Versión|Actualizaciones|
|--|--|--|
|Windows 10 | 2004 o posterior|[KB4601382 o posterior](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 o posterior](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

Puede administrar el modo pantalla completa de Microsoft Edge asignado a la aplicación única a través de la [Configuración de Windows](/deployedge/microsoft-edge-configure-kiosk-mode#configure-using-windows-settings) y de Intune.

### <a name="multi-app-kiosk"></a>Pantalla completa de varias aplicaciones

Microsoft Edge se puede ejecutar con [acceso asignado a varias aplicaciones](/windows/configuration/lock-down-windows-10-to-specific-apps) en Windows 10, que es el equivalente del tipo de pantalla completa de "Exploración normal" de Microsoft Edge (versión anterior). Para configurar Microsoft Edge con acceso asignado de varias aplicaciones, sigue las instrucciones sobre cómo configurar una [pantalla completa de varias aplicaciones.](/windows/configuration/lock-down-windows-10-to-specific-apps) (El AUMID para el canal estable de Microsoft Edge es **MSEdge**).

### <a name="configure-using-windows-settings"></a>Usar la configuración de Windows

La configuración de Windows es la manera más sencilla de configurar uno o dos dispositivos de quiosco de aplicación única. Usa los siguientes pasos para configurar un equipo de pantalla completa de una sola aplicación.

1. En la siguiente tabla, se listan las actualizaciones mínimas del sistema para los sistemas operativos.

|Sistema operativo|Versión|Actualizaciones|
|--|--|--|
|Windows 10 | 2004 o posterior|[KB4601382 o posterior](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 o posterior](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. Para probar las últimas funciones, puedes descargar el último [Canal estable de Microsoft Edge](https://www.microsoft.com/edge/business/download), versión 89 o superior.

3. En el ordenador de pantalla completa, abra la configuración de Windows y escriba "pantalla completa" en el campo de búsqueda. Selecciona  **Configurar un quiosco (acceso asignado)**, como se muestra en la siguiente captura de pantalla, para abrir el cuadro de diálogo de creación del quiosco.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar el quiosco con el acceso asignado":::

4. En la página **Configurar un quiosco** , haz clic en  **Empezar**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Página de quiosco: introducción":::

5. Escribe un nombre para crear una nueva cuenta de quiosco o elije una cuenta existente de la lista rellenada y haz clic en  **Siguiente**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Modo de pantalla completa: crear cuenta":::

6. En la página **Elegir una aplicación de quiosco** , selecciona **Microsoft** Edge y haz clic en  **Siguiente**.

   > [!NOTE]
   > Esto solo se aplica a Microsoft Edge Dev, Beta y canales estables.

     :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Pantalla completa: inicio de sesión digital en pantalla completa.":::

7. Elija una de las siguientes opciones para la visualización de Microsoft Edge cuando se ejecuta en modo pantalla completa:

   - Señalización de indicación digital/interactiva: muestra un sitio específico en el modo de pantalla completa que ejecuta Microsoft Edge
   - Explorador público: ejecuta una versión multipestaña limitada de Microsoft Edge.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Cómo se usará el modo de pantalla completa: signo digital de pantalla completa":::

8. Seleccione  **Siguiente**.
9. Escribe la dirección URL que quieres cargar cuando se inicie la pantalla completa.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Modo de pantalla completa: escribir URL":::

10. Acepta el valor predeterminado de 5 minutos para el tiempo de inactividad o proporciona un valor.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Modo de pantalla completa: introducir el tiempo de inactividad":::

11. Haz clic en  **Siguiente**.
12. Cierra la ventana  **Configuración**  para guardar y aplicar las opciones.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Modo de pantalla completa: finalizar la configuración":::

13. Cerrar sesión desde el dispositivo de pantalla completa e iniciar sesión con la cuenta de pantalla completa local para validar la configuración.

## <a name="functional-limitations"></a>Limitaciones funcionales

Con el lanzamiento de esta versión de vista previa de la modalidad de pantalla completa, continuamos trabajando para mejorar el producto y agregar nuevas características.

Actualmente no admitimos las siguientes características y le recomendamos que las desactive:

- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [IsolateOrigins](./microsoft-edge-policies.md#isolateorigins)
- [ManagedFavorites](./microsoft-edge-policies.md#managedfavorites)
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled)
- [EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled)
- [InternetExplorerIntegrationLevel](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [Extensiones](./microsoft-edge-policies.md#extensions-policies)
- [BackgroundModeEnabled](./microsoft-edge-policies.md#backgroundmodeenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)

## <a name="see-also"></a>Vea también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Planear su implementación de Microsoft Edge](deploy-edge-plan-deployment.md)
- [Configurar quioscos multimedia y señales digitales en las ediciones de escritorio de Windows](/windows/configuration/kiosk-methods)
- [Planear la transición al modo de pantalla completa](microsoft-edge-kiosk-mode-transition-plan.md)
