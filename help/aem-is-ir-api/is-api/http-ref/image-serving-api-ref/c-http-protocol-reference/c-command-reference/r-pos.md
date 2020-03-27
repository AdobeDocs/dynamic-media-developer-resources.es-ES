---
description: Posición de la capa.
seo-description: Posición de la capa.
seo-title: pos
solution: Experience Manager
title: pos
topic: Scene7 Image Serving - Image Rendering API
uuid: e9872ce9-5c47-49c5-9c87-4fa8441c4770
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pos{#pos}

Posición de la capa.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento de píxeles desde el origen de esta capa hasta el origen de la capa 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codeN</span> </p></td> 
  <td class="stentry"> <p>Desplazamiento normalizado desde el origen de esta capa hasta el origen de la capa 0 (real, real). </p></td> 
 </tr> 
</table>

En el caso de las capas de imagen, texto y color sólido, `pos=` especifica la posición de un anclaje de capa en relación con el anclaje de capa 0. `posN=` los valores de las coordenadas se normalizan en relación con el tamaño real de la capa 0 rect.

En el caso de las capas de efecto, desplaza la capa de efecto en relación con la capa principal. `pos=`

Los valores positivos mueven la capa hacia la derecha/abajo, en negativo hacia la izquierda/arriba. `posN=0.5,0.5` mueve la capa la mitad de la capa 0 de anchura y altura hacia abajo y hacia la derecha.

## Propiedades {#section-51a60cdc52d040538fef378ace7c2e7d}

Atributo de capa. Se omite if `layer=0` o `layer=comp`.

## Predeterminado {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Esto coloca el anclaje de capa en la misma ubicación que el anclaje de capa 0 si se trata de una capa de imagen, texto o color sólido. Coloca una capa de efecto directamente sobre la capa principal o debajo de ella.

## Ejemplo {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Consulte Ejemplo A en [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Véase también {#section-812d95575ba542808e8387d0a8650606}

[origen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
