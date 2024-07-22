---
title: texto
description: Texto de capa. Especifica texto y contenido de formato para una capa de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---

# texto{#text}

Texto de capa. Especifica texto y contenido de formato para una capa de texto.

` text= *`cadena`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> cadena </span> </p> </td> 
  <td class="stentry"> <p>Cadena de texto enriquecido (RTF) o cadena de texto sin formato. </p> </td> 
 </tr> 
</table>

Todo el control de la fuente, el color de fuente y el formato de párrafo se logra mediante comandos RTF. Consulte [Formato de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) para obtener información adicional.

`text=` admite la escala automática del texto para rellenar el rectángulo de capa especificado con `size=`.

Ver [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` admite el cambio de tamaño automático de la capa de texto para que se ajuste al texto procesado (cuando no se especifica `size=` o solo se especifica la anchura). Tenga en cuenta que, en este caso, sólo se puede aplicar uno de los comandos de alineación RTF `\ql`, `\qr` y `\qc`; en caso contrario, se devuelve un error.

## Propiedades {#section-8c0f020094a44c6b858454ef91ab4edf}

Atributo de capa. Se aplica a `layer=0` si `layer=comp`. Exclusivo de forma mutua con `src=` y `textPs=` en la misma capa; prevalece la última aparición de `text=`, `textPs=` y `src=`, y determina si se trata de una imagen o de una capa de texto. Ignorado por las capas de efecto.

## Predeterminado {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Ninguno.

## Ejemplo {#section-d011f765ec5c418d814a821019b0eef0}

Vea los ejemplos de [Formato de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) y [Ejemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) en [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Véase también {#section-207b779ab67342a5acd343e6bcc749c4}

[Formato de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Posición de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
