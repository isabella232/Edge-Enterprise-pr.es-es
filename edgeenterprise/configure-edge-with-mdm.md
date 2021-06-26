---
title: Configurar Microsoft Edge con Administración de dispositivos móviles
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 04/06/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar Microsoft Edge con Administración de dispositivos móviles.
ms.openlocfilehash: a24e6d171707cdc02b6dbecb573e1238f1273426
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617610"
---
# <a name="configure-microsoft-edge-using-mobile-device-management"></a>Configurar Microsoft Edge con Administración de dispositivos móviles

En este artículo se explica cómo configurar Microsoft Edge en Windows 10 con [Administración de dispositivos móviles (MDM)](/windows/client-management/mdm/), mediante [Ingesta ADMX](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration). Este artículo describe también:

- Cómo [crear un identificador uniforme de recursos Open Mobile Alliance (OMA-URI) para directivas de Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).
- Cómo [configurar Microsoft Edge en Intune usando la ingesta ADMX y OMA-URI personalizado](#configure-microsoft-edge-in-intune-using-admx-ingestion).

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="prerequisites"></a>Requisitos previos

Windows 10, con los siguientes requisitos mínimos del sistema:

- Windows 10, versión 1903 con [KB4512941](https://support.microsoft.com/help/4512941/) y [KB4517211](https://support.microsoft.com/help/4517211/) instaladas
- Windows 10, versión 1809 con [KB4512534](https://support.microsoft.com/help/4512534/) y [KB4520062](https://support.microsoft.com/help/4520062/) instaladas
- Windows 10, versión 1803 con [KB4512509](https://support.microsoft.com/help/4512509/) y [KB4519978](https://support.microsoft.com/help/4519978) instaladas
- Windows 10, versión 1709 con [KB4516071](https://support.microsoft.com/help/4516071/) y [KB4520006](https://support.microsoft.com/help/4520006) instaladas

## <a name="overview"></a>Introducción

Puedes configurar Microsoft Edge en Windows 10 usando MDM con tu proveedor de administración de movilidad empresarial (EMM) o MDM preferido que admita [Ingesta ADMX](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).

La configuración de Microsoft Edge con MDM es un proceso de dos partes:

1. Ingestión del archivo ADMX de Microsoft Edge en el proveedor EMM o MDM. Consulta a tu proveedor para obtener instrucciones sobre cómo ingerir un archivo ADMX.

   > [!NOTE]
   > Para Microsoft Intune, consulta [Configurar Microsoft Edge en intune con la ingesta ADMX](#configure-microsoft-edge-in-intune-using-admx-ingestion).

2. [Creación de un OMA-URI para una directiva de Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).

## <a name="create-an-oma-uri-for-microsoft-edge-policies"></a>Crear un OMA-URI para directivas de Microsoft Edge

En las siguientes secciones se describe cómo crear la ruta de acceso OMA-URI y buscar y definir el valor en formato XML para las directivas de explorador obligatorias y recomendadas.

Antes de empezar, descarga el archivo de plantillas de directiva de Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) desde la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) y extrae el contenido.

Hay tres pasos para definir el OMA-URI:

1. [Crear la ruta OMA-URI](#create-the-oma-uri-path)
2. [Especificar el tipo de datos OMA-URI](#specify-the-data-type)
3. [Establecer el valor OMA-URI](#set-the-value-for-a-browser-policy)

### <a name="create-the-oma-uri-path"></a>Crear la ruta OMA-URI

Usa la fórmula siguiente como guía para crear las rutas de acceso OMA-URI. <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| Parámetro         | Descripción                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | Usa "Edge" o lo que hayas definido al ingerir la plantilla administrativa. Por ejemplo, si usaste "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", usa "MicrosoftEdge".<br/><br/> El `<ADMXIngestionName>` debe coincidir con lo usado al ingerir el archivo ADMX. |
| \<ADMXNamespace>  | "microsoft_edge" o "microsoft_edge_recommended", en función de si estás estableciendo una directiva obligatoria o recomendada. |
| \<ADMXCategory>   | La "parentCategory" de la directiva se define en el archivo ADMX. Omite la `<ADMXCategory>` si la directiva no está agrupada (no está definida "parentCategory"). |
| \<PolicyName>     | El nombre de la directiva se puede encontrar en el artículo [Referencia de directivas de explorador](./microsoft-edge-policies.md) . |

#### <a name="uri-path-example"></a>Ejemplos de rutas de URI:

Para este ejemplo, supongamos que el nodo `<ADMXIngestName>` se denominó “Edge" y que estás estableciendo una directiva obligatoria. La ruta de acceso URI sería:<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

Si la directiva no está en un grupo (por ejemplo, DiskCacheSize), quita "`~<ADMXCategory>`". Sustituye `<PolicyName>` por el nombre de la directiva, DiskCacheSize. La ruta URI sería:<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

Si la directiva está en un grupo, sigue estos pasos:

1. Abre **msedge.admx** con cualquier editor de xml.
2. Busca el nombre de la directiva que deseas establecer. Por ejemplo, "ExtensionInstallForceList".
3. Usa el valor del atributo *ref* del elemento *parentCategory*. Por ejemplo, "Extensiones" de \<parentCategory ref=" Extensions"/>.
4. Reemplaza `<ADMXCategory>` por el valor del atributo *ref* para crear la ruta URI. La ruta URI sería:<br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### <a name="specify-the-data-type"></a>Especificar el tipo de datos

El tipo de datos OMA-URI siempre es “String”.

### <a name="set-the-value-for-a-browser-policy"></a>Establecer el valor de una directiva de explorador

En esta sección se describe cómo establecer el valor en formato XML para cada tipo de datos. Ve a la [Referencia de directivas de explorador](./microsoft-edge-policies.md) para buscar el tipo de datos de la directiva.

> [!NOTE]
> Para los tipos de datos que no sean booleanos, el valor siempre comienza por `<enabled/>`.

#### <a name="boolean-data-type"></a>Tipo de datos booleano

Para las directivas que sean tipos booleanos, usa `<enabled/>` o `<disabled/>`.

#### <a name="integer-data-type"></a>Tipo de datos enteros

El valor siempre debe comenzar con el elemento `<enabled/>`, seguido de `<data id="[valueName]" value="[decimal value]"/>`.

Para buscar el nombre de valor y el valor decimal de una página de nueva pestaña, sigue los pasos siguientes:

1. Abre **msedge.admx** con cualquier editor de xml.
2. Busca el elemento `<policy>` en el que el atributo de nombre coincida con el nombre de directiva que deseas establecer. Para "RestoreOnStartup", busca `name="RestoreOnStartup"`.
3. En el nodo `<elements>`, busca el valor que quieras establecer.
4. Usa el valor en el atributo "valueName" del nodo `<elements>`. Para "RestoreOnStartup", "valueName" es "RestoreOnStartup".
5. Usa el valor del atributo "value" en el nodo `<decimal>`. Para que "RestoreOnStartup" abra la página de nueva pestaña, el valor es "5".

Para abrir la página de nueva pestaña en el inicio, usa:<br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### <a name="list-of-strings-data-type"></a>Lista de tipos de datos de cadena

El valor siempre debe comenzar con el elemento `<enabled/>`, seguido de `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.

> [!NOTE]
> El nombre de atributo "id=" no es el nombre de la directiva, incluso aunque en la mayoría de los casos coincida con el nombre de la directiva. Es el valor del atributo de id de nodo \<list>, que se encuentra en el archivo ADMX.

Para buscar el listID y definir el valor para bloquear una dirección URL, sigue estos pasos:

1. Abre **msedge.admx** con cualquier editor de xml.
2. Busca el elemento `<policy>` en el que el atributo de nombre coincida con el nombre de directiva que deseas establecer. Para "URLBlocklist", busca `name="URLBlocklist"`.
3. Usa el valor del atributo "id" del nodo `<list> node for [listID]`.
4. El "value" es una lista de direcciones URL separadas por punto y coma (;)

Por ejemplo, para bloquear el acceso a `contoso.com` y `https://ssl.server.com`:<br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### <a name="dictionary-or-string-data-type"></a>Diccionario de tipos de datos de cadena

El valor siempre debe comenzar por `<enabled/>`, seguido de `<data id="[textID]" value="[string]"/>`.

Para buscar el textID y definir el valor establecido para la configuración regional, sigue estos pasos:

1. Abre **msedge.admx** con cualquier editor de xml.
2. Busca el elemento `<policy>` en el que el atributo de nombre coincida con el nombre de directiva que deseas establecer. Para "ApplicationLocaleValue", busca `name="ApplicationLocaleValue"`.
3. Usa el valor del atributo "id" del nodo `<text>` para `[textID]`.
4. Establece el "valor" en el código de cultura.

Para establecer la configuración regional en "es-US" con la directiva "ApplicationLocaleValue":<br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### <a name="create-the-oma-uri-for-a-recommended-policies"></a>Crear el OMA-URI para una directiva recomendada

La definición de la ruta URI para las directivas recomendadas depende de la directiva que quieras configurar.

#### <a name="to-define-the-uri-path-for-a-recommended-policy"></a>Para definir la ruta URI para una directiva recomendada

Usa la fórmula de ruta URI (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) y los siguientes pasos para definir la ruta URI:

1. Abre **msedge.admx** con cualquier editor de xml.
2. Si la directiva que quieres configurar no está en un grupo, salta al paso 4 y quita `~<ADMXCategory>` de la ruta.
3. Si la directiva que deseas configurar está en un grupo:

   - Para buscar la `<ADMXCategory>`, busca la directiva que deseas establecer. Al buscar, añade al final "_recommended" al nombre de la directiva. Por ejemplo, una búsqueda de "RegisteredProtocolHandlers_recommended" presenta el siguiente resultado:

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - Copia el valor del atributo *ref* del elemento `<parentCategory>`. Para "ContentSettings", copia "ContentSettings_recommended" desde `<parentCategory ref=" ContentSettings_recommended"/>`.
   - Reemplaza `<ADMXCategory>` por el valor del atributo *ref* para crear la ruta URI en la fórmula de ruta URI.

4. El `<PolicyName>` es el nombre de la directiva con "_recommended" puesto al final.

#### <a name="oma-uri-path-examples-for-recommended-policies"></a>Ejemplos de ruta OMA-URI para directivas recomendadas

La siguiente tabla muestra ejemplos de rutas OMA-URI para las directivas recomendadas.

|              Directiva               |             OMA-URI                      |
|-----------------------------------|------------------------------------------|
| [RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [PasswordManagerEnabled](./microsoft-edge-policies.md#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [PrintHeaderFooter](./microsoft-edge-policies.md#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [HomePageLocation](./microsoft-edge-policies.md#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [ShowHomeButton](./microsoft-edge-policies.md#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### <a name="oma-uri-examples"></a>Ejemplos de OMA-URI

Ejemplos de OMA-URI con su ruta URI, tipo y un valor de ejemplo.

#### <a name="boolean-data-type-examples"></a>Ejemplos de tipo de datos booleano

*[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nombre    | Microsoft Edge: ShowHomeButton                                                       |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| tipo    | Cadena                                                                               |
| Valor   | `<enabled/>`                                                                          |

*[DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nombre    | Microsoft Edge: DefaultSearchProviderEnabled                                         |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| tipo    | Cadena                                                                               |
| Valor   | `<disable/>`                                                                          |

### <a name="integer-data-type-examples"></a>Ejemplos de tipo de datos enteros

*[AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nombre    | Microsoft Edge: AutoImportAtFirstRun                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| tipo    | Cadena                                                                               |
| Valor   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*[DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nombre    | Microsoft Edge: DefaultImagesSetting                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| tipo    | Cadena                                                                               |
| Valor   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*[DiskCacheSize](./microsoft-edge-policies.md#diskcachesize):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nombre    | Microsoft Edge: DiskCacheSize                                                        |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| tipo    | Cadena                                                                               |
| Valor   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### <a name="list-of-strings-data-type-examples"></a>Lista de ejemplos de tipos de datos de cadena
<!--
*[NotificationsAllowedForUrls](./microsoft-edge-policies.md#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                           |
-->
*[RestoreOnStartupURLS](./microsoft-edge-policies.md#restoreonstartupurls):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nombre    | Microsoft Edge: RestoreOnStartupURLS                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| Tipo    | Cadena                                                                               |
| Valor   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br>Para elementos de lista múltiples: `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nombre    | Microsoft Edge: ExtensionInstallForcelist                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| Tipo    | Cadena                                                                               |
| Valor   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### <a name="dictionary-and-string-data-type-example"></a>Ejemplo de diccionario y tipo de datos de cadena

*[ProxyMode](./microsoft-edge-policies.md#proxymode):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nombre    | Microsoft Edge: ProxyMode                                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| Tipo    | Cadena                                                                               |
| Valor   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## <a name="configure-microsoft-edge-in-intune-using-admx-ingestion"></a>Configurar Microsoft Edge en intune usando la ingesta ADMX

La manera recomendada de configurar Microsoft Edge con Microsoft Intune es usar el perfil de plantillas administrativas, tal y como se describe en [Configurar las opciones de la directiva de Microsoft Edge con Microsoft Intune](./configure-edge-with-intune.md)c Si deseas evaluar una directiva que actualmente no está disponible en las plantillas administrativas de Microsoft Edge en intune, puedes configurar Microsoft Edge usando una [configuración personalizada para dispositivos con Windows 10 en intune](/intune/configuration/custom-settings-windows-10).

Esta sección describe cómo:

1. [Ingerir el archivo ADMX de Microsoft Edge en Intune](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [Establecer una Directiva con OMA-URI personalizado en Intune](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> Como procedimiento recomendado, no uses un perfil OMA-URI personalizado y un perfil de plantillas de administración para configurar la misma opción de Microsoft Edge en Intune. Si implementas la misma directiva con un OMA-URI personalizado y un perfil de plantilla administrativa, pero con valores diferentes, los usuarios obtendrán resultados impredecibles. Te recomendamos encarecidamente que quites tu perfil de OMA-URI antes de usar un perfil de plantillas de administración.

### <a name="ingest-the-microsoft-edge-admx-file-into-intune"></a>Ingerir el archivo ADMX de Microsoft Edge en Intune

En esta sección se describe cómo ingerir la plantilla administrativa de Microsoft Edge (archivo **msedge.admx**) en Intune.

> [!WARNING]
> No modifiques el archivo ADMX antes de ingerir el archivo.

Para ingerir el archivo ADMX, sigue estos pasos:

1. Descarga el archivo de plantillas de directiva de Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) desde la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) y extrae el contenido. El archivo que quieres ingerir es **msedge.admx**.
2. Inicia sesión en [Microsoft Azure Portal](https://portal.azure.com).
3. Selecciona **Intune** desde _Todos los servicios_, o busca Intune en el cuadro de búsqueda del portal.
4. En _Microsoft Intune - Resumen_, selecciona **Configuración de dispositivos** | **Perfiles**.
5. En la barra de comandos superior, selecciona **+ Crear perfil**.

   ![Crear un perfil de dispositivo](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. Facilita la siguiente información de perfil:

   - **Nombre**: introduce un nombre descriptivo. Para este ejemplo, "Configuración ingerida de ADMX de Microsoft Edge".
   - **Descripción**: introduce una descripción opcional del perfil.
   - **Plataforma**: selecciona "Windows 10 y posteriores"
   - **Tipo de perfil**: Selecciona "Personalizado"

7. En **Configuración OMA-URI personalizada**, haz clic en **Agregar** para agregar una ingesta de ADMX.

   ![Agregar ingesta para OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. En **Agregar fila**, facilita la siguiente información:

   - **Nombre**: introduce un nombre descriptivo. Para este ejemplo, usa "Ingesta de ADMX de Microsoft Edge".
   - **Descripción**: introduce una descripción opcional de la opción.
   - **OMA-URI**: introduce "*./Device/Vendor/msft/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"
   - **Tipo de datos**: selecciona "Cadena"
   - **Valor**: este área de entrada aparece después de seleccionar el **Tipo de datos**. Abre el archivo msedge.admx desde el archivo de plantillas de directiva de Microsoft Edge que extrajiste en el paso 1. Copia **TODO el texto** desde el archivo msedge.admx y pégalo en el área de texto **Valor** que se muestra en la siguiente captura de pantalla.

        ![Agregar una ingesta de ADMX](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - Haz clic en **Aceptar**.

9. En **Configuración OMA-URI personalizada**, haz click en **Aceptar**.
10. En **Crear perfil**, haz clic en **Crear**. La siguiente captura de pantalla muestra información sobre el perfil recién creado.

    ![Información de nuevo perfil de dispositivo ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### <a name="set-a-policy-using-custom-oma-uri-in-intune"></a>Establecer una Directiva con OMA-URI personalizado en Intune

> [!NOTE]
> Antes de seguir los pasos de esta sección, debes completar los pasos descritos en [Ingerir el archivo ADMX de Microsoft Edge en Intune](#ingest-the-microsoft-edge-admx-file-into-intune).

1. Inicia sesión en [Microsoft Azure Portal](https://portal.azure.com).
2. Selecciona **Intune** desde _Todos los servicios_, o busca Intune en el cuadro de búsqueda del portal.
3. Ve a **Intune**>**Configuración de dispositivo**>**Perfiles**.
4. Selecciona el perfil "Configuración ingerida de ADMX de Microsoft Edge" o el nombre que usaste para el perfil.
5. Para agregar la configuración de directiva de Microsoft Edge, debes abrir **Configuración OMA-URI personalizada**. En **Administrar**, haz clic en **Propiedades** y luego haz clic en **Configuración**.

    ![Configurar opciones de perfil](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. En **Configuración OMA-URI personalizada**, haz clic en **Agregar**.

    ![Agregar fila a configuración OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. En **Agregar fila**, facilita la siguiente información:

   - **Nombre**: introduce un nombre descriptivo. Es recomendable usar el nombre de la directiva que quieres configurar. Para este ejemplo, usa "ShowHomeButton".
   - **Descripción** (opcional): introduce una descripción de la opción.
   - **OMA-URI**: introduce el OMA-URI para la directiva. Usando la directiva para "ShowHomeButton" como ejemplo, emplea esta cadena: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"
   - **Tipo de datos**: selecciona el tipo de datos de configuración de directiva. Para la directiva "ShowHomeButton", usa "Cadena"
   - **Valor**: especifica la opción que quieras configurar para la directiva. Para el ejemplo "ShowHomeButton", introduce "\<enabled/>". La siguiente captura de pantalla muestra las opciones para configurar una directiva.

        ![Agregar fila, configuración OMA-URI personalizada](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - Haz clic en **Aceptar**.

8. En **Configuración OMA-URI personalizada**, haz click en **Aceptar**.
9. En el perfil "**Configuración ingerida de ADMX de Microsoft Edge - Propiedades**" (o el nombre que hayas usado), haz clic en **Guardar**.

Después de crear el perfil y establecer las propiedades, tendrás que [asignar el perfil en Microsoft Intune](/intune/configuration/device-profile-assign).

#### <a name="confirm-that-the-policy-was-set"></a>Confirmar que se ha establecido la directiva

Usa los siguientes pasos para confirmar que la directiva de Microsoft Edge usa el perfil que has creado. (Deja tiempo a Microsoft Intune para propagar la directiva a un dispositivo que hayas asignado en el ejemplo de perfil "Configuración ingerida de ADMX de Microsoft Edge").

1. Abre Microsoft Edge y ve a *edge://policy*.
2. En la página **Directivas**, mira a ver si se enumera la directiva que estableciste en el perfil.
3. Si no aparece la directiva, consulta [Diagnosticar errores de MDM en Windows 10](/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) o [Solucionar problemas de configuración de directiva](#troubleshoot-a-policy-setting).

#### <a name="troubleshoot-a-policy-setting"></a>Solucionar problemas de configuración de directiva

Si una directiva de Microsoft Edge no surte efecto, sigue los pasos que se indican a continuación:

Abre la página *edge://policy* en el dispositivo de destino (un dispositivo al que asignaste el perfil en Microsoft Intune) y busca la directiva. Si la directiva no está en la página *edge://Policy*, intenta lo siguiente:

- Comprueba que la directiva esté en el Registro y que sea correcta. En el dispositivo de destino, abre el Editor del Registro de Windows 10 (**tecla Windows+ r**, introduce “*regedit*” y ,a continuación, presiona **Entrar**). Comprueba que la directiva esté definida correctamente en la ruta *\Software\Policies\ Microsoft\Edge*. Si no aparece la directiva en la ruta prevista, la directiva no se ha insertado correctamente en el dispositivo.
- Comprueba que la ruta OMA-URI sea correcta y que el valor sea una cadena XML válida. Si alguno de estos valores es incorrecto, la directiva no se insertará en el dispositivo de destino.

Para obtener más sugerencias sobre la solución de problemas, consulta [Configurar Microsoft Intune](/intune/fundamentals/setup-steps) y [Sincronizar dispositivos](/intune/remote-actions/device-sync).

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar la directiva de Microsoft Edge con Microsoft Intune](configure-edge-with-intune.md)
- [Administración de dispositivos móviles](/windows/client-management/mdm/)
- [Usar la configuración personalizada para dispositivos con Windows 10 en Intune](/intune/configuration/custom-settings-windows-10)
- [Configuración de directiva de aplicaciones de Win32 y Puente de dispositivo de escritorio](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [Descripción de las directivas respaldadas por ADMX](/windows/client-management/mdm/understanding-admx-backed-policies)