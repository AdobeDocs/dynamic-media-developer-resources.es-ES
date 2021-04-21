---
description: Ajustar tono. Cambia el tono de cada píxel visible de la capa o imagen compuesta por la cantidad especificada.
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 2%

---


# op_hue{#op-hue}

Ajustar tono. Cambia el tono de cada píxel visible de la capa o imagen compuesta por la cantidad especificada.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste del tono en grados (-180...+180 int). </p></td> 
 </tr> 
</table>

Basado en un rango de matiz de 360 grados.

## Propiedades {#section-55779644700b4c808a624cdf5a04447e}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por capas de efecto. Las imágenes o capas CMYK se convierten a RGB antes de aplicar la operación.

## Predeterminado {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, sin ningún cambio en el tono.
