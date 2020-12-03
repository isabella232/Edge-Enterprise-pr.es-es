---
title: Automatizar Microsoft Edge para la implementación en macOS con Microsoft Intune
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 11/30/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Cómo automatizar Microsoft Edge para la implementación en macOS con Jamf.
ms.openlocfilehash: 8639c0b7bf78bb8e22370dba29b592af73d8cb40
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194728"
---
# <span data-ttu-id="fee09-103">Implementar en macOS con Jamf</span><span class="sxs-lookup"><span data-stu-id="fee09-103">Deploy to macOS with Jamf</span></span>

<span data-ttu-id="fee09-104">En este artículo se describe cómo implementar Microsoft Edge para macOS usando Jamf.</span><span class="sxs-lookup"><span data-stu-id="fee09-104">This article describes how to deploy Microsoft Edge for macOS using Jamf.</span></span>

> [!NOTE]
> <span data-ttu-id="fee09-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fee09-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="fee09-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fee09-106">Prerequisites</span></span>

<span data-ttu-id="fee09-107">Antes de implementar Microsoft Edge, asegúrate de cumplir los requisitos previos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fee09-107">Before you deploy Microsoft Edge, make sure you meet the following prerequisites:</span></span>

- <span data-ttu-id="fee09-108">El archivo de instalación de Microsoft Edge, **MicrosoftEdgeDev-\<version\>.pkg** está en una ubicación accesible de la red.</span><span class="sxs-lookup"><span data-stu-id="fee09-108">The Microsoft Edge installation file,  **MicrosoftEdgeDev-\<version\>.pkg** is in an accessible location on your network.</span></span> <span data-ttu-id="fee09-109">Puedes descargar los archivos de instalación de Microsoft Edge Enterprise desde la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="fee09-109">You can download the Microsoft Edge Enterprise installation files from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="fee09-110">Tienes una cuenta de nube de Jamf con el nivel de acceso y privilegios necesarios para crear e implementar archivos de instalación en equipos.</span><span class="sxs-lookup"><span data-stu-id="fee09-110">You have a Jamf Cloud account with the level of access and privileges needed to create and deploy installation files to computers.</span></span>

## <span data-ttu-id="fee09-111">Para implementar Microsoft Edge con Jamf:</span><span class="sxs-lookup"><span data-stu-id="fee09-111">To deploy Microsoft Edge using Jamf:</span></span>

