---
title: Microsoft Edge compatible para la Protección de la información de Windows
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 04/24/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge compatible para la Protección de la información de Windows
ms.openlocfilehash: 4ec48d258deb1cf6d4436716f14aa2561cee2a50
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981227"
---
# <span data-ttu-id="d2701-103">Microsoft Edge compatible para la Protección de la información de Windows (WIP)</span><span class="sxs-lookup"><span data-stu-id="d2701-103">Microsoft Edge support for Windows Information Protection (WIP)</span></span>

<span data-ttu-id="d2701-104">Este artículo describe cómo Microsoft Edge es compatible con la protección de información de Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="d2701-104">This article describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span>

> [!NOTE]
> <span data-ttu-id="d2701-105">Esto se aplica para la versión 81 de Microsoft Edge o posterior</span><span class="sxs-lookup"><span data-stu-id="d2701-105">This applies to Microsoft Edge version 81 or later.</span></span>

## <span data-ttu-id="d2701-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="d2701-106">Overview</span></span>

<span data-ttu-id="d2701-107">La Protección de la información de Windows (WIP) es una característica de Windows 10 que ayuda a proteger los datos de la empresa contra la divulgación no autorizada o accidental.</span><span class="sxs-lookup"><span data-stu-id="d2701-107">Windows Information Protection (WIP) is a Windows 10 feature that helps protect enterprise data from unauthorized or accidental disclosure.</span></span> <span data-ttu-id="d2701-108">Con el aumento del trabajo a distancia, hay un mayor riesgo de compartir datos corporativos fuera del lugar de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d2701-108">With the rise of remote work, there's an increased risk of sharing corporate data outside the workplace.</span></span> <span data-ttu-id="d2701-109">Este riesgo aumenta cuando las actividades personales y laborales se realizan en dispositivos corporativos.</span><span class="sxs-lookup"><span data-stu-id="d2701-109">This risk increases when personal activities and work activities occur on corporate devices.</span></span>

<span data-ttu-id="d2701-110">Microsoft Edge es compatible con WIP para ayudar a proteger el contenido en un entorno web en el que los usuarios suelen compartir y distribuir contenido.</span><span class="sxs-lookup"><span data-stu-id="d2701-110">Microsoft Edge supports WIP to help protect content in a web environment where users often share and distribute content.</span></span>

### <span data-ttu-id="d2701-111">Requisitos del sistema</span><span class="sxs-lookup"><span data-stu-id="d2701-111">System requirements</span></span>

<span data-ttu-id="d2701-112">Los siguientes requisitos se aplican a los dispositivos que utilizan WIP en la empresa:</span><span class="sxs-lookup"><span data-stu-id="d2701-112">The follow requirements apply to devices using WIP in the enterprise:</span></span>

