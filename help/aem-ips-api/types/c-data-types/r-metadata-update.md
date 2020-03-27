---
description: Establece valores de metadatos para un recurso específico utilizado con setAssetMetadata. Describe los cambios que desea realizar en los metadatos.
seo-description: Establece valores de metadatos para un recurso específico utilizado con setAssetMetadata. Describe los cambios que desea realizar en los metadatos.
seo-title: MetadataUpdate
solution: Experience Manager
title: MetadataUpdate
topic: Scene7 Image Production System API
uuid: 09d3940b-117d-4d83-8b12-e86520c9da34
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MetadataUpdate{#metadataupdate}

Establece valores de metadatos para un recurso específico utilizado con setAssetMetadata. Describe los cambios que desea realizar en los metadatos.

>[!NOTE]
>
>Si se pasa el campo de un solo valor, el valor de la etiqueta del recurso se restablecerá al valor de etiqueta especificado.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Identificador del campo de metadatos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Valor de actualización de metadatos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Valor de metadatos booleano (solo para campos con tipo booleano). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Valor de metadatos largo (solo para campos interescritos). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:doble</span> </td> 
   <td colname="col3"> Valor de metadatos de Doble (solo para campos con tipo flotante). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Valor de metadatos de fecha (solo para campos con fecha escrita). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> <p>Añade a la lista de valor de etiqueta existente para el recurso. 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">Los campos de etiqueta de un solo valor almacenan solo el último valor. </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">Un campo de etiqueta de diccionario fijo devuelve un error si el valor no está en el diccionario. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3">Reemplaza la lista de valor de etiqueta existente para el recurso. 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">Los campos de etiqueta de un solo valor almacenan solo el último valor. </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">Un campo de etiqueta de diccionario fijo devuelve un error si el valor no está en el diccionario. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Elimina los valores especificados de la lista de valor de etiqueta del recurso, si están presentes. </td> 
  </tr> 
 </tbody> 
</table>

