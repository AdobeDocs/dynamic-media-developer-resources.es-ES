---
description: Calidad JPEG. Especifica los atributos de codificación JPEG para controlar el nivel de compresión. Esto a su vez varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.
seo-description: Calidad JPEG. Especifica los atributos de codificación JPEG para controlar el nivel de compresión. Esto a su vez varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f69845d-3b25-41a7-b6c0-83cf1d2bc450
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

Calidad JPEG. Especifica los atributos de codificación JPEG para controlar el nivel de compresión. Esto a su vez varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.

` qlt= *``*[, *`cualitychroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> calidad </span> </p> </td> 
  <td class="stentry"> <p>Calidad de codificación JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> cromatismo </span> </p> </td> 
  <td class="stentry"> <p>Baja resolución de cromaticidad JPEG (0=normal, 1=disable); opcional, el valor predeterminado es 0. </p> </td> 
 </tr> 
</table>

Higher *`quality`* values increase file size and quality, lower values decrease file sizes and reduce perceived image quality. Si el valor es superior a 90, suele generar imágenes que no se distinguen de la imagen sin comprimir.

Defina el *`chroma`* indicador para desactivar el muestreo bajo cromaticidad RGB empleado por los codificadores JPEG típicos. Esto puede aumentar el enfoque percibido de los bordes de una imagen cuando el borde se define mediante un cambio de tono en lugar de un brillo. La configuración de este indicador puede provocar un ligero aumento en el tamaño del archivo. Experimente con esta configuración si el texto parece ligeramente borroso.

## Propiedades {#section-925a44cbdc9042db8d4eb149cd073d21}

Solicitar atributo. Se aplica independientemente de la configuración de la capa actual. Se omite si el formato de archivo de imagen de salida no admite codificación JPEG. Consulte la descripción de `fmt=` para obtener información sobre qué formatos de imagen de salida admiten `qlt=`.

*`chroma`* se omite si el tipo de píxel de salida es CMYK o gris.

## Predeterminado {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Ejemplo {#section-d7d33871d401433aa51d028823eae7a9}

Reduzca la calidad para una transmisión más rápida a través de una conexión de bajo ancho de banda:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Aumente la calidad de las conexiones de ancho de banda alto:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Véase también {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [atributo::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
