---
title: Configurar la directiva de Microsoft Edge para Windows con Microsoft Intune
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/18/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar la directiva de Microsoft Edge para Windows con Microsoft Intune.
ms.openlocfilehash: 0189a3fc2f9dc115563e7cf6dca1df960680bf22
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447564"
---
# <a name="configure-microsoft-edge-policy-settings-with-microsoft-intune"></a><span data-ttu-id="3765f-103">Configurar la directiva de Microsoft Edge con Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="3765f-103">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>

<span data-ttu-id="3765f-104">Este artículo explica cómo configurar la directiva de Microsoft Edge para Windows 10 con Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="3765f-104">This article explains how to configure Microsoft Edge policy settings for Windows 10 using Microsoft Intune.</span></span>

> [!NOTE]
> <span data-ttu-id="3765f-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="3765f-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="3765f-106">Puedes configurar las directivas y opciones de Microsoft Edge agregando un perfil de configuración de dispositivo a Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="3765f-106">You can configure Microsoft Edge policies and settings by adding a device configuration profile to Microsoft Intune.</span></span> <span data-ttu-id="3765f-107">El uso de Intune para administrar y aplicar directivas es esencialmente equivalente al uso de la directiva de grupo de Active Directory o a la configuración de Objeto de directiva de grupo (GPO) local en los dispositivos de usuario.</span><span class="sxs-lookup"><span data-stu-id="3765f-107">Using Intune to manage and enforce policies is equivalent to using Active Directory Group Policy or configuring local Group Policy Object (GPO) settings on user devices.</span></span>

<span data-ttu-id="3765f-108">Para obtener más información acerca de la administración de directivas de Microsoft Edge con Microsoft Intune, puedes leer [Administrar el acceso a la Web usando Microsoft Edge con Microsoft Intune](/intune/manage-microsoft-edge), pero ten en cuenta que el artículo vinculado es específico de las versiones 45 y anteriores de Microsoft Edge, por lo que puede contener información y referencias que no se aplican a las versiones 77 y posteriores de Microsoft Edge Enterprise.</span><span class="sxs-lookup"><span data-stu-id="3765f-108">For more information about managing Microsoft Edge policies with Microsoft Intune, you can read [Manage web access by using Microsoft Edge with Microsoft Intune](/intune/manage-microsoft-edge), but keep in mind that the linked article is specific to Microsoft Edge version 45 and earlier and therefore may contain information and references that don't apply to Microsoft Edge Enterprise version 77 and later.</span></span>

> [!TIP]
> <span data-ttu-id="3765f-109">Para obtener información sobre cómo configurar Microsoft Edge en macOS con Microsoft Intune, consulte [Configurar para macOS](configure-microsoft-edge-on-mac.md).</span><span class="sxs-lookup"><span data-stu-id="3765f-109">For information on how to configure Microsoft Edge on macOS using Microsoft Intune, see [Configure for macOS](configure-microsoft-edge-on-mac.md).</span></span>

## <a name="create-a-profile-to-manage-settings-in-microsoft-edge-for-windows-10"></a><span data-ttu-id="3765f-110">Crear un perfil para administrar la configuración de Microsoft Edge para Windows 10</span><span class="sxs-lookup"><span data-stu-id="3765f-110">Create a profile to manage settings in Microsoft Edge for Windows 10</span></span>

<span data-ttu-id="3765f-111">Con las plantillas administrativas de Microsoft Intune, puedes administrar directivas de grupo de Microsoft Edge en los dispositivos con Windows 10 mediante la nube.</span><span class="sxs-lookup"><span data-stu-id="3765f-111">Using Administrative Templates in Microsoft Intune, you can manage Microsoft Edge group policies on your Windows 10 devices using the cloud.</span></span> <span data-ttu-id="3765f-112">Esta sección te ayudará a crear una plantilla para configurar opciones de aplicaciones específicas para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3765f-112">This section will help you create a template to configure Microsoft Edge-specific application settings.</span></span> <span data-ttu-id="3765f-113">Al crear la plantilla, se crea un perfil de configuración de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3765f-113">When you create the template, it creates a device configuration profile.</span></span> <span data-ttu-id="3765f-114">A continuación, puedes asignar o implementar este perfil en los dispositivos con Windows 10 de la organización.</span><span class="sxs-lookup"><span data-stu-id="3765f-114">You can then assign or deploy this profile to Windows 10 devices in your organization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3765f-115">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3765f-115">Prerequisites</span></span>

