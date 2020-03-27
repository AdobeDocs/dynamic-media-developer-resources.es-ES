---
description: Texto de capa. Especifica el texto y el formato del contenido de una capa de texto.
seo-description: Texto de capa. Especifica el texto y el formato del contenido de una capa de texto.
seo-title: texto
solution: Experience Manager
title: texto
topic: Scene7 Image Serving - Image Rendering API
uuid: 5b4f9282-83a3-488d-b5d2-deb2c92de564
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# texto{#text}

Texto de capa. Especifica el texto y el formato del contenido de una capa de texto.

` text= *`cadena`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> cadena </span> </p> </td> 
  <td class="stentry"> <p>Cadena con formato de texto enriquecido (RTF) o cadena de texto sin formato. </p> </td> 
 </tr> 
</table>

Todos los controles de fuente, color de fuente y formato de párrafo se consiguen mediante comandos RTF. Consulte Formato [de](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) texto para obtener más información.

`text=` admite el escalado automático del texto para rellenar el rectángulo de capa especificado con `size=`.

Consulte [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` admite el ajuste automático del tamaño de la capa de texto para que se ajuste al texto procesado (cuando no `size=` se especifica o solo se especifica la anchura). Tenga en cuenta que en este caso solo se puede aplicar uno de los comandos de alineación de RTF `\ql`, `\qr`, y `\qc` ; en caso contrario, se devuelve un error.

## Propiedades {#section-8c0f020094a44c6b858454ef91ab4edf}

Atributo de capa. Se aplica a `layer=0` if `layer=comp`. Mutuamente exclusiva con `src=` y `textPs=` en la misma capa; la última incidencia de `text=`, `textPs=`y `src=` prevalece y determina si se trata de una imagen o una capa de texto. Omitido por capas de efectos.

## Predeterminado {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Ninguno.

## Ejemplo {#section-d011f765ec5c418d814a821019b0eef0}

Consulte los ejemplos de Formato [de](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) texto y [Ejemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) en [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Véase también {#section-207b779ab67342a5acd343e6bcc749c4}

[Formato](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)de texto, posición [de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
