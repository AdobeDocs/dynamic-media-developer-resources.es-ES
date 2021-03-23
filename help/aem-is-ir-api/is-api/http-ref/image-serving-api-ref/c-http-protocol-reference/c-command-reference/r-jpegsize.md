---
description: Tamaño de Jpeg en KiloBytes. Especifica el tamaño máximo de la respuesta JPEG en kilobytes.
seo-description: Tamaño de Jpeg en KiloBytes. Especifica el tamaño máximo de la respuesta JPEG en kilobytes.
seo-title: jpegSize
solution: Experience Manager
title: jpegSize
uuid: 832163ca-0554-481d-b87f-bf322f415274
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 3%

---


# jpegSize{#jpegsize}

Tamaño de Jpeg en KiloBytes. Especifica el tamaño máximo de la respuesta JPEG en kilobytes.

`jpegSize= *`tamaño`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p> </td> 
  <td class="stentry"> <p>Tamaño en kilobytes. </p></td> 
 </tr> 
</table>

Si se establece en un valor positivo, y si la respuesta JPEG con la calidad JPEG especificada no supera este valor, la imagen se devuelve como respuesta. De lo contrario, la calidad JPEG disminuye hasta que produce una imagen que se ajusta al tamaño especificado o hasta que determina que no se puede ajustar. En este último caso, la solicitud falla con un error.

Un valor de 0 significa que la respuesta no está restringida por el tamaño.

No se permiten valores negativos.

## Propiedades {#section-19e544e77d35478b98fe8666f27d6968}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Se omite si el formato de imagen de salida no es JPEG.

## Predeterminado {#section-198b798ed187453197e0969c641d6fb5}

0

## Ejemplo {#section-46bf806fd3ef4875b7726df32b6f834d}

El tamaño de garantía no es demasiado grande para la entrega a un dispositivo con memoria limitada:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Véase también {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [atributo::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
