---
description: Ajuste el equilibrio de color. Ajusta el valor de cada componente de color RGB por separado.
seo-description: Ajuste el equilibrio de color. Ajusta el valor de cada componente de color RGB por separado.
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
topic: Scene7 Image Serving - Image Rendering API
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# op_colorbalance{#op-colorbalance}

Ajuste el equilibrio de color. Ajusta el valor de cada componente de color RGB por separado.

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste del componente rojo (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste del componente verde (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste del componente azul (-100...+100 int). </p></td> 
 </tr> 
</table>

Los datos de imagen de entrada en gris y CMYK se convierten a RGB mediante conversión nativa, lo que no es exacto cuando la gestión de color está activada.

## Propiedades {#section-dff9c934f7c1442bbd02379b688d82e2}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Omitido por capas de efectos. Las imágenes y capas CMYK se convierten a RGB antes de que se aplique la operación.

## Predeterminado {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` sin cambios en los colores.

## Ejemplo {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Empuje el equilibrio de color hacia el rojo:

... `&op_colorBalance=100,0,0&`...
