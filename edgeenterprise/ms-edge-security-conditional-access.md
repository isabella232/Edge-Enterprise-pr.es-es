---
title: Microsoft Edge y acceso condicional
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge y acceso condicional
ms.openlocfilehash: 27d93627f8a86ad821a00d6d78b7db352e9e557a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642856"
---
# <a name="microsoft-edge-and-conditional-access"></a><span data-ttu-id="a3ddd-103">Microsoft Edge y acceso condicional</span><span class="sxs-lookup"><span data-stu-id="a3ddd-103">Microsoft Edge and Conditional Access</span></span>
  
<span data-ttu-id="a3ddd-104">En el presente artículo, se describe cómo Microsoft Edge es compatible con el acceso condicional y cómo acceder a los recursos protegidos por el acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-104">This article describes how Microsoft Edge supports Conditional Access, and how to access resources protected by Conditional Access.</span></span>

> [!NOTE]
> <span data-ttu-id="a3ddd-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="a3ddd-106">Un aspecto clave de la seguridad en la nube es la identidad y el acceso cuando se trata de administrar los recursos de la nube.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-106">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="a3ddd-107">En un mundo orientado a los móviles y la nube, los usuarios pueden acceder a los recursos de la organización usando diversos dispositivos y aplicaciones desde cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-107">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="a3ddd-108">Como resultado de esto, no es suficiente centrarse en quién puede acceder a un recurso.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-108">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="a3ddd-109">También debes tener en cuenta el modo en que se accede a un recurso.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-109">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="a3ddd-110">El Acceso condicional de Azure Active Directory (Azure AD) te ayuda a dominar el equilibrio entre seguridad y productividad.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-110">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

## <a name="accessing-conditional-access-protected-resources-in-microsoft-edge"></a><span data-ttu-id="a3ddd-111">Obtención de acceso a recursos protegidos de acceso condicional en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a3ddd-111">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="a3ddd-112">Microsoft Edge admite el Acceso condicional de Azure AD de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-112">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="a3ddd-113">No hay necesidad de instalar una extensión diferente.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-113">There's no need to install a separate extension.</span></span> <span data-ttu-id="a3ddd-114">Cuando inicias sesión en un perfil de Microsoft Edge con credenciales Azure AD de empresa, Microsoft Edge permite un acceso sin problemas a los recursos de la nube de empresa protegidos mediante acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-114">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="a3ddd-115">En un dispositivo compatible, la identidad que acceda al recurso deberá coincidir con la identidad del perfil.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-115">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="a3ddd-116">Si no es así, verás un mensaje como el que se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-116">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="a3ddd-117">En el ejemplo de captura de pantalla, "testadmin@evostsoneboxtest.com" es la cuenta de inicio de sesión necesaria para obtener acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-117">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Mensaje de acceso condicional en el explorador](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="a3ddd-119">Para continuar, debes cambiar al perfil requerido (si tienes uno) o crear un perfil con la identidad coincidente.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-119">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="a3ddd-120">Para iniciar sesión y trabajar con su perfil, haz clic en la imagen de cuenta en la esquina superior derecha del explorador.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-120">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="a3ddd-121">Puedes usar el menú desplegable para:</span><span class="sxs-lookup"><span data-stu-id="a3ddd-121">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="a3ddd-122">Selecciona otro perfil.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-122">Select another profile.</span></span> <span data-ttu-id="a3ddd-123">Haz clic en el nombre de perfil.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-123">Click the profile name.</span></span>
- <span data-ttu-id="a3ddd-124">Crear un perfil.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-124">Create a profile.</span></span> <span data-ttu-id="a3ddd-125">Haz clic en **Agregar un perfil**.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-125">Click **Add a profile**.</span></span>
- <span data-ttu-id="a3ddd-126">Administra tus perfiles.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-126">Manage your profiles.</span></span> <span data-ttu-id="a3ddd-127">Haz clic en **Administrar configuración de perfil**.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-127">Click **Manage profile settings**.</span></span>

<span data-ttu-id="a3ddd-128">Esta compatibilidad está disponible en todas las plataformas, incluidas todas las versiones compatibles de Windows y macOS.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-128">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <a name="how-to-deploy-conditional-access-in-azure-active-directory"></a><span data-ttu-id="a3ddd-129">Cómo implementar el acceso condicional de Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a3ddd-129">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="a3ddd-130">[Implementar acceso condicional](/azure/active-directory/conditional-access/plan-conditional-access) proporciona una guía detallada para ayudar a implementar el acceso condicional en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a3ddd-130">[Deploy Conditional Access](/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3ddd-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3ddd-131">See also</span></span>

- [<span data-ttu-id="a3ddd-132">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a3ddd-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a3ddd-133">Vídeo: Seguridad, compatibilidad y capacidad de administración</span><span class="sxs-lookup"><span data-stu-id="a3ddd-133">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)