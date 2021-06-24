---
description: Define la lista de recursos asociados a un conjunto de imágenes.
solution: Experience Manager
title: setImageSetMembers
feature: Dynamic Media Classic,SDK/API,Conjuntos de imágenes
role: Developer,Administrator
exl-id: c30df5fe-e355-45d4-8c06-e396caca0d58
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 12%

---

# setImageSetMembers{#setimagesetmembers}

Define la lista de recursos asociados a un conjunto de imágenes.

Esta operación ignora el parámetro `pageReset` para `ImageSets` y `SpinSets` y fuerza el valor a true.

## Tipos de usuarios autorizados {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura al recurso del conjunto de imágenes y acceso de lectura a cada recurso miembro.

## Parámetros {#section-2f46efcd24c648aeacba738509426e46}

**Entrada (setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Identificador de la empresa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Controlador del conjunto de imágenes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Matriz de miembros de recursos que pertenecen al conjunto de imágenes. </td> 
  </tr> 
 </tbody> 
</table>

**Salida (setImageSetMembersReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-7b87219034464aa98524178ccee27738}

Este ejemplo de código utiliza una matriz de miembros para establecer los miembros de un conjunto de imágenes.

**Solicitar**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**Respuesta**

Ninguno.
