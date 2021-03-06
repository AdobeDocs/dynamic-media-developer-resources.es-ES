---
description: Dilar/erosionar imagen. Aplica un dilato morfológico (radio > 0) o un erosionado (radio < 0) a los datos de la imagen.
solution: Experience Manager
title: op_growth
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---

# op_growth{#op-grow}

Dilar/erosionar imagen. Aplica un dilato morfológico (radio > 0) o un erosionado (radio &lt; 0) a los datos de la imagen.

`op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode radius en píxeles (int -100..100). </p></td> 
 </tr> 
</table>

`*``*` radiusis en píxeles en relación con la imagen compuesta. Si la imagen es de color, cada componente se procesa de forma independiente.

Se utiliza principalmente para modificar el tamaño de los efectos de capa. También es útil para lograr efectos especiales en capas de texto o capas de color sólido con máscaras.

## Propiedades {#section-b1c66d65168d4ea695e8662ea690bd4e}

Atributo de capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`.

## Predeterminado {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, sin ningún cambio.

## Véase también {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Efectos de capa](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
