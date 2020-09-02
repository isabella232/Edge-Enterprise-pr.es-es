---
title: Reversión de Microsoft Edge para empresas
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 07/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Cómo revertir Microsoft Edge a una versión anterior
ms.openlocfilehash: 9af0881a079dd3059e567eaadb912b3d929924c4
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981127"
---
# Cómo revertir Microsoft Edge a una versión anterior

Este artículo describe cómo revertir a una versión anterior de Microsoft Edge con la característica de reversión.

>[!NOTE]
>Este artículo se aplica a Microsoft Edge, versión 86 o posterior.

## Introducción a la característica de reversión

La reversión permite sustituir la versión del navegador Microsoft Edge por una versión anterior. Esta característica está diseñada para servir como red de seguridad para las empresas que implementan Microsoft Edge. Ofrece un método para solucionar problemas con Microsoft Edge. Las ventajas de la reversión son la capacidad para revertir a la versión anterior del explorador de forma fácil y rápida. La reversión reduce el impacto potencial de un problema de Microsoft Edge en las operaciones empresariales.

## Antes de comenzar

Es importante comprender cómo se instala la característica de reversión en un entorno de Microsoft Edge. Es posible implementar la reversión mediante dos métodos distintos: manualmente con un paquete MSI o con Microsoft Edge Update y la directiva de grupo. También recomendamos el uso de una selección de directivas de grupo para una implementación más fluida.

### Recomendaciones

La característica de reversión tiene como objetivo ser una corrección temporal para problemas que se puedan encontrar en una actualización del explorador Microsoft Edge. Se recomienda a los usuarios que instalen la última versión del explorador Microsoft Edge para usar la protección proporcionada por las últimas actualizaciones de seguridad. Revertir a una versión anterior supone un riesgo de exposición a problemas de seguridad conocidos.

Antes de revertir temporalmente a la versión anterior, recomendamos encarecidamente que se habilite la sincronización para todos los usuarios de la organización. Si no se activa la sincronización, se corre el riesgo de pérdida definitiva de datos de búsqueda. Para obtener más información sobre la sincronización, consulte [Sugerencias de Microsoft Edge](microsoft-edge-enterprise-sync.md).

> [!CAUTION]
> Usa la reversión solo cuando sea necesario: siempre se corre el riesgo de perder datos.

## Habilitar la reversión manual con un MSI

Siga los pasos que se indican a continuación para la reversión manual con un MSI.

1. Deshabilite las actualizaciones de Microsoft Edge.

   > [!NOTE]
   > Recomendamos instalar las plantillas administrativas más recientes. Para obtener más información, consulte [Descarga e instala la plantilla administrativa de Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).

   - Abra el editor de directivas de grupo local y vaya a *Configuración del equipo>Plantillas administrativas>Microsoft Edge Update>Aplicaciones>Microsoft Edge>*.
   - Seleccione **Invalidar directiva de actualización** y, a continuación, seleccione **Habilitar**.
   - En **Opciones**, seleccione **Actualización deshabilitada** en la lista desplegable Directiva.

