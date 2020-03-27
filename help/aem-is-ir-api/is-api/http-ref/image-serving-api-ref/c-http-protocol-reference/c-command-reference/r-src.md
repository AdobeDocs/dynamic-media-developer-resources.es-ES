---
description: Imagen de capa.
seo-description: Imagen de capa.
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# src{#src}

Imagen de capa.

` src= *``*|{[is|ir|fxg]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> objeto </span> </p> </td> 
  <td class="stentry"> <p>Objeto de imagen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>Servicio de imágenes anidado, Representación de imágenes o solicitud externa. </p> </td> 
 </tr> 
</table>

## Descripción {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Especifica la imagen de origen de una capa de imagen.

*`object`* puede ser una entrada de catálogo o un archivo de imagen/SVG.

Consulte [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Las solicitudes anidadas o incrustadas se encierran entre llaves. Prefijo una solicitud de servicio de imágenes incrustada con `is`, una solicitud de procesamiento de imágenes incrustada con `ir`y una solicitud de procesamiento de gráficos FXG con `fxg`. Se asume una solicitud a un servidor externo si no se especifica ningún prefijo.

Consulte Anidación e incrustación [de solicitudes](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

>[!NOTE]
>
>La representación de gráficos FXG solo está disponible en el entorno alojado de Scene7 y puede requerir licencias adicionales. Póngase en contacto con la asistencia de Scene7 para obtener más información.

## Propiedades {#section-2c22bb89a35d470f833df8ba898efd93}

Atributo de capa. Se aplica a `layer=0` if `layer=comp`. Mutuamente exclusiva con `text=` y `textPs=` en la misma capa; la última incidencia de `text=`, `textPs=`o `src=` prevalece y determina si es una imagen o una capa de texto. Omitido por capas de efectos.

*`object`*no se puede resolver en otro registro de catálogo que incluya un `src=` o `mask=` comando en su `catalog::Modifier`. (Utilice el anidado de solicitudes para lograr un efecto similar).

Los prefijos `is`, `ir`y `fxg` distinguen entre mayúsculas y minúsculas.

## Predeterminado {#section-a92f3882041b4d43ae2caf014647165f}

Para la capa 0, se utiliza el objeto del componente de ruta de la URL si no `src=` se especifica. No hay ningún valor predeterminado para otras capas.

## Véase también {#section-e467e03330564796932ac081f1c9c1d0}

[catálogo::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)[object, plantillasAnidación e incrustación de solicitudes](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
