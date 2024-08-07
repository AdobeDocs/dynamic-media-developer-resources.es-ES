---
title: caption
description: Parámetro común a todos los visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# caption{#caption}

Parámetro común a todos los visualizadores.

>[!NOTE]
>
>Este comando no se aplica al Visor de imágenes de vídeo.

` caption= *`archivo`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> archivo </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una dirección URL o una ruta al contenido de subtítulos WebVTT. El servicio de imágenes proporciona el archivo WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica el estado predeterminado del título. Habilitado es <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Este visor admite subtítulos mediante archivos WebVTT alojados. Los subtítulos especificados con este parámetro se aplican al vídeo que aparece primero en los conjuntos de medios; los vídeos posteriores se reproducen sin subtítulos. No se admiten indicaciones y regiones superpuestas. Operadores de posicionamiento de señal admitidos:

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Clave </p> </th> 
   <th colname="col2" class="entry"> <p>Nombre </p> </th> 
   <th colname="col3" class="entry"> <p>Valores </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>alineación de prueba </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> izquierda|derecha|centro|inicio|final </span> </p> </td> 
   <td colname="col4"> <p> Controla la alineación del texto. </p> <p>El valor predeterminado es <span class="codeph"> en el medio </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>posición del texto </p> </td> 
   <td colname="col3"> <p> 0-100% </p> </td> 
   <td colname="col4"> <p> Porcentaje de margen en el componente VideoPlayer para el principio del texto del rótulo. </p> <p>El valor predeterminado es <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>tamaño de línea </p> </td> 
   <td colname="col3"> <p> 0-100% </p> </td> 
   <td colname="col4"> <p> Porcentaje de anchura del vídeo utilizado para los subtítulos. </p> <p>El valor predeterminado es <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>posición de línea </p> </td> 
   <td colname="col3"> <p> 0%-100%|entero </p> </td> 
   <td colname="col4"> <p> Determina la posición de la línea en la página. </p> <p>Si se expresa como un entero sin signo de porcentaje, entonces es el número de líneas de la parte superior donde se muestra el texto. </p> <p>Si se expresa como un porcentaje (el símbolo de porcentaje es el último carácter), el texto del rótulo se mostrará ese porcentaje en el área de visualización. </p> <p>El valor predeterminado es <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Si hay otras funciones WebVTT presentes en el archivo WebVTT, no son compatibles; sin embargo, no interrumpen los subtítulos.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> archivo </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una dirección URL o una ruta al contenido de subtítulos WebVTT. El archivo WebVTT lo proporciona el servicio de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica el estado predeterminado del título. </p> <p>Habilitado es <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional.

## Predeterminado {#section-d411e450028c460392cb8508f8ccc5d9}

Ninguno.

## Ejemplo {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
