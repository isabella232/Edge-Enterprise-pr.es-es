---
title: Implementar Microsoft Edge con System Center Configuration Manager
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Aprende a implementar Microsoft Edge con System Center Configuration Manager (SCCM).
ms.openlocfilehash: 0e3011178853a13562bd41a1f149975ab10317d07a48b5e19c3d6cf9d791a48e
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726574"
---
# <a name="deploy-microsoft-edge-using-system-center-configuration-manager"></a>Implementar Microsoft Edge con System Center Configuration Manager

En este artículo se muestra cómo automatizar una implementación de Microsoft Edge con System Center Configuration Manager (SCCM).

>[!NOTE]
>Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="before-you-begin"></a>Antes de comenzar

Revisa la información de [Introducción a la administración de aplicaciones en Configuration Manager](/sccm/apps/understand/introduction-to-application-management). Este artículo de administración de aplicaciones te ayudará a comprender la terminología que se usa en este artículo y es una guía para preparar el sitio para la instalación de aplicaciones.

Descarga los archivos de instalación de Microsoft Edge Enterprise (**MicrosoftEdgeDevEnterpriseX64.msi** y/o **MicrosoftEdgeDevEnterpriseX86.msi**) desde la [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).

Asegúrese de almacenar los archivos de instalación de Microsoft Edge en una ubicación de red accesible.

## <a name="create-the-application"></a>Crear la aplicación

Crearás la aplicación mediante un asistente del Administrador de configuración.

### <a name="start-the-create-application-wizard-and-create-the-application"></a>Iniciar el Asistente para crear aplicaciones y crear la aplicación  

1. En la consola del Administrador de configuración, haz clic en **Biblioteca de software** > **Administración de aplicaciones** > **Aplicaciones**.  

