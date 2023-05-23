---
description: Texto de capa (compatible con Adobe Photoshop). Especifica el cuerpo del texto de una capa de texto.
solution: Experience Manager
title: textPs
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95f343ce-bea3-425e-9a25-d1d141a976d9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# textPs{#textps}

Texto de capa (compatible con Adobe Photoshop). Especifica el cuerpo del texto de una capa de texto.

`textPs= *`cadena`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> cadena</span> </span> </p> </td> 
  <td class="stentry"> <p>Cadena con formato de texto enriquecido (RTF). </p></td> 
 </tr> 
</table>

Todo el control de la fuente, el color de fuente y el formato de párrafo se logra mediante comandos RTF.

Consulte [Formato de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` admite funciones ampliadas, como la justificación, el flujo de texto en regiones no rectangulares definidas con `textFlowPath=` y/o `textFlowXPath=`, y procesamiento de texto a lo largo de rutas arbitrarias definidas con `textPath=`.

## Propiedades {#section-a289dc26b6534b41998b1e241d5f2f92}

Atributo de capa. Se aplica a `layer=0` if `layer=comp`. Exclusivo de forma mutua con `src=` y `text=` en la misma capa. La última incidencia de `text=`, `textPs=`, y `src=` prevalece y determina si se trata de una imagen o de una capa de texto. Ignorado por las capas de efecto.

## Predeterminado {#section-11c2ae2c96d64a0a9c207252df663e4d}

Ninguno.

## Véase también {#section-5c2b25767d2b47b5be817271ab12e13c}

[Formato de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
