---
description: Máscara de imagen. Especifica una imagen de máscara independiente que se utilizará como máscara no asociada.
seo-description: Máscara de imagen. Especifica una imagen de máscara independiente que se utilizará como máscara no asociada.
seo-title: máscara
solution: Experience Manager
title: máscara
topic: Scene7 Image Serving - Image Rendering API
uuid: 2dc14d20-f02a-4a77-9b73-0c01e10d448d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# mask{#mask}

Máscara de imagen. Especifica una imagen de máscara independiente que se utilizará como máscara no asociada.

`mask= *``*|{[is|ir]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objeto</span> </p></td> 
  <td class="stentry"> <p>Objeto de imagen que se va a utilizar como imagen o máscara de capa. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Servicio de imágenes anidado, Representación de imágenes o solicitud externa. </p></td> 
 </tr> 
</table>

*`object`* puede ser una entrada de catálogo o un archivo de imagen/SVG. Se puede especificar para capas de imagen y capas de color sólido.

Si *`object`* se resuelve en una entrada de catálogo de imágenes, `catalog::MaskPath` se utiliza o, si no `catalog::MaskPath` se define, `catalog::Path` se utiliza. Si *`object`* no se resuelve en una entrada de catálogo, se interpreta como una ruta de archivo.

En todos los casos, si la imagen de origen tiene un canal alfa, se utiliza. De lo contrario, la imagen se convierte a escala de grises, si es necesario, antes de utilizarse como máscara de capa.

Si una máscara está conectada a una capa de color sólido, se puede recortar y escalar con las mismas reglas que se usan para las imágenes de las capas de imagen. `size=`, `scale=`, o `res=` puede utilizarse para escalar la máscara.

Las máscaras de capa también se pueden especificar en forma de *`nestedRequest`*. Las solicitudes anidadas o incrustadas se encierran entre llaves. Prefijo una solicitud de servicio de imágenes incrustada con `is` y una solicitud de procesamiento de imágenes incrustada con `ir`. Se asume una solicitud a un servidor externo si no se especifica ningún prefijo. Consulte Anidación y incrustación [de solicitudes](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) para obtener más información.

## Propiedades {#section-a093043dc249423b8ae322cefb0d545d}

Imagen o atributo de capa. Se aplica a la capa 0 si `layer=comp`. Omitido por capas de efectos.

*`object`* no debe resolverse en un registro de catálogo que incluya un `src=` o un `mask=` comando en `catalog::Modifier`.

Los prefijos `is` y `ir` no distinguen entre mayúsculas y minúsculas.

## Predeterminado {#section-10cf793c665f49deb1b248faa3b618a9}

Si no `mask=` se especifica explícitamente y la imagen de capa está asociada a una entrada de catálogo, se `catalog::MaskPath` utiliza. De lo contrario, se utilizará el canal alfa de la imagen de capa, si está presente. Si no hay ningún canal alfa, la capa no tiene máscara y el rectángulo de la capa se representa completamente opaco.

## Ejemplo {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Utilice varias máscaras independientes para colorear diferentes áreas de una imagen. Las regiones coloreadas y enmascaradas se colocan en capas sobre la imagen original sin modificar:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Véase también {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catálogo::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , Anidación y incrustación [de solicitudes](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
