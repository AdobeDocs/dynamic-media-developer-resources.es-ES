---
description: Extender la capa. Añade los márgenes en una capa o recorta el rectángulo de la capa.
seo-description: Extender la capa. Añade los márgenes en una capa o recorta el rectángulo de la capa.
seo-title: extender
solution: Experience Manager
title: extender
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ca69994-e788-41a9-93ac-f22b6b9920d0
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# extender{#extend}

Extender la capa. Añade los márgenes en una capa o recorta el rectángulo de la capa.

`extend= *``*, *``*, *``*, *`izquierdaderecha inferior`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> izquierda,arriba,abajo,derecha</span></span> </p></td> 
  <td class="stentry"> <p>Número de píxeles que se van a añadir (o eliminar, si el valor es negativo) al borde izquierdo, superior, derecho e inferior del rectángulo de la capa (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>Cantidad de espacio para agregar (o quitar, si el valor es negativo) al borde izquierdo, superior, derecho e inferior del rectángulo de capa, expresado como cantidades normalizadas en relación con el tamaño del rectángulo de capa original (real, real, real, real, real). </p></td> 
 </tr> 
</table>

`extend=` se aplica a la capa  ** después de recortar la imagen (  `crop=`) y se han aplicado todas las transformaciones de capa, incluidas  `rotate=`,

El área extendida se rellena con `bgColor=` o, si no se especifica, permanece transparente.

Los valores de argumento para `extendN=` se normalizan en relación con el tamaño del rectángulo de capa después de aplicar las transformaciones de capa, incluyendo `rotate=`.

## Propiedades {#section-8fc94de871f841f3bf5e1df135972ca9}

Atributo de capa. Se aplica a la capa 0 si `layer=comp`. Omitido por capas de efectos.

## Predeterminado {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, para no cambiar el rectángulo de la capa.

## Ejemplos {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Recorte una imagen y, a continuación, agregue un borde rojo de 5 píxeles de ancho:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Ajuste la escala de una imagen a 200 píxeles de ancho y añada texto de título a un margen de 30 píxeles por encima de la imagen.**

Tenga en cuenta que la altura de la imagen compuesta varía en función de la proporción de aspecto de la imagen.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Véase también {#section-2d9572be32ca4602b60920b3810f3638}

[recorte=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [tamaño=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b),  [origen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
