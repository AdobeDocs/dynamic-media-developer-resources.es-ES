---
description: Opacidad. Especifica la opacidad del material.
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

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
