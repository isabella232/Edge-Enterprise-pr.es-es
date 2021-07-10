---
title: Sintaxis de Expresiones regulares 2
ms.author: comanea
author: dan-wesley
manager: seanlyn
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Sintaxis de Expresiones regulares 2
ms.openlocfilehash: 2fd0607939d4dd6ac9730390be869fa5be7149b2
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642226"
---
# <a name="regular-expression-2-re2h-syntax"></a>Sintaxis de Expresiones regulares 2 (re2.h)

Las expresiones regulares son una notación para describir conjuntos de cadenas de caracteres. Cuando una cadena se encuentra en el conjunto descrito por una expresión regular, se entiende, a menudo, que la expresión regular coincide con la cadena.

La expresión regular más simple es un carácter literal único. A excepción de los metacaracteres como *\*+?()|*, los caracteres coinciden con sí mismos. Para hacer coincidir un metacarácter, haga que se escape con una barra diagonal inversa: \+ coincidirá con un carácter más literal.

Se pueden modificar o concatenar dos expresiones regulares para formar una nueva expresión regular: si *e<sub>1</sub>* coincide con _s_ y *e<sub>2</sub>* coincide con _t_, entonces *e<sub>1</sub>* | *e<sub>2</sub>* coincide con _s_ o _t_, y *e<sub>1</sub>* *e<sub>2</sub>*  coincide con_st_.

Los metacaracteres _\*_ , _+_ , y _?_ son operadores de repetición: *e<sub>1</sub>* _\*_ coincide con una secuencia de cero o más (probablemente diferentes) cadenas, cada una de las cuales coincide con *e<sub>1</sub>*; *e<sub>1</sub>* _+_ coincide con una o más de una; *e<sub>1</sub>* _?_ coincide con cero o una.

La precedencia de operadores, desde el enlace más débil hasta el más fuerte, es, primero, alternancia, luego, concatenación y, por último, los operadores de repetición. Se pueden usar paréntesis explícitos para forzar significados distintos, al igual que en las expresiones aritméticas. Ejemplos: _ab|cd_ es equivalente a _(ab)|(cd)_ ; _ab\*_ es equivalente a _a(b\*)_ .

De la sintaxis descrita hasta ahora, la mayoría es de la sintaxis de las expresiones regulares _egrep_ de Unix. Este subconjunto basta para describir todos los lenguajes regulares: en líneas generales, un lenguaje regular es un conjunto de cadenas que se pueden hacer coincidir a través de un único paso por el texto utilizando solo una cantidad fija de memoria. Las utilidades de las expresiones regulares más recientes (en especial, Perl y aquellas que la han copiado) han agregado varios operadores nuevos y secuencias de escape, que hacen que las expresiones regulares sean más concisas y, a veces, más codificadas, pero, por lo general, no son más eficaces.

En esta página, se muestra la sintaxis de las expresiones regulares aceptada por RE2.

También se muestran algunas sintaxis aceptadas por PCRE, PERL y VIM.

## <a name="syntax-tables"></a>Tablas de sintaxis

