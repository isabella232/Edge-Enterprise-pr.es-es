---
title: Usar directivas de grupo para administrar extensiones de Microsoft Edge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Usar directivas de grupo para administrar extensiones de Microsoft Edge en la empresa
ms.openlocfilehash: a633b036c1733716dfb257b4711bca57bd6721f0
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618276"
---
# <a name="use-group-policies-to-manage-microsoft-edge-extensions"></a><span data-ttu-id="bfc9d-103">Usar directivas de grupo para administrar extensiones de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bfc9d-103">Use group policies to manage Microsoft Edge extensions</span></span>

<span data-ttu-id="bfc9d-104">En este artículo se describen las opciones y los pasos para administrar extensiones mediante el uso de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-104">This article describes the options and steps for managing extensions by using group policies.</span></span> <span data-ttu-id="bfc9d-105">Estas opciones suponen que ya tiene Microsoft Edge administrado para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-105">These options  assume that you already have Microsoft Edge managed for your users.</span></span> <span data-ttu-id="bfc9d-106">Si aún no ha configurado Microsoft Edge para que se administre para los usuarios, siga el vínculo siguiente para hacerlo ahora.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-106">If you have not already set up Microsoft Edge to be managed for your users please follow the below link to do so now.</span></span>

- [<span data-ttu-id="bfc9d-107">Administrar extensiones de Microsoft Edge en la empresa</span><span class="sxs-lookup"><span data-stu-id="bfc9d-107">Manage Microsoft Edge extensions in the enterprise</span></span>](/deployedge/microsoft-edge-manage-extensions)

> [!NOTE]
> <span data-ttu-id="bfc9d-108">Este artículo aplica a Microsoft Edge, versión77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="block-extensions-based-on-their-permissions"></a><span data-ttu-id="bfc9d-109">Bloquear extensiones en función de sus permisos</span><span class="sxs-lookup"><span data-stu-id="bfc9d-109">Block extensions based on their permissions</span></span>

<span data-ttu-id="bfc9d-110">Puede controlar qué extensiones pueden instalar los usuarios en función de los permisos mediante la directiva [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).</span><span class="sxs-lookup"><span data-stu-id="bfc9d-110">You can control what extensions your users can install based on permissions using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span> <span data-ttu-id="bfc9d-111">Si una extensión instalada necesita un permiso que se encuentra bloqueado, no se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-111">If an installed extension needs a permission that’s blocked, it just won't run.</span></span> <span data-ttu-id="bfc9d-112">La extensión no se quita, solo se deshabilita.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-112">The extension isn't removed, just disabled.</span></span>

> [!NOTE]
> <span data-ttu-id="bfc9d-113">El valor de permisos bloqueados solo se puede establecer dentro de la directiva de configuración de extensiones.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-113">The blocked permissions setting can only be set within the extension settings policy.</span></span>  

<span data-ttu-id="bfc9d-114">Siga estos pasos como guía para bloquear una extensión.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-114">Use the following steps as a guide for blocking an extension.</span></span>

1. <span data-ttu-id="bfc9d-115">Abra el editor de administración de directivas de grupo, vaya a **Plantillas administrativas > Microsoft Edge > Extensiones**  y, a continuación, seleccione **Configurar las opciones de administración de extensiones**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-115">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**  and then select **Configure extension management settings**.</span></span>
2. <span data-ttu-id="bfc9d-116">Habilite la directiva y, a continuación, escriba los permisos que quiera permitir o bloquear, mediante una cadena JSON que se comprime.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-116">Enable the policy, then enter the permissions that you want allowed or blocked, by using a JSON string that gets compressed.</span></span> <span data-ttu-id="bfc9d-117">En la captura de pantalla siguiente se muestra cómo bloquear una extensión que usa el permiso "usb".</span><span class="sxs-lookup"><span data-stu-id="bfc9d-117">The next screenshot shows how to block an extension that uses the permission "usb".</span></span>

    :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-1.png" alt-text="Configure la directiva de grupo para bloquear una extensión.":::

<span data-ttu-id="bfc9d-119">En el ejemplo siguiente se muestra el código JSON para bloquear cualquier extensión que necesite el uso del permiso "usb" y su cadena comprimida.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-119">The following example shows the JSON to block any extension that needs the use of permission "usb" and its compressed string.</span></span>