2. Obtenga el MSI.

   - Descargue [desde aquí](https://www.microsoft.com/edge/business/download) el archivo MSI para la versión a la que desea volver.
   - Guarde el MSI en el escritorio.

3. Ejecute el comando de reversión.

   - Abra el símbolo del sistema de Windows con **Ejecutar como administrador**.
   - Escriba el comando siguiente, donde: *C:\Users\username\Desktop\test* es la ruta de acceso al MSI previamente descargado y FileName es el nombre del archivo .msi:<br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > Para obtener más información sobre msiexec, consulte [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).
   - Cierre y vuelva a abrir Microsoft Edge para comprobar que la reversión se ha realizado correctamente. En **Configuración y más** (ALT + F), ve a **Configuración** y seleccione **Acerca de Microsoft Edge**.

## Habilitar la reversión con Microsoft Edge Update y la directiva de grupo

Siga los pasos siguientes para habilitar la reversión con Microsoft Edge Update y la directiva de grupo

1. Abra el editor de directivas de grupo local y vaya a *Configuración del equipo>Plantillas administrativas>Microsoft Edge Update>Aplicaciones>Microsoft Edge>*.
2. Seleccione **Revertir a la versión de destino** y, a continuación, seleccione **Habilitado**.
3. Seleccione **Anular la versión de destino** y elija la versión del explorador a la que se desea revertir.
4. Seleccione **Invalidar directiva de actualización** y, a continuación, seleccione **Habilitar**. En **Opciones**, elija una de las siguientes opciones de la lista desplegable Directiva (excepto **Actualización deshabilitada**):

   - Permitir siempre actualizaciones
   - Solo actualizaciones silenciosas automáticas
   - Solo actualizaciones manuales  

5. La reversión se producirá la próxima vez que Microsoft Edge Update compruebe si hay alguna actualización.

   > [!NOTE]
   > Si se desea que la reversión se realice inmediatamente, se debe cambiar el intervalo de sondeo de Microsoft Edge Update o habilitar la reversión mediante un MSI.

### Errores comunes de reversión

Los siguientes errores impiden la reversión:

- La entrada es una versión de destino no compatible
- La entrada es una versión de destino no existente
- El formato de la entrada es incorrecto

### Directivas de grupo recomendadas

Las siguientes directivas de grupo y configuraciones son muy recomendables para la reversión.

#### Directivas de grupo de sincronización

- ForceSync. Establece ForceSync como habilitado. Esta directiva forzará la habilitación de la sincronización en todos los usuarios de Azure Active Directory (Azure AD). Esta directiva solo es válida para las versiones 86 y posteriores de Microsoft Edge.
- *Configurar la lista de los tipos que se excluyen de la directiva de sincronización* permite a los administradores controlar los datos que los usuarios pueden sincronizar.

#### Reinicio de las directivas de grupo del explorador

Se recomienda forzar un reinicio en los usuarios después de habilitar la reversión.

- Habilite *Notificar al usuario que se recomienda o se requiere el reinicio del navegador para realizar las actualizaciones pendientes*. En opciones, seleccione **Necesario**.
- Habilite *Establecer el período de tiempo de las notificaciones de actualización* y, a continuación, establezca el tiempo deseado en milisegundos.

## Preguntas frecuentes

### Reversión manual mediante MSI

#### ¿Qué errores genéricos de MSI se pueden producir?

1. Si la directiva de grupo Instalar actualización está deshabilitada, no se realizará la reversión.

   - Para usar la reversión, asegúrese de que Instalar está **Habilitada**. Si esta directiva está deshabilitada, impide la instalación de los canales de Microsoft Edge. Para obtener más información, consulte [Instalar](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).

2. Si no hay actualizaciones predefinidas, se bloquearán las instalaciones de Microsoft Edge, a no ser que *Permitir la experiencia de exploradores en paralelo de Microsoft Edge* está habilitada.

   - Para las versiones de Windows 1903 y 1909: Si la última actualización es anterior a octubre de 2019, es posible que tenga este problema.
   - Para las versiones de Windows 1709, 1803 y 1809: Si la última actualización es anterior a noviembre de 2019, es posible que tenga este problema.<br>
Para obtener más información, consulte [Actualizaciones de Windows para admitir la próxima versión de Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)

#### Se mostró el siguiente mensaje de error después de usar el símbolo del sistema y no se realizó la reversión. ¿Cuál es el problema?

![Mensaje de estado de la reversión](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

*ALLOWDOWNGRADE=1* no se ha ejecutado.

### Reversión con Microsoft Edge Update y la directiva de grupo

#### Configuro *Reversión a la versión de destino*, con *Invalidación de directiva de actualización* habilitada; escribo la versión del explorador deseada para *Invalidación de versión de destino*, pero la versión del explorador no es la que esperaba. ¿Cuál es el problema?

Algunos errores comunes que impiden la reversión son:

- Si no se ha establecido Revertir a la versión de destino, la reversión no se ejecutará.
- Existe uno de los siguientes problemas con la configuración de invalidación de la versión de destino:

  - Invalidación de versión de destino se ha establecido en una versión de destino no compatible.
  - Invalidación de versión de destino se ha establecido en una versión de destino que no existe.
  - La entrada de Invalidación de versión de destino tiene un formato incorrecto.

- Si se establece Invalidación de directiva de actualización en "Actualizaciones deshabilitadas", Microsoft Edge Update no aceptará ninguna actualización. Como resultado, no se ejecutará la reversión.

### Configuro todas las directivas de grupo correctamente, pero no se ha ejecutado la reversión. ¿Qué ha ocurrido?

Microsoft Edge Update todavía no ha ejecutado una búsqueda de actualizaciones. De manera predeterminada, la actualización automática busca actualizaciones cada 10 horas. Para solucionar este problema, cambie el intervalo de sondeo de Microsoft Edge Update con la directiva de grupo Invalidar el período de buscar actualizaciones automáticas Para obtener más información, consulte la directiva [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes).

### Como administrador de TI, he seguido todos los pasos para revertir correctamente. Solo se revirtió una parte del grupo de usuarios. ¿Por qué todavía no se han revertido el resto de usuarios?

La configuración de directiva de grupo todavía no se ha sincronizado con todos los clientes. Cuando los administradores configuran una directiva de grupo, los clientes no reciben esta configuración de forma instantánea.

<!--
You can update all users' group policy with the  

When admins set all users don't get this setting instantaneously 

GP Update force group policy – link to this 

-->





## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
