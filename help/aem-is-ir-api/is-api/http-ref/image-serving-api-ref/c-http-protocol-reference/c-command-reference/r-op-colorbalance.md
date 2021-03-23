---
description: Ajuste el equilibrio de color. Ajusta el valor de cada componente de color RGB por separado.
seo-description: Ajuste el equilibrio de color. Ajusta el valor de cada componente de color RGB por separado.
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '134'
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
