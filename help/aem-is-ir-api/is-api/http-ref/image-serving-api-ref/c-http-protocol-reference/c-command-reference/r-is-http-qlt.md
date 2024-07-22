---
title: qlt
description: Calidad JPEG. Especifica atributos de codificación del JPEG para controlar el nivel de compresión. Esto, a su vez, varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 6%

---

# qlt{#qlt}

Calidad JPEG. Especifica atributos de codificación del JPEG para controlar el nivel de compresión. Esto, a su vez, varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.

` qlt= *`calidad`*[, *`croma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> calidad </span> </p> </td> 
  <td class="stentry"> <p>Calidad de codificación JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> croma </span> </p> </td> 
  <td class="stentry"> <p>Disminución de resolución de cromaticidad del JPEG (0=normal, 1=deshabilitar); opcional, el valor predeterminado es 0. </p> </td> 
 </tr> 
</table>

Los valores *`quality`* más altos aumentan el tamaño y la calidad del archivo, los valores más bajos reducen el tamaño del archivo y reducen la calidad de imagen percibida. Si el valor es superior a 90, suele generar imágenes que no se distinguen de la imagen sin comprimir.

Establezca el indicador *`chroma`* para deshabilitar la disminución de resolución de cromaticidad RGB empleada por los codificadores JPEG típicos. Esto puede aumentar la nitidez percibida de los bordes de una imagen cuando el borde se define por un cambio en el tono en lugar de en el brillo. La configuración de este indicador puede provocar un ligero aumento en el tamaño del archivo. Experimente con esta configuración si el texto parece ligeramente borroso.

## Propiedades {#section-925a44cbdc9042db8d4eb149cd073d21}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Se ignora si el formato del archivo de imagen de salida no admite la codificación del JPEG. Consulte la descripción de `fmt=` para obtener información sobre los formatos de imagen de salida que admiten `qlt=`.

*`chroma`* se omite si el tipo de píxel de salida es CMYK o gris.

## Predeterminado {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Ejemplo {#section-d7d33871d401433aa51d028823eae7a9}

Reduzca la calidad para una transmisión más rápida a través de una conexión de bajo ancho de banda:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Aumente la calidad de las conexiones de gran ancho de banda:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Véase también {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [atributo::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
