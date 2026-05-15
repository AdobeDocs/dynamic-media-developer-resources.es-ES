---
title: jpegSize
description: Tamaño JPEG en Kilobytes. Especifica el tamaño máximo de la respuesta de JPEG en kilobytes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
TQID: 'https://experienceleague.adobe.com/FXPTcUoMZP-mA-PyuaLqLFqqY9ITLWkjWgezRFUDiHI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 3%

---

# jpegSize{#jpegsize}

Tamaño JPEG en Kilobytes. Especifica el tamaño máximo de la respuesta de JPEG en kilobytes.

`jpegSize= *`tamaño`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> tamaño</span></span> </p> </td> 
  <td class="stentry"> <p>Tamaño en kilobytes. </p></td> 
 </tr> 
</table>

Si se establece en un valor positivo y la respuesta de JPEG con la calidad de JPEG especificada no supera este valor, esa imagen se devuelve como respuesta. De lo contrario, la calidad del JPEG disminuye hasta que produce una imagen que se ajusta al tamaño especificado o hasta que determina que no cabe. En este último caso, la solicitud falla con un error.

Un valor de 0 significa que la respuesta no está restringida por el tamaño.

No se permiten valores negativos.

## Propiedades {#section-19e544e77d35478b98fe8666f27d6968}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Se ignora si el formato de imagen de salida no es JPEG.

## Predeterminado {#section-198b798ed187453197e0969c641d6fb5}

0

## Ejemplo {#section-46bf806fd3ef4875b7726df32b6f834d}

El tamaño de la garantía no es demasiado grande para entregarlo a un dispositivo con memoria limitada:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Véase también {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [atributo::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
