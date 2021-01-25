---
description: Calidad JPEG. Especifica los atributos de codificación JPEG para controlar el nivel de compresión.
seo-description: Calidad JPEG. Especifica los atributos de codificación JPEG para controlar el nivel de compresión.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 46f5b0da-7fe7-4daf-947b-bb5f5f5f5e6d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 7%

---


# qlt{#qlt}

Calidad JPEG. Especifica los atributos de codificación JPEG para controlar el nivel de compresión.

` qlt= *``*[. *`cualitychroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> calidad </span> </p> </td> 
  <td class="stentry"> <p>Calidad de codificación JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> cromatismo  </span> </p> </td> 
  <td class="stentry"> <p>Baja resolución de cromaticidad JPEG (0=normal, 1=disable); opcional, el valor predeterminado es 0. </p> </td> 
 </tr> 
</table>

Especifica los atributos de codificación JPEG para controlar el nivel de compresión. Esto a su vez varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.

Los valores *`quality`* más altos aumentan el tamaño y la calidad del archivo, los valores más bajos disminuyen el tamaño del archivo y reducen la calidad de imagen percibida. Si el valor es superior a 90, suele generar imágenes que no se distinguen de la imagen sin comprimir.

Establezca el indicador *`chroma`* para desactivar el muestreo de disminución de cromaticidad empleado por los codificadores JPEG típicos. Esto puede aumentar el enfoque percibido de los bordes de una imagen cuando el borde se define mediante un cambio de tono en lugar de un brillo. La configuración de este indicador puede provocar un ligero aumento en el tamaño del archivo. Experimente con esta configuración si el texto parece ligeramente borroso.

## Propiedades {#section-897b61c786dd4230a2c5807f2f40e722}

Puede ocurrir en cualquier parte de la solicitud.

Se omite si el formato de imagen de salida no admite compresión JPEG. Consulte la descripción de `fmt=` para obtener una lista de los formatos de imagen de salida que admiten compresión JPEG.

## Predeterminado {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Véase también {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [atributo::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
