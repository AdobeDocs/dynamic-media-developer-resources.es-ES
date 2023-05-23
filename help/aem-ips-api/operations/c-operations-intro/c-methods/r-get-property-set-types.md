---
description: Obtiene los tipos de conjuntos de propiedades asociados a los tipos de conjuntos de propiedades globales o compañía especificados si no se especifica ninguna compañía.
solution: Experience Manager
title: getPropertySetTypes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7686d30b-e071-4950-8af1-4dd25312ce4b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 15%

---

# getPropertySetTypes{#getpropertysettypes}

Obtiene los tipos de conjuntos de propiedades asociados a los tipos de conjuntos de propiedades globales o compañía especificados si no se especifica ninguna compañía.

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

**Entrada (getPropertySetTypesParam)**

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
   <td colname="col4">El identificador de la compañía a la que están asociados los tipos de conjuntos de propiedades. <p>Omita si desea devolver tipos de conjuntos de propiedades globales. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (getPropertySetTypesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| typeArray | `types:PropertySetTypeArray` | Sí | Una matriz de tipos de conjuntos de propiedades asociados a la compañía especificada o los tipos de conjuntos de propiedades globales si no se especificó ninguna compañía. |

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
