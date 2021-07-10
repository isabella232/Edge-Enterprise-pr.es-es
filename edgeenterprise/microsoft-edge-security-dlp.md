---
title: Prevención de pérdida de datos en Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Prevención de pérdida de datos (DLP) en Microsoft Edge
ms.openlocfilehash: acbc9dab14c193f4f7cb06eb61e676083bfdf6ef
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642656"
---
# <a name="data-loss-prevention-dlp-in-microsoft-edge"></a><span data-ttu-id="9a50d-103">Prevención de pérdida de datos (DLP) en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9a50d-103">Data Loss Prevention (DLP) in Microsoft Edge</span></span>

<span data-ttu-id="9a50d-104">La prevención de pérdida de datos (DLP) es un sistema de tecnologías que identifican y protegen los datos confidenciales de la empresa de la divulgación no autorizada.</span><span class="sxs-lookup"><span data-stu-id="9a50d-104">Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure.</span></span> <span data-ttu-id="9a50d-105">Con el fin de cumplir las normas de la industria y los estándares empresariales, las organizaciones deben proteger la información confidencial y evitar la divulgación no autorizada.</span><span class="sxs-lookup"><span data-stu-id="9a50d-105">To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure.</span></span> <span data-ttu-id="9a50d-106">La información confidencial incluye datos financieros o información de identificación personal (PII), como números de tarjeta de crédito, números de la seguridad social o registros de salud, entre muchas otras cosas.</span><span class="sxs-lookup"><span data-stu-id="9a50d-106">Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.</span></span>

<span data-ttu-id="9a50d-107">El trabajo remoto ha aumentado el énfasis en el uso de DLP.</span><span class="sxs-lookup"><span data-stu-id="9a50d-107">Remote work has increased the emphasis on using DLP.</span></span> <span data-ttu-id="9a50d-108">Con el creciente uso de las actividades personales y laborales en los dispositivos, las empresas están experimentando un mayor riesgo de que se compartan de forma no autorizada datos corporativos externos al lugar de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9a50d-108">With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.</span></span>

<span data-ttu-id="9a50d-109">Esta mezcla de las actividades de los usuarios también se distribuye en los dispositivos, en la que los datos se mueven entre dispositivos corporativos y de la empresa a través de una variedad de redes privadas y públicas.</span><span class="sxs-lookup"><span data-stu-id="9a50d-109">This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks.</span></span> <span data-ttu-id="9a50d-110">El resultado neto es un riesgo mucho mayor de revelar datos confidenciales.</span><span class="sxs-lookup"><span data-stu-id="9a50d-110">The net result is a dramatically increased risk of exposing sensitive data.</span></span>

<span data-ttu-id="9a50d-111">Microsoft Edge es compatible de forma nativa con dos soluciones DLP distintas, DLP de Microsoft Endpoint y la protección de información de Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="9a50d-111">Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).</span></span>

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a><span data-ttu-id="9a50d-112">Prevención de pérdida de datos de Microsoft Endpoint (DLP de Endpoint)</span><span class="sxs-lookup"><span data-stu-id="9a50d-112">Microsoft Endpoint data loss prevention (Endpoint DLP)</span></span>

<span data-ttu-id="9a50d-113">DLP de Microsoft Endpoint es la siguiente generación de prevención de pérdida de datos con conceptos modernos como la protección centrada en los datos.</span><span class="sxs-lookup"><span data-stu-id="9a50d-113">Microsoft Endpoint DLP is the next generation of data loss prevention using modern concepts such as data-centric protection.</span></span> <span data-ttu-id="9a50d-114">Está integrado en Windows 10 y Microsoft Edge, de modo que no necesitará agentes ni complementos adicionales en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a50d-114">It's built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device.</span></span>

> [!NOTE]
> <span data-ttu-id="9a50d-115">Esto se aplica a la versión 85 y a las posteriores de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a50d-115">This applies to Microsoft Edge version 85 or later.</span></span>

<span data-ttu-id="9a50d-116">Para más información sobre DLP de punto de conexión, use los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="9a50d-116">To learn more about Endpoint DLP, use the following resources:</span></span>

