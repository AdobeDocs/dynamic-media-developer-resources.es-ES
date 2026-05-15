---
title: extender
description: Extender capa. Agrega márgenes a una capa o recorta el rectángulo de la capa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
TQID: 'https://experienceleague.adobe.com/9toLDEF2GoV-F5J-lxjswISzwgooS4FwqeGF4Gav0tc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 1%

---

# extender{#extend}

Extender capa. Agrega márgenes a una capa o recorta el rectángulo de la capa.

`extend= *`izquierda`*, *`superior`*, *`derecha`*, *`inferior`*`

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

`extend=` se ha aplicado a la capa *después de* de recortar la imagen (`crop=`) y se han aplicado todas las transformaciones de capa, incluida `rotate=`.

El área extendida está llena con `bgColor=` o, si no se especifica, permanece transparente.

Los valores de argumento de `extendN=` se normalizan en relación con el tamaño de la capa directamente después de aplicar las transformaciones de capa, incluido `rotate=`.

## Propiedades {#section-8fc94de871f841f3bf5e1df135972ca9}

Atributo de capa. Se aplica a la capa 0 si `layer=comp`. Ignorado por las capas de efecto.

## Predeterminado {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, sin cambiar el rectángulo de capa.

## Ejemplos {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Recortar una imagen y, a continuación, agregar un borde rojo de 5 píxeles de ancho:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Escale una imagen a una anchura de 200 píxeles y agregue texto de título a un margen de 30 píxeles por encima de la imagen.**

Tenga en cuenta que la altura de la imagen compuesta varía en función de la relación de aspecto de la imagen.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Véase también {#section-2d9572be32ca4602b60920b3810f3638}

[recorte=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [tamaño=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
