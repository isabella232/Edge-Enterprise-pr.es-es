---
title: Configurar Microsoft Edge para Windows
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 10/09/2019
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar las opciones de directiva de Microsoft Edge en dispositivos Windows
ms.openlocfilehash: 99aaf002f868ce29e81aa40024fa1de2e83d76e1
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981043"
---
# Configurar las opciones de directiva de Microsoft Edge en Windows

Usa la siguiente información para configurar las opciones de directiva de Microsoft Edge en tus dispositivos Windows.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## Configurar las opciones de directiva en Windows

Puedes usar los _objetos de directiva de grupo (GPO)_ para configurar las opciones de directiva en Microsoft Edge y las actualizaciones de Microsoft Edge administradas en todas las versiones de Windows. También puedes aprovisionar la directiva a través del Registro para dispositivos Windows que están unidos a un dominio Microsoft Active Directory, o a instancias de Windows 10 Pro o Enterprise inscritas para la administración de dispositivos en Microsoft Intune. Para configurar Microsoft Edge con objetos de directiva de grupo, instala _plantillas administrativas_ que agreguen reglas y configuraciones de Microsoft Edge al almacén central de directivas de grupo en el dominio de Active Directory o en la carpeta de plantillas de definición de directivas en equipos individuales y, a continuación, configura las directivas específicas que quieras establecer.

Puedes usar la directiva de grupo Active Directory para configurar las opciones de directiva de Microsoft Edge si prefieres administrar la directiva a nivel de dominio. Esto te permite administrar globalmente la configuración de la directiva, enfocando distintas configuraciones de directiva a determinadas UO, o usando filtros WMI para aplicar la configuración solamente a los usuarios o equipos devueltos por una consulta en particular. Si deseas configurar directivas en equipos individuales, puedes aplicar la configuración de directiva que solo afecte al dispositivo local mediante el Editor de directivas de grupo local en el equipo de destino.

Microsoft Edge admite tanto las directivas _obligatorias_ como las _recomendadas_. Las directivas obligatorias invalidan las preferencias del usuario e impiden que el usuario las modifique, mientras que las directivas recomendadas proporcionan una configuración predeterminada que el usuario puede invalidar. La mayoría de las directivas son solo obligatorias; un subconjunto de ellas son obligatorias y recomendadas. Si se establecen ambas versiones de una directiva, la configuración obligatoria tendrá prioridad.

>[!TIP]
> Puedes usar Microsoft Intune para configurar las opciones de la directiva de Microsoft Edge. Para obtener más información, consulta [Configurar Microsoft Edge con Microsoft Intune](configure-edge-with-intune.md).

Hay dos plantillas administrativas para Microsoft Edge que se pueden aplicar en el equipo o en el nivel de dominio de Active Directory:

- *msedge. admx* para [configurar las opciones de Microsoft Edge](microsoft-edge-policies.md)
- *msedgeupdate.admx* para [administrar las actualizaciones de Microsoft Edge](microsoft-edge-update-policies.md).

Para comenzar, descarga e instala la plantilla administrativa de Microsoft Edge.

### 1. Descarga e instala la plantilla administrativa de Microsoft Edge

Si deseas configurar las opciones de directiva de Microsoft Edge en Active Directory, descarga los archivos en una ubicación de red a la que puedas acceder desde un controlador de dominio o una estación de trabajo con las Herramientas de administración remota del servidor (RSAT) instaladas. Para configurar en un equipo individual, solo tienes que descargar los archivos en ese equipo.

Cuando agregas los archivos de plantilla administrativa a la ubicación adecuada, la configuración de directiva de Microsoft Edge está disponible inmediatamente en el Editor de directivas de grupo.

Ve a la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) para descargar el archivo de plantillas de directiva de Microsoft Edge (*MicrosoftEdgePolicyTemplates.cab*) y extrae el contenido.

#### Agregar la plantilla administrativa a Active Directory

