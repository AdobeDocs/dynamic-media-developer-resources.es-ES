---
description: Ajuste el tono. Cambia el tono de cada píxel visible de la capa o imagen compuesta por la cantidad especificada.
seo-description: Ajuste el tono. Cambia el tono de cada píxel visible de la capa o imagen compuesta por la cantidad especificada.
seo-title: op_hue
solution: Experience Manager
title: op_hue
topic: Scene7 Image Serving - Image Rendering API
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# op_hue{#op-hue}

Ajuste el tono. Cambia el tono de cada píxel visible de la capa o imagen compuesta por la cantidad especificada.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de tono en grados (-180...+180 int). </p></td> 
 </tr> 
</table>

Basado en un rango de tono de 360 grados.

## Propiedades {#section-55779644700b4c808a624cdf5a04447e}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Omitido por capas de efectos. Las imágenes o capas CMYK se convierten a RGB antes de que se aplique la operación.

## Predeterminado {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, sin cambios de tono.