- <span data-ttu-id="d2701-113">Windows10, versión 1607 o posterior</span><span class="sxs-lookup"><span data-stu-id="d2701-113">Windows 10, version 1607 or later</span></span>
- <span data-ttu-id="d2701-114">Sólo SKUs de clientes de Windows</span><span class="sxs-lookup"><span data-stu-id="d2701-114">Only Windows client SKUs</span></span>
- <span data-ttu-id="d2701-115">Una de las soluciones de administración descritas en [requisitos previos de WIP](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="d2701-115">One of the management solutions described in [WIP prerequisites](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)</span></span>

### <span data-ttu-id="d2701-116">Beneficios de la Protección de la Información de Windows</span><span class="sxs-lookup"><span data-stu-id="d2701-116">Windows Information Protection benefits</span></span>

<span data-ttu-id="d2701-117">El WIP proporciona los siguientes beneficios:</span><span class="sxs-lookup"><span data-stu-id="d2701-117">WIP provides the following benefits:</span></span>

- <span data-ttu-id="d2701-118">Separación obvia entre los datos personales y corporativos, sin necesidad de que los empleados cambien de entornos o aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d2701-118">Obvious separation between personal and corporate data, without requiring employees to switch environments or apps.</span></span>
- <span data-ttu-id="d2701-119">Protección de datos adicional para aplicaciones de línea de negocio sin necesidad de actualizar las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d2701-119">Additional data protection for existing line-of-business apps without a need to update the apps.</span></span>
- <span data-ttu-id="d2701-120">La capacidad de borrar a distancia los datos corporativos de los dispositivos inscritos en la administración de dispositivos móviles de Microsoft Intune (MDM) sin afectar a los datos personales.</span><span class="sxs-lookup"><span data-stu-id="d2701-120">The ability to remote wipes corporate data from Intune Mobile Device Management (MDM) enrolled devices while leaving personal data unaffected.</span></span> 
- <span data-ttu-id="d2701-121">Informes de auditoría para el seguimiento de los problemas y para la adopción de medidas correctivas, como la capacitación de los usuarios en materia de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="d2701-121">Audit reports for tracking issues and for remedial actions such as compliance training for users.</span></span>
- <span data-ttu-id="d2701-122">Integración con su sistema de gestión existente para configurar, desplegar y gestionar WIP.</span><span class="sxs-lookup"><span data-stu-id="d2701-122">Integration with your existing management system to configure, deploy, and manage WIP.</span></span> <span data-ttu-id="d2701-123">Algunos ejemplos son Microsoft Intune, el Administrador de configuración de Microsoft Endpoint, o su actual sistema de administración de dispositivos móviles (MDM).</span><span class="sxs-lookup"><span data-stu-id="d2701-123">Some examples are Microsoft Intune, Microsoft Endpoint Configuration Manager, or your current mobile device management (MDM) system.</span></span>

## <span data-ttu-id="d2701-124">Modos de protección y directiva de WIP</span><span class="sxs-lookup"><span data-stu-id="d2701-124">WIP policy and protection modes</span></span>

<span data-ttu-id="d2701-125">Mediante las directivas, puede configurar los cuatro modos de protección descritos en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d2701-125">Using policies, you can configure the four protection modes described in the following table.</span></span> <span data-ttu-id="d2701-126">Para más información, consulte[modos de protección WIP](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).</span><span class="sxs-lookup"><span data-stu-id="d2701-126">For more information, see [WIP-protection modes](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).</span></span>

| <span data-ttu-id="d2701-127">Modo</span><span class="sxs-lookup"><span data-stu-id="d2701-127">Mode</span></span> | <span data-ttu-id="d2701-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2701-128">Description</span></span> |
|------|-------------|
| <span data-ttu-id="d2701-129">Bloquear</span><span class="sxs-lookup"><span data-stu-id="d2701-129">Block</span></span> | <span data-ttu-id="d2701-130">WIP busca prácticas de uso compartido inapropiado de datos y evita que el empleado complete la acción.</span><span class="sxs-lookup"><span data-stu-id="d2701-130">WIP looks for inappropriate data sharing practices and stops the employee from completing the action.</span></span> <span data-ttu-id="d2701-131">Esta búsqueda puede incluir el uso compartido de datos de la empresa con aplicaciones no protegidas por la empresa, además del uso compartido de datos de la empresa entre aplicaciones o el intento de uso compartido fuera de la red de la organización.</span><span class="sxs-lookup"><span data-stu-id="d2701-131">This search can include sharing enterprise data to non-enterprise-protected apps in addition to sharing enterprise data between apps or attempting to share outside of your organization's network.</span></span> |
| <span data-ttu-id="d2701-132">Permitir invalidaciones</span><span class="sxs-lookup"><span data-stu-id="d2701-132">Allow Overrides</span></span> | <span data-ttu-id="d2701-133">WIP busca usos compartidos inapropiados de datos y advierte a los empleados si realizan acciones potencialmente no seguras.</span><span class="sxs-lookup"><span data-stu-id="d2701-133">WIP looks for inappropriate data sharing, warning employees if they do something deemed potentially unsafe.</span></span> <span data-ttu-id="d2701-134">Sin embargo, este modo de administración permite a los empleados invalidar la directiva y compartir los datos, registrando la acción en el registro de auditoría.</span><span class="sxs-lookup"><span data-stu-id="d2701-134">However, this management mode lets the employee override the policy and share the data, logging the action to your audit log.</span></span> |
| <span data-ttu-id="d2701-135">Silencio</span><span class="sxs-lookup"><span data-stu-id="d2701-135">Silent</span></span> | <span data-ttu-id="d2701-136">WIP se ejecuta de forma silenciosa, registra el intercambio de datos inapropiados, sin detener nada que hubiera sido requerido para la interacción del empleado en el modo Permitir anulaciones.</span><span class="sxs-lookup"><span data-stu-id="d2701-136">WIP runs silently, logging inappropriate data sharing, without stopping anything that would have been prompted for employee interaction while in Allow Overrides mode.</span></span> <span data-ttu-id="d2701-137">Las acciones no autorizadas siguen detenidas, como, por ejemplo, el intento de acceso inapropiado de aplicaciones a un recurso de red o datos protegidos por WIP.</span><span class="sxs-lookup"><span data-stu-id="d2701-137">Unallowed actions, like apps inappropriately trying to access a network resource or WIP-protected data, are still stopped.</span></span> |
| <span data-ttu-id="d2701-138">Desactivado</span><span class="sxs-lookup"><span data-stu-id="d2701-138">Off</span></span> | <span data-ttu-id="d2701-139">WIP está desactivo y no ayuda a proteger ni auditar los datos.</span><span class="sxs-lookup"><span data-stu-id="d2701-139">WIP is turned off and doesn't help to protect or audit your data.</span></span> <span data-ttu-id="d2701-140">Tras desactivar WIP, se intentan descifrar los archivos etiquetados de WIP en las unidades conectadas localmente.</span><span class="sxs-lookup"><span data-stu-id="d2701-140">After you turn off WIP, an attempt is made to decrypt any WIP-tagged files on the locally attached drives.</span></span> <span data-ttu-id="d2701-141">Tenga en cuenta que la información previa de directiva y descifrado no se vuelve a aplicar automáticamente si vuelve a activar la protección WIP.</span><span class="sxs-lookup"><span data-stu-id="d2701-141">Your previous decryption and policy info isn't automatically reapplied if you turn WIP protection back on.</span></span>
 |

## <span data-ttu-id="d2701-142">Las características WIP compatibles en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d2701-142">WIP features supported in Microsoft Edge</span></span>

<span data-ttu-id="d2701-143">A partir de la versión 81 de Microsoft Edge, se admiten las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="d2701-143">Starting with Microsoft Edge version 81, the following features are supported:</span></span>

- <span data-ttu-id="d2701-144">Los sitios de trabajo se indicarán con un icono de maletín en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d2701-144">Work sites will be indicated by a briefcase icon on the address bar.</span></span>  
- <span data-ttu-id="d2701-145">Los archivos descargados de un lugar de trabajo se encriptan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d2701-145">Files downloaded from a work location are automatically encrypted.</span></span>
- <span data-ttu-id="d2701-146">Silenciar/Bloquear/Anular la carga de archivos de trabajo en lugares que no son de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d2701-146">Silent/Block/Override enforcement for work file uploads to non-work locations.</span></span>  
- <span data-ttu-id="d2701-147">Silenciar/Bloquear/Anular las acciones de arrastrar y soltar archivos.</span><span class="sxs-lookup"><span data-stu-id="d2701-147">Silent/Block/Override enforcement for file Drag & Drop actions.</span></span>
- <span data-ttu-id="d2701-148">Silenciar/Bloquear/Anular el cumplimiento de las acciones del Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="d2701-148">Silent/Block/Override enforcement for Clipboard actions.</span></span>
- <span data-ttu-id="d2701-149">Navegar a lugares de trabajo desde perfiles no laborales se redirige automáticamente al Perfil de trabajo (asociado con Azure AD Identity.)</span><span class="sxs-lookup"><span data-stu-id="d2701-149">Browsing to work locations from non-work profiles automatically redirects to the Work Profile (associated with the Azure AD Identity.)</span></span>
- <span data-ttu-id="d2701-150">El modo IE es compatible con la funcionalidad WIP completa.</span><span class="sxs-lookup"><span data-stu-id="d2701-150">IE Mode supports full WIP functionality.</span></span>

## <span data-ttu-id="d2701-151">Trabajando con WIP en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d2701-151">Working with WIP in Microsoft Edge</span></span>

<span data-ttu-id="d2701-152">Después de que se habilite el soporte WIP para Microsoft Edge, los usuarios verán cuando se acceda a la información relacionada con el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d2701-152">After WIP support is enabled for Microsoft Edge, users will see when work-related information is accessed.</span></span> <span data-ttu-id="d2701-153">La siguiente captura de pantalla muestra el icono de un maletín en la barra de direcciones, lo que indica que se accede a la información relacionada con el trabajo a través del navegador.</span><span class="sxs-lookup"><span data-stu-id="d2701-153">The next screenshot shows the briefcase icon in the address bar, indicating that work-related information is accessed via the browser.</span></span>

 ![Indicador de la barra de direcciones para los sitios marcados como "trabajo".](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-notify.png)

<span data-ttu-id="d2701-155">Microsoft Edge ofrece a los usuarios la posibilidad de compartir contenido protegido en un sitio web no aprobado.</span><span class="sxs-lookup"><span data-stu-id="d2701-155">Microsoft Edge gives users the ability to share protected content in an unapproved website.</span></span> <span data-ttu-id="d2701-156">La siguiente captura de pantalla muestra el aviso de Microsoft Edge que permite a un usuario utilizar contenido protegido en un sitio web no aprobado.</span><span class="sxs-lookup"><span data-stu-id="d2701-156">The next screenshot shows the Microsoft Edge prompt that allows a user to use protected content in an unapproved website.</span></span>

 ![Solicitud de anulación de contenido protegido](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-override.png)

## <span data-ttu-id="d2701-158">Configurar las directivas compatibles con WIP</span><span class="sxs-lookup"><span data-stu-id="d2701-158">Configure policies to support WIP</span></span>

<span data-ttu-id="d2701-159">El uso de WIP con Microsoft Edge requiere la presencia de un perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d2701-159">Using WIP with Microsoft Edge requires the presence of a work profile.</span></span>

### <span data-ttu-id="d2701-160">Asegure la presencia de un perfil de trabajo</span><span class="sxs-lookup"><span data-stu-id="d2701-160">Ensure the presence of a work profile</span></span>

<span data-ttu-id="d2701-161">En equipos híbridos Unidos, Microsoft Edge inicia sesión automáticamente en la cuenta Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="d2701-161">On hybrid joined machines, Microsoft Edge is automatically signed in with the Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="d2701-162">Para asegurarse de que los usuarios no eliminen este perfil necesario para la WIP, configure la siguiente directiva:</span><span class="sxs-lookup"><span data-stu-id="d2701-162">To make sure that users don't remove this profile, which is needed for WIP, configure the following policy:</span></span>

- [<span data-ttu-id="d2701-163">NonRemovableProfileEnabled</span><span class="sxs-lookup"><span data-stu-id="d2701-163">NonRemovableProfileEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#nonremovableprofileenabled)

> [!NOTE]
> <span data-ttu-id="d2701-164">Si su entorno no es un híbrido unido, puede unirse a un híbrido usando estas instrucciones: [Planifique la implementación de su híbrido Azure Active Directory](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-plan).</span><span class="sxs-lookup"><span data-stu-id="d2701-164">If your environment isn't hybrid joined, you can hybrid join using these instructions: [Plan your hybrid Azure Active Directory join implementation](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-plan).</span></span>

<span data-ttu-id="d2701-165">Si la unión híbrida no es una opción, puede usar cuentas de Active Directory locales para permitir que Microsoft Edge cree automáticamente un perfil de trabajo especial con las cuentas de dominio de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="d2701-165">If hybrid joining isn't an option, you can use on-prem Active Directory accounts to allow Microsoft Edge to auto create a special work profile with the users' domain accounts.</span></span> <span data-ttu-id="d2701-166">Tenga en cuenta que las cuentas locales pueden no recibir todas las funciones de Azure AD, como la sincronización de la nube, Office NTP y muchas más.</span><span class="sxs-lookup"><span data-stu-id="d2701-166">Note that on-premises accounts may not receive all of Azure AD's features, such as cloud sync, Office NTP, and so on.)</span></span>

#### <span data-ttu-id="d2701-167">Cuentas de Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="d2701-167">Active Directory (AD) accounts</span></span>

<span data-ttu-id="d2701-168">Para las cuentas de AD, debes configurar la siguiente política para que Microsoft Edge cree automáticamente un perfil de trabajo especial.</span><span class="sxs-lookup"><span data-stu-id="d2701-168">For AD accounts, you must configure the following policy to have the Microsoft Edge auto create a special work profile.</span></span>

- [<span data-ttu-id="d2701-169">ConfigureOnPremisesAccountAutoSignIn</span><span class="sxs-lookup"><span data-stu-id="d2701-169">ConfigureOnPremisesAccountAutoSignIn</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)

### <span data-ttu-id="d2701-170">Directivas de Windows10 para WIP</span><span class="sxs-lookup"><span data-stu-id="d2701-170">Windows policies for WIP</span></span>

<span data-ttu-id="d2701-171">Puede configurar WIP usando las directivas de Windows.</span><span class="sxs-lookup"><span data-stu-id="d2701-171">You can configure WIP using Windows policies.</span></span> <span data-ttu-id="d2701-172">Para más información, consulte[Crear y desplegar directivas WIP usando Microsoft Intune ](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)</span><span class="sxs-lookup"><span data-stu-id="d2701-172">For more information, see [Create and deploy WIP policies using Microsoft Intune](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)</span></span>

## <span data-ttu-id="d2701-173">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="d2701-173">Frequently Asked Questions</span></span>

### <span data-ttu-id="d2701-174">¿Cómo puedo resolver el código de error -2147024540?</span><span class="sxs-lookup"><span data-stu-id="d2701-174">How do I resolve Error Code -2147024540?</span></span>

<span data-ttu-id="d2701-175">Este código de error corresponde al siguiente error de Protección de información de Windows:\* ERROR_EDP_POLICY_DENIES_OPERATION: La operación solicitada fue bloqueada por la política de Protección de información de Windows. Para obtener más información, póngase en contacto con el administrador del sistema.\*</span><span class="sxs-lookup"><span data-stu-id="d2701-175">This error code corresponds to the following Windows Information Protection error: *ERROR_EDP_POLICY_DENIES_OPERATION: The requested operation was blocked by Windows Information Protection policy. For more information, contact your system administrator.*</span></span>

<span data-ttu-id="d2701-176">Microsoft Edge muestra este error cuando la organización ha habilitado Windows Information Protection (WIP) para permitir que solo los usuarios con solicitudes aprobadas puedan tener acceso a los recursos corporativos.</span><span class="sxs-lookup"><span data-stu-id="d2701-176">Microsoft Edge shows this error when the organization has enabled Windows Information Protection (WIP) to only allow users with approved applications to access corporate resources.</span></span> <span data-ttu-id="d2701-177">En este caso, dado que Microsoft Edge no está en la lista de aplicaciones aprobadas, el administrador tendrá que actualizar las directivas de WIP para conceder acceso a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d2701-177">In this case because Microsoft Edge isn't on the approved applications list, the admin will have to update the WIP policies to grant access to Microsoft Edge.</span></span>

<span data-ttu-id="d2701-178">La siguiente captura de pantalla muestra cómo se usa Microsoft Intune para agregar Microsoft Edge como aplicación permitida para WIP.</span><span class="sxs-lookup"><span data-stu-id="d2701-178">The following screenshot shows how the Microsoft Intune is used to add Microsoft Edge as an allowed app for WIP.</span></span>

 ![Cuadro de diálogo de Intune para agregar Microsoft Edge como aplicación para WIP](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-exemption.png)

<span data-ttu-id="d2701-180">Si no usa Microsoft Intune, descargue y aplique la actualización de directiva en el archivo [Directiva de WIP Enterprise AppLocker](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip).</span><span class="sxs-lookup"><span data-stu-id="d2701-180">If you're not using Microsoft Intune, download and apply the policy update in the [WIP Enterprise AppLocker Policy](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip) file.</span></span>

## <span data-ttu-id="d2701-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d2701-181">See also</span></span>

- [<span data-ttu-id="d2701-182">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="d2701-182">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise) 
- [<span data-ttu-id="d2701-183">Proteger los datos de la empresa mediante Protección de información de Windows</span><span class="sxs-lookup"><span data-stu-id="d2701-183">Protect enterprise data using Windows Information Protection</span></span>](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
