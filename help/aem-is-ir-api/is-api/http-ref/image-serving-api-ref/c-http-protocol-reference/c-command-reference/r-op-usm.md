---
title: op_usm
description: Máscara de enfoque. El enfoque enmascara la capa o la imagen de vista final, después de todo el escalado, si layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 6%

---

# op_usm{#op-usm}

Máscara de enfoque. El enfoque enmascara la capa o la imagen de vista final, después de todo el escalado, si layer=comp.

Se supone que los parámetros se aplican a la imagen de resolución completa y se reducen al procesar una imagen con disminución de resolución.

`op_usm= *`cantidad`*[, *`radio`*[, *`umbral`*[, *`monocromo`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> cantidad</span></span> </p></td> 
  <td class="stentry"> <p>Factor de intensidad del filtro (real 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radio</span></span> </p></td> 
  <td class="stentry"> <p>Radio de núcleo del filtro en píxeles (real 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> umbral</span></span> </p></td> 
  <td class="stentry"> <p>Nivel de umbral del filtro (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromo</span></span> </p></td> 
  <td class="stentry"> <p>Establezca el valor en 0 para aplicarlo a cada componente de color por separado o en 1 para aplicarlo únicamente al brillo (intensidad) de la imagen. </p> <p> <span class="codeph"><span class="varname"> monocromo</span></span> se ignora en las imágenes en escala de grises. </p></td> 
 </tr> 
</table>

La máscara de capa o la máscara compuesta también se enfoca.

## Propiedades {#section-fb5311b34d164946b74dadb32359518a}

Atributo de capa o atributo de vista. Se aplica a la capa actual o a la imagen de vista final si `layer=comp`. Ignorado por las capas de efecto.

## Predeterminado {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` sin efecto de máscara de enfoque.

## Véase también {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
