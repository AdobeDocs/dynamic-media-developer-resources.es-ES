---
description: Genera una imagen en miniatura para el vídeo.
seo-description: Genera una imagen en miniatura para el vídeo.
seo-title: MediaOptions
solution: Experience Manager
title: MediaOptions
topic: Scene7 Image Production System API
uuid: 4de59678-1bef-484c-9a43-ded531537aeb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MediaOptions{#mediaoptions}

Genera una imagen en miniatura para el vídeo.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3">Una matriz de <span class="codeph"> controladores PropertySet</span> que hacen referencia a los ajustes preestablecidos de codificación de vídeo para la transcodificación de vídeos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generar miniatura</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Cuando es true, se extrae el primer fotograma del vídeo y se utiliza como imagen en miniatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ThumbnailOptions</span> </td> 
   <td colname="col3">Opcional. Permite elegir un fotograma de vídeo concreto para utilizarlo como imagen en miniatura. <p>Para especificar una imagen en miniatura, pase el tiempo (en milisegundos desde el inicio de vídeo) del fotograma que desee utilizar. Los valores van desde 0 hasta el final del vídeo. <p>Nota: Si especifica la hora de forma incorrecta, <span class="codeph"> generar miniatura</span> tiene el valor predeterminado true. </p></p><p>Consulte <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> ThumbnailOptions</a>. </p></td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## Utilizado por {#section-87cb83407198432c95eaa2db9f12f9db}

El `mediaOptions` tipo lo utiliza:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

