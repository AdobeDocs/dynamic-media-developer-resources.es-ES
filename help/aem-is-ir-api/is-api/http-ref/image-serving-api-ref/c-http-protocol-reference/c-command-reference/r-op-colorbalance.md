---
title: op_colorbalance
description: Ajuste el equilibrio de color. Ajusta el valor de cada componente de color de RGB por separado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
TQID: 'https://experienceleague.adobe.com/etLnTD-hMe5kOnvak7n47O0XwOWvqtC5av4FkYZpaGI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 1%

---

# op_colorbalance{#op-colorbalance}

Ajuste el equilibrio de color. Ajusta el valor de cada componente de color de RGB por separado.

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

Los datos de imagen de entrada de gris y CMYK se convierten a RGB mediante conversión naive, que no es precisa cuando la administración de color está habilitada.

## Propiedades {#section-dff9c934f7c1442bbd02379b688d82e2}

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por las capas de efecto. Las imágenes y las capas CMYK se convierten a RGB antes de que se aplique la operación.

## Predeterminado {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` para que no haya cambios en los colores.

## Ejemplo {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Empuje el balance de color hacia el rojo:

... `&op_colorBalance=100,0,0&`...
