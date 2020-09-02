---
title: Usar Microsoft Edge para protegerse de aplicaciones potencialmente no deseadas
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 03/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Usar Microsoft Edge para protegerse de aplicaciones potencialmente no deseadas
ms.openlocfilehash: 615442acc0e9ed58da37aa0ef8b3747e916a8024
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981045"
---
# Protección contra aplicaciones potencialmente no deseadas (PUAs)

Este artículo explica cómo puede protegerse contra las aplicaciones potencialmente no deseadas (PUA) usando Microsoft Edge o usando el Antivirus Windows Defender.

> [!NOTE]
> Este artículo se aplica a la versión 80 o posterior de Microsoft Edge.

## Introducción

Las aplicaciones potencialmente no deseadas no se consideran virus o malware, pero estas aplicaciones pueden realizar acciones en los puntos de conexión que afecten negativamente al rendimiento o al uso de los mismos. Por ejemplo, el *Software de evasión* trata activamente de evadir la detección por parte de los productos de seguridad. Este tipo de software puede aumentar el riesgo de que su red se infecte con algún malware actual. La PUA también puede referirse a aplicaciones que se consideran de mala reputación.

Para una descripción de los criterios utilizados para clasificar el software como una PUA, consulte [Aplicación potencialmente no deseada](https://docs.microsoft.com/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).

## Protección en contra de la PUA con Microsoft Edge

Microsoft Edge (versión 80.0.361.50 o posterior) bloquea las descargas de PUA y las URL de recursos asociados.

Puede configurar la protección activando la función **Bloquear aplicaciones potencialmente no deseadas** en Microsoft Edge.

> [!NOTE]
> La entrada del [blog del Microsoft Edge Team](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) describe esta nueva característica, y explica cómo manejar una aplicación mal etiquetada o reportar una aplicación como no deseada.

### Para habilitar la protección de PUA:

1. Abra **Configuración** en el navegador.
2. Seleccione **Privacidad y servicios**.
3. En la sección de **Servicios**, compruebe que la pantalla **SmartScreen de Microsoft Defender** esté activada. Si no, entonces active la pantalla SmartScreen de Microsoft Defender. El ejemplo de la siguiente captura de pantalla muestra que el navegador es administrado por la organización y que el SmartScreen de Microsoft Defender está activado.

   ![Active el Microsoft Edge PUA en Ajustes](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. En la sección de **Servicios**, utilice el botón que se muestra en la captura de pantalla anterior para activar la opción de **Bloquear aplicaciones potencialmente no deseadas**.

   > [!TIP]
   > Puede explorar con seguridad la función de bloqueo de URL de la protección PUA probándola en una de nuestras[páginas de demostración](https://demo.smartscreen.msft.net/) de SmartScreen de Windows Defender.

Cuando Microsoft Edge detecte un PUA, verá un mensaje como el de la siguiente captura de pantalla.

   ![Mensaje de advertencia de Microsoft Edge PUA](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### Para crear un bloque en contra de los URLs asociados a la PUA

Después de activar la protección PUA en Microsoft Edge, Windows Defender SmartScreen lo protegerá de las URLs asociadas a PUA.

Hay varias formas en que los administradores pueden configurar cómo Microsoft Edge y el SmartScreen de Windows Defender trabajan juntos para proteger a los usuarios de las URLs asociadas a la PUA. Para más información, consulta lo siguiente:

- [Configurar las opciones de directiva de Microsoft Edge en Windows](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge)
- [Configuración de SmartScreen](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreen-settings)
- [Directiva de SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [Configurar SmartScreen de Windows Defender](https://docs.microsoft.com/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

Los administradores también pueden personalizar la lista de bloqueo de la Protección contra amenazas avanzada de Microsoft Defender (Microsoft Defender ATP). Pueden utilizar el portal de Protección contra amenazas avanzada de Microsoft Defender para [crear y gestionar indicadores para IPs y URLs](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).

## Protección contra la PUA con el Antivirus Windows Defender

El artículo [Detectar y bloquear aplicaciones potencialmente no deseadas](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) también describe cómo se puede configurar el Antivirus Windows Defender para activar la protección PUA. Puede configurar la protección usando cualquiera de las siguientes opciones:

- [Microsoft Intune](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [Administrador de configuración de Microsoft Endpoint](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [Directiva de grupo](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [Cmdlets de PowerShell](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

Cuando Windows Defender detecta un archivo PUA en un punto de conexión, lo pone en cuarentena y lo notifica al usuario ([a menos que las notificaciones estén desactivadas](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) en el mismo formato que una detección de amenazas normal (con el prefacio de "PUA:".) Las amenazas detectadas también aparecen en la [lista de cuarentena de la aplicación de Seguridad de Windows](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).

### Notificaciones y eventos de PUA

Hay varias formas en que un administrador puede ver los eventos de PUA:

- En el Visor de eventos de Windows, pero no en el Administrador de Configuración de Microsoft Endpoint o en Intune.
- En un correo electrónico si las notificaciones de correo electrónico para las detecciones de la PUA están activadas.
- En los registros de eventos del [Antivirus Windows Defender](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus), donde se registra un evento PUA bajo el ID de evento 1116 con el mensaje: "La plataforma antimalware detectó malware u otro software potencialmente no deseado".

> [!NOTE]
> Los usuarios verán que "*.exe ha sido bloqueado como una aplicación potencialmente no deseada por la aplicación SmartScreen de Microsoft Defender".

### Habilitar una aplicación en la lista

Al igual que Microsoft Edge, el Antivirus Windows Defender proporciona una forma de permitir archivos que se bloquean por error o que se necesitan para completar una tarea. Si esto sucede, puedes habilitar un archivo en la lista Para obtener más información, consulte [Cómo configurar Endpoint Protection en el Administrador de configuración](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders) para aprender a excluir archivos o carpetas específicos.

## Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Protección contra amenazas](https://docs.microsoft.com/windows/security/threat-protection/index)
- [Configurar la protección en tiempo real, heurística y de comportamiento](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [Protección de última generación](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [Base de seguridad para el Microsoft Edge basado en el Chrome, versión 79](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)
