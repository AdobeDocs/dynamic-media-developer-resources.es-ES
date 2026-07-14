---
title: áspero
description: Rugosidad superficial del material. Especifica la rugosidad relativa de la superficie de material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
TQID: 'https://experienceleague.adobe.com/FhLagzJwQodPihSxkEyBl8zSnEU0gDq0zevixYMApUY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 182
ht-degree: 1%

---

# áspero{#rough}

Rugosidad superficial del material. Especifica la rugosidad relativa de la superficie de material.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Rugosidad de la superficie (0...100 por ciento) o -1 para seleccionar la rugosidad por defecto. </p> </td> 
 </tr> 
</table>

Se utiliza para controlar el efecto de procesamiento de la reflexión 3D. Los valores de rugosidad más bajos suelen producir efectos de reflexión más suaves; los valores más altos provocan la aleatorización y la dispersión de la imagen reflejada.

Cada tipo de material (`type=`) define un efecto de procesamiento de reflexión mínimo y máximo basado en la rugosidad. Para algunos tipos de material (por ejemplo, papel de pared), `rough=` tiene un impacto mínimo en el aspecto de la reflexión, mientras que para otros tipos de material (por ejemplo, piedra o cerámica), el efecto es considerablemente más pronunciado.

`rough=-1` define la rugosidad como un valor predeterminado interno del servidor (40% para tipos de material típicos).

## Propiedades {#section-515375758b254c80af576271bdb61bb8}

Atributo de material. Se ignora si la viñeta no tiene capacidad de reflexión 3D, si el objeto de destino no tiene geometría 3D asociada o si el objeto de destino no refleja ningún otro objeto de la escena.

## Predeterminado {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` Si el material se basa en una entrada del catálogo; en caso contrario, aproximadamente el 40%.

## Véase también {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)

