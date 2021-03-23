---
description: Parámetro común a todos los visualizadores.
seo-description: Parámetro común a todos los visualizadores.
seo-title: caption
solution: Experience Manager
title: caption
uuid: e5a715c4-9b5b-48fc-8228-5e7416e2b71a
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 6%

---


# caption{#caption}

Parámetro común a todos los visualizadores.

>[!NOTE]
>
>Este comando no se aplica al visualizador de imágenes de vídeo.

` caption= *`archivo`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una dirección URL o ruta al contenido del subtítulo WebVTT. Image Serving proporciona el archivo WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica el estado del rótulo predeterminado. Habilitado es <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Este visor admite subtítulos optativos mediante archivos WebVTT alojados. Los subtítulos especificados con este parámetro se aplican al vídeo que aparece primero en los conjuntos de medios; los vídeos siguientes se reproducen sin subtítulos. No se admiten las rutas y regiones superpuestas. Operadores de posicionamiento de señal admitidos:

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
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end  </span> </p> </td> 
   <td colname="col4"> <p> Controla la alineación del texto. </p> <p>El valor predeterminado es <span class="codeph"> central </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">  </span> </p> </td> 
   <td colname="col2"> <p>posición del texto </p> </td> 
   <td colname="col3"> <p> 0 %-100 % </p> </td> 
   <td colname="col4"> <p> Porcentaje de inserción en el componente VideoPlayer para el principio del texto del rótulo. </p> <p>El valor predeterminado es <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S  </span> </p> </td> 
   <td colname="col2"> <p>tamaño de línea </p> </td> 
   <td colname="col3"> <p> 0 %-100 % </p> </td> 
   <td colname="col4"> <p> Porcentaje de la anchura del vídeo utilizado para los rótulos. </p> <p>El valor predeterminado es <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>posición de línea </p> </td> 
   <td colname="col3"> <p> 0%-100%|entero </p> </td> 
   <td colname="col4"> <p> Determina la posición de línea en la página. </p> <p>Si se expresa como un entero sin signo de porcentaje, entonces es el número de líneas desde la parte superior donde se muestra el texto. </p> <p>Si se expresa como un porcentaje (el signo de porcentaje es el último carácter), se mostrará el texto del rótulo ese porcentaje en el área de visualización. </p> <p>El valor predeterminado es <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Tenga en cuenta que si hay otras funciones WebVTT presentes en el archivo WebVTT, no serán compatibles; sin embargo, no interrumpirán el subtítulos.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una dirección URL o ruta al contenido del subtítulo WebVTT. El archivo WebVTT se proporciona mediante Image Serving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica el estado del rótulo predeterminado. </p> <p>Habilitado es <span class="codeph"> 1 </span>. </p> </td> 
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