### <a name="json-example"></a><span data-ttu-id="bfc9d-120">Ejemplo de JSON</span><span class="sxs-lookup"><span data-stu-id="bfc9d-120">JSON example</span></span>

   ```json
   { 
        "*": { 
             "blocked_permissions": ["usb"] 
        } 
   } 
   ```

   ```json
   {"*":{"blocked_permissions":["usb"]}} 
   ```

   > [!NOTE]
   > <span data-ttu-id="bfc9d-121">Para bloquear todas las extensiones que usan el permiso, use un asterisco para el id. de extensión, como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-121">To block all extensions that use the permission, use an asterisk for the extension ID, as shown in the previous example.</span></span> <span data-ttu-id="bfc9d-122">Si especifica un id. de extensión, la directiva solo se aplicará a esa extensión.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-122">If you specify one extension ID, the policy will only apply to that extension.</span></span> <span data-ttu-id="bfc9d-123">Puede bloquear más de una, pero deben ser entradas independientes.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-123">You can block more than one, but they need to be separate entries.</span></span>

## <a name="prevent-extensions-from-altering-web-pages"></a><span data-ttu-id="bfc9d-124">Impedir que las extensiones modifiquen páginas web</span><span class="sxs-lookup"><span data-stu-id="bfc9d-124">Prevent extensions from altering web pages</span></span>

<span data-ttu-id="bfc9d-125">Este valor impide que las extensiones lean y cambien datos de sitios web y dominios confidenciales.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-125">This setting prevents extensions from reading and changing  data from sensitive websites and domains.</span></span> <span data-ttu-id="bfc9d-126">El bloqueo de acciones no deseadas se realiza bloqueando acciones como la inserción de scripts en los sitios web, la lectura de las cookies o la realización de modificaciones de solicitudes web.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-126">Blocking unwanted actions is done by blocking actions such as script injection into your websites, reading the cookies, or making web-request modifications.</span></span> <span data-ttu-id="bfc9d-127">Este valor no impide que los usuarios instalen o quiten extensiones, solo impide que las extensiones alteren los sitios web especificados.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-127">This setting doesn’t prevent your users from installing or removing extensions, it only prevents extensions from altering the specified websites.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bfc9d-128">El valor de hosts permitidos/bloqueados en tiempo de ejecución solo se puede establecer dentro de la directiva de configuración de extensiones.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-128">The Runtime allowed/blocked hosts setting can only be set within the extension settings policy.</span></span>  

<span data-ttu-id="bfc9d-129">Puede configurar las siguientes opciones en la directiva ExtensionSettings para evitar (o permitir) modificaciones de sitios web o dominios:</span><span class="sxs-lookup"><span data-stu-id="bfc9d-129">You can configure the following settings in the ExtensionSettings policy to prevent (or allow) alterations of websites or domains:</span></span>

- <span data-ttu-id="bfc9d-130">**Runtime_blocked_hosts**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-130">**Runtime_blocked_hosts**.</span></span> <span data-ttu-id="bfc9d-131">Este valor impide que las extensiones realicen cambios o lean datos de los sitios web que especifique.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-131">This setting blocks extensions from making changes or reading data from the websites you specify.</span></span>
- <span data-ttu-id="bfc9d-132">**Runtime_allowed_hosts**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-132">**Runtime_allowed_hosts**.</span></span> <span data-ttu-id="bfc9d-133">Este valor permite que las extensiones realicen cambios o lean datos de los sitios web que especifique.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-133">This setting allows extensions to make changes or read data from the websites you specify.</span></span> <span data-ttu-id="bfc9d-134">El formato siguiente se usa para especificar los sitios en la cadena JSON de la directiva:</span><span class="sxs-lookup"><span data-stu-id="bfc9d-134">The following format is used for specifying your site(s) in the JSON string in the policy:</span></span>

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` <span data-ttu-id="bfc9d-135">las secciones son obligatorias, pero la sección `[subdomain|*]` es opcional.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-135">sections are required, but `[subdomain|*]` section is optional.</span></span>

<span data-ttu-id="bfc9d-136">En la tabla siguiente se muestran ejemplos de patrones de host válidos y patrones coincidentes.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-136">The following table shows examples of valid host patterns and matching patterns.</span></span>

|<span data-ttu-id="bfc9d-137">Patrones de host válidos</span><span class="sxs-lookup"><span data-stu-id="bfc9d-137">Valid host patterns</span></span>|<span data-ttu-id="bfc9d-138">Coincidencias</span><span class="sxs-lookup"><span data-stu-id="bfc9d-138">Matches</span></span>|<span data-ttu-id="bfc9d-139">Sin coincidencias</span><span class="sxs-lookup"><span data-stu-id="bfc9d-139">Doesn't match</span></span>|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | <span data-ttu-id="bfc9d-140">Todas las direcciones URL</span><span class="sxs-lookup"><span data-stu-id="bfc9d-140">All URLs</span></span>  |   |

<span data-ttu-id="bfc9d-141">Siga estos pasos como guía para bloquear o permitir que las extensiones accedan a un sitio web o dominio.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-141">Use the following steps as a guide to block or allow extensions to access a website or domain.</span></span>

1. <span data-ttu-id="bfc9d-142">Abra el editor de administración de directivas de grupo, vaya a **Plantillas administrativas > Microsoft Edge > Extensiones** y, a continuación, seleccione **Configurar las opciones de administración de extensiones**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-142">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**, and then select **Configure extension management settings**.</span></span>  
2. <span data-ttu-id="bfc9d-143">Habilite la directiva y, a continuación, escriba los permisos que quiera permitir o bloquear, mediante la compresión de los permisos en una única cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-143">Enable the policy, then enter the permissions that you want allowed or blocked, compressing the permissions to a single JSON string.</span></span>

<span data-ttu-id="bfc9d-144">En los ejemplos siguientes se muestra cómo bloquear extensiones en un nombre de host y cómo bloquear extensiones en el mismo dominio.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-144">The following examples show how to block extensions on a hostname and how to block extensions on the same domain.</span></span>

### <a name="json-example-to-block-hostname"></a><span data-ttu-id="bfc9d-145">Ejemplo de JSON para bloquear el nombre de host</span><span class="sxs-lookup"><span data-stu-id="bfc9d-145">JSON example to block hostname</span></span>

<span data-ttu-id="bfc9d-146">En este ejemplo se muestra la cadena JSON y JSON comprimida para bloquear que cualquier extensión acceda al nombre de host de `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-146">This example shows the JSON and compressed JSON string to block any extension from accessing the `www.microsoft.com` hostname.</span></span>

