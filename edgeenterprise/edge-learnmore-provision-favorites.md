---
title: Aprovisionar favoritos en Microsoft Edge
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 09/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Aprovisionar favoritos en Microsoft Edge
ms.openlocfilehash: 94bd42573bdbc0fd1b971ded1c82e5fe152acc54
ms.sourcegitcommit: 854dd73eb168960c0eb4b483f81a8efe88806a64
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088724"
---
# <span data-ttu-id="e4081-103">Aprovisionar favoritos en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e4081-103">Provision favorites for Microsoft Edge</span></span>

<span data-ttu-id="e4081-104">Hemos realizado mejoras en el aprovisionamiento de favoritos basándonos en los comentarios de los clientes.</span><span class="sxs-lookup"><span data-stu-id="e4081-104">Based on customer feedback, we've made improvements to provisioning favorites.</span></span> <span data-ttu-id="e4081-105">A partir de la versión 85 de Microsoft Edge, los administradores ya no tienen que diseñar manualmente un archivo para aprovisionar favoritos.</span><span class="sxs-lookup"><span data-stu-id="e4081-105">Starting with Microsoft Edge version 85, Admins no longer have to manually craft a file to provision favorites.</span></span> <span data-ttu-id="e4081-106">Los administradores pueden agregar favoritos y carpetas mediante la interfaz de usuario de Microsoft Edge para generar un archivo que puede exportarse a una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e4081-106">Admins can add favorites and folders using the Microsoft Edge UI to generate a file that can be exported to a group policy.</span></span>

