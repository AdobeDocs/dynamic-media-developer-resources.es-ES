---
description: Rugosidad de la superficie material. Especifica la rugosidad relativa de la superficie material.
seo-description: Rugosidad de la superficie material. Especifica la rugosidad relativa de la superficie material.
seo-title: it
solution: Experience Manager
title: it
topic: Scene7 Image Serving - Image Rendering API
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# rough{#rough}

Rugosidad de la superficie material. Especifica la rugosidad relativa de la superficie material.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Rugosidad de superficie (0...100 por ciento) o -1 para seleccionar la rugosidad predeterminada. </p> </td> 
 </tr> 
</table>

Se utiliza para controlar el efecto de procesamiento de reflejo 3D. Los valores de rugosidad más bajos suelen producir efectos de reflexión más suaves; los valores más altos provocan aleatorización y dispersión de la imagen reflejada.

Cada tipo de material ( `type=`) define un mínimo y un máximo efecto de procesamiento de reflejo basado en la rugosidad. Para algunos tipos de material (por ejemplo, papel de pared), `rough=` tiene pocas repercusiones en el aspecto del reflejo, mientras que para otros tipos de material (por ejemplo, piedra o cerámica), el efecto es considerablemente más pronunciado.

`rough=-1` establece la rugosidad en un valor predeterminado interno del servidor (40% para tipos de material típicos).

## Propiedades {#section-515375758b254c80af576271bdb61bb8}

Atributo Material. Se omite si la viñeta no tiene capacidad de reflexión 3D, si el objeto destinatario no tiene geometría 3D asociada o si el objeto destinatario no refleja ningún otro objeto de la escena.

## Predeterminado {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` si el material está basado en una entrada de catálogo, de lo contrario aproximadamente el 40 %.

## Véase también {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ,  [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
