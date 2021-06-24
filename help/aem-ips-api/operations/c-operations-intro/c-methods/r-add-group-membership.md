---
description: Agrega un usuario a una matriz de grupos.
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: c5b5e155-d285-4304-98bc-1d938793e2c0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 14%

---

# addGroupMembership{#addgroupmembership}

Agrega un usuario a una matriz de grupos.

Sintaxis

## Tipos de usuarios autorizados {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-e250f6ddb13646808c6a8860b6442bc5}

**Entrada (addGroupMembershipParam)**

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Gestione al usuario cuya pertenencia a un grupo desee añadir. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Matriz de identificadores de los grupos a los que desea que pertenezca la empresa. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (addGroupMembershipParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-f7a1f40c3d7a40ea964b29056c734d81}

En este ejemplo se agrega un grupo a una empresa con `*`groupHandleArray`*`. Este ejemplo utiliza un solo grupo.

**Solicitar**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Respuesta**

Ninguno.
