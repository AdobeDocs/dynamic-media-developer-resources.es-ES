---
title: rgn
description: Región de interés. Especifica una región rectangular de interés (ROI) en la imagen compuesta, expresada en píxeles.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fa597ba-f949-47f2-bb0f-5c078b5c7524
TQID: 'https://experienceleague.adobe.com/NJ--WHYqUvttsXg-Gn2-FyVUdZJG9SAduOLaaG80nY8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 2%

---

# rgn{#rgn}

Región de interés. Especifica una región rectangular de interés (ROI) en la imagen compuesta, expresada en píxeles.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento de píxeles desde la esquina superior izquierda de la imagen compuesta hasta la parte superior izquierda del ROI (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> tamaño</span> </p></td> 
  <td class="stentry"> <p>Tamaño del ROI en píxeles (int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` solo define un ROI sin recortar la imagen. Cuando se aplican también `wid=` o `hei=` de mayor tamaño que, es posible que los datos adicionales de la imagen compuesta estén visibles en la imagen de respuesta final.

## Propiedades {#section-53edb35f4e364d7ca13fd0886e8b0c86}

Ver atributo. Se aplica independientemente de la configuración de capa actual.

Cualquier área del ROI que se extienda fuera de la imagen compuesta se rellenará con `bgc=`.

`rgn=` se ha aplicado antes del escalado final y la conexión con `scl=`, `wid=`, `hei=`, `fit=`, `rect=` o `align=`.

## Predeterminado {#section-6a3df8f670084def900ffef9dab7e94a}

Imagen compuesta completa ( `rgn=0,0,width,height`).

## Véase también {#section-07883760f25c4d17aedbee36b7883891}

[recorte=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [extensión=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
