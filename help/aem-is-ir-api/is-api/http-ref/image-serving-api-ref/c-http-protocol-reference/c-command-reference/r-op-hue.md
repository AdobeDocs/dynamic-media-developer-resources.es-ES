---
title: op_hue
description: Ajusta el tono de la imagen. Desplaza el tono de cada píxel visible de la capa o imagen compuesta en la cantidad especificada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
TQID: 'https://experienceleague.adobe.com/6VSkHDcXsf531qB6okDvLt-xIyFoiw-fG3Z11a-Ne5g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
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

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por las capas de efecto. Las imágenes o capas CMYK se convierten a RGB antes de que se aplique la operación.

## Predeterminado {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, sin cambio de tono.
