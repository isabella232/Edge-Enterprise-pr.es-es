---
title: Establecer Microsoft Edge como explorador predeterminado en Windows y macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 1/15/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Aprende a establecer Microsoft Edge como explorador predeterminado
ms.openlocfilehash: c8cc45e0fe42dcbbd828dd81ae568f141cda2985
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981092"
---
# <span data-ttu-id="05bf3-103">Establecer Microsoft Edge como explorador predeterminado</span><span class="sxs-lookup"><span data-stu-id="05bf3-103">Set Microsoft Edge as the default browser</span></span>

<span data-ttu-id="05bf3-104">En este artículo se explica como puedes establecer Microsoft Edge como explorador predeterminado en Windows y macOS.</span><span class="sxs-lookup"><span data-stu-id="05bf3-104">This article explains how you can set Microsoft Edge as the default browser on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="05bf3-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior, en Windows 8 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="05bf3-105">This article applies to Microsoft Edge version 77 or later on Windows 8 and Windows 10.</span></span> <span data-ttu-id="05bf3-106">Para Windows 7 y macOS, consulta la directiva [Establecer Microsoft Edge como explorador predeterminado](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled).</span><span class="sxs-lookup"><span data-stu-id="05bf3-106">For Windows 7 and macOS, see the [Set Microsoft Edge as default browser](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled) policy.</span></span>

## <span data-ttu-id="05bf3-107">Introducción</span><span class="sxs-lookup"><span data-stu-id="05bf3-107">Introduction</span></span>

