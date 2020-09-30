---
title: Aprovisionar favoritos en Microsoft Edge
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 09/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Aprovisionar favoritos en Microsoft Edge
ms.openlocfilehash: 94bd42573bdbc0fd1b971ded1c82e5fe152acc54
ms.sourcegitcommit: 854dd73eb168960c0eb4b483f81a8efe88806a64
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088724"
---
# Aprovisionar favoritos en Microsoft Edge

Hemos realizado mejoras en el aprovisionamiento de favoritos basándonos en los comentarios de los clientes. A partir de la versión 85 de Microsoft Edge, los administradores ya no tienen que diseñar manualmente un archivo para aprovisionar favoritos. Los administradores pueden agregar favoritos y carpetas mediante la interfaz de usuario de Microsoft Edge para generar un archivo que puede exportarse a una directiva de grupo.

En este artículo se describe cómo aprovisionar un conjunto de favoritos y de carpetas en la organización. Puede usar la directiva [Configurar favoritos](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#configure-favorites) para aprovisionar favoritos y carpetas.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 85 o posterior.

## Requisitos previos y recomendaciones

- La versión 85 de Microsoft Edge con la plantilla administrativa adecuada instalada para las directivas de grupo.
- Le recomendamos usar un perfil nuevo en Microsoft Edge para aprovisionar estos favoritos. Todos los favoritos que se guarden con el perfil se incluirán en la exportación.  

## Aprovisionar favoritos y carpetas

Siga los siguientes pasos para aprovisionar favoritos y carpetas para los usuarios.

1. Vaya a la barra de direcciones de Microsoft Edge y escriba esta dirección URL: *edge://flags/#edge-favorites-admin-export*.
2. En **Exportar la configuración de favoritos para administradores**, seleccione **Habilitado** en la lista desplegable y, a continuación, haga clic en **Reiniciar**.

3. Vaya a la página **Favoritos** en *edge://favorites* para agregar los favoritos y las carpetas que quiera aprovisionar.

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. Cuando termine de agregar favoritos y carpetas, los exportará para que puedan usarse en la directiva **Configurar favoritos**. Vaya a la barra de direcciones, desplácese hasta *edge://favorites*, haga clic en los puntos suspensivos "**...**" y elija **Exportar la configuración de favoritos**. La siguiente captura de pantalla muestra las opciones que tiene para aprovisionar favoritos.

   ![Opciones de menú para trabajar con favoritos.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. En **Exportar la configuración de favoritos**, especifique un nombre para la carpeta que verán los usuarios. Escriba el nombre de la carpeta y elija el formato de plataforma que quiera usar. Haga clic en **Copiar en el portapapeles**. La siguiente captura de pantalla muestra "Favoritos administrados" para el nombre de la carpeta, y la plataforma es Windows.

   ![Cuadro de diálogo para exportar favoritos a una carpeta de Windows.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. Abra el Editor de directivas de grupo, desplácese a *Configuración del equipo/Plantillas administrativas/* y seleccione **Configurar favoritos**. Habilite la directiva "Configurar favoritos". En **Opciones:**, pegue el contenido exportado en el área de texto Configurar favoritos y, a continuación, haga clic en **Aplicar**. La siguiente captura de pantalla muestra un ejemplo de la carpeta "Favoritos administrados" del paso 5.

   ![Use gpedit para habilitar y configurar la directiva "Configurar favoritos".](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. Haga clic en **Aceptar** o **Aplicar** para guardar la configuración de la directiva.

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)