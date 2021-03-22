---
description: Máscara de enfoque. El enfoque enmascara la capa o la imagen de vista final, después de todo el escalado, si layer=comp.
seo-description: Máscara de enfoque. El enfoque enmascara la capa o la imagen de vista final, después de todo el escalado, si layer=comp.
seo-title: op_usm
solution: Experience Manager
title: op_usm
uuid: c647e063-2405-489b-b14d-a70638ac8af7
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 6%

---


# op_usm{#op-usm}

Máscara de enfoque. El enfoque enmascara la capa o la imagen de vista final, después de todo el escalado, si layer=comp.

Se supone que los parámetros se aplican a la imagen de resolución completa y se reducen al procesar una imagen con disminución de resolución.

`op_usm= *``*[, *``*[, *``*[, *`amount tradiuswhholdmonchrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> cantidad</span></span> </p></td> 
  <td class="stentry"> <p>Factor de intensidad del filtro (real 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p></td> 
  <td class="stentry"> <p>Filtre el radio del núcleo en píxeles (real 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> umbral</span></span> </p></td> 
  <td class="stentry"> <p>Nivel de umbral de filtro (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromo</span></span> </p></td> 
  <td class="stentry"> <p>Ajuste en 0 para aplicar a cada componente de color por separado o en 1 para aplicar solo al brillo (intensidad) de la imagen. </p> <p> <span class="codeph"><span class="varname"> </span></span> se ignora el monocromo en las imágenes en escala de grises. </p></td> 
 </tr> 
</table>

La máscara de capa o la máscara compuesta también se endurecen.

## Propiedades {#section-fb5311b34d164946b74dadb32359518a}

Atributo de capa o atributo de vista. Se aplica a la capa actual o a la imagen de vista final si es `layer=comp`. Ignorado por capas de efecto.

## Predeterminado {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` para que no tenga efecto de máscara de enfoque.

## Véase también {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
