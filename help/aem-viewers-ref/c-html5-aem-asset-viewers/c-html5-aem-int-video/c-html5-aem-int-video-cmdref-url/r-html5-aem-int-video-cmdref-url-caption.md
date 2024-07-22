---
title: caption
description: Comando de URL para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 8eb2aa50-52b9-4b63-9789-87e492f34a22
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 3%

---

# caption{#caption}

Comando de URL para el visualizador de vídeo interactivo.

` caption= *`archivo`*[,0|1]`

El visor admite subtítulos a través de archivos WebVTT alojados. No se admiten indicaciones y regiones superpuestas. Los operadores de posicionamiento de referencia admitidos son los siguientes:

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Clave </p> </th> 
   <th colname="col2" class="entry"> <p>Nombre </p> </th> 
   <th colname="col3" class="entry"> <p>Valor </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>alineación de texto </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> izquierda|derecha|centro|inicio|final </span> </p> </td> 
   <td colname="col4"> <p> Controle la alineación del texto. </p> <p>El valor predeterminado es <span class="codeph"> en el medio </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>posición del texto </p> </td> 
   <td colname="col3"> <p> 0-100% </p> </td> 
   <td colname="col4"> <p> Porcentaje de margen en el componente VideoPlayer para el principio del texto del rótulo. </p> <p>El valor predeterminado es 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>tamaño de línea </p> </td> 
   <td colname="col3"> <p> 0-100% </p> </td> 
   <td colname="col4"> <p> Porcentaje de anchura del vídeo utilizado para los subtítulos. </p> <p>El valor predeterminado es 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>posición de línea </p> </td> 
   <td colname="col3"> <p> 0%-100%|entero </p> </td> 
   <td colname="col4"> <p> Determina la posición de la línea en la página. </p> <p>Si se expresa como un número entero (sin signo de porcentaje), entonces es el número de líneas de la parte superior donde se muestra el texto. </p> <p>Si es un porcentaje (el símbolo de porcentaje es el último carácter), el texto del rótulo se muestra ese porcentaje en el área de visualización. </p> <p>El valor predeterminado es 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

Otras funciones WebVTT presentes en el archivo WebVTT no son compatibles, pero no deben interrumpir los subtítulos.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> archivo </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una dirección URL o una ruta al contenido de subtítulos WebVTT. Proporcione el archivo WebVTT mediante el servicio de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica el estado predeterminado del título (habilitado es <span class="codeph"> 1 </span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

Ninguno.

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.caption.vtt,1
```
