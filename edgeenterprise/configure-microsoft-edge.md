---
title: Configurar Microsoft Edge para Windows
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar las opciones de directiva de Microsoft Edge en dispositivos Windows
ms.openlocfilehash: a5db4352e723539843a5ad80a7b067e670bced5c
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979741"
---
# <a name="configure-microsoft-edge-policy-settings-on-windows"></a>Configurar las opciones de directiva de Microsoft Edge en Windows

Usa la siguiente información para configurar las opciones de directiva de Microsoft Edge en tus dispositivos Windows.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="configure-policy-settings-on-windows"></a>Configurar las opciones de directiva en Windows

Puedes usar los _objetos de directiva de grupo (GPO)_ para configurar las opciones de directiva en Microsoft Edge y las actualizaciones de Microsoft Edge administradas en todas las versiones de Windows. También puedes aprovisionar la directiva a través del Registro para dispositivos Windows que están unidos a un dominio Microsoft Active Directory, o a instancias de Windows 10 Pro o Enterprise inscritas para la administración de dispositivos en Microsoft Intune. Para configurar Microsoft Edge con objetos de directiva de grupo, instala _plantillas administrativas_ que agreguen reglas y configuraciones de Microsoft Edge al almacén central de directivas de grupo en el dominio de Active Directory o en la carpeta de plantillas de definición de directivas en equipos individuales y, a continuación, configura las directivas específicas que quieras establecer.

Puedes usar la directiva de grupo Active Directory para configurar las opciones de directiva de Microsoft Edge si prefieres administrar la directiva a nivel de dominio. Esto te permite administrar globalmente la configuración de la directiva, enfocando distintas configuraciones de directiva a determinadas UO, o usando filtros WMI para aplicar la configuración solamente a los usuarios o equipos devueltos por una consulta en particular. Si deseas configurar directivas en equipos individuales, puedes aplicar la configuración de directiva que solo afecte al dispositivo local mediante el Editor de directivas de grupo local en el equipo de destino.

Microsoft Edge admite tanto las directivas _obligatorias_ como las _recomendadas_. Las directivas obligatorias invalidan las preferencias del usuario e impiden que el usuario las modifique, mientras que las directivas recomendadas proporcionan una configuración predeterminada que el usuario puede invalidar. La mayoría de las directivas son solo obligatorias; un subconjunto de ellas son obligatorias y recomendadas. Si se establecen ambas versiones de una directiva, la configuración obligatoria tendrá prioridad. Una directiva recomendada solo se hace efectiva cuando el usuario no ha modificado la configuración.

>[!TIP]
> Puedes usar Microsoft Intune para configurar las opciones de la directiva de Microsoft Edge. Para obtener más información, consulta [Configurar Microsoft Edge con Microsoft Intune](configure-edge-with-intune.md).

Hay dos plantillas administrativas para Microsoft Edge que se pueden aplicar en el equipo o en el nivel de dominio de Active Directory:

- *msedge. admx* para [configurar las opciones de Microsoft Edge](microsoft-edge-policies.md)
- *msedgeupdate.admx* para [administrar las actualizaciones de Microsoft Edge](microsoft-edge-update-policies.md).

Para comenzar, descarga e instala la plantilla administrativa de Microsoft Edge.

### <a name="1-download-and-install-the-microsoft-edge-administrative-template"></a>1. Descarga e instala la plantilla administrativa de Microsoft Edge

Si deseas configurar las opciones de directiva de Microsoft Edge en Active Directory, descarga los archivos en una ubicación de red a la que puedas acceder desde un controlador de dominio o una estación de trabajo con las Herramientas de administración remota del servidor (RSAT) instaladas. Para configurar en un equipo individual, solo tienes que descargar los archivos en ese equipo.

Cuando agregas los archivos de plantilla administrativa a la ubicación adecuada, la configuración de directiva de Microsoft Edge está disponible inmediatamente en el Editor de directivas de grupo.

Ve a la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) para descargar el archivo de plantillas de directiva de Microsoft Edge (*MicrosoftEdgePolicyTemplates.cab*) y extrae el contenido.

#### <a name="add-the-administrative-template-to-active-directory"></a>Agregar la plantilla administrativa a Active Directory

