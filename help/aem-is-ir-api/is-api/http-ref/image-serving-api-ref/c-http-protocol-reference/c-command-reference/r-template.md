---
description: Plantilla de composición. Permite especificar una plantilla de composición ubicada en un catálogo que no sea el catálogo principal.
solution: Experience Manager
title: plantilla
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 6%

---

# plantilla{#template}

Plantilla de composición. Permite especificar una plantilla de composición en un catálogo que no sea el catálogo principal.

`template= *`plantilla`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objeto</span> </p> </td> 
  <td class="stentry"> <p>Plantilla. </p></td> 
 </tr> 
</table>

*`template`* debe ser una entrada de catálogo de imágenes con el cuerpo de plantilla contenido en  `catalog::Modifier`.

Cuando `template=` está presente, el objeto especificado en la ruta de solicitud no se aplica como origen para la capa 0. Sin embargo, se puede hacer referencia a él como `src=` o `mask=` en cualquier parte de la plantilla mediante la variable de ruta predefinida `$object$` como valor `src=`. `catalog::Modifier` del objeto especificado en la ruta de solicitud solo se aplica con la sustitución de  `$object$` dentro de la plantilla, mientras que siempre  `catalog::PostModifier` se aplica.

La capa 0 se define en el cuerpo de la plantilla y puede ser una imagen, color sólido, texto o una capa de solicitud anidada o incrustada.

`catalog:PostModifier` of  *`object`* se ignora cuando  *`object`* se utiliza con  `template=`.

## Predeterminado {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Ninguno.

## Propiedades {#section-daf3afb1d09c45a6a394468d0874c439}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual.

## Ejemplo {#section-9a4f260ed43342b186b0fe855f34bca6}

Consulte los ejemplos en [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Véase también {#section-067587444f774469931ecafd5a39834c}

[objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), variable de ruta  [predefinida](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
