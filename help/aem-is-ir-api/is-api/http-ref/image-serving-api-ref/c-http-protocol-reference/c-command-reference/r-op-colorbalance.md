---
title: op_colorbalance
description: Ajuste el equilibrio de color. Ajusta el valor de cada componente de color del RGB por separado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---

# op_colorbalance{#op-colorbalance}

Ajuste el equilibrio de color. Ajusta el valor de cada componente de color del RGB por separado.

`op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste de componente rojo (-100...+100 int). </p></td> 
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

Los datos de imagen de entrada de gris y CMYK se convierten en RGB mediante conversión naive, que no es precisa cuando la administración de color está habilitada.

## Propiedades {#section-dff9c934f7c1442bbd02379b688d82e2}

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por las capas de efecto. Las imágenes y las capas CMYK se convierten en RGB antes de que se aplique la operación.

## Predeterminado {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` para que no haya cambios en los colores.

## Ejemplo {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Empuje el balance de color hacia el rojo:

... `&op_colorBalance=100,0,0&`...
