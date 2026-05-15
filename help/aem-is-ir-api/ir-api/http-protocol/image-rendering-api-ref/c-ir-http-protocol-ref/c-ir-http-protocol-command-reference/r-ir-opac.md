---
title: opaco
description: Opacidad. Especifica la opacidad del material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
TQID: 'https://experienceleague.adobe.com/j4Y-Lk-BL8VybOYqbP256D81w8FFbQqdS0q8z6Y5l1c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 0%

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

Si el material incluye una imagen con un canal alfa, `opac=` se puede usar para hacer la imagen más transparente, pero no más opaca.

## Propiedades {#section-352f7b82ede54159b6afb90ae4b559ec}

Atributo de material. Se ignora si la selección de objeto actual o el material no admiten opacidad.

## Predeterminado {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, para un material completamente opaco (si la imagen no incluye un canal alfa).
