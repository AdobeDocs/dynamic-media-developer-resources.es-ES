---
title: Efectos de capa
description: Los efectos de sombra y resplandor de capas de estilo Photoshop se implementan utilizando subcapas especiales (capas de efecto) que se pueden unir a cualquier capa (la capa principal), incluidas capa=0 y capa=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 2%

---

# Efectos de capa{#layer-effects}

Los efectos de sombra y resplandor de capas de estilo Photoshop se implementan utilizando subcapas especiales (capas de efecto) que se pueden unir a cualquier capa (la capa principal), incluidas capa=0 y capa=comp.

Aunque las capas de efectos admiten una serie de atributos y comandos de imagen y capa estándar, no están pensadas para ser capas de uso general y no admiten datos de texto o imagen independientes.

Se puede adjuntar cualquier número de efectos de capa a una sola capa principal.

## Efectos internos y externos {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Los efectos internos* se representan sobre la capa principal y sólo son visibles en las áreas opacas de la capa principal. *Los efectos externos* se representan detrás de la capa principal (por lo que nunca son visibles dentro de las áreas opacas de la capa principal) y se pueden colocar en cualquier lugar dentro del lienzo de composición. Un efecto interior o exterior se elige asignando un número de capa de efecto positivo o negativo con el comando `effect=`. El comando `effect=` también controla el orden Z entre varias capas de efectos conectadas a la misma capa principal.

## Relación con la capa principal {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Las capas de efectos se dimensionan automáticamente y se colocan para que coincidan con la capa principal (es decir, la capa de efecto hereda los valores `size=` y `origin=` de la capa principal). `pos=` se puede usar para desplazar la capa de efecto fuera de la capa principal, como suele ser necesario para los efectos de sombra y sombra interna. Mientras que para las capas estándar `pos=` especifica un desplazamiento entre los orígenes de esta capa y la capa 0, para las capas de efecto `pos=` especifica el desplazamiento entre los orígenes de la capa de efecto y la capa principal.

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

Todos los demás comandos de imagen y capa contenidos en las capas de efecto se ignoran.

## Macros de efectos predeterminados {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Para facilitar el uso de efectos de capa, IS proporciona dos macros con el catálogo de imágenes predeterminado, `$shadow$` y `$glow$`, que proporcionan valores predeterminados para atributos de capa de efecto similares a los efectos de capa de Photoshop. En la tabla siguiente se enumeran los comandos de efectos y las macros que deben utilizarse para implementar los efectos de capa predeterminados. Naturalmente, cualquiera de los atributos especificados en las macros se puede modificar en la dirección URL o se pueden crear macros alternativas para implementar efectos de capa personalizados.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> efecto deseado</b> </th> 
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
   <td> <p> <span class="codeph"> efecto=1&amp;$sombra$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Resplandor externo </p> </td> 
   <td> <p> <span class="codeph"> efecto=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Resplandor interior </p> </td> 
   <td> <p> <span class="codeph"> efecto=1&amp;$resplandor$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplos {#section-4c449fdf707b43858917fb271fa1fe96}

Añada un borde rojo de tres píxeles de ancho con una opacidad del 50 % a una capa:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

El borde sigue los contornos del canal alfa o la máscara de la imagen. La configuración `effect=1` colocaría el borde en el borde interior en su lugar.

Agregar una sombra paralela azulada a una imagen con los ajustes de efecto predeterminados (excepto el color):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` agrega un pequeño margen a los bordes inferiores derechos de la imagen, lo que evita que la sombra paralela se recorte a los límites de la imagen.

## Véase también {#section-1acccccf534549aea23d4c008c17e7c0}

[efecto=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [Macros de comandos%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
