---
title: Actualizaciones de Windows para Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Actualizaciones de Windows para Microsoft Edge
ms.openlocfilehash: 880e5a591ee23ff852981e73fe4fc4cd815be9ad
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447154"
---
# <a name="windows-updates-to-support-the-next-version-of-microsoft-edge"></a>Actualizaciones de Windows para admitir la próxima versión de Microsoft Edge

En este artículo se describe cómo se actualizará Windows para admitir la próxima versión de Microsoft Edge.

> [!IMPORTANT]
> Consulta la [entrada del blog](https://aka.ms/EdgeLegacyEOS) del equipo de producto e Microsoft Edge sobre la finalización del servicio de Microsoft Edge (versión anterior).

> [!NOTE]
> Este artículo se aplica al canal Estable de Microsoft Edge.

## <a name="microsoft-edge-and-the-windows-release-cycle"></a>Microsoft Edge y el ciclo de versión de Windows

La próxima versión de Microsoft Edge ofrece funcionalidades de actualización más frecuentes y flexibles. Dado que las versiones del explorador no están unidas a las versiones principales de Windows, se realizarán cambios en el sistema operativo para garantizar que la próxima versión de Microsoft Edge se adapte perfectamente a Windows. Como resultado, las actualizaciones de características se publicarán en un ciclo de 6 semanas (aproximadamente). Las actualizaciones de seguridad y compatibilidad se publicarán según sea necesario.

## <a name="updates-and-the-user-experience"></a>Actualizaciones y experiencia del usuario

Las actualizaciones no cambiarán la experiencia del usuario hasta que se instale el canal Estable de la próxima versión de Microsoft Edge. La instalación de Microsoft Edge Beta, Dev o Canary no desencadenará ningún cambio en Windows. Estas versiones del explorador se instalarán junto con los exploradores existentes.

Cuando se aplican todas las actualizaciones Y el canal Estable de la próxima versión de Microsoft Edge se instala en el nivel del sistema, surtirán efecto los siguientes cambios en el sistema:

- Todas las anclas del menú Inicio, los iconos y los accesos directos de la versión actual de Microsoft Edge se migrarán a la próxima versión de Microsoft Edge.
- Todas las anclas y accesos directos de la barra de tareas de la versión actual de Microsoft Edge se migrarán a la próxima versión de Microsoft Edge.
- La próxima versión de Microsoft Edge estará anclada a la barra de tareas. Si la versión actual de Microsoft Edge ya está anclada, se reemplazará.
- La próxima versión de Microsoft Edge agregará un acceso directo al escritorio. Si la versión actual de Microsoft Edge ya tiene acceso directo, se reemplazará.
- La mayoría de los protocolos que Microsoft Edge trata de manera predeterminada se migrarán a la próxima versión de Microsoft Edge.
- Microsoft Edge actual se ocultará se ocultará de todas las superficies de experiencia del usuario en el SO, incluida la configuración, todas las aplicaciones y todos los diálogos de compatibilidad de archivo o protocolo.
- Todos los intentos de iniciar la versión actual de Microsoft Edge se redirigirán a la próxima versión de Microsoft Edge.

  > [!NOTE]
  > Las instalaciones en el nivel de usuario no desencadenarán estos comportamientos.

Además de los cambios anteriores, existen cambios que se producirán independientemente de si se ha instalado el canal Estable de la próxima versión de Microsoft Edge.

- Microsoft Edge dejará de estar registrado para los libros y protocolos XML que no sean compatibles con la próxima versión de Microsoft Edge. Los usuarios que intenten abrir estos protocolos obtendrán un diálogo que les pedirá elegir una aplicación predeterminada. Obtén más información sobre los cambios en el soporte de libros en [Descargar una aplicación ePub para seguir leyendo libros electrónicos](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0).

## <a name="timeline"></a>Línea de tiempo

Los cambios necesarios para admitir la experiencia descrita se entregarán con tres actualizaciones para las diferentes versiones de Windows.

### <a name="windows-versions-1903-and-1909"></a>Versiones 1903 y 1909 de Windows

- El primer conjunto de cambios en la actualización opcional de julio de 2019, distribuida con la actualización de seguridad de agosto de 2019.
- El segundo conjunto de cambios en la actualización opcional de agosto de 2019, distribuida con la actualización de seguridad de septiembre de 2019.

  > [!NOTE]
  > Esta es la actualización en la que Microsoft Edge dejará de estar registrado para el protocolo XML.

- El tercer conjunto de cambios en una actualización opcional de septiembre de 2019, distribuida con la actualización de seguridad de octubre de 2019.

  > [!NOTE]
  > Esta es la actualización en la que Microsoft Edge dejará de admitir libros electrónicos.

### <a name="windows-versions-1709-1803-and-1809"></a>Versiones 1709, 1803 y 1809 de Windows

- El primer conjunto de cambios en una actualización opcional de agosto de 2019, distribuida con la actualización de seguridad de septiembre de 2019.
- El segundo conjunto de cambios en una actualización opcional de septiembre de 2019, distribuida con la actualización de seguridad de octubre de 2019.

  > [!NOTE]
  > Esta es la actualización en la que Microsoft Edge dejará de estar registrado para el protocolo XML.

- El tercer conjunto de cambios en una actualización opcional de octubre de 2019, distribuida con la actualización de seguridad de noviembre de 2019.

  > [!NOTE]
  > Esta es la actualización en la que Microsoft Edge dejará de admitir libros electrónicos.

En la siguiente tabla se facilitan los detalles de las actualizaciones específicas de cada conjunto de cambios.

| Windows 10 | Más información | Descarga requerida |
|--|--|--|
| Versión 1709 | [KB4525241](https://support.microsoft.com/help/4525241/windows-10-update-kb4525241) | [Actualización acumulativa de Windows 10, versión 1709](https://www.catalog.update.microsoft.com/Search.aspx?q=4525241) |
| Versión 1803  | [KB4525237](https://support.microsoft.com/help/4525237/windows-10-update-kb4525237) | [Actualización acumulativa de Windows 10, versión 1803](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4525237) |
| Versión 1809  | [KB4523205](https://support.microsoft.com/help/4523205/windows-10-update-kb4523205) | [Actualización acumulativa de Windows 10, versión 1809](https://www.catalog.update.microsoft.com/Search.aspx?q=4523205) |
| Versiones 1903 y 1909 |[KB4517389](https://support.microsoft.com/help/4517389/windows-10-update-kb4517389)  | [Actualización acumulativa de Windows 10, versiones 1903 y 1909](https://www.catalog.update.microsoft.com/Search.aspx?q=4517389) |

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Documentación de Microsoft Edge](./index.yml)