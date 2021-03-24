---
description: Obtiene un tipo de conjunto de propiedades mediante un identificador de una empresa y el nombre del tipo de conjunto de propiedades. Obtiene una estructura de tipo con el identificador del tipo y el tipo de propiedad.
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 11%

---


# getPropertySetType{#getpropertysettype}

Obtiene un tipo de conjunto de propiedades mediante un identificador de una empresa y el nombre del tipo de conjunto de propiedades. Obtiene una estructura de tipo con el identificador del tipo y el tipo de propiedad.

Sintaxis

## Tipos de usuarios autorizados {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-c9a53400c44744668bd7915f72d2bf3d}

**Entrada (getPropertySetTypeParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | No | El identificador de la empresa. Opcional porque un tipo de conjunto de propiedades puede pertenecer a varias empresas. |
| `*`name`*` | `xsd:string` | Sí | Nombre del tipo del conjunto de propiedades. |

**Salida (getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PropertySetType</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4">La estructura de tipo que contiene: 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">Gestionar. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">Escriba el nombre. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">Tipo de propiedad. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">Valor que indica si el tipo permite varios tipos de propiedad. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplos {#section-1b57199415e34a8fa449f864f8895b14}

Este ejemplo de código devuelve un tipo de conjunto de propiedades por nombre.

**Solicitar**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**Respuesta**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```

