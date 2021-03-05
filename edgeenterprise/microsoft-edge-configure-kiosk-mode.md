---
title: Configurar el modo de pantalla completa en Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 03/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Obtenga información sobre las características del modo de pantalla completa y sobre cómo configurar las opciones del modo de pantalla completa de Microsoft Edge.
ms.openlocfilehash: 9f2ce26f2c505ba3fc9e2e05b057e5d5df8257fe
ms.sourcegitcommit: 8da3a4de1a14514014b6d7b103ba79f2ace48044
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "11388549"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a>Configurar el modo de pantalla completa en Microsoft Edge

En este artículo se describe cómo configurar las opciones de pantalla completa de Microsoft Edge que puedes probar. También hay una guía básica de las características a las que nos dirigiremos.

> [!NOTE]
> Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.

## <a name="overview"></a>Introducción

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
|[Barra de direcciones de solo lectura](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (directiva) |N|esté |89|N|
|[Eliminar descargas al salir](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (directiva)  | esté|esté |89|N|
|F11 bloqueado (entrada y salida en pantalla completa) | esté | esté | 89 |esté|
|F12 bloqueado (Iniciar Herramientas de desarrollo) | esté | esté | 89 |Y|
| Soporte con varias pestañas | N| esté| 89|Y|
|[Permitir compatibilidad con direcciones URL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) (directiva)|esté|esté|89|N|
|[Bloquear compatibilidad con direcciones URL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) (directiva)|Y|esté|89|N|
|[Mostrar el botón Inicio](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showhomebutton) (directiva)|N|esté|89|Y|
|[Administrar favoritos](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedfavorites) (directiva)|N|esté|89|Y|
|[Habilitar impresora](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printingenabled) (directiva)|Y|esté|89|Y|
|[Configurar la nueva dirección URL de la página de pestaña](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation) (directiva)|N|esté||S|
|Botón Finalizar sesión * | N| esté| 89|Y|
|Todas las direcciones URL internas de Microsoft Edge están bloqueadas, excepto *edge://downloads* y *edge://print* |N|esté|89|S|
| CTRL+N bloqueado (abrir una nueva ventana) * | S | esté | 89 |Y|
| CTRL+T bloqueado (abrir nueva pestaña) |S | N | 89 |Y|
|La configuración y más (...) mostrará solo las opciones necesarias  |esté |esté |89 |esté|
|Restringir el inicio de otras aplicaciones desde el explorador|Y|esté|90/91|Y|
|Bloqueo de la configuración de impresión de la interfaz de usuario|Y|esté|90/91|Y|
|[Establecer la página de la nueva pestaña como página principal](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepageisnewtabpage) (directiva)|-|-|TBD|S|

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

Usa cualquiera de las directivas de Microsoft Edge que se enumeran en la tabla siguiente para mejorar la experiencia de pantalla completa del tipo de pantalla completa de Microsoft Edge que configures. Para más información sobre estas directivas, consulta [Microsoft Edge: referencia de directiva de explorador](https://docs.microsoft.com/deployedge/microsoft-edge-policies).

> [!NOTE]
> La configuración de directivas no está limitada a las directivas enumeradas en la tabla siguiente, pero se deben probar directivas adicionales para garantizar que la funcionalidad del modo de pantalla completa no se vea afectada negativamente.

|Directiva de grupo|Señalización digital\interactiva|Exploración pública de una sola aplicación|
|--|--|--|
|[Impresión](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | esté|esté |
|[HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |N | esté|
|[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |N | esté|
|[NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |N |esté |
|[FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |N |esté |
|[URLAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |esté |esté |
|[URLBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |esté | esté|
|[ManagedSearchEngines](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |N | esté|
|[UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |N | esté|
|[VerticalTabsAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | N|esté |
|[Configuración de SmartScreen](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |esté |Y |
|[EdgeCollectionsEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgecollectionsenabled)|Y|esté|

## <a name="microsoft-edge-with-assigned-access"></a>Microsoft Edge con acceso asignado

### <a name="single-app-kiosk"></a>Quiosco multimedia de aplicación única

Microsoft Edge admite actualmente un subconjunto de los mismos tipos de modo de pantalla completa de Microsoft Edge (versión heredada) para el acceso asignado a una sola aplicación con las siguientes experiencias de bloqueo: señalización digital/interactiva y exploración pública.  

El modo de pantalla completa de Microsoft Edge con una sola aplicación de acceso asignado está disponible actualmente para pruebas con la última compilación de [Compilación preliminar de Windows 10 Insider](https://insider.windows.com/) versión 20215 o posterior, y con el [Canal beta de Microsoft Edge,](https://www.microsoftedgeinsider.com/download)versión 89 o posterior.

**¿Cómo puedo obtener la vista previa de Windows Insider?**

Para instalar una versión preliminar de Windows 10 Insider en un PC, sigue las instrucciones que se indican en  [Introducción a las versiones preliminares de Windows 10 Insider](https://docs.microsoft.com/windows-insider/get-started).

### <a name="multi-app-kiosk"></a>Pantalla completa de varias aplicaciones

Microsoft Edge se puede ejecutar con [acceso asignado a varias aplicaciones](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) en Windows 10, que es el equivalente del tipo de pantalla completa de "Exploración normal" de Microsoft Edge (versión anterior). Para configurar Microsoft Edge con acceso asignado de varias aplicaciones, sigue las instrucciones sobre cómo configurar una [pantalla completa de varias aplicaciones.](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) (El AUMID para el canal estable de Microsoft Edge es **MSEdge**).

Al usar Microsoft Edge con acceso asignado de varias aplicaciones, puede configurar la pantalla completa de Microsoft Edge para usar las [directivas de explorador de Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) para configurar la experiencia de exploración para satisfacer sus requisitos únicos.

### <a name="configure-using-windows-settings"></a>Usar la configuración de Windows

La configuración de Windows es la manera más sencilla de configurar uno o dos dispositivos de quiosco de aplicación única. Usa los siguientes pasos para configurar un equipo de quiosco de una sola aplicación.

1. Instala la última versión preliminar de Windows 10 Insider, versiones 20215 o superiores. Sigue las instrucciones que se indican en [Introducción a las compilaciones preliminares de Windows 10 Insider](https://docs.microsoft.com/windows-insider/get-started).
2. Para probar las características más recientes, puede descargar el [canal Microsoft Edge Beta](https://www.microsoftedgeinsider.com/download) más reciente, versión 89 o posterior.
3. En el ordenador quiosco, abra la configuración de Windows y escriba "quiosco" en el campo de búsqueda. Selecciona  **Configurar un quiosco (acceso asignado)**, como se muestra en la siguiente captura de pantalla, para abrir el cuadro de diálogo de creación del quiosco.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar el quiosco con el acceso asignado":::

4. En la página **Configurar un quiosco** , haz clic en  **Empezar**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Página de quiosco: introducción":::

5. Escribe un nombre para crear una nueva cuenta de quiosco o elije una cuenta existente de la lista rellenada y haz clic en  **Siguiente**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Modo de pantalla completa: crear cuenta":::

6. En la página **Elegir una aplicación de quiosco** , selecciona **Microsoft** Edge y haz clic en  **Siguiente**.

   > [!NOTE]
   > Esto solo se aplica a Microsoft Edge Dev, Beta y canales estables.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Modo de pantalla completa: elegir una aplicación":::

7. Elige una de las siguientes opciones para decidir cómo se muestra Microsoft Edge cuando se ejecuta en el modo de pantalla completa:

   - Señalización de indicación digital/interactiva: muestra un sitio específico en el modo de pantalla completa que ejecuta Microsoft Edge
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

13. Cerrar sesión desde el dispositivo de pantalla completa e iniciar sesión con la cuenta de pantalla completa local para validar la configuración.

## <a name="functional-limitations"></a>Limitaciones funcionales

Con el lanzamiento de esta vista previa de la modalidad de pantalla completa, continuamos trabajando para mejorar el producto y agregar nuevas características.

Se recomienda desactivar:

- [InPrivateModeAvailability](https://docs.microsoft.com/deployedge/microsoft-edge-policies#inprivatemodeavailability)
- [IsolateOrigins](https://docs.microsoft.com/deployedge/microsoft-edge-policies#isolateorigins)
- [ManagedFavorites](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedfavorites)
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled)
- [EdgeCollectionsEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgecollectionsenabled)
- [UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed)
- [DefaultPopupsSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultpopupssetting)
- [StartupBoostEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [Extensiones](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [BackgroundModeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## <a name="roadmap"></a>Guía básica

### <a name="in-early-2021"></a>A principios de 2021

Agregaremos las siguientes características y soporte:

- Disponibilidad general del modo de pantalla completa de Microsoft Edge con acceso asignado a una sola aplicación en Windows 10 1909 y versiones posteriores.
- Características adicionales de paridad con Microsoft Edge (versión anterior).
- Integración con Intune para configurar dispositivos con la experiencia de usuario del perfil de modo de pantalla completa.
- Restringir el inicio de otras aplicaciones desde el explorador.
- Bloqueo de la configuración de impresión de la interfaz de usuario.

## <a name="see-also"></a>Vea también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Planear su implementación de Microsoft Edge](deploy-edge-plan-deployment.md)
- [Configurar quioscos multimedia y señales digitales en las ediciones de escritorio de Windows](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Planear la transición al modo de pantalla completa](microsoft-edge-kiosk-mode-transition-plan.md)
