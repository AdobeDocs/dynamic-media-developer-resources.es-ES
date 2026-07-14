---
title: bgc
description: Color de fondo. Especifica el color de sustracción de las texturas y calcomanías coloreables.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
TQID: 'https://experienceleague.adobe.com/0Er9kHrfQj1lt14SlNJHxqddJZOp8BaO-lLYSqc5ajU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 2%

---

# bgc {#bgc}

Color de fondo. Especifica el color de sustracción de las texturas y calcomanías coloreables.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>Valor de color RGB o gris. </p></td> 
 </tr> 
</table>

El algoritmo de colorización de texturas de Image Rendering es sencillo: los valores de los componentes de `bgc=` se restan de los valores de los píxeles de textura; se agrega `color=` y, por último, el resultado se recorta a `0,0,0` y `255,255,255`.

Para los usos típicos de la colorización de texturas, el valor de `bgc=` puede ser el color más importante o dominante de la imagen de textura. La creación de imágenes de Dynamic Media proporciona herramientas semiautomáticas que extraen valores de color `bgc=` razonables de las imágenes de texturas.

Cuando se aplica un material de textura a un objeto de viñeta no texturable, `bgc=` se aplica como color de primer plano si no se especifica `color=`.

## Propiedades {#section-b2db6f147d7f443ba9f671de04c2ef19}

Atributo de material. Ignorado por el color sólido y los materiales del gabinete.

## Predeterminado {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` Si el material se basa en una entrada de catálogo; en caso contrario, `bgc=808080` (gris neutro).

## Ejemplo {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Colorea un tejido de ropa cuya textura tenga el color RGB dominante 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Véase también {#section-de9958dd63a742b4b5d780c59a57da33}

[catálogo::ColorBase](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)