<span data-ttu-id="05bf3-108">Puedes usar la directiva de grupo **Establecer un archivo de configuración de asociaciones predeterminadas**, o la configuración de Administración de dispositivos móviles [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) para establecer Microsoft Edge como explorador predeterminado para la organización.</span><span class="sxs-lookup"><span data-stu-id="05bf3-108">You can use the **Set a default associations configuration file** Group Policy or the [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting to set Microsoft Edge as the default browser for your organization.</span></span>

<span data-ttu-id="05bf3-109">Para establecer el canal estable de Microsoft Edge como explorador predeterminado para los archivos html, los vínculos http/https y los archivos PDF, usa el siguiente ejemplo de archivo de asociación de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="05bf3-109">To set Microsoft Edge Stable as the default browser for html files, http/https links, and PDF files use the following application association file example:</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations> 
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> <span data-ttu-id="05bf3-110">Para establecer Microsoft Edge Beta como explorador predeterminado, establece **ApplicationName** en "Microsoft Edge Beta" y **ProgId** en "MSEdgeBHTML".</span><span class="sxs-lookup"><span data-stu-id="05bf3-110">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="05bf3-111">Para establecer Microsoft Edge Dev como explorador predeterminado, establece **ApplicationName** en "Microsoft Edge Dev" y **ProgId** en "MSEdgeDHTML".</span><span class="sxs-lookup"><span data-stu-id="05bf3-111">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>


> [!NOTE]
> <span data-ttu-id="05bf3-112">Las asociaciones de archivo predeterminadas no se aplican si Microsoft Edge no está instalado en el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="05bf3-112">The default file associations aren't applied if Microsoft Edge isn't installed on the target device.</span></span> <span data-ttu-id="05bf3-113">En este escenario, se pide al usuario que seleccione su aplicación predeterminada cuando abre un vínculo o un archivo htm/html.</span><span class="sxs-lookup"><span data-stu-id="05bf3-113">In this scenario, users are prompted to select their default application when they open a link or a htm/html file.</span></span>

## <span data-ttu-id="05bf3-114">Establecer Microsoft Edge como explorador predeterminado en dispositivos unidos al dominio</span><span class="sxs-lookup"><span data-stu-id="05bf3-114">Set Microsoft Edge as the default browser on domain-joined devices</span></span>

<span data-ttu-id="05bf3-115">Puedes establecer Microsoft Edge como explorador predeterminado en dispositivos unidos al dominio configurando la directiva de grupo **Establecer un archivo de configuración de asociaciones predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="05bf3-115">You can set Microsoft Edge as the default browser on domain-joined devices by configuring the **Set a default associations configuration file** group policy.</span></span> <span data-ttu-id="05bf3-116">Activar esta directiva de grupo requiere crear y almacenar un archivo de configuración de asociaciones predeterminado.</span><span class="sxs-lookup"><span data-stu-id="05bf3-116">Turning this group policy on requires you to create and store a default associations configuration file.</span></span> <span data-ttu-id="05bf3-117">Este archivo se almacena localmente o en un recurso compartido de red.</span><span class="sxs-lookup"><span data-stu-id="05bf3-117">This file is stored locally or on a network share.</span></span> <span data-ttu-id="05bf3-118">Para obtener más información sobre cómo crear este archivo, consulta [Exportar o importar asociaciones de aplicaciones predeterminadas](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span><span class="sxs-lookup"><span data-stu-id="05bf3-118">For more information about creating this file, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span></span>

### <span data-ttu-id="05bf3-119">Para configurar la directiva de grupo para un archivo de configuración de asociaciones de protocolos y tipos de archivo predeterminados:</span><span class="sxs-lookup"><span data-stu-id="05bf3-119">To configure the group policy for a default file type and protocol associations configuration file:</span></span>

1. <span data-ttu-id="05bf3-120">Abre el editor de directiva de grupo y ve a **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.</span><span class="sxs-lookup"><span data-stu-id="05bf3-120">Open the Group Policy editor and go to the **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.</span></span>
2. <span data-ttu-id="05bf3-121">Selecciona **Definir un archivo de configuración de asociaciones predeterminadas**.</span><span class="sxs-lookup"><span data-stu-id="05bf3-121">Select **Set a default associations configuration file**.</span></span>
3. <span data-ttu-id="05bf3-122">Haz clic en **Configuración de directiva** y, después, en **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="05bf3-122">Click **policy setting**, and then click **Enabled**.</span></span>
4. <span data-ttu-id="05bf3-123">En **Opciones**, escribe la ubicación en el archivo de configuración de asociaciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="05bf3-123">Under **Options:**, type the location to your default associations configuration file.</span></span>
5. <span data-ttu-id="05bf3-124">Haz clic en **Aceptar** para guardar la configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="05bf3-124">Click **OK** to save the policy settings.</span></span>

<span data-ttu-id="05bf3-125">En el ejemplo de la siguiente captura de pantalla se muestra un archivo de asociaciones denominado *appassoc.xml* en un recurso compartido de red al que se puede acceder desde el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="05bf3-125">The example in the next screenshot shows an associations file named *appassoc.xml* on a network share that is accessible from the target device.</span></span>

   ![Habilitar la asociación de archivos en la directiva de grupo](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > <span data-ttu-id="05bf3-127">Si esta opción está habilitada y el dispositivo del usuario está unido a un dominio, el archivo de configuración de asociaciones se procesará la próxima vez que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="05bf3-127">If this setting is enabled and the user's device is domain-joined, the associations configuration file is processed the next time the user signs on.</span></span>

## <span data-ttu-id="05bf3-128">Establecer Microsoft Edge como explorador predeterminado en dispositivos unidos a Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="05bf3-128">Set Microsoft Edge as the default browser on Azure Active Directory joined devices</span></span>

<span data-ttu-id="05bf3-129">Para establecer Microsoft Edge como explorador predeterminado en dispositivos unidos a Azure Active Directory, sigue los pasos de configuración de Administración de dispositivos móviles [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) usando el siguiente archivo de asociación de aplicaciones como ejemplo.</span><span class="sxs-lookup"><span data-stu-id="05bf3-129">To set Microsoft Edge as the default browser on Azure Active Directory joined devices follow the steps in the [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting using the following application association file as an example.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> <span data-ttu-id="05bf3-130">Para establecer Microsoft Edge Beta como explorador predeterminado, establece **ApplicationName** en "Microsoft Edge Beta" y **ProgId** en "MSEdgeBHTML".</span><span class="sxs-lookup"><span data-stu-id="05bf3-130">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="05bf3-131">Para establecer Microsoft Edge Dev como explorador predeterminado, establece **ApplicationName** en "Microsoft Edge Dev" y **ProgId** en "MSEdgeDHTML".</span><span class="sxs-lookup"><span data-stu-id="05bf3-131">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>

## <span data-ttu-id="05bf3-132">Establecer Microsoft Edge como explorador predeterminado en macOS</span><span class="sxs-lookup"><span data-stu-id="05bf3-132">Set Microsoft Edge as the default browser on macOS</span></span>

<span data-ttu-id="05bf3-133">Intentar establecer mediante programación el explorador predeterminado en macOS hace que aparezca un aviso al usuario final.</span><span class="sxs-lookup"><span data-stu-id="05bf3-133">Attempting to programmatically set the default browser on macOS causes a prompt to appear for the end user.</span></span> <span data-ttu-id="05bf3-134">Este aviso es una característica de seguridad de macOS que puede quitarse de manera automatizada únicamente mediante AppleScript.</span><span class="sxs-lookup"><span data-stu-id="05bf3-134">This prompt is a macOS security feature that can only be automated away by using an AppleScript.</span></span>

<span data-ttu-id="05bf3-135">Debido a esta limitación, existen dos métodos principales para establecer Microsoft Edge como explorador predeterminado en macOS.</span><span class="sxs-lookup"><span data-stu-id="05bf3-135">Because of this limitation, there are two main methods for setting Microsoft Edge as the default browser on a macOS.</span></span> <span data-ttu-id="05bf3-136">La primera opción es reinstalar en el dispositivo una imagen de macOS donde Microsoft Edge ya se haya establecido como explorador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="05bf3-136">The first option is to flash the device with an image of macOS where Microsoft Edge has already been set as the default browser.</span></span> <span data-ttu-id="05bf3-137">La otra opción es usar la directiva [Establecer Microsoft Edge como explorador predeterminado](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled) , que pide al usuario establecer Microsoft Edge como explorador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="05bf3-137">The other option is to use the [Set Microsoft Edge as default browser](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled) policy, which prompts the user to set Microsoft Edge as the default browser.</span></span>

<span data-ttu-id="05bf3-138">Al usar cualquiera de estos métodos, el usuario sigue pudiendo cambiar el explorador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="05bf3-138">When using either of these methods, it is still possible for a user to change the default browser.</span></span> <span data-ttu-id="05bf3-139">Esto se debe a motivos de seguridad, la preferencia de explorador predeterminado no se puede bloquear mediante programación.</span><span class="sxs-lookup"><span data-stu-id="05bf3-139">This is because for security reasons, the default browser preference can’t be blocked programmatically.</span></span> <span data-ttu-id="05bf3-140">Por este motivo, se recomienda implementar la directiva **Establecer Microsoft Edge como explorador predeterminado** incluso si crea una imagen como Microsoft Edge como explorador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="05bf3-140">For this reason, we recommend that you deploy the **Set Microsoft Edge as default browser** policy even if you create an image with Microsoft Edge as the default browser.</span></span> <span data-ttu-id="05bf3-141">Si la directiva se establece, y un usuario cambia el explorador predeterminado de Microsoft Edge, la próxima vez que abra Microsoft Edge se le pedirá que lo establezca como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="05bf3-141">If the policy is set and a user changes the default browser from Microsoft Edge the next time they open Microsoft Edge, they will be prompted to set it as the default.</span></span>

## <span data-ttu-id="05bf3-142">Consulta también</span><span class="sxs-lookup"><span data-stu-id="05bf3-142">See also</span></span>

- [<span data-ttu-id="05bf3-143">Planear tu implementación de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="05bf3-143">Plan your deployment of Microsoft Edge</span></span>](https://docs.microsoft.com/DeployEdge/deploy-edge-plan-deployment)
- [<span data-ttu-id="05bf3-144">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="05bf3-144">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="05bf3-145">Establecer Microsoft Edge como explorador predeterminado (Windows 7 y macOS)</span><span class="sxs-lookup"><span data-stu-id="05bf3-145">Set Microsoft Edge as default browser (Windows 7 and macOS)</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled)
- [<span data-ttu-id="05bf3-146">Windows 10: ¿Cómo configurar asociaciones de archivos para profesionales de TI?</span><span class="sxs-lookup"><span data-stu-id="05bf3-146">Windows 10 – How to configure file associations for IT Pros?</span></span>](https://docs.microsoft.com/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [<span data-ttu-id="05bf3-147">Exportar o importar asociaciones de aplicaciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="05bf3-147">Export or Import Default Application Associations</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [<span data-ttu-id="05bf3-148">Introducción a DISM</span><span class="sxs-lookup"><span data-stu-id="05bf3-148">DISM Overview</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/what-is-dism)
  - [<span data-ttu-id="05bf3-149">DISM: Administración y mantenimiento de imágenes de implementación</span><span class="sxs-lookup"><span data-stu-id="05bf3-149">DISM - Deployment Image Servicing and Management</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)
