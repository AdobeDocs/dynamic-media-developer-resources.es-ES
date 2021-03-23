---
description: Dilar/erosionar imagen. Aplica un dilato morfológico (radio > 0) o un erosionado (radio < 0) a los datos de la máscara.
seo-description: Dilar/erosionar imagen. Aplica un dilato morfológico (radio > 0) o un erosionado (radio < 0) a los datos de la máscara.
seo-title: op_growthMaskR
solution: Experience Manager
title: op_growthMaskR
uuid: b81968e7-ebaf-426c-9230-1afcf4b5cf24
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%

---


# op_growthMaskR{#op-growmaskr}

Dilar/erosionar imagen. Aplica un dilato morfológico (radio > 0) o un erosionado (radio &lt; 0) a los datos de la máscara.

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode el radio en píxeles donde <span class="codeph"><span class="varname"> radiusR</span></span> se aplica tal cual, independientemente de si la máscara se reduce (int -100..100). </p></td> 
 </tr> 
</table>

Se utiliza principalmente para reducir o ampliar ligeramente una máscara para evitar artefactos alrededor del borde de la máscara.

## Propiedades {#section-b1c66d65168d4ea695e8662ea690bd4e}

Se aplica a la capa actual o a la capa `0` si `layer=comp`.

## Predeterminado {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, sin ningún cambio.

## Véase también {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Efectos de capa](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_growth](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growthMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
