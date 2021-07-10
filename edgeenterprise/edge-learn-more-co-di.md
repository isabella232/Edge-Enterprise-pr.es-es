---
title: ClickOnce y DirectInvoke en Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Aprende sobre ClickOnce y DirectInvoke en Microsoft Edge.
ms.openlocfilehash: 3d124f141e9212ba5ab25d4b725d32add62077a3
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642056"
---
# <a name="understand-the-clickonce-and-directinvoke-features-in-microsoft-edge"></a><span data-ttu-id="738d6-103">Conocer las funciones de ClickOnce y DirectInvoke en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="738d6-103">Understand the ClickOnce and DirectInvoke features in Microsoft Edge</span></span>

<span data-ttu-id="738d6-104">ClickOnce y DirectInvoke son funciones disponibles en IE y Microsoft Edge (versión 45 y versiones anteriores) que admiten el uso de un controlador de archivos para descargar archivos desde un sitio web.</span><span class="sxs-lookup"><span data-stu-id="738d6-104">ClickOnce and DirectInvoke are features available in IE and Microsoft Edge (version 45 and earlier) that support the use of a file handler to download files from a website.</span></span> <span data-ttu-id="738d6-105">Aunque sirven para fines diferentes, ambas funciones permiten que los sitios web especifiquen que un archivo solicitado para descarga se pasa a un controlador de archivos en el dispositivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="738d6-105">Although they serve different purposes, both features let websites specify that a file requested for download is passed to a file handler on the user's device.</span></span> <span data-ttu-id="738d6-106">El controlador de archivos nativo de Windows controla las solicitudes de ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="738d6-106">ClickOnce requests are handled by the native file handler in Windows.</span></span> <span data-ttu-id="738d6-107">Las solicitudes DirectInvoke se controlan mediante un controlador de archivos registrado especificado mediante el sitio web que hospeda el archivo.</span><span class="sxs-lookup"><span data-stu-id="738d6-107">DirectInvoke requests are handled by a registered file handler specified by the website hosting the file.</span></span>

<span data-ttu-id="738d6-108">Para obtener más información sobre estas funciones, consulta:</span><span class="sxs-lookup"><span data-stu-id="738d6-108">For more information about these features, see:</span></span>

