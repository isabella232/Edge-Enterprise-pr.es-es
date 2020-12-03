---
title: Configurar Microsoft Edge en macOS con Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar las opciones de directiva de Microsoft Edge en dispositivos Mac con Jamf
ms.openlocfilehash: 1859d9fb1fd3ea8ff6908c41f75df21a8b338769
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194718"
---
# <span data-ttu-id="81f4d-103">Configurar las opciones de directiva de Microsoft Edge en macOS con Jamf</span><span class="sxs-lookup"><span data-stu-id="81f4d-103">Configure Microsoft Edge policy settings on macOS with Jamf</span></span>

<span data-ttu-id="81f4d-104">Este artículo describe cómo configurar las opciones de directiva en macOS con un archivo de manifiesto de directiva de Microsoft Edge en Jamf Pro 10.19.</span><span class="sxs-lookup"><span data-stu-id="81f4d-104">This article describes how to configure policy settings on macOS using a Microsoft Edge policy manifest file on Jamf Pro 10.19.</span></span>

<span data-ttu-id="81f4d-105">También puede configurar las opciones de directiva de Microsoft Edge en macOS mediante un archivo de lista de propiedades (.plist).</span><span class="sxs-lookup"><span data-stu-id="81f4d-105">You can also configure Microsoft Edge policy settings on macOS by using a property list (.plist) file.</span></span> <span data-ttu-id="81f4d-106">Para obtener más información, consulte [configurar para macOS con un archivo .plist](configure-microsoft-edge-on-mac.md)</span><span class="sxs-lookup"><span data-stu-id="81f4d-106">For more information, see [Configure for macOS using a .plist](configure-microsoft-edge-on-mac.md)</span></span>


## <span data-ttu-id="81f4d-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="81f4d-107">Prerequisites</span></span>

<span data-ttu-id="81f4d-108">Se necesita el siguiente software:</span><span class="sxs-lookup"><span data-stu-id="81f4d-108">The following software is required:</span></span>

- <span data-ttu-id="81f4d-109">Canal 81 Microsoft Edge Stable</span><span class="sxs-lookup"><span data-stu-id="81f4d-109">Microsoft Edge Stable channel 81</span></span>
- <span data-ttu-id="81f4d-110">Archivo de plantillas de directiva, versión 81.0.416.3</span><span class="sxs-lookup"><span data-stu-id="81f4d-110">Policy Templates file, version 81.0.416.3</span></span>
- <span data-ttu-id="81f4d-111">Jamf Pro, versión 10.19</span><span class="sxs-lookup"><span data-stu-id="81f4d-111">Jamf Pro, Version 10.19</span></span>

## <span data-ttu-id="81f4d-112">Acerca del menú de configuración personalizada y de la aplicación de Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="81f4d-112">About the Jamf Pro Application & Custom Settings menu</span></span>

<span data-ttu-id="81f4d-113">Antes de Jamf Pro 10,18, administrar Office 365 suponía la creación manual de un archivo .plist.</span><span class="sxs-lookup"><span data-stu-id="81f4d-113">Before Jamf Pro 10.18, managing Office 365 involved manually building a .plist file.</span></span> <span data-ttu-id="81f4d-114">Este era un flujo de trabajo muy largo que requería sólidos conocimientos técnicos.</span><span class="sxs-lookup"><span data-stu-id="81f4d-114">This was a time-consuming workflow that required a strong technical background.</span></span> <span data-ttu-id="81f4d-115">Jamf Pro 10.18 eliminó estos obstáculos al simplificar el proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="81f4d-115">Jamf Pro 10.18 eliminated those barriers by streamlining the configuration process.</span></span> <span data-ttu-id="81f4d-116">Sin embargo, los administradores de TI solo podrían usar esta nueva interfaz de usuario para aplicaciones específicas y dominios de preferencias especificados por Jamf.</span><span class="sxs-lookup"><span data-stu-id="81f4d-116">However, IT Admins could only use this new user interface for specific applications and preference domains specified by Jamf.</span></span>

<span data-ttu-id="81f4d-117">En Jamf Pro 10.19, un usuario puede cargar un manifiesto JSON como "esquema personalizado" para dirigirse a cualquier dominio de preferencias, y la interfaz de usuario gráfica se generará a partir de este manifiesto.</span><span class="sxs-lookup"><span data-stu-id="81f4d-117">In Jamf Pro 10.19, a user can upload a JSON manifest as a "custom schema" to target any preference domain, and the graphical user interface will be generated from this manifest.</span></span> <span data-ttu-id="81f4d-118">El esquema personalizado que se crea sigue la especificación de esquema JSON.</span><span class="sxs-lookup"><span data-stu-id="81f4d-118">The custom schema that's created follows the JSON Schema specification.</span></span>

