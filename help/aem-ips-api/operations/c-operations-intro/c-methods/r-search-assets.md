---
description: Busque recursos en función de los criterios especificados.
solution: Experience Manager
title: searchAssets
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 12%

---


# searchAssets{#searchassets}

Busque recursos en función de los criterios especificados.

Sintaxis

## searchAssets: Acerca de {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` es el método principal para recuperar recursos IPS. Este método se utiliza para varios fines, como explorar la jerarquía de carpetas o encontrar un recurso específico por su nombre.

**Tamaño de respuesta**

`searchAssets` devuelve hasta 1000 activos en una sola llamada. Para devolver hasta 10 000 activos por llamada, limite los datos de respuesta a un subconjunto de los campos `totalRows`, `name`, `handle`, `type` y `subType`. Para devolver conjuntos más grandes, configure la paginación con el parámetro `resultPage`.

**Limitar tamaño de archivo de resultado con responseFieldArray o excludeFieldArray**

Limite el tamaño del conjunto de datos con los parámetros `responseFieldArray` o `excludFieldArray` . Estos parámetros ayudan a reducir el uso de memoria y el ancho de banda y pueden mejorar los tiempos de respuesta del servidor.

## Tipos de usuarios autorizados {#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura para devolver recursos.

## Parámetros {#section-49aabc0600764f55a8b7017d86ded44f}

**Entrada (searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obligatorio? </th> 
   <th colname="col4" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El identificador de la empresa con los recursos que desea buscar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Permite que los administradores trabajen como usuarios diferentes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Permite que los administradores trabajen como parte de un grupo diferente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> carpeta</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Ruta raíz para buscar recursos. Si se omite, se utiliza la carpeta raíz de la empresa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Configúrelo en <span class="codeph"> true</span> para buscar subcarpetas. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Opción de estado de publicación. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Selección del estado de la papelera. El valor predeterminado es <span class="codeph"> NotInTrash</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Elección de modos de coincidencia de búsqueda para combinar los resultados de <span class="codeph"> keywordArray</span>, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span> y  <span class="codeph"> metadataConditionArray</span>. El valor predeterminado es <span class="codeph"> MatchAll</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> <p>Nota:  Parámetro obsoleto. Se recomienda que no lo use. </p> </p> <p>Una matriz de cadenas de palabras clave que se deben coincidir. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Elección de modos de coincidencia de búsqueda para combinar las coincidencias de <span class="codeph"> systemFieldCondition</span>. El valor predeterminado es <span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipos:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matriz de condiciones de campo del sistema. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Constantes de cadena de los modos de coincidencia de búsqueda. El valor predeterminado es <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:TagConditionArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Una matriz de predicados de búsqueda de campos de etiqueta. </p> <p>Los predicados se combinan según la configuración <span class="codeph"> tagMatchMode</span> y luego se combinan con cualquier término de <span class="codeph"> keywordArray</span>, <span class="codeph"> systemFieldConditionArray</span> y <span class="codeph"> metadataConditionArray</span> según la configuración <span class="codeph"> conditionMatchMode</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Buscar modos de coincidencia para combinar las coincidencias <span class="codeph"> metadataCondition</span>. El valor predeterminado es <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipos:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matriz de condiciones de búsqueda de campos de metadatos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matriz de tipos de recursos que se incluyen en la búsqueda. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matriz de tipos de recursos que se excluirán de la búsqueda. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Una lista de nombres de subtipos con los que filtrar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictoSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Si <span class="codeph"> true</span> y <span class="codeph"> assetSubTypeArray</span> no están vacíos, solo se devuelven los activos cuyos subtipos se encuentran en <span class="codeph"> assetSubTypeArray</span>. Si <span class="codeph"> es false</span> (valor predeterminado), se devuelven los recursos sin ningún subtipo definido. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Si el valor es true, los recursos de subproducto generados durante la ingesta de un recurso principal, como las imágenes de página PDF dañadas, se excluyen de los resultados de búsqueda. El valor predeterminado es false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipos:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matriz de condiciones de generación de recursos de subproducto para excluir de los resultados de búsqueda. Si está presente, este parámetro anula la configuración excludeByproducts . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sting</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Gestión de un proyecto que contiene los recursos que se van a buscar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Número máximo de resultados que se van a devolver. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Especifica la página de resultados que se van a devolver, en función del tamaño de página <span class="codeph"> recordsPerPage</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Selección de los campos de ordenación de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Elección de la dirección. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Contiene una lista de campos y subcampos para su inclusión en la respuesta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Contiene una lista de campos y subcampos para su exclusión de la respuesta. </td> 
  </tr> 
 </tbody> 
</table>

**Salida (searchAssetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`totalRows`*` | `xsd:int` | No | Número de filas que devuelve una búsqueda cuando los registros por página no están limitados. |
| `*`assetArray`*` | `types:AssetArray` | No | Recursos que devuelve la búsqueda. |

## Ejemplos {#section-725484cc09b54772a838ad2cc930b94b}

Este ejemplo de código busca recursos de imagen que pertenecen a una empresa específica. La respuesta se trunca para su brevedad.

**Solicitar**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**Respuesta**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```