1. En un controlador de dominio o una estación de trabajo con RSAT, busca la carpeta **PolicyDefinition** (también conocida como _Almacén central_) en cualquier controlador de dominio de tu dominio. Para versiones anteriores de Windows Server, es posible que tengas que crear la carpeta PolicyDefinition. Para obtener más información, consulta [Cómo crear y administrar el almacén central de plantillas administrativas de directivas de grupo en Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).
1. Abre *MicrosoftEdgePolicyTemplates* y ve a **windows** > **admx**.
1. Copia el archivo *msedge.admx* en la carpeta PolicyDefinition. (Ejemplo: %systemroot%\sysvol\domain\policies\PolicyDefinitions)
1. En la carpeta *admx*, abre la carpeta de idioma apropiada. Por ejemplo, si estás en EE. UU., abre la carpeta **en-US**.
1. Copia el archivo *msedge.adml* en la carpeta de idioma correspondiente de la carpeta PolicyDefinition. Si no existe, crea la carpeta. (Ejemplo: %systemroot%\sysvol\domain\policies\PolicyDefinitions\EN-US)
1. Si tu dominio tiene más de un controlador de dominio, los nuevos archivos ADMX se replicarán en ellos en el siguiente intervalo de replicación del dominio.
1. Para confirmar que los archivos se hayan cargado correctamente, abre el **Editor de administración de directivas de grupo** desde las herramientas administrativas de Windows y expande **Configuración de equipo** > **Directivas** > **Plantillas administrativas** > **Microsoft Edge**. Deberían aparecer ver uno o varios nodos de Microsoft Edge, como se muestra a continuación.

    ![Directivas de Microsoft Edge](./media/configure-microsoft-edge/edge-gpo-policies.png)

#### Agregar la plantilla administrativa a un equipo individual

1. En el equipo de destino, abre *MicrosoftEdgePolicyTemplates* y ve a **windows** > **admx**.
2. Copia el archivo *msedge.admx* en la carpeta de plantillas Definición de directivas. (Ejemplo: C:\Windows\PolicyDefinitions)
3. En la carpeta *admx*, abre la carpeta de idioma apropiada. Por ejemplo, si estás en EE. UU., abre la carpeta **en-US**.
4. Copia el archivo *msedge.adml* en la carpeta de idioma correspondiente de la carpeta de definición de directivas. (Ejemplo: C:\Windows\PolicyDefinitions\en-US)
5. Para confirmar que los archivos se hayan cargado correctamente, abre Editor de directivas de grupo local directamente (tecla Windows + R y escribe gpedit.msc) o abre MMC y carga el complemento de Editor de directivas de grupo local. Si se produce un error, suele deberse a que los archivos se encuentran en una ubicación incorrecta.

<!--
To add the administrative template to manage Microsoft Edge updates:

1. Open the *MicrosoftEdgePolicyTemplates* file and go to **windows** > **admx**.
2. Copy the *msedgeupdate.admx* file to your Policy Definition template folder. (Example: C:\Windows\PolicyDefinitions)
3. In the *updatepolicies* folder, open the appropriate language folder. For example, if you’re in Germany, open the **de-DE** folder.
4. Copy the *msedgeupdate.adml* file to the matching language folder in your Policy Definition folder. (Example: C:\Windows\PolicyDefinitions\de-DE)
5. Open MMC and load the Local Group Policy Editor snap-in to confirm the files loaded correctly. If an error occurs, it’s usually because the files are in an incorrect location.

> [!NOTE]
> Currently the Microsoft Edge update policies are only localized in en-US. Additional language support will be added in a future release.
-->

### 2. Establece directivas obligatorias o recomendadas

Puedes establecer directivas obligatorias o recomendadas para configurar Microsoft Edge con el Editor de directivas de grupo para equipos Active Directory y individuales. Puedes aplicar la configuración de directivas a la **Configuración del equipo** o a la **Configuración de usuario** seleccionando el nodo apropiado como se describe a continuación.

