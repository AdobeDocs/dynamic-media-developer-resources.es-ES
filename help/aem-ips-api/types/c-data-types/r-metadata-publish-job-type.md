---
description: Publica metadatos en el servidor de metadatos.
seo-description: Publica metadatos en el servidor de metadatos.
seo-title: MetadataPublishJobType
solution: Experience Manager
title: MetadataPublishJobType
topic: Scene7 Image Production System API
uuid: 14cbb67e-56dc-4a25-b871-740be7ea7858
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 9%

---


# MetadataPublishJobType{#metadatapublishjobtype}

Publica metadatos en el servidor de metadatos.

Sintaxis

## Parámetros {#section-6c51fa689b3648fbb7c7945a7e176d0a}

<table id="table_23B5CFC5C3F946F9AFDB6A83A1AAB7AF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> forcePublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Establezca <span class="codeph"> True</span> para publicar <i>todos</i> los datos en el servidor de metadatos de nuevo. <p>Nota:  Dependiendo de la cantidad de datos, esto puede llevar de varios minutos a algunas horas. </p><p>No configure este parámetro si desea publicar solo metadatos nuevos o modificados. </p></td> 
  </tr> 
 </tbody> 
</table>

