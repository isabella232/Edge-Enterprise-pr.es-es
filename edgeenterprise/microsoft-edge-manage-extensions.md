---
title: Administrar extensiones de Microsoft Edge en la empresa
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Administrar extensiones de Microsoft Edge en la empresa
ms.openlocfilehash: 69c10bfa1e041d48f99594e6ac85dd39ba66379ca8d6d7fe12f1bdef6f3b54fe
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724922"
---
# <a name="manage-microsoft-edge-extensions-in-the-enterprise"></a>Administrar extensiones de Microsoft Edge en la empresa

En este artículo se proporcionan instrucciones prácticas recomendadas para los administradores que gestionan las extensiones de Microsoft Edge en sus organizaciones. Puede usar la información de este artículo para desarrollar una estrategia para administrar extensiones en su organización.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="introduction"></a>Introducción

Las organizaciones desean proteger los datos corporativos y de usuario, y evaluar las extensiones del explorador para garantizar que son seguras y relevantes para su empresa. Los administradores desean:

- Impedir que se instalen aplicaciones y extensiones incorrectas.
- Mantenga las extensiones que los usuarios necesitan para realizar su trabajo.
- Administrar el acceso a los datos de usuario y empresa.  

Este artículo es el primero de una serie que ayuda a los administradores a administrar extensiones para proporcionar una experiencia segura y productiva para sus usuarios. Esta serie recorre las distintas opciones y le ayuda a elegir el mejor método para administrar extensiones. La serie consta de los siguientes artículos:

- [Administrar las extensiones de Microsoft Edge en la empresa](microsoft-edge-manage-extensions.md). Cree una estrategia para administrar las extensiones y configurar las plantillas administrativas necesarias para administrar el explorador.
- [Usar directivas de grupo para administrar extensiones de Microsoft Edge](microsoft-edge-manage-extensions-policies.md). Opciones que usan directivas de grupo para administrar extensiones.
- [Crear una tienda web para las extensiones de Microsoft Edge](microsoft-edge-manage-extensions-webstore.md). Crear y hospedar extensiones.
- [Preguntas más frecuentes sobre las extensiones de Microsoft Edge](microsoft-edge-manage-extensions-faq.md). Preguntas más frecuentes.

## <a name="things-to-consider-when-managing-extensions"></a>Aspectos a tener en cuenta al administrar extensiones

Los usuarios necesitan acceso a determinadas aplicaciones, sitios y extensiones para realizar su trabajo y, al mismo tiempo, proteger los datos de los usuarios y de la empresa. Una estrategia de seguridad eficaz implica hacer las preguntas correctas para su empresa y cómo las extensiones pueden adaptarse a las necesidades de su empresa. Algunas de las preguntas clave que se pueden hacer son:

- ¿Qué normativas y medidas de cumplimiento debo cumplir?
- ¿Hay algunas extensiones que pidan permisos demasiado amplios, lo que podría ir en contra de las directivas de seguridad de datos de mi empresa?
- ¿Cuántos datos corporativos o de usuario se almacenan en los dispositivos de mis usuarios?

A medida que responda a estas preguntas, puede usar las directivas granulares que Microsoft Edge proporciona para:

- Bloquear o permitir extensiones en los equipos de los usuarios en función de las directivas de protección de datos.
- Forzar la instalación de extensiones en los dispositivos de los usuarios para que tengan herramientas que necesitan para ser productivos.
- Extensiones allowlist o blocklist para permitir la menor cantidad de derechos necesarios para que los usuarios realicen su trabajo.

El modelo tradicional para administrar extensiones usa el enfoque allowlist y blocklist para extensiones específicas. Sin embargo, Microsoft Edge también le permite administrar los permisos solicitados por las extensiones. Con este modelo, puede decidir qué derechos y permisos desea permitir que usen las extensiones en sus equipos y dispositivos y, a continuación, implementar una directiva global que permita o bloquee extensiones según sus requisitos.  

## <a name="understand-extension-permissions"></a>Comprender los permisos de las extensiones

Las extensiones pueden requerir derechos para realizar cambios en un dispositivo o una página web para ejecutarse correctamente. Estos derechos se denominan permisos. Los desarrolladores deben enumerar qué derechos y acceso necesitan sus extensiones. Existen dos categorías principales para los permisos y muchas extensiones necesitan los dos permisos siguientes:

- Los permisos de host requieren que la extensión enumere las páginas web que puede ver o modificar.
- Los permisos de dispositivo son los derechos que necesita una extensión en el dispositivo donde se está ejecutando.

Algunos ejemplos de estos permisos son: acceso a un puerto USB, almacenamiento o pantalla de visualización y comunicación con programas nativos.  

## <a name="get-ready-to-manage-extensions"></a>Prepárese para administrar las extensiones

## <a name="before-you-begin"></a>Antes de empezar

Las opciones de extensiones suponen que ya tiene Microsoft Edge administrado para los usuarios. Para obtener más información acerca de cómo configurar plantillas administrativas para las directivas de Microsoft Edge, vea:

-   [Configurar las opciones de directiva de Microsoft Edge en Windows](/DeployEdge/configure-microsoft-edge)
-   [Configurar para Windows con Intune](/mem/intune/configuration/administrative-templates-configure-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
-   [Configurar para Windows con Administración de dispositivos móviles](/deployedge/configure-edge-with-mdm)
-   [Configurar para macOS con un .plist](/deployedge/configure-microsoft-edge-on-mac)
-   [Configurar para macOS con Jamf](/deployedge/configure-microsoft-edge-on-mac-jamf)

Los pasos de configuración de este artículo son para Windows. Para la implementación correspondiente en MAC/Linux, vea la referencia de directiva del explorador Microsoft Edge.

## <a name="decide-which-extensions-to-allow"></a>Decidir qué extensiones permitir

La mayoría de las organizaciones deben administrar las extensiones según sus permisos y a qué sitios web tienen acceso. Este método es más seguro, más fácil de administrar y escalable para organizaciones grandes.  

- Permisos bloqueados o permitidos: Permite controlar las extensiones según los permisos que necesitan.
- Hosts de bloques en tiempo de ejecución: Permite controlar a qué sitios web pueden tener acceso estas extensiones.

El uso de este enfoque ahorra tiempo porque solo necesita establecerlos una vez. Con la directiva de hosts en tiempo de ejecución, se protegerán los sitios más importantes. También hay otras opciones, como:

-   Forzar instalación de extensiones: Permite instalar extensiones de forma silenciosa.
-   Allowlist/blocklist (si es necesario): Decida qué extensiones se pueden instalar.

Siga estos pasos como guía para decidir qué extensiones permitir en su organización.

1. Cree una lista de las extensiones que los empleados necesitan en sus equipos. Pruebe las extensiones en un entorno de prueba para diagnosticar problemas de compatibilidad con aplicaciones internas.
2. Elija qué sitios deben ser más seguros.

   - Descubra los dominios o sitios web internos confidenciales que necesita para impedir que las extensiones realicen cambios o lean los datos.  
   - Impedir el acceso a estos sitios bloqueando las llamadas a la API cuando se ejecuta la extensión. Esto incluye el bloqueo de solicitudes web, la lectura de cookies, la inyección de JavaScript, XHR y así sucesivamente.

3. Determine qué permisos son necesarios para que se ejecuten estas extensiones. Identifique qué permisos representan riesgos potenciales para los usuarios.

   - Audite las extensiones que los usuarios han instalado y vea qué permisos necesitan. Puede ver el archivo JSON del manifiesto de la aplicación web en el código de la extensión. Siga estos pasos para ver qué derechos necesita la extensión:

     - Instale la extensión desde el sitio web [Complementos de Microsoft Edge](https://microsoftedge.microsoft.com/addons/) o desde [Chrome Web Store](https://chrome.google.com/webstore).
     - Pruebe la extensión y comprenda cómo funciona en su organización.
     - Revise los permisos que requiere la extensión accediendo a *edge://extensions*. Por ejemplo, la extensión Microsoft Office que se muestra en la siguiente imagen solicita los permisos "Leer el historial de exploración" y "Mostrar notificaciones". Sopese la utilidad de esta extensión con respecto al nivel de permisos que solicita. Después de aprobar una extensión para su organización, adminístrela con las siguientes herramientas.
   :::image type="content" source="media/microsoft-edge-manage-extensions/manage-extesions-office-extension.png" alt-text="Extensión de Microsoft Office con permisos.":::

   - También puede validar las extensiones solicitadas por los usuarios de la organización antes de aprobarlas en la organización. Algunos de los permisos que usan las extensiones pueden ser imprecisos. Para las aplicaciones críticas para la empresa, puede ponerse en contacto directamente con el desarrollador o el proveedor de la aplicación a fin de obtener más información sobre la extensión o ver el código fuente. Deben poder detallar los cambios que la extensión puede realizar en dispositivos y sitios web.
   - Revise la lista Declarar permisos, que enumera todos los permisos que puede usar una extensión. En esta lista, puede decidir qué permisos desea permitir en su organización.

4. Cree una lista maestra a partir de los datos recopilados. Esta lista incluirá la siguiente información:

   - **Extensiones necesarias**. Esta lista podría organizarse por departamento, ubicación de oficina u otra información relevante.
   - **Extensión Allowlist**. Extensiones necesarias con permisos que pueden bloquearse, pero que podrán ejecutarse. Los usuarios necesitan estas extensiones o se determina que no son un riesgo a través de conversaciones con el proveedor.
   - **Extensión Blocklist**. Extensiones cuya instalación está bloqueada. Las extensiones de esta lista tienen permisos que no se pueden ejecutar. También incluya los sitios y dominios principales que se mantendrán seguros y a los que no se les permitirá el acceso a extensiones. Más adelante puede comparar esta lista de bloqueo con otras que ya tiene implementadas. Es posible que encuentre que puede relajar las directivas de listas de bloqueo actuales.

5. Presente su lista a las partes interesadas y al equipo de sistemas de información para que lo compren.
6. Pruebe la nueva directiva en el laboratorio o con un pequeño paquete piloto en su organización.
7. Implemente estos nuevos conjuntos de directivas para los empleados en fases. Para obtener más información, vea [Usar directivas de grupo para administrar extensiones de Microsoft Edge](microsoft-edge-manage-extensions-policies.md).
8. Revise los comentarios de los usuarios.
9. Repita y ajuste el proceso mensual, trimestral o anualmente.

Con la línea base de los permisos permitidos aplicados y los sitios corporativos confidenciales protegidos, puede proporcionar a su empresa más seguridad a la vez que ofrece una mejor experiencia a los usuarios. El personal puede instalar extensiones que antes no podía, pero no ejecutarlas en sitios empresariales confidenciales.  

## <a name="see-also"></a>Vea también

- [Usar directivas de grupo para administrar extensiones de Microsoft Edge](microsoft-edge-manage-extensions-policies.md)
- [Crear una tienda web para las extensiones de Microsoft Edge](microsoft-edge-manage-extensions-webstore.md)
- [Guía de referencia para la directiva ExtensionSettings](microsoft-edge-manage-extensions-ref-guide.md)
- [Preguntas más frecuentes sobre extensiones de Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)