<span data-ttu-id="81f4d-119">Para obtener más información, vea [perfiles de configuración del equipo](https://jamf.it/computer-configuration-profiles) en la guía del administrador de Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="81f4d-119">For more information, see [Computer Configuration Profiles](https://jamf.it/computer-configuration-profiles) in the Jamf Pro Administrator's Guide.</span></span>

## <span data-ttu-id="81f4d-120">Obtener el manifiesto de directiva para una versión específica de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="81f4d-120">Get the policy manifest for a specific version of Microsoft Edge</span></span>

<span data-ttu-id="81f4d-121">Para obtener el manifiesto de directiva:</span><span class="sxs-lookup"><span data-stu-id="81f4d-121">To get the policy manifest:</span></span>

- <span data-ttu-id="81f4d-122">Diríjase a la [Página de inicio Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="81f4d-122">Go to the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="81f4d-123">En la lista desplegable Canal o versión, seleccione **cualquier canal con la versión 81 o posterior.**_.</span><span class="sxs-lookup"><span data-stu-id="81f4d-123">On the Channel/Version dropdown list, select **any channel with version 81 or later.**_.</span></span>
- <span data-ttu-id="81f4d-124">En la lista desplegable Compilación, seleccione cualquier _*compilación 81 o posterior.*\*_</span><span class="sxs-lookup"><span data-stu-id="81f4d-124">On the Build dropdown list, select any _*81 build or later.*\*_.</span></span>
- <span data-ttu-id="81f4d-125">Haga clic en obtener archivos de directiva para descargar nuestro paquete de plantillas de directivas.</span><span class="sxs-lookup"><span data-stu-id="81f4d-125">Click GET POLICY FILES to download our policy templates bundle.</span></span>

  > [!NOTE]
  > <span data-ttu-id="81f4d-126">Actualmente, el conjunto de plantillas de directiva está firmado como archivo CAB.</span><span class="sxs-lookup"><span data-stu-id="81f4d-126">Currently, the policy templates bundle is signed as a CAB file.</span></span> <span data-ttu-id="81f4d-127">Tendrá que usar una herramienta de terceros, como The Unarchiver para abrir el archivo en macOS.</span><span class="sxs-lookup"><span data-stu-id="81f4d-127">You'll need to use a 3rd party tool, such as The Unarchiver to open the file on macOS.</span></span>

<span data-ttu-id="81f4d-128">Después de desempaquetar el archivo CAB, desempaquete el archivo ZIP y vaya al directorio "mac" de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="81f4d-128">After you unpack the CAB file, unpack the ZIP file and navigate to the "mac" top level directory.</span></span> <span data-ttu-id="81f4d-129">El manifiesto, denominado "policy_manifest.json", se encuentra en este directorio.</span><span class="sxs-lookup"><span data-stu-id="81f4d-129">The manifest, which is named "policy_manifest.json", is in this directory.</span></span>

<span data-ttu-id="81f4d-130">Este manifiesto se publicará en cada paquete de directivas empezando con la compilación 81.0.416.3.</span><span class="sxs-lookup"><span data-stu-id="81f4d-130">This manifest will be published in every policy bundle starting with build 81.0.416.3.</span></span> <span data-ttu-id="81f4d-131">Si desea probar directivas en el canal de desarrollo, puede tomar el manifiesto asociado a cada lanzamiento de desarrollo y probarlo en Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="81f4d-131">If you want to test policies in the Dev channel, you can take the manifest associated with each Dev release and test it in Jamf Pro.</span></span>  

## <span data-ttu-id="81f4d-132">Usar el manifiesto de directiva en Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="81f4d-132">Use the policy manifest in Jamf Pro</span></span>

<span data-ttu-id="81f4d-133">Siga los pasos siguientes para cargar el manifiesto de directiva en Jamf Pro y crear un perfil de directiva para macOS.</span><span class="sxs-lookup"><span data-stu-id="81f4d-133">Use the following steps to upload the policy manifest to Jamf Pro and then create a policy profile for macOS.</span></span>

1. <span data-ttu-id="81f4d-134">Inicie sesión en Jamf.</span><span class="sxs-lookup"><span data-stu-id="81f4d-134">Sign in to Jamf.</span></span>
2. <span data-ttu-id="81f4d-135">Seleccione la pestaña _\*Equipo\*\*.</span><span class="sxs-lookup"><span data-stu-id="81f4d-135">Select the _*Computer*\* tab.</span></span>
3. <span data-ttu-id="81f4d-136">En **administración de contenido**, seleccione **perfiles de configuración**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-136">Under **Content Management**, select **Configuration Profiles**.</span></span>
4. <span data-ttu-id="81f4d-137">En la página **perfiles de configuración**, haga clic en **+ nuevo**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-137">On the **Configuration Profiles** page, click **+ New**.</span></span>

   ![Agregar un perfil nuevo en Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. <span data-ttu-id="81f4d-139">En **Nuevo perfil de configuración de macOS**>**opciones**, seleccione **aplicación y configuración personalizada**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-139">On **New macOS Configuration Profile**>**Options**, select **Application & Custom Settings**.</span></span>
6. <span data-ttu-id="81f4d-140">En la ventana emergente **configuración personalizada y de la aplicación**, haga clic en **configurar**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-140">On the **Application & Custom Settings** popup window, click **Configure**.</span></span>

   ![Configurar la aplicación y la configuración personalizada](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. <span data-ttu-id="81f4d-142">En la sección **aplicación y configuración personalizada**, configure los valores que se muestran en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="81f4d-142">In the **Application & Custom Settings** section, set the values shown in the following screen shot.</span></span>

   ![Origen de perfil y esquema personalizado](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - <span data-ttu-id="81f4d-144">Para **método de creación**, elija **configurar las opciones**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-144">For **Creation Method**, pick **Configure settings**.</span></span>
   - <span data-ttu-id="81f4d-145">Para **origen**, elija **esquema personalizado**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-145">For **Source**, pick **Custom Schema**.</span></span>
   - <span data-ttu-id="81f4d-146">Para **dominio de preferencia**, proporcione el nombre de su dominio.</span><span class="sxs-lookup"><span data-stu-id="81f4d-146">For **Preference Domain**, provide the name of your domain.</span></span> <span data-ttu-id="81f4d-147">Este ejemplo usa *com.microsoft.Edge* como dominio.</span><span class="sxs-lookup"><span data-stu-id="81f4d-147">This example uses *com.microsoft.Edge* as the domain.</span></span>
   - <span data-ttu-id="81f4d-148">Para **esquema personalizado**, pegue el contenido del archivo de manifiesto "policy_manifest.json".</span><span class="sxs-lookup"><span data-stu-id="81f4d-148">For **Custom Schema**, paste the contents of the "policy_manifest.json" manifest file.</span></span>
   - <span data-ttu-id="81f4d-149">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-149">Click **Save**.</span></span>

8. <span data-ttu-id="81f4d-150">Después de guardar el perfil, Jamf muestra la sección **general** que se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="81f4d-150">After you save the profile, Jamf displays the **General** section shown in the next screen shot.</span></span>

   ![Configurar la sección general](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - <span data-ttu-id="81f4d-152">Proporcione un **nombre** para mostrar para el perfil y una **descripción**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-152">Provide a display **Name** for the profile and a **Description**.</span></span>
   - <span data-ttu-id="81f4d-153">Conserve la configuración predeterminada para **categoría**, que es **ninguna**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-153">Keep the default setting for **Category**, which is **None**.</span></span>
   - <span data-ttu-id="81f4d-154">Para **método de distribución**, las opciones son **instalar automáticamente** o **estar disponibles en autoservicio**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-154">For **Distribution Method**, the options are **Install Automatically** or **Make Available in Self Service**.</span></span>
   - <span data-ttu-id="81f4d-155">Para **nivel**, las opciones son **nivel de usuario** o **nivel de equipo**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-155">For **Level**, the options are **User Level** or **Computer Level**.</span></span>
   - <span data-ttu-id="81f4d-156">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-156">Click **Save**.</span></span>

9. <span data-ttu-id="81f4d-157">Después de guardar la sección General, Jamf muestra el perfil de configuración "canal de Microsoft Edge Beta" configurado en nuestro ejemplo.</span><span class="sxs-lookup"><span data-stu-id="81f4d-157">After you save the General section, Jamf shows the "Microsoft Edge Beta Channel" configuration profile set up for our example.</span></span> <span data-ttu-id="81f4d-158">En la siguiente captura de pantalla, tenga en cuenta que puede seguir trabajando con el perfil si hace clic en **editar** o bien, si ya ha terminado, haga clic en **listo**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-158">In the next screen shot, note that you can keep working the profile by clicking **Edit** or if you're finished, click **Done**.</span></span>

   ![Nuevo perfil de configuración con opciones](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > <span data-ttu-id="81f4d-160">Puede editar este perfil después de que se haya guardado y en otra sesión de Jamf.</span><span class="sxs-lookup"><span data-stu-id="81f4d-160">You can edit this profile after it's been saved and in another Jamf session.</span></span> <span data-ttu-id="81f4d-161">Por ejemplo, podría decidir cambiar el método de distribución para que esté disponible en autoservicio.</span><span class="sxs-lookup"><span data-stu-id="81f4d-161">For example, you might decide to change the Distribution Method to Make Available in Self Service.</span></span>

   <span data-ttu-id="81f4d-162">Para hacer una edición de seguimiento en el Microsoft Edge Stable Channel, o para eliminarlo, seleccione el nombre del perfil, que se muestra en la siguiente captura de pantalla de Perfiles de configuración.</span><span class="sxs-lookup"><span data-stu-id="81f4d-162">To do a follow up edit on the Microsoft Edge Stable Channel, or delete it, select the profile name, shown in the following Configuration Profiles screen shot.</span></span>

   ![Lista de perfiles de configuración](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

<span data-ttu-id="81f4d-164">Después de crear el nuevo perfil de configuración aún tiene que configurar el **ámbito** del perfil.</span><span class="sxs-lookup"><span data-stu-id="81f4d-164">After you create the new configuration profile you still have to configure the **Scope** for the profile.</span></span>

### <span data-ttu-id="81f4d-165">Para configurar el ámbito</span><span class="sxs-lookup"><span data-stu-id="81f4d-165">To configure the scope</span></span>

1. <span data-ttu-id="81f4d-166">Para **destinos**, proporcione la siguiente configuración mínima:</span><span class="sxs-lookup"><span data-stu-id="81f4d-166">For **Targets**, provide the following minimum settings:</span></span>

   - <span data-ttu-id="81f4d-167">EQUIPOS DE DESTINO.</span><span class="sxs-lookup"><span data-stu-id="81f4d-167">TARGET COMPUTERS.</span></span> <span data-ttu-id="81f4d-168">Las opciones son equipos específicos o todos los equipos.</span><span class="sxs-lookup"><span data-stu-id="81f4d-168">The options are Specific Computers or All Computers.</span></span>
   - <span data-ttu-id="81f4d-169">USUARIOS DE DESTINO.</span><span class="sxs-lookup"><span data-stu-id="81f4d-169">TARGET USERS.</span></span> <span data-ttu-id="81f4d-170">Las opciones son usuarios específicos o todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="81f4d-170">The options are Specific Users or All Users.</span></span>
   - <span data-ttu-id="81f4d-171">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-171">Click **Save**.</span></span>
2. <span data-ttu-id="81f4d-172">Para **limitaciones**, conserve la configuración predeterminada: ninguna.</span><span class="sxs-lookup"><span data-stu-id="81f4d-172">For **Limitations**, keep the default setting: None.</span></span> <span data-ttu-id="81f4d-173">Haga clic en **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-173">Click **Cancel**.</span></span>
3. <span data-ttu-id="81f4d-174">Para **exclusiones**, conserve la configuración predeterminada: ninguna.</span><span class="sxs-lookup"><span data-stu-id="81f4d-174">For **Exclusions**, keep the default setting: None.</span></span> <span data-ttu-id="81f4d-175">Haga clic en **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="81f4d-175">Click **Cancel**.</span></span>

## <span data-ttu-id="81f4d-176">Consulte también</span><span class="sxs-lookup"><span data-stu-id="81f4d-176">See also</span></span>

- [<span data-ttu-id="81f4d-177">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="81f4d-177">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="81f4d-178">Configurar para macOS con Intune</span><span class="sxs-lookup"><span data-stu-id="81f4d-178">Configure for macOS with Intune</span></span>](configure-microsoft-edge-on-mac.md)
- [<span data-ttu-id="81f4d-179">Configurar para Windows</span><span class="sxs-lookup"><span data-stu-id="81f4d-179">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="81f4d-180">Configurar para Windows con Intune</span><span class="sxs-lookup"><span data-stu-id="81f4d-180">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
