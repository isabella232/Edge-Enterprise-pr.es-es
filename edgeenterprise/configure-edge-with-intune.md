---
title: Configurar la directiva de Microsoft Edge para Windows con Microsoft Intune
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configurar la directiva de Microsoft Edge para Windows con Microsoft Intune.
ms.openlocfilehash: 63eb29018bf4ec9c5a32d11b215f422e150383c9
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979832"
---
# <a name="configure-microsoft-edge-policy-settings-with-microsoft-intune"></a>Configurar la directiva de Microsoft Edge con Microsoft Intune

Este artículo explica cómo configurar la directiva de Microsoft Edge para Windows 10 con Microsoft Intune.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

Puedes configurar las directivas y opciones de Microsoft Edge agregando un perfil de configuración de dispositivo a Microsoft Intune. El uso de Intune para administrar y aplicar directivas es esencialmente equivalente al uso de la directiva de grupo de Active Directory o a la configuración de Objeto de directiva de grupo (GPO) local en los dispositivos de usuario.

Para obtener más información acerca de la administración de directivas de Microsoft Edge con Microsoft Intune, puedes leer [Administrar el acceso a la Web usando Microsoft Edge con Microsoft Intune](/intune/manage-microsoft-edge), pero ten en cuenta que el artículo vinculado es específico de las versiones 45 y anteriores de Microsoft Edge, por lo que puede contener información y referencias que no se aplican a las versiones 77 y posteriores de Microsoft Edge Enterprise.

> [!TIP]
> Para obtener información sobre cómo configurar Microsoft Edge en macOS con Microsoft Intune, consulte [Configurar para macOS](configure-microsoft-edge-on-mac.md).

## <a name="create-a-profile-to-manage-settings-in-microsoft-edge-for-windows-10"></a>Crear un perfil para administrar la configuración de Microsoft Edge para Windows 10

Con las plantillas administrativas de Microsoft Intune, puedes administrar directivas de grupo de Microsoft Edge en los dispositivos con Windows 10 mediante la nube. Esta sección te ayudará a crear una plantilla para configurar opciones de aplicaciones específicas para Microsoft Edge. Al crear la plantilla, se crea un perfil de configuración de dispositivo. A continuación, puedes asignar o implementar este perfil en los dispositivos con Windows 10 de la organización.

### <a name="prerequisites"></a>Requisitos previos

