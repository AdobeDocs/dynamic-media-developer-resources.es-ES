---
description: Devuelve recursos en función de una matriz de nombres de recursos.
solution: Experience Manager
title: getAssetsByName
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Developer,Administrator
exl-id: e48574e3-9d16-45fb-b4c8-98b5e092e611
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 14%

---

# getAssetsByName{#getassetsbyname}

Devuelve recursos en función de una matriz de nombres de recursos.

Sintaxis

## Tipos de usuarios autorizados {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Solo devuelve recursos a los que el usuario tiene acceso de lectura.

## Parámetros {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**Entrada (getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
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
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El identificador de la empresa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Proporciona acceso como otro usuario. Disponible solo para administradores. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Se utiliza para filtrar por un grupo específico. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Matriz de nombres de recursos que se van a recuperar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matriz de tipos de recurso permitidos para los recursos recuperados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matriz de tipos de recurso excluidos para los recursos recuperados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matriz de subtipos de recursos permitidos para los recursos recuperados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictoSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Si <span class="codeph"> true</span> y <span class="codeph"> assetSubTypeArray</span> no están vacíos, solo se devuelven los activos cuyos subtipos se encuentran en <span class="codeph"> assetSubTypeArray</span>. </p> <p>Si <span class="codeph"> es false</span>, se incluyen los activos sin ningún subtipo definido. </p> <p>El valor predeterminado es <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Contiene una lista de campos y subcampos incluidos en la respuesta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Contiene una lista de campos y subcampos excluidos de la respuesta. </td> 
  </tr> 
 </tbody> 
</table>

**Salida (getAssetsByNameReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`assetArray`*` | `types:AssetArray` | No | Matriz de recursos que coinciden con los criterios del filtro. |

## Ejemplos {#section-3b7447398e574c88aeaf8ca159cc78dd}

Este ejemplo de código devuelve dos recursos de tipo imagen.

**Solicitar**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**Respuesta**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```
