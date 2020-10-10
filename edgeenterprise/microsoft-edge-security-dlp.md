---
title: Prevención de pérdida de datos en Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 10/08/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Prevención de pérdida de datos (DLP) en Microsoft Edge
ms.openlocfilehash: 59c1b68c0526a49a2ee30283893707852514828d
ms.sourcegitcommit: 2af303fc97e8493024e2359fa2e8be162ab95a59
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104632"
---
# <span data-ttu-id="9b71a-103">Prevención de pérdida de datos (DLP) en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9b71a-103">Data Loss Prevention (DLP) in Microsoft Edge</span></span>

<span data-ttu-id="9b71a-104">La prevención de pérdida de datos (DLP) es un sistema de tecnologías que identifican y protegen los datos confidenciales de la empresa de la divulgación no autorizada.</span><span class="sxs-lookup"><span data-stu-id="9b71a-104">Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure.</span></span> <span data-ttu-id="9b71a-105">Con el fin de cumplir las normas de la industria y los estándares empresariales, las organizaciones deben proteger la información confidencial y evitar la divulgación no autorizada.</span><span class="sxs-lookup"><span data-stu-id="9b71a-105">To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure.</span></span> <span data-ttu-id="9b71a-106">La información confidencial incluye datos financieros o información de identificación personal (PII), como números de tarjeta de crédito, números de la seguridad social o registros de salud, entre muchas otras cosas.</span><span class="sxs-lookup"><span data-stu-id="9b71a-106">Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.</span></span>

<span data-ttu-id="9b71a-107">El trabajo remoto ha aumentado el énfasis en el uso de DLP.</span><span class="sxs-lookup"><span data-stu-id="9b71a-107">Remote work has increased the emphasis on using DLP.</span></span> <span data-ttu-id="9b71a-108">Con el creciente uso de las actividades personales y laborales en los dispositivos, las empresas están experimentando un mayor riesgo de que se compartan de forma no autorizada datos corporativos externos al lugar de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9b71a-108">With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.</span></span>

<span data-ttu-id="9b71a-109">Esta mezcla de las actividades de los usuarios también se distribuye en los dispositivos, en la que los datos se mueven entre dispositivos corporativos y de la empresa a través de una variedad de redes privadas y públicas.</span><span class="sxs-lookup"><span data-stu-id="9b71a-109">This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks.</span></span> <span data-ttu-id="9b71a-110">El resultado neto es un riesgo mucho mayor de revelar datos confidenciales.</span><span class="sxs-lookup"><span data-stu-id="9b71a-110">The net result is a dramatically increased risk of exposing sensitive data.</span></span>

<span data-ttu-id="9b71a-111">Microsoft Edge es compatible de forma nativa con dos soluciones DLP distintas, DLP de Microsoft Endpoint y la protección de información de Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="9b71a-111">Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).</span></span>

## <span data-ttu-id="9b71a-112">Administrador de puntos de conexión de Microsoft</span><span class="sxs-lookup"><span data-stu-id="9b71a-112">Microsoft Endpoint DLP</span></span>

<span data-ttu-id="9b71a-113">Microsoft Endpoint DLP es la siguiente generación de DLP que usa conceptos modernos como, por ejemplo, la protección centrada en datos.</span><span class="sxs-lookup"><span data-stu-id="9b71a-113">Microsoft Endpoint DLP is the next generation of DLP using modern concepts such as data-centric protection.</span></span> <span data-ttu-id="9b71a-114">Está integrado en Windows 10 y Microsoft Edge, por lo que no necesita complementos o agentes adicionales en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b71a-114">It's  built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device.</span></span> <span data-ttu-id="9b71a-115">Para más información sobre las DLP de Endpoint, lea [más información sobre la prevención de pérdida de datos de Microsoft 365 Endpoint](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="9b71a-115">To learn more about endpoint DLP, read [Learn about Microsoft 365 Endpoint data loss prevention](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide).</span></span>

> [!NOTE]
> <span data-ttu-id="9b71a-116">Esto se aplica a Microsoft Edge, versión 85 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9b71a-116">This applies to Microsoft Edge version 85 or later.</span></span>

