---
title: Interrupción de las descargas de archivos potencialmente peligrosos
ms.author: kvice
author: AndreaLBarr
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Interrupción de las descargas de archivos potencialmente peligrosos
ms.openlocfilehash: 527b98b54cf03f6c116624296c63803b57a7f0c4
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642676"
---
# <a name="interrupting-downloads-of-potentially-dangerous-files"></a>Interrupción de las descargas de archivos potencialmente peligrosos

El componente de Directivas de tipo de archivo de Microsoft Edge permite clasificar los archivos según su nivel de "peligrosidad", de modo que los archivos inofensivos (por ejemplo,`.txt` los archivos) pueden descargarse libremente, mientras que los archivos potencialmente peligrosos (por ejemplo,`.dll` los archivos) se someten a un mayor grado de revisión y a una experiencia de usuario más consciente de la seguridad.

## <a name="determining-the-danger-level-of-a-file-type"></a>Determinando el nivel de peligro de un tipo de archivo

Microsoft Edge hereda sus directivas de tipo de archivo del navegador Chromium; puede ver el contenido actual de la lista[aquí](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb). Dentro de la lista, verá que cada tipo tiene un danger_level, que es uno de los tres valores: `DANGEROUS`, `NOT_DANGEROUS`, o `ALLOW_ON_USER_GESTURE`.

Las dos primeras son sencillas: **NOT_DANGEROUS** significa que el archivo es seguro para descargar, incluso si la descarga fue accidental. **DANGEROUS** significa que el navegador debe advertir siempre al usuario de que la descarga puede dañar su dispositivo.

El tercer ajuste **ALLOW_ON_USER_GESTURE** es más sutil. Estos archivos son potencialmente peligrosos, pero lo más probable es que sean inofensivos si el usuario solicitó la descarga. Microsoft Edge permitirá que estas descargas se realicen automáticamente si se cumplen dos condiciones:

1. Hay un[gesto del usuario](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) asociado a la solicitud de red que inició la descarga (por ejemplo, el usuario hizo clic en un enlace a la descarga).
2. Existe una visita previa registrada al origen de referencia (la página que enlaza con la descarga) antes de la medianoche más reciente (es decir, ayer o antes). Esto implica que el usuario tiene un historial de visitas al sitio.

La descarga también se realizará de forma automática si el usuario la ha iniciado explícitamente mediante el comando del menú contextual **Guardar vínculo como**, ha introducido la URL de la descarga directamente en la barra de direcciones del navegador o si Microsoft Defender SmartScreen ha indicado que el archivo es seguro.

**Actualización:** a partir de la versión 91, Microsoft Edge interrumpirá las descargas que no dispongan del gesto requerido

## <a name="user-experience-for-downloads-lacking-gestures"></a>Experiencia de usuario para descargas sin gestos

Si una descarga de un tipo potencialmente peligroso se inicia sin el gesto requerido, Microsoft Edge indica que la descarga "fue bloqueada". Los comandos nombrados `Keep` y `Delete` están disponibles desde el... menú en el elemento de descarga para que el usuario pueda continuar o cancelar la descarga.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="La descarga fue bloqueada":::

En la página `edge://downloads`, el usuario verá las mismas opciones:

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="Opción de mantener la eliminación de MSG":::

## <a name="enterprise-controls"></a>Control de la empresa

Aunque es poco probable que los usuarios se encuentren con interrupciones en las descargas de los sitios que utilizan a diario, sí pueden encontrarlas en las descargas legítimas de los sitios que utilizan rara vez. Para ayudar a racionalizar la experiencia de los usuarios de las empresas, existe una directiva de grupo.

Las empresas pueden utilizar [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) para especificar los tipos de archivo que se pueden descargar de sitios específicos sin interrupción. Por ejemplo, la siguiente directiva permite que los archivos XML se descarguen de contoso.com y woodgrovebank.com sin interrupción, y que los archivos MSG se descarguen de cualquier sitio.

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a>Tipos de archivos que requieren un gesto

Las últimas directivas de [tipos de archivos](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb)están publicadas en el código fuente de Chromium. A partir de mayo de 2021, los tipos de archivo con una`danger_level` de `ALLOW_ON_USER_GESTURE` al menos una plataforma de SO incluyen:
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="danger-level-may-vary-by-operating-system"></a>El nivel de peligro puede variar según el sistema operativo

La configuración del tipo de archivo a veces varía en función de la plataforma del sistema operativo del cliente. Por ejemplo, un `.exe` no es peligroso en un Mac, mientras que un `.applescript` es inofensivo en Windows.
