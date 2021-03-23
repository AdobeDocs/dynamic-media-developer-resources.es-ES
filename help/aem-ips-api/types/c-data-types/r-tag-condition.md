---
description: Define las condiciones de búsqueda para los campos de etiqueta.
seo-description: Define las condiciones de búsqueda para los campos de etiqueta.
seo-title: TagCondition
solution: Experience Manager
title: TagCondition
uuid: c7727267-05b6-4011-9ddf-7f3134e9609b
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 6%

---


# TagCondition{#tagcondition}

Define las condiciones de búsqueda para los campos de etiqueta.

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
   <td colname="col3"> Identificador de campo de etiqueta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Depende del tipo de campo de etiqueta y de si se utiliza el campo value o valueArray . 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Si se pasa <span class="codeph"> valor</span>, <span class="codeph"> op</span> debe ser la constante de cadena Coincide. La condición coincide con cualquier recurso asociado al valor de la etiqueta. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Si se pasa <span class="codeph"> valueArray</span> , el campo superior puede ser la constante <span class="codeph"> coincide conAny</span> para campos de etiquetas individuales o multivalor. Una condición <span class="codeph"> coincide con Cualquiera</span> coincide con cualquier recurso que esté asociado con al menos uno de los valores de etiqueta en <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Para los campos de etiqueta de varios valores, el campo superior se puede establecer en la constante <span class="codeph"> Coincide con todos</span> con el campo <span class="codeph"> valueArray</span>. En este caso, la condición solo coincide con los activos que están asociados a todos los valores de etiqueta en <span class="codeph"> valueArray</span> (posiblemente además de otros valores de etiqueta). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
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

