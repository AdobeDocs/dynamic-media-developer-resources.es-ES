---
title: DescomprimirOpciones
description: Cargue la configuración para procesar los archivos ZIP y TAR como recursos principales (Ninguno) o para extraer y cargar su contenido (Descomprimir).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 89222959-3701-4ea6-bcae-98ceec93764f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# [!DNL UnCompressOptions]{#uncompressoptions}

Cargue la configuración para procesar los archivos ZIP y TAR como recursos principales (Ninguno) o para extraer y cargar su contenido (Descomprimir).

>[!NOTE]
>
>La configuración `None` es la predeterminada.

## Parámetros {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> proceso</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Controla el procesamiento de archivos ZIP y TAR. Proporciona dos opciones: 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> Ninguno:</span> Procesar como recursos principales. </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> Descomprimir:</span> Extraer y procesar el contenido. </li>
     </ul><p>Nota: Las constantes de cadena distinguen entre mayúsculas y minúsculas. Use <span class="codeph"> Descomprimir</span>, no <span class="codeph"> descomprimir</span> ni <span class="codeph"> descomprimir</span>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## Utilizado por {#section-b2a829cf5511412e968bb2000f85cc31}

El tipo `unCompressionOptions` lo utiliza:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [CargarTrabajo](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
