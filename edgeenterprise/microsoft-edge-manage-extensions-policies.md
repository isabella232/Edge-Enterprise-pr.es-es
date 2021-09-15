---
title: Usar directivas de grupo para administrar extensiones de Microsoft Edge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Usar directivas de grupo para administrar extensiones de Microsoft Edge en la empresa
ms.openlocfilehash: dad239a448ec1f0ebef60c7072bfaad5c3baed57
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11980241"
---
# <a name="use-group-policies-to-manage-microsoft-edge-extensions"></a>Usar directivas de grupo para administrar extensiones de Microsoft Edge

En este artículo se describen las opciones y los pasos para administrar extensiones mediante el uso de directivas de grupo. Estas opciones suponen que ya tiene Microsoft Edge administrado para los usuarios. Si aún no ha configurado Microsoft Edge para que se administre para los usuarios, siga el vínculo siguiente para hacerlo ahora.

- [Administrar extensiones de Microsoft Edge en la empresa](/deployedge/microsoft-edge-manage-extensions)

> [!NOTE]
> Este artículo aplica a Microsoft Edge, versión 77 o posterior.

## <a name="block-extensions-based-on-their-permissions"></a>Bloquear extensiones en función de sus permisos

Puede controlar qué extensiones pueden instalar los usuarios en función de los permisos mediante la directiva [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings). Si una extensión instalada necesita un permiso que se encuentra bloqueado, no se ejecutará. La extensión no se quita, solo se deshabilita.

> [!NOTE]
> El valor de permisos bloqueados solo se puede establecer dentro de la directiva de configuración de extensiones.  

Siga estos pasos como guía para bloquear una extensión.

1. Abra el editor de administración de directivas de grupo, vaya a **Plantillas administrativas > Microsoft Edge > Extensiones**  y, a continuación, seleccione **Configurar las opciones de administración de extensiones**.
2. Habilite la directiva y, a continuación, escriba los permisos que quiera permitir o bloquear, mediante una cadena JSON que se comprime. En la captura de pantalla siguiente se muestra cómo bloquear una extensión que usa el permiso "usb".

    :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-1.png" alt-text="Configure la directiva de grupo para bloquear una extensión.":::

En el ejemplo siguiente se muestra el código JSON para bloquear cualquier extensión que necesite el uso del permiso "usb" y su cadena comprimida.

### <a name="json-example"></a>Ejemplo de JSON

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
   > Para bloquear todas las extensiones que usan el permiso, use un asterisco para el id. de extensión, como se muestra en el ejemplo anterior. Si especifica un id. de extensión, la directiva solo se aplicará a esa extensión. Puede bloquear más de una, pero deben ser entradas independientes.

## <a name="prevent-extensions-from-altering-web-pages"></a>Impedir que las extensiones modifiquen páginas web

Este valor impide que las extensiones lean y cambien datos de sitios web y dominios confidenciales. El bloqueo de acciones no deseadas se realiza bloqueando acciones como la inserción de scripts en los sitios web, la lectura de las cookies o la realización de modificaciones de solicitudes web. Este valor no impide que los usuarios instalen o quiten extensiones, solo impide que las extensiones alteren los sitios web especificados. 
  
> [!NOTE]
> El valor de hosts permitidos/bloqueados en tiempo de ejecución solo se puede establecer dentro de la directiva de configuración de extensiones.  

Puede configurar las siguientes opciones en la directiva ExtensionSettings para evitar (o permitir) modificaciones de sitios web o dominios:

