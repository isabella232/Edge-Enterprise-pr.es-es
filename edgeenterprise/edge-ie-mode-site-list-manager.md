---
title: 'Enterprise Site List Manager en Microsoft Edge '
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Habilitar y usar Enterprise Site List Manager en Microsoft Edge '
ms.openlocfilehash: aa468888a05753fb5b033a8b99c2f6045f4e1b12
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617410"
---
# <a name="enterprise-site-list-manager-in-microsoft-edge"></a>Enterprise Site List Manager en Microsoft Edge

>[!Note]
> La aplicación de escritorio Internet Explorer 11 se retirará y dejará de recibir soporte el 15 de junio de 2022 (para ver una lista de lo que se verá afectado, [consulte las preguntas frecuentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Las mismas aplicaciones y sitios de IE11 que usa hoy pueden abrirse en Microsoft Edge mediante el uso del modo Internet Explorer. [Más información aquí](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

En este artículo, se explica cómo usar y habilitar el acceso de Enterprise Site List Manager en Microsoft Edge para crear, editar y exportar la lista de sitios del Modo de empresa para el modo Internet Explorer.

> [!NOTE]
> Este artículo se aplica a la versión 89 de Microsoft Edge o posteriores. 

## <a name="overview"></a>Información general

Enterprise Site List Manager es una versión dentro del explorador de la [herramienta independiente Enterprise Mode Site List Manager](https://www.microsoft.com/download/details.aspx?id=49974) que le permite crear, editar y exportar la lista de sitios de la organización.

Las futuras mejoras en la herramienta para el modo Internet Explorer estarán disponibles a través de Enterprise Site List Manager en Microsoft Edge. La herramienta independiente seguirá estando disponible en el Centro de descargas, pero no recibirá ninguna actualización de características.

## <a name="enabling-access-to-enterprise-site-list-manager"></a>Habilitar el acceso a Enterprise Site List Manager

Puede configurar el acceso a la herramienta mediante la directiva de grupo [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed).

Si está habilitada, los usuarios verán una opción denominada Enterprise Site List Manager en el panel de navegación izquierdo en *edge://compat*. Si está deshabilitado, los usuarios no verán el punto de entrada a Enterprise Site List Manager en el panel de navegación izquierdo. Este es el comportamiento predeterminado.

## <a name="using-the-enterprise-site-list-manager"></a>Usar Enterprise Site List Manager

La herramienta Enterprise Site List Manager usa la versión 2 del esquema. Si importa la versión 1 del esquema a Enterprise Site List Manager (esquema v.2), se guardará el archivo XML en la versión 2 del esquema. Consulte la [Guía del esquema v.2 del Modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

### <a name="add-single-sites-to-your-site-list"></a>Agregar sitios únicos a la lista de sitios  

Siga estos pasos para agregar sitios individuales a la lista de sitios.

> [!NOTE]
> Solo puede agregar direcciones URL específicas, no zonas de Internet o de Intranet.

1. En Enterprise Site List Manager, haga clic en  **Agregar un sitio**.
2. Escriba la dirección URL del sitio web que desea agregar, por ejemplo:  <domain>.com o  <domain>.com/<path>  en el cuadro de dirección URL.
3. Seleccione una de las siguientes opciones en la lista**Abrir en** :

   - **IE11**. Abre el sitio en la aplicación IE11.
   - **Modo IE**. Abre el sitio en modo Internet Explorer en Microsoft Edge si está habilitado y, en caso contrario, en la aplicación IE11. Consulte  [Modo Internet Explorer en Microsoft Edge](./edge-ie-mode.md).
   - **MSEdge**. Abre el sitio en Microsoft Edge.
   - **Configurable**. Permite que el sitio participe en la determinación del motor en el modo IE. Consulte [Sitios configurables en modo IE](./edge-learnmore-configurable-sites-ie-mode.md).
   - **Ninguno**. Se abre en el explorador que elija el usuario.  

4. En  **Modo de compatibilidad**, elija una de las siguientes opciones:

   - **IE8Enterprise**. Carga el sitio en el Modo de empresa en IE8.
   - **IE7Enterprise**. Carga el sitio en el Modo de empresa en IE7.
   - **IE[x]**. Donde [x] es el número de modo del documento y el sitio carga en el modo del documento especificado.
   - **Modo predeterminado**. Carga el sitio con el modo de compatibilidad predeterminado para la página.

   La ruta de acceso dentro de un dominio puede requerir un modo de compatibilidad distinto del propio dominio. Por ejemplo, el dominio podría verse bien en el explorador predeterminado IE11, pero la ruta de acceso puede tener problemas y requerir el uso del Modo de empresa. Si ha agregado el dominio anteriormente, su opción de compatibilidad original seguirá estando seleccionada. Sin embargo, si el dominio es nuevo, el  **Modo de empresa en IE8**  se selecciona de manera automática.

   El Modo de empresa tiene prioridad sobre los modos de documento, por lo que los sitios que ya están incluidos en la lista de sitios del Modo de empresa no se verán afectados por esta actualización y seguirán cargándose en el Modo de empresa, como de costumbre. Para obtener información más específica acerca de los modos del documento, consulte  [Corregir problemas de compatibilidad web con los modos del documento y la lista de sitios del Modo de empresa](/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list).

5. La casilla **Permitir redireccionamiento** se aplica al tratamiento de redireccionamientos del lado del servidor. Si marca esta casilla, se abrirán los redireccionamientos del lado del servidor en el explorador especificado por la etiqueta de apertura. Para más información, consulte  [aquí](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes).
6. Escriba los comentarios sobre el sitio web en el cuadro de **Comentario**. Los administradores solo pueden ver los comentarios mientras están en esta herramienta, y estos comentarios se conservan en el XML de la lista de sitios.
7. Haga clic en  **Agregar** para agregar el sitio a la lista de sitios.

### <a name="export-site-list-to-xml"></a>Exportar lista de sitios a XML

Después de crear la lista de sitios en Enterprise Site List Manager, puede exportar el contenido a un archivo Enterprise Mode (.EMIE) o XML. 

> [!NOTE]
> Este archivo incluye todas las direcciones URL, incluidas las selecciones del modo de compatibilidad, y debería guardarse en algún lugar seguro.

Para exportar la lista de sitios, siga estos pasos:

1. En Enterprise Site List Manager, haga clic en **Exportar a XML**.
2. Escriba un **número de versión** y un **nombre de archivo**.
3. Haga clic en **Exportar**.

Puede guardar el archivo localmente o en un recurso compartido de red. No obstante, debe estar seguro de implementarlo en la ubicación especificada en la clave del Registro. Para obtener más información, consulte  [Activar el modo Internet Explorer y usar una lista de sitios](./edge-ie-mode-policies.md).

### <a name="import-multiple-sites-to-your-site-list"></a>Importar varios sitios a la lista de sitios

Después de crear el archivo .xml, puede agregar sitios de manera masiva al editor con **Importar desde XML**.

Si desea reemplazar todo el contenido del editor, haga clic en los puntos suspensivos (...) y, a continuación, elija **Borrar lista**. Después de limpiar el editor, siga estos pasos para importar el sitio.

1. En Enterprise Site List Manager, haga clic en **Importar desde XML**. 
2. Haga clic en **Elegir archivo** para seleccionar la lista de sitios para agregar los sitios incluidos a la herramienta. Seleccione la lista de sitios que desea agregar y, a continuación, haga clic en **Abrir**. Los formatos admitidos para importar son .xml, .emie o .txt que contengan el esquema v.2 para la lista de sitios del Modo de empresa. Consulte la [Guía del esquema v.2 del Modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).
3. Haga clic en  **Cargar**  para agregar los sitios desde el archivo TP al editor.

Puede guardar el archivo localmente o en un recurso compartido de red. No obstante, debe estar seguro de implementarlo en la ubicación especificada en la clave del Registro. Para obtener más información, consulte  [Activar el modo Internet Explorer y usar una lista de sitios](./edge-ie-mode-policies.md).

### <a name="edit-sites-in-your-site-list"></a>Editar sitios en la lista de sitios

 Puede editar atributos de entradas de sitio existentes en Enterprise Site List Manager. También puede agregar, quitar o suprimir comentarios asociados.

1. En Enterprise Site List Manager, haga clic en los puntos suspensivos (...) y elija **Editar sitio** para la dirección URL que desea editar.
2. Puede editar cualquier atributo de la entrada del sitio, excepto la dirección URL. Haga clic en **Guardar** después de finalizar la edición.

   > [!NOTE]
   > Si desea eliminar una entrada de sitio, elija **Eliminar sitio** en el paso 1.

3. Haga clic en **Exportar a XML** y guarde el archivo actualizado.

Puede guardar el archivo localmente o en un recurso compartido de red. No obstante, debe estar seguro de implementarlo en la ubicación especificada en la clave del Registro. Para obtener más información, consulte  [Activar el modo Internet Explorer y usar una lista de sitios](./edge-ie-mode-policies.md).

### <a name="preview-your-site-list-in-xml-format"></a>Obtener una vista previa de la lista de sitios en formato XML

Puede obtener una vista previa de los sitios en el editor en formato XML antes de exportar y guardar el archivo en la ubicación de la lista de sitios. Haga clic en **Vista previa XML** para abrir el archivo en una pestaña nueva.

### <a name="search-in-the-enterprise-site-list-manager"></a>Buscar en Enterprise Site List Manager

Puede realizar una búsqueda para ver si un sitio específico ya aparece en la lista de sitios, de modo que no intente agregarlo de nuevo.

Para buscar, escriba parte de la dirección URL en el cuadro de búsqueda  **Filtrar sitios por dirección URL** en la esquina superior derecha del editor.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Acerca del modo IE](./edge-ie-mode.md)
- [Guía del esquema v.2 del Modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)
- [Información adicional del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)