- Para configurar una directiva obligatoria, abre el Editor de directivas de grupo y ve a (**Configuración del equipo** o **Configuración de usuario**) > **Directivas** > **Plantillas administrativas** > **Microsoft Edge**.
- Para configurar una directiva recomendada, abre el Editor de directivas de grupo y ve a (**Configuración del equipo** o **Configuración de usuario**) > **Directivas** > **Plantillas administrativas** > **Microsoft Edge - Configuración predeterminada (los usuarios pueden invalidarla)**.

  ![Abrir el Editor de directivas de grupo](./media/configure-microsoft-edge/edge-ad-policy.png)

### 3. Prueba las directivas

En un dispositivo cliente de destino, abre Microsoft Edge y navega a **edge://policy** para ver todas las directivas que se aplican. Si aplicaste la configuración de directiva en el equipo local, las directivas deberían aparecer inmediatamente. Es posible que tengas que cerrar y volver a abrir Microsoft Edge si estaba abierto mientras estabas configurando las opciones de directiva.

![Ver las directivas configuradas en el explorador](./media/configure-microsoft-edge/edge-gpEdit.png)

Para la configuración de directiva de grupo de Active Directory, la configuración de directiva se propaga a los equipos del dominio en un intervalo regular definido por el administrador del dominio, y los equipos de destino podrían no recibir actualizaciones de directivas inmediatamente. Para actualizar manualmente la configuración de la directiva de grupo de Active Directory en un equipo de destino, ejecuta el siguiente comando desde un símbolo del sistema o sesión de PowerShell sesión en el equipo de destino:

``` powershell
gpupdate /force
```

Es posible que tengas que cerrar y volver a abrir Microsoft Edge para que aparezcan las nuevas directivas.

También puedes usar REGEDIT.exe en un equipo de destino para ver la configuración del Registro que almacena la configuración de directiva de grupo. Esta configuración se encuentra en la ruta del Registro **HKLM\SOFTWARE\Policies\Microsoft\Edge**.

## Preguntas frecuentes

### ¿Se puede configurar Microsoft Edge para usar las preferencias maestras?

Si, puedes configurar Microsoft Edge para usar un archivo de preferencias maestras?

 Un archivo de preferencias maestras permite configurar las opciones predeterminadas cuando se implementa Microsoft Edge. También puedes usar un archivo de preferencias maestras para aplicar la configuración en equipos que no están administrados por un sistema de administración de dispositivos. Esta configuración se aplica al perfil del usuario la primera vez que el usuario ejecuta el explorador. Cuando el usuario ejecute el explorador, no se aplicarán los cambios realizados en el archivo de preferencias principales. Un usuario puede cambiar la configuración de las preferencias maestras del explorador. Si quieres que una configuración sea obligatoria o cambiar una configuración después de la primera ejecución del explorador, debes usar una directiva.

Un archivo de preferencias principales permite personalizar muchas opciones de configuración y preferencias diferentes del explorador, incluidas las que se comparten con otros exploradores basados en Chromium y las específicas de Microsoft Edge.  Las preferencias relacionadas con la directiva pueden configurarse mediante el archivo de preferencias maestras. En los casos en los que se establece una directiva y hay un conjunto de preferencias maestro correspondiente, la configuración de directiva tiene prioridad.

> [!IMPORTANT]
> Es posible que todas las preferencias disponibles no sean coherentes con la terminología Microsoft Edge y las convenciones de nomenclatura.  No hay ninguna garantía de que estas preferencias sigan funcionando según lo previsto en futuras versiones. Las preferencias se pueden cambiar u omitir en versiones posteriores.

Un archivo de preferencias maestras es un archivo de texto que se ha formateado usando marcado JSON. Este archivo debe agregarse al mismo directorio que el ejecutable msedge.exe. Para implementaciones de empresa por todo el sistema en Windows, suele ser: *Windows: C:\Program Files\Microsoft\Edge\Application\master_preferences*.

## Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar para Windows con Intune](configure-edge-with-intune.md)
- [Configurar para macOS](configure-microsoft-edge-on-mac.md)
- [Examinar directivas de empresa de Microsoft Edge](microsoft-edge-policies.md)