```json
{ 
    "*":{ 
            "runtime_blocked_hosts":["www.microsoft.com"] 
    } 
} 
```

```json
{"*":{"runtime_blocked_hosts":["www.microsoft.com"]}} 
```

> [!NOTE]
> <span data-ttu-id="bfc9d-147">Para bloquear que todas las extensiones accedan a la página web, use un asterisco para el id. de extensión, como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-147">To block all extensions from accessing a webpage, use an asterisk for the extension ID, as shown in the previous example.</span></span>  <span data-ttu-id="bfc9d-148">Si especifica un id. de extensión en lugar de un asterisco, la directiva solo se aplicará a esa extensión.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-148">If you specify one extension ID instead of an asterisk, the policy will only apply to that extension.</span></span> <span data-ttu-id="bfc9d-149">Puede bloquear más de una extensión, pero deben ser entradas independientes.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-149">You can block more than one extension, but they need to be separate entries.</span></span>

### <a name="json-example-to-block-extensions-on-same-domain"></a><span data-ttu-id="bfc9d-150">Ejemplo de JSON para bloquear extensiones en el mismo dominio</span><span class="sxs-lookup"><span data-stu-id="bfc9d-150">JSON example to block extensions on same domain</span></span>

<span data-ttu-id="bfc9d-151">En este ejemplo se muestra la cadena JSON y JSON comprimida para bloquear que determinadas extensiones se ejecuten en el mismo dominio, "importantwebsite".</span><span class="sxs-lookup"><span data-stu-id="bfc9d-151">This example shows the JSON and compressed JSON string to block specific extensions from running on the same domain, "importantwebsite".</span></span>

```json
{ 
    "aapbdbdomjkkjkaonfhkkikfgjllcleb": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    }, 
    "bfbmjmiodbnnpllbbbfblcplfjjepjdn": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    } 
} 
```

```json
{"aapbdbdomjkkjkaonfhkkikfgjllcleb": {"runtime_blocked_hosts": ["*://,*.importantwebsite"]},"bfbmjmiodbnnpllbbbfblcplfjjepjdn": {"runtime_blocked_hosts": ["*://*.importantwebsite"]}} 
```

## <a name="allow-or-block-extensions-in-group-policy"></a><span data-ttu-id="bfc9d-152">Permitir o bloquear extensiones en la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="bfc9d-152">Allow or block extensions in group policy</span></span>

<span data-ttu-id="bfc9d-153">Puede usar las directivas [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) y [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) para controlar qué extensiones están bloqueadas o permitidas.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-153">You can use the [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) and [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) policies to control which extensions are blocked or allowed.</span></span> <span data-ttu-id="bfc9d-154">Siga estos pasos como guía para permitir todas las extensiones excepto las que desee bloquear.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-154">Use the following steps as a guide to allow all extensions except those you want to block.</span></span>

