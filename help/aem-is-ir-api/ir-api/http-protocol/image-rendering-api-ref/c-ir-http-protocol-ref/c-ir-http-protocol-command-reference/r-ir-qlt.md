---
title: qlt
description: Calidad JPEG. Especifica atributos de codificación de JPEG para controlar el nivel de compresión.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 7%

---

# qlt{#qlt}

Calidad JPEG. Especifica atributos de codificación de JPEG para controlar el nivel de compresión.

` qlt= *`calidad`*[. *`croma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> calidad </span> </p> </td> 
  <td class="stentry"> <p>Calidad de codificación de JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> croma </span> </p> </td> 
  <td class="stentry"> <p>Disminución de resolución de cromaticidad de JPEG (0=normal, 1=deshabilitar); opcional, el valor predeterminado es 0. </p> </td> 
 </tr> 
</table>

Especifica atributos de codificación de JPEG para controlar el nivel de compresión. A su vez, esto varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.

Los valores *`quality`* más altos aumentan el tamaño y la calidad del archivo, los valores más bajos reducen el tamaño del archivo y reducen la calidad de imagen percibida. Si el valor es superior a 90, suele generar imágenes que no se distinguen de la imagen sin comprimir.

Establezca el indicador *`chroma`* para deshabilitar la disminución de resolución de cromaticidad empleada por los codificadores habituales de JPEG. Este ajuste puede aumentar la nitidez percibida de los bordes de una imagen cuando el borde se define por un cambio en el tono en lugar de en el brillo. La configuración de este indicador puede provocar un ligero aumento en el tamaño del archivo. Experimente con esta configuración si el texto parece ligeramente borroso.

## Propiedades {#section-897b61c786dd4230a2c5807f2f40e722}

Puede producirse en cualquier lugar de la solicitud.

Se ignora si el formato de imagen de salida no admite la compresión JPEG. Consulte la descripción de `fmt=` para obtener una lista de formatos de imagen de salida compatibles con la compresión JPEG.

## Predeterminado {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Véase también {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [atributo::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