- **Runtime_blocked_hosts**. Este valor impide que las extensiones realicen cambios o lean datos de los sitios web que especifique.
- **Runtime_allowed_hosts**. Este valor permite que las extensiones realicen cambios o lean datos de los sitios web que especifique. El formato siguiente se usa para especificar los sitios en la cadena JSON de la directiva:

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` las secciones son obligatorias, pero la sección `[subdomain|*]` es opcional.

En la tabla siguiente se muestran ejemplos de patrones de host válidos y patrones coincidentes.

|Patrones de host válidos|Coincidencias|Sin coincidencias|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | Todas las direcciones URL  |   |

Siga estos pasos como guía para bloquear o permitir que las extensiones accedan a un sitio web o dominio.

1. Abra el editor de administración de directivas de grupo, vaya a **Plantillas administrativas > Microsoft Edge > Extensiones** y, a continuación, seleccione **Configurar las opciones de administración de extensiones**.  
2. Habilite la directiva y, a continuación, escriba los permisos que quiera permitir o bloquear, mediante la compresión de los permisos en una única cadena JSON.

En los ejemplos siguientes se muestra cómo bloquear extensiones en un nombre de host y cómo bloquear extensiones en el mismo dominio.

### <a name="json-example-to-block-hostname"></a>Ejemplo de JSON para bloquear el nombre de host

En este ejemplo se muestra la cadena JSON y JSON comprimida para bloquear que cualquier extensión acceda al nombre de host de `www.microsoft.com`.

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
> Para bloquear que todas las extensiones accedan a la página web, use un asterisco para el id. de extensión, como se muestra en el ejemplo anterior.  Si especifica un id. de extensión en lugar de un asterisco, la directiva solo se aplicará a esa extensión. Puede bloquear más de una extensión, pero deben ser entradas independientes.

### <a name="json-example-to-block-extensions-on-same-domain"></a>Ejemplo de JSON para bloquear extensiones en el mismo dominio

En este ejemplo se muestra la cadena JSON y JSON comprimida para bloquear que determinadas extensiones se ejecuten en el mismo dominio, "importantwebsite".

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

## <a name="allow-or-block-extensions-in-group-policy"></a>Permitir o bloquear extensiones en la directiva de grupo

Puede usar las directivas [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) y [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) para controlar qué extensiones están bloqueadas o permitidas. Siga estos pasos como guía para permitir todas las extensiones excepto las que desee bloquear.

1. Abra el editor de administración de directivas de grupo, vaya a **Plantillas administrativas > Microsoft Edge > Extensiones** y, a continuación, seleccione **Controlar qué extensiones no se pueden instalar**.
2. Seleccione **Habilitado**.
3. Haga clic en **Mostrar**.
4. Escriba el id. de la aplicación de las extensiones que desea bloquear. Al agregar varios id. de la aplicación, use una fila independiente para cada id.
5. Para bloquear todas las extensiones, escriba **\*** en la directiva para evitar que se instalen las extensiones. Puede usarlo junto con la directiva "Permitir que se instalen extensiones específicas" para permitir que solo se instalen determinadas extensiones. En la captura de pantalla siguiente se muestra una extensión que se bloqueará en función del id. de la aplicación proporcionado.

   :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-2.png" alt-text="Use el id. de la aplicación para bloquear una extensión.":::

   > [!TIP]
   > Si no encuentra el id. de la aplicación de una extensión, examine la extensión en el sitio web de complementos de Microsoft Edge. Busque la extensión específica y verá el id. de la aplicación al final de la dirección URL en el omnibox.

> [!NOTE]
> Puede agregar una extensión a la lista de bloqueados que ya está instalada en el equipo de un usuario. Esto deshabilitará la extensión e impedirá que el usuario la vuelva a habilitar. No se desinstalará, solo se deshabilitará.

## <a name="force-install-an-extension"></a>Forzar la instalación de una extensión

Use la directiva [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) para controlar qué extensiones están bloqueadas o permitidas. Siga estos pasos como guía para forzar la instalación de una extensión.

1. En el Editor de directiva de grupo, vaya a **Plantillas administrativas > Microsoft Edge > Extensiones >** y, a continuación, seleccione **Controlar qué extensiones se instalan de forma silenciosa**.
2. Seleccione **Habilitado**.  
3. Haga clic en **Mostrar**.
4. Escriba el id. de la aplicación o los id. de la extensión o extensiones que desea forzar la instalación.  

La extensión se instalará de forma silenciosa sin necesidad de interacción por parte del usuario. El usuario tampoco podrá desinstalar ni deshabilitar la extensión. Este valor sobrescribirá cualquier directiva de la lista de bloqueados que esté habilitada.

> [!NOTE]
> Para las extensiones hospedadas en el almacén web de Chrome, use una cadena como: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.

## <a name="block-extensions-from-a-specific-store-or-update-url"></a>Bloquear extensiones de un almacén específico o una dirección URL de actualización

Para bloquear extensiones de un almacén o dirección URL determinados, solo tiene que bloquear la *update_url* para ese almacén mediante la directiva [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).

Siga estos pasos como guía para bloquear extensiones de un almacén o una dirección URL determinados.

1. Abra el editor de administración de directivas de grupo, vaya a **Plantillas administrativas > Microsoft Edge > Extensiones** y, a continuación, seleccione **Configurar las opciones de administración de extensiones**.  
2. Habilite la directiva y, a continuación, escriba los permisos que desea permitir o bloquear, comprimiéndolos en una sola cadena JSON.

En el ejemplo siguiente se muestra la cadena JSON y JSON comprimida para bloquear desde Chrome Web Store mediante su dirección URL de actualización (`https://clients2.google.com/service/update2/crx`).

### <a name="json-example-for-blocking-on-update-url"></a>Ejemplo de JSON para bloquear la dirección URL de actualización

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
> Aún puede usar **ExtensionInstallForcelist** y **ExtensionInstallAllowlist** para permitir o forzar la instalación de extensiones específicas incluso si el almacén está bloqueado con el JSON del ejemplo anterior.

## <a name="see-also"></a>Consulte también

- [Administrar extensiones de Microsoft Edge en la empresa](microsoft-edge-manage-extensions.md)
- [Crear una tienda web para hospedar las extensiones de Microsoft Edge](microsoft-edge-manage-extensions-webstore.md)
- [Guía de referencia para la directiva ExtensionSettings](microsoft-edge-manage-extensions-ref-guide.md)
- [Preguntas más frecuentes sobre extensiones de Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
