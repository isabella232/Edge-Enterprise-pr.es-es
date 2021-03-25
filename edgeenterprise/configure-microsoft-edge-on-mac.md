---
title: Configurar Microsoft Edge para macOS con un .plist
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar las opciones de directiva de Microsoft Edge en macOS con un .plist
ms.openlocfilehash: 3f297c11d8009c85a1bc5e17447681ee2b9ef1e2
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447454"
---
# <a name="configure-microsoft-edge-policy-settings-for-macos-using-a-plist"></a><span data-ttu-id="d1c2a-103">Configurar las opciones de directiva de Microsoft Edge en macOS con un .plist</span><span class="sxs-lookup"><span data-stu-id="d1c2a-103">Configure Microsoft Edge policy settings for macOS using a .plist</span></span>

<span data-ttu-id="d1c2a-104">En este artículo se describe cómo configurar Microsoft Edge en macOS con un archivo de lista de propiedades (.plist).</span><span class="sxs-lookup"><span data-stu-id="d1c2a-104">This article describes how to configure Microsoft Edge on macOS using a property list (.plist) file.</span></span> <span data-ttu-id="d1c2a-105">Obtendrá información sobre cómo crear este archivo e implementarlo en Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-105">You'll learn how to create this file and then deploy it to Microsoft Intune.</span></span>