- [<span data-ttu-id="9a50d-117">Vídeo: Prevención de pérdida de datos (DLP) de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9a50d-117">Video: Microsoft Edge and Data loss prevention (DLP)</span></span>](microsoft-edge-video-security-dlp.md)
- [<span data-ttu-id="9a50d-118">Más información sobre la prevención de pérdida de datos de Endpoint de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9a50d-118">Learn about Microsoft 365 Endpoint data loss prevention</span></span>](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide)
- [<span data-ttu-id="9a50d-119">Introducción a la prevención de pérdida de datos de Endpoint</span><span class="sxs-lookup"><span data-stu-id="9a50d-119">Get started with Endpoint data loss prevention</span></span>](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide)

<span data-ttu-id="9a50d-120">Microsoft Edge aplica directivas configuradas por el administrador para los archivos confidenciales y registra eventos de auditoría para las actividades que no cumplan con la normativa.</span><span class="sxs-lookup"><span data-stu-id="9a50d-120">Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.</span></span>

<span data-ttu-id="9a50d-121">Entre las actividades de usuario que se pueden auditar y administrar en los dispositivos que ejecutan Windows 10 se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="9a50d-121">Some of the user activities that you can audit and manage on devices running Windows 10 include the following activities:</span></span>

- <span data-ttu-id="9a50d-122">Carga de archivos: proteger la carga de archivos confidenciales en ubicaciones en la nube no autorizadas.</span><span class="sxs-lookup"><span data-stu-id="9a50d-122">File Upload: Protect sensitive file upload to unauthorized cloud locations.</span></span> <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- <span data-ttu-id="9a50d-123">Protección del portapapeles: proteger la copia de datos confidenciales desde el archivo.</span><span class="sxs-lookup"><span data-stu-id="9a50d-123">Clipboard Protection: Protect sensitive data from being copied out of the file.</span></span>
- <span data-ttu-id="9a50d-124">Protección de impresión: proteger el archivo confidencial para que no se imprima.</span><span class="sxs-lookup"><span data-stu-id="9a50d-124">Print Protection: Protect sensitive file from being printed.</span></span>
- <span data-ttu-id="9a50d-125">Guardar en USB/red: proteger el archivo confidencial para que no se guarde en un almacenamiento USB extraíble o en ubicaciones de red no autorizadas.</span><span class="sxs-lookup"><span data-stu-id="9a50d-125">Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.</span></span>

<span data-ttu-id="9a50d-126">Para obtener información más detallada sobre las actividades de usuario que se pueden auditar y administrar, consulte [actividades de Endpoint que se pueden supervisar y tomar medidas en](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span><span class="sxs-lookup"><span data-stu-id="9a50d-126">For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span></span>

## <a name="windows-information-protection"></a><span data-ttu-id="9a50d-127">Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="9a50d-127">Windows Information Protection</span></span>

<span data-ttu-id="9a50d-128">Consulte [Soporte técnico para protección de la información de Windows](./microsoft-edge-security-windows-information-protection.md), donde se describe cómo Microsoft Edge es compatible con la protección de información de Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="9a50d-128">Check out [Support for Windows Information Protection](./microsoft-edge-security-windows-information-protection.md), which describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span> <span data-ttu-id="9a50d-129">Puede obtener más información sobre los requisitos del sistema, las prestaciones y las características compatibles en las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="9a50d-129">You can learn moe about system requirements, benefits, and supported features in the following sections:</span></span>

- [<span data-ttu-id="9a50d-130">Requisitos del sistema</span><span class="sxs-lookup"><span data-stu-id="9a50d-130">System Requirements</span></span>](./microsoft-edge-security-windows-information-protection.md#system-requirements)
- [<span data-ttu-id="9a50d-131">Beneficios de la Protección de la Información de Windows</span><span class="sxs-lookup"><span data-stu-id="9a50d-131">Windows Information Protection Benefits</span></span>](./microsoft-edge-security-windows-information-protection.md#windows-information-protection-benefits)
- [<span data-ttu-id="9a50d-132">Las características WIP compatibles en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9a50d-132">WIP features supported in Microsoft Edge</span></span>](./microsoft-edge-security-windows-information-protection.md#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a><span data-ttu-id="9a50d-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9a50d-133">See also</span></span>

- [<span data-ttu-id="9a50d-134">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="9a50d-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="9a50d-135">Vídeo: prevención de pérdida de datos-Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9a50d-135">Video: Data loss prevention - Microsoft Edge</span></span>](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [<span data-ttu-id="9a50d-136">Información general sobre la prevención de pérdida de datos</span><span class="sxs-lookup"><span data-stu-id="9a50d-136">Overview of data loss prevention</span></span>](/microsoft-365/compliance/data-loss-prevention-policies?preserve-view=true&view=o365-worldwide)
- [<span data-ttu-id="9a50d-137">Proteger los datos de tu empresa con Windows Information Protection (WIP)</span><span class="sxs-lookup"><span data-stu-id="9a50d-137">Protect your enterprise data using Windows Information Protection</span></span>](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)