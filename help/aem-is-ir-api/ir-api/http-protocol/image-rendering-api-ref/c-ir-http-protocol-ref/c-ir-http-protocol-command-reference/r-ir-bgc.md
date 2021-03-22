---
description: Color de fondo. Especifica el color de sustracción para texturas y calcomanías que se pueden colorear.
seo-description: Color de fondo. Especifica el color de sustracción para texturas y calcomanías que se pueden colorear.
seo-title: bgc
solution: Experience Manager
title: bgc
uuid: 551a0da8-dd1f-484a-bf7e-f4896370340a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 6%

---


# bgc{#bgc}

Color de fondo. Especifica el color de sustracción para texturas y calcomanías que se pueden colorear.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>Valor de color RGB o gris. </p></td> 
 </tr> 
</table>

El algoritmo de colorización de textura del renderizado de imágenes es bastante sencillo: los valores de componentes de `bgc=` se restan de los píxeles de textura, se añade `color=` y finalmente el resultado se recorta a `0,0,0` y `255,255,255`.

Para usos típicos de la colorización de textura, el valor de `bgc=` puede ser el color más importante o dominante de la imagen de textura. La creación de imágenes de Dynamic Media proporciona herramientas semiautomáticas que extraen valores de color `bgc=` razonables de las imágenes de texturas.

Cuando se aplica un material de textura a un objeto de viñeta no texturable, `bgc=` se aplica como color de primer plano si no se especifica `color=`.

## Propiedades {#section-b2db6f147d7f443ba9f671de04c2ef19}

Atributo de material. Ignorado por materiales de color sólido y de gabinete.

## Predeterminado {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` si el material está basado en una entrada de catálogo, en caso contrario  `bgc=808080` (gris neutro).

## Ejemplo {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Colorice una tela de indumentaria cuya textura tenga el color RGB dominante 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Véase también {#section-de9958dd63a742b4b5d780c59a57da33}

[catálogo::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ,  [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
