---
title: Automatizar Microsoft Edge para la implementación en macOS con Microsoft Intune
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 11/30/2019
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Cómo automatizar Microsoft Edge para la implementación en macOS con Jamf.
ms.openlocfilehash: e56ed4c2a9c0ebb4a4341830cd09ca040e80a657
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617530"
---
# <a name="deploy-to-macos-with-jamf"></a>Implementar en macOS con Jamf

En este artículo se describe cómo implementar Microsoft Edge para macOS usando Jamf.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="prerequisites"></a>Requisitos previos

Antes de implementar Microsoft Edge, asegúrate de cumplir los requisitos previos siguientes:

- El archivo de instalación de Microsoft Edge, **MicrosoftEdgeDev-\<version\>.pkg** está en una ubicación accesible de la red. Puedes descargar los archivos de instalación de Microsoft Edge Enterprise desde la [página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).
- Tienes una cuenta de nube de Jamf con el nivel de acceso y privilegios necesarios para crear e implementar archivos de instalación en equipos.

## <a name="to-deploy-microsoft-edge-using-jamf"></a>Para implementar Microsoft Edge con Jamf:

1. Inicia sesión en Jamf y ve a **Toda la configuración**.

    ![Abrir Toda la configuración](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. En **Toda la configuración**, haz clic en **Administración de equipos**.

    ![Selecciona Administración de equipos.](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. En **Administración de equipos**, haz clic en **Paquetes**.

    ![Seleccionar Paquetes](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. En la página **Paquetes**, haz clic en **+ Nuevo** para agregar un nuevo paquete.

    ![Seleccionar Nuevo para agregar un nuevo paquete](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. En la página **Nuevo paquete**, escribe los detalles del paquete y, a continuación haz clic en **Guardar**. (Por ejemplo, NOMBRE PARA MOSTRAR, INFORMACIÓN o NOTAS).

    ![Seleccionar Guardar para guardar la información del paquete](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. Selecciona **Equipos** en la barra de menús y, a continuación, selecciona **Directivas** en la barra de navegación.

7. Selecciona **+ Nuevo** para mostrar el panel **Nueva directiva**.

    ![Seleccionar Nuevo para crear una nueva directiva](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. En la pestaña **Opciones**, selecciona **General**.

    - En **NOMBRE PARA MOSTRAR**, escribe el nombre para mostrar de la directiva.
    - En **Desencadenador**, selecciona el evento que desencadenará la nueva directiva. (En el siguiente ejemplo, el evento es Inicio).

    ![Escribir la información sobre implementación](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. En la pestaña **Opciones**, haz clic en **Paquetes**.

10. En el menú emergente **Configurar paquetes**, haz clic en **Configurar**.

    ![Configurar el paquete](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. El paquete que agregaste se muestra en el panel **Paquetes**. Haz clic en **Agregar**. En este ejemplo, el paquete es "MicrosoftEdgeBeta" en la siguiente captura de pantalla.

    ![Agregar paquete](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. En la página **Nueva directiva**, usa las listas desplegables para seleccionar el **PUNTO DE DISTRIBUCIÓN** y la **ACCIÓN** a tomar para la directiva. Haz clic en **Guardar**. La captura de pantalla siguiente usa el "Punto de distribución predeterminado de cada equipo" e "Instalar" como ejemplo.

    ![Seleccionar punto de distribución y acción](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. En la página **Nueva directiva**, selecciona la pestaña **Ámbito**. Puedes administrar el ámbito de la implementación en función de los equipos o los usuarios. Para este ejemplo, selecciona **Todos los equipos** en la lista desplegable **EQUIPOS DE DESTINO** y, a continuación, haz clic en **Guardar**.

    ![Seleccionar el ámbito de la implementación](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. En este punto, puedes revisar la directiva de implementación de Microsoft Edge. Si las opciones de implementación cumplen los requisitos, haz clic en **Listo**.

    ![Hacer clic en Listo](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > Puedes volver a una directiva de implementación en cualquier momento para cambiar la configuración.

¡Enhorabuena! Acabas de finalizar la configuración Jamf para implementar Microsoft Edge para macOS. Cuando la condición de desencadenador que definiste sea verdadera, el paquete se implementará en los equipos que especificaste.

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Jamf.com](https://www.jamf.com/)
- [Integrar Jamf con Microsoft Intune](/intune/conditional-access-integrate-jamf)