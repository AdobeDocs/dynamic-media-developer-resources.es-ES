---
title: opaco
description: Opacidad. Especifica la opacidad del material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# opaco{#opac}

Opacidad. Especifica la opacidad del material.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Opacidad del material (porcentaje); 0...100 </p> </td> 
 </tr> 
</table>

Las siguientes combinaciones de material y objeto admiten opacidad variable:

* Color sólido y texturas repetibles aplicadas a objetos de superposición textural.
* Materiales de revestimiento de ventanas aplicados a objetos de marco de revestimiento de ventanas.
* Calcomanías aplicadas a objetos de textura u objetos de pared.

Si el material incluye una imagen con un canal alfa, `opac=` puede utilizarse para hacer que la imagen sea más transparente, pero no más opaca.

## Propiedades {#section-352f7b82ede54159b6afb90ae4b559ec}

Atributo de material. Se ignora si la selección de objeto actual o el material no admiten opacidad.

## Predeterminado {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, para un material completamente opaco (si la imagen no incluye un canal alfa).