1. En un controlador de dominio o una estación de trabajo con RSAT, busca la carpeta **PolicyDefinition** (también conocida como _Almacén central_) en cualquier controlador de dominio de tu dominio. Para versiones anteriores de Windows Server, es posible que tengas que crear la carpeta PolicyDefinition. Para obtener más información, consulta [Cómo crear y administrar el almacén central de plantillas administrativas de directivas de grupo en Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).
2. Abre *MicrosoftEdgePolicyTemplates* y ve a **windows** > **admx**.
3. Copia el archivo *msedge.admx* en la carpeta PolicyDefinition. (Ejemplo: %systemroot%\sysvol\domain\policies\PolicyDefinitions)
4. En la carpeta *admx*, abre la carpeta de idioma apropiada. Por ejemplo, si estás en EE. UU., abre la carpeta **en-US**.
5. Copia el archivo *msedge.adml* en la carpeta de idioma correspondiente de la carpeta PolicyDefinition. Si no existe, crea la carpeta. (Ejemplo: %systemroot%\sysvol\domain\policies\PolicyDefinitions\EN-US)
6. Si tu dominio tiene más de un controlador de dominio, los nuevos archivos ADMX se replicarán en ellos en el siguiente intervalo de replicación del dominio.
7. Para confirmar que los archivos se hayan cargado correctamente, abre el **Editor de administración de directivas de grupo** desde las herramientas administrativas de Windows y expande **Configuración de equipo** > **Directivas** > **Plantillas administrativas** > **Microsoft Edge**. Deberían aparecer ver uno o varios nodos de Microsoft Edge, como se muestra a continuación.

    ![Directivas de Microsoft Edge](./media/configure-microsoft-edge/edge-gpo-policies.png)

#### <a name="add-the-administrative-template-to-an-individual-computer"></a>Agregar la plantilla administrativa a un equipo individual

1. En el equipo de destino, abre *MicrosoftEdgePolicyTemplates* y ve a **windows** > **admx**.
2. Copia el archivo *msedge.admx* en la carpeta de plantillas Definición de directivas. (Ejemplo: C:\Windows\PolicyDefinitions)
3. En la carpeta *admx*, abre la carpeta de idioma apropiada. Por ejemplo, si estás en EE. UU., abre la carpeta **en-US**.
4. Copia el archivo *msedge.adml* en la carpeta de idioma correspondiente de la carpeta de definición de directivas. (Ejemplo: C:\Windows\PolicyDefinitions\en-US)
5. Para confirmar que los archivos se hayan cargado correctamente, abre Editor de directivas de grupo local directamente (tecla Windows + R y escribe gpedit.msc) o abre MMC y carga el complemento de Editor de directivas de grupo local. Si se produce un error, suele deberse a que los archivos se encuentran en una ubicación incorrecta.

### <a name="2-set-mandatory-or-recommended-policies"></a>2. Establece directivas obligatorias o recomendadas

Puedes establecer directivas obligatorias o recomendadas para configurar Microsoft Edge con el Editor de directivas de grupo para equipos Active Directory y individuales. Puedes aplicar la configuración de directivas a la **Configuración del equipo** o a la **Configuración de usuario** seleccionando el nodo apropiado como se describe a continuación.

- Para configurar una directiva obligatoria, abre el Editor de directivas de grupo y ve a (**Configuración del equipo** o **Configuración de usuario**) > **Directivas** > **Plantillas administrativas** > **Microsoft Edge**.
- Para configurar una directiva recomendada, abre el Editor de directivas de grupo y ve a (**Configuración del equipo** o **Configuración de usuario**) > **Directivas** > **Plantillas administrativas** > **Microsoft Edge - Configuración predeterminada (los usuarios pueden invalidarla)**.

  ![Abrir el Editor de directivas de grupo](./media/configure-microsoft-edge/edge-ad-policy.png)

### <a name="3-test-your-policies"></a>3. Prueba las directivas

En un dispositivo cliente de destino, abre Microsoft Edge y navega a **edge://policy** para ver todas las directivas que se aplican. Si aplicaste la configuración de directiva en el equipo local, las directivas deberían aparecer inmediatamente. Es posible que tengas que cerrar y volver a abrir Microsoft Edge si estaba abierto mientras estabas configurando las opciones de directiva.

![Ver las directivas configuradas en el explorador](./media/configure-microsoft-edge/edge-gpEdit.png)

Para la configuración de directiva de grupo de Active Directory, la configuración de directiva se propaga a los equipos del dominio en un intervalo regular definido por el administrador del dominio, y los equipos de destino podrían no recibir actualizaciones de directivas inmediatamente. Para actualizar manualmente la configuración de la directiva de grupo de Active Directory en un equipo de destino, ejecuta el siguiente comando desde un símbolo del sistema o sesión de PowerShell sesión en el equipo de destino:

``` powershell
gpupdate /force
```

Es posible que tengas que cerrar y volver a abrir Microsoft Edge para que aparezcan las nuevas directivas.

También puedes usar REGEDIT.exe en un equipo de destino para ver la configuración del Registro que almacena la configuración de directiva de grupo. Esta configuración se encuentra en la ruta del Registro **HKLM\SOFTWARE\Policies\Microsoft\Edge**.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar para Windows con Intune](configure-edge-with-intune.md)
- [Configurar para macOS](configure-microsoft-edge-on-mac.md)
- [Examinar directivas de empresa de Microsoft Edge](microsoft-edge-policies.md)


