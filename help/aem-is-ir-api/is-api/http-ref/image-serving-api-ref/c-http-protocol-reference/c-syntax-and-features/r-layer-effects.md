---
description: Los efectos de sombra y resplandor de capa de estilo Photoshop se implementan utilizando subcapas especiales (capas de efecto) que pueden acoplarse a cualquier capa (la capa principal), incluidas layer=0 y layer=comp.
seo-description: Los efectos de sombra y resplandor de capa de estilo Photoshop se implementan utilizando subcapas especiales (capas de efecto) que pueden acoplarse a cualquier capa (la capa principal), incluidas layer=0 y layer=comp.
seo-title: Efectos de capa
solution: Experience Manager
title: Efectos de capa
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 076e98de-cbbb-457b-984a-367a935b4356
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 2%

---


# Efectos de capa{#layer-effects}

Los efectos de sombra y resplandor de capa de estilo Photoshop se implementan utilizando subcapas especiales (capas de efecto) que pueden acoplarse a cualquier capa (la capa principal), incluidas layer=0 y layer=comp.

Aunque las capas de efecto admiten una serie de comandos y atributos de capa y de imagen estándar, no están pensadas para ser capas de uso general y no admiten datos de imagen o texto independientes.

Se puede asociar cualquier número de efectos de capa a una sola capa principal.

## Efectos interiores y exteriores {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Los* efectos interiores se representan sobre la capa principal y solo se ven en áreas opacas de la capa principal. *Los* efectos exteriores se representan detrás de la capa principal (por lo tanto, nunca serán visibles dentro de las áreas opacas de la capa principal) y se pueden colocar en cualquier lugar dentro del lienzo de composición. Se elige un efecto interior o exterior asignando un número de capa de efecto positivo o negativo con el comando `effect=`. El comando `effect=` también controla el orden z entre varias capas de efecto conectadas a la misma capa principal.

## Relación con la capa principal {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Las capas de efecto cambian de tamaño y se colocan automáticamente para que coincidan con la capa principal (es decir, la capa de efecto hereda los valores `size=` y `origin=` de la capa principal). `pos=` puede utilizarse para desplazar la capa de efecto de la capa principal, como suele ser necesario para los efectos de sombra interiores y de colocación. Mientras que para las capas estándar `pos=` especifica un desplazamiento entre los orígenes de esta capa y la capa 0, para las capas de efecto `pos=` especifica el desplazamiento entre los orígenes de la capa de efecto y la capa principal.

## Comandos y atributos admitidos {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

Las capas de efectos aceptan los siguientes comandos y atributos:

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

Se omiten todos los demás comandos de imagen y capa contenidos en las capas de efecto.

## Macros de efectos predeterminados {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Para facilitar el uso de los efectos de capa, IS proporciona dos macros con el catálogo de imágenes predeterminado, `$shadow$` y `$glow$`, que proporcionan valores predeterminados para los atributos de capa de efecto que son similares a los efectos de capa de Photoshop. Las siguientes listas de tabla que afectan al comando y a la macro deben utilizarse para implementar los efectos de capa predeterminados. Naturalmente, cualquiera de los atributos especificados en las macros se puede modificar en la dirección URL o se pueden crear macros alternativas para implementar efectos de capa personalizados.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Efecto deseado</b> </th> 
   <th class="entry"> <b> Comando</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Sombra paralela </p> </td> 
   <td> <p> <span class="codeph"> efecto=-1&amp;$sombra$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Sombra interior </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$Shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Resplandor externo </p> </td> 
   <td> <p> <span class="codeph"> efecto=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Resplandor interior </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplos {#section-4c449fdf707b43858917fb271fa1fe96}

Añada un borde rojo de tres píxeles de ancho con un 50 % de opacidad en una capa:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

El borde seguirá los contornos del canal alfa o la máscara de la imagen. Si se establece `effect=1` se coloca el borde en el borde interior.

Añada una sombra paralela azulada en una imagen mediante la configuración predeterminada del efecto (excepto el color):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` agrega un pequeño margen a los bordes inferiores derecho de la imagen, lo que evita que la sombra paralela se recorte a los límites de la imagen.

## Véase también {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135),  [Macros de comando%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
