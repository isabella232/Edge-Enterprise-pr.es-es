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
ms.openlocfilehash: 4e9d513c4d1144d4109064d7aa42e4ef31a59b88
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448034"
---
# <a name="protect-against-potentially-unwanted-applications-puas"></a><span data-ttu-id="6d201-103">Protección contra aplicaciones potencialmente no deseadas (PUAs)</span><span class="sxs-lookup"><span data-stu-id="6d201-103">Protect against potentially unwanted applications (PUAs)</span></span>

<span data-ttu-id="6d201-104">Este artículo explica cómo puede protegerse contra las aplicaciones potencialmente no deseadas (PUA) usando Microsoft Edge o usando el Antivirus Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="6d201-104">This article explains how you can protect against potentially unwanted applications (PUAs) using Microsoft Edge or by using Windows Defender Antivirus.</span></span>

> [!NOTE]
> <span data-ttu-id="6d201-105">Este artículo se aplica a la versión 80 o posterior de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6d201-105">This article applies to Microsoft Edge version 80 or later.</span></span>

## <a name="overview"></a><span data-ttu-id="6d201-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="6d201-106">Overview</span></span>

<span data-ttu-id="6d201-107">Las aplicaciones potencialmente no deseadas no se consideran virus o malware, pero estas aplicaciones pueden realizar acciones en los puntos de conexión que afecten negativamente al rendimiento o al uso de los mismos.</span><span class="sxs-lookup"><span data-stu-id="6d201-107">Potentially unwanted applications aren't considered to be viruses or malware, but these apps might perform actions on endpoints that adversely affect endpoint performance or use.</span></span> <span data-ttu-id="6d201-108">Por ejemplo, el *Software de evasión* trata activamente de evadir la detección por parte de los productos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6d201-108">For example, *Evasion software* actively tries to evade detection by security products.</span></span> <span data-ttu-id="6d201-109">Este tipo de software puede aumentar el riesgo de que su red se infecte con algún malware actual.</span><span class="sxs-lookup"><span data-stu-id="6d201-109">This kind of software can increase the risk of your network being infected with actual malware.</span></span> <span data-ttu-id="6d201-110">La PUA también puede referirse a aplicaciones que se consideran de mala reputación.</span><span class="sxs-lookup"><span data-stu-id="6d201-110">PUA can also refer to applications that are considered to have poor reputation.</span></span>

<span data-ttu-id="6d201-111">Para una descripción de los criterios utilizados para clasificar el software como una PUA, consulte [Aplicación potencialmente no deseada](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).</span><span class="sxs-lookup"><span data-stu-id="6d201-111">For a description of the criteria used to classify software as a PUA, see [Potentially unwanted application](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).</span></span>

## <a name="protect-against-pua-with-microsoft-edge"></a><span data-ttu-id="6d201-112">Protección en contra de la PUA con Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6d201-112">Protect against PUA with Microsoft Edge</span></span>

<span data-ttu-id="6d201-113">Microsoft Edge (versión 80.0.361.50 o posterior) bloquea las descargas de PUA y las URL de recursos asociados.</span><span class="sxs-lookup"><span data-stu-id="6d201-113">Microsoft Edge (version 80.0.361.50 or later) blocks PUA downloads and associated resource URLs.</span></span>

<span data-ttu-id="6d201-114">Puede configurar la protección activando la función **Bloquear aplicaciones potencialmente no deseadas** en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6d201-114">You can set up protection by enabling the **Block potentially unwanted apps** feature in Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="6d201-115">La entrada del [blog del Microsoft Edge Team](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) describe esta nueva característica, y explica cómo manejar una aplicación mal etiquetada o reportar una aplicación como no deseada.</span><span class="sxs-lookup"><span data-stu-id="6d201-115">The [Microsoft Edge Team blog post](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) describes this new feature and explains how to handle a mislabeled app or report an app as unwanted.</span></span>

