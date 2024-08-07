---
title: op_grewMask
description: Dilate/erode la imagen. Aplica un dilato morfológico (radio > 0) o erosión (radio < 0) a los datos de la máscara.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 2%

---

# op_grewMask{#op-growmask}

Dilate/erode la imagen. Aplica un dilato morfológico (radio > 0) o erosión (radio &lt; 0) a los datos de la máscara.

`op_growMask= *`radio`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radio</span> </p> </td> 
  <td class="stentry"> <p>Radio de dilatación/erosión en píxeles donde se supone que el radio se aplica a la máscara de resolución completa y, por lo tanto, se reduce para máscaras con disminución de resolución (int -100..100). </p></td> 
 </tr> 
</table>

Se utiliza principalmente para aumentar o reducir ligeramente una máscara para evitar artefactos alrededor del borde de la máscara.

## Propiedades {#section-b1c66d65168d4ea695e8662ea690bd4e}

Se aplica a la capa actual o a la capa `0` si `layer=comp`.

## Predeterminado {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, sin ningún cambio.

## Véase también {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Efectos de capa](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grew](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_grewMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
