---
description: Opacidad. Especifica la opacidad del material.
seo-description: Opacidad. Especifica la opacidad del material.
seo-title: opac
solution: Experience Manager
title: opac
uuid: 0f5b11f0-af65-4abd-947e-7a28cb8de263
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# opac{#opac}

Opacidad. Especifica la opacidad del material.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>opacidad del material (porcentaje); 0...100 </p> </td> 
 </tr> 
</table>

Las siguientes combinaciones de materiales y objetos admiten la opacidad de las variables:

* Color sólido y texturas repetibles aplicadas a objetos de superposición texturables.
* Materiales de recubrimiento de ventanas aplicados a objetos de marco de recubrimiento de ventanas.
* Decales aplicados a objetos texturables o de pared.

Si el material incluye una imagen con un canal alfa, `opac=` puede utilizarse para hacer la imagen más transparente, pero no más opaca.

## Propiedades {#section-352f7b82ede54159b6afb90ae4b559ec}

Atributo de material. Se omite si la selección de objeto actual o el material no admiten opacidad.

## Predeterminado {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, para un material totalmente opaco (si la imagen no incluye un canal alfa).
