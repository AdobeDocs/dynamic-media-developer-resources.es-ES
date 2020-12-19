---
description: Máscara de enfoque. El enfoque enmascara la capa o la imagen de la vista final, después de todo, si layer=comp.
seo-description: Máscara de enfoque. El enfoque enmascara la capa o la imagen de la vista final, después de todo, si layer=comp.
seo-title: op_usmR
solution: Experience Manager
title: op_usmR
topic: Scene7 Image Serving - Image Rendering API
uuid: 98afd83c-097e-40b4-b0a6-647f70b95fae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# op_usmR{#op-usmr}

Máscara de enfoque. El enfoque enmascara la capa o la imagen de la vista final, después de todo, si layer=comp.

Los parámetros se aplican tal cual, independientemente de si se ha producido un muestreo descendente.

`op_usmR= *``*[, *``*[, *``*[, *`amountRumbralRumbral monocromo`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> cantidad</span></span> </p></td> 
  <td class="stentry"> <p>Factor de intensidad del filtro (real 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>Filtre el radio del núcleo en píxeles (real 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> umbral</span></span> </p></td> 
  <td class="stentry"> <p>Nivel de umbral de filtro (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromo</span></span> </p></td> 
  <td class="stentry"> <p>Establezca en 0 para aplicar a cada componente de color por separado o en 1 para aplicar solo al brillo (intensidad) de la imagen. </p> <p><span class="codeph"> <span class="varname"> los </span></span> monocromos se omiten en las imágenes en escala de grises. </p> </td> 
 </tr> 
</table>

La máscara de capa o la máscara compuesta también se enfocan.

## Propiedades {#section-fb5311b34d164946b74dadb32359518a}

Atributo de capa o atributo de vista. Se aplica a la capa actual o a la imagen de vista final si `layer=comp`. Las capas de efectos lo ignoran.

## Predeterminado {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` sin efecto de máscara de enfoque.

## Véase también {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
