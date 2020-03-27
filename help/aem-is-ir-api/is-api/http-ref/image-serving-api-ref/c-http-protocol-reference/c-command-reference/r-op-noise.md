---
description: Añadir ruido. Añade el ruido aleatorio en los datos de la imagen en primer plano o en el primer plano de una capa de efecto.
seo-description: Añadir ruido. Añade el ruido aleatorio en los datos de la imagen en primer plano o en el primer plano de una capa de efecto.
seo-title: op_sound
solution: Experience Manager
title: op_sound
topic: Scene7 Image Serving - Image Rendering API
uuid: 531f7a94-149b-4090-a163-a1895156250b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_sound{#op-noise}

Añadir ruido. Añade el ruido aleatorio en los datos de la imagen en primer plano o en el primer plano de una capa de efecto.

`op_noise= *``*[,uniform|gaussian[, *`valmonocromo`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Cantidad de ruido en porcentaje (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Seleccione una distribución uniforme de ruido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussiano</span> </p> </td> 
   <td colname="col2"> <p>Seleccione la distribución gaussiana de ruido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monocromo</span> </p> </td> 
   <td colname="col2"> <p>Se establece en 0 para el ruido de color, 1 para el ruido gris. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* se ignora en las imágenes en escala de grises.

## Propiedades {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`.

## Predeterminado {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, sin ruido.
