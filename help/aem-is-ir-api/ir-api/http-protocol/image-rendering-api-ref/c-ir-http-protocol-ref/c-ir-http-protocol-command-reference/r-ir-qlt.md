---
description: Calidad de Jpeg. Especifica los atributos de codificación JPEG para controlar el nivel de compresión.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 7%

---


# qlt{#qlt}

Calidad de Jpeg. Especifica los atributos de codificación JPEG para controlar el nivel de compresión.

` qlt= *``*[. *`cualitychroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> calidad </span> </p> </td> 
  <td class="stentry"> <p>Calidad de codificación JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> croma  </span> </p> </td> 
  <td class="stentry"> <p>Muestreo descendente de cromaticidad JPEG (0=normal, 1=disable); opcional, el valor predeterminado es 0. </p> </td> 
 </tr> 
</table>

Especifica los atributos de codificación JPEG para controlar el nivel de compresión. Esto a su vez varía el tamaño del archivo (la cantidad de datos de respuesta) y, indirectamente, la calidad visual de la imagen resultante.

Los valores más altos de *`quality`* aumentan el tamaño y la calidad del archivo, los valores más bajos reducen el tamaño de los archivos y reducen la calidad de imagen percibida. Si el valor es superior a 90, suele generar imágenes que no se distinguen de la imagen sin comprimir.

Establezca el indicador *`chroma`* para desactivar el muestreo descendente de cromaticidad empleado por los codificadores JPEG típicos. Esto puede aumentar la percepción de nitidez de los bordes en una imagen cuando el borde se define mediante un cambio de tono en lugar de un brillo. Configurar este indicador puede causar un ligero aumento en el tamaño del archivo. Experimente con esta configuración si el texto parece ligeramente borroso.

## Propiedades {#section-897b61c786dd4230a2c5807f2f40e722}

Puede ocurrir en cualquier parte de la solicitud.

Se omite si el formato de imagen de salida no admite compresión JPEG. Consulte la descripción de `fmt=` para obtener una lista de los formatos de imagen de salida que admiten la compresión JPEG.

## Predeterminado {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Véase también {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [atributo::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
