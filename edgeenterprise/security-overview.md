---
title: Introducción a la seguridad de Microsoft Edge
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 04/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Introducción a la implementación de la seguridad de Microsoft Edge
ms.openlocfilehash: f22f2dcbace00cd535d201950c2af488c708525b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981226"
---
# <span data-ttu-id="8238d-103">Introducción a la seguridad de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8238d-103">Overview of Microsoft Edge security</span></span>
  
<span data-ttu-id="8238d-104">Los administradores de TI de la empresa suelen enfrentar una gran cantidad de desafíos de seguridad existentes y emergentes, a la vez que protegen los dispositivos y la red corporativa frente a ataques malintencionados y evitan los accesos no autorizados y las pérdidas de datos corporativos.</span><span class="sxs-lookup"><span data-stu-id="8238d-104">IT admins in the enterprise are constantly facing a myriad of existing and emerging security challenges while protecting the corporate network and devices from malicious attacks and preventing unauthorized access and leaks of corporate data.</span></span> <span data-ttu-id="8238d-105">Microsoft Edge proporciona varias capacidades únicas creadas nativamente que ayudan a afrontar estos desafíos.</span><span class="sxs-lookup"><span data-stu-id="8238d-105">Microsoft Edge provides several natively built, unique capabilities that help address these challenges.</span></span>

> [!NOTE]
> <span data-ttu-id="8238d-106">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="8238d-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="8238d-107">Acceso condicional</span><span class="sxs-lookup"><span data-stu-id="8238d-107">Conditional Access</span></span>

<span data-ttu-id="8238d-108">Un aspecto clave de la seguridad en la nube es la identidad y el acceso cuando se trata de administrar los recursos de la nube.</span><span class="sxs-lookup"><span data-stu-id="8238d-108">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="8238d-109">En un mundo orientado a los móviles y la nube, los usuarios pueden acceder a los recursos de la organización usando diversos dispositivos y aplicaciones desde cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="8238d-109">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="8238d-110">Como resultado de esto, no es suficiente centrarse en quién puede acceder a un recurso.</span><span class="sxs-lookup"><span data-stu-id="8238d-110">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="8238d-111">También debes tener en cuenta el modo en que se accede a un recurso.</span><span class="sxs-lookup"><span data-stu-id="8238d-111">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="8238d-112">El Acceso condicional de Azure Active Directory (Azure AD) te ayuda a dominar el equilibrio entre seguridad y productividad.</span><span class="sxs-lookup"><span data-stu-id="8238d-112">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

### <span data-ttu-id="8238d-113">Obtención de acceso a recursos protegidos de acceso condicional en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8238d-113">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="8238d-114">Microsoft Edge admite el Acceso condicional de Azure AD de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="8238d-114">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="8238d-115">No hay necesidad de instalar una extensión diferente.</span><span class="sxs-lookup"><span data-stu-id="8238d-115">There's no need to install a separate extension.</span></span> <span data-ttu-id="8238d-116">Cuando inicias sesión en un perfil de Microsoft Edge con credenciales Azure AD de empresa, Microsoft Edge permite un acceso sin problemas a los recursos de la nube de empresa protegidos mediante acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="8238d-116">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="8238d-117">En un dispositivo compatible, la identidad que acceda al recurso deberá coincidir con la identidad del perfil.</span><span class="sxs-lookup"><span data-stu-id="8238d-117">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="8238d-118">Si no es así, verás un mensaje como el que se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8238d-118">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="8238d-119">En el ejemplo de captura de pantalla, "testadmin@evostsoneboxtest.com" es la cuenta de inicio de sesión necesaria para obtener acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="8238d-119">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Mensaje de acceso condicional en el explorador](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="8238d-121">Para continuar, debes cambiar al perfil requerido (si tienes uno) o crear un perfil con la identidad coincidente.</span><span class="sxs-lookup"><span data-stu-id="8238d-121">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="8238d-122">Para iniciar sesión y trabajar con su perfil, haz clic en la imagen de cuenta en la esquina superior derecha del explorador.</span><span class="sxs-lookup"><span data-stu-id="8238d-122">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="8238d-123">Puedes usar el menú desplegable para:</span><span class="sxs-lookup"><span data-stu-id="8238d-123">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="8238d-124">Selecciona otro perfil.</span><span class="sxs-lookup"><span data-stu-id="8238d-124">Select another profile.</span></span> <span data-ttu-id="8238d-125">Haz clic en el nombre de perfil.</span><span class="sxs-lookup"><span data-stu-id="8238d-125">Click the profile name.</span></span>
- <span data-ttu-id="8238d-126">Crear un perfil.</span><span class="sxs-lookup"><span data-stu-id="8238d-126">Create a profile.</span></span> <span data-ttu-id="8238d-127">Haz clic en **Agregar un perfil**.</span><span class="sxs-lookup"><span data-stu-id="8238d-127">Click **Add a profile**.</span></span>
- <span data-ttu-id="8238d-128">Administra tus perfiles.</span><span class="sxs-lookup"><span data-stu-id="8238d-128">Manage your profiles.</span></span> <span data-ttu-id="8238d-129">Haz clic en **Administrar configuración de perfil**.</span><span class="sxs-lookup"><span data-stu-id="8238d-129">Click **Manage profile settings**.</span></span>

<span data-ttu-id="8238d-130">Esta compatibilidad está disponible en todas las plataformas, incluidas todas las versiones compatibles de Windows y macOS.</span><span class="sxs-lookup"><span data-stu-id="8238d-130">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <span data-ttu-id="8238d-131">Cómo implementar el acceso condicional de Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8238d-131">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="8238d-132">[Implementar acceso condicional](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) proporciona una guía detallada para ayudar a implementar el acceso condicional en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8238d-132">[Deploy Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <span data-ttu-id="8238d-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8238d-133">See also</span></span>

- [<span data-ttu-id="8238d-134">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="8238d-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="8238d-135">Vídeo: Seguridad, compatibilidad y capacidad de administración</span><span class="sxs-lookup"><span data-stu-id="8238d-135">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)
