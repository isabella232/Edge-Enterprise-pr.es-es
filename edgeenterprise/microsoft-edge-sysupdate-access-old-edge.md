---
title: Obtener acceso a la versión anterior de Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Obtén información acerca de cómo obtener acceso a la versión heredada de Microsoft Edge.
ms.openlocfilehash: e4733d020f3a681ded50e5a087fe086d39362201
ms.sourcegitcommit: f7f7eb69d2298b0f9779a9fd28e3c4e297ef2e05
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125522"
---
# Obtener acceso a la versión heredada de Microsoft Edge tras la instalación de la nueva versión de Microsoft Edge

Obtén información acerca de cómo obtener acceso a la versión heredada de Microsoft Edge tras la instalación de la nueva versión de Microsoft Edge.

> [!NOTE]
> Este artículo se aplica al [canal Estable](microsoft-edge-channels.md) de Microsoft Edge.

Si bien la mayoría de las organizaciones querrán reemplazar Microsoft Edge heredado por la nueva versión, hay algunas situaciones en las que los usuarios necesitarán obtener acceso a ambas versiones. Por ejemplo:

- Personal de soporte técnico y de asistencia que interactúa con usuarios que usan una o ambas versiones de Microsoft Edge.
- Desarrolladores que dan soporte a clientes que usan una o ambas versiones de Microsoft Edge.

> [!IMPORTANT]
> No se recomienda el uso para producción de Microsoft Edge (versión anterior) en paralelo con la nueva versión de Microsoft Edge. Esta configuración solo debería usarse en casos específicos en los que se necesitan pruebas con ambas versiones del explorador.
>
> La aplicación de Microsoft Edge (versión anterior) llegará al fin de soporte el 9 de marzo de 2021 para dar paso al nuevo Microsoft Edge. Esto significa que Microsoft Edge (versión anterior) no recibirá actualizaciones de seguridad después de esa fecha. Este cambio se aplica a todas las experiencias que se ejecutan en la aplicación de escritorio de Microsoft Edge (versión anterior). [Más información](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).

## Antes de comenzar
> [!NOTE]
> A partir de la versión 20H2 de Windows 10, se dejará de incluir Microsoft Edge (versión anterior). A partir de esta versión de Windows 10, no se admite la experiencia en paralelo.

Los procedimientos descritos en este artículo se aplican a los sistemas que se han actualizado con las últimas actualizaciones de seguridad. Cuando se instale la nueva versión de Microsoft Edge, se ocultará la versión antigua (Microsoft Edge [versión heredada]). De manera predeterminada, todos los intentos de iniciar la versión anterior redirigirán al usuario a la versión recientemente instalada de Microsoft Edge. En este artículo se describe cómo puede seguir usando Microsoft Edge heredado después de instalar Microsoft Edge.

## Inicio rápido: experiencia en paralelo con el canal Microsoft Edge Beta y Microsoft Edge (versión anterior)

Antes de usar las instrucciones detalladas de este artículo, tenga en cuenta los dos pasos siguientes para permitir que los usuarios ejecuten Microsoft Edge (versión anterior) y el [canal Microsoft Edge Beta](microsoft-edge-channels.md) en paralelo.

1. Impide la instalación automática del canal estable de Microsoft Edge por parte de [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).

   > [!TIP]
   > Usa el [kit de herramientas de bloqueo](microsoft-edge-blocker-toolkit.md) para deshabilitar la entrega automática de Microsoft Edge.

