---
title: lustre
description: Brillo superficial de material. Especifica el brillo relativo de la superficie de material. Se utiliza para seleccionar el mapa de iluminación y controlar la renderización de efectos de brillo y reflejos 3D.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# lustre{#gloss}

Brillo superficial de material. Especifica el brillo relativo de la superficie de material. Se utiliza para seleccionar el mapa de iluminación y controlar la renderización de efectos de brillo y reflejos 3D.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Brillo (0...100 por ciento) o -1 para el valor de brillo predeterminado (referencia). </p></td> 
 </tr> 
</table>

Los valores de brillo más altos suelen causar reflejos más fuertes y más nítidos y, si los efectos de brillo están activados en la viñeta, refuerzan los resaltados especulares en la superficie del material, sobre todo al aumentar el contraste de iluminación. Cada tipo de material ( `type=`) define un efecto de procesamiento mínimo y máximo. Para algunos tipos de material (por ejemplo, papel de pared), `gloss=` tiene un impacto mínimo en el aspecto del efecto de renderización, mientras que para otros tipos de materiales (por ejemplo, piedra o cerámica), el efecto es sustancialmente más pronunciado.

If `illum=-1` y si la viñeta define varios mapas de iluminación, `gloss=` selecciona el mapa de iluminación utilizado para la operación de renderización actual. El procesador elige el mapa de iluminación cuyo valor de brillo es el más cercano al brillo especificado.

`gloss=-1` Selecciona el valor de brillo de referencia del mapa de iluminación seleccionado, tal como se define en las propiedades de vista de la viñeta. Este valor garantiza que el mapa de iluminación se utilice exactamente como se creó, sin más modificaciones, incluso si los efectos de brillo están activados. If `illum=-1` a continuación, se utiliza el valor de brillo de referencia del primer mapa de iluminación de la vista de viñeta.

## Propiedades {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Atributo de material. Se ignora si la viñeta no define varios mapas de iluminación. O bien, si `illum=` se especifica, si la viñeta no incluye datos de reflexión 3D. O bien, si el objeto actual no admite reflejos 3D, o si los efectos de brillo están desactivados en la viñeta.

## Predeterminado {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` Si el material se basa en una entrada de catálogo, de lo contrario el valor de brillo de referencia del mapa de iluminación por defecto o el mapa de iluminación especificado por `illum=`.

## Véase también {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Brillo](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [áspero=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
