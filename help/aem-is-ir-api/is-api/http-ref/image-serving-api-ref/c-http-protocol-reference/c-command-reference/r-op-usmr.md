---
description: Máscara de enfoque. El enfoque enmascara la capa o la imagen de vista final, después de todo el escalado, si layer=comp.
solution: Experience Manager
title: op_usmR
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# op_usmR{#op-usmr}

Máscara de enfoque. El enfoque enmascara la capa o la imagen de vista final, después de todo el escalado, si layer=comp.

Los parámetros se aplican tal cual, independientemente de si se ha producido un muestreo descendente.

`op_usmR= *`cantidad`*[, *`radiusR`*[, *`umbral`*[, *`monocromo`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> cantidad</span></span> </p></td> 
  <td class="stentry"> <p>Factor de intensidad del filtro (real 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>Radio de núcleo del filtro en píxeles (real 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> umbral</span></span> </p></td> 
  <td class="stentry"> <p>Nivel de umbral del filtro (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromo</span></span> </p></td> 
  <td class="stentry"> <p>Establezca el valor en 0 para aplicarlo a cada componente de color por separado o en 1 para aplicarlo únicamente al brillo (intensidad) de la imagen. </p> <p><span class="codeph"> <span class="varname"> monocromo</span></span> se ignora en las imágenes en escala de grises. </p> </td> 
 </tr> 
</table>

La máscara de capa o la máscara compuesta también se enfoca.

## Propiedades {#section-fb5311b34d164946b74dadb32359518a}

Atributo de capa o atributo de vista. Se aplica a la capa actual o a la imagen de vista final si `layer=comp`. Las capas de efectos lo ignoran.

## Predeterminado {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` sin efecto de máscara de enfoque.

## Véase también {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
