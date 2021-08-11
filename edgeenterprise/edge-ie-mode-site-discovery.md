---
title: Guía paso a paso para la Detección de sitio empresarial
ms.author: collw
author: appcompatguy
manager: saudm
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Usar Detección de sitio empresarial para preparar para el modo IE
ms.openlocfilehash: c3f8cbd18c4353bfa32e379c26038ced432b6ac5bbdbb0ed1579add7ad0b74da
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724543"
---
# <a name="enterprise-site-discovery-step-by-step-guide"></a>Guía paso a paso para la Detección de sitio empresarial

>[!Note]
> La aplicación de escritorio Internet Explorer 11 se retirará y dejará de recibir soporte el 15 de junio de 2022 (para ver una lista de lo que se verá afectado, [consulte las preguntas frecuentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Las mismas aplicaciones y sitios de IE11 que use hoy pueden abrirse en Microsoft Edge mediante el uso del modo Internet Explorer. [Más información aquí](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Este artículo proporciona una guía paso a paso para usar la Detección de sitio empresarial con Microsoft Endpoint Configuration Manager.

Detección del sitio empresarial puede ayudarte a configurar la Lista de sitios del modo empresarial. Detección del sitio empresarial te ayudará a:

- Detectar qué sitios usan modos de documento heredados. A no ser que estos sitios detecten exploradores modernos y proporcionen un código HTML diferente, es probable que necesiten usar el modo IE.
- Detectar los sitios que usan controles ActiveX. Microsoft Edge no admite controles ActiveX. A no ser que estos sitios detecten exploradores modernos y proporcionen un código HTML diferente, es probable que necesiten usar el modo IE.

> [!NOTE]
> Este artículo se aplica a los canales de Microsoft Edge **Estable**, **Beta** y **Dev**, versión 77 o posterior.

## <a name="prerequisites"></a>Requisitos previos

En esta guía se presupone que está familiarizado con el uso de Administrador de configuración de Microsoft Endpoint y que tiene instaladas las siguientes funciones y servicios:

1. Administrador de configuración de Microsoft Endpoint
2. Microsoft SQL Server Reporting Services
3. (Opcional) Rol de punto de servicios de creación de informes de Configuration Manager configurado

## <a name="download-enterprise-site-discovery-tools"></a>Descargar herramientas de Detección de sitio empresarial

Descarga las herramientas siguientes:

- [Paquete de configuración e instalación de Detección del sitio empresarial](https://go.microsoft.com/fwlink/p/?LinkId=517719)
- [Creador de informes de Microsoft](https://www.microsoft.com/download/details.aspx?id=53613)

## <a name="enable-enterprise-site-discovery"></a>Habilitar la Detección de sitio empresarial

Para poder conectarte al Instrumental de administración de Windows (WMI) y recuperar los datos de detección del sitio, primero tienes que implementar el proveedor de clase WMI en el dispositivo.

Desde el **paquete de configuración e instalación del sitio empresarial**, extrae el contenido en una carpeta del recurso compartido de la biblioteca de software definitiva. Ejemplo: **\\\\DSL\\EnterpriseSiteDiscovery**.

Después, crea un paquete en el Administrador de configuración de Microsoft Endpoint, tal y como se describe en la [documentación](/configmgr/apps/deploy-use/packages-and-programs), seleccionando las opciones siguientes:

- En la página **Paquete**, selecciona **Nombre** y especifica el nombre **Habilitar la detección del sitio**
- En la página **Paquete**, selecciona **Este paquete contiene los archivos de origen**
- En la página **Paquete**, especifica la carpeta de origen en la que extrajiste los archivos (por ejemplo, **\\\\DSL\\EnterpriseSiteDiscovery**).
- En la página **Tipo de programa**, elige **Programa estándar**
- En la página **Programa estándar**, escribe la línea de comandos para configurar la Detección de sitio en el dispositivo, como se indica a continuación:
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1
  ```
  > [!NOTE]
  > El script admite el uso de modificadores de línea de comandos para `-ZoneAllowList` y `-SiteAllowList`. Para este procedimiento detallado, configuraremos estas opciones mediante la directiva de grupo (a continuación).
- En la página **Programa estándar**, selecciona la opción para ejecutar **Oculto**.
- En la página **Programa estándar**, en **El programa se puede ejecutar**, selecciona la opción **Independientemente de si un usuario ha iniciado sesión**

Después de crear el paquete, haz doble clic en el nombre del paquete **Habilitar detección de sitio** para ver sus propiedades. En la propiedad **Después de ejecutar**, selecciona **Configuration Manager reinicia el equipo**. Se iniciará la recopilación de datos WMI cuando se reinicien los dispositivos.

> [!NOTE]
> Puedes configurar la cantidad de tiempo que un usuario tiene para reiniciar el dispositivo, como se describe en la [documentación de configuración del cliente](/configmgr/core/clients/deploy/about-client-settings#computer-restart).

## <a name="configure-enterprise-site-discovery-via-group-policy"></a>Configurar la Detección de sitio empresarial a través de la directiva de grupo

Con la Detección de sitio empresarial habilitada, puedes configurar los datos que recopilarás. Ten en cuenta los requisitos de las leyes y normativas locales como se describe [aquí](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery#what-data-is-collected).

1. Abre el Editor de directivas de grupo.
2. Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Componentes de Windows** > **Internet Explorer**. 
3. Haz doble clic en **Activar resultados WMI de la Detección de sitio**
4. Selecciona **Habilitado**
5. Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración de directiva.

Puedes limitar las zonas en las que recopilas datos del sitio:

1. Haz doble clic en **Limitar los resultados de la detección de sitio por zona**
2. Selecciona **Habilitado**
3. Introduce una máscara de bit que indique para qué zonas habilitar la Detección de sitio:
    1. Zona de sitios restringidos
    2. Zona de Internet
    3. Zona de sitios de confianza
    4. Zona de Intranet local
    5. Zona de equipo local
    
    Ejemplo 1: **00010** recopilará datos solo para la zona de Intranet local

    Ejemplo 2: **10111** recopilará los datos de todas las zonas excepto la zona de Internet
4. Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración de directiva.

Puedes limitar los dominios en los que recopilas datos del sitio:

1. Haz doble clic en **Limitar los resultados de la detección de sitio por dominio**
2. Selecciona **Habilitado**
3. Escribe los dominios para los que quieres recopilar datos, un dominio por línea.
4. Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración de directiva.

## <a name="collect-site-discovery-data-using-configuration-manager"></a>Recopilar datos de Detección de sitio con Configuration Manager

Ahora que tus dispositivos generan datos, es el momento de recopilar estos datos en Configuration Manager.

1. En la consola de Configuration Manager, elige **Administración** > **Configuración de cliente** > **Configuración de cliente predeterminada**
2. En la pestaña **Inicio**, en el grupo **Propiedades**, elige **Propiedades**.
3. En el cuadro de diálogo **Configuración de cliente predeterminada**, elige **Inventario de hardware**
4. En la lista **Configuración de dispositivo**, elige **Establecer clases**
5. En el cuadro de diálogo **Clases de inventario de hardware**, elige **Agregar**
6. En el cuadro de diálogo **Agregar clase de inventario de hardware**, haz clic en **Conectar**
7. En el cuadro de diálogo **Conectar al Instrumental de administración de Windows (WMI)**, escribe el nombre de un equipo en el que está configurada la Detección de sitio empresarial. Si te estás conectando a otro equipo, necesitarás las credenciales con permiso para obtener acceso a WMI.
8. En el cuadro de texto **Espacio de nombres WMI**, escribe **root\cimv2\IETelemetry**
9. Elige **Conectar**
10. En el cuadro de diálogo **Agregar clase de inventario de hardware**, en la lista **Clases de inventario**, selecciona las clases WMI **IESystemINfo**, **IEUrlInfo** y **IECountInfo*.
11. Haga clic en **Aceptar** para cerrar el cuadro de diálogo **Calificadores de clase** y los otros cuadros de diálogo abiertos.

Cuando el cliente actualiza la configuración desde el punto de administración, se notificarán los datos cuando se ejecute el siguiente inventario de hardware (de manera predeterminada, cada siete días).

## <a name="import-site-discovery-reports"></a>Importar informes de Detección de sitio

El paquete de tección de sitio empresarial incluye dos informes de ejemplo. Un informe muestra los sitios que usan los controles ActiveX y otro muestra los sitios que usan modos de documentos heredados.

### <a name="configure-the-site-discovery-sample-report"></a>Configura el informe de muestra de Detección de sitio

Usa el siguiente procedimiento para crear un informe de ejemplo que use tres orígenes de datos: los sitios que visita el usuario, información sobre su sistema y los modos de documento que usan los sitios. Este informe te ayuda a identificar los sitios que pueden depender de modos de documentos heredados.

1. Copia el informe **SCCM_Report-Site_Discovery.rdl** al servidor de Configuration Manager.
2. Instala el [Generador de informes de Microsoft](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).
3. Haz doble clic en **SCCM_Report-Site_Discovery.rdl** para abrir el informe en el Generador de informes.
4. La primera vez que intentas abrir el informe, intentará ponerse en contacto con el servidor en el que se creó. Cuando se te pida **Conectar al servidor de informes**, haz clic en **No**.
5. Cuando se abra el informe, expande **Orígenes de datos** y haz doble clic en **DataSource1**.
6. En la ventana **Propiedades de origen de datos**, selecciona **Usar una conexión incrustada en el informe** y, después, haz clic en el botón **Compilación...**.
7. En la ventana **Propiedades de conexión**, selecciona **Nombre del servidor** y escribe el nombre del servidor de Configuration Manager. Después, en **Selecciona o especifica el nombre de la base de datos**, selecciona el nombre de la base de datos de Configuration Manager de la lista desplegable.
8. Haz clic en **Aceptar** para cerrar la ventana **Propiedades de conexión**.
9. Para probar la conexión, haz clic en **Probar conexión**. Si la conexión se ha realizado correctamente, haz clic en **Aceptar** para cerrar la ventana de **Propiedades de origen de datos**.
10. Repite los pasos del 5 al 9 para **Origen de datos 2**.
11. Expande **Conjuntos de datos** y haz doble clic en **DataSet1**.
12. En la ventana **Propiedades del conjunto de datos**, haz clic en el cuadro de texto **Consulta:** y reemplaza **USAR CM_A1B** con el nombre de la base de datos que seleccionaste en el paso 7.
13. Repite los pasos 11 y 12 para **DataSet2**, **DataSet3** y **DataSet4**.
14. En la pestaña **Inicio** de la cinta de opciones, haz clic en el botón **Ejecutar** para probar el informe.
15. Guarda el informe.
16. Cierra el generador de informes de Microsoft.
17. Cambia el nombre del archivo por **Detección de sitio.rdl**

### <a name="configure-the-activex-sample-report"></a>Configurar el informe de ejemplo de ActiveX

Usa el siguiente procedimiento para crear un informe de ejemplo que use un origen de datos: los sitios que usan controles ActiveX. Ya que Internet Explorer es el único explorador que admite controles ActiveX, estos sitios pueden requerir el modo IE.

1. Copia el informe **Informe de muestra SCCM: ActiveX.rdl** en el servidor de Configuration Manager.
2. Instala el [Generador de informes de Microsoft](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).
3. Haz doble clic en **Informe de muestra SCCM: ActiveX.rdl** para abrir el informe en el generador de informes.
4. La primera vez que intentas abrir el informe, intentará ponerse en contacto con el servidor en el que se creó. Cuando se te pida **Conectar al servidor de informes**, haz clic en **No**.
5. Cuando se abra el informe, expande **Orígenes de datos** y haz doble clic en **AutoGen__5C6358F2_4BB6_4a1b_A16E_8D96795D8602_**.
6. En la ventana **Propiedades de origen de datos**, selecciona **Usar una conexión incrustada en el informe** y, después, haz clic en el botón **Compilación...**.
7. En la ventana **Propiedades de conexión**, selecciona **Nombre del servidor** y escribe el nombre del servidor de Configuration Manager. Después, en **Selecciona o especifica el nombre de la base de datos**, selecciona el nombre de la base de datos de Configuration Manager de la lista desplegable.
8. Haz clic en **Aceptar** para cerrar la ventana **Propiedades de conexión**.
9. Para probar la conexión, haz clic en **Probar conexión**. Si la conexión se ha realizado correctamente, haz clic en **Aceptar** para cerrar la ventana de **Propiedades de origen de datos**.
10. Expande **Conjuntos de datos** y haz doble clic en **DataSet1**.
11. En la ventana **Propiedades del conjunto de datos**, haz clic en el cuadro de texto **Consulta:** y reemplaza **USAR CM_A1B** con el nombre de la base de datos que seleccionaste en el paso 7.
12. En la pestaña **Inicio** de la cinta de opciones, haz clic en el botón **Ejecutar** para probar el informe.
13. Guarda el informe.
14. Cierra el generador de informes de Microsoft.
15. Cambia el nombre del archivo a **ActiveX**

### <a name="upload-configured-reports-to-microsoft-sql-server-reporting-services"></a>Cargar informes configurados a Microsoft SQL Server Reporting Services

Una vez que hayas configurado los informes para tu entorno, cárgalos en el servidor de informes.

1. Abre la aplicación **Reporting Services Configuration Manager**.
2. En la ventana **Conexión del servidor de informes**, haz clic en **Conectar** y, después, haz clic en la dirección URL que se muestra en **Identificación del sitio del portal web**
3. En la ventana del explorador que se abre (deberías estar en la página **SQL Server Reporting Services**), haz clic en la carpeta **ConfigMgr_SCCMSiteCode** para el código de tu sitio SCCM.
4. En la cinta de opciones, mueve el puntero sobre **+ Nuevo** y haz clic en el elemento de menú **Carpeta**.
5. Escribe un nombre de carpeta, por ejemplo, **Detección de sitio empresarial** y, después, haz clic en el botón **Crear**.
6. Haz clic en la carpeta **Detección de sitio empresarial**.
7. En la cinta de opciones, haz clic en el botón **Cargar**.
8. Selecciona el informe **Detección de sitio** y haz clic en **Aceptar**.
9. Repite los pasos 7 y 8 para el informe de **ActiveX**.

### <a name="view-reports-in-configuration-manager"></a>Ver informes en Configuration Manager

Ahora que has personalizado y cargado los informes, puedes verlos en Configuration Manager.

1. En la consola de Configuration Manager, elige **Supervisar** > **Creación de informes** > **Informes** > **Detección de sitio empresarial**
2. Haz doble clic en un informe para verlo.

## <a name="disable-enterprise-site-discovery"></a>Deshabilitar la Detección de sitio empresarial

Cuando hayas terminado de recopilar datos, debes deshabilitar la detección de sitio empresarial. Crea un segundo paquete para deshabilitar la detección de sitio empresarial en el Administrador de configuración de Microsoft Endpoint, tal como se describe en la [documentación](/configmgr/apps/deploy-use/packages-and-programs), seleccionando las opciones siguientes:

- En la página **Paquete**, selecciona **Nombre** y especifica el nombre **Deshabilitar la detección de sitio**
- En la página **Paquete**, selecciona **Este paquete contiene los archivos de origen**
- En la página **Paquete**, especifica la carpeta de origen en la que extrajiste los archivos (por ejemplo, **\\\\DSL\\EnterpriseSiteDiscovery**).
- En la página **Tipo de programa**, elige **Programa estándar**
- En la página **Programa estándar**, escribe la línea de comandos que deshabilitará la Dtección de sitio en el dispositivo, tal como se indica a continuación:
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1 -IEFeatureOff
  ```
- En la página **Programa estándar**, selecciona la opción para ejecutar **Oculto**
- En la página **Programa estándar**, en **El programa se puede ejecutar**, selecciona la opción **Independientemente de si un usuario ha iniciado sesión**

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Acerca del modo IE](./edge-ie-mode.md)
- [Información adicional del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Información adicional de Detección de sitio empresarial](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)