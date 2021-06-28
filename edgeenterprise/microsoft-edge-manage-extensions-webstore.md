---
title: Extensiones de Microsoft Edge de prueba interna
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 04/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Obtenga información sobre cómo empaquetar y probar internamente extensiones de Microsoft Edge en la empresa.
ms.openlocfilehash: 403b6879b15c146f40fa2564da76eae59b2abe88
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618274"
---
# <a name="self-host-microsoft-edge-extensions"></a><span data-ttu-id="83559-103">Extensiones de Microsoft Edge de prueba interna</span><span class="sxs-lookup"><span data-stu-id="83559-103">Self-host Microsoft Edge extensions</span></span>

<span data-ttu-id="83559-104">En este artículo se proporcionan instrucciones básicas para empaquetar una extensión para hospedarla en su propia tienda web.</span><span class="sxs-lookup"><span data-stu-id="83559-104">This article provides basic guidance for packaging an extension to host on your own webstore.</span></span> <span data-ttu-id="83559-105">También incluye instrucciones sobre cómo implementar extensiones en dispositivos y usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="83559-105">It also includes instructions on how to deploy extensions to devices and users in your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="83559-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="83559-106">Prerequisites</span></span>

<span data-ttu-id="83559-107">Para probar internamente sus propias extensiones, deberá proporcionar sus propios servicios de hospedaje web para las extensiones y sus archivos de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="83559-107">To self-host your own extensions, you will need to provide your own web hosting services for the extensions and their manifest files.</span></span>

 <span data-ttu-id="83559-108">En los pasos siguientes se presupone que ya ha creado la extensión, tiene cierta experiencia con archivos XML, tiene conocimientos prácticos sobre la configuración de la directiva de grupo y sabe cómo usar el Registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="83559-108">The following steps assume that you’ve already created your extension, have some experience with XML files, have a working knowledge of configuring group policy, and know how to use the Windows registry.</span></span>

## <a name="publish-an-extension"></a><span data-ttu-id="83559-109">Publicación de una extensión</span><span class="sxs-lookup"><span data-stu-id="83559-109">Publish an extension</span></span>

<span data-ttu-id="83559-110">Antes de publicar una extensión, debe empaquetarse en un archivo CRX (extensión de Chrome).</span><span class="sxs-lookup"><span data-stu-id="83559-110">Before you publish an extension it needs to be packed into a CRX (Chrome extension) file.</span></span> <span data-ttu-id="83559-111">Siga estos pasos como guía para empaquetar una extensión como un archivo CRX.</span><span class="sxs-lookup"><span data-stu-id="83559-111">Use the following steps as a guide to packing an extension as a CRX file.</span></span>

1. <span data-ttu-id="83559-112">En la barra de direcciones de Microsoft Edge, vaya a *edge://extensions* y active **Modo de desarrollador** si aún no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="83559-112">In the Microsoft Edge address bar, go to *edge://extensions* and turn on **Developer mode** if it’s not already enabled.</span></span>
2. <span data-ttu-id="83559-113">En **Extensiones instaladas**, haga clic en **Extensión del paquete** para crear el archivo CRX.</span><span class="sxs-lookup"><span data-stu-id="83559-113">Under **Installed extensions**, click **Pack Extension** to create the CRX file.</span></span>
3. <span data-ttu-id="83559-114">Use el cuadro de diálogo **Extensión del paquete** para buscar el directorio que tiene el origen de la extensión.</span><span class="sxs-lookup"><span data-stu-id="83559-114">Use the **Pack extension** dialog to find the directory that has the source for the extension.</span></span> <span data-ttu-id="83559-115">Seleccione el directorio y haga clic en **Extensión del paquete**.</span><span class="sxs-lookup"><span data-stu-id="83559-115">Select the directory and then click **Pack extension**.</span></span>  <span data-ttu-id="83559-116">Esto creará el archivo CRX, junto con un archivo PEM.</span><span class="sxs-lookup"><span data-stu-id="83559-116">This will create your CRX file, along with a PEM file.</span></span> <span data-ttu-id="83559-117">Guarde el archivo PEM, ya que es necesario para realizar actualizaciones de versión en la extensión.</span><span class="sxs-lookup"><span data-stu-id="83559-117">Save the PEM file because it’s needed for making version updates to the extension.</span></span> <span data-ttu-id="83559-118">En la captura de pantalla siguiente se muestra el cuadro de diálogo **Extensión del paquete** para buscar el directorio raíz de la extensión.</span><span class="sxs-lookup"><span data-stu-id="83559-118">The next screenshot shows the **Pack extension** dialog for locating the root directory of the extension.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="Cuadro de diálogo Extensión del paquete para buscar el código fuente de una extensión.":::

   > [!IMPORTANT]
   > <span data-ttu-id="83559-120">Almacene el archivo PEM en una ubicación segura, ya que es la clave de la extensión y es necesaria para futuras actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="83559-120">Store the PEM file in a safe location because it’s the key for the extension and it’s needed for future updates.</span></span>