- [<span data-ttu-id="738d6-109">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="738d6-109">ClickOnce</span></span>](/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [<span data-ttu-id="738d6-110">DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="738d6-110">DirectInvoke</span></span>]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> <span data-ttu-id="738d6-111">Actualmente, Chromium no proporciona compatibilidad nativa para ClickOnce ni DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="738d6-111">Currently, Chromium doesn't provide native support for ClickOnce or DirectInvoke.</span></span>

## <a name="overview-prerequisites-and-process"></a><span data-ttu-id="738d6-112">Introducción: requisitos previos y proceso</span><span class="sxs-lookup"><span data-stu-id="738d6-112">Overview: prerequisites and process</span></span>

<span data-ttu-id="738d6-113">Para que ClickOnce y DirectInvoke funcionen como se espera y para que el controlador de archivos se solicite correctamente, el controlador de archivos debe estar registrado en el sistema operativo como compatible con ClickOnce o DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="738d6-113">For ClickOnce and DirectInvoke to work as designed and for the file handler to be successfully requested, the file handler must be registered to the operating system as supporting ClickOnce or DirectInvoke.</span></span> <span data-ttu-id="738d6-114">Este registro suele producirse cuando está instalado el sistema operativo original o cuando un programa nuevo que está instalado solicita la capacidad de usar DirectInvoke para actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="738d6-114">This registration typically happens when the original operating system is installed or when a new program that's installed requests the ability to use DirectInvoke for updates.</span></span>

<span data-ttu-id="738d6-115">Cuando un sitio web recibe una solicitud de descarga que requiera ClickOnce o DirectInvoke, tienen lugar las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="738d6-115">When a website receives a download request that requires ClickOnce or DirectInvoke, the following actions happen:</span></span>

- <span data-ttu-id="738d6-116">El sitio web solicita que el explorador use un controlador de archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="738d6-116">The website requests that the browser use a specified file handler.</span></span>
- <span data-ttu-id="738d6-117">El explorador comprueba el Registro del sistema operativo para ver si el controlador de archivos está registrado para el tipo de archivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="738d6-117">The browser checks the operating system registry to see if the file handler is registered for the requested file type.</span></span>
- <span data-ttu-id="738d6-118">Si el controlador de archivos está registrado, el explorador llama al controlador de archivos y pasa la dirección URL como argumento al controlador de archivos.</span><span class="sxs-lookup"><span data-stu-id="738d6-118">If the file handler is registered, the browser calls the file handler and passes the URL as an argument to the file handler.</span></span>
- <span data-ttu-id="738d6-119">El controlador de archivos procesa la dirección URL y descarga el archivo.</span><span class="sxs-lookup"><span data-stu-id="738d6-119">The file handler processes the URL and downloads the file.</span></span>

  > [!NOTE]
  > <span data-ttu-id="738d6-120">La dirección URL se usa para determinar el origen del archivo, así como los parámetros que se deben usar para acceder al archivo.</span><span class="sxs-lookup"><span data-stu-id="738d6-120">The URL is used to determine the source of the file, as well as any parameters to use when accessing the file.</span></span>  <span data-ttu-id="738d6-121">Por ejemplo: puntos de conexión, un manifiesto o metadatos.</span><span class="sxs-lookup"><span data-stu-id="738d6-121">For example: endpoints, a manifest, or metadata.</span></span>

## <a name="use-cases"></a><span data-ttu-id="738d6-122">Casos de uso</span><span class="sxs-lookup"><span data-stu-id="738d6-122">Use cases</span></span>

<span data-ttu-id="738d6-123">Los siguientes casos de uso son representativos.</span><span class="sxs-lookup"><span data-stu-id="738d6-123">The following use cases are representative.</span></span>

<span data-ttu-id="738d6-124">Puedes usar ClickOnce para implementar y actualizar fácilmente software en dispositivos con interacción mínima del usuario.</span><span class="sxs-lookup"><span data-stu-id="738d6-124">You can use ClickOnce to easily deploy and update software on devices with minimal user interaction.</span></span> <span data-ttu-id="738d6-125">Los usuarios pueden instalar y ejecutar una aplicación Windows haciendo clic en un vínculo de una página web.</span><span class="sxs-lookup"><span data-stu-id="738d6-125">Users can install and run a Windows application by clicking a link in a web page.</span></span> <span data-ttu-id="738d6-126">Si se configura correctamente, la aplicación ClickOnce puede instalar programas sin que los usuarios establezcan configuraciones para el instalador.</span><span class="sxs-lookup"><span data-stu-id="738d6-126">If configured correctly, the ClickOnce application can install programs without having users set configurations for the installer.</span></span> <span data-ttu-id="738d6-127">Por ejemplo, las ubicaciones de los archivos, las opciones de instalación, etc.</span><span class="sxs-lookup"><span data-stu-id="738d6-127">For example, file locations, what options to install, and so on.</span></span>

<span data-ttu-id="738d6-128">Los casos de uso de DirectInvoke dependen del propósito del sitio web que solicita DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="738d6-128">DirectInvoke use cases depend on the intent of the website requesting DirectInvoke.</span></span> <span data-ttu-id="738d6-129">Por ejemplo, la función de edición de archivos colaborativa de Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="738d6-129">For example, the collaborative file-editing feature of Microsoft Word.</span></span> <span data-ttu-id="738d6-130">En lugar de hacer clic en un vínculo y descargar toda la copia de un documento en el que estás trabajando con tus colegas, DirectInvoke te permite descargar las partes del documento que se han cambiado.</span><span class="sxs-lookup"><span data-stu-id="738d6-130">Instead of clicking a link and downloading the entire copy of a document you're working on with your colleagues, DirectInvoke lets you download the parts of the document that have been changed.</span></span> <span data-ttu-id="738d6-131">Esta estrategia reduce la cantidad de datos transferidos y puede reducir el tiempo necesario para abrir el documento.</span><span class="sxs-lookup"><span data-stu-id="738d6-131">This strategy reduces the amount of data transferred and can reduce the time needed to open the document.</span></span>  

## <a name="current-support-for-clickonce-and-directinvoke-in-microsoft-edge"></a><span data-ttu-id="738d6-132">Compatibilidad actual de ClickOnce y DirectInvoke en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="738d6-132">Current support for ClickOnce and DirectInvoke in Microsoft Edge</span></span>

<span data-ttu-id="738d6-133">Compatibilidad con ClickOnce y DirectInvoke:</span><span class="sxs-lookup"><span data-stu-id="738d6-133">Support for ClickOnce and DirectInvoke:</span></span>

- <span data-ttu-id="738d6-134">ClickOnce y DirectInvoke son compatibles de forma predeterminada para todos los usuarios de Windows.</span><span class="sxs-lookup"><span data-stu-id="738d6-134">ClickOnce and DirectInvoke are supported out of the box for all Windows users.</span></span>

  > [!NOTE]
  > <span data-ttu-id="738d6-135">Los usuarios que quieran deshabilitar la compatibilidad con ClickOnce pueden ir a *edge://flags/#edge-click-once* y seleccionar **Deshabilitar** en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="738d6-135">Users that want to disable ClickOnce support can go to *edge://flags/#edge-click-once* and select **Disabled** from the dropdown list.</span></span> <span data-ttu-id="738d6-136">Posteriormente tendrás que **Reiniciar** el explorador.</span><span class="sxs-lookup"><span data-stu-id="738d6-136">You'll have to **Restart** the browser.</span></span>

- <span data-ttu-id="738d6-137">ClickOnce y DirectInvoke no son compatibles con ninguna otra plataforma que no sea Windows.</span><span class="sxs-lookup"><span data-stu-id="738d6-137">ClickOnce and DirectInvoke aren't supported on any platforms other than Windows.</span></span>

## <a name="clickonce-and-directinvoke-file-handling-security"></a><span data-ttu-id="738d6-138">Seguridad de administración de archivos de ClickOnce y DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="738d6-138">ClickOnce and DirectInvoke file handling security</span></span>

<span data-ttu-id="738d6-139">ClickOnce y DirectInvoke están protegidos por el servicio de análisis de reputación de direcciones URL de SmartScreen de Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="738d6-139">ClickOnce and DirectInvoke are protected by Microsoft Defender SmartScreen's URL reputation scanning service.</span></span>

<span data-ttu-id="738d6-140">Si el servicio de reputación de direcciones URL de SmartScreen de Microsoft Defender marca una solicitud ClickOnce o DirectInvoke como no segura, los usuarios con ClickOnce o DirectInvoke habilitado verán dos ventanas emergentes.</span><span class="sxs-lookup"><span data-stu-id="738d6-140">If a ClickOnce or a DirectInvoke request is flagged by the Microsoft Defender SmartScreen URL reputation service as unsafe, users with ClickOnce or DirectInvoke enabled will see two popups.</span></span>

<span data-ttu-id="738d6-141">El primer elemento emergente pregunta al usuario si desea abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="738d6-141">The first popup asks the user if they want to open the file.</span></span> <span data-ttu-id="738d6-142">Este elemento emergente se muestra independientemente de si el archivo se marcó como seguro o no seguro.</span><span class="sxs-lookup"><span data-stu-id="738d6-142">This popup is displayed regardless of whether the file was flagged as safe or unsafe.</span></span> <span data-ttu-id="738d6-143">El usuario puede **Informar del archivo como no seguro**, **Cancelar** la solicitud o hacer clic en **Abrir** para continuar.</span><span class="sxs-lookup"><span data-stu-id="738d6-143">The user can **Report the file as unsafe**, **Cancel** the request, or click **Open** to continue.</span></span>

   ![Aviso de abrir archivo](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

<span data-ttu-id="738d6-145">Si el usuario intenta abrir el archivo y el archivo se marcó como no seguro, se muestra un segundo elemento emergente.</span><span class="sxs-lookup"><span data-stu-id="738d6-145">If the user tries to open the file, and the file was flagged as unsafe, a second popup is displayed.</span></span>  <span data-ttu-id="738d6-146">Este elemento emergente advierte al usuario de que el archivo se marcó como no seguro y le pregunta si está seguro de que desea descargar el archivo.</span><span class="sxs-lookup"><span data-stu-id="738d6-146">This popup warns the user that the file was flagged as unsafe, and asks them if they're sure they want to download the file.</span></span>

<span data-ttu-id="738d6-147">El segundo elemento emergente solo aparece si:</span><span class="sxs-lookup"><span data-stu-id="738d6-147">The second popup only shows up if:</span></span>

- <span data-ttu-id="738d6-148">el archivo es un archivo ClickOnce o DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="738d6-148">the file is a ClickOnce or DirectInvoke file</span></span>
- <span data-ttu-id="738d6-149">ClickOnce o DirectInvoke están habilitados</span><span class="sxs-lookup"><span data-stu-id="738d6-149">ClickOnce or DirectInvoke are enabled</span></span>
- <span data-ttu-id="738d6-150">el archivo está marcado como no seguro</span><span class="sxs-lookup"><span data-stu-id="738d6-150">the file is flagged as unsafe</span></span>

 ![Aviso de abrir un archivo no seguro](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> <span data-ttu-id="738d6-152">Si se deshabilitan ClickOnce o DirectInvoke, los archivos solicitados se tratan como descargas normales y, si están marcados como no seguros, se registrarán como no seguros.</span><span class="sxs-lookup"><span data-stu-id="738d6-152">If ClickOnce or DirectInvoke are disabled, requested files are treated as regular downloads and if flagged as unsafe, will be marked as unsafe.</span></span> <span data-ttu-id="738d6-153">Esto es coherente con el tratamiento de otras descargas no seguras.</span><span class="sxs-lookup"><span data-stu-id="738d6-153">This is consistent with the treatment of other unsafe downloads.</span></span>

## <a name="clickonce-and-directinvoke-policies"></a><span data-ttu-id="738d6-154">Directivas ClickOnce y DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="738d6-154">ClickOnce and DirectInvoke policies</span></span>

<span data-ttu-id="738d6-155">Hay dos directivas de grupo que puedes usar para habilitar o deshabilitar ClickOnce y DirectInvoke para los usuarios de empresa.</span><span class="sxs-lookup"><span data-stu-id="738d6-155">There are two group policies that you can use to enable or disable ClickOnce and DirectInvoke for enterprise users.</span></span> <span data-ttu-id="738d6-156">Estas dos directivas son [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled) y [DirectInvokeEnabled](./microsoft-edge-policies.md#directinvokeenabled).</span><span class="sxs-lookup"><span data-stu-id="738d6-156">These two policies are [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled) and [DirectInvokeEnabled](./microsoft-edge-policies.md#directinvokeenabled).</span></span> <span data-ttu-id="738d6-157">Estas dos directivas se etiquetan en el Editor de directivas de grupo como "Permitir que los usuarios abran archivos mediante el protocolo ClickOnce" y "Permitir que los usuarios abran archivos mediante el protocolo DirectInvoke", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="738d6-157">These two policies are labeled in the Group Policy Editor as "Allow users to open files using the ClickOnce protocol" and "Allow users to open files using the DirectInvoke protocol" respectively.</span></span>

## <a name="clickonce-and-directinvoke-behavior"></a><span data-ttu-id="738d6-158">Comportamiento ClickOnce y DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="738d6-158">ClickOnce and DirectInvoke behavior</span></span>

<span data-ttu-id="738d6-159">En los siguientes ejemplos se muestra el control de archivos cuando se habilitan o deshabilitan ClickOnce y DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="738d6-159">The following examples show file handling when ClickOnce and DirectInvoke are enabled or disabled.</span></span>

### <a name="clickonce-enabled"></a><span data-ttu-id="738d6-160">ClickOnce habilitado</span><span class="sxs-lookup"><span data-stu-id="738d6-160">ClickOnce enabled</span></span>

1. <span data-ttu-id="738d6-161">Un usuario abre un vínculo a una página que solicita soporte de ClickOnce y recibe el aviso de la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="738d6-161">A user opens a link to a page that requests ClickOnce support and gets the prompt in the next screenshot.</span></span>

   ![Aviso de abrir un archivo no seguro](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. <span data-ttu-id="738d6-163">Después de que el usuario haga clic en **Abrir**, ClickOnce intenta iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="738d6-163">After the user clicks **Open**, ClickOnce attempts to launch the application.</span></span>

   ![ClickOnce intenta iniciar la aplicación](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. <span data-ttu-id="738d6-165">Cuando el usuario hace clic en **Abrir**, el explorador muestra un elemento emergente que pregunta al usuario si está seguro de que desea instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="738d6-165">After the user clicks **Open**, the browser shows a popup that asks the user if they're sure they want to install the application.</span></span>

   ![Aviso de abrir el archivo](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > <span data-ttu-id="738d6-167">La interfaz, los mensajes y las opciones mostradas mediante el controlador de archivos de ClickOnce variará según el tipo y la configuración del archivo al que se accede.</span><span class="sxs-lookup"><span data-stu-id="738d6-167">The interface, messaging, and options shown by the ClickOnce file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <a name="clickonce-disabled"></a><span data-ttu-id="738d6-168">ClickOnce deshabilitado</span><span class="sxs-lookup"><span data-stu-id="738d6-168">ClickOnce disabled</span></span>

1. <span data-ttu-id="738d6-169">Cuando un usuario abre un vínculo a una página que solicita compatibilidad con ClickOnce, verá un mensaje en la bandeja de descarga similar al que se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="738d6-169">When a user opens a link to a page that requests ClickOnce support, they will see a message in the download tray that is similar to the one in the next screenshot.</span></span>

   ![Aviso de descarga de archivo](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### <a name="directinvoke-enabled"></a><span data-ttu-id="738d6-171">DirectInvoke habilitado</span><span class="sxs-lookup"><span data-stu-id="738d6-171">DirectInvoke enabled</span></span>

1. <span data-ttu-id="738d6-172">Un usuario abre un vínculo a una página que solicita soporte de DirectInvoke y recibe el aviso de la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="738d6-172">A user opens a link to a page that requests DirectInvoke support and gets the prompt in the next screenshot.</span></span>

   ![Aviso de abrir archivo](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. <span data-ttu-id="738d6-174">Cuando el usuario hace clic en **Abrir**, se abrirá el controlador de archivos solicitado.</span><span class="sxs-lookup"><span data-stu-id="738d6-174">When the user clicks **Open**, the requested file handler is opened.</span></span> <span data-ttu-id="738d6-175">En este ejemplo, se usa Microsoft Word para abrir el documento que se muestra en la captura de pantalla anterior.</span><span class="sxs-lookup"><span data-stu-id="738d6-175">In this example, Microsoft Word is used to open the document that's shown in the previous screenshot.</span></span>

   > [!NOTE]
   > <span data-ttu-id="738d6-176">La interfaz, los mensajes y las opciones mostradas mediante el controlador de archivos de DirectInvoke variará según el tipo y la configuración del archivo al que se accede.</span><span class="sxs-lookup"><span data-stu-id="738d6-176">The interface, messaging, and options shown by the DirectInvoke file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <a name="directinvoke-disabled"></a><span data-ttu-id="738d6-177">DirectInvoke deshabilitado</span><span class="sxs-lookup"><span data-stu-id="738d6-177">DirectInvoke disabled</span></span>

1. <span data-ttu-id="738d6-178">Cuando un usuario abre un vínculo a una página que solicita soporte de DirectInvoke, DirectInvoke se comporta del mismo modo que cuando se deshabilita ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="738d6-178">When a user opens a link to a page that requests DirectInvoke support, DirectInvoke behaves the same as when ClickOnce is disabled.</span></span> <span data-ttu-id="738d6-179">Aparecerá un mensaje en la bandeja de descargas similar al que se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="738d6-179">They will see a message in the download tray that's similar to the one in the next screenshot.</span></span>

   ![Aviso de abrir archivo](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## <a name="see-also"></a><span data-ttu-id="738d6-181">Consulta también</span><span class="sxs-lookup"><span data-stu-id="738d6-181">See also</span></span>

- [<span data-ttu-id="738d6-182">Seguridad e implementación de ClickOnce</span><span class="sxs-lookup"><span data-stu-id="738d6-182">ClickOnce security and deployment</span></span>](/visualstudio/deployment/clickonce-security-and-deployment)
- [<span data-ttu-id="738d6-183">DirectInvoke en Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="738d6-183">DirectInvoke in Internet Explorer</span></span>](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/jj215788(v=vs.85))
- [<span data-ttu-id="738d6-184">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="738d6-184">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)