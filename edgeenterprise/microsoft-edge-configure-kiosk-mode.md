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
# <span data-ttu-id="fb861-103">Configurar la pantalla completa en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fb861-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="fb861-104">En este artículo se describe cómo configurar las opciones de pantalla completa de Microsoft Edge que puedes probar.</span><span class="sxs-lookup"><span data-stu-id="fb861-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="fb861-105">También hay una guía básica de las características relevantes.</span><span class="sxs-lookup"><span data-stu-id="fb861-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="fb861-106">Este artículo es aplicable para Microsoft Edge, versión 87 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fb861-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="fb861-107">Introducción</span><span class="sxs-lookup"><span data-stu-id="fb861-107">Overview</span></span>

<span data-ttu-id="fb861-108">El modo de pantalla completa de Microsoft Edge ofrece dos experiencias de bloqueo del explorador para que las organizaciones puedan crear, administrar y proporcionar la mejor experiencia para sus clientes.</span><span class="sxs-lookup"><span data-stu-id="fb861-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="fb861-109">Están disponibles las siguientes experiencias de bloqueo:</span><span class="sxs-lookup"><span data-stu-id="fb861-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="fb861-110">La experiencia de indicación digital/interactiva muestra un sitio específico en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="fb861-110">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="fb861-111">La experiencia de explorador público ejecuta una versión multipestaña limitada de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fb861-111">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="fb861-112">En ambas experiencias se ejecuta una sesión de Microsoft Edge InPrivate, que protege los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="fb861-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="fb861-113">Configurar la pantalla completa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fb861-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="fb861-114">Ya está disponible un conjunto inicial de características de modo de pantalla completa para probar el Canal Microsoft Edge Canary, versión 87.</span><span class="sxs-lookup"><span data-stu-id="fb861-114">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="fb861-115">Puedes descargar Microsoft Edge Canary en la página [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download).</span><span class="sxs-lookup"><span data-stu-id="fb861-115">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="fb861-116">Características del modo de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="fb861-116">Kiosk mode features</span></span>

<span data-ttu-id="fb861-117">Las siguientes características están disponibles:</span><span class="sxs-lookup"><span data-stu-id="fb861-117">The following features are available:</span></span>

- <span data-ttu-id="fb861-118">La navegación de InPrivate protege los datos del usuario eliminando los datos y descargas del explorador cuando termina la sesión.</span><span class="sxs-lookup"><span data-stu-id="fb861-118">InPrivate navigation protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="fb861-119">Una directiva para configurar la eliminación de descargas al dejar la sesión.</span><span class="sxs-lookup"><span data-stu-id="fb861-119">A policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="fb861-120">La opción de restablecer una sesión de usuario después de un determinado período de inactividad.</span><span class="sxs-lookup"><span data-stu-id="fb861-120">The option to reset a user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="fb861-121">Un conjunto inicial de funciones de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="fb861-121">An initial set of lockdown functionality.</span></span> <span data-ttu-id="fb861-122">Están disponibles las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="fb861-122">The following functions are available:</span></span>

  - <span data-ttu-id="fb861-123">Menú contextual del mouse</span><span class="sxs-lookup"><span data-stu-id="fb861-123">Mouse context menu</span></span>
  - <span data-ttu-id="fb861-124">Herramientas de desarrollo con la tecla F12</span><span class="sxs-lookup"><span data-stu-id="fb861-124">F12 Developer Tools</span></span>
  - <span data-ttu-id="fb861-125">Salir de la pantalla completa con la tecla F11 (si estás en el modo de pantalla completa)</span><span class="sxs-lookup"><span data-stu-id="fb861-125">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="fb861-126">Bloqueo del conjunto inicial de páginas *Edge://*</span><span class="sxs-lookup"><span data-stu-id="fb861-126">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="fb861-127">A medida que el modo de pantalla completa evolucione, habrá más características disponibles.</span><span class="sxs-lookup"><span data-stu-id="fb861-127">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="fb861-128">Uso del modo de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="fb861-128">Use kiosk mode features</span></span>