1. <span data-ttu-id="fee09-112">Inicia sesión en Jamf y ve a **Toda la configuración**.</span><span class="sxs-lookup"><span data-stu-id="fee09-112">Sign on to Jamf and go to **All Settings**.</span></span>

    ![Abrir Toda la configuración](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. <span data-ttu-id="fee09-114">En **Toda la configuración**, haz clic en **Administración de equipos**.</span><span class="sxs-lookup"><span data-stu-id="fee09-114">Under **All Settings**, click **Computer Management**.</span></span>

    ![Selecciona Administración de equipos.](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. <span data-ttu-id="fee09-116">En **Administración de equipos**, haz clic en **Paquetes**.</span><span class="sxs-lookup"><span data-stu-id="fee09-116">Under **Computer Management**, click **Packages**.</span></span>

    ![Seleccionar Paquetes](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. <span data-ttu-id="fee09-118">En la página **Paquetes**, haz clic en **+ Nuevo** para agregar un nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="fee09-118">On the **Packages** page, click **+ New** to add a new package.</span></span>

    ![Seleccionar Nuevo para agregar un nuevo paquete](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. <span data-ttu-id="fee09-120">En la página **Nuevo paquete**, escribe los detalles del paquete y, a continuación haz clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="fee09-120">On the **New Package** page, enter the details about the package and then click **Save**.</span></span> <span data-ttu-id="fee09-121">(Por ejemplo, NOMBRE PARA MOSTRAR, INFORMACIÓN o NOTAS).</span><span class="sxs-lookup"><span data-stu-id="fee09-121">(For example, DISPLAY NAME, INFO, or NOTES.)</span></span>

    ![Seleccionar Guardar para guardar la información del paquete](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. <span data-ttu-id="fee09-123">Selecciona **Equipos** en la barra de menús y, a continuación, selecciona **Directivas** en la barra de navegación.</span><span class="sxs-lookup"><span data-stu-id="fee09-123">Select **Computers** on the menu bar, and then select **Policies** in the navigation bar.</span></span>

7. <span data-ttu-id="fee09-124">Selecciona **+ Nuevo** para mostrar el panel **Nueva directiva**.</span><span class="sxs-lookup"><span data-stu-id="fee09-124">Select **+ New** to display the **New Policy** pane.</span></span>

    ![Seleccionar Nuevo para crear una nueva directiva](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. <span data-ttu-id="fee09-126">En la pestaña **Opciones**, selecciona **General**.</span><span class="sxs-lookup"><span data-stu-id="fee09-126">On the **Options** tab, select **General**.</span></span>

    - <span data-ttu-id="fee09-127">En **NOMBRE PARA MOSTRAR**, escribe el nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="fee09-127">Under **DISPLAY NAME**, enter the display name for the policy.</span></span>
    - <span data-ttu-id="fee09-128">En **Desencadenador**, selecciona el evento que desencadenará la nueva directiva.</span><span class="sxs-lookup"><span data-stu-id="fee09-128">Under **Trigger**, select the event that will trigger the policy.</span></span> <span data-ttu-id="fee09-129">(En el siguiente ejemplo, el evento es Inicio).</span><span class="sxs-lookup"><span data-stu-id="fee09-129">(In the following example, the event is Startup.)</span></span>

    ![Escribir la información sobre implementación](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. <span data-ttu-id="fee09-131">En la pestaña **Opciones**, haz clic en **Paquetes**.</span><span class="sxs-lookup"><span data-stu-id="fee09-131">On the **Options** tab, click **Packages**.</span></span>

10. <span data-ttu-id="fee09-132">En el menú emergente **Configurar paquetes**, haz clic en **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="fee09-132">On the **Configure Packages** popup, click **Configure**.</span></span>

    ![Configurar el paquete](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. <span data-ttu-id="fee09-134">El paquete que agregaste se muestra en el panel **Paquetes**.</span><span class="sxs-lookup"><span data-stu-id="fee09-134">The package that you added shows on the **Packages** pane.</span></span> <span data-ttu-id="fee09-135">Haz clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="fee09-135">Click **Add**.</span></span> <span data-ttu-id="fee09-136">En este ejemplo, el paquete es "MicrosoftEdgeBeta" en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="fee09-136">For this example, the package is "MicrosoftEdgeBeta" in the following screenshot.</span></span>

    ![Agregar paquete](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. <span data-ttu-id="fee09-138">En la página **Nueva directiva**, usa las listas desplegables para seleccionar el **PUNTO DE DISTRIBUCIÓN** y la **ACCIÓN** a tomar para la directiva.</span><span class="sxs-lookup"><span data-stu-id="fee09-138">On the **New Policy** page, uUse the drop-down lists to select the **DISTRIBUTION POINT** and **ACTION** to take for the policy.</span></span> <span data-ttu-id="fee09-139">Haz clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="fee09-139">Click **Save**.</span></span> <span data-ttu-id="fee09-140">La captura de pantalla siguiente usa el "Punto de distribución predeterminado de cada equipo" e "Instalar" como ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fee09-140">The following screenshot uses "Each computer's default distribution point" and "Install" as an example.</span></span>

    ![Seleccionar punto de distribución y acción](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. <span data-ttu-id="fee09-142">En la página **Nueva directiva**, selecciona la pestaña **Ámbito**. Puedes administrar el ámbito de la implementación en función de los equipos o los usuarios.</span><span class="sxs-lookup"><span data-stu-id="fee09-142">On the **New Policy** page, select the **Scope** tab. You can manage the scope of the deployment based on computers or users.</span></span> <span data-ttu-id="fee09-143">Para este ejemplo, selecciona **Todos los equipos** en la lista desplegable **EQUIPOS DE DESTINO** y, a continuación, haz clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="fee09-143">For this example, select **All Computers** from the **TARGET COMPUTERS** drop-down list and then click **Save**.</span></span>

    ![Seleccionar el ámbito de la implementación](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. <span data-ttu-id="fee09-145">En este punto, puedes revisar la directiva de implementación de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fee09-145">At this point you can review the Microsoft Edge deployment policy.</span></span> <span data-ttu-id="fee09-146">Si las opciones de implementación cumplen los requisitos, haz clic en **Listo**.</span><span class="sxs-lookup"><span data-stu-id="fee09-146">If the deployment options meet your requirements, click **Done**.</span></span>

    ![Hacer clic en Listo](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > <span data-ttu-id="fee09-148">Puedes volver a una directiva de implementación en cualquier momento para cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="fee09-148">You can return to a deployment policy at any time to change settings.</span></span>

<span data-ttu-id="fee09-149">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="fee09-149">Congratulations!</span></span> <span data-ttu-id="fee09-150">Acabas de finalizar la configuración Jamf para implementar Microsoft Edge para macOS.</span><span class="sxs-lookup"><span data-stu-id="fee09-150">You’ve just finished configuring Jamf to deploy Microsoft Edge for macOS.</span></span> <span data-ttu-id="fee09-151">Cuando la condición de desencadenador que definiste sea verdadera, el paquete se implementará en los equipos que especificaste.</span><span class="sxs-lookup"><span data-stu-id="fee09-151">When the trigger condition you defined is true, the package will get deployed to the computers you specified.</span></span>

## <span data-ttu-id="fee09-152">Consulta también</span><span class="sxs-lookup"><span data-stu-id="fee09-152">See also</span></span>

- [<span data-ttu-id="fee09-153">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="fee09-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="fee09-154">Jamf.com</span><span class="sxs-lookup"><span data-stu-id="fee09-154">Jamf.com</span></span>](https://www.jamf.com/)
- [<span data-ttu-id="fee09-155">Integrar Jamf con Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="fee09-155">Integrate Jamf with Microsoft Intune</span></span>](https://docs.microsoft.com/intune/conditional-access-integrate-jamf)
