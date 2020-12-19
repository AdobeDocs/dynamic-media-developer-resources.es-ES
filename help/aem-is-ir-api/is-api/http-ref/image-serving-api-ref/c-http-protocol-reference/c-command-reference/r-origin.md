---
description: Origen de capas.
seo-description: Origen de capas.
seo-title: origen
solution: Experience Manager
title: origen
topic: Scene7 Image Serving - Image Rendering API
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# origen{#origin}

Origen de capas.

`origin= *`coord`*`

`originN= *`codeN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>Desplazamiento de píxeles desde la esquina superior izquierda del rectángulo de la capa (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codeN</span> </p></td> 
  <td class="stentry"> <p>Desplazamiento normalizado desde el centro de la capa recto (real, real). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>El rect de capa siempre incluye cualquier modificación de `extend=`.

Define el punto de alineación del rectángulo de capa, que se utiliza para colocar el rectángulo de capa en relación con la capa 0 mediante `pos=`. `originN=0,0` coloca el origen de la capa en el centro del rectángulo de la capa. `originN=-0.5,-0.5` y  `origin=0,0` es la esquina superior izquierda y  `originN=0.5,0.5` es la esquina inferior derecha del rectángulo de la capa.

## Propiedades {#section-60f639e36ada43d1abc6bfc100afc925}

Atributo de capa. Se aplica a la capa actual o a la capa 0 si `layer=comp`. No se ven afectadas por las transformaciones de capa ( `crop=`, `scale=`, `rotate=`, `flip=`) aplicadas al origen de capa. Anula `anchor=`. Omitido por capas de efectos.

## Predeterminado {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Si no se especifica `origin=`, el origen de la capa se determina aplicando las transformaciones de la capa al anclaje de la imagen. Si no se conoce el anclaje de imagen, se utiliza el centro del rectángulo de capa ( `originN=0,0`).

## Ejemplo {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Consulte el ejemplo A en [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Véase también {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
