---
description: Define las condiciones de búsqueda para los campos de etiquetas.
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# [!DNL TagCondition]{#tagcondition}

Define las condiciones de búsqueda para los campos de etiquetas.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Controlador de campo de etiqueta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Depende del tipo de campo de etiqueta y de si se utiliza el campo value o valueArray. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Si se pasa <span class="codeph"> valor</span>, <span class="codeph"> op</span> debe ser la constante de cadena Matches. La condición coincide con cualquier recurso asociado al valor de la etiqueta. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Si se pasa <span class="codeph"> valueArray</span>, el campo superior puede ser la constante <span class="codeph"> MatchesAny</span> para campos de etiqueta únicos o multivalor. Una condición <span class="codeph"> MatchesAny</span> coincide con cualquier recurso asociado con al menos uno de los valores de etiqueta en <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Para campos de etiquetas de varios valores, el campo superior se puede establecer en la constante <span class="codeph"> MatchesAll</span> con el campo <span class="codeph"> valueArray</span>. En este caso, la condición solo coincide con los recursos asociados con todos los valores de etiqueta de <span class="codeph"> valueArray</span> (posiblemente además de otros valores de etiqueta). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valor</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Un valor coincidente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Varios valores coincidentes. </td> 
  </tr> 
 </tbody> 
</table>