<span data-ttu-id="fb861-129">Puedes invocar el modo de pantalla completa de Microsoft Edge con las siguientes opciones de línea de comandos de Windows 10:</span><span class="sxs-lookup"><span data-stu-id="fb861-129">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="fb861-130">Indicación digital/interactiva de pantalla completa:</span><span class="sxs-lookup"><span data-stu-id="fb861-130">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="fb861-131">Exploración pública de pantalla completa:</span><span class="sxs-lookup"><span data-stu-id="fb861-131">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="fb861-132">Opciones de la línea de comandos adicionales</span><span class="sxs-lookup"><span data-stu-id="fb861-132">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="fb861-133">: deshabilita la primera experiencia de ejecución de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fb861-133">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="fb861-134">: cambia el tiempo en minutos de la última actividad de usuario antes de que el modo de pantalla completa de Microsoft Edge restablezca la sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="fb861-134">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="fb861-135">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="fb861-135">The following values are supported:</span></span>

  - <span data-ttu-id="fb861-136">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="fb861-136">Default values</span></span>
    - <span data-ttu-id="fb861-137">Pantalla completa: desactivado</span><span class="sxs-lookup"><span data-stu-id="fb861-137">Full screen - turned off</span></span>
    - <span data-ttu-id="fb861-138">Navegación pública: 5 min</span><span class="sxs-lookup"><span data-stu-id="fb861-138">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="fb861-139">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="fb861-139">Allowed values</span></span>
    - <span data-ttu-id="fb861-140">0: desactiva el temporizador</span><span class="sxs-lookup"><span data-stu-id="fb861-140">0 - turns off the timer</span></span>
    - <span data-ttu-id="fb861-141">1-1440: número de minutos para restablecer el temporizador de inactividad</span><span class="sxs-lookup"><span data-stu-id="fb861-141">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="fb861-142">Microsoft Edge con acceso asignado</span><span class="sxs-lookup"><span data-stu-id="fb861-142">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="fb861-143">Quiosco multimedia de aplicación única</span><span class="sxs-lookup"><span data-stu-id="fb861-143">Single app kiosk</span></span>

<span data-ttu-id="fb861-144">En la actualidad, Microsoft Edge es compatible con un subconjunto de los mismos tipos de pantalla completa que Microsoft Edge (versión anterior) para el acceso asignado a una sola aplicación con las siguientes experiencias de bloqueo, señalización digital e interactiva y navegación pública.</span><span class="sxs-lookup"><span data-stu-id="fb861-144">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences, Digital/Interactive signage and Public-browsing.</span></span>  

