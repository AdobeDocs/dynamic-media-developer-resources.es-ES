---
description: Mueve varios recursos independientemente entre sí. Para ello, se utiliza el tipo AssetMove incluido en assetMoveArray. Cada campo AssetMove contiene una carpeta de destino.
seo-description: Mueve varios recursos independientemente entre sí. Para ello, se utiliza el tipo AssetMove incluido en assetMoveArray. Cada campo AssetMove contiene una carpeta de destino.
seo-title: moveAssets
solution: Experience Manager
title: moveAssets
topic: Scene7 Image Production System API
uuid: 178f9979-fff5-45ce-a001-1263d1770ea8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveAssets{#moveassets}

Mueve varios recursos independientemente entre sí. Para ello, se utiliza el tipo AssetMove incluido en assetMoveArray. Cada campo AssetMove contiene una carpeta de destino.

Sintaxis

## Tipos de usuarios autorizados {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-7d47f663474b41cc83439288ac133cc5}

**Entrada (moveAssetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con los recursos que se van a mover. |
| ` *`assetMoveArray`*` | `types:AssetMoveArray` | Sí | Matriz de movimiento de recursos. Contiene un recurso y una carpeta de destino de recursos. |

**Output (moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El recuento de recursos se movió correctamente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Recuento de recursos que generaban advertencias cuando la operación intentaba moverlos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Recuento de recursos que generaban errores cuando la operación intentaba moverlos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <span class="codeph"></span>AssetOperationFaults que contienen: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Recursos que generaron las advertencias. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Códigos de advertencia. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Motivo de la advertencia. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <span class="codeph"></span>AssetOperationFaults que contienen: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Recursos que generaron los errores. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Códigos de error. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Motivo de los errores. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplos {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

Este ejemplo de código mueve los recursos a una ubicación específica especificada por el `assetMoveArray`. La matriz incluye el identificador de recurso y su identificador de carpeta. La respuesta indica que los recursos se movieron correctamente.

**Solicitar**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**Respuesta**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

