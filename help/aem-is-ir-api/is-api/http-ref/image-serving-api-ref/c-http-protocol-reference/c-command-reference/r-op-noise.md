---
description: Añada ruido. Agrega ruido aleatorio a los datos de la imagen en primer plano o al primer plano de una capa de efecto.
solution: Experience Manager
title: op_sound
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# op_sound{#op-noise}

Añada ruido. Agrega ruido aleatorio a los datos de la imagen en primer plano o al primer plano de una capa de efecto.

`op_noise= *``*[,uniform|gaussian[, *`valmonrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Cantidad de ruido en porcentaje (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Seleccione una distribución de ruido uniforme. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussiano</span> </p> </td> 
   <td colname="col2"> <p>Seleccione la distribución de ruido gaussiano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monocromo</span> </p> </td> 
   <td colname="col2"> <p>Establézcalo en 0 para ruido de color, 1 para ruido gris. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* se ignora para imágenes en escala de grises.

## Propiedades {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`.

## Predeterminado {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, sin ruido.
