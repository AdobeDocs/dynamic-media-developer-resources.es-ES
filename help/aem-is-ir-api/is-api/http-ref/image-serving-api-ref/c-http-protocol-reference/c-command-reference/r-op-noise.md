---
description: Añada ruido. Añade ruido aleatorio a los datos de imagen de primer plano o al primer plano de una capa de efecto.
solution: Experience Manager
title: op_sound
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 1%

---

# op_sound{#op-noise}

Añada ruido. Añade ruido aleatorio a los datos de imagen de primer plano o al primer plano de una capa de efecto.

`op_noise= *`val`*[,uniform|gaussian[, *`monocromo`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Cantidad de ruido en porcentaje (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Seleccione una distribución uniforme del ruido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussiano</span> </p> </td> 
   <td colname="col2"> <p>Seleccione la distribución del ruido gaussiano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monocromo</span> </p> </td> 
   <td colname="col2"> <p>Defina en 0 para el ruido de color y en 1 para el ruido gris. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* se ignora en las imágenes en escala de grises.

## Propiedades {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`.

## Predeterminado {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, para que no haya ruido.
