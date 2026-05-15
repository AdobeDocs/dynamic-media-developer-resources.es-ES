---
title: qlt
description: Calidad JPEG. Especifica atributos de codificación de JPEG para controlar el nivel de compresión. Esto, a su vez, varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
TQID: 'https://experienceleague.adobe.com/sf3ydtf3lGCG1BfJfc1vW5hXFBawbeWJwXNSJdUEei8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 15%

---

# qlt{#qlt}

Calidad JPEG. Especifica atributos de codificación de JPEG para controlar el nivel de compresión. Esto, a su vez, varía el tamaño del archivo (cantidad de datos de respuesta) e, indirectamente, la calidad visual de la imagen resultante.

` qlt= *`Calidad`*[, *`croma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> calidad </span> </span> </p> </td> 
  <td class="stentry"> <p>Calidad de codificación de JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> croma </span> </span> </p> </td> 
  <td class="stentry"> <p>Disminución de resolución de cromaticidad de JPEG (0=normal, 1=deshabilitar); opcional, el valor predeterminado es 0. </p> </td> 
 </tr> 
</table>

Solo se usa si `fmt=jpg`. Ignorado de otro modo

Unos valores de calidad altos aumentan el tamaño del archivo y la calidad; unos valores bajos reducen el tamaño de los archivos y la calidad de imagen percibida. Si el valor es superior a 90, suele generar imágenes que no se distinguen de la imagen sin comprimir.

Establezca el indicador `chroma` para deshabilitar la disminución de resolución de cromaticidad de RGB empleada por los codificadores de JPEG típicos. Esto puede aumentar la nitidez percibida de los bordes de una imagen cuando el borde se define por un cambio en el tono en lugar de en el brillo. La configuración de este indicador puede provocar un ligero aumento en el tamaño del archivo. Experimente con esta configuración si el texto parece ligeramente borroso.

Se omite `chroma` si el tipo de píxel de salida es CMYK o gris.

## Ejemplo {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`
