---
title: 'Configuración por sitio por directiva '
ms.author: collw
author: AndreaLBarr
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 'Configuración por sitio por directiva '
ms.openlocfilehash: 4f1bf9a421f0098ba8105e78f77ac4af62530239
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979812"
---
# <a name="persite-configuration-by-policy"></a>Configuración por sitio por directiva

## <a name="introduction-browsers-as-decision-makers"></a>Introducción: Exploradores como responsables de la toma de decisiones

Como parte de cada carga de página, los exploradores toman muchas decisiones, ¿debería haber disponible una API determinada? ¿Se debería permitir una carga de recursos? ¿Se debería permitir la ejecución del script? La lista es larga.

En la mayoría de los casos, las decisiones se rigen por dos entradas: una configuración de usuario y la dirección URL de la página para la que se toma la decisión.

En la plataforma web de Internet Explorer heredada, cada una de estas decisiones se denominaba  [URLAction](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178%28v%3dvs.85%29) y la directiva de grupo empresarial y la configuración de usuario dentro del Panel de control de Internet controlaba cómo el explorador manejaba cada decisión.  

En Microsoft Edge, la mayoría de los permisos por sitio se controlan mediante la configuración y las directivas expresadas mediante una sintaxis simple con compatibilidad limitada con caracteres comodín. Las Zonas de Seguridad de Windows se siguen usando solo para un pequeño número de decisiones de configuración.

## <a name="background-windows-security-zones"></a>Fondo: Zonas de Seguridad de Windows

Para simplificar la configuración del usuario o su administrador, la plataforma heredada clasificaba los sitios en cinco  **Zonas de seguridad** diferentes: equipo local, intranet local, de confianza, Internet y sitios restringidos.

Al tomar una decisión, el explorador asignaría primero el sitio web a una zona y, después, consultaría la configuración de esa URLAction para esa zona a fin de decidir qué hacer. Los valores predeterminados razonables, como "Satisfacer automáticamente los desafíos de autenticación de mi Intranet", significaban que la mayoría de los usuarios nunca necesitaban cambiar ninguna configuración de sus valores predeterminados.

Los usuarios pueden usar el Panel de control de Internet para asignar sitios específicos a zonas y configurar los resultados de permisos para cada zona. En entornos administrados, los administradores pueden usar la directiva de grupo para asignar sitios específicos a zonas (a través de la directiva "Lista de asignación de sitio a zona") y especificar la configuración de URLActions por zona. Más allá de la asignación manual administrativa o de usuarios de sitios a zonas, la heurística adicional podría  [asignar sitios a la zona de Intranet local](/archive/blogs/ieinternals/the-intranet-zone). En concreto, los nombres de host sin punto (por ejemplo, `http://payroll`) se asignaban a la zona de Intranet. Si se usaba un script de configuración de proxy, todos los sitios configurados para omitir el proxy se asignarían a la zona de Intranet.

Microsoft Edge (versión anterior) heredó la arquitectura de zonas de su predecesora, Internet Explorer, con algunos cambios para simplificar:

- Las cinco zonas integradas de Windows se contrajeron en tres: Internet (Internet), De confianza (Intranet + De confianza) y Equipo local. Se quitó la zona Sitios restringidos.

- Las asignaciones de zona a URLAction se codificaron de forma permanente en el explorador, omitiendo las directivas de grupo y la configuración en el Panel de control de Internet.

## <a name="per-site-permissions-in-the-microsoft-edge"></a>Permisos por sitio en Microsoft Edge

A diferencia de sus predecesores, el nuevo Microsoft Edge hace un uso muy limitado de las Zonas de Seguridad de Windows. En su lugar, la mayoría de los permisos y características que ofrecen a los administradores la configuración por sitio a través de  [directiva](/deployedge/microsoft-edge-policies) se basan en listas de reglas en el  [formato de filtro de dirección URL](/DeployEdge/edge-learnmmore-url-list-filter%20format).

Cuando los usuarios finales abran <code>edge://settings/content/siteDetails?site=https://example.com</code>, encontrarán una larga lista de modificadores de configuración y listas para varios permisos. Los usuarios rara vez usan la página de configuración directamente. En su lugar. toman decisiones mientras exploran con varios widgets y conmutadores en la lista desplegable  **Información de página**  (que aparece al hacer clic en el icono de bloqueo en la barra de direcciones) o a través de varios mensajes o botones en el borde derecho de la barra de direcciones.

