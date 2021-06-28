---
title: Edge para la infraestructura de escritorio de virtualización
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge para infraestructura de escritorio virtualizado.
ms.openlocfilehash: eaad1b72934b336ce86d14dd8da92a6984d21914
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618266"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a>Microsoft Edge para infraestructura de escritorio virtualizado

En este artículo se describen los requisitos y limitaciones para usar Microsoft Edge en un entorno virtualizado.

## <a name="what-is-vdi"></a>¿Qué es la VDI?

La infraestructura de escritorio virtual (VDI) es una tecnología de virtualización que hospeda un sistema operativo de escritorio y aplicaciones en un servidor centralizado en un centro de datos. Esto permite una experiencia de escritorio totalmente personalizada para los usuarios con un origen centralizado totalmente seguro y compatible.

Microsoft Edge se pueden usar en un entorno virtualizado de las mismas maneras que en el dispositivo local, todo ello mientras se ejecuta desde un entorno de servidor seguro y controlado. En función de la solución VDI elegida, también es posible proporcionar a los usuarios un acceso fluido a las aplicaciones y sitios de la intranet.

La mayoría de las características de Edge se admiten en entornos VDI sin ninguna configuración especial. Sin embargo, para garantizar una experiencia óptima, se recomienda seguir las instrucciones que se indican a continuación.

## <a name="platforms-certified-for-edge"></a>Plataformas certificadas para Edge

- Azure Virtual Desktop
- Citrix Virtual Apps and Desktops (anteriormente conocido como XenApp y XenDesktop)

Aunque el equipo de Edge aún no ha comprobado otras soluciones de VDI, se espera que los flujos de trabajo más comunes en Edge sean compatibles. Las instrucciones proporcionadas a continuación pueden o no ser aplicables a la solución elegida.

## <a name="edge-on-vdi-performance-considerations"></a>Consideraciones de rendimiento de Edge en VDI

Al diseñar el entorno de VDI, debe considerar cuidadosamente los flujos de trabajo y las necesidades de los usuarios para lograr un rendimiento óptimo, así como los límites de la configuración del servidor.

Edge recomienda los siguientes requisitos mínimos para implementar Edge en entornos de VDI:

- vCPU: de 2 a 4 núcleos por usuario
- RAM: 1 GB por usuario

Tenga en cuenta que las extensiones y aplicaciones web complejas de gran tamaño requerirán más memoria y tendrán que tenerse en cuenta al configurar el entorno.

## <a name="edge-on-non-persisted-vdi-environments"></a>Edge en entornos de VDI no persistentes

Muchas soluciones de VDI permiten el acceso a entornos persistentes, donde se asigna a los usuarios un entorno virtual que persiste entre sesiones, y entornos no persistentes, donde los usuarios se asignan a uno de varios equipos disponibles, posiblemente una máquina diferente cada sesión, los datos de usuario pueden o no sincronizarse entre sesiones.

Cuando se usa un entorno no persistente, normalmente se crea una "imagen dorada" que se usa para cada dispositivo que incluye las aplicaciones y configuraciones necesarias. A continuación se muestran nuestras recomendaciones para preparar Edge para ese tipo de imagen.

### <a name="deploy-edge"></a>Implementación de Edge

Si está en Windows 10, versión 1803 y posteriores, debe tener Microsoft Edge instalado en el sistema. Sin embargo, si tiene una versión anterior de Windows o quiere implementar un canal diferente de Edge, se recomiendan los pasos siguientes.

