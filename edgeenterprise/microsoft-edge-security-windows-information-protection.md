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
ms.openlocfilehash: a9981947462627ae4884f18f4df6accf2ee60f12
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447194"
---
# <a name="microsoft-edge-support-for-windows-information-protection-wip"></a>Microsoft Edge compatible para la Protección de la información de Windows (WIP)

Este artículo describe cómo Microsoft Edge es compatible con la protección de información de Windows (WIP).

> [!NOTE]
> Esto se aplica para la versión 81 de Microsoft Edge o posterior

## <a name="overview"></a>Introducción

La Protección de la información de Windows (WIP) es una característica de Windows 10 que ayuda a proteger los datos de la empresa contra la divulgación no autorizada o accidental. Con el aumento del trabajo a distancia, hay un mayor riesgo de compartir datos corporativos fuera del lugar de trabajo. Este riesgo aumenta cuando las actividades personales y laborales se realizan en dispositivos corporativos.

Microsoft Edge es compatible con WIP para ayudar a proteger el contenido en un entorno web en el que los usuarios suelen compartir y distribuir contenido.

### <a name="system-requirements"></a>Requisitos del sistema

Los siguientes requisitos se aplican a los dispositivos que utilizan WIP en la empresa:

- Windows10, versión 1607 o posterior
- Sólo SKUs de clientes de Windows
- Una de las soluciones de administración descritas en [requisitos previos de WIP](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)

### <a name="windows-information-protection-benefits"></a>Beneficios de la Protección de la Información de Windows

El WIP proporciona los siguientes beneficios:

- Separación obvia entre los datos personales y corporativos, sin necesidad de que los empleados cambien de entornos o aplicaciones.
- Protección de datos adicional para aplicaciones de línea de negocio sin necesidad de actualizar las aplicaciones.
- La capacidad de borrar a distancia los datos corporativos de los dispositivos inscritos en la administración de dispositivos móviles de Microsoft Intune (MDM) sin afectar a los datos personales. 
- Informes de auditoría para el seguimiento de los problemas y para la adopción de medidas correctivas, como la capacitación de los usuarios en materia de cumplimiento.
- Integración con su sistema de gestión existente para configurar, desplegar y gestionar WIP. Algunos ejemplos son Microsoft Intune, el Administrador de configuración de Microsoft Endpoint, o su actual sistema de administración de dispositivos móviles (MDM).

## <a name="wip-policy-and-protection-modes"></a>Modos de protección y directiva de WIP

Mediante las directivas, puede configurar los cuatro modos de protección descritos en la siguiente tabla. Para más información, consulte[modos de protección WIP](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).

| Modo | Descripción |
|------|-------------|
| Bloquear | WIP busca prácticas de uso compartido inapropiado de datos y evita que el empleado complete la acción. Esta búsqueda puede incluir el uso compartido de datos de la empresa con aplicaciones no protegidas por la empresa, además del uso compartido de datos de la empresa entre aplicaciones o el intento de uso compartido fuera de la red de la organización. |
| Permitir invalidaciones | WIP busca usos compartidos inapropiados de datos y advierte a los empleados si realizan acciones potencialmente no seguras. Sin embargo, este modo de administración permite a los empleados invalidar la directiva y compartir los datos, registrando la acción en el registro de auditoría. |
| Silencio | WIP se ejecuta de forma silenciosa, registra el intercambio de datos inapropiados, sin detener nada que hubiera sido requerido para la interacción del empleado en el modo Permitir anulaciones. Las acciones no autorizadas siguen detenidas, como, por ejemplo, el intento de acceso inapropiado de aplicaciones a un recurso de red o datos protegidos por WIP. |
| Desactivado | WIP está desactivo y no ayuda a proteger ni auditar los datos. Tras desactivar WIP, se intentan descifrar los archivos etiquetados de WIP en las unidades conectadas localmente. Tenga en cuenta que la información previa de directiva y descifrado no se vuelve a aplicar automáticamente si vuelve a activar la protección WIP.
 |

## <a name="wip-features-supported-in-microsoft-edge"></a>Las características WIP compatibles en Microsoft Edge

A partir de la versión 81 de Microsoft Edge, se admiten las siguientes características:

