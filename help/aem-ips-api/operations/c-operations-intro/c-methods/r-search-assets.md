---
description: Busque recursos en función de los criterios especificados.
solution: Experience Manager
title: searchAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 58bd80e4-e9eb-43e4-8508-04e330f0ad26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 6%

---

# searchAssets{#searchassets}

Busque recursos en función de los criterios especificados.

Sintaxis

## searchAssets: Acerca de {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` es el método principal para recuperar recursos IPS. Este método se utiliza para varios fines, como examinar la jerarquía de carpetas o buscar un recurso específico por su nombre.

**Tamaño de respuesta**

`searchAssets` devuelve hasta 1000 recursos en una sola llamada. Para devolver hasta 10 000 recursos por llamada, limite los datos de respuesta a un subconjunto de los campos `totalRows`, `name`, `handle`, `type` y `subType`. Para devolver conjuntos más grandes, configure la paginación con el parámetro `resultPage`.

**Limitar tamaño del archivo de resultados con responseFieldArray o excludeFieldArray**

Limite el tamaño del conjunto de datos con los parámetros `responseFieldArray` o `excludFieldArray`. Estos parámetros ayudan a reducir el uso de memoria y el ancho de banda, y pueden mejorar los tiempos de respuesta del servidor.

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
>El usuario debe tener acceso de lectura para devolver los recursos.

## Parámetros {#section-49aabc0600764f55a8b7017d86ded44f}

**Entrada (searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> ¿Requerido? </th> 
   <th colname="col4" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El identificador de la compañía con los recursos que desea buscar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Permite que los administradores trabajen como un usuario diferente. </td> 
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
   <td colname="col4"> Ruta de acceso raíz para buscar recursos. Si se omite, se utiliza la carpeta raíz de la compañía. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Se establece en <span class="codeph"> true</span> para buscar subcarpetas. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Opción de estado de Publish. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Opción de estado de papelera. El valor predeterminado es <span class="codeph"> NotInTrash</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Elección de modos de coincidencia de búsqueda para combinar los resultados de <span class="codeph"> keywordArray</span>, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span> y <span class="codeph"> metadataConditionArray</span>. El valor predeterminado es <span class="codeph"> MatchAll</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> <p>Nota: Parámetro obsoleto. Se aconseja que no lo use. </p> </p> <p>Matriz de palabras clave de cadena que debe coincidir. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Elección de modos de coincidencia de búsqueda para combinar <span class="codeph"> coincidencias de systemFieldCondition</span>. El valor predeterminado es <span class="codeph"> MatchAll</span> </p>. </td> 
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
   <td colname="col4">Constantes de cadena de Modos de coincidencia de búsqueda. El valor predeterminado es <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:TagConditionArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Matriz de predicados de búsqueda de campos de etiquetas. </p> <p>Los predicados se combinan según la configuración <span class="codeph"> tagMatchMode</span> y, a continuación, se combinan con cualquier término de <span class="codeph"> keywordArray</span>, <span class="codeph"> systemFieldConditionArray</span> y <span class="codeph"> metadataConditionArray</span> según la configuración de <span class="codeph"> conditionMatchMode</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Buscar modos de coincidencia para combinar <span class="codeph"> coincidencias metadataCondition</span>. El valor predeterminado es <span class="codeph"> MatchAll</span>. </td> 
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
   <td colname="col4"> Matriz de tipos de recursos que se incluirán en la búsqueda. </td> 
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
   <td colname="col4"> Una lista de nombres de subtipo con los que filtrar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Si <span class="codeph"> true</span> y <span class="codeph"> assetSubTypeArray</span> no están vacíos, solo se devuelven los recursos cuyos subtipos están en <span class="codeph"> assetSubTypeArray</span>. Si <span class="codeph"> es false</span> (predeterminado), se devuelven recursos sin un subtipo definido. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Si el valor es True, los recursos de subproductos generados durante la ingesta de un recurso principal, como las imágenes de página de PDF copiadas desde CD, se excluyen de los resultados de búsqueda. El valor predeterminado es false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipos:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matriz de condiciones de generación de recursos de subproductos que se excluirán de los resultados de búsqueda. Si está presente, este parámetro anula la configuración excludeByproducts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Controlador de un proyecto que contiene los recursos que se van a buscar. </td> 
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
   <td colname="col4">Especifica la página de resultados que se va a devolver, en función de <span class="codeph"> recordsPerPage</span> tamaño de página. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Elección de los campos de ordenación de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Elección de la dirección del orden. </td> 
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
   <td colname="col4"> Contiene una lista de campos y subcampos para la exclusión de la respuesta. </td> 
  </tr> 
 </tbody> 
</table>

**Salida (searchAssetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| totalRows | `xsd:int` | No | Número de filas que devuelve una búsqueda cuando los registros por página no están limitados. |
| assetArray | `types:AssetArray` | No | Assets que devuelve la búsqueda. |

## Ejemplos {#section-725484cc09b54772a838ad2cc930b94b}

Este ejemplo de código busca recursos de imagen que pertenecen a una compañía específica. La respuesta se trunca por su brevedad.

**Solicitud**

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
