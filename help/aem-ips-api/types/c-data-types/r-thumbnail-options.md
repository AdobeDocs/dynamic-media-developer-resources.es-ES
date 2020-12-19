---
description: Tipo opcional que permite elegir un fotograma de vídeo concreto para utilizarlo como imagen en miniatura.
seo-description: Tipo opcional que permite elegir un fotograma de vídeo concreto para utilizarlo como imagen en miniatura.
seo-title: ThumbnailOptions
solution: Experience Manager
title: ThumbnailOptions
topic: Scene7 Image Production System API
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# ThumbnailOptions{#thumbnailoptions}

Tipo opcional que permite elegir un fotograma de vídeo concreto para utilizarlo como imagen en miniatura.

Sintaxis

## Parámetros {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>Establece el tiempo (en milisegundos desde el inicio de vídeo) del fotograma que desea utilizar para la miniatura de vídeo. Los valores van desde 0 hasta el final del vídeo. <p>Nota: El sistema utiliza el primer fotograma del vídeo para la miniatura si se especifica el tiempo incorrectamente. Consulte <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```