1. Descargue el paquete MSI de Edge que coincida con el sistema operativo de la máquina virtual de VDI desde:

    - [Descargar Microsoft Edge para empresas - Microsoft](https://www.microsoft.com/edge/business/download)

2. Instale MSI en la máquina virtual de VDI mediante la ejecución del siguiente comando:

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a>Deshabilitar actualizaciones automáticas

En el caso de las máquinas no persistentes, se recomienda deshabilitar las actualizaciones automáticas y, en su lugar, actualizar Edge actualizando la "imagen dorada" para asegurarse de que no haya discrepancias de versiones entre el grupo de máquinas.

Consulte las siguientes directivas para deshabilitar las actualizaciones automáticas:

- [Valor predeterminado de Invalidar directiva de actualización](/deployedge/microsoft-edge-update-policies#updatedefault)

- [Invalidar directiva de actualización](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a>Administración de perfiles

En las configuraciones no persistentes, es importante tener en cuenta que es posible que las máquinas virtuales no mantengan el estado de usuario entre sesiones o que a los usuarios se les asigne una máquina virtual que nunca hayan usado antes y, por tanto, no tengan ninguno de sus datos de usuario.

Edge admite varios métodos para sincronizar datos de usuario, de modo que estén disponibles independientemente de cómo accedan a Edge.

### <a name="azure-ad-sync"></a>Sincronización de Azure AD

Si su plan de Azure AD lo admite, la sincronización empresarial es el método más rápido y sencillo para asegurarse de que los datos de usuario de Edge se sincronizan con todos los dispositivos de usuario.  

Consulte lo siguiente para más información sobre los requisitos y la configuración.  

- [Configurar la sincronización empresarial de Microsoft Edge | Microsoft Docs](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a>Sincronización local para usuarios de Active Directory

Con la sincronización local, Microsoft Edge guarda los favoritos y la configuración de un usuario de Active Directory en un archivo que se puede mover entre diferentes equipos.  

Consulte lo siguiente para más información sobre los requisitos y la configuración.  

- [Sincronización local para usuarios de Active Directory (AD) | Microsoft Docs](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a>Redirección de perfiles de usuario  

Hay varias soluciones para migrar y redirigir toda la carpeta de usuario para asegurarse de que el contexto de usuario se mantiene en estos entornos no persistentes. Póngase en contacto con su proveedor de VDI para determinar la solución recomendada.

Algunas soluciones populares incluyen:

- [Introducción a FSLogix: | FSLogix | Microsoft Docs](/fslogix/overview)
- [Configuración de Citrix Profile Management](https://support.citrix.com/article/CTX222893)

También se puede recomendar que, al usar este método, se excluyan las carpetas innecesarias de la carpeta de usuario de la que se ha hecho una copia de seguridad para reducir los tiempos de carga iniciales cuando los usuarios inician sesión en una máquina y se migra el perfil. Si es así, se recomienda excluir las siguientes carpetas de la copia de seguridad para reducir el tamaño.

- %LocalAppData%\Microsoft\Edge\User Data\Default\Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed

## <a name="known-issues"></a>Problemas conocidos

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a>Microsoft Edge se bloquea en versiones anteriores de XenApp y XenDesktop

Este problema debería mitigarse en las versiones más recientes. Sin embargo, si encuentra este problema en su entorno, puede solucionar el problema deshabilitando Citrix API Hooks para Edge. Consulte [Cómo deshabilitar Citrix API Hooks por cada aplicación.](https://support.citrix.com/article/CTX107825)

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a>Rendimiento degradado al representar páginas con tablas HTML excepcionalmente grandes

Se sabe que las siguientes directivas de Citrix ralentizan la representación de páginas HTML con tablas muy grandes (más de 30000 filas).

- Pantalla del teclado automático
- Control remoto del cuadro combinado

Para más información, consulte [Configuración de directivas de experiencia móvil (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html). Deshabilitar estas directivas debería mitigar el problema.

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a>Los escenarios de autorización del Administrador de cuentas de Windows (Azure Sync) producen un error en Edge cuando se ejecutan como una aplicación de conexión directa de Citrix

Se trata de un problema conocido en Edge y otras aplicaciones que usan WAM (como Office) debido a que los componentes de Windows necesarios para estos escenarios no se inicializan cuando se ejecutan en el modo "directo". Una solución alternativa para este problema:

- Use Edge a través de un Escritorio remoto al host de Citrix en lugar de como una aplicación remota directa.
- En su lugar, use aplicaciones remotas de Azure Virtual Desktop, que tienen mitigaciones para este problema.