<span data-ttu-id="e4081-107">En este artículo se describe cómo aprovisionar un conjunto de favoritos y de carpetas en la organización.</span><span class="sxs-lookup"><span data-stu-id="e4081-107">This article describes how to provision a set of favorites and folders for your organization.</span></span> <span data-ttu-id="e4081-108">Puede usar la directiva [Configurar favoritos](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#configure-favorites) para aprovisionar favoritos y carpetas.</span><span class="sxs-lookup"><span data-stu-id="e4081-108">You can use the [Configure favorites](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#configure-favorites) policy to provision favorites and folders.</span></span>

> [!NOTE]
> <span data-ttu-id="e4081-109">Este artículo se aplica a Microsoft Edge, versión 85 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e4081-109">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="e4081-110">Requisitos previos y recomendaciones</span><span class="sxs-lookup"><span data-stu-id="e4081-110">Prerequisites and recommendations</span></span>

- <span data-ttu-id="e4081-111">La versión 85 de Microsoft Edge con la plantilla administrativa adecuada instalada para las directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="e4081-111">Microsoft Edge version 85 with the appropriate administrative template installed for group policies.</span></span>
- <span data-ttu-id="e4081-112">Le recomendamos usar un perfil nuevo en Microsoft Edge para aprovisionar estos favoritos.</span><span class="sxs-lookup"><span data-stu-id="e4081-112">We recommend that you use a new profile in Microsoft Edge to provision these favorites.</span></span> <span data-ttu-id="e4081-113">Todos los favoritos que se guarden con el perfil se incluirán en la exportación.</span><span class="sxs-lookup"><span data-stu-id="e4081-113">All favorites that are saved with the profile will be included in the export.</span></span>  

## <span data-ttu-id="e4081-114">Aprovisionar favoritos y carpetas</span><span class="sxs-lookup"><span data-stu-id="e4081-114">Provision favorites and folders</span></span>

<span data-ttu-id="e4081-115">Siga los siguientes pasos para aprovisionar favoritos y carpetas para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="e4081-115">Use the following steps to provision favorites and folders for your users.</span></span>

1. <span data-ttu-id="e4081-116">Vaya a la barra de direcciones de Microsoft Edge y escriba esta dirección URL: *edge://flags/#edge-favorites-admin-export*.</span><span class="sxs-lookup"><span data-stu-id="e4081-116">Go to the Microsoft Edge address bar and type this URL: *edge://flags/#edge-favorites-admin-export*.</span></span>
2. <span data-ttu-id="e4081-117">En **Exportar la configuración de favoritos para administradores**, seleccione **Habilitado** en la lista desplegable y, a continuación, haga clic en **Reiniciar**.</span><span class="sxs-lookup"><span data-stu-id="e4081-117">Under **Favorites configuration export for administrators**, pick **Enabled** from the dropdown list and then click **Restart**.</span></span>

3. <span data-ttu-id="e4081-118">Vaya a la página **Favoritos** en *edge://favorites* para agregar los favoritos y las carpetas que quiera aprovisionar.</span><span class="sxs-lookup"><span data-stu-id="e4081-118">Go to the **Favorites** page at *edge://favorites* so you can add the favorites and folders that you want to provision.</span></span>

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. <span data-ttu-id="e4081-119">Cuando termine de agregar favoritos y carpetas, los exportará para que puedan usarse en la directiva **Configurar favoritos**.</span><span class="sxs-lookup"><span data-stu-id="e4081-119">When you finish adding favorites and folders you'll export them so they can be used by the **Configure favorites** policy.</span></span> <span data-ttu-id="e4081-120">Vaya a la barra de direcciones, desplácese hasta *edge://favorites*, haga clic en los puntos suspensivos "**...**" y elija **Exportar la configuración de favoritos**.</span><span class="sxs-lookup"><span data-stu-id="e4081-120">Go to the address bar and navigate to *edge://favorites*, click the ellipsis "**…**" and choose **Export favorites configuration**.</span></span> <span data-ttu-id="e4081-121">La siguiente captura de pantalla muestra las opciones que tiene para aprovisionar favoritos.</span><span class="sxs-lookup"><span data-stu-id="e4081-121">The next screenshot shows the options you have when provisioning favorites.</span></span>

   ![Opciones de menú para trabajar con favoritos.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. <span data-ttu-id="e4081-123">En **Exportar la configuración de favoritos**, especifique un nombre para la carpeta que verán los usuarios.</span><span class="sxs-lookup"><span data-stu-id="e4081-123">Under **Export your favorites configuration** you provide a name for the folder that your users will see.</span></span> <span data-ttu-id="e4081-124">Escriba el nombre de la carpeta y elija el formato de plataforma que quiera usar.</span><span class="sxs-lookup"><span data-stu-id="e4081-124">Type the Folder name and pick the Platform format you want to use.</span></span> <span data-ttu-id="e4081-125">Haga clic en **Copiar en el portapapeles**.</span><span class="sxs-lookup"><span data-stu-id="e4081-125">Click **Copy to clipboard**.</span></span> <span data-ttu-id="e4081-126">La siguiente captura de pantalla muestra "Favoritos administrados" para el nombre de la carpeta, y la plataforma es Windows.</span><span class="sxs-lookup"><span data-stu-id="e4081-126">The next screenshot shows "Managed favorites" for the folder name and the platform is Windows.</span></span>

   ![Cuadro de diálogo para exportar favoritos a una carpeta de Windows.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. <span data-ttu-id="e4081-128">Abra el Editor de directivas de grupo, desplácese a *Configuración del equipo/Plantillas administrativas/* y seleccione **Configurar favoritos**.</span><span class="sxs-lookup"><span data-stu-id="e4081-128">Open the Group Policy Editor, navigate to *Computer Configuration/Administrative Templates/* and pick **Configure Favorites**.</span></span> <span data-ttu-id="e4081-129">Habilite la directiva "Configurar favoritos".</span><span class="sxs-lookup"><span data-stu-id="e4081-129">Enable the "Configure Favorites" policy.</span></span> <span data-ttu-id="e4081-130">En **Opciones:**, pegue el contenido exportado en el área de texto Configurar favoritos y, a continuación, haga clic en **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="e4081-130">Under **Options:**, paste the exported contents in the Configure favorites text area then click **Apply**.</span></span> <span data-ttu-id="e4081-131">La siguiente captura de pantalla muestra un ejemplo de la carpeta "Favoritos administrados" del paso 5.</span><span class="sxs-lookup"><span data-stu-id="e4081-131">The next screenshot shows an example of the "Managed favorites" folder from step 5.</span></span>

   ![Use gpedit para habilitar y configurar la directiva "Configurar favoritos".](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. <span data-ttu-id="e4081-133">Haga clic en **Aceptar** o **Aplicar** para guardar la configuración de la directiva.</span><span class="sxs-lookup"><span data-stu-id="e4081-133">Click **OK** or **Apply** to safe the policy settings.</span></span>

## <span data-ttu-id="e4081-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e4081-134">See also</span></span>

- [<span data-ttu-id="e4081-135">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="e4081-135">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)