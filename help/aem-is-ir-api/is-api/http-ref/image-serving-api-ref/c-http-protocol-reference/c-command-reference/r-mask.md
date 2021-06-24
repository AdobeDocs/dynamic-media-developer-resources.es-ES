---
description: Máscara de imagen. Especifica una imagen de máscara independiente que se utilizará como máscara no asociada.
solution: Experience Manager
title: mask
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 1%

---

# mask{#mask}

Máscara de imagen. Especifica una imagen de máscara independiente que se utilizará como máscara no asociada.

`mask= *``*|{[is|ir]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objeto</span> </p></td> 
  <td class="stentry"> <p>Objeto de imagen que se utilizará como imagen o máscara de capa. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Servidor de imágenes anidado, renderización de imágenes o solicitud externa. </p></td> 
 </tr> 
</table>

*`object`* puede ser una entrada de catálogo o un archivo de imagen/SVG. Se puede especificar para capas de imagen y capas de color sólido.

Si *`object`* se resuelve en una entrada de catálogo de imágenes, se utiliza `catalog::MaskPath` o, si `catalog::MaskPath` no está definido, se utiliza `catalog::Path`. Si *`object`* no se resuelve en una entrada de catálogo, se interpreta como una ruta de archivo.

En todos los casos, si la imagen de origen tiene un canal alfa, se utiliza. De lo contrario, la imagen se convierte a escala de grises, si es necesario, antes de utilizarse como máscara de capa.

Si una máscara está unida a una capa de color sólido, se puede recortar y escalar utilizando las mismas reglas utilizadas para las imágenes en capas de imagen. `size=`,  `scale=`, o  `res=` pueden utilizarse para escalar la máscara.

Las máscaras de capa también se pueden especificar en forma de *`nestedRequest`*. Las solicitudes anidadas o incrustadas se encierran entre llaves. Agregue a una solicitud de Image Serving incrustada el prefijo `is` y a una solicitud de procesamiento de imágenes incrustada `ir`. Se asume una solicitud a un servidor externo si no se especifica ningún prefijo. Consulte [Anidado de solicitudes e Incrustación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) para obtener más información.

## Propiedades {#section-a093043dc249423b8ae322cefb0d545d}

Imagen o atributo de capa. Se aplica a la capa 0 si `layer=comp`. Ignorado por capas de efecto.

*`object`* no debe resolver en un registro de catálogo que incluya un  `src=` comando o  `mask=` en  `catalog::Modifier`.

Los prefijos `is` y `ir` no distinguen entre mayúsculas y minúsculas.

## Predeterminado {#section-10cf793c665f49deb1b248faa3b618a9}

Si `mask=` no se especifica explícitamente y si la imagen de capa está asociada con una entrada de catálogo, se utiliza `catalog::MaskPath`. De lo contrario, se utiliza el canal alfa de la imagen de capa, si está presente. Si no hay ningún canal alfa, la capa no tiene máscara y el rectángulo de la capa se representa completamente opaco.

## Ejemplo {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Utilice varias máscaras independientes para colorear diferentes áreas de una imagen. Las regiones coloreadas y enmascaradas están en capas sobre la imagen original sin modificar:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Véase también {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) ,  [catálogo::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) ,  [Solicitud de anidación e Incrustación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