<span data-ttu-id="fb861-145">Actualmente, la pantalla completa de Microsoft Edge con acceso asignado está disponible para probar con la última  [versión preliminar de Windows 10 Insider](https://insider.windows.com/), versión 20215 o superiores, y con el  [Canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), versión 87.0.644.4 o superiores.</span><span class="sxs-lookup"><span data-stu-id="fb861-145">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="fb861-146">¿Cómo puedo obtener la vista previa de Windows Insider?</span><span class="sxs-lookup"><span data-stu-id="fb861-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="fb861-147">Para instalar una versión preliminar de Windows 10 Insider en un PC, sigue las instrucciones que se indican en  [Introducción a las versiones preliminares de Windows 10 Insider](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="fb861-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="fb861-148">Pantalla completa de varias aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fb861-148">Multi-app kiosk</span></span>

<span data-ttu-id="fb861-149">Microsoft Edge se puede ejecutar con [acceso asignado a varias aplicaciones](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) en Windows 10, que es el equivalente del tipo de pantalla completa de "Exploración normal" de Microsoft Edge (versión anterior).</span><span class="sxs-lookup"><span data-stu-id="fb861-149">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="fb861-150">Para configurar Microsoft Edge con acceso asignado a varias aplicaciones, sigue las instrucciones acerca de cómo [Configurar un quiosco multimedia de varias aplicaciones](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span><span class="sxs-lookup"><span data-stu-id="fb861-150">To configure Microsoft Edge with multi-app assigned access follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="fb861-151">(El AUMID para el canal estable de Microsoft Edge es **MSEdge**).</span><span class="sxs-lookup"><span data-stu-id="fb861-151">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="fb861-152">Al configurar la pantalla completa de Microsoft Edge cuando usas Microsoft Edge con acceso asignado de varias aplicaciones, puedes usar las [directivas del explorador Microsoft Edge](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) para configurar la experiencia de exploración de manera que cumpla con tus requisitos únicos.</span><span class="sxs-lookup"><span data-stu-id="fb861-152">Configure Microsoft Edge kiosk mode When using Microsoft Edge with multi-app assigned access you can use the [Microsoft Edge browser policies](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="fb861-153">Usar la configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="fb861-153">Configure using Windows Settings</span></span>

<span data-ttu-id="fb861-154">La configuración de Windows es la manera más sencilla de configurar uno o dos dispositivos de quiosco de aplicación única.</span><span class="sxs-lookup"><span data-stu-id="fb861-154">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="fb861-155">Usa los siguientes pasos para configurar un equipo de quiosco de una sola aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb861-155">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="fb861-156">Instala la última versión preliminar de Windows 10 Insider, versiones 20215 o superiores.</span><span class="sxs-lookup"><span data-stu-id="fb861-156">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="fb861-157">Sigue las instrucciones que se indican en [Introducción a las versiones preliminares de Windows 10](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="fb861-157">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="fb861-158">Instala la última versión del [canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), 87.0.644.4 o superior.</span><span class="sxs-lookup"><span data-stu-id="fb861-158">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644.4 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="fb861-159">Dado que es necesario instalar a nivel de dispositivo, solo se admite un canal que no sea Canary.</span><span class="sxs-lookup"><span data-stu-id="fb861-159">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="fb861-160">En el equipo de quiosco, abre la configuración de Windows y escribe "quiosco" en el campo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fb861-160">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="fb861-161">Selecciona  **Configurar un quiosco (acceso asignado)**, como se muestra en la siguiente captura de pantalla, para abrir el cuadro de diálogo de creación del quiosco.</span><span class="sxs-lookup"><span data-stu-id="fb861-161">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar el quiosco con el acceso asignado":::

4. <span data-ttu-id="fb861-163">En la página **Configurar un quiosco** , haz clic en  **Empezar**.</span><span class="sxs-lookup"><span data-stu-id="fb861-163">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Configurar el quiosco con el acceso asignado":::

5. <span data-ttu-id="fb861-165">Escribe un nombre para crear una nueva cuenta de quiosco o elije una cuenta existente de la lista rellenada y haz clic en  **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="fb861-165">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Configurar el quiosco con el acceso asignado":::

6. <span data-ttu-id="fb861-167">En la página **Elegir una aplicación de quiosco** , selecciona **Microsoft** Edge y haz clic en  **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="fb861-167">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="fb861-168">Esto solo se aplica a Microsoft Edge Dev, Beta y canales estables.</span><span class="sxs-lookup"><span data-stu-id="fb861-168">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Configurar el quiosco con el acceso asignado":::

7. <span data-ttu-id="fb861-170">Elige una de las siguientes opciones para decidir cómo se muestra Microsoft Edge cuando se ejecuta en el modo de pantalla completa:</span><span class="sxs-lookup"><span data-stu-id="fb861-170">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="fb861-171">Señalización de indicación digital/interactiva: muestra un sitio específico en el modo de pantalla completa que ejecuta Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fb861-171">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="fb861-172">Explorador público: ejecuta una versión multipestaña limitada de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fb861-172">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Configurar el quiosco con el acceso asignado":::

8. <span data-ttu-id="fb861-174">Selecciona  **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="fb861-174">Select **Next**.</span></span>
9. <span data-ttu-id="fb861-175">Escribe la dirección URL que quieres cargar cuando se inicie la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="fb861-175">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Configurar el quiosco con el acceso asignado":::

10. <span data-ttu-id="fb861-177">Acepta el valor predeterminado de 5 minutos para el tiempo de inactividad o proporciona un valor.</span><span class="sxs-lookup"><span data-stu-id="fb861-177">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Configurar el quiosco con el acceso asignado":::

11. <span data-ttu-id="fb861-179">Haz clic en  **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="fb861-179">Click **Next**.</span></span>
12. <span data-ttu-id="fb861-180">Cierra la ventana  **Configuración**  para guardar y aplicar las opciones.</span><span class="sxs-lookup"><span data-stu-id="fb861-180">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Configurar el quiosco con el acceso asignado":::

13. <span data-ttu-id="fb861-182">Cierra sesión en el dispositivo de quiosco e inicia sesión con la cuenta de quiosco local para validar la configuración.</span><span class="sxs-lookup"><span data-stu-id="fb861-182">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="fb861-183">Limitaciones funcionales</span><span class="sxs-lookup"><span data-stu-id="fb861-183">Functional limitations</span></span>

<span data-ttu-id="fb861-184">Con el lanzamiento de esta vista previa de la modalidad de pantalla completa, continuamos trabajando para mejorar el producto y agregar nuevas características.</span><span class="sxs-lookup"><span data-stu-id="fb861-184">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="fb861-185">El modo de pantalla completa no es compatible actualmente con las siguientes funciones (estamos trabajando para que lo sea en el futuro):</span><span class="sxs-lookup"><span data-stu-id="fb861-185">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="fb861-186">Colecciones</span><span class="sxs-lookup"><span data-stu-id="fb861-186">Collections</span></span>
- <span data-ttu-id="fb861-187">Extensions</span><span class="sxs-lookup"><span data-stu-id="fb861-187">Extensions</span></span>
- <span data-ttu-id="fb861-188">Modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="fb861-188">Internet Explorer mode</span></span>
- <span data-ttu-id="fb861-189">Protección de aplicaciones de Microsoft Defender (WDAG)</span><span class="sxs-lookup"><span data-stu-id="fb861-189">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="fb861-190">Guía básica</span><span class="sxs-lookup"><span data-stu-id="fb861-190">Roadmap</span></span>

### <span data-ttu-id="fb861-191">A finales de este año (2020)</span><span class="sxs-lookup"><span data-stu-id="fb861-191">Later this year (2020)</span></span>

<span data-ttu-id="fb861-192">Agregaremos las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="fb861-192">We'll add the following features:</span></span>

- <span data-ttu-id="fb861-193">Botón Finalizar sesión</span><span class="sxs-lookup"><span data-stu-id="fb861-193">End session button</span></span>
- <span data-ttu-id="fb861-194">Barra de direcciones de solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb861-194">Read only address bar</span></span>  
  - <span data-ttu-id="fb861-195">Configurable con la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="fb861-195">Configurable with group policy</span></span>
  - <span data-ttu-id="fb861-196">Cuando esté habilitado, los usuarios no podrán editar la barra de direcciones y navegar a otra página.</span><span class="sxs-lookup"><span data-stu-id="fb861-196">When enabled, users will be prevented from editing the address bar and navigating to another page.</span></span>

- <span data-ttu-id="fb861-197">Más funciones de bloqueo:</span><span class="sxs-lookup"><span data-stu-id="fb861-197">More lockdown functions:</span></span>

  - <span data-ttu-id="fb861-198">Se bloquearán aceleradores adicionales (por ejemplo, CTRL + N)</span><span class="sxs-lookup"><span data-stu-id="fb861-198">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="fb861-199">El menú "..."  de configuración solo habilitará las opciones necesarias (por ejemplo, Imprimir, Ayuda, Comentarios y Leer en voz alta).</span><span class="sxs-lookup"><span data-stu-id="fb861-199">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="fb861-200">Bloqueo adicional de páginas *edge://* (por ejemplo, *edge://settings*)</span><span class="sxs-lookup"><span data-stu-id="fb861-200">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="fb861-201">Configurar la interfaz de usuario de opciones de impresión</span><span class="sxs-lookup"><span data-stu-id="fb861-201">Configure print options UI</span></span>
  - <span data-ttu-id="fb861-202">Limitar el explorador de archivos a la carpeta de descargas.</span><span class="sxs-lookup"><span data-stu-id="fb861-202">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="fb861-203">A principios de 2021</span><span class="sxs-lookup"><span data-stu-id="fb861-203">In early 2021</span></span>

<span data-ttu-id="fb861-204">Agregaremos las siguientes características y soporte:</span><span class="sxs-lookup"><span data-stu-id="fb861-204">We'll add the following support and features:</span></span>

- <span data-ttu-id="fb861-205">Disponibilidad general del modo de pantalla completa de Microsoft Edge con el acceso asignado a una sola aplicación en Windows.</span><span class="sxs-lookup"><span data-stu-id="fb861-205">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="fb861-206">Características adicionales de paridad con Microsoft Edge (versión anterior).</span><span class="sxs-lookup"><span data-stu-id="fb861-206">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="fb861-207">Integración con Intune para configurar dispositivos con la experiencia de usuario del perfil de modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="fb861-207">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="fb861-208">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fb861-208">See also</span></span>

- [<span data-ttu-id="fb861-209">Configurar quioscos multimedia y señales digitales en las ediciones de escritorio de Windows</span><span class="sxs-lookup"><span data-stu-id="fb861-209">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="fb861-210">Implementar la pantalla completa de Microsoft Edge (versión heredada)</span><span class="sxs-lookup"><span data-stu-id="fb861-210">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="fb861-211">Planear tu implementación de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fb861-211">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="fb861-212">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="fb861-212">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