- Windows 10 con los siguientes requisitos mínimos del sistema:
  - Windows 10 versión 1909
  - Windows 10, versión 1903 con [KB4512941](https://support.microsoft.com/kb/4512941) instalada
  - Windows 10, versión 1809 con [KB4512534](https://support.microsoft.com/kb/4512534) instalada
  - Windows 10, versión 1803 con [KB4512509](https://support.microsoft.com/kb/4512509) instalada
  - Windows 10, versión 1709 con [KB4516071](https://support.microsoft.com/kb/4516071) instalada

### <a name="use-administrative-templates-to-create-a-policy-for-microsoft-edge"></a>Use plantillas administrativas para crear una directiva para Microsoft Edge

Este procedimiento aprovecha las plantillas administrativas (que es posible que esté familiarizado con la Directiva de grupo) que están integradas en Intune. Para crear una directiva para Microsoft Edge, puede usar estas plantillas seleccionando configuración en una lista preconfigurada.

1. Inicie sesión en el portal [Microsoft Endpoint Manager](https://endpoint.microsoft.com/).
2. Seleccione **Dispositivos** en el panel de navegación de la parte izquierda.
3. Desde **dispositivos** | **Información general**, seleccione **Perfiles de configuración** (en el encabezado Directiva).
4. En la barra de comandos superior, selecciona **Crear perfil**.
5. En la lista desplegable que se muestra debajo de **Plataforma**, seleccione **Windows 10 y luego**.
6. En la lista desplegable debajo de **Tipo de perfil**, seleccione **Plantillas**.
7. En Nombre **de plantilla,** seleccione **Plantillas administrativas** y, a continuación, haga clic en **el botón** Crear. La siguiente captura de pantalla muestra las listas desplegables para seleccionar la plataforma y el tipo de perfil.

    ![Seleccionar plataforma y tipo de perfil](./media/configure-edge-with-intune/create-profile-platform.png)

7. En la pestaña **Datos básicos**, escriba un **nombre** descriptivo, como la directiva de Microsoft Edge. Opcionalmente, escriba una **Descripción** de la directiva.
La siguiente captura de pantalla muestra el formulario para la pestaña **Datos básicos** y la barra de menús muestra los pasos siguientes (como pestañas atenuadas) para crear el perfil.

   ![Escriba el nombre y la descripción](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. Selecciona **Siguiente**.
9. En la pestaña **Opciones de configuración**, seleccione la carpeta Microsoft Edge en una de las siguientes ubicaciones:

   - debajo de la carpeta configuración del equipo
   - debajo de la carpeta configuración del usuario

   La configuración disponible para Microsoft Edge se mostrará en el panel derecho. Por ejemplo, en la siguiente captura de pantalla, puede ver *Configuración de equipo/Microsoft Edge/Permitir restricciones de descarga*.

   ![Pestaña de opciones de configuración](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > Para obtener la lista de todas las opciones disponibles de Microsoft Edge, vea [Microsoft Edge: directivas](./microsoft-edge-policies.md) y [Microsoft Edge: directivas de actualización](./microsoft-edge-update-policies.md).

10. Use el campo de búsqueda ("buscar para filtrar elementos...") para buscar una configuración específica que desee configurar. En este ejemplo, la cadena de búsqueda es "Página principal". La siguiente captura de pantalla muestra los resultados de la búsqueda.

    ![Resultados de la búsqueda](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. Cuando encuentre la configuración que desea configurar, selecciónela para mostrar los valores que se pueden establecer. En la siguiente captura de pantalla, selecciono "configurar la dirección URL de la página principal" como ejemplo.

    ![Configurar la dirección URL de la página principal](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. Habilite la directiva y escriba un valor para la dirección URL de la página principal, como se muestra en la captura de pantalla anterior.

13. Haga clic en **Aceptar**. La columna de configuración "Estado" debería aparecer como "Activado", como se muestra en el siguiente ejemplo de captura de pantalla.

    ![El estado de configuración está habilitado](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. Haga clic en el botón **Siguiente**.

15. En la pestaña **Etiquetas de ámbito**, agregue una etiqueta de ámbito si lo desea. en caso contrario, haga clic en el botón **siguiente**.

16. En la pestaña **Tareas**, haga clic en **+ seleccionar grupos para incluir** asignar esta directiva al grupo de Azure Active Directory (Azure AD) que contiene los dispositivos o los usuarios que quiere que reciban esta configuración de directiva. Vea [Asignar perfiles de usuario y dispositivo en Microsoft Intune](/intune/device-profile-assign) para obtener información sobre cómo asignar el perfil a los grupos de usuarios o dispositivos de Azure AD.

    ![Seleccionar grupos para incluir](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. Haga clic en el botón **Siguiente**.

18. En la pestaña **Revisar + crear**, revise el resumen de los cambios para asegurarse de que es correcto y, a continuación, haga clic en el botón **Crear**.

19. La directiva recién creada (directiva de Microsoft Edge) se muestra en la siguiente captura de pantalla.

    ![Seleccionar grupos para incluir](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

Para obtener más información acerca de los perfiles de Windows 10, consulta [Uso de plantillas de Windows 10 para configurar la directiva de grupo en Microsoft Intune](/intune/administrative-templates-windows).

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Administrar el acceso a la Web usando Microsoft Edge con Microsoft Intune](/intune/manage-microsoft-edge)
- [Usa plantillas de Windows 10 para configurar las opciones de la directiva de grupo en Microsoft Intune](/intune/administrative-templates-windows)
- [Implementar Microsoft Edge con Microsoft Intune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