2. En la pestaña **Inicio**, en el grupo **Crear**, haz clic en **Crear aplicación**. O bien, haz clic con el botón secundario en **Aplicaciones**, en la barra de navegación, y después haz clic en **Crear aplicación**.

    ![Crear aplicación](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. En la página **General** del **Asistente para crear aplicaciones**, elige **Detectar automáticamente la información sobre esta aplicación a partir de archivos de instalación**. Esto rellena previamente parte de la información del asistente con información que se ha extraído del archivo de instalación .msi. Facilita la información siguiente:  

   - **Tipo**: elige **Windows Installer (archivo \*.msi)**.  

   - **Ubicación**: escribe la ubicación (o haz clic en **Examinar** para seleccionar la ubicación) del archivo de instalación **MicrosoftEdgeDevEnterpriseX64.msi** o **MicrosoftEdgeDevEnterpriseX86.msi**. Ten en cuenta que la ubicación debe especificarse en el formulario *\\\Server\Share\File* para que el Administrador de configuración encuentre los archivos de instalación.  

   La página **Especificar configuración para esta aplicación** será similar al siguiente ejemplo:  

    ![Especificar la configuración para esta aplicación](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. Haz clic en **Siguiente**. En **Detalles** de la página **Información importada**, verás información sobre la aplicación y cualquier archivo asociado que se haya importado. Haz clic en **Siguiente** para continuar con el asistente.  

    ![Ver información importante](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. En la página **Información general**, puedes agregar más información sobre la aplicación. Por ejemplo, la versión del software, comentarios del administrador y el publicador. Puedes usar esta información para ayudarte a ordenar y encontrar la aplicación en la consola del Administrador de configuración.

   También puedes usar el campo **Programa de instalación** para especificar la línea de comandos completa que se usará para instalar la aplicación en los PC. Puedes editarlo para agregar tus propias propiedades (por ejemplo, **/q** para una instalación desatendida).

   En la captura de pantalla siguiente se muestra un ejemplo en el que se usan los campos **Especificar información sobre esta aplicación**.

   ![Especificar los metadatos de la aplicación](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. Haz clic en **Siguiente**.
7. En la página **Resumen**, puedes confirmar la configuración de la aplicación en **Detalles** y, a continuación, terminar de usar el asistente. Haz clic en **Siguiente**.  

    ![Detalles de configuración de la aplicación](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. En la página **Finalización**, haz clic en **Cerrar**.

    ![Diálogo Éxito](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

Has terminado de crear la aplicación. Usa los siguientes pasos para verlo en el Administrador de configuración:

- selecciona el **área de** trabajo de la biblioteca de software
- expande **Administración de aplicaciones**
- haz clic en **Aplicaciones**.

La siguiente captura de pantalla muestra el ejemplo usado para este artículo.  

![Aplicaciones](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## <a name="change-application-properties-and-deployment-settings"></a>Cambiar la configuración de las propiedades y la implementación de la aplicación

Después de crear una aplicación, puedes refinar la configuración de la aplicación si es necesario. Para ver las propiedades de la aplicación:

- selecciona la aplicación
- en **Inicio**>**Propiedades**, haz clic en **Propiedades**.  

   ![Configurar las propiedades de la aplicación](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 En la página de diálogo **<nombre de aplicación\> Propiedades de la aplicación**, verás una vista con pestañas de los elementos que puedes configurar para cambiar el comportamiento de la aplicación. Para obtener más información sobre las opciones que puedes configurar, consulta [Crear aplicaciones](/sccm/apps/deploy-use/create-applications).

Para este ejemplo, cambiarás algunas propiedades del tipo de implementación de la aplicación. Para cambiar las propiedades de implementación:

1. Haz clic en la pestaña **Tipos de implementación**.
2. En **Tipos de implementación:**, selecciona el **Nombre** de la aplicación.
3. Haz clic en **Editar**.

   ![Editar el tipo de implementación](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### <a name="add-a-requirement-to-the-deployment-type"></a>Agregar un requisito al tipo de implementación

 Los requisitos especifican las condiciones que deben cumplirse para que una aplicación pueda instalarse en un dispositivo. Puedes elegir entre los requisitos integrados o puedes crear los tuyos propios. Por ejemplo, puedes agregar un requisito para que la aplicación solo se instale solo en los PC que ejecutan Windows 10 **x86** o **x64**, según la arquitectura del procesador de destino del archivo de instalación. En este ejemplo, tendrás que especificar Windows 10 **x86**.

1. En la página de propiedades de tipo de implementación que acabas de abrir, haz clic en la pestaña **Requisitos**.

2. Haz clic en **Agregar** para abrir el cuadro de diálogo **Crear requisito**.

    ![Crear requisito](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. En el cuadro de diálogo **Crear requisito**, especifica la siguiente información:

    - **Categoría**: **Dispositivo**  

    - **Condición**: **Sistema operativo**  

    - **Tipo de regla**: **Valor**  

    - **Operador**: **Uno de**  

    - En la lista de sistemas operativos, selecciona **Windows 10** > **Todos los Windows 10 (32 bits)**.  

    Cuando hayas terminado, el cuadro de diálogo será similar al siguiente ejemplo de captura de pantalla:

    ![Agregar requisito](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. Haz clic en **Aceptar** para cerrar todas las páginas de propiedades abiertas y volver a la lista **Aplicaciones** de la consola de Administrador de configuración.  

## <a name="add-the-application-content-to-a-distribution-point"></a>Agregar el contenido de la aplicación a un punto de distribución  

Para implementar la aplicación actualizada en los PC, asegúrate de que el contenido de la aplicación se copie en un punto de distribución. Los PC tienen acceso al punto de distribución para instalar la aplicación.  

>[!TIP]
>Para obtener más información sobre los puntos de distribución y la administración de contenido en Administrador de configuración, consulta [Implementar y administrar contenido para System Center Configuration Manager](/sccm/core/servers/deploy/configure/deploy-and-manage-content).  

1. En la consola del Administrador de configuración, haz clic en **Biblioteca de software**.  

2. En el área de trabajo **Biblioteca de software**, expande **Aplicaciones**. Selecciona la aplicación que hayas creado en la lista de aplicaciones.

3. En la pestaña **Inicio** del grupo **Implementación**, haz clic en **Distribuir contenido**.  

4. En la página **General** del **Asistente de distribución de contenido**, compruebe que el nombre de la aplicación sea correcto y, a continuación, haga clic en **Siguiente**.  

5. En la página **Contenido**, revisa la información que se copiará al punto de distribución y luego haz clic en **Siguiente**.  

6. En la página **Destino del contenido**, haz clic en **Agregar** para seleccionar una o más colecciones, puntos de distribución o grupos de puntos de distribución en los que instalar el contenido de la aplicación.

7. Completa el asistente.

Puedes comprobar que el contenido de la aplicación se copió correctamente en el punto de distribución desde el área de trabajo **Supervisión**, en **Estado de distribución** > **Estado del contenido**.  

## <a name="deploy-the-application"></a>Implementar la aplicación  

A continuación, implementa la aplicación en una colección de dispositivos de la jerarquía. En este ejemplo, se implementa la aplicación en la colección de dispositivos **Todos los sistemas**.  

>[!TIP]
>Recuerda que solo los equipos con Windows 10 de la arquitectura de procesador especificada instalarán la aplicación, debido a los requisitos que seleccionaste anteriormente.  

1. En la consola del Administrador de configuración, haz clic en **Biblioteca de software** > **Administración de aplicaciones** > **Aplicaciones**.

2. En la lista de aplicaciones, selecciona la aplicación que hayas creado anteriormente. Luego, en la pestaña **Inicio**, en el grupo **Implementación**, haz clic en **Implementar**, o haz clic con el botón secundario en la aplicación y selecciona **Implementar**.

    ![Implementar la aplicación](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. En la página **General** del **Asistente para implementar software**, haz clic en **Examinar** para seleccionar la colección de dispositivos en la que quieres implementar la aplicación.

    ![Busca el archivo de instalación](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. En la página **Contenido**, comprueba que el punto de distribución desde el que quieres que los PC instalen la aplicación esté seleccionado.

    ![Especificar punto de distribución](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. En la página **Configuración de implementación**, asegúrate de que la acción de implementación esté establecida en **Instalar** y que el propósito de la implementación esté establecido en **Requerido**.

    ![Configurar las opciones de la implementación](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    >Al establecer el propósito de implementación en **Requerido**, te aseguras de que la aplicación esté instalada en los PC que cumplan con los requisitos que estableciste. Si estableces este valor en **Disponible**, los usuarios pueden instalar la aplicación a petición desde el Centro de software.  

6. En la página **Programación**, puedes configurar cuándo se instalará la aplicación. Para este ejemplo, selecciona **Lo antes posible después del tiempo disponible**.

    ![Programar la implementación](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. En la página **Experiencia de usuario**, selecciona los valores deseados y haz clic en **Siguiente**.

    ![Especificar la experiencia del usuario](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. Especifica las opciones de alerta deseadas y haz clic en **Siguiente**.

    ![Especificar la configuración de alertas](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. Completa el asistente.

Usa la información de la siguiente sección **Supervisar la aplicación** para ver el estado de la implementación de la aplicación.  

## <a name="monitor-the-application"></a>Supervisar la aplicación

 En esta sección, echaremos un vistazo rápido al estado de implementación de la aplicación que acabas de implementar.  

### <a name="to-review-the-deployment-status"></a>Para revisar el estado de implementación  

1. En la consola de Administrador de configuración, haga clic en **Supervisión** > **Implementaciones**.  

2. En la lista de implementaciones, selecciona la aplicación.

    ![Supervisar la implementación](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. En la pestaña **Inicio** del grupo **Implementación**, haga clic en **Ver estado**.  

4. Selecciona una de las siguientes pestañas para ver más actualizaciones de estado sobre la implementación de la aplicación:  

    - **Correcto**: la aplicación se instaló correctamente en los PC indicados.  

    - **En curso**: la aplicación aún no ha finalizado la instalación.  

    - **Error**: se ha producido un error al instalar la aplicación en los PC indicados. También se muestra información adicional sobre el error.  

    - **Requisitos no cumplidos**: no se realizó ningún intento de instalación en los dispositivos indicados porque no cumplían los requisitos que configuraste (en este ejemplo, porque no ejecutan Windows 10).

    - **Desconocido**: Administrador de configuración no pudo informar del estado de la implementación. Vuelve a consultar más tarde.  

    >[!TIP]
    >Existen diversas formas en las que puedes supervisar las implementaciones de aplicaciones. Para obtener más información, consulta [Supervisar aplicaciones desde la consola de System Center Configuration Manager](/sccm/apps/deploy-use/monitor-applications-from-the-console).  

## <a name="end-user-experience"></a>Experiencia de usuario final  

Los usuarios que dispongan de PC administrados por el Administrador de configuración que ejecuten Windows 10 para la arquitectura de procesador especificada verán un mensaje en el que se les indica que deben instalar la aplicación de Microsoft Edge Dev. Cuando acepten esta opción de instalación, se instalará la aplicación.  

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Crear e implementar una aplicación con System Center Configuration Manager.](/sccm/apps/get-started/create-and-deploy-an-application)