---
description: Opacidad. Especifica la opacidad del material.
seo-description: Opacidad. Especifica la opacidad del material.
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f5b11f0-af65-4abd-947e-7a28cb8de263
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 4%

---


# opac{#opac}

Opacidad. Especifica la opacidad del material.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Opacidad del material (porcentaje); 0...100 </p> </td> 
 </tr> 
</table>

Las siguientes combinaciones de objetos y materiales admiten la opacidad de las variables:

* Colores sólidos y texturas repetibles aplicados a objetos de superposición texturables.
* Materiales de cobertura de ventanas aplicados a objetos de marco de cobertura de ventanas.
* Decales aplicados a objetos texturables u objetos de pared.

Si el material incluye una imagen con un canal alfa, `opac=` puede utilizarse para hacer la imagen más transparente, pero no más opaca.

## Propiedades {#section-352f7b82ede54159b6afb90ae4b559ec}

Atributo Material. Se omite si la selección de objetos actual o el material no admiten opacidad.

## Predeterminado {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, para un material totalmente opaco (si la imagen no incluye un canal alfa).
