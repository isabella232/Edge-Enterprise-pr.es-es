---
title: Restablecer datos de Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 07/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Cómo restablecer datos de Microsoft Edge en la nube
ms.openlocfilehash: 65984daea523a7749a28d8ab6a4dd990c5fea849
ms.sourcegitcommit: 9088e839e82d80c72460586e9af0610c6ca71b83
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2021
ms.locfileid: "11675936"
---
# <a name="reset-microsoft-edge-data-in-the-cloud"></a>Restablecer datos de Microsoft Edge en la nube

En este artículo se describen los pasos para restablecer los datos de Microsoft Edge en la nube.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge versión 88 o posterior, a menos que se indique lo contrario.

> [!NOTE]
> Si su inquilino está en un entorno GCC Mod, el administrador de inquilinos deberá presentar una solicitud de soporte técnico a Microsoft para restablecer sus datos.

## <a name="overview"></a>Introducción

Hay situaciones en las que puedes querer restablecer los datos de Microsoft Edge en la nube. Por ejemplo, quieres sincronizar los datos, pero Microsoft Edge notifica que no puede sincronizar los datos. También es posible que quieras asegurarte de que tus datos se quitan de la nube de Microsoft. En ambos casos, Microsoft Edge te permite realizar un restablecimiento de datos en la nube.

## <a name="back-up-your-favorites"></a>Hacer una copia de seguridad de tus favoritos

Antes de restablecer, te recomendamos que hagas una copia de seguridad de tus favoritos. Siga estos pasos para realizar una copia de seguridad de sus favoritos.

1. En Microsoft Edge, **Presione Ctrl + Mayús + O > Elija los tres puntos > Haga clic en Exportar favoritos**.
2. Elija el archivo en el que quiere guardar los favoritos. Puede escribir su propio nombre de archivo o usar el nombre que Microsoft Edge proporciona de forma predeterminada, "favoritos_mes_día_año.html" como nombre de archivo. Por ejemplo, "favorites_07_05_21.html". Si necesita restaurar los favoritos más adelante, puede hacerlo desde ese archivo.
3. Haz clic en **Guardar**.

## <a name="perform-a-reset-to-fix-a-synchronization-problem"></a>Realizar un restablecimiento para corregir un problema de sincronización

Si Microsoft Edge informa de que no puede sincronizar los datos y sugiere restablecerlos, realiza un restablecimiento para corregir el problema.

Sigue los pasos siguientes para restablecer.

1. En primer lugar, asegúrate de que has cerrado la sesión de Microsoft Edge en todos los dispositivos, incluidos los dispositivos móviles, excepto el dispositivo en el que estás realizando el restablecimiento. Para cerrar la sesión de Microsoft Edge, seleccione **Configuración > Perfiles > Cerrar sesión**. Al cerrar sesión, no seleccione la opción para borrar los favoritos, la configuración, etc. de su dispositivo local.
2. Después de cerrar la sesión de todos los demás dispositivos, abra Microsoft Edge en el escritorio. Seleccione **Configuración > Perfiles > Restablecer sincronización**. En el cuadro de diálogo resultante, elija reanudar la sincronización después de restablecer los datos y, a continuación, seleccione **Restablecer ahora**.

## <a name="perform-a-reset-to-remove-your-data-from-microsofts-cloud"></a>Realizar un restablecimiento para quitar los datos de la nube de Microsoft

Si quieres quitar los datos de la nube de Microsoft, sigue estos pasos para restablecer.

1. Detenga la sincronización en dispositivos excepto el dispositivo en el que está realizando el restablecimiento.  En Microsoft Edge, seleccione **Configuración > Perfiles > Desactivar sincronización**.  
2. Después de detener la sincronización, seleccione **Configuración > Perfiles > Restablecer sincronización**. En el cuadro de diálogo resultante, **no** elija reanudar la sincronización en este dispositivo después de restablecer la sincronización. Seleccione **Restablecer**.

## <a name="what-to-expect-during-and-after-a-data-reset"></a>Qué esperar durante y después de restablecer datos

Un restablecimiento de datos puede tardar entre unos segundos y unos minutos, en función de la cantidad de datos que hayas almacenado en la nube de Microsoft. En algunos casos, es posible que veas un mensaje que indica que no se pudo completar un restablecimiento y una sugerencia para volver a restablecerlo. En ese caso, espera unas pocas horas e intenta restablecer los datos de nuevo. Si sigues sin poder restablecer los datos, ponte en contacto con el soporte técnico de Microsoft Edge.

Después de completar correctamente un restablecimiento de datos, los datos volverán a sincronizarse desde el dispositivo si eliges reanudar la sincronización después del restablecimiento. Si quieres sincronizar desde otros dispositivos, deberás volver a iniciar sesión en esos dispositivos. Sin embargo, si no has elegido reanudar la sincronización, los datos de Microsoft Edge se quitarán de la nube y los datos ya no se sincronizarán.

## <a name="see-also"></a>Consulta también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sincronización de Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