1. <span data-ttu-id="bfc9d-155">Abra el editor de administración de directivas de grupo, vaya a **Plantillas administrativas > Microsoft Edge > Extensiones** y, a continuación, seleccione **Controlar qué extensiones no se pueden instalar**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-155">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions >** and then select **Control which extensions cannot be installed**.</span></span>
2. <span data-ttu-id="bfc9d-156">Seleccione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-156">Select **Enabled**.</span></span>
3. <span data-ttu-id="bfc9d-157">Haga clic en **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-157">Click **Show**.</span></span>
4. <span data-ttu-id="bfc9d-158">Escriba el id. de la aplicación de las extensiones que desea bloquear.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-158">Enter the app ID of the extensions that you want to block.</span></span> <span data-ttu-id="bfc9d-159">Al agregar varios id. de la aplicación, use una fila independiente para cada id.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-159">When adding multiple app ID’s use a separate row for each ID.</span></span>
5. <span data-ttu-id="bfc9d-160">Para bloquear todas las extensiones, escriba **\*** en la directiva para evitar que se instalen las extensiones.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-160">To block all extensions, type **\*** into the policy to prevent any extensions from being installed.</span></span> <span data-ttu-id="bfc9d-161">Puede usarlo junto con la directiva "Permitir que se instalen extensiones específicas" para permitir que solo se instalen determinadas extensiones.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-161">You can use this in conjunction with the "Allow specific extensions to be installed" policy to only allow certain extensions to be installed.</span></span> <span data-ttu-id="bfc9d-162">En la captura de pantalla siguiente se muestra una extensión que se bloqueará en función del id. de la aplicación proporcionado.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-162">The next screenshot shows an extension that will be blocked based on the app ID that's provided.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-2.png" alt-text="Use el id. de la aplicación para bloquear una extensión.":::

   > [!TIP]
   > <span data-ttu-id="bfc9d-164">Si no encuentra el id. de la aplicación de una extensión, examine la extensión en el sitio web de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-164">If you can’t find the app ID of an extension, look at the extension in the Microsoft Edge Add-ons website.</span></span> <span data-ttu-id="bfc9d-165">Busque la extensión específica y verá el id. de la aplicación al final de la dirección URL en el omnibox.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-165">Find the specific extension and you will see the app ID at the end of the URL in the omnibox.</span></span>

> [!NOTE]
> <span data-ttu-id="bfc9d-166">Puede agregar una extensión a la lista de bloqueados que ya está instalada en el equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-166">You can add an extension to the blocklist that’s already installed on a user’s computer.</span></span> <span data-ttu-id="bfc9d-167">Esto deshabilitará la extensión e impedirá que el usuario la vuelva a habilitar.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-167">This will disable the extension and prevent the user from re-enabling it.</span></span> <span data-ttu-id="bfc9d-168">No se desinstalará, solo se deshabilitará.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-168">It won't be uninstalled, just disabled.</span></span>

## <a name="force-install-an-extension"></a><span data-ttu-id="bfc9d-169">Forzar la instalación de una extensión</span><span class="sxs-lookup"><span data-stu-id="bfc9d-169">Force-install an extension</span></span>

<span data-ttu-id="bfc9d-170">Use la directiva [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) para controlar qué extensiones están bloqueadas o permitidas.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-170">Use the [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) policy to control which extensions are blocked or allowed.</span></span> <span data-ttu-id="bfc9d-171">Siga estos pasos como guía para forzar la instalación de una extensión.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-171">Use the following steps as a guide to force-install an extension.</span></span>

1. <span data-ttu-id="bfc9d-172">En el Editor de directiva de grupo, vaya a **Plantillas administrativas > Microsoft Edge > Extensiones >** y, a continuación, seleccione **Controlar qué extensiones se instalan de forma silenciosa**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-172">In the Group Policy Editor, go to **Administrative Templates> Microsoft Edge >  Extensions >** and then select **Control which extensions are installed silently**.</span></span>
2. <span data-ttu-id="bfc9d-173">Seleccione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-173">Select **Enabled**.</span></span>  
3. <span data-ttu-id="bfc9d-174">Haga clic en **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-174">Click **Show**.</span></span>
4. <span data-ttu-id="bfc9d-175">Escriba el id. de la aplicación o los id. de la extensión o extensiones que desea forzar la instalación.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-175">Enter the app ID or IDs of the extension or extensions you want to force-install.</span></span>  

