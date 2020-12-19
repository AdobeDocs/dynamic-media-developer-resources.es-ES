---
description: Luminosidad de la superficie del material. Especifica el brillo relativo de la superficie del material. Se utiliza para seleccionar el mapa de iluminación y controlar la representación de los efectos de brillo y los reflejos 3D.
seo-description: Luminosidad de la superficie del material. Especifica el brillo relativo de la superficie del material. Se utiliza para seleccionar el mapa de iluminación y controlar la representación de los efectos de brillo y los reflejos 3D.
seo-title: brillo
solution: Experience Manager
title: brillo
topic: Scene7 Image Serving - Image Rendering API
uuid: 3774e08b-d24e-4cf2-8719-32a21bb9bcb6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 1%

---


# gloss{#gloss}

Luminosidad de la superficie del material. Especifica el brillo relativo de la superficie del material. Se utiliza para seleccionar el mapa de iluminación y controlar la representación de los efectos de brillo y los reflejos 3D.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Brillo (0...100 por ciento) o -1 para el valor de brillo predeterminado (referencia). </p></td> 
 </tr> 
</table>

Los valores de brillo más altos suelen provocar reflejos más fuertes y más nítidos y, si los efectos de brillo están activados en la viñeta, fortalece los resaltados especulares en la superficie material, principalmente aumentando el contraste de la iluminación. Cada tipo de material ( `type=`) define un mínimo y un máximo efecto de procesamiento. Para algunos tipos de material (por ejemplo, papel de pared), `gloss=` tiene pocas repercusiones en el aspecto del efecto de procesamiento, mientras que para otros tipos de material (por ejemplo, piedra o cerámica), el efecto es considerablemente más pronunciado.

Si `illum=-1` y la viñeta define varios mapas de iluminación, `gloss=` selecciona el mapa de iluminación utilizado para la operación de procesamiento actual. El procesador elige el mapa de iluminación cuyo valor de brillo es el más cercano al brillo especificado.

`gloss=-1` selecciona el valor de brillo de referencia del mapa de iluminación seleccionado, tal como se define en las propiedades de vista de la viñeta. Esto garantiza que el mapa de iluminación se utilice exactamente como se creó, sin más modificaciones, incluso si los efectos de brillo están activados. Si `illum=-1` también se utiliza el valor de brillo de referencia del primer mapa de iluminación de la vista de viñeta.

## Propiedades {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Atributo Material. Se omite si la viñeta no define varios mapas de iluminación o si se especifica `illum=`, si la viñeta no incluye datos de reflejo 3D o si el objeto actual no admite reflejos 3D, o si los efectos de brillo están desactivados en la viñeta.

## Predeterminado {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` si el material se basa en una entrada de catálogo, en caso contrario el valor de brillo de referencia del mapa de iluminación por defecto o del mapa de iluminación especificado por  `illum=`.

## Véase también {#section-29f5b761481a4c52a499a2e16e63c70b}

[atributo::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35),  [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180),  [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a),  [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
