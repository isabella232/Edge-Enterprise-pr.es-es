---
title: Guía detallada de la directiva ExtensionSettings
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Guía de referencia detallada para configurar extensiones de Microsoft Edge mediante la directiva ExtensionSettings.
ms.openlocfilehash: 67e3cffaa842f591a3d4c3035104addd19e34fd8
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979962"
---
# <a name="detailed-guide-to-the-extensionsettings-policy"></a>Guía detallada de la directiva ExtensionSettings

Microsoft Edge ofrece varias formas de administrar extensiones. Una manera común es establecer varias directivas en un solo lugar con una cadena JSON en el Editor de directiva de grupo de Windows o en el Registro de Windows mediante la directiva [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="before-you-begin"></a>Antes de empezar

Decide si quiere establecer aquí toda la configuración de administración de extensiones o establecer estos controles a través de otras directivas.
  
La directiva ExtensionSettings puede sobrescribir otras directivas que haya establecido en otra parte de la directiva de grupo, incluidas las siguientes:

- [ExtensionAllowedTypes](/DeployEdge/microsoft-edge-policies#extensionallowedtypes)
- [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist)
- [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ExtensionInstallSources](/DeployEdge/microsoft-edge-policies#extensioninstallsources)
- [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallsources)

## <a name="extensionsettings-policy-fields"></a>Campos de directiva ExtensionSettings

Esta directiva puede controlar configuraciones, como la dirección URL de actualización, desde donde se descargará la extensión para la instalación inicial, y los permisos bloqueados, o qué permisos no se pueden ejecutar. Los campos de directiva disponibles se describen en la tabla siguiente.

| &nbsp; | Descripción |
|--|--|
| **allowed_types** | Solo se puede usar para configurar los valores predeterminados,*. Especifica los tipos de aplicaciones o extensiones que los usuarios pueden instalar en Microsoft Edge. El valor es una lista de cadenas, cada una de las cuales debe ser de uno de los siguientes tipos: "extension", "theme", "user_script", y "hosted_app".   |
| **blocked_install_message**| Si impide que los usuarios instalen determinadas extensiones, puede especificar un mensaje personalizado que se mostrará en el explorador si los usuarios intentan instalarlas.<br>Incorpore texto al mensaje de error genérico que se muestra en el sitio web de complementos de Microsoft Edge. Por ejemplo, puede indicar a los usuarios cómo ponerse en contacto con su departamento de TI o por qué una extensión determinada no está disponible. El mensaje puede tener hasta 1000 caracteres.   |
|**blocked_permissions**  | Impide que los usuarios instalen y ejecuten extensiones que soliciten determinados permisos de API que su organización no permite. Por ejemplo, puede bloquear las extensiones que tienen acceso a las cookies. Si una extensión requiere un permiso que bloqueó, el usuario no podrá instalarla. Si los usuarios instalaron previamente la extensión, ya no se cargará. Si una extensión contiene un permiso bloqueado como requisito opcional, se instala como de costumbre. Después, cuando se ejecuta la extensión, los permisos bloqueados se rechazan automáticamente.<br>Para obtener una lista de los permisos disponibles, vea [declarar permisos](/microsoft-edge/extensions-chromium/enterprise/declare-permissions).   |
| **installation_mode**| Controla si las extensiones especificadas se agregan a Microsoft Edge y cómo. Puede elegir cualquiera de las siguientes opciones para establecer el modo de instalación:<br>- allowed: Los usuarios pueden instalar la extensión. Si no se define ningún modo de instalación, esta configuración es la predeterminada.<br>- blocked: Los usuarios no pueden instalar la extensión.<br>- force_installed: Instalar automáticamente la extensión sin interacción del usuario. Los usuarios no pueden quitarla. También debe definir la ubicación de descarga de la extensión mediante update_url. **Nota**: No puede usar esta configuración con * porque Microsoft Edge no sabrá qué extensión instalar automáticamente.<br>- normal_installed: Instalar automáticamente la extensión sin interacción del usuario. Los usuarios pueden deshabilitarla. También debe definir la ubicación de descarga de la extensión mediante update_url. **Nota**: No puede usar esta configuración con * porque Microsoft Edge no sabrá qué extensión instalar automáticamente.<br>- removed: Los usuarios no pueden instalar la extensión. Si los usuarios instalaron previamente la extensión, Microsoft Edge la quita. |  |
| **install_sources** | Solo se puede usar para configurar los valores predeterminados,*. Especifica qué direcciones URL pueden instalar extensiones. Tanto la ubicación del archivo *.crx como la página desde la que se inicia la descarga (la de referencia) deben estar permitidas por estos patrones. Para obtener ejemplos de patrones de dirección URL, vea los [patrones de coincidencia](/microsoft-edge/extensions-chromium/enterprise/match-patterns).  |
| **minimum_version_required** |Microsoft Edge deshabilita las extensiones, incluidas las extensiones instaladas por la fuerza, con una versión anterior a la versión mínima especificada.<br>El formato de la cadena de versión es el mismo que el que se usa en el manifiesto de extensión.     |
| **update_url** | Only applies to force_installed and normal_installed. Especifica de dónde Microsoft Edge debe descargar una extensión. Si la extensión se hospeda en el sitio web de complementos de Microsoft Edge, use esta ubicación: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.<br>Microsoft Edge usa la dirección URL que especifique para la instalación inicial de la extensión. Para las actualizaciones de extensiones posteriores, Microsoft Edge usa la dirección URL en el manifiesto de la extensión.   |
| **runtime_allowed_hosts**| Permite que las extensiones interactúen con sitios web especificados, incluso si también se definen en runtime_blocked_hosts. Puede especificar hasta 100 entradas. Se descartan las entradas adicionales.<br>El formato del patrón de host es similar a [patrones de coincidencia](/microsoft-edge/extensions-chromium/enterprise/match-patterns) excepto en que no puede definir la ruta de acceso. Por ejemplo:<br>- *://*.example.com<br>- *://example.*: se admiten los caracteres comodín eTLD     |
| **runtime_blocked_hosts**| Impedir que las extensiones interactúen con los sitios web especificados o los modifiquen. Las modificaciones incluyen el bloqueo de la inserción de JavaScript, el acceso a cookies y las modificaciones de solicitudes web.<br>Puede especificar hasta 100 entradas. Se descartan las entradas adicionales.<br>El formato del patrón de host es similar a los patrones de coincidencia, salvo que no se puede definir la ruta de acceso. Por ejemplo:<br>- *://*.example.com<br>- *://example.*: se admiten los caracteres comodín eTLD   |
| **override_update_url**| Disponible desde edge 93<br>Si se establece en , Edge usa la dirección URL de actualización especificada en la directiva ExtensionSettings o en la directiva `true` ExtensionInstallForcelist, para actualizaciones de extensión posteriores.<br>Si no se establece o se establece en , Edge usa la dirección URL especificada en el manifiesto de la extensión `false` para actualizaciones.|


## <a name="configure-using-a-json-string-in-windows-group-policy-editor"></a>Configuración mediante una cadena JSON en el Editor de directivas de grupo de Windows

En los pasos para usar la directiva de configuración de extensiones mediante GPO se supone que ya ha importado ADM/ADMX para las directivas de Microsoft Edge.

1. Abra el editor de directivas de grupo y vaya a **Microsoft Edge > Extensiones > Configurar la directiva de configuración de administración de extensiones**.
2. Habilite la directiva y escriba sus datos de notación de objetos JavaScript (JSON) compacta en el cuadro de texto como una sola línea sin saltos de línea.
3. Para validar la directiva y compactarla en una sola línea, use una herramienta de compresión JSON.

### <a name="properly-format-json-for-the-extension-settings-policy"></a>JSON de formato correcto para la directiva de configuración de extensiones

Debe comprender las dos partes de esta directiva: el ámbito predeterminado y el ámbito individual. El ámbito predeterminado es uno genérico para las extensiones sin su propio ámbito. El ámbito individual solo se aplica solo a esa extensión.  

El ámbito predeterminado se identifica mediante el asterisco (*). En el ejemplo siguiente se define un ámbito predeterminado y un ámbito de extensión individual.

```json
{ 
   “*”: {}, 
   “nckgahadagoaajjgafhacjanaoiihapd”: {} 
} 
```

Una extensión solo obtendrá su configuración de un ámbito. Si hay un ámbito de extensión individual para esa extensión, será la configuración que se aplique a esa extensión. Si no existe ningún ámbito de extensión individual, la extensión usará el ámbito predeterminado.  

En el siguiente ejemplo de JSON se impide que cualquier extensión se ejecute en `.example.com` y se bloquea cualquier extensión que requiera el permiso "USB".

```json
{ 
  "*": { 
    "runtime_blocked_hosts": ["*://*.example.com"], 
    "blocked_permissions": ["usb"] 
  } 
} 
```

**JSON compacta**

```json
{"*":{"runtime_blocked_hosts":["*://*.example.com"],"blocked_permissions":["usb"]}} 
```

### <a name="a-few-more-json-examples-for-extension-settings"></a>Algunos ejemplos más de JSON para la configuración de extensiones

#### <a name="using-installation_mode-property-to-allow-and-block-extensions"></a>Uso de la propiedad installation_mode para permitir y bloquear extensiones

- El usuario puede instalar todas las extensiones; esta es la configuración predeterminada 

  `{ "*": {"installation_mode": "allowed" }}`
- El usuario no puede instalar ninguna extensión.  

  `{ "*": {"installation_mode": "blocked" }}`

- Especifique un mensaje personalizado para mostrar cuando se bloquee la instalación.

   `{"*": {"blocked_install_message": ["Call IT(408 - 555 - 1234) for an exception"]}}`

#### <a name="using-installation_mode-property-to-force-install-extensions"></a>Uso de la propiedad installation_mode para forzar la instalación de extensiones

Cuando se usa installation_mode como "force_installed", la extensión se instala automáticamente sin la interacción del usuario. Un usuario no puede deshabilitar ni quitar la extensión. Si se instala una extensión "normal" o "force", también se debe definir el campo **update_url**. Este campo indica la ubicación desde la que se puede instalar la extensión. Use las siguientes ubicaciones para el campo **update_url**:

- Si la extensión que está descargando está hospedada en la tienda de complementos de Microsoft Edge, use [https://edge.microsoft.com/extensionwebstorebase/v1/crx](https://edge.microsoft.com/extensionwebstorebase/v1/crx).
- Si la extensión que va a descargar está hospedada en Chrome Web Store, use [https://clients2.google.com/service/update2/crx](https://clients2.google.com/service/update2/crx).
- Si hospeda la extensión en su propio servidor, use la dirección URL donde Microsoft Edge puede descargar la extensión empaquetada (archivo .crx). Ejemplo de JSON:

   `{"nckgahadagoaajjgafhacjanaoiihapd": {"installation_mode": "force_installed","update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"}}`
  
En el ejemplo anterior, en lugar de "force_installed", si usa "normal_installed", la extensión se instala automáticamente sin interacción del usuario, pero pueden deshabilitar la extensión.  

   > [!TIP]
   > Dar formato a una cadena de JSON correctamente puede resultar complicado. Use un comprobador de JSON antes de implementar la directiva. También puede probar la versión anterior de la [herramienta Generador de configuración de extensiones](https://microsoft.github.io/edge-extension-settings-generator/minimal)

## <a name="configure-using-the-windows-registry"></a>Configurar mediante el registro de Windows

La directiva ExtensionSettings debe escribirse en el registro con esta clave:

`HKLM\Software\Policies\Microsoft\Edge\`

> [!NOTE]
> Es posible usar HKCU en lugar de HKLM. La ruta de acceso equivalente se puede configurar con el objeto de directiva de grupo (GPO).  

Para Microsoft Edge, toda la configuración se iniciará con esta clave:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\`

La siguiente clave que creará es el identificador de extensión para el ámbito individual o un asterisco (*) para el ámbito predeterminado. Por ejemplo, usaría la siguiente ubicación para la configuración que se aplica a Google Hangouts:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\nckgahadagoaajjgafhacjanaoiihapd`

Para la configuración que se aplica al ámbito predeterminado, use esta ubicación:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\*`

Una configuración diferente requerirá formatos diferentes, en función de si son una cadena o una matriz de cadenas. Los valores de matriz requieren ["value"]. Los valores de cadena se pueden escribir tal cual. En la lista siguiente se muestra qué valores son matrices o cadenas:

- Installation_mode = String
- update_url = String
- blocked_permissions = Array of strings
- allowed_permissions = Array of Strings
- minimum_version_required = String
- runtime_blocked_hosts = Array of strings
- runtime_allowed_hosts = Array of Strings
- blocked_install_message = String


## <a name="see-also"></a>Vea también

- [Administrar extensiones de Microsoft Edge en la empresa](microsoft-edge-manage-extensions.md)
- [Usar directivas de grupo para administrar extensiones de Microsoft Edge](microsoft-edge-manage-extensions-policies.md)
- [Preguntas más frecuentes sobre extensiones de Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
