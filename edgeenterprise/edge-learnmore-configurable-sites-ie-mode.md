---
title: Microsoft Edge y sitios configurables en modo IE
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/28/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge y sitios configurables en modo IE
ms.openlocfilehash: 1bffdef8c88b7a83d999b29763fcca258102ed51
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447334"
---
# <a name="learn-about-configurable-sites-in-ie-mode"></a>Obtenga información sobre los sitios configurables en modo IE

En este artículo, se explica la característica de sitios configurables de la lista de sitios del Modo de empresa al usar el modo IE en Microsoft Edge.

## <a name="prerequisites"></a>Requisitos previos

- Actualizaciones de Windows

  - Windows 10, versión 1909; Windows Server, versión 1909 (KB4550945 o superior)
  - Windows 10, versión 1903; Windows Server, versión 1903 (KB4550945 o superior)
  - Windows 10, versión 1809; Windows Server, versión 1809, y Windows Server 2019 (KB4550969 o superior)
  - Windows 10, versión 1803 (KB4550944 o superior)
  - Windows 10, versión 1607; Windows Server 2016 (KB4556826 o superior)
  - Versión inicial de Windows 10, julio de 2015 (KB4550947 o superior)
  - Windows 8.1 (KB4556798 o superior)

- Microsoft Edge, versión 83 o posterior
- [Modo IE](./edge-ie-mode.md) configurado con la lista de sitios del Modo de empresa

## <a name="overview"></a>Introducción

La configuración de sitios que necesitan el modo IE en la lista de sitios del Modo de empresa funcionará correctamente para la mayoría de los entornos con aplicaciones heredadas. Sin embargo, en algunos casos, este método no es el más adecuado para configurar un subconjunto de sitios para abrirlo en modo IE sin representar un dominio completo en modo IE. Por ejemplo, este método no es el más adecuado cuando el entorno contiene tanto aplicaciones modernas como heredadas que se ejecutan en un único servidor y usted quiere tener flexibilidad para representar en modo IE solo las aplicaciones heredadas, y para representar las aplicaciones restantes en el modo de Microsoft Edge.

La solución consiste en usar la característica de sitios configurables de la lista de sitios del Modo de empresa. Cuando la característica está habilitada, Microsoft Edge permite a los sitios con la etiqueta "configurable" participar en la determinación del motor en modo IE.

## <a name="how-configurable-sites-works"></a>Funcionamiento de los sitios configurables

### <a name="automatic-switching-from-the-microsoft-edge-engine-to-the-ie-mode-engine"></a>Cambio automático del motor de Microsoft Edge al motor en modo IE

Para usar la característica de sitios configurables, necesitará uno o más sitios de la lista de sitios del Modo de empresa para tener la opción `<open-in>Configurable</open-in>`.

Por ejemplo:

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

Cuando la característica de sitios configurables está habilitada, sucede lo siguiente:

1. Cuando se realiza una solicitud a un sitio configurable, Microsoft Edge envía el encabezado de solicitud HTTP "`X-InternetExplorerModeConfigurable: 1`".
2. Es posible que un sitio configurable envíe una respuesta de redirección (por ejemplo, HTTP 302) con el encabezado de respuesta HTTP "`X-InternetExplorerMode: 1`", para solicitar que Microsoft Edge cargue el sitio en modo IE.
3. El destino del redireccionamiento (es decir, el valor del encabezado de respuesta de **Ubicación**) también tiene que ser un sitio **Configurable** o **Neutro**; de lo contrario, el encabezado de respuesta en modo IE se omitirá. Por lo general, se espera que el destino del redireccionamiento sea el mismo que la dirección URL original. Sin embargo, no tiene por qué ser así necesariamente.

   > [!NOTE]
   > La respuesta de redirección está sujeta al almacenamiento en caché, según el comportamiento normal de almacenamiento en caché de HTTP de Microsoft Edge para redirecciones.

### <a name="switching-back-from-ie-mode-engine-to-microsoft-edge-engine"></a>Volver a cambiar el motor del modo IE al motor de Microsoft Edge

Al habilitar los sitios configurables en Microsoft Edge, se habilitan automáticamente los siguientes comportamientos en las pestañas del modo IE:

1. Al realizar una solicitud a un sitio configurable, las pestañas del modo IE envían el encabezado de solicitud HTTP "`X-InternetExplorerModeConfigurable: 1`", al igual que las pestañas de Microsoft Edge.
2. Es posible que un sitio configurable envíe una respuesta de redirección (por ejemplo, HTTP 302) con el encabezado de respuesta HTTP "`X-InternetExplorerMode: 0`", para solicitar que la navegación vuelva al modo Microsoft Edge.
3. El destino del redireccionamiento (es decir, el valor del encabezado de respuesta de **Ubicación**) también tiene que ser un sitio **Configurable** o **Neutro**; de lo contrario, el encabezado de respuesta en modo IE se omitirá. Por lo general, se espera que el destino del redireccionamiento sea el mismo que la dirección URL original. Sin embargo, no tiene por qué ser así necesariamente.

   > [!NOTE]
   > La respuesta de redirección está sujeta al almacenamiento en caché, según el comportamiento normal de almacenamiento en caché de HTTP de Microsoft Edge para redirecciones.

> [!TIP]
> Ambos motores de exploración envían el mismo encabezado de solicitud "`X-InternetExplorerModeConfigurable: 1`" a sitios configurables. Debe usar el encabezado de solicitud de agente de usuario para distinguir las solicitudes del modo de Microsoft Edge de las del modo IE, para evitar el redireccionamiento cuando el sitio ya se está cargando en el motor adecuado.

## <a name="see-also"></a>Consulte también

- [Acerca del modo IE](./edge-ie-mode.md)
- [Información adicional del modo de empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)