---
description: Dilate/erode la imagen. Aplica un dilato morfológico (radio > 0) o erosión (radio < 0) a los datos de la máscara.
solution: Experience Manager
title: op_grewMaskR
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# op_grewMaskR{#op-growmaskr}

Dilate/erode la imagen. Aplica un dilato morfológico (radio > 0) o erosión (radio &lt; 0) a los datos de la máscara.

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Radio de dilatación/erosión en píxeles donde <span class="codeph"><span class="varname"> radiusR</span></span> se aplica tal cual, independientemente de si la máscara está reducida de resolución (int -100..100). </p></td> 
 </tr> 
</table>

Se utiliza principalmente para aumentar o reducir ligeramente una máscara para evitar artefactos alrededor del borde de la máscara.

## Propiedades {#section-b1c66d65168d4ea695e8662ea690bd4e}

Se aplica a la capa actual o a la capa `0` if `layer=comp`.

## Predeterminado {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, para no cambiarlo.

## Véase también {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Efectos de capa](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grew](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_grewMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
