---
title: ClickOnce y DirectInvoke en Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Aprende sobre ClickOnce y DirectInvoke en Microsoft Edge.
ms.openlocfilehash: 3d124f141e9212ba5ab25d4b725d32add62077a3
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642056"
---
# <a name="understand-the-clickonce-and-directinvoke-features-in-microsoft-edge"></a>Conocer las funciones de ClickOnce y DirectInvoke en Microsoft Edge

ClickOnce y DirectInvoke son funciones disponibles en IE y Microsoft Edge (versión 45 y versiones anteriores) que admiten el uso de un controlador de archivos para descargar archivos desde un sitio web. Aunque sirven para fines diferentes, ambas funciones permiten que los sitios web especifiquen que un archivo solicitado para descarga se pasa a un controlador de archivos en el dispositivo del usuario. El controlador de archivos nativo de Windows controla las solicitudes de ClickOnce. Las solicitudes DirectInvoke se controlan mediante un controlador de archivos registrado especificado mediante el sitio web que hospeda el archivo.

Para obtener más información sobre estas funciones, consulta:

- [ClickOnce](/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [DirectInvoke]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> Actualmente, Chromium no proporciona compatibilidad nativa para ClickOnce ni DirectInvoke.

## <a name="overview-prerequisites-and-process"></a>Introducción: requisitos previos y proceso

Para que ClickOnce y DirectInvoke funcionen como se espera y para que el controlador de archivos se solicite correctamente, el controlador de archivos debe estar registrado en el sistema operativo como compatible con ClickOnce o DirectInvoke. Este registro suele producirse cuando está instalado el sistema operativo original o cuando un programa nuevo que está instalado solicita la capacidad de usar DirectInvoke para actualizaciones.

Cuando un sitio web recibe una solicitud de descarga que requiera ClickOnce o DirectInvoke, tienen lugar las siguientes acciones:

- El sitio web solicita que el explorador use un controlador de archivo especificado.
- El explorador comprueba el Registro del sistema operativo para ver si el controlador de archivos está registrado para el tipo de archivo solicitado.
- Si el controlador de archivos está registrado, el explorador llama al controlador de archivos y pasa la dirección URL como argumento al controlador de archivos.
- El controlador de archivos procesa la dirección URL y descarga el archivo.

  > [!NOTE]
  > La dirección URL se usa para determinar el origen del archivo, así como los parámetros que se deben usar para acceder al archivo.  Por ejemplo: puntos de conexión, un manifiesto o metadatos.

## <a name="use-cases"></a>Casos de uso

Los siguientes casos de uso son representativos.

Puedes usar ClickOnce para implementar y actualizar fácilmente software en dispositivos con interacción mínima del usuario. Los usuarios pueden instalar y ejecutar una aplicación Windows haciendo clic en un vínculo de una página web. Si se configura correctamente, la aplicación ClickOnce puede instalar programas sin que los usuarios establezcan configuraciones para el instalador. Por ejemplo, las ubicaciones de los archivos, las opciones de instalación, etc.

Los casos de uso de DirectInvoke dependen del propósito del sitio web que solicita DirectInvoke. Por ejemplo, la función de edición de archivos colaborativa de Microsoft Word. En lugar de hacer clic en un vínculo y descargar toda la copia de un documento en el que estás trabajando con tus colegas, DirectInvoke te permite descargar las partes del documento que se han cambiado. Esta estrategia reduce la cantidad de datos transferidos y puede reducir el tiempo necesario para abrir el documento.  

## <a name="current-support-for-clickonce-and-directinvoke-in-microsoft-edge"></a>Compatibilidad actual de ClickOnce y DirectInvoke en Microsoft Edge

Compatibilidad con ClickOnce y DirectInvoke:

- ClickOnce y DirectInvoke son compatibles de forma predeterminada para todos los usuarios de Windows.

  > [!NOTE]
  > Los usuarios que quieran deshabilitar la compatibilidad con ClickOnce pueden ir a *edge://flags/#edge-click-once* y seleccionar **Deshabilitar** en la lista desplegable. Posteriormente tendrás que **Reiniciar** el explorador.

- ClickOnce y DirectInvoke no son compatibles con ninguna otra plataforma que no sea Windows.

## <a name="clickonce-and-directinvoke-file-handling-security"></a>Seguridad de administración de archivos de ClickOnce y DirectInvoke

ClickOnce y DirectInvoke están protegidos por el servicio de análisis de reputación de direcciones URL de SmartScreen de Microsoft Defender.

Si el servicio de reputación de direcciones URL de SmartScreen de Microsoft Defender marca una solicitud ClickOnce o DirectInvoke como no segura, los usuarios con ClickOnce o DirectInvoke habilitado verán dos ventanas emergentes.

El primer elemento emergente pregunta al usuario si desea abrir el archivo. Este elemento emergente se muestra independientemente de si el archivo se marcó como seguro o no seguro. El usuario puede **Informar del archivo como no seguro**, **Cancelar** la solicitud o hacer clic en **Abrir** para continuar.

   ![Aviso de abrir archivo](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

Si el usuario intenta abrir el archivo y el archivo se marcó como no seguro, se muestra un segundo elemento emergente.  Este elemento emergente advierte al usuario de que el archivo se marcó como no seguro y le pregunta si está seguro de que desea descargar el archivo.

El segundo elemento emergente solo aparece si:

- el archivo es un archivo ClickOnce o DirectInvoke
- ClickOnce o DirectInvoke están habilitados
- el archivo está marcado como no seguro

 ![Aviso de abrir un archivo no seguro](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> Si se deshabilitan ClickOnce o DirectInvoke, los archivos solicitados se tratan como descargas normales y, si están marcados como no seguros, se registrarán como no seguros. Esto es coherente con el tratamiento de otras descargas no seguras.

## <a name="clickonce-and-directinvoke-policies"></a>Directivas ClickOnce y DirectInvoke

Hay dos directivas de grupo que puedes usar para habilitar o deshabilitar ClickOnce y DirectInvoke para los usuarios de empresa. Estas dos directivas son [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled) y [DirectInvokeEnabled](./microsoft-edge-policies.md#directinvokeenabled). Estas dos directivas se etiquetan en el Editor de directivas de grupo como "Permitir que los usuarios abran archivos mediante el protocolo ClickOnce" y "Permitir que los usuarios abran archivos mediante el protocolo DirectInvoke", respectivamente.

## <a name="clickonce-and-directinvoke-behavior"></a>Comportamiento ClickOnce y DirectInvoke

En los siguientes ejemplos se muestra el control de archivos cuando se habilitan o deshabilitan ClickOnce y DirectInvoke.

### <a name="clickonce-enabled"></a>ClickOnce habilitado

1. Un usuario abre un vínculo a una página que solicita soporte de ClickOnce y recibe el aviso de la siguiente captura de pantalla.

   ![Aviso de abrir un archivo no seguro](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. Después de que el usuario haga clic en **Abrir**, ClickOnce intenta iniciar la aplicación.

   ![ClickOnce intenta iniciar la aplicación](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. Cuando el usuario hace clic en **Abrir**, el explorador muestra un elemento emergente que pregunta al usuario si está seguro de que desea instalar la aplicación.

   ![Aviso de abrir el archivo](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > La interfaz, los mensajes y las opciones mostradas mediante el controlador de archivos de ClickOnce variará según el tipo y la configuración del archivo al que se accede.

### <a name="clickonce-disabled"></a>ClickOnce deshabilitado

1. Cuando un usuario abre un vínculo a una página que solicita compatibilidad con ClickOnce, verá un mensaje en la bandeja de descarga similar al que se muestra en la siguiente captura de pantalla.

   ![Aviso de descarga de archivo](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### <a name="directinvoke-enabled"></a>DirectInvoke habilitado

1. Un usuario abre un vínculo a una página que solicita soporte de DirectInvoke y recibe el aviso de la siguiente captura de pantalla.

   ![Aviso de abrir archivo](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. Cuando el usuario hace clic en **Abrir**, se abrirá el controlador de archivos solicitado. En este ejemplo, se usa Microsoft Word para abrir el documento que se muestra en la captura de pantalla anterior.

   > [!NOTE]
   > La interfaz, los mensajes y las opciones mostradas mediante el controlador de archivos de DirectInvoke variará según el tipo y la configuración del archivo al que se accede.

### <a name="directinvoke-disabled"></a>DirectInvoke deshabilitado

1. Cuando un usuario abre un vínculo a una página que solicita soporte de DirectInvoke, DirectInvoke se comporta del mismo modo que cuando se deshabilita ClickOnce. Aparecerá un mensaje en la bandeja de descargas similar al que se muestra en la siguiente captura de pantalla.

   ![Aviso de abrir archivo](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## <a name="see-also"></a>Consulta también

- [Seguridad e implementación de ClickOnce](/visualstudio/deployment/clickonce-security-and-deployment)
- [DirectInvoke en Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/jj215788(v=vs.85))
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)