### <a name="to-enable-pua-protection"></a><span data-ttu-id="6d201-116">Para habilitar la protección de PUA:</span><span class="sxs-lookup"><span data-stu-id="6d201-116">To enable PUA protection:</span></span>

1. <span data-ttu-id="6d201-117">Abra **Configuración** en el navegador.</span><span class="sxs-lookup"><span data-stu-id="6d201-117">Open **Settings** in the browser.</span></span>
2. <span data-ttu-id="6d201-118">Seleccione **Privacidad y servicios**.</span><span class="sxs-lookup"><span data-stu-id="6d201-118">Select **Privacy and services**.</span></span>
3. <span data-ttu-id="6d201-119">En la sección de **Servicios**, compruebe que la pantalla **SmartScreen de Microsoft Defender** esté activada.</span><span class="sxs-lookup"><span data-stu-id="6d201-119">In the **Services** section, check to see that **Microsoft Defender SmartScreen** is turned on.</span></span> <span data-ttu-id="6d201-120">Si no, entonces active la pantalla SmartScreen de Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="6d201-120">If not, then turn on Microsoft Defender SmartScreen.</span></span> <span data-ttu-id="6d201-121">El ejemplo de la siguiente captura de pantalla muestra que el navegador es administrado por la organización y que el SmartScreen de Microsoft Defender está activado.</span><span class="sxs-lookup"><span data-stu-id="6d201-121">The example in the following screenshot shows the browser is managed by the organization and that Microsoft Defender SmartScreen is turned on.</span></span>

   ![Active el Microsoft Edge PUA en Ajustes](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. <span data-ttu-id="6d201-123">En la sección de **Servicios**, utilice el botón que se muestra en la captura de pantalla anterior para activar la opción de **Bloquear aplicaciones potencialmente no deseadas**.</span><span class="sxs-lookup"><span data-stu-id="6d201-123">In the **Services** section, use the toggle shown in the preceding screenshot to turn on **Block potentially unwanted apps**.</span></span>

   > [!TIP]
   > <span data-ttu-id="6d201-124">Puede explorar con seguridad la función de bloqueo de URL de la protección PUA probándola en una de nuestras[páginas de demostración](https://demo.smartscreen.msft.net/) de SmartScreen de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="6d201-124">You can safely explore the URL-blocking feature of PUA protection by testing it out on one of our Windows Defender SmartScreen [demo pages](https://demo.smartscreen.msft.net/).</span></span>

<span data-ttu-id="6d201-125">Cuando Microsoft Edge detecte un PUA, verá un mensaje como el de la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="6d201-125">When Microsoft Edge detects a PUA, you will see a message like the one in the next screenshot.</span></span>

   ![Mensaje de advertencia de Microsoft Edge PUA](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### <a name="to-block-against-pua-associated-urls"></a><span data-ttu-id="6d201-127">Para crear un bloque en contra de los URLs asociados a la PUA</span><span class="sxs-lookup"><span data-stu-id="6d201-127">To block against PUA-associated URLs</span></span>

<span data-ttu-id="6d201-128">Después de activar la protección PUA en Microsoft Edge, Windows Defender SmartScreen lo protegerá de las URLs asociadas a PUA.</span><span class="sxs-lookup"><span data-stu-id="6d201-128">After you turn on PUA protection in Microsoft Edge, Windows Defender SmartScreen will protect you from PUA-associated URLs.</span></span>

<span data-ttu-id="6d201-129">Hay varias formas en que los administradores pueden configurar cómo Microsoft Edge y el SmartScreen de Windows Defender trabajan juntos para proteger a los usuarios de las URLs asociadas a la PUA.</span><span class="sxs-lookup"><span data-stu-id="6d201-129">There are several ways admins can configure how Microsoft Edge and Windows Defender SmartScreen work together to protect users from PUA-associated URLs.</span></span> <span data-ttu-id="6d201-130">Para más información, consulta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6d201-130">For more information, see:</span></span>

- [<span data-ttu-id="6d201-131">Configurar las opciones de directiva de Microsoft Edge en Windows</span><span class="sxs-lookup"><span data-stu-id="6d201-131">Configure Microsoft Edge policy settings on Windows</span></span>](./configure-microsoft-edge.md)
- [<span data-ttu-id="6d201-132">Configuración de SmartScreen</span><span class="sxs-lookup"><span data-stu-id="6d201-132">SmartScreen settings</span></span>](./microsoft-edge-policies.md#smartscreen-settings)
- [<span data-ttu-id="6d201-133">Directiva de SmartScreenPuaEnabled</span><span class="sxs-lookup"><span data-stu-id="6d201-133">SmartScreenPuaEnabled policy</span></span>](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [<span data-ttu-id="6d201-134">Configurar SmartScreen de Windows Defender</span><span class="sxs-lookup"><span data-stu-id="6d201-134">Configure Windows Defender SmartScreen</span></span>](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

<span data-ttu-id="6d201-135">Los administradores también pueden personalizar la lista de bloqueo de la Protección contra amenazas avanzada de Microsoft Defender (Microsoft Defender ATP).</span><span class="sxs-lookup"><span data-stu-id="6d201-135">Admins can also customize the Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP) block list.</span></span> <span data-ttu-id="6d201-136">Pueden utilizar el portal de Protección contra amenazas avanzada de Microsoft Defender para [crear y gestionar indicadores para IPs y URLs](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).</span><span class="sxs-lookup"><span data-stu-id="6d201-136">They can use the Microsoft Defender ATP portal to [create and manage indicators for IPs and URLs](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).</span></span>

## <a name="protect-against-pua-with-windows-defender-antivirus"></a><span data-ttu-id="6d201-137">Protección contra la PUA con el Antivirus Windows Defender</span><span class="sxs-lookup"><span data-stu-id="6d201-137">Protect against PUA with Windows Defender Antivirus</span></span>

<span data-ttu-id="6d201-138">El artículo [Detectar y bloquear aplicaciones potencialmente no deseadas](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) también describe cómo se puede configurar el Antivirus Windows Defender para activar la protección PUA.</span><span class="sxs-lookup"><span data-stu-id="6d201-138">The [Detect and block potentially unwanted applications](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) article also describes how you can configure Windows Defender Antivirus to enable PUA protection.</span></span> <span data-ttu-id="6d201-139">Puede configurar la protección usando cualquiera de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="6d201-139">You can configure protection using any of the following options:</span></span>

- [<span data-ttu-id="6d201-140">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="6d201-140">Microsoft Intune</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [<span data-ttu-id="6d201-141">Administrador de configuración de Microsoft Endpoint</span><span class="sxs-lookup"><span data-stu-id="6d201-141">Microsoft Endpoint Configuration Manager</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [<span data-ttu-id="6d201-142">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="6d201-142">Group Policy</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [<span data-ttu-id="6d201-143">Cmdlets de PowerShell</span><span class="sxs-lookup"><span data-stu-id="6d201-143">PowerShell cmdlets</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

<span data-ttu-id="6d201-144">Cuando Windows Defender detecta un archivo PUA en un punto de conexión, lo pone en cuarentena y lo notifica al usuario ([a menos que las notificaciones estén desactivadas](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) en el mismo formato que una detección de amenazas normal (con el prefacio de "PUA:".) Las amenazas detectadas también aparecen en la [lista de cuarentena de la aplicación de Seguridad de Windows](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).</span><span class="sxs-lookup"><span data-stu-id="6d201-144">When Windows Defender detects a PUA file on an endpoint it quarantines the file and notifies the user ([unless notifications are disabled](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) in the same format as a normal threat detection (prefaced with "PUA:".) Detected threats also appear in the [quarantine list in the Windows Security app](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).</span></span>

### <a name="pua-notifications-and-events"></a><span data-ttu-id="6d201-145">Notificaciones y eventos de PUA</span><span class="sxs-lookup"><span data-stu-id="6d201-145">PUA notifications and events</span></span>

<span data-ttu-id="6d201-146">Hay varias formas en que un administrador puede ver los eventos de PUA:</span><span class="sxs-lookup"><span data-stu-id="6d201-146">There are several ways an admin can see PUA events:</span></span>

- <span data-ttu-id="6d201-147">En el Visor de eventos de Windows, pero no en el Administrador de Configuración de Microsoft Endpoint o en Intune.</span><span class="sxs-lookup"><span data-stu-id="6d201-147">In the Windows Event Viewer, but not in Microsoft Endpoint Configuration Manager or Intune.</span></span>
- <span data-ttu-id="6d201-148">En un correo electrónico si las notificaciones de correo electrónico para las detecciones de la PUA están activadas.</span><span class="sxs-lookup"><span data-stu-id="6d201-148">In an email if email notifications for PUA detections is turned on.</span></span>
- <span data-ttu-id="6d201-149">En los registros de eventos del [Antivirus Windows Defender](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus), donde se registra un evento PUA bajo el ID de evento 1116 con el mensaje: "La plataforma antimalware detectó malware u otro software potencialmente no deseado".</span><span class="sxs-lookup"><span data-stu-id="6d201-149">In [Windows Defender Antivirus](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus) event logs, where a PUA event is recorded under event ID 1116 with the message: "The antimalware platform detected malware or other potentially unwanted software."</span></span>

> [!NOTE]
> <span data-ttu-id="6d201-150">Los usuarios verán que "\*.exe ha sido bloqueado como una aplicación potencialmente no deseada por la aplicación SmartScreen de Microsoft Defender".</span><span class="sxs-lookup"><span data-stu-id="6d201-150">Users will see "\*.exe has been blocked as a potentially unwanted app by Microsoft Defender SmartScreen".</span></span>

### <a name="allow-list-an-app"></a><span data-ttu-id="6d201-151">Habilitar una aplicación en la lista</span><span class="sxs-lookup"><span data-stu-id="6d201-151">Allow-list an app</span></span>

<span data-ttu-id="6d201-152">Al igual que Microsoft Edge, el Antivirus Windows Defender proporciona una forma de permitir archivos que se bloquean por error o que se necesitan para completar una tarea.</span><span class="sxs-lookup"><span data-stu-id="6d201-152">Like Microsoft Edge, Windows Defender Antivirus provides a way to allow files that are blocked by mistake or needed to complete a task.</span></span> <span data-ttu-id="6d201-153">Si esto sucede, puedes habilitar un archivo en la lista</span><span class="sxs-lookup"><span data-stu-id="6d201-153">If this happens you can allow-list a file.</span></span> <span data-ttu-id="6d201-154">Para obtener más información, consulte [Cómo configurar Endpoint Protection en el Administrador de configuración](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders) para aprender a excluir archivos o carpetas específicos.</span><span class="sxs-lookup"><span data-stu-id="6d201-154">For more information, see [How to Configure Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders) to learn how to exclude specific files or folders.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d201-155">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6d201-155">See also</span></span>

- [<span data-ttu-id="6d201-156">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="6d201-156">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6d201-157">Protección contra amenazas</span><span class="sxs-lookup"><span data-stu-id="6d201-157">Threat protection</span></span>](/windows/security/threat-protection/index)
- [<span data-ttu-id="6d201-158">Configurar la protección en tiempo real, heurística y de comportamiento</span><span class="sxs-lookup"><span data-stu-id="6d201-158">Configure behavioral, heuristic, and real-time protection</span></span>](/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [<span data-ttu-id="6d201-159">Protección de última generación</span><span class="sxs-lookup"><span data-stu-id="6d201-159">Next-generation protection</span></span>](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [<span data-ttu-id="6d201-160">Base de seguridad para el Microsoft Edge basado en el Chrome, versión 79</span><span class="sxs-lookup"><span data-stu-id="6d201-160">Security baseline for Chromium-based Microsoft Edge, version 79</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)