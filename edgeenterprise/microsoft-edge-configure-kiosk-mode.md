---
title: Configurar la pantalla completa en Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 09/24/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar la pantalla completa en Microsoft Edge
ms.openlocfilehash: 17852cc7c7e4921a0fbef7d09a3f1c3d3cccf49f
ms.sourcegitcommit: b1285b7745eb41b241d706b401f8ce78fa33b227
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2020
ms.locfileid: "11078670"
---
# <span data-ttu-id="f5899-103">Configurar la pantalla completa en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f5899-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="f5899-104">En este artículo se describe cómo configurar las opciones de pantalla completa de Microsoft Edge que puedes probar.</span><span class="sxs-lookup"><span data-stu-id="f5899-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="f5899-105">También hay una guía básica de las características relevantes.</span><span class="sxs-lookup"><span data-stu-id="f5899-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="f5899-106">Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f5899-106">This article applies to Microsoft Edge version 87 or later.</span></span>

<span data-ttu-id="f5899-107">Para obtener información sobre la pantalla completa de Microsoft Edge (versión heredada) (versión 45 y anteriores), consulta [Implementar pantalla completa de Microsoft Edge](https://aka.ms/edgekioskmode).</span><span class="sxs-lookup"><span data-stu-id="f5899-107">For information about Microsoft Edge Legacy kiosk mode (version 45 and earlier) see [Deploy Microsoft Edge kiosk mode](https://aka.ms/edgekioskmode).</span></span>

## <span data-ttu-id="f5899-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="f5899-108">Overview</span></span>

<span data-ttu-id="f5899-109">El modo de pantalla completa de Microsoft Edge ofrece dos experiencias de bloqueo del explorador para que las organizaciones puedan crear, administrar y proporcionar la mejor experiencia para sus clientes.</span><span class="sxs-lookup"><span data-stu-id="f5899-109">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="f5899-110">Están disponibles las siguientes experiencias de bloqueo:</span><span class="sxs-lookup"><span data-stu-id="f5899-110">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="f5899-111">La experiencia de indicación digital/interactiva muestra un sitio específico en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="f5899-111">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="f5899-112">La experiencia de explorador público ejecuta una versión multipestaña limitada de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f5899-112">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="f5899-113">En ambas experiencias se ejecuta una sesión de Microsoft Edge InPrivate, que protege los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="f5899-113">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="f5899-114">Configurar la pantalla completa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f5899-114">Set up Microsoft Edge kiosk mode</span></span>  

<span data-ttu-id="f5899-115">Ya está disponible un conjunto inicial de características de modo de pantalla completa para probar el Canal Microsoft Edge Canary, versión 87.</span><span class="sxs-lookup"><span data-stu-id="f5899-115">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="f5899-116">Puedes descargar Microsoft Edge Canary en la página [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download).</span><span class="sxs-lookup"><span data-stu-id="f5899-116">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="f5899-117">Características del modo de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="f5899-117">Kiosk mode features</span></span>

<span data-ttu-id="f5899-118">Las siguientes características están disponibles:</span><span class="sxs-lookup"><span data-stu-id="f5899-118">The following features are available:</span></span>

- <span data-ttu-id="f5899-119">Exploración InPrivate.</span><span class="sxs-lookup"><span data-stu-id="f5899-119">InPrivate navigation.</span></span> <span data-ttu-id="f5899-120">Protege los datos del usuario eliminando los datos y descargas del explorador cuando termina la sesión.</span><span class="sxs-lookup"><span data-stu-id="f5899-120">Protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="f5899-121">Directiva para configurar la eliminación de descargas al dejar la sesión.</span><span class="sxs-lookup"><span data-stu-id="f5899-121">Policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="f5899-122">Restablecer la sesión del usuario después de un período de inactividad determinado.</span><span class="sxs-lookup"><span data-stu-id="f5899-122">Reset user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="f5899-123">Conjunto inicial de funciones de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="f5899-123">Initial set of lockdown functionality.</span></span> <span data-ttu-id="f5899-124">Están disponibles las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5899-124">The following functions are available:</span></span>

  - <span data-ttu-id="f5899-125">Menú contextual del mouse</span><span class="sxs-lookup"><span data-stu-id="f5899-125">Mouse context menu</span></span>
  - <span data-ttu-id="f5899-126">Herramientas de desarrollo con la tecla F12</span><span class="sxs-lookup"><span data-stu-id="f5899-126">F12 Developer Tools</span></span>
  - <span data-ttu-id="f5899-127">Salir de la pantalla completa con la tecla F11 (si estás en el modo de pantalla completa)</span><span class="sxs-lookup"><span data-stu-id="f5899-127">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="f5899-128">Bloqueo del conjunto inicial de páginas *Edge://*</span><span class="sxs-lookup"><span data-stu-id="f5899-128">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="f5899-129">A medida que el modo de pantalla completa evolucione, habrá más características disponibles.</span><span class="sxs-lookup"><span data-stu-id="f5899-129">As kiosk mode evolves, more features will be available.</span></span>

### <span data-ttu-id="f5899-130">Uso del modo de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="f5899-130">Use kiosk mode features</span></span>

<span data-ttu-id="f5899-131">Puedes invocar el modo de pantalla completa de Microsoft Edge con las siguientes opciones de línea de comandos de Windows 10:</span><span class="sxs-lookup"><span data-stu-id="f5899-131">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="f5899-132">Indicación digital/interactiva de pantalla completa:</span><span class="sxs-lookup"><span data-stu-id="f5899-132">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="f5899-133">Exploración pública de pantalla completa:</span><span class="sxs-lookup"><span data-stu-id="f5899-133">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

#### <span data-ttu-id="f5899-134">Opciones de la línea de comandos adicionales</span><span class="sxs-lookup"><span data-stu-id="f5899-134">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="f5899-135">: deshabilita la primera experiencia de ejecución de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f5899-135">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="f5899-136">: cambia el tiempo en minutos de la última actividad de usuario antes de que el modo de pantalla completa de Microsoft Edge restablezca la sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="f5899-136">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="f5899-137">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5899-137">The following values are supported:</span></span>

  - <span data-ttu-id="f5899-138">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="f5899-138">Default values</span></span>
    - <span data-ttu-id="f5899-139">Pantalla completa: desactivado</span><span class="sxs-lookup"><span data-stu-id="f5899-139">Full screen - turned off</span></span>
    - <span data-ttu-id="f5899-140">Navegación pública: 5 min</span><span class="sxs-lookup"><span data-stu-id="f5899-140">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="f5899-141">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="f5899-141">Allowed values</span></span>
    - <span data-ttu-id="f5899-142">0: desactiva el temporizador</span><span class="sxs-lookup"><span data-stu-id="f5899-142">0 - turns off the timer</span></span>
    - <span data-ttu-id="f5899-143">1-1440: número de minutos para restablecer el temporizador de inactividad</span><span class="sxs-lookup"><span data-stu-id="f5899-143">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="f5899-144">Configurar el modo de pantalla completa con el acceso asignado</span><span class="sxs-lookup"><span data-stu-id="f5899-144">Set up kiosk mode with assigned access</span></span>

<span data-ttu-id="f5899-145">Actualmente, la pantalla completa de Microsoft Edge con acceso asignado se puede probar con la última [versión preliminar de Windows 10 Insider](https://insider.windows.com/), versiones 20215 o superiores, y con el [Canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), versiones 87.0.644.4 o superiores.</span><span class="sxs-lookup"><span data-stu-id="f5899-145">Microsoft Edge kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4  or higher.</span></span>

**<span data-ttu-id="f5899-146">¿Cómo puedo obtener la vista previa de Windows Insider?</span><span class="sxs-lookup"><span data-stu-id="f5899-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="f5899-147">Para instalar una versión preliminar de Windows 10 en un PC, sigue las instrucciones que se indican en [Introducción a las versiones preliminares de Windows 10](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="f5899-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="f5899-148">Usar la configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="f5899-148">Configure using Windows Settings</span></span>

<span data-ttu-id="f5899-149">La configuración de Windows es la manera más sencilla de configurar uno o dos dispositivos de quiosco de aplicación única.</span><span class="sxs-lookup"><span data-stu-id="f5899-149">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="f5899-150">Usa los siguientes pasos para configurar un equipo de quiosco de una sola aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5899-150">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="f5899-151">Instala la última versión preliminar de Windows 10 Insider, versiones 20215 o superiores.</span><span class="sxs-lookup"><span data-stu-id="f5899-151">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="f5899-152">Sigue las instrucciones que se indican en [Introducción a las versiones preliminares de Windows 10](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="f5899-152">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="f5899-153">Instala la última versión del [canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), 87.0.644.4 o superior.</span><span class="sxs-lookup"><span data-stu-id="f5899-153">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644.4 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="f5899-154">Dado que es necesario instalar a nivel de dispositivo, solo se admite un canal que no sea Canary.</span><span class="sxs-lookup"><span data-stu-id="f5899-154">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="f5899-155">En el equipo de quiosco, abre la configuración de Windows y escribe "quiosco" en el campo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f5899-155">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="f5899-156">Selecciona  **Configurar un quiosco (acceso asignado)**, como se muestra en la siguiente captura de pantalla, para abrir el cuadro de diálogo de creación del quiosco.</span><span class="sxs-lookup"><span data-stu-id="f5899-156">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar el quiosco con el acceso asignado":::

4. <span data-ttu-id="f5899-158">En la página **Configurar un quiosco** , haz clic en  **Empezar**.</span><span class="sxs-lookup"><span data-stu-id="f5899-158">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Configurar el quiosco con el acceso asignado":::

5. <span data-ttu-id="f5899-160">Escribe un nombre para crear una nueva cuenta de quiosco o elije una cuenta existente de la lista rellenada y haz clic en  **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f5899-160">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Configurar el quiosco con el acceso asignado":::

6. <span data-ttu-id="f5899-162">En la página **Elegir una aplicación de quiosco** , selecciona **Microsoft** Edge y haz clic en  **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f5899-162">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f5899-163">Esto solo se aplica a Microsoft Edge Dev, Beta y canales estables.</span><span class="sxs-lookup"><span data-stu-id="f5899-163">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Configurar el quiosco con el acceso asignado":::

7. <span data-ttu-id="f5899-165">Elige una de las siguientes opciones para decidir cómo se muestra Microsoft Edge cuando se ejecuta en el modo de pantalla completa:</span><span class="sxs-lookup"><span data-stu-id="f5899-165">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="f5899-166">Señalización de indicación digital/interactiva: muestra un sitio específico en el modo de pantalla completa que ejecuta Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f5899-166">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="f5899-167">Explorador público: ejecuta una versión multipestaña limitada de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f5899-167">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Configurar el quiosco con el acceso asignado":::

8. <span data-ttu-id="f5899-169">Selecciona  **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f5899-169">Select **Next**.</span></span>
9. <span data-ttu-id="f5899-170">Escribe la dirección URL que quieres cargar cuando se inicie la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="f5899-170">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Configurar el quiosco con el acceso asignado":::

10. <span data-ttu-id="f5899-172">Acepta el valor predeterminado de 5 minutos para el tiempo de inactividad o proporciona un valor.</span><span class="sxs-lookup"><span data-stu-id="f5899-172">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Configurar el quiosco con el acceso asignado":::

11. <span data-ttu-id="f5899-174">Haz clic en  **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f5899-174">Click **Next**.</span></span>
12. <span data-ttu-id="f5899-175">Cierra la ventana  **Configuración**  para guardar y aplicar las opciones.</span><span class="sxs-lookup"><span data-stu-id="f5899-175">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Configurar el quiosco con el acceso asignado":::

13. <span data-ttu-id="f5899-177">Cierra sesión en el dispositivo de quiosco e inicia sesión con la cuenta de quiosco local para validar la configuración.</span><span class="sxs-lookup"><span data-stu-id="f5899-177">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="f5899-178">Limitaciones funcionales</span><span class="sxs-lookup"><span data-stu-id="f5899-178">Functional limitations</span></span>

<span data-ttu-id="f5899-179">Con el lanzamiento de esta vista previa de la modalidad de pantalla completa, continuamos trabajando para mejorar el producto y agregar nuevas características.</span><span class="sxs-lookup"><span data-stu-id="f5899-179">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="f5899-180">El modo de pantalla completa no es compatible actualmente con las siguientes funciones (estamos trabajando para que lo sea en el futuro):</span><span class="sxs-lookup"><span data-stu-id="f5899-180">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="f5899-181">Colecciones</span><span class="sxs-lookup"><span data-stu-id="f5899-181">Collections</span></span>
- <span data-ttu-id="f5899-182">Extensions</span><span class="sxs-lookup"><span data-stu-id="f5899-182">Extensions</span></span>
- <span data-ttu-id="f5899-183">Modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f5899-183">Internet Explorer mode</span></span>
- <span data-ttu-id="f5899-184">Protección de aplicaciones de Microsoft Defender (WDAG)</span><span class="sxs-lookup"><span data-stu-id="f5899-184">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="f5899-185">Guía básica</span><span class="sxs-lookup"><span data-stu-id="f5899-185">Roadmap</span></span>

### <span data-ttu-id="f5899-186">A finales de este año (2020)</span><span class="sxs-lookup"><span data-stu-id="f5899-186">Later this year (2020)</span></span>

<span data-ttu-id="f5899-187">Agregaremos las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="f5899-187">We'll add the following features:</span></span>

- <span data-ttu-id="f5899-188">Botón Finalizar sesión</span><span class="sxs-lookup"><span data-stu-id="f5899-188">End session button</span></span>
- <span data-ttu-id="f5899-189">Barra de direcciones URL de solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5899-189">Read only URL address bar</span></span>  
  - <span data-ttu-id="f5899-190">Configurable con la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="f5899-190">Configurable with group policy</span></span>
  - <span data-ttu-id="f5899-191">Cuando se habilite, los usuarios no podrán editar la dirección URL de la barra de direcciones para intentar ir a otra página.</span><span class="sxs-lookup"><span data-stu-id="f5899-191">When enabled, users will be prevented from editing the address bar URL to try navigating away to another page.</span></span>

- <span data-ttu-id="f5899-192">Más funciones de bloqueo:</span><span class="sxs-lookup"><span data-stu-id="f5899-192">More lockdown functions:</span></span>

  - <span data-ttu-id="f5899-193">Se bloquearán aceleradores adicionales (por ejemplo, CTRL + N)</span><span class="sxs-lookup"><span data-stu-id="f5899-193">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="f5899-194">El menú "..."  de configuración solo habilitará las opciones necesarias (por ejemplo, Imprimir, Ayuda, Comentarios y Leer en voz alta).</span><span class="sxs-lookup"><span data-stu-id="f5899-194">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="f5899-195">Bloqueo adicional de páginas *edge://* (por ejemplo, *edge://settings*)</span><span class="sxs-lookup"><span data-stu-id="f5899-195">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="f5899-196">Configurar la interfaz de usuario de opciones de impresión</span><span class="sxs-lookup"><span data-stu-id="f5899-196">Configure print options UI</span></span>
  - <span data-ttu-id="f5899-197">Limitar el explorador de archivos a la carpeta de descargas.</span><span class="sxs-lookup"><span data-stu-id="f5899-197">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="f5899-198">A principios de 2021</span><span class="sxs-lookup"><span data-stu-id="f5899-198">In early 2021</span></span>

<span data-ttu-id="f5899-199">Agregaremos las siguientes características y soporte:</span><span class="sxs-lookup"><span data-stu-id="f5899-199">We'll add the following support and features:</span></span>

- <span data-ttu-id="f5899-200">Disponibilidad general del modo de pantalla completa de Microsoft Edge con el acceso asignado a una sola aplicación en Windows.</span><span class="sxs-lookup"><span data-stu-id="f5899-200">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="f5899-201">Características adicionales de paridad con Microsoft Edge (versión anterior).</span><span class="sxs-lookup"><span data-stu-id="f5899-201">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="f5899-202">Integración con Intune para configurar dispositivos con la experiencia de usuario del perfil de modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="f5899-202">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="f5899-203">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f5899-203">See also</span></span>

- [<span data-ttu-id="f5899-204">Configurar quioscos multimedia y señales digitales en las ediciones de escritorio de Windows</span><span class="sxs-lookup"><span data-stu-id="f5899-204">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="f5899-205">Implementar la pantalla completa de Microsoft Edge (versión heredada)</span><span class="sxs-lookup"><span data-stu-id="f5899-205">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="f5899-206">Planear tu implementación de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f5899-206">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="f5899-207">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f5899-207">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)