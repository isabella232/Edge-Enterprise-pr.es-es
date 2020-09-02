---
title: Descargas de contenido mixto en Microsoft Edge
ms.author: kele
author: dan-wesley
manager: srugh
ms.date: 04/30/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Descargas de contenido mixto en Microsoft Edge
ms.openlocfilehash: 57da17a8684b97aad88e7837ff9d070f6862357b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981131"
---
# <span data-ttu-id="85e5f-103">Obtén más información sobre las descargas de contenido mixto en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="85e5f-103">Learn about Microsoft Edge and mixed content downloads</span></span>

<span data-ttu-id="85e5f-104">En este artículo se explican las descargas de contenido mixto y cómo Microsoft Edge las maneja.</span><span class="sxs-lookup"><span data-stu-id="85e5f-104">This article explains mixed content downloads and how Microsoft Edge handles them.</span></span>

>[!NOTE]
><span data-ttu-id="85e5f-105">Este artículo se aplica a Microsoft Edge, versión 85 o posterior.</span><span class="sxs-lookup"><span data-stu-id="85e5f-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="85e5f-106">¿Qué son las descargas de contenido mixto?</span><span class="sxs-lookup"><span data-stu-id="85e5f-106">What are mixed content downloads?</span></span>

<span data-ttu-id="85e5f-107">Se produce una descarga de contenido mixto cuando inicias una descarga desde una página HTML que se cargó a través de una conexión HTTPS segura, pero se produce una de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="85e5f-107">A mixed content download happens when you start a download from an HTML page that was loaded over a secure HTTPS connection, but one of the following conditions exists:</span></span>

- <span data-ttu-id="85e5f-108">Una o más redirecciones de la ubicación de descarga se ha cargado mediante una conexión HTTP no segura.</span><span class="sxs-lookup"><span data-stu-id="85e5f-108">One or more of the download location's redirects was loaded over an insecure HTTP connection.</span></span>
- <span data-ttu-id="85e5f-109">La ubicación de descarga final se ha cargado mediante una conexión HTTP no segura.</span><span class="sxs-lookup"><span data-stu-id="85e5f-109">The final download location was loaded over an insecure HTTP connection.</span></span>

<span data-ttu-id="85e5f-110">En cualquier de los dos escenarios se produce la descarga de contenido mixto porque la solicitud se realizó mediante una conexión de HTTPS segura y el contenido, tanto HTTP como HTTPS, se invoca cuando llega al destino final de descarga.</span><span class="sxs-lookup"><span data-stu-id="85e5f-110">Either scenario is a mixed content because the request was made using secure HTTPS and both HTTP and HTTPS content are involved in reaching the final download destination.</span></span> <span data-ttu-id="85e5f-111">Los exploradores modernos muestran advertencias sobre este tipo de contenido para indicar al usuario que esa descarga podría transferirse de forma insegura, aunque la página original a la que se accedió era segura.</span><span class="sxs-lookup"><span data-stu-id="85e5f-111">Modern browsers display warnings about this type of content to indicate to the user that this download may be transferred insecurely even though the original page accessed was secure.</span></span>

## <span data-ttu-id="85e5f-112">Advertencias de descarga y opciones de usuario</span><span class="sxs-lookup"><span data-stu-id="85e5f-112">Download warnings and user options</span></span>

<span data-ttu-id="85e5f-113">La advertencia de descarga garantiza que los usuarios sepan que el archivo que se está descargando podría ser leído por atacantes malintencionados en su red.</span><span class="sxs-lookup"><span data-stu-id="85e5f-113">The download warning ensures that users know that the file they're downloading could be read by malicious attackers on their network.</span></span> <span data-ttu-id="85e5f-114">Esta advertencia permite a los usuarios tomar decisiones fundamentadas sobre si se debe descargar el archivo.</span><span class="sxs-lookup"><span data-stu-id="85e5f-114">This warning lets a user make an informed decision on whether to download the file.</span></span>

