---
description: Extender capa. Agrega márgenes a una capa o recorta el rectángulo de la capa.
solution: Experience Manager
title: extender
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# extender{#extend}

Extender capa. Agrega márgenes a una capa o recorta el rectángulo de la capa.

`extend= *`left`*, *`top`*, *`derecha`*, *`bottom`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> izquierda, arriba, abajo, derecha</span></span> </p></td> 
  <td class="stentry"> <p>Número de píxeles que se van a agregar (o quitar de, si el valor es negativo) al borde izquierdo, superior, derecho e inferior de la capa recta (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>Cantidad de espacio para añadir (o eliminar, si el valor es negativo) el borde izquierdo, superior, derecho e inferior de la capa recta, expresada como cantidades normalizadas en relación con el tamaño de la capa recta original (real, real, real, real). </p></td> 
 </tr> 
</table>

`extend=` se aplica a la capa *después* la imagen se recorta ( `crop=`) y todas las transformaciones de capa, incluyendo `rotate=`, se han aplicado.

El área extendida está llena de `bgColor=`, o, si no se especifica, permanece transparente.

Valores de argumento para `extendN=` se normalizan en relación con el tamaño de la capa recta después de las transformaciones de capa, lo que incluye `rotate=` se han aplicado.

## Propiedades {#section-8fc94de871f841f3bf5e1df135972ca9}

Atributo de capa. Se aplica a la capa 0 si `layer=comp`. Ignorado por las capas de efecto.

## Predeterminado {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, para que no se produzca ningún cambio en el rectángulo de capa.

## Ejemplos {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Recorte una imagen y, a continuación, añada un borde rojo de 5 píxeles de ancho:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Escale una imagen a una anchura de 200 píxeles y añada texto de título a un margen de 30 píxeles por encima de la imagen.**

Tenga en cuenta que la altura de la imagen compuesta varía en función de la relación de aspecto de la imagen.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Véase también {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
