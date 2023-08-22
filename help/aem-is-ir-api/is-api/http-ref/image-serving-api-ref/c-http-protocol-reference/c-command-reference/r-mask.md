---
title: enmascarar
description: Máscara de imagen. Especifica una imagen de máscara independiente que se utilizará como máscara no asociada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 1%

---

# enmascarar{#mask}

Máscara de imagen. Especifica una imagen de máscara independiente que se utilizará como máscara no asociada.

`mask= *`objeto`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objeto</span> </p></td> 
  <td class="stentry"> <p>Objeto de imagen que se utilizará como imagen o máscara de capa. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Servicio de imágenes anidado, procesamiento de imágenes o solicitud externa. </p></td> 
 </tr> 
</table>

*`object`* puede ser una entrada de catálogo o un archivo de imagen/SVG. Se puede especificar para capas de imagen y capas de color sólido.

If *`object`* se resuelve en una entrada del catálogo de imágenes, `catalog::MaskPath` se utiliza, o, si `catalog::MaskPath` no está definida, entonces `catalog::Path` se utiliza. If *`object`* no se resuelve en una entrada de catálogo y, a continuación, se interpreta como una ruta de archivo.

En todos los casos, si la imagen de origen tiene un canal alfa, se utiliza. De lo contrario, la imagen se convierte a escala de grises, si es necesario, antes de utilizarla como máscara de capa.

Si una máscara está conectada a una capa de color sólido, se puede recortar y escalar utilizando las mismas reglas utilizadas para las imágenes en las capas de imagen. `size=`, `scale=`, o `res=` se puede utilizar para escalar la máscara.

Las máscaras de capa también se pueden especificar como *`nestedRequest`*. Las solicitudes anidadas o incrustadas están encerradas entre llaves. Agregue a una solicitud de servicio de imágenes incrustada el prefijo `is` y una solicitud de procesamiento de imágenes incrustada con `ir`. Si no se especifica ningún prefijo, se asume una solicitud a un servidor externo. Consulte [Solicitar anidamiento e incrustación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) para obtener más información.

## Propiedades {#section-a093043dc249423b8ae322cefb0d545d}

Atributo de imagen o capa. Se aplica a la capa 0 si `layer=comp`. Ignorado por las capas de efecto.

*`object`* no debe resolverse en un registro de catálogo que incluya un `src=` o `mask=` command in `catalog::Modifier`.

El `is` y `ir` Los prefijos no distinguen entre mayúsculas y minúsculas.

## Predeterminado {#section-10cf793c665f49deb1b248faa3b618a9}

If `mask=` no se especifica explícitamente y si la imagen de capa está asociada a una entrada de catálogo, `catalog::MaskPath` se utiliza. De lo contrario, se utiliza el canal alfa de la imagen de capa, si está presente. Si no hay canal alfa, la capa no tiene máscara y el rectángulo de la capa se vuelve completamente opaco.

## Ejemplo {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Utilice varias máscaras independientes para colorear diferentes áreas de una imagen. Las regiones coloreadas y enmascaradas se superponen sobre la imagen original sin modificar:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Véase también {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Solicitar anidamiento e incrustación](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
