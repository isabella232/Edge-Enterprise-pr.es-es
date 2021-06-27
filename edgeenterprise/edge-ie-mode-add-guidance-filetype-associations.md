---
title: Asociar extensiones de archivo con el modo Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Asociar extensiones de archivo con el modo Internet Explorer
ms.openlocfilehash: c027b11e426cd665cb9e6cc25b4c9f66a0c6762a
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617460"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a><span data-ttu-id="10723-103">Asociar extensiones de archivos con el modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="10723-103">Associate file extensions with Internet Explorer mode</span></span>

>[!Note]
> <span data-ttu-id="10723-104">La aplicación de escritorio Internet Explorer 11 será retirada y dejará de recibir soporte el 15 de junio de 2022 (para ver una lista de lo que está en juego, [ consulte las preguntas frecuentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span><span class="sxs-lookup"><span data-stu-id="10723-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="10723-105">Las mismas aplicaciones y sitios de IE11 que use hoy pueden abrirse en Microsoft Edge con el modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="10723-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="10723-106">[Más información aquí](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span><span class="sxs-lookup"><span data-stu-id="10723-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="10723-107">En este artículo explica cómo asociar Microsoft Edge con el modo Internet Explorer con extensiones para aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="10723-107">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="10723-108">Este artículo se aplica a Microsoft Edge, versión 86 o posterior.</span><span class="sxs-lookup"><span data-stu-id="10723-108">This article applies to Microsoft Edge version 86 or later.</span></span>

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a><span data-ttu-id="10723-109">Instrucciones para la asociación de extensiones de archivo con el modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="10723-109">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="10723-110">Las instrucciones siguientes muestran una entrada que asocia Microsoft Edge con el modo IE con el tipo de archivo .mht.</span><span class="sxs-lookup"><span data-stu-id="10723-110">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="10723-111">Use los pasos siguientes como guía para configurar una asociación de archivos.</span><span class="sxs-lookup"><span data-stu-id="10723-111">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="10723-112">Se pueden establecer extensiones de archivos específicos para abrirlos en el modo Internet Explorer de forma predeterminada usando la directiva para **definir un archivo de configuración de asociaciones predeterminadas**.</span><span class="sxs-lookup"><span data-stu-id="10723-112">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="10723-113">Para obtener más información, consulte [Directiva CSP: ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="10723-113">For more information, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="10723-114">Defina un nuevo ProgID con el canal de Microsoft Edge para usarlo para abrirlo con el modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="10723-114">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="10723-115">El ProgID incluye el nombre y el icono de la aplicación, así como la ruta de acceso completa a msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="10723-115">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""
```

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"
```

2. <span data-ttu-id="10723-116">Configure las actualizaciones del shell para pasar la línea de comandos necesaria para abrir con el modo IE.</span><span class="sxs-lookup"><span data-stu-id="10723-116">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="10723-117">Por último, asocie la extensión de archivo .mht a un ProgID nuevo.</span><span class="sxs-lookup"><span data-stu-id="10723-117">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="10723-118">Agregue su ProgID como nombre de valor con el tipo de valor de REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="10723-118">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="10723-119">Después de asignar las claves descritas en el ejemplo anterior, los usuarios verán una opción adicional en el menú **Abrir con** para abrir un archivo .mht usando \<channel\> el modo IE de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="10723-119">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <a name="registry-example"></a><span data-ttu-id="10723-120">Registro de ejemplo</span><span class="sxs-lookup"><span data-stu-id="10723-120">Registry Example</span></span>

<span data-ttu-id="10723-121">Puede guardar el fragmento siguiente de código como un archivo .reg e importarlo en el registro.</span><span class="sxs-lookup"><span data-stu-id="10723-121">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

```markdown
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""

```

## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a><span data-ttu-id="10723-122">Configuración de tipos de archivo para abrir en el modo de Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="10723-122">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="10723-123">Al iniciar Edge 88, puede configurar determinados vínculos de tipos de archivos para que se abran en el modo de Internet Explorer mediante el [menú contextual Mostrar Directiva para abrir vínculos en el modo de Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).</span><span class="sxs-lookup"><span data-stu-id="10723-123">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).</span></span>

<span data-ttu-id="10723-124">Puede definir los tipos de archivo a los que se aplicará esta opción, especificando extensiones de archivo en esta directiva [abrir archivos locales en el modo Internet Explorer lista permitir extensión de archivo](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span><span class="sxs-lookup"><span data-stu-id="10723-124">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <a name="see-also"></a><span data-ttu-id="10723-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="10723-125">See also</span></span>

- [<span data-ttu-id="10723-126">Acerca del modo IE</span><span class="sxs-lookup"><span data-stu-id="10723-126">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="10723-127">Información de sitios configurables</span><span class="sxs-lookup"><span data-stu-id="10723-127">Configurable sites information</span></span>](./edge-learnmore-configurable-sites-ie-mode.md)
- [<span data-ttu-id="10723-128">Información adicional del modo de empresa</span><span class="sxs-lookup"><span data-stu-id="10723-128">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="10723-129">Configuración de asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="10723-129">Setting file type associations</span></span>](/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="10723-130">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="10723-130">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)