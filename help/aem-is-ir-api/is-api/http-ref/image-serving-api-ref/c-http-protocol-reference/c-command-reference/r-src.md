---
description: Imagen de capa.
solution: Experience Manager
title: src
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# src{#src}

Imagen de capa.

` src= *`objeto`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> objeto </span> </p> </td> 
  <td class="stentry"> <p>Objeto de imagen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>Servicio de imágenes anidado, procesamiento de imágenes o solicitud externa. </p> </td> 
 </tr> 
</table>

## Descripción {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Especifica la imagen de origen de una capa de imagen.

*`object`* puede ser una entrada de catálogo o un archivo de imagen/SVG.

Consulte [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Las solicitudes anidadas o incrustadas están encerradas entre llaves. Agregue a una solicitud de servicio de imágenes incrustada el prefijo `is`, una solicitud de procesamiento de imágenes incrustada con `ir`y una solicitud de procesamiento de gráficos FXG con `fxg`. Si no se especifica ningún prefijo, se asume una solicitud a un servidor externo.

Consulte [Solicitar anidamiento e incrustación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Propiedades {#section-2c22bb89a35d470f833df8ba898efd93}

Atributo de capa. Se aplica a `layer=0` if `layer=comp`. Exclusivo de forma mutua con `text=` y `textPs=` en la misma capa; la última aparición de cualquiera de las dos `text=`, `textPs=`, o `src=` prevalece y determina si se trata de una imagen o de una capa de texto. Ignorado por las capas de efecto.

*`object`* no se puede resolver en otro registro de catálogo que incluya un `src=` o `mask=` comando en su `catalog::Modifier`. (Utilice el anidamiento de solicitudes para lograr un efecto similar).

El `is`, `ir`, y `fxg` Los prefijos distinguen entre mayúsculas y minúsculas.

## Predeterminado {#section-a92f3882041b4d43ae2caf014647165f}

Para la capa 0, se utiliza el objeto del componente de ruta de la dirección URL si `src=` no especificado. No hay ningún valor por defecto para otras capas.

## Véase también {#section-e467e03330564796932ac081f1c9c1d0}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Solicitar anidamiento e incrustación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
