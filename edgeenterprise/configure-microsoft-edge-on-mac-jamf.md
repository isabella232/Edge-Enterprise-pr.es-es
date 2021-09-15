---
title: Configurar Microsoft Edge en macOS con Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 6/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configurar las opciones de directiva de Microsoft Edge en dispositivos Mac con Jamf
ms.openlocfilehash: 8556a5b1d0fc01feb67fc86cb016a9ed47061b55
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979742"
---
# <a name="configure-microsoft-edge-policy-settings-on-macos-with-jamf"></a>Configurar las opciones de directiva de Microsoft Edge en macOS con Jamf

Este artículo describe cómo configurar las opciones de directiva en macOS con un archivo de manifiesto de directiva de Microsoft Edge en Jamf Pro 10.19.

También puede configurar las opciones de directiva de Microsoft Edge en macOS mediante un archivo de lista de propiedades (.plist). Para obtener más información, consulte [configurar para macOS con un archivo .plist](configure-microsoft-edge-on-mac.md)


## <a name="prerequisites"></a>Requisitos previos

Se necesita el siguiente software:

- Canal 81 Microsoft Edge Stable
- Archivo de plantillas de directiva, versión 81.0.416.3
- Jamf Pro, versión 10.19

## <a name="about-the-jamf-pro-application--custom-settings-menu"></a>Acerca del menú de configuración personalizada y de la aplicación de Jamf Pro

Antes de Jamf Pro 10,18, administrar Office 365 suponía la creación manual de un archivo .plist. Este era un flujo de trabajo muy largo que requería sólidos conocimientos técnicos. Jamf Pro 10.18 eliminó estos obstáculos al simplificar el proceso de configuración. Sin embargo, los administradores de TI solo podrían usar esta nueva interfaz de usuario para aplicaciones específicas y dominios de preferencias especificados por Jamf.

En Jamf Pro 10.19, un usuario puede cargar un manifiesto JSON como "esquema personalizado" para dirigirse a cualquier dominio de preferencias, y la interfaz de usuario gráfica se generará a partir de este manifiesto. El esquema personalizado que se crea sigue la especificación de esquema JSON.

Para obtener más información, vea [perfiles de configuración del equipo](https://jamf.it/computer-configuration-profiles) en la guía del administrador de Jamf Pro.

## <a name="get-the-policy-manifest-for-a-specific-version-of-microsoft-edge"></a>Obtener el manifiesto de directiva para una versión específica de Microsoft Edge

Para obtener el manifiesto de directiva:

- Diríjase a la [Página de inicio Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).
- En la lista desplegable Canal/Versión, seleccione **cualquier canal con la versión 81 o posterior.***
- En la lista desplegable Compilación, seleccione cualquier **compilación del 81 o posterior.***.
- Haga clic en obtener archivos de directiva para descargar nuestro paquete de plantillas de directivas.

  > [!NOTE]
  > Actualmente, el conjunto de plantillas de directiva está firmado como archivo CAB. Tendrá que usar una herramienta de terceros, como The Unarchiver para abrir el archivo en macOS.

Después de desempaquetar el archivo CAB, desempaquete el archivo ZIP y vaya al directorio "mac" de nivel superior. El manifiesto, denominado "policy_manifest.json", se encuentra en este directorio.

Este manifiesto se publicará en cada paquete de directivas empezando con la compilación 81.0.416.3. Si desea probar directivas en el canal de desarrollo, puede tomar el manifiesto asociado a cada lanzamiento de desarrollo y probarlo en Jamf Pro.  

## <a name="use-the-policy-manifest-in-jamf-pro"></a>Usar el manifiesto de directiva en Jamf Pro

Siga los pasos siguientes para cargar el manifiesto de directiva en Jamf Pro y crear un perfil de directiva para macOS.

1. Inicie sesión en Jamf.
2. Seleccione la pestaña **equipo**.
3. En **administración de contenido**, seleccione **perfiles de configuración**.
4. En la página **perfiles de configuración**, haga clic en **+ nuevo**.

   ![Agregar un perfil nuevo en Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. En **Nuevo perfil de configuración de macOS**>**opciones**, seleccione **aplicación y configuración personalizada**.
6. En la ventana emergente **configuración personalizada y de la aplicación**, haga clic en **configurar**.

   ![Configurar la aplicación y la configuración personalizada](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. En la sección **aplicación y configuración personalizada**, configure los valores que se muestran en la siguiente captura de pantalla.

   ![Origen de perfil y esquema personalizado](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - Para **método de creación**, elija **configurar las opciones**.
   - Para **origen**, elija **esquema personalizado**.
   - Para **dominio de preferencia**, proporcione el nombre de su dominio. Este ejemplo usa *com.microsoft.Edge* como dominio.
   - Para **esquema personalizado**, pegue el contenido del archivo de manifiesto "policy_manifest.json".
   - Haga clic en **Guardar**.

8. Después de guardar el perfil, Jamf muestra la sección **general** que se muestra en la siguiente captura de pantalla.

   ![Configurar la sección general](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - Proporcione un **nombre** para mostrar para el perfil y una **descripción**.
   - Conserve la configuración predeterminada para **categoría**, que es **ninguna**.
   - Para **método de distribución**, las opciones son **instalar automáticamente** o **estar disponibles en autoservicio**.
   - Para **nivel**, las opciones son **nivel de usuario** o **nivel de equipo**.
   - Haga clic en **Guardar**.

9. Después de guardar la sección General, Jamf muestra el perfil de configuración "canal de Microsoft Edge Beta" configurado en nuestro ejemplo. En la siguiente captura de pantalla, tenga en cuenta que puede seguir trabajando con el perfil si hace clic en **editar** o bien, si ya ha terminado, haga clic en **listo**.

   ![Nuevo perfil de configuración con opciones](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > Puede editar este perfil después de que se haya guardado y en otra sesión de Jamf. Por ejemplo, podría decidir cambiar el método de distribución para que esté disponible en autoservicio.

   Para hacer una edición de seguimiento en el Microsoft Edge Stable Channel, o para eliminarlo, seleccione el nombre del perfil, que se muestra en la siguiente captura de pantalla de Perfiles de configuración.

   ![Lista de perfiles de configuración](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

Después de crear el nuevo perfil de configuración aún tiene que configurar el **ámbito** del perfil.

### <a name="to-configure-the-scope"></a>Para configurar el ámbito

1. Para **destinos**, proporcione la siguiente configuración mínima:

   - EQUIPOS DE DESTINO. Las opciones son equipos específicos o todos los equipos.
   - USUARIOS DE DESTINO. Las opciones son usuarios específicos o todos los usuarios.
   - Haga clic en **Guardar**.
2. Para **limitaciones**, conserve la configuración predeterminada: ninguna. Haga clic en **Cancelar**.
3. Para **exclusiones**, conserve la configuración predeterminada: ninguna. Haga clic en **Cancelar**.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar para macOS con Intune](configure-microsoft-edge-on-mac.md)
- [Configurar para Windows](configure-microsoft-edge.md)
- [Configurar para Windows con Intune](configure-edge-with-intune.md)
