---
description: Obtiene los tipos de conjunto de propiedades asociados con la compañía especificada o los tipos de conjunto de propiedades globales si no se especifica ninguna compañía.
seo-description: Obtiene los tipos de conjunto de propiedades asociados con la compañía especificada o los tipos de conjunto de propiedades globales si no se especifica ninguna compañía.
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
topic: Dynamic Media Image Production System API
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 12%

---


# getPropertySetTypes{#getpropertysettypes}

Obtiene los tipos de conjunto de propiedades asociados con la compañía especificada o los tipos de conjunto de propiedades globales si no se especifica ninguna compañía.

Sintaxis

## Tipos de usuarios autorizados {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-ac3ed9e036b54ea993f544046ff0e15d}

**Input (getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obligatorio </th> 
   <th colname="col4" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Identificador de la compañía con la que están asociados los tipos de conjunto de propiedades. <p>Omita si desea devolver tipos de conjuntos de propiedades globales. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getPropertySetTypesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`typeArray`*` | `types:PropertySetTypeArray` | Sí | Matriz de tipos de conjuntos de propiedades asociados con la compañía especificada o los tipos de conjuntos de propiedades globales si no se ha especificado ninguna compañía. |

## Ejemplos {#section-280c406a90864409856aee44d4069a52}

**Solicitar**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**Respuesta**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```

