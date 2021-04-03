---
title: Configurar directivas de modo IE
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 03/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar directivas de modo IE
ms.openlocfilehash: a2abf6f6ef71c1f30786031ef19b9633bfafc43f
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470168"
---
# <a name="configure-ie-mode-policies"></a>Configurar directivas de modo IE

Este artículo explica cómo se configuran las directivas de modo IE.

> [!NOTE]
> Este artículo se aplica a los canales de Microsoft Edge **Estable**, **Beta** y **Dev**, versión 77 o posterior.

La configuración del modo IE requiere tres pasos:

1. [Configurar la integración de Internet Explorer](#configure-internet-explorer-integration)
2. [Redirigir sitios de Microsoft Edge al modo IE](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. (Opcional) [Redirigir sitios de IE a Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)

    1. Si está listo para deshabilitar la aplicación IE11, siga los pasos descritos en [ Deshabilitar Internet Explorer 11](https://docs.microsoft.com/deployedge/edge-ie-disable-ie11)
    2. De lo contrario, siga el resto de los pasos en [Redirigir sitios de IE a Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge)

> [!NOTE]
> Las directivas para habilitar el modo IE se pueden configurar con Intune. Para obtener más información, consulta [Agregar Microsoft Edge a Microsoft Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) y [Configurar las directivas de Microsoft Edge con Microsoft Intune](./configure-edge-with-intune.md).

## <a name="configure-internet-explorer-integration"></a>Configurar la integración de Internet Explorer

Se puede configurar Internet Explorer para abrirlo directamente desde Microsoft Edge (modo IE). También se puede configurar Internet Explorer para abrirlo con una ventana independiente de Internet Explorer 11. La mayoría de los usuarios prefieren abrir los sitios directamente desde Microsoft Edge en modo IE.

### <a name="enable-internet-explorer-integration-using-group-policy"></a>Habilitar la integración de Internet Explorer mediante la directiva de grupo

1. Descarga u usa la última [plantilla administrativa de Microsoft Edge](https://www.microsoft.com/en-us/edge/business/download).
2. Abre el Editor de directivas de grupo.
3. Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Microsoft Edge**.
4. Haz doble clic en **Configurar la integración de Internet Explorer**.
5. Seleccione **Habilitado**.
6. En **Opciones**, establece el valor de la lista desplegable en 
   -  **Modo de Internet Explorer** para que los sitios se abran en modo IE en Microsoft Edge
   -  **Internet Explorer 11** si quiere que los sitios se abran en una ventana independiente de Internet Explorer 11
   -  **Ninguno** para deshabilitar el modo de Internet Explorer cuando se establece por edge://flags o mediante opciones de línea de comandos

   > [!NOTE]
   > Establecer la directiva en **Deshabilitado** implica que la directiva deshabilita el modo IE, pero puede establecerse con las opciones de línea de comandos o edge://flags.
7. Haz clic en **Aceptar** o en **Aplicar** para guardar esta configuración de directiva.

## <a name="redirect-sites-from-microsoft-edge-to-ie-mode"></a>Redirigir sitios de Microsoft Edge al modo IE

Hay 2 opciones para identificar qué sitios deben abrirse en modo IE:

- (Recomendado) [Configurar sitios en la lista de sitios de empresa](#configure-sites-on-the-enterprise-site-list)
- [Configurar todos los sitios de intranet](#configure-all-intranet-sites)

### <a name="configure-sites-on-the-enterprise-site-list"></a>Configurar los sitios de la lista de sitios de empresa

Puedes usar las siguientes directivas de grupo para configurar sitios específicos a abrir en modo IE:

- [Usar la lista de sitios web de IE del modo de empresa](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)
- [Configurar la lista de sitios de modo de empresa](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, versión 78 o posterior)<br/>Esta directiva permite crear una lista de sitios del modo de empresa independiente para Microsoft Edge. Al habilitar esta directiva, se invalida la configuración de la directiva "Usar la lista de sitios web de IE del modo de empresa", siempre que la opción "Configurar integración de Internet Explorer" esté habilitada. La deshabilitación o la no configuración de esta directiva no afecta al comportamiento predeterminado de la directiva "Configurar integración de Internet Explorer".
    > [!NOTE]
    > No es obligatorio configurar la directiva de Microsoft Edge. Muchas organizaciones usan esto para invalidar, lo que les permite dirigir la Lista de sitios actual a todos los usuarios con la directiva de IE, y dirigir más fácilmente una versión actualizada a las pruebas piloto con la directiva de Microsoft Edge.

Para obtener más información sobre la lista de sitios de modo de empresa, consulta:

- [Usar Enterprise Mode Site List Manager](/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- [Agregar varios sitios a la lista de sitios del modo de empresa mediante un archivo y la herramienta Enterprise Mode Site List Manager (esquema v.2)](/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).

### <a name="configure-using-the-use-the-enterprise-mode-ie-website-list-policy"></a>Configurar usando la directiva de listas de sitios web de IE de modo de empresa

El modo IE puede usar la directiva existente que configura la Lista de sitios de empresas para Internet Explorer, lo que le permite crear y mantener una lista única.

1. Crear o volver a usar una lista de sitios XML
    1. Todos los sitios que tengan el elemento _\<open-in\>IE11\</open-in\>_ se abrirán ahora en modo IE.
2. Abre el Editor de directivas de grupo.
3. Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Componentes de Windows** > **Internet Explorer**.
4. Haz doble clic en **Usar la lista de sitios web de IE del Modo de empresa**.
5. Seleccione **Habilitado**.
6. En **Opciones**, escribe la ubicación de la lista de sitios web. Puedes usar una de las siguientes ubicaciones:
    - (Recomendado) Ubicación HTTPS: **https**:**//iemode/sites.xml**
    - Archivo de red local: **\\\network\shares\sites.xml**
    - Archivo local: **file:///c:/Users/\<user\>/Documents/sites.xml**
7. Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración.

### <a name="configure-using-the-configure-the-enterprise-mode-site-list-policy"></a>Configurar con la directiva configurar el modo de empresa de lista de sitios

También es posible configurar el modo IE con una directiva independiente para Microsoft Edge. Esta directiva adicional permite anular la lista de sitios de Internet Explorer. Por ejemplo, algunas organizaciones dirigirán la lista de sitios de producción a todos los usuarios. Después, será posible implementar la lista de sitios piloto para un pequeño grupo de usuarios que usen esta directiva.

1. Crear o volver a usar una lista de sitios XML
    1. Todos los sitios que tengan el elemento _\<open-in\>IE11\</open-in\>_ se abrirán ahora en modo IE.
2. Abre el Editor de directivas de grupo.
3. Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Microsoft Edge**.
4. Haz doble clic en **Configurar la lista de sitios del modo de empresa**.
5. Seleccione **Habilitado**.
6. En **Opciones**, escribe la ubicación de la lista de sitios web. Puedes usar una de las siguientes ubicaciones:
    - (Recomendado) Ubicación HTTPS: **https**:**//iemode/sites.xml** <!--Trying to keep this from being an active link in MD -->
    - Archivo de red local: **\\\network\shares\sites.xml**
    - Archivo local: **file:///c:/Users/\<user\>/Documents/sites.xml**
7. Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración.

### <a name="configure-all-intranet-sites"></a>Configurar todos los sitios de intranet

El modo IE se puede configurar como "para todos los sitios" en la zona Intranet local. Es posible quitar sitios individuales del modo IE con una lista de sitios de modo de empresa.

>[!NOTE]
>
> La zona de Intranet local contiene sitios agregados explícitamente, pero también asigna sitios a esta zona mediante heurística. Esto puede incluir nombres de host sin punto (p.ej. **https**:**//nomina**) y sitios que el script de configuración de proxy configura para eludir el proxy. Si un usuario externo controla DNS o proxy, podría exigir el uso de los sitios web en modo IE.

1. Abre el Editor de directivas de grupo local.
2. Haz clic en **Configuración del equipo** > **Plantillas administrativas** > **Microsoft Edge**.
3. Haz doble clic en **Enviar todos los sitios de intranet a Internet Explorer**.
4. Selecciona **Habilitado** y luego haz clic en **Aceptar** o **Aplicar** para guardar la configuración de directiva.

## <a name="redirect-sites-from-ie-to-microsoft-edge"></a>Redirigir sitios de IE a Microsoft Edge

Es posible impedir que los usuarios usen Internet Explorer para los sitios que no lo necesiten. Internet Explorer puede redirigir sitios automáticamente a Microsoft Edge si no están en la lista de sitios.

1. Abre el Editor de directivas de grupo.
2. Haz clic en **Configuración del equipo** > **Herramientas administrativas** > **Componentes de Windows** > **Internet Explorer**.
3. Haz doble clic en **Enviar todos los sitios que no se incluyan en la lista de sitios del modo de empresa a Microsoft Edge**.
4. Selecciona **Habilitado**
5. Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración.
6. Haga doble clic en **configurar qué canal de Microsoft Edge usar para abrir sitios redirigidos**.
7. Seleccione **Habilitado**.
8. En **Opciones**, selecciona las tres opciones principales para el canal que usará: Internet Explorer se redirigirá a la opción de mayor jerarquía que el usuario haya instalado en el dispositivo:
   - Microsoft Edge Stable
   - Microsoft Edge Beta versión 77 o posterior
   - Microsoft Edge Dev versión 77 o posterior
   - Microsoft Edge Canary versión 77 o posterior
   - Microsoft Edge versión 45 o anterior
9. Haz clic en **Aceptar** o **Aplicar** para guardar esta configuración.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Acerca del modo IE](./edge-ie-mode.md)
- [Información adicional del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)