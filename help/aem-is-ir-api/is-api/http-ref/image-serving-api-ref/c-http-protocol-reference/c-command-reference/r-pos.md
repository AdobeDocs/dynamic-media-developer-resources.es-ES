---
description: Posición de la capa.
solution: Experience Manager
title: pos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

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
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Desplazamiento normalizado desde el origen de esta capa hasta el origen de la capa 0 (real, real). </p></td> 
 </tr> 
</table>

En el caso de las capas de imagen, texto y color sólido, `pos=` especifica la posición de un anclaje de capa en relación con el anclaje de capa 0. `posN=` los valores de coordenadas se normalizan en relación con el tamaño real de la capa 0 rect.

En el caso de capas de efecto, `pos=` desplaza la capa de efecto en relación con la capa principal.

Los valores positivos mueven la capa hacia la derecha/abajo, los negativos hacia la izquierda/arriba. `posN=0.5,0.5` mueve la capa a la mitad de la anchura y altura de la capa 0 hacia abajo y hacia la derecha.

## Propiedades {#section-51a60cdc52d040538fef378ace7c2e7d}

Atributo de capa. Ignorado si `layer=0` o `layer=comp`.

## Predeterminado {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Esto coloca el anclaje de la capa en la misma ubicación que el anclaje de la capa 0 si se trata de una capa de imagen, texto o color sólido. Coloca una capa de efecto directamente encima o debajo de su capa principal.

## Ejemplo {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Consulte el Ejemplo A en [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Véase también {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
