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
# <span data-ttu-id="8c350-103">Microsoft Edge y acceso condicional</span><span class="sxs-lookup"><span data-stu-id="8c350-103">Microsoft Edge and Conditional Access</span></span>
  
<span data-ttu-id="8c350-104">En el presente artículo, se describe cómo Microsoft Edge es compatible con el acceso condicional y cómo acceder a los recursos protegidos por el acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="8c350-104">This article describes how Microsoft Edge supports Conditional Access, and how to access resources protected by Conditional Access.</span></span>

> [!NOTE]
> <span data-ttu-id="8c350-105">Este artículo se aplica a Microsoft Edge, versión 77 o posterior.</span><span class="sxs-lookup"><span data-stu-id="8c350-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="8c350-106">Un aspecto clave de la seguridad en la nube es la identidad y el acceso cuando se trata de administrar los recursos de la nube.</span><span class="sxs-lookup"><span data-stu-id="8c350-106">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="8c350-107">En un mundo orientado a los móviles y la nube, los usuarios pueden acceder a los recursos de la organización usando diversos dispositivos y aplicaciones desde cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="8c350-107">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="8c350-108">Como resultado de esto, no es suficiente centrarse en quién puede acceder a un recurso.</span><span class="sxs-lookup"><span data-stu-id="8c350-108">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="8c350-109">También debes tener en cuenta el modo en que se accede a un recurso.</span><span class="sxs-lookup"><span data-stu-id="8c350-109">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="8c350-110">El Acceso condicional de Azure Active Directory (Azure AD) te ayuda a dominar el equilibrio entre seguridad y productividad.</span><span class="sxs-lookup"><span data-stu-id="8c350-110">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

## <span data-ttu-id="8c350-111">Obtención de acceso a recursos protegidos de acceso condicional en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8c350-111">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="8c350-112">Microsoft Edge admite el Acceso condicional de Azure AD de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="8c350-112">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="8c350-113">No hay necesidad de instalar una extensión diferente.</span><span class="sxs-lookup"><span data-stu-id="8c350-113">There's no need to install a separate extension.</span></span> <span data-ttu-id="8c350-114">Cuando inicias sesión en un perfil de Microsoft Edge con credenciales Azure AD de empresa, Microsoft Edge permite un acceso sin problemas a los recursos de la nube de empresa protegidos mediante acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="8c350-114">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="8c350-115">En un dispositivo compatible, la identidad que acceda al recurso deberá coincidir con la identidad del perfil.</span><span class="sxs-lookup"><span data-stu-id="8c350-115">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="8c350-116">Si no es así, verás un mensaje como el que se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8c350-116">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="8c350-117">En el ejemplo de captura de pantalla, "testadmin@evostsoneboxtest.com" es la cuenta de inicio de sesión necesaria para obtener acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="8c350-117">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Mensaje de acceso condicional en el explorador](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="8c350-119">Para continuar, debes cambiar al perfil requerido (si tienes uno) o crear un perfil con la identidad coincidente.</span><span class="sxs-lookup"><span data-stu-id="8c350-119">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="8c350-120">Para iniciar sesión y trabajar con su perfil, haz clic en la imagen de cuenta en la esquina superior derecha del explorador.</span><span class="sxs-lookup"><span data-stu-id="8c350-120">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="8c350-121">Puedes usar el menú desplegable para:</span><span class="sxs-lookup"><span data-stu-id="8c350-121">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="8c350-122">Selecciona otro perfil.</span><span class="sxs-lookup"><span data-stu-id="8c350-122">Select another profile.</span></span> <span data-ttu-id="8c350-123">Haz clic en el nombre de perfil.</span><span class="sxs-lookup"><span data-stu-id="8c350-123">Click the profile name.</span></span>
- <span data-ttu-id="8c350-124">Crear un perfil.</span><span class="sxs-lookup"><span data-stu-id="8c350-124">Create a profile.</span></span> <span data-ttu-id="8c350-125">Haz clic en **Agregar un perfil**.</span><span class="sxs-lookup"><span data-stu-id="8c350-125">Click **Add a profile**.</span></span>
- <span data-ttu-id="8c350-126">Administra tus perfiles.</span><span class="sxs-lookup"><span data-stu-id="8c350-126">Manage your profiles.</span></span> <span data-ttu-id="8c350-127">Haz clic en **Administrar configuración de perfil**.</span><span class="sxs-lookup"><span data-stu-id="8c350-127">Click **Manage profile settings**.</span></span>

<span data-ttu-id="8c350-128">Esta compatibilidad está disponible en todas las plataformas, incluidas todas las versiones compatibles de Windows y macOS.</span><span class="sxs-lookup"><span data-stu-id="8c350-128">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <span data-ttu-id="8c350-129">Cómo implementar el acceso condicional de Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8c350-129">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="8c350-130">[Implementar acceso condicional](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) proporciona una guía detallada para ayudar a implementar el acceso condicional en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8c350-130">[Deploy Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <span data-ttu-id="8c350-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8c350-131">See also</span></span>

- [<span data-ttu-id="8c350-132">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c350-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="8c350-133">Vídeo: Seguridad, compatibilidad y capacidad de administración</span><span class="sxs-lookup"><span data-stu-id="8c350-133">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)