Las empresas pueden usar la directiva de grupo para aprovisionar listas de sitios para directivas individuales que controlan el comportamiento del explorador. Para encontrar estas directivas, simplemente abra la  [Documentación de directiva de grupo de Microsoft Edge](/deployedge/microsoft-edge-policies)  y busque **ForUrls**  para buscar las directivas que permiten y bloquean el comportamiento en función de la dirección URL del sitio cargado. La mayoría de las configuraciones pertinentes se enumeran en la sección  [Directiva de grupo para configuración de contenido](/deployedge/microsoft-edge-policies#content-settings).

También hay varias directivas (cuyos nombres contienen  **Predeterminada**) que controlan el comportamiento predeterminado de una configuración determinada.

Muchas de las opciones de configuración están muy ocultas (WebSerial, WebMIDI) y a menudo no hay ninguna razón para cambiar el valor predeterminado (Imágenes) de una configuración.

## <a name="common-questions"></a>Preguntas comunes

## <a name="q-can-the-url-filter-format-match-on-a-sites-ip-address"></a>P: ¿Puede coincidir el formato de filtro de dirección URL en la dirección IP de un sitio?

No, el formato no admite la especificación de un intervalo de IP para las listas de permitidos y bloqueados. Admite la especificación de  **literales **de IP individuales, pero estas reglas solo se respetan si el usuario navega al sitio mediante dicho literal (por ejemplo,  <http://127.0.0.1/>). Si se usa un nombre de host (<http://localhost>), la regla de literal de IP no se respetará aunque la dirección IP resuelta del host coincida con la dirección IP de la lista de filtros.

## <a name="q-can-url-filters-matchjustdotless-host-names"></a>P: ¿Los filtros de dirección URL pueden coincidir solo con nombres de host sin punto?

No. Debe enumerar individualmente cada nombre de host deseado, por ejemplo, (`https://payroll`, `https://stock`, `https://who`, etc.).

Si fue lo suficientemente previsor como para estructurar la intranet de modo que los nombres de host tengan el formato:

- <div style="display: inline">`https://payroll.contoso-intranet.com`</div>

- <div style="display: inline">`https://timecard.contoso-intranet.com`</div>

- <div style="display: inline">`https://sharepoint.contoso-intranet.com`</div>

Enhorabuena, ha implementado un procedimiento recomendado. Puede configurar cada directiva deseada con una entrada ***.contoso-intranet.com**  y se incluirá en toda la Intranet.

## <a name="use-of-security-zones-inthe-microsoft-edge"></a>Uso de zonas de seguridad en Microsoft Edge

Aunque Microsoft Edge se basa principalmente en directivas individuales que usan el formato de filtro URL, sigue usando las Zonas de seguridad de Windows de forma predeterminada en un pequeño número de lugares con el fin de simplificar la implementación dentro de las empresas que han dependido históricamente de la configuración de zonas. Los comportamientos siguientes se controlan mediante la directiva de zona:

1. Al decidir si se van a liberar automáticamente las credenciales de autenticación integrada de Windows (Kerberos/NTLM)

2. Al decidir cómo controlar las descargas de archivos

3. Para el modo Internet Explorer

## <a name="credential-release"></a>Liberación de credenciales

De forma predeterminada, Microsoft Edge evaluará URLACTION_CREDENTIALS_USE para decidir si la autenticación integrada de Windows se usa automáticamente o si el usuario debería ver en su lugar un mensaje de autenticación manual. Configurar una [directiva de lista de sitios AuthServerAllowlist](/deployedge/microsoft-edge-policies#authserverallowlist) impedirá que se consulte la directiva de zona.

## <a name="file-downloads"></a>Descargas de archivos

Las evidencias sobre los orígenes de una descarga de archivos (la llamada "[Marca de la Web](https://textslashplain.com/2016/04/04/downloads-and-the-mark-of-the-web/)" se registran para los archivos descargados de la zona de Internet. Otras aplicaciones (por ejemplo, Shell de Windows, Microsoft Office, etc.) pueden tener en cuenta estas evidencias de origen al decidir cómo administrar un archivo.

Si la directiva de Zona de Seguridad de Windows está configurada para deshabilitar la configuración Iniciar aplicaciones y archivos no seguros, el administrador de descargas de Microsoft Edge bloqueará las descargas de archivos de los sitios de esa zona con una nota: "No se pudo descargar: bloqueado".  

## <a name="ie-mode"></a>Modo IE

El modo IE se puede configurar para  [abrir todos los sitios de Intranet en modo IE](/deployedge/edge-ie-mode#configure-all-intranet-sites). En esta configuración, Edge evalúa la zona de una dirección URL al decidir si debe abrirse o no en modo IE. Más allá de esta decisión inicial, las pestañas del modo IE ejecutan en realidad Internet Explorer y, como consecuencia, evalúan la configuración de zonas para cada decisión de directiva, tal como hacía Internet Explorer.

## <a name="summary"></a>Resumen

En la mayoría de los casos, la configuración de Microsoft Edge se puede dejar en sus valores predeterminados. Los administradores que quieran cambiar los valores predeterminados para todos los sitios o sitios específicos pueden usar las directivas de grupo adecuadas para especificar listas de sitios o comportamientos predeterminados. En algunos casos (liberación de credenciales, descarga de archivos y modo IE), los administradores seguirán controlando el comportamiento mediante la configuración de Zonas de Seguridad de Windows.