- <span data-ttu-id="3765f-116">Windows 10 con los siguientes requisitos mínimos del sistema:</span><span class="sxs-lookup"><span data-stu-id="3765f-116">Windows 10 with the following minimum system requirements:</span></span>
  - <span data-ttu-id="3765f-117">Windows 10 versión 1909</span><span class="sxs-lookup"><span data-stu-id="3765f-117">Windows 10, version 1909</span></span>
  - <span data-ttu-id="3765f-118">Windows 10, versión 1903 con [KB4512941](https://support.microsoft.com/kb/4512941) instalada</span><span class="sxs-lookup"><span data-stu-id="3765f-118">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/kb/4512941) installed</span></span>
  - <span data-ttu-id="3765f-119">Windows 10, versión 1809 con [KB4512534](https://support.microsoft.com/kb/4512534) instalada</span><span class="sxs-lookup"><span data-stu-id="3765f-119">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/kb/4512534) installed</span></span>
  - <span data-ttu-id="3765f-120">Windows 10, versión 1803 con [KB4512509](https://support.microsoft.com/kb/4512509) instalada</span><span class="sxs-lookup"><span data-stu-id="3765f-120">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/kb/4512509) installed</span></span>
  - <span data-ttu-id="3765f-121">Windows 10, versión 1709 con [KB4516071](https://support.microsoft.com/kb/4516071) instalada</span><span class="sxs-lookup"><span data-stu-id="3765f-121">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/kb/4516071) installed</span></span>

### <a name="use-administrative-templates-to-create-a-policy-for-microsoft-edge"></a><span data-ttu-id="3765f-122">Use plantillas administrativas para crear una directiva para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3765f-122">Use Administrative Templates to create a policy for Microsoft Edge</span></span>

<span data-ttu-id="3765f-123">Este procedimiento aprovecha las plantillas administrativas (que es posible que esté familiarizado con la Directiva de grupo) que están integradas en Intune.</span><span class="sxs-lookup"><span data-stu-id="3765f-123">This procedure leverages Administrative templates (which you might be familiar with from Group Policy) that are built into Intune.</span></span> <span data-ttu-id="3765f-124">Para crear una directiva para Microsoft Edge, puede usar estas plantillas seleccionando configuración en una lista preconfigurada.</span><span class="sxs-lookup"><span data-stu-id="3765f-124">You can use these templates to create a policy for Microsoft Edge by selecting settings from a pre-configured list.</span></span>

1. <span data-ttu-id="3765f-125">Inicie sesión en el portal [Microsoft Endpoint Manager](https://endpoint.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="3765f-125">Sign in to the [Microsoft Endpoint Manager](https://endpoint.microsoft.com/) portal.</span></span>
2. <span data-ttu-id="3765f-126">Seleccione **Dispositivos** en el panel de navegación de la parte izquierda.</span><span class="sxs-lookup"><span data-stu-id="3765f-126">Select **Devices** in the left-hand navigation pane.</span></span>
3. <span data-ttu-id="3765f-127">Desde **dispositivos** | **Información general**, seleccione **Perfiles de configuración** (en el encabezado Directiva).</span><span class="sxs-lookup"><span data-stu-id="3765f-127">From **Devices** | **Overview**, select **Configuration Profiles** (under Policy heading).</span></span>
4. <span data-ttu-id="3765f-128">En la barra de comandos superior, selecciona **Crear perfil**.</span><span class="sxs-lookup"><span data-stu-id="3765f-128">On the top command bar, select **Create profile**.</span></span>
5. <span data-ttu-id="3765f-129">En la lista desplegable que se muestra debajo de **Plataforma**, seleccione **Windows 10 y luego**.</span><span class="sxs-lookup"><span data-stu-id="3765f-129">In the drop-down list below **Platform**, select **Windows 10 and later**.</span></span>
6. <span data-ttu-id="3765f-130">En la lista desplegable que se muestra debajo de **Perfil**, seleccione **Plantillas administrativas** y, a continuación, haga clic en el botón**crear**.</span><span class="sxs-lookup"><span data-stu-id="3765f-130">In the drop-down list below **Profile**, select **Administrative Templates** and then click the **Create** button.</span></span> <span data-ttu-id="3765f-131">La siguiente captura de pantalla muestra las listas desplegables para seleccionar la plataforma y el tipo de perfil.</span><span class="sxs-lookup"><span data-stu-id="3765f-131">The next screenshot shows the drop-down lists to select the platform and type of profile.</span></span>

    ![Seleccionar plataforma y tipo de perfil](./media/configure-edge-with-intune/create-profile-platform.png)

7. <span data-ttu-id="3765f-133">En la pestaña **Datos básicos**, escriba un **nombre** descriptivo, como la directiva de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3765f-133">On the **Basics** tab, enter a descriptive **Name**, such as Microsoft Edge Policy.</span></span> <span data-ttu-id="3765f-134">Opcionalmente, escriba una **Descripción** de la directiva.</span><span class="sxs-lookup"><span data-stu-id="3765f-134">Optionally, enter a  **Description** for the policy.</span></span>
<span data-ttu-id="3765f-135">La siguiente captura de pantalla muestra el formulario para la pestaña **Datos básicos** y la barra de menús muestra los pasos siguientes (como pestañas atenuadas) para crear el perfil.</span><span class="sxs-lookup"><span data-stu-id="3765f-135">The next screenshot shows the form for the **Basics** tab and the menu bar shows the next steps (as grayed out tabs) to create the profile.</span></span>

   ![Escriba el nombre y la descripción](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. <span data-ttu-id="3765f-137">Selecciona **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3765f-137">Select **Next**.</span></span>
9. <span data-ttu-id="3765f-138">En la pestaña **Opciones de configuración**, seleccione la carpeta Microsoft Edge en una de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="3765f-138">On the **Configuration settings** tab, select the Microsoft Edge folder in one of the following locations:</span></span>

   - <span data-ttu-id="3765f-139">debajo de la carpeta configuración del equipo</span><span class="sxs-lookup"><span data-stu-id="3765f-139">below the Computer Configuration folder</span></span>
   - <span data-ttu-id="3765f-140">debajo de la carpeta configuración del usuario</span><span class="sxs-lookup"><span data-stu-id="3765f-140">below the User Configuration folder.</span></span>

   <span data-ttu-id="3765f-141">La configuración disponible para Microsoft Edge se mostrará en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="3765f-141">The available settings for Microsoft Edge will be shown on the right pane.</span></span> <span data-ttu-id="3765f-142">Por ejemplo, en la siguiente captura de pantalla, puede ver *Configuración de equipo/Microsoft Edge/Permitir restricciones de descarga*.</span><span class="sxs-lookup"><span data-stu-id="3765f-142">For example, *Computer Configuration/Microsoft Edge/Allow download restrictions* shown in the following screenshot.</span></span>

   ![Pestaña de opciones de configuración](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > <span data-ttu-id="3765f-144">Para obtener la lista de todas las opciones disponibles de Microsoft Edge, vea [Microsoft Edge: directivas](./microsoft-edge-policies.md) y [Microsoft Edge: directivas de actualización](./microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="3765f-144">See [Microsoft Edge – Policies](./microsoft-edge-policies.md) and [Microsoft Edge – Update policies](./microsoft-edge-update-policies.md) for the most complete and up to date list of all the available settings for Microsoft Edge.</span></span>

10. <span data-ttu-id="3765f-145">Use el campo de búsqueda ("buscar para filtrar elementos...") para buscar una configuración específica que desee configurar.</span><span class="sxs-lookup"><span data-stu-id="3765f-145">Use the search field ("Search to filter items ...") to find a specific setting you want to configure.</span></span> <span data-ttu-id="3765f-146">En este ejemplo, la cadena de búsqueda es "Página principal".</span><span class="sxs-lookup"><span data-stu-id="3765f-146">In this example, the search string is "home page".</span></span> <span data-ttu-id="3765f-147">La siguiente captura de pantalla muestra los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3765f-147">The next screenshot shows the search results.</span></span>

    ![Resultados de la búsqueda](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. <span data-ttu-id="3765f-149">Cuando encuentre la configuración que desea configurar, selecciónela para mostrar los valores que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="3765f-149">After you find the setting you intend to configure, select it to expose the values you can set.</span></span> <span data-ttu-id="3765f-150">En la siguiente captura de pantalla, selecciono "configurar la dirección URL de la página principal" como ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3765f-150">In the next screenshot, we selected "Configure the home page URL" as an example.</span></span>

    ![Configurar la dirección URL de la página principal](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. <span data-ttu-id="3765f-152">Habilite la directiva y escriba un valor para la dirección URL de la página principal, como se muestra en la captura de pantalla anterior.</span><span class="sxs-lookup"><span data-stu-id="3765f-152">Enable the policy and enter a value for the Home page URL, as shown in the previous screenshot.</span></span>

13. <span data-ttu-id="3765f-153">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3765f-153">Click **OK**.</span></span> <span data-ttu-id="3765f-154">La columna de configuración "Estado" debería aparecer como "Activado", como se muestra en el siguiente ejemplo de captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="3765f-154">The settings "State" column should appear as "Enabled", as shown in the following screenshot example.</span></span>

    ![El estado de configuración está habilitado](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. <span data-ttu-id="3765f-156">Haga clic en el botón **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3765f-156">Click the **Next** button.</span></span>

15. <span data-ttu-id="3765f-157">En la pestaña **Etiquetas de ámbito**, agregue una etiqueta de ámbito si lo desea. en caso contrario, haga clic en el botón **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3765f-157">On the **Scope tags** tab, add a Scope tag if wanted, otherwise click the **Next** button.</span></span>

16. <span data-ttu-id="3765f-158">En la pestaña **Tareas**, haga clic en **+ seleccionar grupos para incluir** asignar esta directiva al grupo de Azure Active Directory (Azure AD) que contiene los dispositivos o los usuarios que quiere que reciban esta configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="3765f-158">On the **Assignments** tab, click **+ Select groups to include** to assign this policy to the Azure Active Directory (Azure AD) group that contains the devices or the users that you want to receive this policy setting.</span></span> <span data-ttu-id="3765f-159">Vea [Asignar perfiles de usuario y dispositivo en Microsoft Intune](/intune/device-profile-assign) para obtener información sobre cómo asignar el perfil a los grupos de usuarios o dispositivos de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3765f-159">See [Assign user and device profiles in Microsoft Intune](/intune/device-profile-assign) for information about how to assign the profile to your Azure AD user or device groups.</span></span>

    ![Seleccionar grupos para incluir](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. <span data-ttu-id="3765f-161">Haga clic en el botón **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3765f-161">Click the **Next** button.</span></span>

18. <span data-ttu-id="3765f-162">En la pestaña **Revisar + crear**, revise el resumen de los cambios para asegurarse de que es correcto y, a continuación, haga clic en el botón **Crear**.</span><span class="sxs-lookup"><span data-stu-id="3765f-162">On the **Review + create** tab, review the summary of your changes to ensure it's correct and then click the **Create** button.</span></span>

19. <span data-ttu-id="3765f-163">La directiva recién creada (directiva de Microsoft Edge) se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="3765f-163">The newly created policy (Microsoft Edge Policy) is shown in the following screenshot.</span></span>

    ![Seleccionar grupos para incluir](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

<span data-ttu-id="3765f-165">Para obtener más información acerca de los perfiles de Windows 10, consulta [Uso de plantillas de Windows 10 para configurar la directiva de grupo en Microsoft Intune](/intune/administrative-templates-windows).</span><span class="sxs-lookup"><span data-stu-id="3765f-165">For more information about Windows 10 profiles, see [Use Windows 10 templates to configure group policy settings in Microsoft Intune](/intune/administrative-templates-windows).</span></span>

## <a name="see-also"></a><span data-ttu-id="3765f-166">Consulta también</span><span class="sxs-lookup"><span data-stu-id="3765f-166">See also</span></span>

- [<span data-ttu-id="3765f-167">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="3765f-167">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="3765f-168">Administrar el acceso a la Web usando Microsoft Edge con Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="3765f-168">Manage web access by using Microsoft Edge with Microsoft Intune</span></span>](/intune/manage-microsoft-edge)
- [<span data-ttu-id="3765f-169">Usa plantillas de Windows 10 para configurar las opciones de la directiva de grupo en Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="3765f-169">Use Windows 10 templates to configure group policy settings in Microsoft Intune</span></span>](/intune/administrative-templates-windows)
- [<span data-ttu-id="3765f-170">Implementar Microsoft Edge con Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="3765f-170">Deploy Microsoft Edge using Microsoft Intune</span></span>](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)