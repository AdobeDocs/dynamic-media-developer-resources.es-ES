---
description: Valores válidos para los campos PropertySetType y createPropertySetTypeParam.
seo-description: Valores válidos para los campos PropertySetType y createPropertySetTypeParam.
seo-title: PropertySetType
solution: Experience Manager
title: PropertySetType
topic: Scene7 Image Production System API
uuid: 83220180-3272-4552-974d-a73e6aad3483
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PropertySetType{#propertysettype}

Valores válidos para los campos PropertySetType y createPropertySetTypeParam.

Los valores incluyen:

* `UserProperty`
* `CompanyProperty`
* `UserCompanyProperty`

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> typeHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Identificador de tipo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Identificador de Compañía. <p>Nota:  El tipo es global si el controlador de compañía no está presente. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Escriba el nombre. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> propertyType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Uno de los tipos de conjuntos de propiedades. Consulte Entrada (<span class="codeph"> createPropertySetTypeParam</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> allowMultiple</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Si se permiten varias instancias de conjuntos de propiedades para adjuntar a un objeto de este tipo. </td> 
  </tr> 
 </tbody> 
</table>

