---
title: opac
description: Opacidad. Especifica la opacidad del material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# opac{#opac}

Opacidad. Especifica la opacidad del material.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>opacidad del material (porcentaje); 0...100 </p> </td> 
 </tr> 
</table>

Las siguientes combinaciones de materiales y objetos admiten la opacidad de las variables:

* Colores sólidos y texturas repetibles aplicados a objetos de superposición textual.
* Materiales de recubrimiento de ventanas aplicados a objetos de marco de recubrimiento de ventanas.
* Decales aplicados a objetos de textura u objetos de pared.

Si el material incluye una imagen con un canal alfa, `opac=` puede utilizarse para hacer la imagen más transparente, pero no más opaca.

## Propiedades {#section-352f7b82ede54159b6afb90ae4b559ec}

Atributo de material. Se omite si la selección de objeto actual o el material no admiten opacidad.

## Predeterminado {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, para un material totalmente opaco (si la imagen no incluye un canal alfa).
