---
title: Asociar extensiones de archivo con el modo Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Asociar extensiones de archivo con el modo Internet Explorer
ms.openlocfilehash: 6c651499401757d9a58e697d1d019a7294bb5fa7
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447374"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a><span data-ttu-id="617f7-103">Asociar extensiones de archivo con el modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="617f7-103">Associate file extensions with Internet Explorer mode</span></span>

<span data-ttu-id="617f7-104">En este artículo explica cómo asociar Microsoft Edge con el modo Internet Explorer con extensiones para aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="617f7-104">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="617f7-105">Este artículo se aplica a Microsoft Edge, versión 86 o posterior.</span><span class="sxs-lookup"><span data-stu-id="617f7-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a><span data-ttu-id="617f7-106">Instrucciones para la asociación de extensiones de archivo con el modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="617f7-106">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="617f7-107">Las instrucciones siguientes muestran una entrada que asocia Microsoft Edge con el modo IE con el tipo de archivo .mht.</span><span class="sxs-lookup"><span data-stu-id="617f7-107">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="617f7-108">Use los pasos siguientes como guía para configurar una asociación de archivos.</span><span class="sxs-lookup"><span data-stu-id="617f7-108">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="617f7-109">Se pueden establecer extensiones de archivos específicos para abrirlos en el modo Internet Explorer de forma predeterminada usando la directiva para **definir un archivo de configuración de asociaciones predeterminadas**.</span><span class="sxs-lookup"><span data-stu-id="617f7-109">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="617f7-110">Para obtener más información, consulte [Directiva CSP: ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="617f7-110">For more information, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="617f7-111">Defina un nuevo ProgID con el canal de Microsoft Edge para usarlo para abrirlo con el modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="617f7-111">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="617f7-112">El ProgID incluye el nombre y el icono de la aplicación, así como la ruta de acceso completa a msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="617f7-112">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="617f7-113">Configure las actualizaciones del shell para pasar la línea de comandos necesaria para abrir con el modo IE.</span><span class="sxs-lookup"><span data-stu-id="617f7-113">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="617f7-114">Por último, asocie la extensión de archivo .mht a un ProgID nuevo.</span><span class="sxs-lookup"><span data-stu-id="617f7-114">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="617f7-115">Agregue su ProgID como nombre de valor con el tipo de valor de REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="617f7-115">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="617f7-116">Después de asignar las claves descritas en el ejemplo anterior, los usuarios verán una opción adicional en el menú **Abrir con** para abrir un archivo .mht usando \<channel\> el modo IE de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="617f7-116">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <a name="registry-example"></a><span data-ttu-id="617f7-117">Registro de ejemplo</span><span class="sxs-lookup"><span data-stu-id="617f7-117">Registry Example</span></span>

<span data-ttu-id="617f7-118">Puede guardar el fragmento siguiente de código como un archivo .reg e importarlo en el registro.</span><span class="sxs-lookup"><span data-stu-id="617f7-118">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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
## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a><span data-ttu-id="617f7-119">Configuración de tipos de archivo para abrir en el modo de Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="617f7-119">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="617f7-120">Al iniciar Edge 88, puede configurar determinados vínculos de tipos de archivos para que se abran en el modo de Internet Explorer mediante el [menú contextual Mostrar Directiva para abrir vínculos en el modo de Internet Explorer](./microsoft-edge-policies.md#show-context-menu-to-open-a-link-in-internet-explorer-mode).</span><span class="sxs-lookup"><span data-stu-id="617f7-120">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](./microsoft-edge-policies.md#show-context-menu-to-open-a-link-in-internet-explorer-mode).</span></span> 

<span data-ttu-id="617f7-121">Puede definir los tipos de archivo a los que se aplicará esta opción, especificando extensiones de archivo en esta directiva [abrir archivos locales en el modo Internet Explorer lista permitir extensión de archivo](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span><span class="sxs-lookup"><span data-stu-id="617f7-121">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <a name="see-also"></a><span data-ttu-id="617f7-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="617f7-122">See also</span></span>

- [<span data-ttu-id="617f7-123">Acerca del modo IE</span><span class="sxs-lookup"><span data-stu-id="617f7-123">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="617f7-124">Información de sitios configurables</span><span class="sxs-lookup"><span data-stu-id="617f7-124">Configurable sites information</span></span>](./edge-learnmore-configurable-sites-ie-mode.md)
- [<span data-ttu-id="617f7-125">Información adicional del modo de empresa</span><span class="sxs-lookup"><span data-stu-id="617f7-125">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="617f7-126">Configuración de asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="617f7-126">Setting file type associations</span></span>](/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="617f7-127">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="617f7-127">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)