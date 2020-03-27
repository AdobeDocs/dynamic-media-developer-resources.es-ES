---
description: Calidad JPEG. Especifica los atributos de codificación JPEG para controlar el nivel de compresión. Esto a su vez varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.
seo-description: Calidad JPEG. Especifica los atributos de codificación JPEG para controlar el nivel de compresión. Esto a su vez varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

Calidad JPEG. Especifica los atributos de codificación JPEG para controlar el nivel de compresión. Esto a su vez varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.

` qlt= *``*[, *`cualitychroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> calidad </span></span> </p> </td> 
  <td class="stentry"> <p>Calidad de codificación JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> croma </span></span> </p> </td> 
  <td class="stentry"> <p>Baja resolución de cromaticidad JPEG (0=normal, 1=disable); opcional, el valor predeterminado es 0. </p> </td> 
 </tr> 
</table>

Se utiliza solamente si `fmt=jpg`. Omitido en caso contrario

Unos valores de calidad altos aumentan el tamaño del archivo y la calidad; unos valores bajos reducen el tamaño de los archivos y la calidad de imagen percibida. Si el valor es superior a 90, suele generar imágenes que no se distinguen de la imagen sin comprimir.

Defina el `chroma` indicador para desactivar el muestreo bajo cromaticidad RGB empleado por los codificadores JPEG típicos. Esto puede aumentar el enfoque percibido de los bordes de una imagen cuando el borde se define mediante un cambio de tono en lugar de un brillo. La configuración de este indicador puede provocar un ligero aumento en el tamaño del archivo. Experimente con esta configuración si el texto parece ligeramente borroso.

`chroma` se omite si el tipo de píxel de salida es CMYK o gris.

## Ejemplo {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