<span data-ttu-id="bfc9d-176">La extensión se instalará de forma silenciosa sin necesidad de interacción por parte del usuario.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-176">The extension will be installed silently with no need for user interaction.</span></span> <span data-ttu-id="bfc9d-177">El usuario tampoco podrá desinstalar ni deshabilitar la extensión.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-177">The user also won’t be able to uninstall or disable the extension.</span></span> <span data-ttu-id="bfc9d-178">Este valor sobrescribirá cualquier directiva de la lista de bloqueados que esté habilitada.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-178">This setting will overwrite over any blocklist policy that’s enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="bfc9d-179">Para las extensiones hospedadas en el almacén web de Chrome, use una cadena como: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-179">For extensions hosted in the Chrome web store use a string such as: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.</span></span>

## <a name="block-extensions-from-a-specific-store-or-update-url"></a><span data-ttu-id="bfc9d-180">Bloquear extensiones de un almacén específico o una dirección URL de actualización</span><span class="sxs-lookup"><span data-stu-id="bfc9d-180">Block extensions from a specific store or update URL</span></span>

<span data-ttu-id="bfc9d-181">Para bloquear extensiones de un almacén o dirección URL determinados, solo tiene que bloquear la *update_url* para ese almacén mediante la directiva [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).</span><span class="sxs-lookup"><span data-stu-id="bfc9d-181">To block extensions from a particular store or URL, you only need to block the *update_url* for that store using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span>

<span data-ttu-id="bfc9d-182">Siga estos pasos como guía para bloquear extensiones de un almacén o una dirección URL determinados.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-182">Use the following steps as a guide to block extensions from an particular store or URL.</span></span>

1. <span data-ttu-id="bfc9d-183">Abra el editor de administración de directivas de grupo, vaya a **Plantillas administrativas > Microsoft Edge > Extensiones** y, a continuación, seleccione **Configurar las opciones de administración de extensiones**.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-183">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions >** and then select **Configure extension management settings**.</span></span>  
2. <span data-ttu-id="bfc9d-184">Habilite la directiva y, a continuación, escriba los permisos que desea permitir o bloquear, comprimiéndolos en una sola cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-184">Enable the policy, then enter the permissions that you want allowed or blocked, compressing it to a single JSON string.</span></span>

<span data-ttu-id="bfc9d-185">En el ejemplo siguiente se muestra la cadena JSON y JSON comprimida para bloquear desde Chrome Web Store mediante su dirección URL de actualización (`https://clients2.google.com/service/update2/crx`).</span><span class="sxs-lookup"><span data-stu-id="bfc9d-185">The next example shows the JSON and compressed JSON string to block from the Chrome Web Store using its update URL (`https://clients2.google.com/service/update2/crx`).</span></span>

### <a name="json-example-for-blocking-on-update-url"></a><span data-ttu-id="bfc9d-186">Ejemplo de JSON para bloquear la dirección URL de actualización</span><span class="sxs-lookup"><span data-stu-id="bfc9d-186">JSON example for blocking on update URL</span></span>

```json
{ 
"update_url:https://clients2.google.com/service/update2/crx":{ 
                                                             " installation_mode":"blocked" 
                                                             } 
} 
```

```json
{"update_url:https://clients2.google.com/service/update2/crx":{"installation_mode":"blocked"}} 
```

> [!NOTE]
> <span data-ttu-id="bfc9d-187">Aún puede usar **ExtensionInstallForcelist** y **ExtensionInstallAllowlist** para permitir o forzar la instalación de extensiones específicas incluso si el almacén está bloqueado con el JSON del ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="bfc9d-187">You can still use **ExtensionInstallForceList** and **ExtensionInstallAllowList** to allow/force install specific extensions even if the store is blocked using the JSON in the previous example.</span></span>

## <a name="see-also"></a><span data-ttu-id="bfc9d-188">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bfc9d-188">See also</span></span>

- [<span data-ttu-id="bfc9d-189">Administrar extensiones de Microsoft Edge en la empresa</span><span class="sxs-lookup"><span data-stu-id="bfc9d-189">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="bfc9d-190">Crear una tienda web para hospedar las extensiones de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bfc9d-190">Create a web store to host Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-webstore.md)
- [<span data-ttu-id="bfc9d-191">Guía de referencia para la directiva ExtensionSettings</span><span class="sxs-lookup"><span data-stu-id="bfc9d-191">Reference guide for the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="bfc9d-192">Preguntas más frecuentes sobre extensiones de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bfc9d-192">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="bfc9d-193">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="bfc9d-193">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