<span data-ttu-id="d1c2a-106">Para obtener más información, consulta [Acerca de los archivos de lista de propiedades de información](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (sitio web de Apple) y [Configuración de carga personalizada](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span><span class="sxs-lookup"><span data-stu-id="d1c2a-106">For more information, see [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple's website) and [Custom payload settings](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span></span>

> [!NOTE]
> <span data-ttu-id="d1c2a-107">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-107">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="configure-microsoft-edge-policies-on-macos"></a><span data-ttu-id="d1c2a-108">Configurar las directivas de Microsoft Edge en macOS</span><span class="sxs-lookup"><span data-stu-id="d1c2a-108">Configure Microsoft Edge policies on macOS</span></span>

<span data-ttu-id="d1c2a-109">El primer paso es crear el archivo plist.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-109">The first step is to create your plist.</span></span> <span data-ttu-id="d1c2a-110">Puedes crear el archivo plist con cualquier editor de texto o puedes usar [Terminal para crear el perfil de configuración](#create-a-configuration-profile-using-terminal).</span><span class="sxs-lookup"><span data-stu-id="d1c2a-110">You can create the plist file with any text editor or you can use [Terminal to create the configuration profile](#create-a-configuration-profile-using-terminal).</span></span> <span data-ttu-id="d1c2a-111">Sin embargo, es más fácil crear y editar un archivo plist con una herramienta que te dé formato al código XML.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-111">However, it's easier to create and edit a plist file using a tool that formats the XML code for you.</span></span> <span data-ttu-id="d1c2a-112">*Xcode* es un entorno de desarrollo integrado gratuito que puedes obtener desde una de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="d1c2a-112">*Xcode* is a free integrated development environment that you can get from one of the following locations:</span></span>

- [<span data-ttu-id="d1c2a-113">Sitio web de desarrolladores de Apple</span><span class="sxs-lookup"><span data-stu-id="d1c2a-113">Apple developer website</span></span>](https://developer.apple.com/xcode/)
- [<span data-ttu-id="d1c2a-114">Mac App Store</span><span class="sxs-lookup"><span data-stu-id="d1c2a-114">Mac App Store</span></span>](https://apps.apple.com/app/xcode/id497799835?mt=12)

<span data-ttu-id="d1c2a-115">Para obtener una lista de las directivas admitidas y sus nombres clave preferidos, consulta [Referencia de directivas del explorador de Microsoft Edge](microsoft-edge-policies.md).</span><span class="sxs-lookup"><span data-stu-id="d1c2a-115">For a list of supported policies and their preference key names, see [Microsoft Edge browser policies reference](microsoft-edge-policies.md).</span></span> <span data-ttu-id="d1c2a-116">En el archivo de plantillas de directiva, que se puede descargar desde la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise), hay un ejemplo de archivo plist (*itadminexample.plist*) en la carpeta de **ejemplos**.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-116">In the policy templates file, which can be downloaded from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise), there's an example plist (*itadminexample.plist*) in the **examples** folder.</span></span> <span data-ttu-id="d1c2a-117">El archivo de ejemplo contiene todos los tipos de datos admitidos que se pueden personalizar para definir la configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-117">The example file contains all supported data types that you can customize to define your policy settings.</span></span> 

<span data-ttu-id="d1c2a-118">El siguiente paso después de crear el contenido del archivo plist, es asignarle un nombre usando el dominio de preferencia de Microsoft Edge, *com.microsoft.Edge*.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-118">The next step after you create the contents of your plist, is to name it using the Microsoft Edge preference domain, *com.microsoft.Edge*.</span></span> <span data-ttu-id="d1c2a-119">El nombre distingue entre mayúsculas y minúsculas y no debe incluir el canal de destino porque se aplica a todos los canales de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-119">The name is case sensitive and should not include the channel you are targeting because it applies to all Microsoft Edge channels.</span></span> <span data-ttu-id="d1c2a-120">El nombre de archivo plist debe ser **_com.microsoft.Edge.plist_**.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-120">The plist file name must be **_com.microsoft.Edge.plist_**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1c2a-121">A partir de la compilación 78.0.249.2, todos los canales de Microsoft Edge en macOS se leen desde el dominio de preferencias **com.microsoft.Edge**.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-121">Starting with build 78.0.249.2, all Microsoft Edge channels on macOS read from the **com.microsoft.Edge** preference domain.</span></span> <span data-ttu-id="d1c2a-122">Todas las versiones anteriores se leían desde un dominio específico de canal, como **com.microsoft.Edge.Dev** para el canal Dev.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-122">All prior releases read from a channel specific domain, such as **com.microsoft.Edge.Dev** for Dev channel.</span></span>

<span data-ttu-id="d1c2a-123">El último paso es implementar el archivo plist en los dispositivos Mac de los usuarios con el proveedor de MDM que prefieras, como Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-123">The last step is to deploy your plist to your users' Mac devices using your preferred MDM provider, such as Microsoft Intune.</span></span> <span data-ttu-id="d1c2a-124">Para obtener instrucciones, consulta [Implementar el archivo plist](#deploy-your-plist).</span><span class="sxs-lookup"><span data-stu-id="d1c2a-124">For instructions see [Deploy your plist](#deploy-your-plist).</span></span>

### <a name="create-a-configuration-profile-using-terminal"></a><span data-ttu-id="d1c2a-125">Crear un perfil de configuración con Terminal</span><span class="sxs-lookup"><span data-stu-id="d1c2a-125">Create a configuration profile using Terminal</span></span>

1. <span data-ttu-id="d1c2a-126">En Terminal, usa el siguiente comando para crear un archivo plist para Microsoft Edge en el escritorio, con la configuración que prefieras:</span><span class="sxs-lookup"><span data-stu-id="d1c2a-126">In Terminal, use the following command to create a plist for Microsoft Edge on your desktop with your preferred settings:</span></span>

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. <span data-ttu-id="d1c2a-127">Convierte el archivo plist de formato binario a texto sin formato:</span><span class="sxs-lookup"><span data-stu-id="d1c2a-127">Convert the plist from binary to plain text format:</span></span>

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

<span data-ttu-id="d1c2a-128">Después de convertir el archivo, comprueba que los datos de la directiva sean correctos y contengan la configuración que quieras para tu perfil de configuración.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-128">After converting the file verify that your policy data is correct and contains the settings you want for your configuration profile.</span></span>

> [!NOTE]
> <span data-ttu-id="d1c2a-129">Solo los pares de clave y valor deben encontrarse en el contenido del archivo plist o xml.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-129">Only key value pairs should be in the contents of the plist or xml file.</span></span> <span data-ttu-id="d1c2a-130">Antes de cargar el archivo en Intune, elimine todos los valores de \<plist> y \<dict> los encabezados XML del archivo.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-130">Prior to uploading your file into Intune remove all the \<plist> and \<dict> values, and xml headers from your file.</span></span> <span data-ttu-id="d1c2a-131">El archivo solo debe contener pares de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-131">The file should only contain key value pairs.</span></span>

## <a name="deploy-your-plist"></a><span data-ttu-id="d1c2a-132">Implementar el archivo plist</span><span class="sxs-lookup"><span data-stu-id="d1c2a-132">Deploy your plist</span></span>

<span data-ttu-id="d1c2a-133">Para Microsoft Intune, crea un nuevo perfil de configuración de dispositivo destinado a la plataforma macOS y selecciona el tipo de perfil del *Archivo de preferencias*.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-133">For Microsoft Intune create a new device configuration profile targeting the macOS platform and select the *Preference file* profile type.</span></span> <span data-ttu-id="d1c2a-134">Elige como destino **com.microsoft.Edge** como nombre de dominio preferente y carga el plist.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-134">Target **com.microsoft.Edge** as the preference domain name and upload your plist.</span></span> <span data-ttu-id="d1c2a-135">Para obtener más información, consulta [Agregar un archivo de lista de propiedades a dispositivos macOS con Microsoft Intune](/intune/configuration/preference-file-settings-macos).</span><span class="sxs-lookup"><span data-stu-id="d1c2a-135">For more information see [Add a property list file to macOS devices using Microsoft Intune](/intune/configuration/preference-file-settings-macos).</span></span>

<span data-ttu-id="d1c2a-136">Para Jamf, carga el archivo .plist como una carga de *Configuración personalizada*.</span><span class="sxs-lookup"><span data-stu-id="d1c2a-136">For Jamf upload the .plist file as a *Custom Settings* payload.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1c2a-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d1c2a-137">See also</span></span>

- [<span data-ttu-id="d1c2a-138">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="d1c2a-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="d1c2a-139">Configurar para macOS con Jamf</span><span class="sxs-lookup"><span data-stu-id="d1c2a-139">Configure for macOS with Jamf</span></span>](configure-microsoft-edge-on-mac-jamf.md)
- [<span data-ttu-id="d1c2a-140">Configurar para Windows</span><span class="sxs-lookup"><span data-stu-id="d1c2a-140">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="d1c2a-141">Configurar para Windows con Intune</span><span class="sxs-lookup"><span data-stu-id="d1c2a-141">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)