<span data-ttu-id="9b71a-117">Microsoft Edge aplica directivas configuradas por el administrador para archivos confidenciales y registra eventos de auditoría para actividades de no conformidad.</span><span class="sxs-lookup"><span data-stu-id="9b71a-117">Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.</span></span>

<span data-ttu-id="9b71a-118">Entre las actividades de usuario que se pueden auditar y administrar en los dispositivos que ejecutan Windows 10 se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="9b71a-118">Some of the user activities that you can audit and manage on devices running Windows 10 include the following activities:</span></span>

- <span data-ttu-id="9b71a-119">Carga de archivos: protege la carga de archivos confidenciales en ubicaciones en la nube no autorizadas.</span><span class="sxs-lookup"><span data-stu-id="9b71a-119">File Upload: Protect sensitive file upload to unauthorized cloud locations.</span></span> <span data-ttu-id="9b71a-120">Las 3 capturas de pantalla siguientes muestran una secuencia en la que un usuario intenta quitar un archivo de datos confidencial en su almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="9b71a-120">The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.</span></span>
- <span data-ttu-id="9b71a-121">Protección del portapapeles: proteger la copia de datos confidenciales de desde el archivo.</span><span class="sxs-lookup"><span data-stu-id="9b71a-121">Clipboard Protection: Protect sensitive data from being copied out of the file.</span></span>
- <span data-ttu-id="9b71a-122">Protección de impresión: proteger el archivo confidencial para que no se imprima.</span><span class="sxs-lookup"><span data-stu-id="9b71a-122">Print Protection: Protect sensitive file from being printed.</span></span>
- <span data-ttu-id="9b71a-123">Guardar en USB/red: proteger el archivo confidencial para que no se guarde en un almacenamiento USB extraíble o en ubicaciones de red no autorizadas.</span><span class="sxs-lookup"><span data-stu-id="9b71a-123">Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.</span></span>

<span data-ttu-id="9b71a-124">Para obtener información más detallada sobre las actividades de usuario que se pueden auditar y administrar, consulte [actividades de Endpoint que se pueden supervisar y tomar medidas en](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span><span class="sxs-lookup"><span data-stu-id="9b71a-124">For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span></span>

## <span data-ttu-id="9b71a-125">Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="9b71a-125">Windows Information Protection</span></span>

<span data-ttu-id="9b71a-126">Consulte [Soporte técnico para protección de la información de Windows](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), donde se describe cómo Microsoft Edge es compatible con la protección de información de Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="9b71a-126">Check out [Support for Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), which describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span> <span data-ttu-id="9b71a-127">Puede obtener más información sobre los requisitos del sistema, las prestaciones y las características compatibles en las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="9b71a-127">You can learn moe about system requirements, benefits, and supported features in the following sections:</span></span>

- [<span data-ttu-id="9b71a-128">Requisitos del sistema</span><span class="sxs-lookup"><span data-stu-id="9b71a-128">System Requirements</span></span>](https://docs.microsoft.com/deployedge/:microsoft-edge-security-windows-information-protection#system-requirements)
- [<span data-ttu-id="9b71a-129">Beneficios de la Protección de la Información de Windows</span><span class="sxs-lookup"><span data-stu-id="9b71a-129">Windows Information Protection Benefits</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [<span data-ttu-id="9b71a-130">Las características WIP compatibles en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9b71a-130">WIP features supported in Microsoft Edge</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## <span data-ttu-id="9b71a-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9b71a-131">See also</span></span>

- [<span data-ttu-id="9b71a-132">Página de aterrizaje de Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="9b71a-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="9b71a-133">Vídeo: prevención de pérdida de datos-Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9b71a-133">Video: Data loss prevention - Microsoft Edge</span></span>](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [<span data-ttu-id="9b71a-134">Información general sobre la prevención de pérdida de datos</span><span class="sxs-lookup"><span data-stu-id="9b71a-134">Overview of data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide)
- [<span data-ttu-id="9b71a-135">Proteger los datos de tu empresa con Windows Information Protection (WIP)</span><span class="sxs-lookup"><span data-stu-id="9b71a-135">Protect your enterprise data using Windows Information Protection</span></span>](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
