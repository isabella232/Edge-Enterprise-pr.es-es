---
title: ¿¿Qué es el modo Internet Explorer?
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Aprenda cómo el modo Internet Explorer en Microsoft Edge proporciona acceso a sitios que necesitan Internet Explorer 11 y acceso a sitios modernos.
ms.openlocfilehash: 5ca14c4d448b573dc7de6781ce86ee62281a48a4
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470228"
---
# <a name="what-is-internet-explorer-ie-mode"></a>¿Qué es el modo Internet Explorer (IE)?

Hemos creado el modo Internet Explorer (IE) en Microsoft Edge para las organizaciones que todavía necesitan Internet Explorer 11 para la compatibilidad con los sitios web existentes, pero también necesitan un navegador moderno. Esta característica facilita a las organizaciones el uso de un solo navegador, para las webs/apps heredadas o para una web/app moderna. Este artículo proporciona una introducción al uso de Microsoft Edge con el modo IE.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="what-is-ie-mode"></a>¿Qué es el modo IE?

El modo IE en Microsoft Edge hace que sea más fácil usar todos los sitios que su organización necesita en un único explorador. Usa el motor de Chromium integrado para sitios modernos y usa el motor Trident MSHTML de Internet Explorer 11 (IE11) para sitios heredados.

Cuando un sitio se carga en modo IE, el indicador del logotipo IE aparece en el lado izquierdo de la barra de navegación. Puede hacer doble clic en el indicador del logotipo IE para mostrar información adicional, como se muestra:

  ![Indicador del logotipo de IE](./media/ie-mode/ie-logo-indicator1.png)

Solo los sitios que configure específicamente (mediante Directiva) usarán el modo IE y todos los demás sitios se mostrarán como sitios web modernos. Para que un sitio use el modo IE, tiene que:

- Enumere el sitio en el modo de empresa XML de la lista de sitios definido en una de estas directivas:
  - Microsoft Edge 78 o posterior, "Configurar la lista de sitios de modo de empresa"
  - Internet Explorer, "Usar la lista de sitios web de IE del modo de empresa"
  > [!NOTE]
  > Solo se procesa una lista de sitios de modo de empresa. La Directiva de lista de sitios de Microsoft Edge tiene prioridad sobre la Directiva de lista de sitios de Internet Explorer.
- Todos los sitios de intranet cuando la **directiva de grupo Enviar todos los sitios de intranet a Internet Explorer** está habilitada (Microsoft Edge 77 o posterior).

### <a name="ie-mode-supports-the-following-internet-explorer-functionality"></a>El modo IE admite las siguientes funciones de Internet Explorer

- Todos los modos de documento y modos de empresa
- Controles ActiveX (como Java o Silverlight)
- Objetos auxiliares de explorador 
- Configuración y directivas de grupo de Internet Explorer que afectan a la configuración de zonas de seguridad y al modo protegido
- Las herramientas de desarrollo F12 para IE, cuando se inicia con [IEChooser](/office/dev/add-ins/testing/debug-add-ins-using-f12-developer-tools-on-windows-10)
- Extensiones de Microsoft Edge (no se admiten las extensiones que interactúan directamente con el contenido de la página de Internet Explorer).

### <a name="ie-mode-doesnt-support-the-following-internet-explorer-functionality"></a>El modo IE no admite las siguientes funciones de Internet Explorer

- Barras de herramientas de Internet Explorer
- Configuración y directivas de grupo de Internet Explorer que afectan al menú de navegación (por ejemplo, motores de búsqueda y páginas principales).
- Herramientas de desarrollo de IE11 or Microsoft Edge F12

## <a name="prerequisites"></a>Requisitos previos

Los siguientes requisitos previos se aplican al uso de Microsoft Edge con modo IE.

> [!IMPORTANT]
> Para garantizar el éxito, instale las últimas actualizaciones para Windows y Microsoft Edge. De no hacerlo, es probable que el modo IE falle.

1. En la tabla siguiente, se listan las actualizaciones mínimas del sistema para los sistemas operativos.

 | Sistema operativo | Versión       | Actualizaciones |
 |------------------|---------------|---------|
 | Windows 10       | 1909 o posterior |         |
 | Windows 10       | 1903          | [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) o posterior |
 | Windows Server   | 1903          | [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) o posterior |
 | Windows 10       | 1809          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) o posterior |
 | Windows Server   | 1809          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) o posterior |
 | Windows Server   | 2019          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) o posterior |
 | Windows 10       | 1803          | [KB4512509](https://support.microsoft.com/help/4512509/windows-10-update-kb4512509) o posterior |
 | Windows 10       | 1709          | [KB4512494](https://support.microsoft.com/help/4512494/windows-10-update-kb4512494) o posterior |
 | Windows 10       | 1607          | [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) o posterior |
 | Windows Server   | 2016          | [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) o posterior |
 | Windows 10       | versión inicial, julio de 2015 | [KB4520011](https://support.microsoft.com/help/4520011/windows-10-update-kb4520011) o posterior |
 | Windows 8       | 8.1              | [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) o posterior; o [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) o posterior |
 | Windows Server   | 2012 R2       | [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) o posterior; o [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) o posterior |
 | Windows 8  | Incrustado            | Instale [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019) para actualizar a Internet Explorer 11; a continuación, instale [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) o posterior; o [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) o posterior |
 | Windows Server   | 2012           | Instale [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019) para actualizar a Internet Explorer 11; a continuación, instale [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) o posterior; o [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) o posterior |
 | Windows 7        |  SP1**        | [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) o posterior. O [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) o posterior |
 | Windows Server   |  2008 R2**    | [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) o posterior. O [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) o posterior |
  > [!IMPORTANT]
  > ** Windows 7 y Windows Server 2008 R2 serán compatibles con Microsoft Edge incluso después de que estos sistemas operativos queden sin soporte. Para que el modo IE sea compatible con estos sistemas operativos, los dispositivos deberán tener las [Actualizaciones de seguridad extendidas para Windows](https://support.microsoft.com/help/4527878/faq-about-extended-security-updates-for-windows-7). Recomendamos que actualice a un sistema operativo compatible lo antes posible para mantener la seguridad. El soporte técnico de Microsoft Edge para las actualizaciones de seguridad extendidas se debe considerar un puente temporal para obtener un estado de SO compatible.

2. Plantilla administrativa de Microsoft Edge. Para obtener más información, consulta [Configurar Microsoft Edge](./configure-microsoft-edge.md).
3. Internet Explorer 11 habilitado en Características de Windows.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Información adicional del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)