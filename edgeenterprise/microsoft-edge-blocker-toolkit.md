---
title: Kit de herramientas de bloqueo para deshabilitar la entrega automática de Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Kit de herramientas de bloqueo para deshabilitar la entrega automática de Microsoft Edge
ms.openlocfilehash: 7563d2c94cf91a8434328699e46c75dbcfb77561
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981205"
---
# Kit de herramientas de bloqueo para deshabilitar la entrega automática de Microsoft Edge (basado en Chromium)

Este artículo describe el kit de herramientas de bloqueo para deshabilitar la entrega y la instalación automáticas de Microsoft Edge. Este artículo se actualizó en el **9/1/2020** con más información sobre los dispositivos que pueden requerir que use el kit de herramientas de bloqueo, el **28/2/2020** para quitar "Administrado por MDM" de los criterios de los dispositivos que se excluirán de esta actualización automática y el **30/6/2020** para reflejar que todos los dispositivos de Windows Update conectados deben recibir esta actualización (efectivo como pronto el 30/7/2020).

> [!NOTE]
> Esto es de aplicación al canal Estable de Microsoft Edge.

## Introducción

Para ayudar a nuestros clientes a estar más seguros y actualizados, Microsoft distribuirá Microsoft Edge (basado en Chromium) a todos los dispositivos conectados a Windows Update que ejecutan Windows10, versión 1803 y más recientes. Este proceso se iniciará después del 15 de enero de 2020 y habrá más información disponible en esa fecha.

El kit de herramientas de bloqueo está pensado para las organizaciones que desean bloquear la entrega automática de Microsoft Edge (basado en Chromium) en dispositivos conectados a Windows Update que ejecutan Windows10, versión 1803 y más recientes.
Los dispositivos administrados por Windows Server Update Services (WSUS) o Windows Update para empresas (WUfB) se excluirán de esta actualización automática.

**Es importante tener en cuenta que:**

- El kit de herramientas de bloqueo no impedirá que los usuarios instalen manualmente Microsoft Edge (basado en Chromium) a partir de descargas desde Internet o desde medios externos.
- Las organizaciones con actualizaciones administradas a través de Windows Update para empresas (WUfB) no recibirán automáticamente esta actualización y no tienen que implementar el kit de herramientas de bloqueo.
- Las organizaciones con entornos administrados con una solución de administración de actualizaciones, como Windows Server Update Services (WSUS) o System Center Configuration Manager (SCCM) no tienen que implementar el kit de herramientas de bloqueo. Pueden usar esos productos para administrar completamente la implementación de actualizaciones publicadas a través de Windows Update y Microsoft Update, incluidas las de Microsoft Edge (basado en Chromium), dentro de su entorno.
- Esta actualización es una actualización independiente (no forma parte de la actualización acumulativa mensual) para ofrecer flexibilidad a los clientes de Enterprise y un control máximo sobre la implementación de esta actualización.
- El nuevo Microsoft Edge (basado en Chromium) se incluirá como parte de la actualización de características de Windows 10, versión 20H2, en la segunda mitad de 2020. El kit de herramientas de bloqueo no impacta en los comportamientos o la implementación de 20H2. Puede ver más información sobre Windows 10, versión 20H2, [aquí](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).

Puedes descargar el archivo ejecutable del kit de herramientas de bloqueo desde [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).

### Componentes del kit de herramientas

Este kit de herramientas incluye los siguientes componentes:

- Script bloqueador ejecutable (.CMD)
- Plantilla administrativa de directiva de grupo (.ADMX y .ADML)

### Sistemas operativos compatibles

Windows 10, versión 1803 y versiones posteriores.

## Script bloqueador

El script crea una clave del Registro y establece el valor asociado en bloquear o no bloquear (en función de la opción de línea de comandos usada) la entrega automática de Microsoft Edge (basado en Chromium) en la máquina local o en una máquina remota de destino.

**Clave del Registro:** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**Nombre del valor clave:** `DoNotUpdateToEdgeWithChromium`

| Valor                | Resultado                         |
|----------------------|--------------------------------|
| *La clave no está definida.* | La distribución *no* está bloqueada. |
| 0                    | La distribución *no* está bloqueada. |
| 1                    | La distribución está bloqueada.       |

El script tiene la siguiente sintaxis de línea de comandos:<br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### Nombre de máquina

El parámetro `<machine name>` es opcional. Si no se especifica, la acción se realiza en la máquina local. De lo contrario, se accede al equipo remoto a través de las funciones de Registro remoto del comando `REG`. Si no se puede acceder al registro remoto debido a los permisos de seguridad o no se encuentra la máquina remota, el comando `REG` devuelve un mensaje de error.

### Conmutadores

Los conmutadores que usa el script son mutuamente excluyentes y solo se actúa sobre el primer conmutador válido de un comando determinado. El script puede ejecutarse varias veces en la misma máquina.

| Conmutador       | descripción                              |
|--------------|------------------------------------------|
| `/B`         | Bloquea la distribución                      |
| `/U`         | No bloquea la distribución                    |
| `/H` o `/?` | Muestra la siguiente ayuda resumida:<br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## Plantilla administrativa de directiva de grupo (archivos .ADMX y .ADML)

La plantilla administrativa de directiva de grupo (archivos .ADMX y .ADML) permite a los administradores importar la nueva configuración de directiva de grupo para bloquear o no bloquear la entrega automática de Microsoft Edge (basado en Chromium) en el entorno de la directiva de grupo y usar la directiva de grupo para ejecutar la acción de forma centralizada entre sistemas de su entorno.

Los usuarios que ejecuten Windows 10 RS3 Enterprise/EDU y RS4 y posteriores podrán ver la directiva en la siguiente ruta de acceso:

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

Esta opción solo está disponible como configuración del equipo; no hay una opción para cada usuario.

> [!IMPORTANT]
> Esta configuración del Registro no se almacena en una clave de directivas y se considera una *preferencia*. Por lo tanto, si el objeto de directiva de grupo que implementa la configuración se quita alguna vez o si la directiva está establecida en **No configurada**, la opción se mantendrá. Para desbloquear la distribución de Microsoft Edge (basado en Chromium) mediante la directiva de grupo, establece la directiva en **Deshabilitada**.

## Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://www.microsoftedgeinsider.com/enterprise)
- [Actualizaciones de Windows para compatibilidad con Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [Cómo acceder a la versión anterior de Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
