---
title: Reversión de Microsoft Edge para empresas
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Cómo revertir Microsoft Edge a una versión anterior
ms.openlocfilehash: e4f1847e40cedb8c551476893fedb64ec55769948edf3cf850c56dc7df9d29c4
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11725982"
---
# <a name="how-to-roll-back-microsoft-edge-to-a-previous-version"></a>Cómo revertir Microsoft Edge a una versión anterior

En este artículo se describe cómo revertir a una versión anterior de Microsoft Edge con la característica de reversión. Para obtener más información sobre esta característica, vea [Vídeo: Reversión de versión de Microsoft Edge](microsoft-edge-video-version-rollback.md).

>[!NOTE]
>Este artículo se aplica a Microsoft Edge, versión 86 o posterior.

## <a name="introduction-to-rollback"></a>Introducción a la característica de reversión

La reversión permite sustituir la versión del navegador Microsoft Edge por una versión anterior. Esta característica está diseñada para servir como red de seguridad para las empresas que implementan Microsoft Edge. Ofrece un método para solucionar problemas con Microsoft Edge. Las ventajas de la reversión son la capacidad para revertir a la versión anterior del explorador de forma fácil y rápida. La reversión reduce el impacto potencial de un problema de Microsoft Edge en las operaciones empresariales.

## <a name="before-you-begin"></a>Antes de comenzar

Es importante comprender cómo se instala la característica de reversión en un entorno de Microsoft Edge. Es posible implementar la reversión mediante dos métodos distintos: manualmente con un paquete MSI o con Microsoft Edge Update y una directiva de grupo. También recomendamos el uso de una selección de directivas de grupo para una implementación más fluida.

### <a name="recommendations"></a>Recomendaciones

La característica de reversión tiene como objetivo ser una corrección temporal para problemas que se puedan encontrar en una actualización del explorador Microsoft Edge. Se recomienda a los usuarios que instalen la última versión del explorador Microsoft Edge para usar la protección proporcionada por las últimas actualizaciones de seguridad. Revertir a una versión anterior supone un riesgo de exposición a problemas de seguridad conocidos.

Antes de revertir temporalmente a la versión anterior, recomendamos encarecidamente que se habilite la sincronización para todos los usuarios de la organización. Si no se activa la sincronización, se corre el riesgo de pérdida definitiva de datos de búsqueda. Para obtener más información sobre la sincronización, consulte [Sugerencias de Microsoft Edge](microsoft-edge-enterprise-sync.md).

> [!CAUTION]
> Usa la reversión solo cuando sea necesario: siempre se corre el riesgo de perder datos.

## <a name="enable-rollback-manually-with-an-msi"></a>Habilitar la reversión manual con un MSI

Siga los pasos que se indican a continuación para la reversión manual con un MSI.

