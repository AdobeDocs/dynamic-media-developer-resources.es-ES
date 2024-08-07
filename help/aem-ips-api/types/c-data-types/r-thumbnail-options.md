---
description: Tipo opcional que permite elegir un fotograma de vídeo concreto para utilizarlo como imagen en miniatura.
solution: Experience Manager
title: ThumbnailOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 6%

---

# [!DNL ThumbnailOptions]{#thumbnailoptions}

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
   <td colname="col3"> <p>Establece el tiempo (en milisegundos desde el inicio del vídeo) para el fotograma que desea utilizar para la miniatura de vídeo. Los valores van del 0 al final del vídeo. <p>Nota: El sistema utiliza el primer fotograma del vídeo para la miniatura si se especifica la hora de forma incorrecta. Consulte <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> opciones de medios</a>. </p></p> </td> 
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