2. Instale el [canal beta](https://www.microsoft.com/edge/business/download) de la nueva versión de Microsoft Edge.

   > [!NOTE]
   > Lea [información adicional](#additional-information) para obtener información sobre la configuración de las claves del registro.

Esta solución es menos compleja y requiere menos administración que la solución detallada descrita en este artículo. Sin embargo, esto significa que ejecutará el canal Beta en lugar del canal estable.

## Experiencia en paralelo con el canal estable de Microsoft Edge y Microsoft Edge (versión anterior)

Si instala el canal estable de la siguiente versión de Microsoft Edge en el nivel del sistema, se ocultará la versión actual (Microsoft Edge heredado). Si desea permitir que los usuarios vean las dos versiones de Microsoft Edge en paralelo en Windows, puede habilitar esta experiencia si configura la directiva de grupo **Permitir la experiencia de exploradores Microsoft Edge en paralelo** como **Habilitada**.

Esta directiva de grupo se documenta [aquí](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)

### Para configurar la directiva de experiencia de explorador en paralelo:

1. Instale las definiciones de directiva desde [Microsoft Edge para la empresa](https://www.microsoft.com/edge/business/download).

   - Elija el canal, la compilación y la plataforma que desee usar y haga clic en Obtener archivos de directiva.
   - Extraiga los archivos comprimidos.
   - Copia msedge.admx y msedgeupdate.admx en el directorio `C:\Windows\PolicyDefinitions`.
   - Copie msedge.adml y msedgeupdate.adml (del directorio correspondiente del idioma o la configuración regional) en el directorio `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]`.

2. Abre el Editor de directivas de grupo (gpedit.msc).
3. En **Configuración del equipo**, ve a *Plantillas administrativas > Microsoft Edge Update > Aplicaciones*.

    > [!NOTE]
    > Si no ve la carpeta *Microsoft Edge Update*, compruebe que el paso 1 se ha completado correctamente.

4. En **Aplicaciones**, haz doble clic en "Permitir la experiencia en paralelo de exploradores Microsoft Edge". Consulta nuestras [directrices de procedimientos recomendados](#best-practice-guidance) antes de continuar con el siguiente paso.

    > [!NOTE]
    > De forma predeterminada, esta directiva de grupo está establecida en "Sin configurar", lo que hace que se oculte Microsoft Edge (versión heredada) cuando la nueva versión de Microsoft Edge está instalada.

5. Selecciona **Habilitada** y, después, haz clic en **Aceptar**.  

Al configurar esta directiva, se establecerá la siguiente clave de registro en '00000001':

- Clave: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- Nombre del valor: `Allowsxs`
- Tipo de valor: `'REG_DWORD'`

#### Instrucciones de prácticas recomendadas

Para disfrutar de la mejor experiencia **Permitir la experiencia de exploradores Microsoft Edge en paralelo** debería estar habilitada antes de que se implemente la nueva versión de Microsoft Edge en los dispositivos de los usuarios.

Si la directiva de grupo está habilitada después de implementar Microsoft Edge, tendrá los siguientes efectos secundarios y acciones requeridas:

1. **Permitir la experiencia de exploradores Microsoft Edge en paralelo** no surtirá efecto hasta hasta después de que se vuelva a ejecutar el instalador para la nueva versión de Microsoft Edge.

   > [!NOTE]
   > El instalador se puede ejecutar directamente o de manera automática cuando se actualice la nueva versión de Microsoft Edge.

2. Microsoft Edge (versión heredada) tendrá que volverse a anclar a Inicio o a la barra de tareas porque el anclaje se migra cuando se implementa la nueva versión de Microsoft Edge.
3. Los sitios que se anclaron a Inicio o a la barra de tareas para Microsoft Edge (versión heredada) se migrarán a la nueva versión de Microsoft Edge.

## Información adicional

Una vez que se han actualizado por completo los sistemas y se ha instalado el canal estable de la próxima versión de Microsoft Edge, se establecen la siguiente clave del Registro y valor:

- Clave: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- Valor de la clave: `BrowserReplacement`

  > [!IMPORTANT]
  > Esta clave se sobrescribe cada vez que se actualiza el canal estable Microsoft Edge. Como práctica recomendada, se aconseja que NO elimines esta clave para permitir que los usuarios accedan a las dos versiones de Microsoft Edge.

## Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Actualizaciones de Windows para compatibilidad con Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md)
