---
description: Calidad de Jpeg. Especifica los atributos de codificación JPEG para controlar el nivel de compresión. Esto a su vez varía el tamaño del archivo (la cantidad de datos de respuesta) y, indirectamente, la calidad visual de la imagen resultante.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 15%

---

# qlt{#qlt}

Calidad de Jpeg. Especifica los atributos de codificación JPEG para controlar el nivel de compresión. Esto a su vez varía el tamaño del archivo (la cantidad de datos de respuesta) y, indirectamente, la calidad visual de la imagen resultante.

` qlt= *``*[, *`cualitychroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> calidad  </span> </span> </p> </td> 
  <td class="stentry"> <p>Calidad de codificación JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> croma  </span> </span> </p> </td> 
  <td class="stentry"> <p>Muestreo descendente de cromaticidad JPEG (0=normal, 1=disable); opcional, el valor predeterminado es 0. </p> </td> 
 </tr> 
</table>

Solo se usa si `fmt=jpg`. Ignorado en caso contrario

Unos valores de calidad altos aumentan el tamaño del archivo y la calidad; unos valores bajos reducen el tamaño de los archivos y la calidad de imagen percibida. Si el valor es superior a 90, suele generar imágenes que no se distinguen de la imagen sin comprimir.

Establezca el indicador `chroma` para desactivar el muestreo descendente de cromaticidad RGB utilizado por los codificadores JPEG típicos. Esto puede aumentar la percepción de nitidez de los bordes en una imagen cuando el borde se define mediante un cambio de tono en lugar de un brillo. Configurar este indicador puede causar un ligero aumento en el tamaño del archivo. Experimente con esta configuración si el texto parece ligeramente borroso.

`chroma` se ignora si el tipo de píxel de salida es CMYK o gris.

## Ejemplo {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