| Tipos de expresiones de carácter único | Ejemplos |
| --- | --- |
| cualquier carácter, posiblemente que incluya nueva línea (s=true) | . |
| clase de carácter | [xyz] |
| clase de carácter negado | [^xyz] |
| clase de carácter de Perl ([vínculo](#user-content-perl)) | \d |
| clase de carácter de Perl negado | \D |
| clase de carácter de ASCII([vínculo](#user-content-ascii)) | [[:alpha:]] |
| clase de carácter de ASCIl negado | [[:^alpha:]] |
| clase de carácter de Unicode (nombre de una letra) | \pN |
| clase de carácter de Unicode | \p{Greek} |
| clase de carácter de Unicode negado (nombre de una letra) | \PN |
| clase de carácter de Unicode negado | \P{Greek} |

|&nbsp;| Composiciones |
| --- | --- |
| xy | x seguido de y |
| x\|y | x o y (prefiere x) |

|&nbsp;| Repeticiones |
| --- | --- |
| x\* | cero o más x, prefiere más |
| x+ | una o más x, prefiere más |
| x? | cero o una x, prefiere una |
| x{n,m} | n o n+1 o ... m x, prefiere más |
| x{n,} | n o más x, prefiere más |
| x{n} | exactamente n x |
| x\*? | cero o más x, prefiere menos |
| x+? | una o más x, prefiere menos |
| x?? | cero o una x, prefiere cero |
| x{n,m}? | n o n+1 o ... m x, prefiere menos |
| x{n,}? | n o más x, prefiere menos |
| x{n}? | exactamente n x |
| x{} | (≡ x\*) (NO COMPATIBLE) VIM |
| x{-} | (≡ x\*?) (NO COMPATIBLE) VIM |
| x{-n} | (≡ x{n}?) (NO COMPATIBLE) VIM |
| x= | (≡ x?) (NO COMPATIBLE) VIM |

Restricción de implementación: los recuentos de formularios x{n,m}, x {n,}, y x {n} rechazan los formularios que crean un recuento de repeticiones mínimo o máximo superior a 1000. Las repeticiones ilimitadas no están sujetas a esta restricción.

|&nbsp;| Repeticiones posesivas |
| --- | --- |
| x\*+ | cero o más x, posesiva (NO COMPATIBLE) |
| x++ | una o más x, posesiva (NO COMPATIBLE) |
| x?+ | cero o una x, posesiva (NO COMPATIBLE) |
| x{n,m}+ | n o ... o m x, posesiva (NO COMPATIBLE) |
| x{n,}+ | n o más x, posesiva (NO COMPATIBLE) |
| x{n}+ | exactamente n x, posesiva (NO COMPATIBLE) |

|&nbsp;| Agrupación |
| --- | --- |
| (re) | grupo de captura numerado (subcoincidencia) |
| (?P&lt;nombre&gt;re) | nombrado &amp; grupo de captura numerado (subcoincidencia) |
| (?&lt;nombre&gt;re) | nombrado &amp; grupo de captura numerado (subcoincidencia) (NO COMPATIBLE) |
| (?&#39;name&#39;re) | nombrado &amp; grupo de captura numerado (subcoincidencia) (NO COMPATIBLE) |
| (?:re) | grupo de no captura |
| (?flags) | establecer flags en el grupo actual; de no captura |
| (?flags:re) | establecer flags durante re; de no captura |
| (?#text) | comentario (NO COMPATIBLE) |
| (?\|x\|y\|z) | restablecimiento de numeración de bifurcación (NO COMPATIBLE) |
| (?&gt;re) | coincidencia posesiva de re (NO COMPATIBLE) |
| re@&gt; | coincidencia posesiva de re (NO COMPATIBLE) VIM |
| %(re) | grupo de no captura (NO COMPATIBLE) VIM |

|&nbsp;| Flags |
| --- | --- |
| i | no distingue mayúsculas de minúsculas (predeterminado false) |
| m | modo de varias líneas: ^ y $ coinciden en línea inicial/final, además del texto inicial/final (predeterminado false) |
| s | dejar . coincidir \n (predeterminado false) |
| U | no expansivo: cambiar significado de x\* y x\*?, x+ y x+?, etc. (predeterminado false) |

La sintaxis de flag es xyz (conjunto) o -xyz (limpiar) o xy-z (conjunto xy, limpiar z).

|&nbsp;| Cadenas vacías |
| --- | --- |
| ^ | al comienzo del texto o la línea (m=true) |
| $ | al final del texto (como \z, no \Z) o línea (m=true) |
| \A | al comienzo del texto |
| \b | en un límite de palabras ASCII (\w en un lado y \W, \A o \z en el otro) |
| \B | no en el límite de palabras ASCII |
| \g | al comienzo del subtexto que se busca (NO COMPATIBLE) PCRE |
| \G | al final de la última coincidencia (NO COMPATIBLE) PERL |
| \Z | al final del texto o antes de la línea nueva al final del texto (NO COMPATIBLE) |
| \z | al final del texto |
| (?=re) | antes del texto que coincide con re (NO COMPATIBLE) |
| (?!re) | antes del texto que no coincide con re (NO COMPATIBLE) |
| (?&lt;=re) | después del texto que coincide con re (NO COMPATIBLE) |
| (?&lt;!re) | después del texto que no coincide con re (NO COMPATIBLE) |
| re&amp; | antes del texto que coincide con re (NO COMPATIBLE) VIM |
| re@= | antes del texto que coincide con re (NO COMPATIBLE) VIM |
| re@! | antes del texto que no coincide con re (NO COMPATIBLE) VIM |
| re@&lt;= | después del texto que coincide con re (NO COMPATIBLE) VIM |
| re@&lt;! | después del texto que no coincide con re (NO COMPATIBLE) VIM |
| \zs | configura el inicio de la coincidencia (= \K) (NO COMPATIBLE) VIM |
| \ze | configura el final de la coincidencia (NO COMPATIBLE) VIM |
| \%^ | comienzo del archivo (NO COMPATIBLE) VIM |
| \%$ | final del archivo (NO COMPATIBLE) VIM |
| \%V | en pantalla (NO COMPATIBLE) VIM |
| \%# | posición del cursor (NO COMPATIBLE) VIM |
| \%&#39;m | marcar posición m (NO COMPATIBLE) VIM |
| \%23l | en línea 23 (NO COMPATIBLE) VIM |
| \%23c | en columna 23 (NO COMPATIBLE) VIM |
| \%23v | en columna virtual 23 (NO COMPATIBLE) VIM |

|&nbsp;| Secuencias de escape |
| --- | --- |
| \a | campana (≡ \007) |
| \f | fuente de formulario (≡ \014) |
| \t | pestaña horizontal (≡ \011) |
| \n | nueva línea (≡ \012) |
| \r | retorno de carro (≡ \015) |
| \v | carácter de pestaña vertical (≡ \013) |
| \* | literal \*, para cualquier carácter de puntuación \* |
| \123 | código de carácter octal (hasta tres dígitos) |
| \x7F | código de carácter hexadecimal (exactamente dos dígitos) |
| \x{10FFFF} | código de carácter hexadecimal |
| \C | coincidir un único byte en modo UTF-8 |
| \Q...\E | texto literal... incluso si ... tiene signos de puntuación |
| \1 | referencia inversa (NO COMPATIBLE) |
| \b | retroceso (NO COMPATIBLE) (uso \010) |
| \cK | carácter de control ^ K (NO COMPATIBLE) (uso \001, etc.) |
| \e | escape (NO COMPATIBLE) (uso \033) |
| \g1 | referencia inversa (NO COMPATIBLE) |
| \g{1} | referencia inversa (NO COMPATIBLE) |
| \g{+1} | referencia inversa (NO COMPATIBLE) |
| \g{-1} | referencia inversa (NO COMPATIBLE) |
| \g{nombre} | referencia inversa con nombre (NO COMPATIBLE) |
| \g&lt;nombre&gt; | llamada de subrutina (NO COMPATIBLE) |
| \g&#39;name&#39; | llamada de subrutina (NO COMPATIBLE) |
| \k&lt;nombre&gt; | referencia inversa con nombre (NO COMPATIBLE) |
| \k&#39;name&#39; | referencia inversa con nombre (NO COMPATIBLE) |
| \lX | X minúscula (NO COMPATIBLE) |
| \ux | x mayúscula (NO COMPATIBLE) |
| \L...\E | texto en minúsculas ... (NO COMPATIBLE) |
| \K | restablecer inicio de $0 (NO COMPATIBLE) |
| \N{nombre} | carácter Unicode con nombre (NO COMPATIBLE) |
| \R | salto de línea (NO COMPATIBLE) |
| \U...\E | texto en mayúsculas ... (NO COMPATIBLE) |
| \X | secuencia Unicode extendida (NO COMPATIBLE) |
| \%d123 | carácter decimal 123 (NO COMPATIBLE) VIM |
| \%xFF | carácter hexadecimal FF (NO COMPATIBLE) VIM |
| \%o123 | carácter octal 123 (NO COMPATIBLE) VIM |
| \%u1234 | carácter Unicode 0x1234 (NO COMPATIBLE) VIM |
| \%U12345678 | carácter Unicode 0x12345678 (NO COMPATIBLE) VIM |

|&nbsp;| Elementos de clases de carácter |
| --- | --- |
| x | carácter único |
| A-Z | rango de caracteres (inclusivo) |
| \d | clase de carácter de Perl |
| [:foo:] | clase foo de carácter de ASCII |
| \p{Foo} | clase foo de carácter de Unicode |
| \pF | clase F de carácter de Unicode (nombre de una letra) |

|&nbsp;| Clases de caracteres con nombre como elementos de clase de carácter |
| --- | --- |
| [\d] | dígitos (≡ \d) |
| [^\d] | no dígitos (≡ \D) |
| [\D] | no dígitos (≡ \D) |
| [^\D] | no no dígitos (≡ \d) |
| [[:name:]] | clase ASCII con nombre dentro de una clase de carácter (≡ [:name:]) |
| [^[:name:]] | clase ASCII con nombre en la clase de caracteres negados (≡ [:^name:]) |
| [\p{Name}] | propiedad de Unicode con nombre dentro de una clase de carácter (≡ \p{Name}) |
| [^\p{Name}] | propiedad de Unicode con nombre dentro de una clase de carácter negado (≡ \P{Name}) |

| <a name="user-content-perl"></a> | clases de caracteres Perl (todos solo ASCII) |
| --- | --- |
| \d | dígitos (≡ [0-9]) |
| \D | no dígitos (≡ [^0-9]) |
| \s | espacio en blanco (≡ [\t\n\f\r]) |
| \S | espacio no en blanco (≡ [^\t\n\f\r]) |
| \w | caracteres de palabras (≡ [0-9A-Za-z\_]) |
| \W | caracteres de no palabras (≡ [^0-9A-Za-z\_]) |
| \h | espacio horizontal (NO COMPATIBLE) |
| \H | espacio no horizontal (NO COMPATIBLE) |
| \v | espacio vertical (NO COMPATIBLE) |
| \V | espacio no vertical (NO COMPATIBLE) |

|<a name="user-content-ascii"></a>  | clases de carácter ASCII |
| --- | --- |
| [[:alnum:]] | alfanumérico (≡ [0-9A-Za-z]) |
| [[:alpha:]] | alfabético (≡ [A-Za-z]) |
| [[:ascii:]] | ASCII (≡ [\x00-\x7F]) |
| [[:blank:]] | en blanco (≡ [\t]) |
| [[:cntrl:]] | control (≡ [\x00-\x1F\x7F]) |
| [[:digit:]] | dígitos (≡ [0-9]) |
| [[:graph:]] | gráfico (≡ `[!-~]` ≡ `[A-Za-z0-9!&quot;#$%&amp;&#39;()\*+,\-./:;&lt;=&gt;?@[\\\]^_`\` `{\|}~]`) |
| [[:lower:]] | minúsculas (≡ [a-z]) |
| [[:print:]] | imprimible (≡ [-~] ≡ [[:graph:]]) |
| [[:punct:]] | puntuación (≡ [!-/:-@[-`{-~]) |
| [[:space:]] | espacio en blanco (≡ [\t\n\v\f\r]) |
| [[:upper:]] | mayúsculas (≡ [A-Z]) |
| [[:word:]] | caracteres de palabras (≡ [0-9A-Za-z\_]) |
| [[:xdigit:]] | dígito hexadecimal (≡ [0-9A-Fa-f]) |

|&nbsp;| Nombres de clase de carácter Unicode: categoría general |
| --- | --- |
| C | otro |
| CC | control |
| CF | format |
| CN | puntos de código sin asignar (NO COMPATIBLE) |
| CO | uso privado |
| CS | sustituto |
| L | letra |
| LC | letra en minúsculas o mayúsculas (NO COMPATIBLE) |
| L&amp; | letra en minúsculas o mayúsculas (NO COMPATIBLE) |
| Ll | letra minúscula |
| LM | letra modificadora |
| LO | otra letra |
| LT | letra del título |
| LU | letra mayúscula |
| M | marca |
| MC | marca de espacio |
| ME | marca de cierre |
| MN | marca de no espacio |
| N | número |
| ND | número decimal |
| NL | número de letra |
| No | otro número |
| P | puntuación |
| PC | puntuación de conector |
| PD | puntuación de guion |
| PE | puntuación de cierre |
| PF | puntuación final |
| Pi | puntuación inicial |
| PO | otra puntuación |
| PS | puntuación de apertura |
| S | symbol |
| SC | símbolo de moneda |
| SK | símbolo modificador |
| SM | símbolo matemático |
| SO | otro símbolo |
| Z | separador |
| Zl | separador de línea |
| ZP | separador de párrafo |
| ZS | separador de espacio |

| Nombres de clase de carácter Unicode: scripts |
| --- |
| Adlam |
| Ahom |
| Anatolia\_Jeroglíficos |
| Árabe |
| Armenio |
| Avéstico |
| Balinés |
| Bamum |
| Bassa\_Vah |
| Batak |
| Bengalí |
| Bhaiksuki |
| Bopomofo |
| Brahmi |
| Braille |
| Buginés |
| Buhid |
| Canadiense\_Indígena |
| Cario |
| Caucásico\_Albanés |
| Chakma |
| Cham |
| Cheroqui |
| Corasmia |
| Común |
| Copto |
| Cuneiforme |
| Chipriota |
| Cirílico |
| Deseret |
| Devanagari |
| Dives\_Akuru |
| Dogri |
| Duployán |
| Egipcio\_Jeroglíficos |
| Elbasan |
| Elymaic |
| Etíope |
| Georgiano |
| Glagolítico |
| Gótico |
| Grantha |
| Griego |
| Gujarati |
| Gunjala\_Gondi |
| Gurumukhi |
| Han |
| Hangul |
| Hanifi\_Rohinyá |
| Hanunoo |
| De Hatra |
| Hebreo |
| Hiragana |
| Imperial\_Arameo |
| Heredado |
| Inscripcional\_Pahlavi |
| Inscripcional\_Partio |
| Javanés |
| Kaithi |
| Kannada |
| Katakana |
| Kayah\_Li |
| Karosti |
| Khitan\_Pequeño\_Script |
| Khmer |
| Khojki |
| Khudabadi |
| Lao |
| Latino |
| Lepcha |
| Limbu |
| Lineal\_A |
| Lineal\_B |
| Lisu |
| Lycio |
| Lydio |
| Mahajani |
| Makassar |
| Malayalam |
| Mandeo |
| Maniqueo |
| Marchen |
| Masaram\_Gondi |
| Medefaidrin |
| Meitei\_Mayek |
| Mende\_Kikakui |
| Meroítico\_Cursiva |
| Meroítico\_Jeroglíficos |
| Miao |
| Modi |
| Mongol |
| Mro |
| Multani |
| Myanmar |
| Nabataeo |
| Nandinagari |
| Nuevo\_Tai\_Lue |
| Newa |
| Nko |
| Nushu |
| Nyiakeng\_Puachue\_Hmong |
| Ogham |
| Ol\_Chiki |
| Antiguo\_Húngaro |
| Antiguo\_Itálico |
| Antiguo\_Septentrional\_Árabe |
| Antiguo\_Pérmico |
| Antiguo\_Persa |
| Antiguo\_Sogdiano |
| Antiguo\_Meridional\_Árabe |
| Antiguo\_Turco |
| Odia |
| Osage |
| Osmanya |
| Pahawh\_Hmong |
| Palmira |
| Pau\_Cin\_Hau |
| Phags\_Pa |
| Fenicio |
| Psalter\_Pahlaví |
| Rejang |
| Rúnico |
| Samaritano |
| Saurashtra |
| Sharada |
| Shaviano |
| Siddham |
| SignoEscritura |
| Sinhala |
| Sogdiano |
| Sora\_Sompeng |
| Soyombo |
| Sundanés |
| Syloti\_Nagri |
| Siríaco |
| Tagalo |
| Tagbanwa |
| Tai\_Le |
| Tai\_Tham |
| Tai\_Viet |
| Takri |
| Tamil |
| Tangut |
| Telugu |
| Thaana |
| Tailandés |
| Tibetano |
| Tifinagh |
| Tirhuta |
| Ugarítico |
| Vai |
| Wancho |
| Warang\_Citi |
| Yazidí |
| Yi |
| Zanabazar\_Cuadrado |

|&nbsp;| clases de carácter Vim |
| --- | --- |
| \i | carácter identificador (NO COMPATIBLE) VIM |
| \I | \i excepto dígitos (NO COMPATIBLE) VIM |
| \k | carácter de palabra clave (NO COMPATIBLE) VIM |
| \K | \k excepto dígitos (NO COMPATIBLE) VIM |
| \f | carácter de nombre de archivo (NO COMPATIBLE) VIM |
| \F | \f excepto dígitos (NO COMPATIBLE) VIM |
| \p | carácter imprimible (NO COMPATIBLE) VIM |
| \P | \p excepto dígitos (NO COMPATIBLE) VIM |
| \s | carácter de espacio en blanco (≡ [\t]) (NO COMPATIBLE) VIM |
| \S | carácter de espacio no en blanco (≡ [^ \t]) (NO COMPATIBLE) VIM |
| \d | dígitos (≡ [0-9]) VIM |
| \D | no \d VIM |
| \x | dígitos hexadecimales (≡ [0-9A-Fa-f]) (NO COMPATIBLE) VIM |
| \X | no \x (NO COMPATIBLE) VIM |
| \o | dígitos octales (≡ [0-7]) (NO COMPATIBLE) VIM |
| \O | no \o (NO COMPATIBLE) VIM |
| \w | carácter de palabra VIM |
| \W | no \w VIM |
| \h | head de carácter de palabra (NO COMPATIBLE) VIM |
| \H | no \h (NO COMPATIBLE) VIM |
| \a | alfabético (NO COMPATIBLE) VIM |
| \A | no \a (NO COMPATIBLE) VIM |
| \l | minúscula (NO COMPATIBLE) VIM |
| \L | no minúscula (NO COMPATIBLE) VIM |
| \u | mayúscula (NO COMPATIBLE) VIM |
| \U | no mayúscula (NO COMPATIBLE) VIM |
| \_x | \x más nueva línea, para cualquier x (NO COMPATIBLE) VIM |
| \c | ignorar mayúsculas o minúsculas (NO COMPATIBLE) VIM |
| \C | coincidir mayúsculas o minúsculas (NO COMPATIBLE) VIM |
| \m | magic (NO COMPATIBLE) VIM |
| \M | nomagic (NO COMPATIBLE) VIM |
| \v | verymagic (NO COMPATIBLE) VIM |
| \V | verynomagic (NO COMPATIBLE) VIM |
| \Z | ignorar las diferencias en Unicode que combinan caracteres (NO COMPATIBLE) VIM |

| &nbsp; | Mágico |
| --- | --- |
| (?{code}) | código Perl arbitrario (NO COMPATIBLE) PERL |
| (??{code}) | código Perl arbitrario pospuesto (NO COMPATIBLE) PERL |
| (?n) | llamada recurrente para el grupo de captura regexp n (NO COMPATIBLE) |
| (?+n) | llamada recurrente para el grupo relativo +n (NO COMPATIBLE) |
| (?-n) | llamada recurrente para el grupo relativo -n (NO COMPATIBLE) |
| (?C) | callout PCRE (NO COMPATIBLE) PCRE |
| (?R) | llamada recurrente a todo el regexp (≡ (? 0)) (NO COMPATIBLE) |
| (?&amp;name) | llamada recurrente para el grupo con nombre (NO COMPATIBLE) |
| (?P=name) | referencia inversa con nombre (NO COMPATIBLE) |
| (?P&gt;name) | llamada recurrente para el grupo con nombre (NO COMPATIBLE) |
| (?(cond)true|falso) | bifurcación condicional (no compatible) |
| (?(cond)true) | bifurcación condicional (no compatible) |
| (\*ACCEPT) | convertir regexps más como prólogo (NO COMPATIBLE) |
| (\*COMMIT) | (NO COMPATIBLE) |
| (\*F) | (NO COMPATIBLE) |
| (\*FAIL) | (NO COMPATIBLE) |
| (\*MARK) | (NO COMPATIBLE) |
| (\*PRUNE) | (NO COMPATIBLE) |
| (\*SKIP) | (NO COMPATIBLE) |
| (\*THEN) | (NO COMPATIBLE) |
| (\*ANY) | establecer convención de nueva línea (NO COMPATIBLE) |
| (\*ANYCRLF) | (NO COMPATIBLE) |
| (\*CR) | (NO COMPATIBLE) |
| (\*CRLF) | (NO COMPATIBLE) |
| (\*LF) | (NO COMPATIBLE) |
| (\*BSR\_ANYCRLF) | establecer convención \R (NO COMPATIBLE) PCRE |
| (\*BSR\_UNICODE) | (NO COMPATIBLE) PCRE |

## <a name="content-license"></a>Licencia de contenido

> [!NOTE]
> Algunas partes de esta página son modificaciones que se basan en trabajo creado y compartido por Chromium.org y que se usan de acuerdo con los términos descritos en la [Licencia internacional de Creative Commons Atribution 4.0](http://creativecommons.org/licenses/by/4.0/). La página original se puede encontrar [aquí](https://github.com/google/re2/wiki/Syntax).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Este trabajo dispone de licencia conforme a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licencia internacional de Creative Commons Attribution 4.0</a>.

## <a name="see-also"></a>Consulte también

- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)