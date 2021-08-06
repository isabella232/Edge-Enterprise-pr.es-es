---
title: Compatibilidad con la plataforma para las características de Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Resumen de la compatibilidad de la plataforma con las características de Microsoft Edge
ms.openlocfilehash: 1ac512d4e9e6279ce2d6fcff5aebede0974eb5cdcf9211c957ace9f015b95010
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727473"
---
# <a name="platform-support-for-microsoft-edge-features"></a>Compatibilidad con la plataforma para las características de Microsoft Edge

En este artículo se resume la compatibilidad de la plataforma con las características de Microsoft Edge.

> [!NOTE]
> Este artículo se aplica a Microsoft Edge, versión 77 o posterior.

## <a name="feature-matrix-for-platforms"></a>Matriz de características de las plataformas

En las siguientes tablas se resume la compatibilidad de las características con las plataformas Windows y macOS.

> [!NOTE]
> Actualmente, Android e iOS no están representados en las tablas de soporte, pero seguimos trabajando en esta información y la actualizaremos.

| Características de seguridad |Win 10|Win 8.1|Win 7|macOS|Dirección URL|
|--------|-------|--------|-----|-------|---|
|Acceso condicional a Azure Active Directory (Azure AD)|Sí|Sí|Sí|Sí|[Acceso condicional a Azure AD](/deployedge/ms-edge-security-conditional-access#accessing-conditional-access-protected-resources-in-microsoft-edge)|
|Protección de aplicaciones de Microsoft Defender|Sí (1890+)|No|No|No|[Protección de aplicaciones de Microsoft Defender](/deployedge/microsoft-edge-security-windows-defender-application-guard) |
|SmartScreen de Microsoft Defender|Sí|Sí|Sí|Sí|[SmartScreen de Microsoft Defender](/deployedge/microsoft-edge-security-smartscreen) |
|Administrador de puntos de conexión de Microsoft|Sí|No|No|No|[Administrador de puntos de conexión de Microsoft](/deployedge/microsoft-edge-security-dlp#microsoft-endpoint-data-loss-prevention-endpoint-dlp)|
|Supervisión de contraseña|Sí|Sí|Sí|Sí|[Supervisión de contraseña](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Generador de contraseñas|Sí|Sí|Sí|Sí|[Generador de contraseñas](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Windows Information Protection (WIP)|Sí (1607+)|No|No|No|[WIP](/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)|

|Características de identidad| Win 10 | Win 8.1 | Win 7 | macOS | Dirección URL |
|--|--|--|--|--|--|
|Inicio de sesión automático (híbrido/AAD-J)|Sí|Sí|Sí|No|[hybrid/AAD-J](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Inicio de sesión automático (unido a dominio)|Sí|Sí|Sí|No|[unido a dominio](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Inicio de sesión automático (la cuenta por defecto del sistema operativo es MSA)|Sí (1709+)|No|No|No|[MSA](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Inicio de sesión único (SSO) del navegador a la web|Sí|Sí|Sí|Sí|[Browser-Web SSO](https://www.microsoft.com/microsoft-365/roadmap?featureid=66332)|
|Conmutación guiada/"Conmutación automática de perfiles"|Sí|Sí|Sí|Sí|[Utilizar varios perfiles en el trabajo y en casa](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Múltiples perfiles|Sí|Sí|Sí|Sí|[Utilizar varios perfiles en el trabajo y en casa](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Sincronización local para Active Directory (AD)|Sí|Sí|Sí|No|[Sincronización local para usuarios de Active Directory (AD)](/deployedge/microsoft-edge-on-premises-sync) |
|SSO de conexión directa|Sí (1709+)|Sí|Sí|Sí|[SSO de conexión directa](/deployedge/microsoft-edge-security-identity#seamless-sso)|
|SSO con Token de actualización principal (PRT)|Sí (1709+)|Sí|Sí|No|[SSO con PRT](/deployedge/microsoft-edge-security-identity#sso-with-primary-refresh-token-prt)|
|Autenticación integrada de Windows (WIA)|Sí|Sí|Sí|Sí* (directiva necesaria)|[WIA](/deployedge/microsoft-edge-security-identity#windows-integrated-authentication-wia)|

|Características adicionales|Win 10|Win 8.1|Win 7|macOS|Dirección URL|
|--------|-------|--------|-----|-------|---|
|Colecciones|Sí|Sí|Sí|Sí|[Colecciones](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/) |
|Página de pestaña nueva de la empresa|Sí|Sí|Sí|Sí|[Página de pestaña nueva](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/) |
|Modo IE|Sí|Sí|Sí|No|[Modo IE](/deployedge/edge-ie-mode#prerequisites)|
|Pantalla completa|Sí|No|No|No|[Pantalla completa](/deployedge/microsoft-edge-configure-kiosk-mode)|
|Búsqueda de Microsoft en Bing|Sí|Sí|Sí|Sí|[Búsqueda inteligente en Bing](https://www.microsoft.com/edge/business/intelligent-search-with-bing) |
|Lector de PDF|Sí|Sí|Sí|Sí|[Lector de PDF](/deployedge/microsoft-edge-pdf) |
|Compras|Sí|Sí|Sí|Sí|[Compras](https://techcommunity.microsoft.com/t5/articles/introducing-shopping-with-microsoft-edge/m-p/1870080) |
|Pestañas suspendidas|Sí|Sí|Sí|Sí|[Introducción a las características](/deployedge/microsoft-edge-relnote-stable-channel)<br>[Última publicación del blog](https://blogs.windows.com/msedgedev/2021/03/04/edge-89-performance/)<br>[Directivas de grupo](/deployedge/microsoft-edge-policies#sleeping-tabs-settings)|
|Sincronización|Sí|Sí|Sí|Sí| [Sincronización de empresa](/deployedge/microsoft-edge-enterprise-sync) |
|Versión de reversión|Sí|Sí|Sí|No|[Versión de reversión](/deployedge/edge-learnmore-rollback) |
|Pestañas verticales|Sí|Sí|Sí|Sí| |

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)