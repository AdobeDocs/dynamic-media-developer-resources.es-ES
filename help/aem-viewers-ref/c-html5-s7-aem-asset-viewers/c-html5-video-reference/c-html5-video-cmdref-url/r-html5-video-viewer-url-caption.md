---
title: caption
description: Comando URL del Visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: a9af3335-ae18-4399-9014-47ec0306a087
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 5%

---

# caption{#caption}

Comando URL del Visor de vídeo.

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
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>alineación de texto </p> </td> 
   <td colname="col3"> <p><span class="codeph"> izquierda|derecha|medio|inicio|final</span> </p> </td> 
   <td colname="col4"> <p> Controle la alineación del texto. </p> <p>El valor predeterminado es <span class="codeph"> middle</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>posición del texto </p> </td> 
   <td colname="col3"> <p> 0-100% </p> </td> 
   <td colname="col4"> <p> Porcentaje de margen en el componente VideoPlayer para el principio del texto del rótulo. </p> <p>El valor predeterminado es 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>tamaño de línea </p> </td> 
   <td colname="col3"> <p> 0-100% </p> </td> 
   <td colname="col4"> <p> Porcentaje de anchura del vídeo utilizado para los subtítulos. </p> <p>El valor predeterminado es 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
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
   <td colname="col1"> <p><span class="codeph"><span class="varname"> archivo</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica una dirección URL o una ruta al contenido de subtítulos WebVTT. Proporcione el archivo WebVTT mediante ImageServing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Especifica el estado predeterminado del título (habilitado es <span class="codeph"> 1</span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

Ninguno.

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
