---
description: Publica metadatos en el servidor de metadatos.
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadatos
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '71'
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
   <td colname="col3">Configúrelo en <span class="codeph"> True</span> para publicar <i>todos los</i> datos en el servidor de metadatos de nuevo. <p>Nota:  En función de la cantidad de datos, esto puede tardar entre varios minutos y algunas horas. </p><p>No configure este parámetro si desea publicar solo metadatos nuevos o modificados. </p></td> 
  </tr> 
 </tbody> 
</table>
