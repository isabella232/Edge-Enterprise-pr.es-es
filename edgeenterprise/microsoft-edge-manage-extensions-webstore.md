---
title: Extensiones de Microsoft Edge de prueba interna
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 04/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Obtenga información sobre cómo empaquetar y probar internamente extensiones de Microsoft Edge en la empresa.
ms.openlocfilehash: 403b6879b15c146f40fa2564da76eae59b2abe88
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618274"
---
# <a name="self-host-microsoft-edge-extensions"></a>Extensiones de Microsoft Edge de prueba interna

En este artículo se proporcionan instrucciones básicas para empaquetar una extensión para hospedarla en su propia tienda web. También incluye instrucciones sobre cómo implementar extensiones en dispositivos y usuarios de la organización.

## <a name="prerequisites"></a>Requisitos previos

Para probar internamente sus propias extensiones, deberá proporcionar sus propios servicios de hospedaje web para las extensiones y sus archivos de manifiesto.

 En los pasos siguientes se presupone que ya ha creado la extensión, tiene cierta experiencia con archivos XML, tiene conocimientos prácticos sobre la configuración de la directiva de grupo y sabe cómo usar el Registro de Windows.

## <a name="publish-an-extension"></a>Publicación de una extensión

Antes de publicar una extensión, debe empaquetarse en un archivo CRX (extensión de Chrome). Siga estos pasos como guía para empaquetar una extensión como un archivo CRX.

1. En la barra de direcciones de Microsoft Edge, vaya a *edge://extensions* y active **Modo de desarrollador** si aún no está habilitado.
2. En **Extensiones instaladas**, haga clic en **Extensión del paquete** para crear el archivo CRX.
3. Use el cuadro de diálogo **Extensión del paquete** para buscar el directorio que tiene el origen de la extensión. Seleccione el directorio y haga clic en **Extensión del paquete**.  Esto creará el archivo CRX, junto con un archivo PEM. Guarde el archivo PEM, ya que es necesario para realizar actualizaciones de versión en la extensión. En la captura de pantalla siguiente se muestra el cuadro de diálogo **Extensión del paquete** para buscar el directorio raíz de la extensión.

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="Cuadro de diálogo Extensión del paquete para buscar el código fuente de una extensión.":::

   > [!IMPORTANT]
   > Almacene el archivo PEM en una ubicación segura, ya que es la clave de la extensión y es necesaria para futuras actualizaciones.

4. Arrastre el archivo CRX a la ventana de extensiones y asegúrese de que se carga.
5. Pruebe la extensión y anote el campo de Id. (es decir, el Id. de CRX) y el número de versión. Necesitará esta información más adelante. En la captura de pantalla siguiente se muestra una extensión de prueba con su identificador de CRX.

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="Ejemplo de extensión que muestra el Id. de CRX":::

6. Cargue el archivo CRX en el host y anote la dirección URL de la ubicación desde la que se descargará. Esta información es necesaria para el archivo de manifiesto XML.
7. Para crear un archivo XML de manifiesto con el identificador de aplicación o extensión, la dirección URL de descarga y la versión, defina los campos siguientes:  

   - **appid**: el identificador de extensión del paso 5
   - **codebase**: la ubicación de descarga del archivo CRX del paso 6
   - **version**: la versión de la aplicación o extensión, que debe coincidir con la versión especificada en el manifiesto de la extensión.

   El siguiente fragmento de código muestra un ejemplo de un archivo de manifiesto XML.

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   Para más información, vea [Actualizar extensiones automáticamente en Microsoft Edge: desarrollo de Microsoft Edge](/microsoft-edge/extensions-chromium/enterprise/auto-update).

8. Cargue el archivo XML completado en una ubicación desde la que se pueda descargar y anote la dirección URL. Esta dirección URL será necesaria cuando instale la extensión mediante una directiva de grupo. Vea [Distribuir una extensión hospedada de forma privada](#distribute-a-privately-hosted-extension).

   > [!IMPORTANT]
   > La ubicación de hospedaje de la extensión no necesita autenticación. Los dispositivos de usuario deben tener acceso a ella dondequiera que se puedan usar.

## <a name="publish-updates-to-an-extension"></a>Publicación de actualizaciones en una extensión

Después de cambiar y probar la extensión actualizada, puede publicarla. Siga estos pasos como guía para publicar una actualización.

1. Cambie el número de versión en el archivo manifest.JSON de la extensión a un número mayor mediante la sintaxis siguiente: `"version":"versionString"`. Si "version":"1.0", puede actualizar a "version":"1.1" o a cualquier número superior a "1.0".
2. Actualice la "versión" de `<updatecheck>` en el archivo XML para que coincida con el número que colocó en el archivo de manifiesto en el paso anterior. Por ejemplo:<br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. Cree un archivo CRX que incluya los nuevos cambios. Vaya a *edge://extensions* y habilite **Modo de desarrollador**.
4. Haga clic en **Extensión del paquete** y vaya al directorio del origen de la extensión.

   > [!IMPORTANT]
   > Use el mismo archivo PEM que se generó y guardó la primera vez que se creó el archivo CRX. Si no usa el mismo archivo PEM, el identificador de aplicación de la extensión cambiará y la actualización se tratará como una nueva extensión.

5. Arrastre y coloque el archivo CRX en la ventana de extensiones y compruebe que se carga.
6. Pruebe la extensión actualizada.
7. Reemplace el archivo CRX antiguo y el archivo XML por los nuevos archivos de la extensión actualizada.

Los cambios de la extensión se tomarán durante el siguiente ciclo de sincronización de directivas. Para más información acerca de la actualización de extensiones, vea: [Actualizar URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) y [Actualizar manifiesto](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).

## <a name="distribute-a-privately-hosted-extension"></a>Distribución de una extensión hospedada de forma privada

Puede compartir el vínculo de la ubicación donde se hospeda el archivo CRX y, en cuanto los usuarios escriban la dirección URL en su explorador, la extensión se descargará e instalará. Los usuarios pueden habilitar la extensión desde la página edge://extensions. Para permitir que los usuarios instalen extensiones de prueba interna, debe agregar los identificadores de CRX de extensión a la directiva [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist).

Como alternativa, puede usar la directiva de grupo [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) para forzar la instalación de una extensión en los dispositivos de los usuarios.

Puede aplicar estas directivas a los usuarios seleccionados, dispositivos o ambos. Recuerde que las actualizaciones de directivas no son instantáneas y la configuración de directiva tardará tiempo en surtir efecto.

## <a name="see-also"></a>Vea también

- [Administrar extensiones de Microsoft Edge en la empresa](microsoft-edge-manage-extensions.md)
- [Usar directivas de grupo para administrar extensiones de Microsoft Edge](microsoft-edge-manage-extensions-policies.md)
- [Guía detallada de la directiva ExtensionSettings](microsoft-edge-manage-extensions-ref-guide.md)
- [Preguntas más frecuentes sobre extensiones de Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
