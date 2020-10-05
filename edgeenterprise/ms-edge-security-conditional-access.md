---
title: Microsoft Edge y acceso condicional
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 10/02/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge y acceso condicional
ms.openlocfilehash: a81d39c15f418dab6565ee7acc45de17f66e3828
ms.sourcegitcommit: 3478cfcf2b03944213a7c7c61f05490bc37aa7c4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/03/2020
ms.locfileid: "11094783"
---
# Microsoft Edge y acceso condicional
  
En el presente artículo, se describe cómo Microsoft Edge es compatible con el acceso condicional y cómo acceder a los recursos protegidos por el acceso condicional.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

Un aspecto clave de la seguridad en la nube es la identidad y el acceso cuando se trata de administrar los recursos de la nube. En un mundo orientado a los móviles y la nube, los usuarios pueden acceder a los recursos de la organización usando diversos dispositivos y aplicaciones desde cualquier lugar. Como resultado de esto, no es suficiente centrarse en quién puede acceder a un recurso. También debes tener en cuenta el modo en que se accede a un recurso. El Acceso condicional de Azure Active Directory (Azure AD) te ayuda a dominar el equilibrio entre seguridad y productividad.

## Obtención de acceso a recursos protegidos de acceso condicional en Microsoft Edge

Microsoft Edge admite el Acceso condicional de Azure AD de forma nativa. No hay necesidad de instalar una extensión diferente. Cuando inicias sesión en un perfil de Microsoft Edge con credenciales Azure AD de empresa, Microsoft Edge permite un acceso sin problemas a los recursos de la nube de empresa protegidos mediante acceso condicional.

En un dispositivo compatible, la identidad que acceda al recurso deberá coincidir con la identidad del perfil.  Si no es así, verás un mensaje como el que se muestra en la siguiente captura de pantalla. En el ejemplo de captura de pantalla, "testadmin@evostsoneboxtest.com" es la cuenta de inicio de sesión necesaria para obtener acceso al recurso.

![Mensaje de acceso condicional en el explorador](./media/edge-security/microsoft-edge-security-conditional-access.png)

Para continuar, debes cambiar al perfil requerido (si tienes uno) o crear un perfil con la identidad coincidente.

Para iniciar sesión y trabajar con su perfil, haz clic en la imagen de cuenta en la esquina superior derecha del explorador. Puedes usar el menú desplegable para:

- Selecciona otro perfil. Haz clic en el nombre de perfil.
- Crear un perfil. Haz clic en **Agregar un perfil**.
- Administra tus perfiles. Haz clic en **Administrar configuración de perfil**.

Esta compatibilidad está disponible en todas las plataformas, incluidas todas las versiones compatibles de Windows y macOS.

### Cómo implementar el acceso condicional de Azure Active Directory

[Implementar acceso condicional](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) proporciona una guía detallada para ayudar a implementar el acceso condicional en Azure Active Directory.

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: Seguridad, compatibilidad y capacidad de administración](/microsoft-edge-video-security-compatibility-manageability.md)