1. Deshabilite las actualizaciones de Microsoft Edge.

   > [!NOTE]
   > Recomendamos instalar las plantillas administrativas más recientes. Para obtener más información, consulte [Descargar e instalar la plantilla administrativa de Microsoft Edge](./configure-microsoft-edge.md#1-download-and-install-the-microsoft-edge-administrative-template).

   - Abra el editor de directivas de grupo local y vaya a *Configuración del equipo>Plantillas administrativas>Microsoft Edge Update>Aplicaciones>Microsoft Edge>*.
   - Seleccione **Invalidar directiva de actualización** y, a continuación, seleccione **Habilitar**.
   - En **Opciones**, seleccione **Actualización deshabilitada** en la lista desplegable Directiva.

2. Obtenga el MSI.

   - Descargue [desde aquí](https://www.microsoft.com/edge/business/download) el archivo MSI para la versión a la que desea volver.
   - Guarde el MSI en el escritorio.

3. Ejecute el comando de reversión.

   - Abra el símbolo del sistema de Windows con **Ejecutar como administrador**.
   - Escriba el comando siguiente, donde: *C:\Usuarios\nombreusuario\Escritorio\prueba* es la ruta de acceso al MSI previamente descargado y NombreArchivo es el nombre del archivo .msi:<br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > Para obtener más información sobre msiexec, consulte [msiexec](/windows-server/administration/windows-commands/msiexec).
   - Cierre y vuelva a abrir Microsoft Edge para comprobar que la reversión se ha realizado correctamente. En **Configuración y más** (ALT + F), ve a **Configuración** y seleccione **Acerca de Microsoft Edge**.

## <a name="enable-rollback-with-microsoft-edge-update-and-group-policy"></a>Habilitar la reversión con una actualización de Microsoft Edge Update y una directiva de grupo

Siga los pasos siguientes para habilitar la reversión con Microsoft Edge Update y una directiva de grupo

1. Abra el editor de directivas de grupo local y vaya a *Configuración del equipo>Plantillas administrativas>Microsoft Edge Update>Aplicaciones>Microsoft Edge>*.
2. Seleccione **Revertir a la versión de destino** y, a continuación, seleccione **Habilitado**.
3. Seleccione **Anular la versión de destino** y elija la versión del explorador a la que se desea revertir.
4. Seleccione **Invalidar directiva de actualización** y, a continuación, seleccione **Habilitar**. En **Opciones**, elija una de las siguientes opciones de la lista desplegable Directiva (excepto **Actualización deshabilitada**):

   - Permitir siempre actualizaciones
   - Solo actualizaciones silenciosas automáticas

     > [!NOTE]
     > Para forzar una actualización de directiva de grupo, escriba `gpupdate /force` en el símbolo del sistema de Administrador de Windows (ejecutar como administrador).

5. Haz clic en **Aceptar** para guardar la configuración de directiva. La reversión se producirá la próxima vez que Microsoft Edge Update compruebe si hay alguna actualización. Si desea que la actualización se realice antes, puede cambiar el intervalo de sondeo de Microsoft Edge Update o habilitar la reversión mediante un MSI.

### <a name="common-rollback-errors"></a>Errores comunes de reversión

Los siguientes errores impiden la reversión:

- La entrada es una versión de destino no admitida
- La entrada es una versión de destino no existente
- El formato de la entrada no es correcto

### <a name="recommended-group-policies"></a>Directivas de grupo recomendadas

Se recomienda encarecidamente usar las siguientes directivas de grupo y configuraciones para la reversión.

#### <a name="sync-group-policies"></a>Directivas de grupo de sincronización

- ForceSync. Establece ForceSync como habilitado. Esta directiva forzará la habilitación de la sincronización para todos los usuarios de Azure Active Directory (Azure AD). Esta directiva solo es válida para las versiones 86 y posteriores de Microsoft Edge.
- *Configurar la lista de los tipos que se excluyen de la directiva de sincronización* permite a los administradores controlar los datos que los usuarios pueden sincronizar.

#### <a name="browser-restart-group-policies"></a>Reinicio de las directivas de grupo del explorador

Se recomienda forzar un reinicio para los usuarios después de habilitar la reversión.

- Habilite *Notificar al usuario que se recomienda o se requiere el reinicio del navegador para realizar las actualizaciones pendientes*. En opciones, seleccione **Necesario**.
- Habilite *Establecer el período de tiempo de las notificaciones de actualización* y, a continuación, establezca el tiempo deseado en milisegundos.

## <a name="snapshot"></a>Instantánea

Una instantánea es una copia de la versión marcada de la carpeta de datos de usuario. Durante una actualización de versión, se crea una instantánea de la versión anterior y se almacena en la carpeta de instantáneas. Tras la reversión, se copia una instantánea de una versión coincidente en la nueva carpeta de datos de usuario y se elimina de la carpeta de instantáneas. Si no hay disponible una instantánea que coincida con la versión al cambiar a una versión anterior, la reversión confiará en la sincronización para rellenar los datos de usuario en la nueva versión de Microsoft Edge.

La directiva de grupo [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) te permite establecer un límite para el número de instantáneas que se pueden conservar en un momento dado. De forma predeterminada, se conservan tres instantáneas. Puede configurar esta directiva para mantener entre 0 y 5 instantáneas.

## <a name="frequently-asked-questions"></a>Preguntas frecuentes

### <a name="manual-msi-rollback"></a>Reversión manual mediante MSI

#### <a name="what-generic-msi-failures-that-can-happen"></a>¿Qué errores genéricos de MSI se pueden producir?

1. Si la directiva de grupo Instalar actualización está deshabilitada, no se realizará la reversión.

   - Para usar la reversión, asegúrese de que Instalar está como **Habilitado**. Si esta directiva está deshabilitada, impide la instalación de los canales de Microsoft Edge. Para obtener más información, consulte [Instalar](./microsoft-edge-update-policies.md#install).

2. Si no hay actualizaciones predefinidas, se bloquearán las instalaciones de Microsoft Edge, a no ser que *Permitir la experiencia de exploradores en paralelo de Microsoft Edge* esté habilitado.

   - Para las versiones de Windows 1903 y 1909: Si la última actualización es anterior a octubre de 2019, es posible que tenga este problema.
   - Para las versiones de Windows 1709, 1803 y 1809: Si la última actualización es anterior a noviembre de 2019, es posible que tenga este problema.<br>
Para obtener más información, consulte [Actualizaciones de Windows que admiten la próxima versión de Microsoft Edge](./microsoft-edge-sysupdate-windows-updates.md)

#### <a name="the-following-error-message-was-shown-after-using-the-command-prompt-and-rollback-didnt-occur-whats-wrong"></a>Se mostró el siguiente mensaje de error después de usar el símbolo del sistema y no se realizó la reversión. ¿Cuál es el problema?

![Mensaje de estado de la reversión](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

*ALLOWDOWNGRADE=1* no se ha ejecutado.

### <a name="microsoft-edge-update-and-group-policy-rollback"></a>Reversión con Microsoft Edge Update y la directiva de grupo

#### <a name="i-set-rollback-to-target-version-enabled-update-policy-override-input-my-desired-browser-version-for-target-version-override-but-the-browser-version-wasnt-what-i-expected-whats-wrong"></a>Establecí *Reversión a la versión de destino*, habilité *Invalidación de directiva de actualización* e indiqué la versión del explorador que quería para *Invalidación de versión de destino*, pero la versión del explorador no fue la que esperaba. ¿Cuál es el problema?

Algunos errores comunes que impiden la reversión son:

- Si no se ha establecido Revertir a la versión de destino, la reversión no se ejecutará.
- Existe uno de los siguientes problemas con la configuración de la invalidación de la versión de destino:

  - La invalidación de versión de destino se ha establecido como una versión de destino que no se admite.
  - La invalidación de versión de destino se ha establecido como una versión de destino que no existe.
  - La entrada de Invalidación de versión de destino tiene un formato incorrecto.

- Si se establece la Invalidación de directiva de actualización en "Actualizaciones deshabilitadas", Microsoft Edge Update no aceptará ninguna actualización y no se ejecutará la reversión.

### <a name="i-set-all-the-group-policies-correctly-but-rollback-didnt-execute-what-happened"></a>Configuro todas las directivas de grupo correctamente, pero no se ha ejecutado la reversión. ¿Qué ha ocurrido?

Microsoft Edge Update todavía no ha ejecutado una búsqueda de actualizaciones. De manera predeterminada, la actualización automática busca actualizaciones cada 10 horas. Para solucionar este problema, puede cambiar el intervalo de sondeo de Microsoft Edge Update con la directiva de grupo de invalidación del período de búsqueda actualizaciones automáticas Para obtener más información, consulte la directiva [AutoUpdateCheckPeriodMinutes](./microsoft-edge-update-policies.md#autoupdatecheckperiodminutes).

### <a name="as-an-it-admin-i-followed-all-the-steps-for-rollback-correctly-only-a-portion-of-my-user-group-was-rolled-back-why-havent-the-other-users-been-rolled-back-yet"></a>Como administrador de TI, seguí todos los pasos de reversión correctamente. Solo se revirtió una parte del grupo de usuarios. ¿Por qué todavía no se ha revertido el resto de usuarios?

La configuración de directiva de grupo todavía no se ha sincronizado con todos los clientes. Cuando los administradores configuran una directiva de grupo, los clientes no reciben esta configuración de forma instantánea. Puede [Forzar una actualización de directiva de grupo remota](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11)).

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: Reversión de versión de Microsoft Edge](microsoft-edge-video-version-rollback.md)