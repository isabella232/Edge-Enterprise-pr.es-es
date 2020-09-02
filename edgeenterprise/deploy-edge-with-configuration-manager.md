---
title: Implementar Microsoft Edge con System Center Configuration Manager
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 09/30/2019
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Aprende a implementar Microsoft Edge con System Center Configuration Manager (SCCM).
ms.openlocfilehash: be14f2db3b28b7585bfad1706b9f82209235df0a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981107"
---
# <span data-ttu-id="72060-103">Implementar Microsoft Edge con System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72060-103">Deploy Microsoft Edge using System Center Configuration Manager</span></span>

<span data-ttu-id="72060-104">En este artículo se muestra cómo automatizar una implementación de Microsoft Edge con System Center Configuration Manager (SCCM).</span><span class="sxs-lookup"><span data-stu-id="72060-104">This article shows you how to automate a Microsoft Edge deployment by using System Center Configuration Manager (SCCM).</span></span>

>[!NOTE]
><span data-ttu-id="72060-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="72060-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="72060-106">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="72060-106">Before you begin</span></span>

<span data-ttu-id="72060-107">Revisa la información de [Introducción a la administración de aplicaciones en Configuration Manager](https://docs.microsoft.com/sccm/apps/understand/introduction-to-application-management).</span><span class="sxs-lookup"><span data-stu-id="72060-107">Review the information in [Introduction to application management in Configuration Manager](https://docs.microsoft.com/sccm/apps/understand/introduction-to-application-management).</span></span> <span data-ttu-id="72060-108">Este artículo de administración de aplicaciones te ayudará a comprender la terminología que se usa en este artículo y es una guía para preparar el sitio para la instalación de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="72060-108">This application management article will help you understand the terminology used in this article and is a guide to preparing your site to install applications.</span></span>

<span data-ttu-id="72060-109">Descarga los archivos de instalación de Microsoft Edge Enterprise (**MicrosoftEdgeDevEnterpriseX64.msi** y/o **MicrosoftEdgeDevEnterpriseX86.msi**) desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="72060-109">Download the Microsoft Edge Enterprise installation files (**MicrosoftEdgeDevEnterpriseX64.msi** and/or **MicrosoftEdgeDevEnterpriseX86.msi**) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="72060-110">Asegúrese de almacenar los archivos de instalación de Microsoft Edge en una ubicación de red accesible.</span><span class="sxs-lookup"><span data-stu-id="72060-110">Make sure you store the Microsoft Edge installation files in an accessible network location.</span></span>

## <span data-ttu-id="72060-111">Crear la aplicación</span><span class="sxs-lookup"><span data-stu-id="72060-111">Create the application</span></span>

<span data-ttu-id="72060-112">Crearás la aplicación mediante un asistente del Administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="72060-112">You'll create the application using a Configuration Manager wizard.</span></span>

### <span data-ttu-id="72060-113">Iniciar el Asistente para crear aplicaciones y crear la aplicación</span><span class="sxs-lookup"><span data-stu-id="72060-113">Start the Create Application Wizard and create the application</span></span>  

1. <span data-ttu-id="72060-114">En la consola del Administrador de configuración, haz clic en **Biblioteca de software** > **Administración de aplicaciones** > **Aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="72060-114">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>  

2. <span data-ttu-id="72060-115">En la pestaña **Inicio**, en el grupo **Crear**, haz clic en **Crear aplicación**.</span><span class="sxs-lookup"><span data-stu-id="72060-115">On the **Home** tab, in the **Create** group, click **Create Application**.</span></span> <span data-ttu-id="72060-116">O bien, haz clic con el botón secundario en **Aplicaciones**, en la barra de navegación, y después haz clic en **Crear aplicación**.</span><span class="sxs-lookup"><span data-stu-id="72060-116">Or, right-click on **Applications** in the navigation bar and then click **Create Application**.</span></span>

    ![Crear aplicación](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. <span data-ttu-id="72060-118">En la página **General** del **Asistente para crear aplicaciones**, elige **Detectar automáticamente la información sobre esta aplicación a partir de archivos de instalación**.</span><span class="sxs-lookup"><span data-stu-id="72060-118">On the **General** page of the **Create Application Wizard**, choose **Automatically detect information about this application from installation files**.</span></span> <span data-ttu-id="72060-119">Esto rellena previamente parte de la información del asistente con información que se ha extraído del archivo de instalación .msi.</span><span class="sxs-lookup"><span data-stu-id="72060-119">This pre-populates some of the information in the wizard with information that's extracted from the installation .msi file.</span></span> <span data-ttu-id="72060-120">Facilita la información siguiente:</span><span class="sxs-lookup"><span data-stu-id="72060-120">Provide the following information:</span></span>  

   - <span data-ttu-id="72060-121">**Tipo**: elige **Windows Installer (archivo \*.msi)**.</span><span class="sxs-lookup"><span data-stu-id="72060-121">**Type**: Choose **Windows Installer (\*.msi file)**.</span></span>  

   - <span data-ttu-id="72060-122">**Ubicación**: escribe la ubicación (o haz clic en **Examinar** para seleccionar la ubicación) del archivo de instalación **MicrosoftEdgeDevEnterpriseX64.msi** o **MicrosoftEdgeDevEnterpriseX86.msi**.</span><span class="sxs-lookup"><span data-stu-id="72060-122">**Location**: Type the location (or click **Browse** to select the location) of the installation file **MicrosoftEdgeDevEnterpriseX64.msi** or **MicrosoftEdgeDevEnterpriseX86.msi**.</span></span> <span data-ttu-id="72060-123">Ten en cuenta que la ubicación debe especificarse en el formulario *\\\Server\Share\File* para que el Administrador de configuración encuentre los archivos de instalación.</span><span class="sxs-lookup"><span data-stu-id="72060-123">Note that the location must be specified in the form *\\\Server\Share\File* for Configuration Manager to locate the installation files.</span></span>  

   <span data-ttu-id="72060-124">La página **Especificar configuración para esta aplicación** será similar al siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="72060-124">Your **Specify settings for this application** page will look like the following example:</span></span>  

    ![Especificar la configuración para esta aplicación](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. <span data-ttu-id="72060-126">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="72060-126">Click **Next**.</span></span> <span data-ttu-id="72060-127">En **Detalles** de la página **Información importada**, verás información sobre la aplicación y cualquier archivo asociado que se haya importado.</span><span class="sxs-lookup"><span data-stu-id="72060-127">Under **Details** on the **Imported Information** page, you'll see information about the application and any associated files that were imported.</span></span> <span data-ttu-id="72060-128">Haz clic en **Siguiente** para continuar con el asistente.</span><span class="sxs-lookup"><span data-stu-id="72060-128">Click **Next** to continue with the wizard.</span></span>  

    ![Ver información importante](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. <span data-ttu-id="72060-130">En la página **Información general**, puedes agregar más información sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-130">On the **General Information** page, you can add more information about the application.</span></span> <span data-ttu-id="72060-131">Por ejemplo, la versión del software, comentarios del administrador y el publicador.</span><span class="sxs-lookup"><span data-stu-id="72060-131">For example, Software version, Administrator comments, and Publisher.</span></span> <span data-ttu-id="72060-132">Puedes usar esta información para ayudarte a ordenar y encontrar la aplicación en la consola del Administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="72060-132">You can use this information to to help you sort and find the application in the Configuration Manager console.</span></span>

   <span data-ttu-id="72060-133">También puedes usar el campo **Programa de instalación** para especificar la línea de comandos completa que se usará para instalar la aplicación en los PC.</span><span class="sxs-lookup"><span data-stu-id="72060-133">You can also use the **Installation program** field to specify the full command line that will be used to install the application on PCs.</span></span> <span data-ttu-id="72060-134">Puedes editarlo para agregar tus propias propiedades (por ejemplo, **/q** para una instalación desatendida).</span><span class="sxs-lookup"><span data-stu-id="72060-134">You can edit this to add your own properties (for example, **/q** for an unattended installation).</span></span>

   <span data-ttu-id="72060-135">En la captura de pantalla siguiente se muestra un ejemplo en el que se usan los campos **Especificar información sobre esta aplicación**.</span><span class="sxs-lookup"><span data-stu-id="72060-135">The following screenshot shows an example where the **Specify information about this application** fields are used.</span></span>

   ![Especificar los metadatos de la aplicación](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. <span data-ttu-id="72060-137">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="72060-137">Click **Next**.</span></span>
7. <span data-ttu-id="72060-138">En la página **Resumen**, puedes confirmar la configuración de la aplicación en **Detalles** y, a continuación, terminar de usar el asistente.</span><span class="sxs-lookup"><span data-stu-id="72060-138">On the **Summary** page, you can confirm your application settings under **Details** and then finish using the wizard.</span></span> <span data-ttu-id="72060-139">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="72060-139">Click **Next**.</span></span>  

    ![Detalles de configuración de la aplicación](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. <span data-ttu-id="72060-141">En la página **Finalización**, haz clic en **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="72060-141">On the **Completion** page, click **Close**.</span></span>

    ![Diálogo Éxito](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

<span data-ttu-id="72060-143">Has terminado de crear la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-143">You've finished creating the application.</span></span> <span data-ttu-id="72060-144">Usa los siguientes pasos para verlo en el Administrador de configuración:</span><span class="sxs-lookup"><span data-stu-id="72060-144">Use the following steps to see it in Configuration Manager:</span></span>

- <span data-ttu-id="72060-145">selecciona el **área de** trabajo de la biblioteca de software</span><span class="sxs-lookup"><span data-stu-id="72060-145">select the **Software Library** workspace</span></span>
- <span data-ttu-id="72060-146">expande **Administración de aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="72060-146">expand **Application Management**</span></span>
- <span data-ttu-id="72060-147">haz clic en **Aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="72060-147">click **Applications**.</span></span>

<span data-ttu-id="72060-148">La siguiente captura de pantalla muestra el ejemplo usado para este artículo.</span><span class="sxs-lookup"><span data-stu-id="72060-148">The following screenshot shows the example used for this article.</span></span>  

![Aplicaciones](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## <span data-ttu-id="72060-150">Cambiar la configuración de las propiedades y la implementación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="72060-150">Change application properties and deployment settings</span></span>

<span data-ttu-id="72060-151">Después de crear una aplicación, puedes refinar la configuración de la aplicación si es necesario.</span><span class="sxs-lookup"><span data-stu-id="72060-151">After you create an application, you can refine the application settings if you need to.</span></span> <span data-ttu-id="72060-152">Para ver las propiedades de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="72060-152">To look at the application properties:</span></span>

- <span data-ttu-id="72060-153">selecciona la aplicación</span><span class="sxs-lookup"><span data-stu-id="72060-153">select the application</span></span>
- <span data-ttu-id="72060-154">en **Inicio**>**Propiedades**, haz clic en **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="72060-154">in **Home**>**Properties**, click **Properties**.</span></span>  

   ![Configurar las propiedades de la aplicación](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 <span data-ttu-id="72060-156">En la página de diálogo **<nombre de aplicación\> Propiedades de la aplicación**, verás una vista con pestañas de los elementos que puedes configurar para cambiar el comportamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-156">In the **<application name\> Application Properties** dialog page, you'll see a tabbed view of the items that you can configure to change the behavior of the application.</span></span> <span data-ttu-id="72060-157">Para obtener más información sobre las opciones que puedes configurar, consulta [Crear aplicaciones](https://docs.microsoft.com/sccm/apps/deploy-use/create-applications).</span><span class="sxs-lookup"><span data-stu-id="72060-157">For more information about the settings you can configure, see [Create applications](https://docs.microsoft.com/sccm/apps/deploy-use/create-applications).</span></span>

<span data-ttu-id="72060-158">Para este ejemplo, cambiarás algunas propiedades del tipo de implementación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-158">For this example, you'll change some properties of the application's deployment type.</span></span> <span data-ttu-id="72060-159">Para cambiar las propiedades de implementación:</span><span class="sxs-lookup"><span data-stu-id="72060-159">To change the deployment properties:</span></span>

1. <span data-ttu-id="72060-160">Haz clic en la pestaña **Tipos de implementación**.</span><span class="sxs-lookup"><span data-stu-id="72060-160">Click the **Deployment Types** tab.</span></span>
2. <span data-ttu-id="72060-161">En **Tipos de implementación:**, selecciona el **Nombre** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-161">Under **Deployment types:**, select the application **Name**</span></span>
3. <span data-ttu-id="72060-162">Haz clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="72060-162">Click **Edit**.</span></span>

   ![Editar el tipo de implementación](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### <span data-ttu-id="72060-164">Agregar un requisito al tipo de implementación</span><span class="sxs-lookup"><span data-stu-id="72060-164">Add a requirement to the deployment type</span></span>

 <span data-ttu-id="72060-165">Los requisitos especifican las condiciones que deben cumplirse para que una aplicación pueda instalarse en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72060-165">Requirements specify conditions that must be met before an application is installed on a device.</span></span> <span data-ttu-id="72060-166">Puedes elegir entre los requisitos integrados o puedes crear los tuyos propios.</span><span class="sxs-lookup"><span data-stu-id="72060-166">You can choose from built-in requirements or you can create your own.</span></span> <span data-ttu-id="72060-167">Por ejemplo, puedes agregar un requisito para que la aplicación solo se instale solo en los PC que ejecutan Windows 10 **x86** o **x64**, según la arquitectura del procesador de destino del archivo de instalación.</span><span class="sxs-lookup"><span data-stu-id="72060-167">For example, you can add a requirement that the application will only be installed on PCs that are running Windows 10 **x86** or **x64**, depending on the installation file's target processor architecture.</span></span> <span data-ttu-id="72060-168">En este ejemplo, tendrás que especificar Windows 10 **x86**.</span><span class="sxs-lookup"><span data-stu-id="72060-168">In this example, you'll specify Windows 10 **x86**.</span></span>

1. <span data-ttu-id="72060-169">En la página de propiedades de tipo de implementación que acabas de abrir, haz clic en la pestaña **Requisitos**.</span><span class="sxs-lookup"><span data-stu-id="72060-169">From the deployment type properties page you just opened, click the **Requirements** tab.</span></span>

2. <span data-ttu-id="72060-170">Haz clic en **Agregar** para abrir el cuadro de diálogo **Crear requisito**.</span><span class="sxs-lookup"><span data-stu-id="72060-170">Click **Add** to open the **Create Requirement** dialog.</span></span>

    ![Crear requisito](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. <span data-ttu-id="72060-172">En el cuadro de diálogo **Crear requisito**, especifica la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="72060-172">In the **Create Requirement** dialog box, specify the following information:</span></span>

    - <span data-ttu-id="72060-173">**Categoría**: **Dispositivo**</span><span class="sxs-lookup"><span data-stu-id="72060-173">**Category**: **Device**</span></span>  

    - <span data-ttu-id="72060-174">**Condición**: **Sistema operativo**</span><span class="sxs-lookup"><span data-stu-id="72060-174">**Condition**: **Operating system**</span></span>  

    - <span data-ttu-id="72060-175">**Tipo de regla**: **Valor**</span><span class="sxs-lookup"><span data-stu-id="72060-175">**Rule type**: **Value**</span></span>  

    - <span data-ttu-id="72060-176">**Operador**: **Uno de**</span><span class="sxs-lookup"><span data-stu-id="72060-176">**Operator**: **One of**</span></span>  

    - <span data-ttu-id="72060-177">En la lista de sistemas operativos, selecciona **Windows 10** > **Todos los Windows 10 (32 bits)**.</span><span class="sxs-lookup"><span data-stu-id="72060-177">From the operating systems list, select **Windows 10** > **All Windows 10 (32-bit)**.</span></span>  

    <span data-ttu-id="72060-178">Cuando hayas terminado, el cuadro de diálogo será similar al siguiente ejemplo de captura de pantalla:</span><span class="sxs-lookup"><span data-stu-id="72060-178">When you're finished, the dialog will look like the following screenshot example:</span></span>

    ![Agregar requisito](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. <span data-ttu-id="72060-180">Haz clic en **Aceptar** para cerrar todas las páginas de propiedades abiertas y volver a la lista **Aplicaciones** de la consola de Administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="72060-180">Click **OK** to close each open property page and return to the **Applications** list in the Configuration Manager console.</span></span>  

## <span data-ttu-id="72060-181">Agregar el contenido de la aplicación a un punto de distribución</span><span class="sxs-lookup"><span data-stu-id="72060-181">Add the application content to a distribution point</span></span>  

<span data-ttu-id="72060-182">Para implementar la aplicación actualizada en los PC, asegúrate de que el contenido de la aplicación se copie en un punto de distribución.</span><span class="sxs-lookup"><span data-stu-id="72060-182">To deploy the updated application to PCs, make sure that the application content is copied to a distribution point.</span></span> <span data-ttu-id="72060-183">Los PC tienen acceso al punto de distribución para instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-183">PCs access the distribution point to install the application.</span></span>  

>[!TIP]
><span data-ttu-id="72060-184">Para obtener más información sobre los puntos de distribución y la administración de contenido en Administrador de configuración, consulta [Implementar y administrar contenido para System Center Configuration Manager](https://docs.microsoft.com/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span><span class="sxs-lookup"><span data-stu-id="72060-184">To find out more about distribution points and content management in Configuration Manager, see [Deploy and manage content for System Center Configuration Manager](https://docs.microsoft.com/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span></span>  

1. <span data-ttu-id="72060-185">En la consola del Administrador de configuración, haz clic en **Biblioteca de software**.</span><span class="sxs-lookup"><span data-stu-id="72060-185">In the Configuration Manager console, click **Software Library**.</span></span>  

2. <span data-ttu-id="72060-186">En el área de trabajo **Biblioteca de software**, expande **Aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="72060-186">In the **Software Library** workspace, expand **Applications**.</span></span> <span data-ttu-id="72060-187">Selecciona la aplicación que hayas creado en la lista de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="72060-187">Select the application you created in the list of applications.</span></span>

3. <span data-ttu-id="72060-188">En la pestaña **Inicio** del grupo **Implementación**, haz clic en **Distribuir contenido**.</span><span class="sxs-lookup"><span data-stu-id="72060-188">On the **Home** tab in the **Deployment** group, click **Distribute Content**.</span></span>  

4. <span data-ttu-id="72060-189">En la página **General** del **Asistente de distribución de contenido**, compruebe que el nombre de la aplicación sea correcto y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="72060-189">On the **General** page of the **Distribute Content Wizard**, check that the application name is correct, and then click **Next**.</span></span>  

5. <span data-ttu-id="72060-190">En la página **Contenido**, revisa la información que se copiará al punto de distribución y luego haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="72060-190">On the **Content** page, review the information that will be copied to the distribution point, and then click **Next**.</span></span>  

6. <span data-ttu-id="72060-191">En la página **Destino del contenido**, haz clic en **Agregar** para seleccionar una o más colecciones, puntos de distribución o grupos de puntos de distribución en los que instalar el contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-191">On the **Content Destination** page, click **Add** to select one or more collections, distribution points, or distribution point groups on which to install the application content.</span></span>

7. <span data-ttu-id="72060-192">Completa el asistente.</span><span class="sxs-lookup"><span data-stu-id="72060-192">Complete the wizard.</span></span>

<span data-ttu-id="72060-193">Puedes comprobar que el contenido de la aplicación se copió correctamente en el punto de distribución desde el área de trabajo **Supervisión**, en **Estado de distribución** > **Estado del contenido**.</span><span class="sxs-lookup"><span data-stu-id="72060-193">You can check that the application content was copied successfully to the distribution point from the **Monitoring** workspace, under **Distribution Status** > **Content Status**.</span></span>  

## <span data-ttu-id="72060-194">Implementar la aplicación</span><span class="sxs-lookup"><span data-stu-id="72060-194">Deploy the application</span></span>  

<span data-ttu-id="72060-195">A continuación, implementa la aplicación en una colección de dispositivos de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="72060-195">Next, deploy the application to a device collection in your hierarchy.</span></span> <span data-ttu-id="72060-196">En este ejemplo, se implementa la aplicación en la colección de dispositivos **Todos los sistemas**.</span><span class="sxs-lookup"><span data-stu-id="72060-196">In this example, you deploy the application to the **All Systems** device collection.</span></span>  

>[!TIP]
><span data-ttu-id="72060-197">Recuerda que solo los equipos con Windows 10 de la arquitectura de procesador especificada instalarán la aplicación, debido a los requisitos que seleccionaste anteriormente.</span><span class="sxs-lookup"><span data-stu-id="72060-197">Remember that only Windows 10 computers of the specified processor architecture will install the application because of the requirements that you selected earlier.</span></span>  

1. <span data-ttu-id="72060-198">En la consola del Administrador de configuración, haz clic en **Biblioteca de software** > **Administración de aplicaciones** > **Aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="72060-198">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>

2. <span data-ttu-id="72060-199">En la lista de aplicaciones, selecciona la aplicación que hayas creado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="72060-199">From the list of applications, select the application that you created earlier.</span></span> <span data-ttu-id="72060-200">Luego, en la pestaña **Inicio**, en el grupo **Implementación**, haz clic en **Implementar**, o haz clic con el botón secundario en la aplicación y selecciona **Implementar**.</span><span class="sxs-lookup"><span data-stu-id="72060-200">Then, on the **Home** tab in the **Deployment** group, click **Deploy**, or right-click the application and select **Deploy**.</span></span>

    ![Implementar la aplicación](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. <span data-ttu-id="72060-202">En la página **General** del **Asistente para implementar software**, haz clic en **Examinar** para seleccionar la colección de dispositivos en la que quieres implementar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-202">On the **General** page of the **Deploy Software Wizard**, click **Browse** to select the device collection to which you want to deploy the application.</span></span>

    ![Busca el archivo de instalación](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. <span data-ttu-id="72060-204">En la página **Contenido**, comprueba que el punto de distribución desde el que quieres que los PC instalen la aplicación esté seleccionado.</span><span class="sxs-lookup"><span data-stu-id="72060-204">On the **Content** page, check that the distribution point from which you want PCs to install the application is selected.</span></span>

    ![Especificar punto de distribución](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. <span data-ttu-id="72060-206">En la página **Configuración de implementación**, asegúrate de que la acción de implementación esté establecida en **Instalar** y que el propósito de la implementación esté establecido en **Requerido**.</span><span class="sxs-lookup"><span data-stu-id="72060-206">On the **Deployment Settings** page, make sure that the deployment action is set to **Install**, and the deployment purpose is set to **Required**.</span></span>

    ![Configurar las opciones de la implementación](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    ><span data-ttu-id="72060-208">Al establecer el propósito de implementación en **Requerido**, te aseguras de que la aplicación esté instalada en los PC que cumplan con los requisitos que estableciste.</span><span class="sxs-lookup"><span data-stu-id="72060-208">By setting the deployment purpose to **Required**, you make sure that the application is installed on PCs that meet the requirements that you set.</span></span> <span data-ttu-id="72060-209">Si estableces este valor en **Disponible**, los usuarios pueden instalar la aplicación a petición desde el Centro de software.</span><span class="sxs-lookup"><span data-stu-id="72060-209">If you set this value to **Available**, then users can install the application on demand from Software Center.</span></span>  

6. <span data-ttu-id="72060-210">En la página **Programación**, puedes configurar cuándo se instalará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-210">On the **Scheduling** page, you can configure when the application will be installed.</span></span> <span data-ttu-id="72060-211">Para este ejemplo, selecciona **Lo antes posible después del tiempo disponible**.</span><span class="sxs-lookup"><span data-stu-id="72060-211">For this example, select **As soon as possible after the available time**.</span></span>

    ![Programar la implementación](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. <span data-ttu-id="72060-213">En la página **Experiencia de usuario**, selecciona los valores deseados y haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="72060-213">On the **User Experience** page, select your desired values and click **Next**.</span></span>

    ![Especificar la experiencia del usuario](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. <span data-ttu-id="72060-215">Especifica las opciones de alerta deseadas y haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="72060-215">Specify your desired alert options and click **Next**.</span></span>

    ![Especificar la configuración de alertas](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. <span data-ttu-id="72060-217">Completa el asistente.</span><span class="sxs-lookup"><span data-stu-id="72060-217">Complete the wizard.</span></span>

<span data-ttu-id="72060-218">Usa la información de la siguiente sección **Supervisar la aplicación** para ver el estado de la implementación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-218">Use the information in the following **Monitor the application** section to see the status of your application deployment.</span></span>  

## <span data-ttu-id="72060-219">Supervisar la aplicación</span><span class="sxs-lookup"><span data-stu-id="72060-219">Monitor the application</span></span>

 <span data-ttu-id="72060-220">En esta sección, echaremos un vistazo rápido al estado de implementación de la aplicación que acabas de implementar.</span><span class="sxs-lookup"><span data-stu-id="72060-220">In this section, you'll take a quick look at the deployment status of the application that you just deployed.</span></span>  

### <span data-ttu-id="72060-221">Para revisar el estado de implementación</span><span class="sxs-lookup"><span data-stu-id="72060-221">To review the deployment status</span></span>  

1. <span data-ttu-id="72060-222">En la consola de Administrador de configuración, haga clic en **Supervisión** > **Implementaciones**.</span><span class="sxs-lookup"><span data-stu-id="72060-222">In the Configuration Manager console, click **Monitoring** > **Deployments**.</span></span>  

2. <span data-ttu-id="72060-223">En la lista de implementaciones, selecciona la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-223">From the list of deployments, select the application.</span></span>

    ![Supervisar la implementación](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. <span data-ttu-id="72060-225">En la pestaña **Inicio** del grupo **Implementación**, haga clic en **Ver estado**.</span><span class="sxs-lookup"><span data-stu-id="72060-225">On the **Home** tab in the **Deployment** group, click **View Status**.</span></span>  

4. <span data-ttu-id="72060-226">Selecciona una de las siguientes pestañas para ver más actualizaciones de estado sobre la implementación de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="72060-226">Select one of the following tabs to see more status updates about the application deployment:</span></span>  

    - <span data-ttu-id="72060-227">**Correcto**: la aplicación se instaló correctamente en los PC indicados.</span><span class="sxs-lookup"><span data-stu-id="72060-227">**Success**: The application installed successfully on the indicated PCs.</span></span>  

    - <span data-ttu-id="72060-228">**En curso**: la aplicación aún no ha finalizado la instalación.</span><span class="sxs-lookup"><span data-stu-id="72060-228">**In Progress**: The application has not yet finished installing.</span></span>  

    - <span data-ttu-id="72060-229">**Error**: se ha producido un error al instalar la aplicación en los PC indicados.</span><span class="sxs-lookup"><span data-stu-id="72060-229">**Error**: An error occurred installing the application on the indicated PCs.</span></span> <span data-ttu-id="72060-230">También se muestra información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="72060-230">Further information about the error is also displayed.</span></span>  

    - <span data-ttu-id="72060-231">**Requisitos no cumplidos**: no se realizó ningún intento de instalación en los dispositivos indicados porque no cumplían los requisitos que configuraste (en este ejemplo, porque no ejecutan Windows 10).</span><span class="sxs-lookup"><span data-stu-id="72060-231">**Requirements Not Met**: No installation attempt was made on the indicated devices because they did not meet the requirements you configured (in this example, because they do not run on Windows 10.)</span></span>

    - <span data-ttu-id="72060-232">**Desconocido**: Administrador de configuración no pudo informar del estado de la implementación.</span><span class="sxs-lookup"><span data-stu-id="72060-232">**Unknown**: Configuration Manager was unable to report the status of the deployment.</span></span> <span data-ttu-id="72060-233">Vuelve a consultar más tarde.</span><span class="sxs-lookup"><span data-stu-id="72060-233">Check back again later.</span></span>  

    >[!TIP]
    ><span data-ttu-id="72060-234">Existen diversas formas en las que puedes supervisar las implementaciones de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="72060-234">There are several ways you can monitor application deployments.</span></span> <span data-ttu-id="72060-235">Para obtener más información, consulta [Supervisar aplicaciones desde la consola de System Center Configuration Manager](https://docs.microsoft.com/sccm/apps/deploy-use/monitor-applications-from-the-console).</span><span class="sxs-lookup"><span data-stu-id="72060-235">For more information, see [Monitor applications from the System Center Configuration Manager console](https://docs.microsoft.com/sccm/apps/deploy-use/monitor-applications-from-the-console).</span></span>  

## <span data-ttu-id="72060-236">Experiencia de usuario final</span><span class="sxs-lookup"><span data-stu-id="72060-236">End-user experience</span></span>  

<span data-ttu-id="72060-237">Los usuarios que dispongan de PC administrados por el Administrador de configuración que ejecuten Windows 10 para la arquitectura de procesador especificada verán un mensaje en el que se les indica que deben instalar la aplicación de Microsoft Edge Dev.</span><span class="sxs-lookup"><span data-stu-id="72060-237">Users who have PCs that are managed by Configuration Manager and are running Windows 10 of the specified processor architecture, will see a message telling them that they must install the Microsoft Edge Dev application.</span></span> <span data-ttu-id="72060-238">Cuando acepten esta opción de instalación, se instalará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72060-238">When they accept this installation option, the application is installed.</span></span>  

## <span data-ttu-id="72060-239">Consulta también</span><span class="sxs-lookup"><span data-stu-id="72060-239">See also</span></span>

- [<span data-ttu-id="72060-240">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="72060-240">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="72060-241">Crear e implementar una aplicación con System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72060-241">Create and deploy an application with System Center Configuration Manager</span></span>](https://docs.microsoft.com/sccm/apps/get-started/create-and-deploy-an-application)