- Los sitios de trabajo se indicarán con un icono de maletín en la barra de direcciones.  
- Los archivos descargados de un lugar de trabajo se encriptan automáticamente.
- Silenciar/Bloquear/Anular la carga de archivos de trabajo en lugares que no son de trabajo.  
- Silenciar/Bloquear/Anular las acciones de arrastrar y soltar archivos.
- Silenciar/Bloquear/Anular el cumplimiento de las acciones del Portapapeles.
- Navegar a lugares de trabajo desde perfiles no laborales se redirige automáticamente al Perfil de trabajo (asociado con Azure AD Identity.)
- El modo IE es compatible con la funcionalidad WIP completa.

## <a name="working-with-wip-in-microsoft-edge"></a>Trabajando con WIP en Microsoft Edge

Después de que se habilite el soporte WIP para Microsoft Edge, los usuarios verán cuando se acceda a la información relacionada con el trabajo. La siguiente captura de pantalla muestra el icono de un maletín en la barra de direcciones, lo que indica que se accede a la información relacionada con el trabajo a través del navegador.

 ![Indicador de la barra de direcciones para los sitios marcados como "trabajo".](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-notify.png)

Microsoft Edge ofrece a los usuarios la posibilidad de compartir contenido protegido en un sitio web no aprobado. La siguiente captura de pantalla muestra el aviso de Microsoft Edge que permite a un usuario utilizar contenido protegido en un sitio web no aprobado.

 ![Solicitud de anulación de contenido protegido](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-override.png)

## <a name="configure-policies-to-support-wip"></a>Configurar las directivas compatibles con WIP

El uso de WIP con Microsoft Edge requiere la presencia de un perfil de trabajo.

### <a name="ensure-the-presence-of-a-work-profile"></a>Asegure la presencia de un perfil de trabajo

En equipos híbridos Unidos, Microsoft Edge inicia sesión automáticamente en la cuenta Azure Active Directory (Azure AD). Para asegurarse de que los usuarios no eliminen este perfil necesario para la WIP, configure la siguiente directiva:

- [NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)

> [!NOTE]
> Si su entorno no es un híbrido unido, puede unirse a un híbrido usando estas instrucciones: [Planifique la implementación de su híbrido Azure Active Directory](/azure/active-directory/devices/hybrid-azuread-join-plan).

Si la unión híbrida no es una opción, puede usar cuentas de Active Directory locales para permitir que Microsoft Edge cree automáticamente un perfil de trabajo especial con las cuentas de dominio de los usuarios. Tenga en cuenta que las cuentas locales pueden no recibir todas las funciones de Azure AD, como la sincronización de la nube, Office NTP y muchas más.

#### <a name="active-directory-ad-accounts"></a>Cuentas de Active Directory (AD)

Para las cuentas de AD, debes configurar la siguiente política para que Microsoft Edge cree automáticamente un perfil de trabajo especial.

- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)

### <a name="windows-policies-for-wip"></a>Directivas de Windows10 para WIP

Puede configurar WIP usando las directivas de Windows. Para más información, consulte[Crear y desplegar directivas WIP usando Microsoft Intune ](/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

### <a name="how-do-i-resolve-error-code--2147024540"></a>¿Cómo puedo resolver el código de error -2147024540?

Este código de error corresponde al siguiente error de Protección de información de Windows:* ERROR_EDP_POLICY_DENIES_OPERATION: La operación solicitada fue bloqueada por la política de Protección de información de Windows. Para obtener más información, póngase en contacto con el administrador del sistema.*

Microsoft Edge muestra este error cuando la organización ha habilitado Windows Information Protection (WIP) para permitir que solo los usuarios con solicitudes aprobadas puedan tener acceso a los recursos corporativos. En este caso, dado que Microsoft Edge no está en la lista de aplicaciones aprobadas, el administrador tendrá que actualizar las directivas de WIP para conceder acceso a Microsoft Edge.

La siguiente captura de pantalla muestra cómo se usa Microsoft Intune para agregar Microsoft Edge como aplicación permitida para WIP.

 ![Cuadro de diálogo de Intune para agregar Microsoft Edge como aplicación para WIP](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-exemption.png)

Si no usa Microsoft Intune, descargue y aplique la actualización de directiva en el archivo [Directiva de WIP Enterprise AppLocker](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip).

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) 
- [Proteger los datos de la empresa mediante Protección de información de Windows](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)