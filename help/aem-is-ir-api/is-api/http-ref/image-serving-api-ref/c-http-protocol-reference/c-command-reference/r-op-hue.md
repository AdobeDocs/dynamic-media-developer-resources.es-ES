---
title: op_hue
description: Ajusta el tono de la imagen. Desplaza el tono de cada píxel visible de la capa o imagen compuesta en la cantidad especificada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# op_hue{#op-hue}

Ajusta el tono de la imagen. Desplaza el tono de cada píxel visible de la capa o imagen compuesta en la cantidad especificada.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de tono en grados (-180...+180 int). </p></td> 
 </tr> 
</table>

Basado en un rango de matices de 360 grados.

## Propiedades {#section-55779644700b4c808a624cdf5a04447e}

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por las capas de efecto. Las imágenes o capas CMYK se convierten en RGB antes de que se aplique la operación.

## Predeterminado {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, para que no haya cambios de tono.