<span data-ttu-id="85e5f-115">En Microsoft Edge, las descargas de contenido mixto se bloquearán, pero los usuarios podrán invalidar el bloqueo y descargar el archivo si lo desean.</span><span class="sxs-lookup"><span data-stu-id="85e5f-115">In Microsoft Edge, mixed content downloads will be blocked but users can override and download the file if they want to.</span></span> <span data-ttu-id="85e5f-116">Microsoft Edge planea empezar a bloquear la descarga de archivos ejecutables de contenido mixto desde la versión 85 de Microsoft Edge. Además, bloqueará diferentes tipos de archivo en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="85e5f-116">Microsoft Edge plans on starting to block mixed content executable file downloads starting with Microsoft Edge version 85 and will block different filetypes in future releases.</span></span>

> [!NOTE]
> <span data-ttu-id="85e5f-117">La implementación de esta característica está sujeta a cambios en función de la programación de lanzamiento y los comentarios de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="85e5f-117">Deployment of this feature is subject to change based on release schedule and user feedback.</span></span>

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

<span data-ttu-id="85e5f-118">En el estante de descarga, el mensaje de advertencia de bloqueo es similar al ejemplo en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="85e5f-118">In the download shelf, the block warning message looks like the example in the next screenshot.</span></span>

 ![Advertencia de contenido mixto en la bandeja de descarga](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

<span data-ttu-id="85e5f-120">En la página de descarga, la advertencia de bloqueo es similar al ejemplo en la siguiente captura de pantalla:</span><span class="sxs-lookup"><span data-stu-id="85e5f-120">On the download page, the block warning looks like the following screenshot example:</span></span>

 ![Aviso de invalidación de bloqueo de contenido mixto](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

<span data-ttu-id="85e5f-122">Si el usuario decide mantener la descarga, se le pedirá que confirme la acción.</span><span class="sxs-lookup"><span data-stu-id="85e5f-122">If a user decides to keep the download, they are prompted to confirm their action.</span></span> <span data-ttu-id="85e5f-123">La siguiente captura de pantalla muestra un ejemplo de este aviso de confirmación.</span><span class="sxs-lookup"><span data-stu-id="85e5f-123">The next screenshot shows an example of this confirmation prompt.</span></span>

 ![Elegir el modo Internet Explorer](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <span data-ttu-id="85e5f-125">Directivas de apoyo</span><span class="sxs-lookup"><span data-stu-id="85e5f-125">Supporting policies</span></span>

<span data-ttu-id="85e5f-126">Las empresas que deseen excluir el bloqueo de contenido mixto en sitios web específicos, pueden usar la directiva [InsecureContentAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#insecurecontentallowedforurls) para ello.</span><span class="sxs-lookup"><span data-stu-id="85e5f-126">Enterprises that want to exclude mixed content blocking from specific websites can use the [InsecureContentAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#insecurecontentallowedforurls) policy to do so.</span></span>

## <span data-ttu-id="85e5f-127">Licencia de contenido</span><span class="sxs-lookup"><span data-stu-id="85e5f-127">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="85e5f-128">Algunas partes de esta página son modificaciones que se basan en trabajo creado y compartido por Chromium.org y que se usan de acuerdo con los términos descritos en la [Licencia internacional de Creative Commons Atribution 4.0](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="85e5f-128">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="85e5f-129">La página original se puede encontrar [aquí](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span><span class="sxs-lookup"><span data-stu-id="85e5f-129">The original page can be found [here](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="85e5f-130">Este trabajo dispone de licencia conforme a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licencia internacional de Creative Commons Attribution 4.0</a>.</span><span class="sxs-lookup"><span data-stu-id="85e5f-130">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <span data-ttu-id="85e5f-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="85e5f-131">See also</span></span>

- [<span data-ttu-id="85e5f-132">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="85e5f-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
