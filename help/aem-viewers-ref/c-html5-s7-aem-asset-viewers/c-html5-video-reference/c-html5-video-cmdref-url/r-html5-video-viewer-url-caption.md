---
description: URL para el visor de vídeos.
seo-description: URL para el visor de vídeos.
seo-title: caption
solution: Experience Manager
title: caption
topic: Dynamic Media
uuid: 670d83c2-bfc5-411a-8581-5103a62aa8cf
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 11%

---


# caption{#caption}

URL para el visor de vídeos.

` caption= *`archivo`*[,0|1]`

El visor admite subtítulos opcionales a través de archivos WebVTT alojados. No se admiten las indicaciones y regiones superpuestas. Los operadores de posicionamiento de señal admitidos son los siguientes:

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
   <td colname="col2"> <p>alinear texto </p> </td> 
   <td colname="col3"> <p><span class="codeph"> left|right|middle|inicio|end</span> </p> </td> 
   <td colname="col4"> <p> Controla la alineación del texto. </p> <p>El valor predeterminado es <span class="codeph"> middle</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>posición de texto </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Porcentaje de inserción en el componente VideoPlayer para el principio del texto del rótulo. </p> <p>El valor predeterminado es 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>tamaño de línea </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Porcentaje de anchura de vídeo utilizado para rótulos. </p> <p>El valor predeterminado es 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>posición de línea </p> </td> 
   <td colname="col3"> <p> 0%-100%|entero </p> </td> 
   <td colname="col4"> <p> Determina la posición de línea en la página. </p> <p>Si se expresa como un entero (sin signo de porcentaje), es el número de líneas desde la parte superior donde se muestra el texto. </p> <p>Si es un porcentaje (el signo de porcentaje es el último carácter), se muestra el texto del rótulo ese porcentaje en el área de visualización. </p> <p>El valor predeterminado es 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

Otras funciones WebVTT presentes en el archivo WebVTT no son compatibles, pero no deben interrumpir el subtítulo.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> archivo</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica una dirección URL o ruta al contenido del subtítulo WebVTT. Proporcione el archivo WebVTT por ImageServing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Especifica el estado del rótulo predeterminado (activado es <span class="codeph"> 1</span>). </p> </td> 
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

