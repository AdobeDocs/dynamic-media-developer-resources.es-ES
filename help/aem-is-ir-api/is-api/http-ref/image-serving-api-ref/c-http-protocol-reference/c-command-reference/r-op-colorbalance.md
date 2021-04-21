---
description: Ajuste el equilibrio de color. Ajusta el valor de cada componente de color RGB por separado.
solution: Experience Manager
title: op_colorbalance
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '120'
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
  <td class="stentry"> <p>Ajuste de componentes verdes (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste del componente azul (-100...+100 int). </p></td> 
 </tr> 
</table>

Los datos de imagen de entrada en gris y CMYK se convierten a RGB mediante conversión nativa, lo que no es exacto cuando la gestión del color está habilitada.

## Propiedades {#section-dff9c934f7c1442bbd02379b688d82e2}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por capas de efecto. Las imágenes y capas CMYK se convierten a RGB antes de aplicar la operación.

## Predeterminado {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` sin ningún cambio en los colores.

## Ejemplo {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Empuje el balance de color hacia el rojo:

... `&op_colorBalance=100,0,0&`...
