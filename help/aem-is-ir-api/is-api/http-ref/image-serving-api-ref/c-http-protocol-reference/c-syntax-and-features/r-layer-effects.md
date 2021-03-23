---
description: Los efectos de sombra y resplandor de capa de estilo Photoshop se implementan utilizando subcapas especiales (capas de efecto) que pueden adjuntarse a cualquier capa (la capa principal), incluidas la capa=0 y la capa=comp.
seo-description: Los efectos de sombra y resplandor de capa de estilo Photoshop se implementan utilizando subcapas especiales (capas de efecto) que pueden adjuntarse a cualquier capa (la capa principal), incluidas la capa=0 y la capa=comp.
seo-title: Efectos de capa
solution: Experience Manager
title: Efectos de capa
uuid: 076e98de-cbbb-457b-984a-367a935b4356
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---


# Efectos de capa{#layer-effects}

Los efectos de sombra y resplandor de capa de estilo Photoshop se implementan utilizando subcapas especiales (capas de efecto) que pueden adjuntarse a cualquier capa (la capa principal), incluidas la capa=0 y la capa=comp.

Aunque las capas de efecto admiten una serie de atributos y comandos estándar de imagen y capa, no están pensados para ser capas de uso general y no admiten imágenes o datos de texto independientes.

Cualquier cantidad de efectos de capa se puede asociar a una sola capa principal.

## Efectos interiores y exteriores {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Los* efectos internos se representan sobre la capa principal y solo son visibles en áreas opacas de la capa principal. *Los* efectos externos se representan detrás de la capa principal (por lo que nunca serán visibles dentro de áreas opacas de la capa principal) y se pueden colocar en cualquier lugar dentro del lienzo de composición. Se elige un efecto interno o externo asignando un número de capa de efecto positivo o negativo con el comando `effect=`. El comando `effect=` también controla el orden z entre varias capas de efecto conectadas a la misma capa principal.

## Relación con la capa principal {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Las capas de efecto cambian de tamaño automáticamente y se colocan para que coincidan con la capa principal (es decir, la capa de efecto hereda los valores `size=` y `origin=` de la capa principal). `pos=` puede utilizarse para desplazar la capa de efecto de la capa principal, como suele ser necesario para los efectos de caída y sombra interna. Mientras que para las capas estándar `pos=` especifica un desplazamiento entre los orígenes de esta capa y la capa 0, para las capas de efecto `pos=` especifica el desplazamiento entre los orígenes de la capa de efecto y la capa principal.

## Comandos y atributos admitidos {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

Las capas de efecto aceptan los siguientes comandos y atributos:

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

Todos los demás comandos de imagen y capa contenidos en las capas de efecto se ignoran.

## Macros de efectos predeterminados {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Para facilitar el uso de los efectos de capa, IS proporciona dos macros con el catálogo de imágenes predeterminado, `$shadow$` y `$glow$`, que proporcionan valores predeterminados para los atributos de capa de efecto que son similares a los efectos de capa de Photoshop. La siguiente tabla enumera qué comando de efecto y macro deben usarse para implementar los efectos de capa predeterminados. Naturalmente, cualquiera de los atributos especificados en las macros se puede modificar en la URL, o se pueden crear macros alternativas para implementar efectos de capa personalizados.

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
   <td> <p> <span class="codeph"> efecto=-1&amp;$Shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Sombra interior </p> </td> 
   <td> <p> <span class="codeph"> efecto=1&amp;$Shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Resplandor externo </p> </td> 
   <td> <p> <span class="codeph"> efecto=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Resplandor interior </p> </td> 
   <td> <p> <span class="codeph"> efecto=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplos {#section-4c449fdf707b43858917fb271fa1fe96}

Añada un borde rojo de tres píxeles de ancho con un 50% de opacidad a una capa:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

El borde seguirá los contornos del canal alfa o la máscara de la imagen. Si se establece `effect=1`, el borde se colocaría en el borde interior.

Agregue una sombra paralela azulada a una imagen mediante la configuración de efecto predeterminada (excepto el color):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` añade un pequeño margen a los bordes inferiores derechos de la imagen, lo que evita que la sombra se recorte a los límites de la imagen.

## Véase también {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135),  [Macros de comandos%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
