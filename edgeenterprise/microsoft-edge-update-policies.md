---
title: Documentación de directiva de Microsoft Edge Update
ms.author: stmoody
author: AndreaLBarr
manager: tahills
ms.date: 07/23/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentación de todas las directivas admitidas por Microsoft Edge Update
ms.openlocfilehash: 9c7eca4d5bdd7c87bea141a422dce3b17f22067c
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11980081"
---
# <a name="microsoft-edge---update-policies"></a>Microsoft Edge: Directivas de actualización

La última versión de Microsoft Edge incluye las siguientes directivas que puedes usar para controlar cómo y cuándo se actualiza Microsoft Edge.

Para obtener información sobre otras directivas disponibles en Microsoft Edge, consulta la [referencia de directiva del explorador Microsoft Edge](microsoft-edge-policies.md)
> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.
## <a name="available-policies"></a>Directivas disponibles
Estas tablas enumeran todas las directivas de grupo relacionadas con la actualización disponibles en esta versión de Microsoft Edge. Usa los vínculos de la tabla para obtener más detalles sobre directivas específicas.

|&nbsp;|&nbsp;| |**-**|-| |**[Aplicaciones](#applications)**|[Preferencias](#preferences)| |**[Servidor proxy](#proxy-server)**|[Vista web de Microsoft Edge](#microsoft-edge-webview)|
### [<a name="applications"></a>Aplicaciones](#applications-policies)
|Nombre de directiva|Título|
|-|-|
|[InstallDefault](#installdefault)|Valor predeterminado de Permitir instalación|
|[UpdateDefault](#updatedefault)|Valor predeterminado de Invalidar directiva de actualización|
|[Instalar](#install)|Permitir instalación (por canal)|
|[Actualizar](#update)|Invalidar directiva de actualización (por canal)|
|[Allowsxs](#allowsxs)|Permitir la experiencia de exploradores Microsoft Edge en paralelo|
|[CreateDesktopShortcutDefault](#createdesktopshortcutdefault)|Impedir la creación de accesos directos de escritorio durante la instalación predeterminada|
|[CreateDesktopShortcut](#createdesktopshortcut)|Impedir la creación de accesos directos de escritorio durante la instalación (por canal)|
|[RollbackToTargetVersion](#rollbacktotargetversion)|Revertir a la versión de destino (por canal)|
|[TargetVersionPrefix](#targetversionprefix)|Invalidación de versión de destino (por canal)|
|[UpdaterExperimentationAndConfigurationServiceControl](#UpdaterExperimentationAndConfigurationServiceControl)| Recuperar configuraciones y experimentos|
### [<a name="preferences"></a>Preferencias](#preferences-policies)
|Nombre de directiva|Título|
|-|-|
|[AutoUpdateCheckPeriodMinutes](#autoupdatecheckperiodminutes)|invalidar el período de buscar actualizaciones automáticas|
|[UpdatesSuppressed](#updatessuppressed)|Período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas|

### [<a name="proxy-server"></a>Servidor proxy](#proxy-server-policies)
|Nombre de directiva|Leyenda|
|-|-|
|[ProxyMode](#proxymode)|Elegir cómo especificar la configuración del servidor proxy|
|[ProxyPacUrl](#proxypacurl)|Dirección URL a un archivo proxy .pac|
|[ProxyServer](#proxyserver)|Dirección o dirección URL del servidor proxy|

### [<a name="microsoft-edge-webview"></a>Microsoft Edge WebView](#microsoft-edge-webview-policies)
|Nombre de directiva|Título|
|-|-|
|[Instalar](#install-webview)|Permitir instalación|
|[Actualización](#update-webview)|Invalidar directiva de actualización|

## <a name="applications-policies"></a>Directivas de aplicaciones

[Volver al principio](#microsoft-edge---update-policies)
### <a name="installdefault"></a>InstallDefault
#### <a name="allow-installation-default"></a>Valor predeterminado de Permitir instalación
>Microsoft Edge Update 1.2.145.5 y posteriores

#### <a name="description"></a>Descripción
Puede especificar el comportamiento predeterminado de todos los canales para permitir o bloquear Microsoft Edge en dispositivos unidos al dominio.

Puede reemplazar esta directiva para canales individuales si habilita la directiva [Permitir instalación](#install) para canales específicos.

Si deshabilita esta directiva, se bloquea la instalación de Microsoft Edge. Esto solo afecta a la instalación de software de Microsoft Edge cuando la directiva "[Permitir instalación](#install)" está establecida en No configurada.

Esta directiva no impide que se ejecute Microsoft Edge Update ni impide que los usuarios instalen software de Microsoft Edge con otros métodos.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: InstallDefault
- Nombre de GP: valor predeterminado de Permitir instalación
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre de valor: InstallDefault
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000001
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="updatedefault"></a>UpdateDefault
#### <a name="update-policy-override-default"></a>Valor predeterminado de Invalidar directiva de actualización
>Microsoft Edge Update 1.2.145.5 y posteriores

#### <a name="description"></a>Descripción
Permite especificar el comportamiento predeterminado de todos los canales relacionados con la manera en que Microsoft Edge Update trata las actualizaciones disponibles para Microsoft Edge. Se puede invalidar para canales individuales especificando la directiva '[Invalidar directiva de actualización](#update)' para esos canales específicos.

  Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge de acuerdo con la configuración de las siguientes opciones:
   - Permitir siempre las actualizaciones: las actualizaciones siempre se aplican cuando se encuentran, ya sea mediante la búsqueda de actualizaciones periódicas o mediante una búsqueda de actualizaciones manual.
   - Solo actualizaciones silenciosas automáticas: las actualizaciones solo se aplican cuando las encuentra la búsqueda periódica de actualizaciones.
   - Solo actualizaciones manuales: las actualizaciones se aplican solo cuando el usuario ejecuta una búsqueda manual de actualizaciones.
   - Actualizaciones deshabilitadas: las actualizaciones nunca se aplican.

  Si seleccionas las actualizaciones manuales, asegúrate de buscar periódicamente actualizaciones mediante el mecanismo de actualización manual de la aplicación, si está disponible. Si deshabilitas las actualizaciones, comprueba periódicamente si las hay y distribúyelas a los usuarios.

  Si no habilitas ni configuras esta directiva, Microsoft Edge Update administra las actualizaciones disponibles según se especifica en la directiva '[Invalidar directiva de actualizaciones](#update)'.

  Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: UpdateDefault
- Nombre de GP: Valor predeterminado de Invalidar directiva de actualización
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre de valor: UpdateDefault
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000003
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="install"></a>Instalar
#### <a name="allow-installation"></a>Permitir instalación
>Microsoft Edge Update 1.2.145.5 y posteriores

#### <a name="description"></a>Descripción
Especifica si se puede instalar un canal de Microsoft Edge en dispositivos unidos al dominio.

  Si habilita esta directiva para un canal, no se bloqueará la instalación de Microsoft Edge.

  Si deshabilita esta directiva para un canal, se bloqueará la instalación de Microsoft Edge.

  Si no configura esta directiva para un canal, la configuración de la directiva "[Valor predeterminado de Permitir instalación](#installdefault)" determinará si los usuarios pueden instalar dicho canal de Microsoft Edge.

  Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: Install
- Nombre de GP: Permitir instalación
- Ruta de GP: 
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: 
  - (Estable): instalar{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): instalar{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canarias): instalar{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): instalar{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000001
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="update"></a>Actualizar
#### <a name="update-policy-override"></a>Invalidar directiva de actualización
>Microsoft Edge Update 1.2.145.5 y posteriores

#### <a name="description"></a>Descripción
Especifica cómo trata Microsoft Edge Update las actualizaciones disponibles de Microsoft Edge.

Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge de acuerdo con la configuración de las siguientes opciones:
  - Permitir siempre las actualizaciones: las actualizaciones siempre se aplican cuando se encuentran, ya sea mediante la búsqueda de actualizaciones periódicas o mediante una búsqueda de actualizaciones manual.
  - Solo actualizaciones silenciosas automáticas: las actualizaciones solo se aplican cuando las encuentra la búsqueda periódica de actualizaciones.
  - Solo actualizaciones manuales: las actualizaciones se aplican solo cuando el usuario ejecuta una búsqueda manual de actualizaciones. (No todas las aplicaciones ofrecen una interfaz para esta opción).
  - Actualizaciones deshabilitadas: las actualizaciones nunca se aplican.

Si seleccionas las actualizaciones manuales, asegúrate de buscar periódicamente actualizaciones mediante el mecanismo de actualización manual de la aplicación, si está disponible. Si deshabilitas las actualizaciones, comprueba periódicamente si las hay y distribúyelas a los usuarios.

Si no habilitas ni configuras esta directiva, Microsoft Edge Update administra las actualizaciones disponibles según se especifica en la directiva '[Valor predeterminado de Invalidar directiva de actualizaciones](#updatedefault)'.

Vea [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) para obtener más información.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: Actualización
- Nombre de GP: Invalidar directiva de actualización
- Ruta de GP: 
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor:
  - (Estable): actualizar{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): actualizar{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canarias): actualizar{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): actualizar{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="allowsxs"></a>Allowsxs
#### <a name="allow-microsoft-edge-side-by-side-browser-experience"></a>Permitir la experiencia de exploradores Microsoft Edge en paralelo
>Microsoft Edge Update 1.2.145.5 y posteriores

#### <a name="description"></a>Descripción
Esta directiva permite a un usuario ejecutar Microsoft Edge (Edge HTML) y Microsoft Edge (basado en Chromium) en paralelo.

Si esta directiva se establece en “No configurado”, Microsoft Edge (basado en Chromium) reemplazará a Microsoft Edge (Edge HTML) después del canal estable de Microsoft Edge (basado en Chromium) y se instalarán las actualizaciones de seguridad de noviembre de 2019.  Este es el mismo comportamiento que la opción “Deshabilitado”.

La opción “Deshabilitado” bloquea la experiencia en paralelo y Microsoft Edge (basado en Chromium) reemplazará a Microsoft Edge (Edge HTML) después del canal estable de Microsoft Edge (basado en Chromium) y se instalarán las actualizaciones de seguridad de noviembre de 2019.  Este es el mismo comportamiento que la opción “No configurado”.

Cuando esta directiva está “Habilitada”, se pueden ejecutar en paralelo Microsoft Edge (Edge HTML) y Microsoft Edge (basado en Chromium) después de instalado Microsoft Edge (basado en Chromium).

Para que esta directiva de grupo surta efecto, debe configurarse antes de la instalación automática de Microsoft Edge (basado en Chromium) por parte de Windows Update. Nota: un usuario puede bloquear la actualización automática de Microsoft Edge (basado en Chromium) mediante el kit de herramientas de bloqueo de Microsoft Edge (basado en Chromium).
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: Allowsxs
- Nombre de GP: permitir la experiencia en paralelo de exploradores Microsoft Edge
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: Allowsxs
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000001
```
[Volver al principio](#microsoft-edge---update-policies)

### <a name="createdesktopshortcutdefault"></a>CreateDesktopShortcutDefault
#### <a name="prevent-desktop-shortcut-creation-upon-install-default"></a>Impedir la creación de accesos directos de escritorio durante la instalación predeterminada
>Microsoft Edge Update 1.3.128.0 y posteriores

#### <a name="description"></a>Descripción
Permite especificar el comportamiento predeterminado de todos los canales para crear un acceso directo en el escritorio cuando se instala Microsoft Edge.

  Si habilita esta directiva, se creará un acceso directo de escritorio cuando se instale Microsoft Edge.
Si deshabilita esta directiva, no se creará ningún acceso directo de escritorio cuando se instale Microsoft Edge.
Si no configura esta directiva, se creará un acceso directo de escritorio a Microsoft Edge durante la instalación.
Si Microsoft Edge ya está instalado, esta directiva no tendrá ningún efecto.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: CreateDesktopShortcutDefault
- Nombre de GP: configuración predeterminada para impedir la creación de accesos directos de escritorio durante la instalación
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Aplicaciones
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: CreateDesktopShortcutDefault
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000001
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="createdesktopshortcut"></a>CreateDesktopShortcut
#### <a name="prevent-desktop-shortcut-creation-upon-install"></a>Impedir la creación de accesos directos de escritorio durante la instalación
>Microsoft Edge Update 1.3.128.0 y posteriores

#### <a name="description"></a>Descripción
Si habilita esta directiva, se creará un acceso directo de escritorio cuando se instale Microsoft Edge.
Si deshabilita esta directiva, no se creará ningún acceso directo de escritorio cuando se instale Microsoft Edge.
Si no configura esta directiva, se creará un acceso directo de escritorio a Microsoft Edge durante la instalación.
Si Microsoft Edge ya está instalado, esta directiva no tendrá ningún efecto.

  Si no configura esta directiva para un canal, la configuración de directiva '[Impedir la creación de accesos directos de escritorio durante la instalación predeterminada](#createdesktopshortcutdefault)' determina la creación de accesos directos cuando se instala Microsoft Edge.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: CreateDesktopShortcut
- Nombre de GP: impedir la creación de métodos abreviados de escritorio durante la instalación
- Ruta de GP: 
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: 
  - (Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000001
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="rollbacktotargetversion"></a>RollbackToTargetVersion
#### <a name="rollback-to-target-version"></a>Revertir a la versión de destino
>Microsoft Edge Update 1.3.133.3 y posteriores

#### <a name="description"></a>Descripción
Especifica que Microsoft Edge Update debe revertir las instalaciones de Microsoft Edge a la versión que se indica en "[Invalidación de la versión de destino](#targetversionprefix)".

Esta directiva no surte efecto a menos que "[Invalidación de la versión de destino](#targetversionprefix)" e "[Invalidación de la directiva de actualización](#update)" se establezcan en uno de los estados activados (es decir, Permitir siempre las actualizaciones, Solo actualizaciones silenciosas automáticas o Solo actualizaciones manuales).

Si deshabilita esta directiva o no la configura, las instalaciones que tengan una versión superior a la especificada por la "[Invalidación de la versión de destino](#targetversionprefix)" quedarán tal cual están.

Si habilita esta directiva, las instalaciones que tengan una versión actual superior a la especificada por la "[Invalidación de la versión de destino](#targetversionprefix)" serán degradadas a la versión de destino.

Se recomienda a los usuarios que instalen la última versión del explorador Microsoft Edge para estar seguros de contar con la protección que proporcionan las últimas actualizaciones de seguridad. Revertir a una versión anterior supone un riesgo de exposición a problemas de seguridad conocidos. Esta directiva está pensada para usarse como una solución provisional para resolver problemas relacionados con una actualización del explorador Microsoft Edge.

Antes de revertir temporalmente a la versión anterior del explorador, recomendamos activar la sincronización ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) para todos los usuarios de la organización. Si no se activa la sincronización, se corre el riesgo de pérdida definitiva de datos de búsqueda. Utilice esta directiva bajo su propia responsabilidad.

Nota: todas las versiones disponibles para la reversión se pueden ver aquí [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).

Esta directiva se aplica a Microsoft Edge, versión 86 o posterior.

Vea [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) para obtener más información.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: RollbackToTargetVersion
- Nombre de GP: Revertir a la versión de destino
- Ruta de GP: 
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: 
  - (Estable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000001
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="targetversionprefix"></a>TargetVersionPrefix
#### <a name="target-version-override"></a>Invalidación de versión de destino
>Microsoft Edge Update 1.3.119.43 y posteriores

#### <a name="description"></a>Descripción
Cuando se habilita esta directiva y la actualización automática está habilitada, Microsoft Edge se actualizará a la versión especificada por este valor de directiva.

El valor de directiva debe ser una versión específica de Microsoft Edge, como 83.0.499.12.

Si un dispositivo tiene una versión más reciente de Microsoft Edge que el valor especificado, Microsoft Edge permanecerá en la versión más reciente, mas no desactualizada a la versión especificada.

Si la versión especificada no existe o no tiene el formato correcto, Microsoft Edge permanecerá en su versión actual y no se actualizará a versiones futuras de manera automática.

Vea [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) para obtener más información.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: TargetVersionPrefix
- Nombre de GP: Invalidación de versión de destino
- Ruta de GP: 
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Beta
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Canary
  - Plantillas administrativas/Microsoft Edge Update/Aplicaciones/Microsoft Edge Dev
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: 
  - (Estable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Tipo de valor: REG_SZ
##### <a name="example-value"></a>Valor de ejemplo:
```
83.0.499.12
```
[Volver al principio](#microsoft-edge---update-policies)

### <a name="updaterexperimentationandconfigurationservicecontrol"></a>UpdaterExperimentationAndConfigurationServiceControl
#### <a name="retrieve-configurations-and-experiments"></a>Recuperar configuraciones y experimentos
>Microsoft Edge Update 1.3.145.1 y versiones posteriores

#### <a name="description"></a>Descripción
En Microsoft Edge Update, el servicio de experimentación y configuración se usa para implementar la carga de experimentación.

La carga de experimentación consiste en una lista de características de desarrollo tempranas que Microsoft está habilitando para probar los comentarios.

Si habilita esta directiva, la carga de experimentación se descarga del Servicio de experimentación y configuración.

Si deshabilita esta directiva, la comunicación con el Servicio de experimentación y configuración se detiene por completo.

Si no configuras esta directiva, en un dispositivo administrado el comportamiento es el mismo que la directiva "deshabilitado".

Si no configura esta directiva, en un dispositivo no administrado, el comportamiento es el mismo que la directiva "habilitada".

#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: UpdateExperimentationAndConfigureationServiceControl
- Nombre de GP: controlar la comunicación del actualizador con el servicio de experimentación y configuración
- Ruta de acceso de GP: Plantillas administrativas/Actualización perimetral de Microsoftt/Microsoft Edge Update
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: UpdaterExperimentationAndConfigurationServiceControl
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000001
```
[Volver al principio](#microsoft-edge---update-policies)

## <a name="preferences-policies"></a>Directivas de preferencias

[Volver al principio](#microsoft-edge---update-policies)
### <a name="autoupdatecheckperiodminutes"></a>AutoUpdateCheckPeriodMinutes
#### <a name="auto-update-check-period-override"></a>invalidar el período de buscar actualizaciones automáticas
>Microsoft Edge Update 1.2.145.5 y posteriores

#### <a name="description"></a>Descripción
Si se habilita, esta directiva permite establecer un valor para el número mínimo de minutos entre las búsquedas de actualizaciones automáticas. De lo contrario, de manera predeterminada, la actualización automática busca actualizaciones cada 10 horas.

  Si quieres deshabilitar todas las búsquedas de actualizaciones automáticas, establece el valor en 0 (no recomendado).
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: AutoUpdateCheckPeriodMinutes
- Nombre de GP: invalidar el período de buscar actualizaciones automáticas
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Preferencias
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre de valor: AutoUpdateCheckPeriodMinutes
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000578
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="updatessuppressed"></a>UpdatesSuppressed
#### <a name="time-period-in-each-day-to-suppress-auto-update-check"></a>Período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas
>Microsoft Edge Update 1.3.33.5 y posteriores

#### <a name="description"></a>Descripción
Si habilitas esta Directiva, las búsquedas de actualizaciones se suprimirán cada día, a partir de Hora:Minuto durante un período de tiempo (en minutos). La duración no se ve afectada por el horario de verano. Por ejemplo, si la hora de inicio es 22:00 y la duración es 480 minutos, las actualizaciones se suprimirán durante 8 horas exactamente, independientemente de si el horario de verano comienza o finaliza durante este período.

  Si deshabilitas o no configuras esta directiva, las búsquedas de actualizaciones no se suprimirán durante ningún período determinado.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: UpdatesSuppressed
- Nombre de GP: período de tiempo en cada día para suprimir la búsqueda de actualizaciones automáticas
  - Opciones {Hora, Minuto, Duración}
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Preferencias
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: 
  - UpdatesSuppressedDurationMin
  - UpdatesSuppressedStartHour
  - UpdatesSuppressedStartMin
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[Volver al principio](#microsoft-edge---update-policies)

## <a name="proxy-server-policies"></a>Directivas de servidor proxy

[Volver al principio](#microsoft-edge---update-policies)
### <a name="proxymode"></a>ProxyMode
#### <a name="choose-how-to-specify-proxy-server-settings"></a>Elegir cómo especificar la configuración del servidor proxy
>Microsoft Edge Update 1.3.21.81 y posteriores

#### <a name="description"></a>Descripción
Permite especificar la configuración del servidor proxy que usa Microsoft Edge Update.

  Si habilitas esta directiva, puedes elegir entre las siguientes opciones de servidor proxy:
   - Si eliges no usar nunca un servidor proxy y siempre te conectas directamente, se ignora el resto de opciones.
   - Si elige usar la configuración proxy del sistema o detectar automáticamente el servidor proxy, se ignora el resto de opciones.
   - Si eliges el modo de servidor proxy fijo, puedes especificar más opciones en '[Dirección o dirección URL del servidor proxy](#proxyserver)'.
   - Si decides usar un script de proxy .pac, debes especificar la dirección URL del script en '[Dirección URL de un archivo de proxy .pac](#proxypacurl)'.

  Si habilitas esta directiva, los usuarios de la organización no pueden cambiar la configuración de proxy en Microsoft Edge Update.

  Si deshabilitas o no configuras esta directiva, no se configuran las opciones del servidor proxy, pero los usuarios de la organización pueden elegir su propia configuración de proxy para Microsoft Edge Update.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: ProxyMode
- Nombre de GP: elige cómo especificar la configuración del servidor proxy
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: ProxyMode
- Tipo de valor: REG_SZ
##### <a name="example-value"></a>Valor de ejemplo:
```
fixed_servers
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="proxypacurl"></a>ProxyPacUrl
#### <a name="url-to-a-proxy-pac-file"></a>Dirección URL a un archivo proxy .pac
>Microsoft Edge Update 1.3.21.81 y posteriores

#### <a name="description"></a>Descripción
Permite especificar una dirección URL para un archivo de configuración automática de proxy (PAC).

  Si habilitas esta directiva, puedes especificar una dirección URL para un archivo PAC que automatice cómo Microsoft Edge Update selecciona el servidor proxy adecuado para localizar un sitio web en particular.

  Esta directiva solo se aplica si has especificado una configuración de proxy manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.

  No configures esta directiva si has especificado una configuración de proxy diferente de manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: ProxyPacUrl
- Nombre de GP: dirección URL a un archivo proxy .pac
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: ProxyPacUrl
- Tipo de valor: REG_SZ
##### <a name="example-value"></a>Valor de ejemplo:
```
https://www.microsoft.com
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="proxyserver"></a>ProxyServer
#### <a name="address-or-url-of-proxy-server"></a>Dirección o dirección URL del servidor proxy
>Microsoft Edge Update 1.3.21.81 y posteriores

#### <a name="description"></a>Descripción
Permite especificar la dirección URL del servidor proxy que usa Microsoft Edge Update.

  Si habilitas esta directiva, puedes establecer la dirección URL del servidor proxy usado por Microsoft Edge Update en tu organización.

  Esta directiva solo se aplica si has seleccionado una configuración de proxy manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.

  No configures esta directiva si has especificado una configuración de proxy diferente de manual en la directiva '[Elegir cómo especificar la configuración del servidor proxy](#proxymode)'.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: ProxyServer
- Nombre de GP: dirección o dirección URL del servidor proxy
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Servidor proxy
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: ProxyServer
- Tipo de valor: REG_SZ
##### <a name="example-value"></a>Valor de ejemplo:
```
https://www.microsoft.com
```
[Volver al principio](#microsoft-edge---update-policies)


## <a name="microsoft-edge-webview-policies"></a>Directivas de Microsoft Edge WebView

[Volver al principio](#microsoft-edge---update-policies)
### <a name="install-webview"></a>Instalar (WebView)
#### <a name="allow-installation"></a>Permitir instalación
>Microsoft Edge Update 1.3.127.1 y posteriores

#### <a name="description"></a>Descripción
Le permite especificar si Microsoft Edge WebView se puede instalar con Microsoft Edge Update.

  - Si habilita esta directiva, los usuarios pueden instalar Microsoft Edge WebView con Microsoft Edge Update.
  - Si deshabilita esta directiva, los usuarios no pueden instalar Microsoft Edge WebView con Microsoft Edge Update.
  - Si no configura esta directiva, la configuración de la directiva del "[Valor predeterminado de Permitir instalación](#installdefault)" determinará si los usuarios pueden instalar Microsoft Edge WebView con Microsoft Edge Update.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: Install
- Nombre de GP: Permitir instalación
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Microsoft Edge WebView
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: 
  - Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000001
```
[Volver al principio](#microsoft-edge---update-policies)


### <a name="update-webview"></a>Actualización (WebView)
#### <a name="update-policy-override"></a>Invalidar directiva de actualización
>Microsoft Edge Update 1.3.127.1 y posteriores

#### <a name="description"></a>Descripción
Te permite especificar si las actualizaciones automáticas están habilitadas para Microsoft Edge WebView. Microsoft Edge WebView es un componente usado por las aplicaciones para mostrar contenido web.
Las actualizaciones automáticas están habilitadas de forma predeterminada. Al deshabilitar las actualizaciones automáticas de Microsoft Edge WebView, se pueden producir problemas de compatibilidad con las aplicaciones que dependen de este componente.

  Si habilitas esta directiva, Microsoft Edge Update trata las actualizaciones de Microsoft Edge WebView de acuerdo con la configuración de las siguientes opciones:
  - Permitir siempre las actualizaciones: las actualizaciones se descargan y aplican automáticamente
  - Actualizaciones deshabilitadas: las actualizaciones nunca se descargan ni aplican

  Si no habilitas esta directiva, las actualizaciones se descargan y se aplican automáticamente.
#### <a name="windows-information-and-settings"></a>Información y configuración de Windows
##### <a name="group-policy-admx-info"></a>Información de directiva de grupo (ADMX)
- Nombre único de GP: Actualización
- Nombre de GP: Invalidar directiva de actualización
- Ruta de GP: Plantillas administrativas/Microsoft Edge Update/Microsoft Edge WebView
- Nombre de archivo GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Configuración del Registro de Windows
- Ruta: HKEY_LOCAL_MACHINE\SOFTWARE\Directivas\Microsoft\EdgeUpdate
- Nombre del valor: 
  - Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- Tipo de valor: REG_DWORD
##### <a name="example-value"></a>Valor de ejemplo:
```
0x00000001
```
[Volver al principio](#microsoft-edge---update-policies)


## <a name="see-also"></a>Consulte también
  - [Configuración de Microsoft Edge](configure-microsoft-edge.md)
  - [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