4. <span data-ttu-id="83559-121">Arrastre el archivo CRX a la ventana de extensiones y asegúrese de que se carga.</span><span class="sxs-lookup"><span data-stu-id="83559-121">Drag the CRX file into your extensions window and make sure that it loads.</span></span>
5. <span data-ttu-id="83559-122">Pruebe la extensión y anote el campo de Id. (es decir, el Id. de CRX) y el número de versión.</span><span class="sxs-lookup"><span data-stu-id="83559-122">Test the extension and take note of the ID field (this is the CRX ID) and version number.</span></span> <span data-ttu-id="83559-123">Necesitará esta información más adelante.</span><span class="sxs-lookup"><span data-stu-id="83559-123">You’ll need this information later.</span></span> <span data-ttu-id="83559-124">En la captura de pantalla siguiente se muestra una extensión de prueba con su identificador de CRX.</span><span class="sxs-lookup"><span data-stu-id="83559-124">The next screenshot shows a test extension with its CRX ID.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="Ejemplo de extensión que muestra el Id. de CRX":::

6. <span data-ttu-id="83559-126">Cargue el archivo CRX en el host y anote la dirección URL de la ubicación desde la que se descargará.</span><span class="sxs-lookup"><span data-stu-id="83559-126">Upload the the CRX file to the host and note the URL of the location it will be downloaded from.</span></span> <span data-ttu-id="83559-127">Esta información es necesaria para el archivo de manifiesto XML.</span><span class="sxs-lookup"><span data-stu-id="83559-127">This information is needed for the XML manifest file.</span></span>
7. <span data-ttu-id="83559-128">Para crear un archivo XML de manifiesto con el identificador de aplicación o extensión, la dirección URL de descarga y la versión, defina los campos siguientes:</span><span class="sxs-lookup"><span data-stu-id="83559-128">To create a manifest XML file with the app/extension ID, download URL, and version, define the following fields:</span></span>  

   - <span data-ttu-id="83559-129">**appid**: el identificador de extensión del paso 5</span><span class="sxs-lookup"><span data-stu-id="83559-129">**appid** - The extension ID from step 5</span></span>
   - <span data-ttu-id="83559-130">**codebase**: la ubicación de descarga del archivo CRX del paso 6</span><span class="sxs-lookup"><span data-stu-id="83559-130">**codebase** - The download location for the CRX file from step 6</span></span>
   - <span data-ttu-id="83559-131">**version**: la versión de la aplicación o extensión, que debe coincidir con la versión especificada en el manifiesto de la extensión.</span><span class="sxs-lookup"><span data-stu-id="83559-131">**version** - The version of the app/extension, which should match the version specified in the manifest of the extension.</span></span>

   <span data-ttu-id="83559-132">El siguiente fragmento de código muestra un ejemplo de un archivo de manifiesto XML.</span><span class="sxs-lookup"><span data-stu-id="83559-132">The next code snippet shows an example of an XML manifest file.</span></span>

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   <span data-ttu-id="83559-133">Para más información, vea [Actualizar extensiones automáticamente en Microsoft Edge: desarrollo de Microsoft Edge](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span><span class="sxs-lookup"><span data-stu-id="83559-133">For more information, see [Auto-update extensions in Microsoft Edge - Microsoft Edge Development](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span></span>

8. <span data-ttu-id="83559-134">Cargue el archivo XML completado en una ubicación desde la que se pueda descargar y anote la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="83559-134">Upload the completed XML file to a location where it can be downloaded from, noting the URL.</span></span> <span data-ttu-id="83559-135">Esta dirección URL será necesaria cuando instale la extensión mediante una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="83559-135">This URL will be needed when you install the extension using a group policy.</span></span> <span data-ttu-id="83559-136">Vea [Distribuir una extensión hospedada de forma privada](#distribute-a-privately-hosted-extension).</span><span class="sxs-lookup"><span data-stu-id="83559-136">See [Distribute a privately hosted extension](#distribute-a-privately-hosted-extension).</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="83559-137">La ubicación de hospedaje de la extensión no necesita autenticación.</span><span class="sxs-lookup"><span data-stu-id="83559-137">The hosting location for the extension doesn’t need authentication.</span></span> <span data-ttu-id="83559-138">Los dispositivos de usuario deben tener acceso a ella dondequiera que se puedan usar.</span><span class="sxs-lookup"><span data-stu-id="83559-138">It needs to be accessible by user devices wherever they might be used.</span></span>

## <a name="publish-updates-to-an-extension"></a><span data-ttu-id="83559-139">Publicación de actualizaciones en una extensión</span><span class="sxs-lookup"><span data-stu-id="83559-139">Publish updates to an extension</span></span>

<span data-ttu-id="83559-140">Después de cambiar y probar la extensión actualizada, puede publicarla.</span><span class="sxs-lookup"><span data-stu-id="83559-140">After you change and test the updated extension you can publish it.</span></span> <span data-ttu-id="83559-141">Siga estos pasos como guía para publicar una actualización.</span><span class="sxs-lookup"><span data-stu-id="83559-141">Use the following steps as a guide for publishing an update.</span></span>

1. <span data-ttu-id="83559-142">Cambie el número de versión en el archivo manifest.JSON de la extensión a un número mayor mediante la sintaxis siguiente: `"version":"versionString"`.</span><span class="sxs-lookup"><span data-stu-id="83559-142">Change the version number in your extension's manifest.JSON file to a higher number using the following syntax: `"version":"versionString"`.</span></span> <span data-ttu-id="83559-143">Si "version":"1.0", puede actualizar a "version":"1.1" o a cualquier número superior a "1.0".</span><span class="sxs-lookup"><span data-stu-id="83559-143">If the "version":"1.0", then you can update to "version":"1.1" or any number higher than "1.0".</span></span>
2. <span data-ttu-id="83559-144">Actualice la "versión" de `<updatecheck>` en el archivo XML para que coincida con el número que colocó en el archivo de manifiesto en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="83559-144">Update the "version" of `<updatecheck>` in the XML file to match the number that you put in the manifest file in the previous step.</span></span> <span data-ttu-id="83559-145">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="83559-145">For example:</span></span><br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. <span data-ttu-id="83559-146">Cree un archivo CRX que incluya los nuevos cambios.</span><span class="sxs-lookup"><span data-stu-id="83559-146">Create a CRX file that includes the new changes.</span></span> <span data-ttu-id="83559-147">Vaya a *edge://extensions* y habilite **Modo de desarrollador**.</span><span class="sxs-lookup"><span data-stu-id="83559-147">Go to *edge://extensions* and enable **Developer mode**.</span></span>
4. <span data-ttu-id="83559-148">Haga clic en **Extensión del paquete** y vaya al directorio del origen de la extensión.</span><span class="sxs-lookup"><span data-stu-id="83559-148">Click **Pack extension** and go to the directory for the extension source.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="83559-149">Use el mismo archivo PEM que se generó y guardó la primera vez que se creó el archivo CRX.</span><span class="sxs-lookup"><span data-stu-id="83559-149">Use the same PEM file that was generated and saved the first time the CRX file was created.</span></span> <span data-ttu-id="83559-150">Si no usa el mismo archivo PEM, el identificador de aplicación de la extensión cambiará y la actualización se tratará como una nueva extensión.</span><span class="sxs-lookup"><span data-stu-id="83559-150">If you don't use the same PEM file the app ID of the extension will change and the update will be treated as a new extension.</span></span>

5. <span data-ttu-id="83559-151">Arrastre y coloque el archivo CRX en la ventana de extensiones y compruebe que se carga.</span><span class="sxs-lookup"><span data-stu-id="83559-151">Drag and drop the CRX file into the extensions window and verify that it loads.</span></span>
6. <span data-ttu-id="83559-152">Pruebe la extensión actualizada.</span><span class="sxs-lookup"><span data-stu-id="83559-152">Test the updated extension.</span></span>
7. <span data-ttu-id="83559-153">Reemplace el archivo CRX antiguo y el archivo XML por los nuevos archivos de la extensión actualizada.</span><span class="sxs-lookup"><span data-stu-id="83559-153">Replace the old CRX file and XML file with the new files for the updated extension.</span></span>

<span data-ttu-id="83559-154">Los cambios de la extensión se tomarán durante el siguiente ciclo de sincronización de directivas.</span><span class="sxs-lookup"><span data-stu-id="83559-154">The extension's changes will be picked up during the next policy sync cycle.</span></span> <span data-ttu-id="83559-155">Para más información acerca de la actualización de extensiones, vea: [Actualizar URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) y [Actualizar manifiesto](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span><span class="sxs-lookup"><span data-stu-id="83559-155">For more information about updating extensions, see: [Update URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) and [Update manifest](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span></span>

## <a name="distribute-a-privately-hosted-extension"></a><span data-ttu-id="83559-156">Distribución de una extensión hospedada de forma privada</span><span class="sxs-lookup"><span data-stu-id="83559-156">Distribute a privately hosted extension</span></span>

<span data-ttu-id="83559-157">Puede compartir el vínculo de la ubicación donde se hospeda el archivo CRX y, en cuanto los usuarios escriban la dirección URL en su explorador, la extensión se descargará e instalará.</span><span class="sxs-lookup"><span data-stu-id="83559-157">You can share the link of the location where the CRX file is hosted, and as soon as users enter the URL in their browser the extension will be downloaded and installed.</span></span> <span data-ttu-id="83559-158">Los usuarios pueden habilitar la extensión desde la página edge://extensions.</span><span class="sxs-lookup"><span data-stu-id="83559-158">Users can enable the extension from the edge://extensions page.</span></span> <span data-ttu-id="83559-159">Para permitir que los usuarios instalen extensiones de prueba interna, debe agregar los identificadores de CRX de extensión a la directiva [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist).</span><span class="sxs-lookup"><span data-stu-id="83559-159">To allow users to install self-hosted extensions, you need to add the extension CRX IDs to the [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist) policy.</span></span>

<span data-ttu-id="83559-160">Como alternativa, puede usar la directiva de grupo [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) para forzar la instalación de una extensión en los dispositivos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="83559-160">Alternatively, you can use group policy [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) to Force-install an extension on your users’ devices.</span></span>

<span data-ttu-id="83559-161">Puede aplicar estas directivas a los usuarios seleccionados, dispositivos o ambos.</span><span class="sxs-lookup"><span data-stu-id="83559-161">You can apply these policies to your selected users, devices, or both.</span></span> <span data-ttu-id="83559-162">Recuerde que las actualizaciones de directivas no son instantáneas y la configuración de directiva tardará tiempo en surtir efecto.</span><span class="sxs-lookup"><span data-stu-id="83559-162">Remember though that policy updates are not instantaneous, and it will take time for the policy settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="83559-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="83559-163">See also</span></span>

- [<span data-ttu-id="83559-164">Administrar extensiones de Microsoft Edge en la empresa</span><span class="sxs-lookup"><span data-stu-id="83559-164">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="83559-165">Usar directivas de grupo para administrar extensiones de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="83559-165">Use group policies to manage Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-policies.md)
- [<span data-ttu-id="83559-166">Guía detallada de la directiva ExtensionSettings</span><span class="sxs-lookup"><span data-stu-id="83559-166">Detailed guide to the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="83559-167">Preguntas más frecuentes sobre extensiones de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="83559-167">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="83559-168">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="83559-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
