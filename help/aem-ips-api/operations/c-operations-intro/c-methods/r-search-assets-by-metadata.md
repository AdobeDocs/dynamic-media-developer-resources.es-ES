---
description: Busca en el repositorio de índices de metadatos los términos de búsqueda dados. Devuelve datos de recursos como el método searchAssets.
seo-description: Busca en el repositorio de índices de metadatos los términos de búsqueda dados. Devuelve datos de recursos como el método searchAssets.
seo-title: searchAssetsByMetadata
solution: Experience Manager
title: searchAssetsByMetadata
topic: Scene7 Image Production System API
uuid: f4119ee9-f6d8-49fb-9d8c-bb200951d983
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# searchAssetsByMetadata{#searchassetsbymetadata}

Busca en el repositorio de índices de metadatos los términos de búsqueda dados. Devuelve datos de recursos como el método searchAssets.

Aunque `searchAssetsByMetadata` le permite buscar campos de metadatos definidos por el usuario, estos campos no se devuelven si se especifican en el `responseMetadataArray`. Para ilustrar este punto, el siguiente ejemplo de código:

```java
<ns:responseMetadataArray>
 <ns:items>custom_attributes.x</ns:items>
</ns:responseMetadataArray>
```

devuelve un valor nulo:

```java
<items>
 <name>custom_attributes.x</name>
 <value>null</value>
</items>
```

Para solucionar este problema, puede utilizar el `fieldHandles` de los recursos devueltos por la búsqueda para ejecutarlos `getAssets` (consulte también [getAssets](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca)). Este método obtiene los valores de campos definidos por el usuario para los recursos en cuestión. Utilice el siguiente ejemplo de sintaxis para buscar campos de metadatos definidos por el usuario:

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## Tipos de usuarios autorizados {#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-5f1edb9c5b914160ab361f4364b8aa8d}

**Entrada (searchAssetsByMetadataParam)**

<table id="table_8FF228D6279241849F3D9E5BA080580C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>El identificador de la compañía. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> Filtro</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipo:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Filtros que ayudan a definir los criterios de búsqueda. </p> <p>Consulte <a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> SearchFilter</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> metadataConditionArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Condiciones que definen los criterios de búsqueda. Consulte a continuación para obtener más información. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> responseMetadataArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:StringArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Campos adicionales que desea rellenar en la respuesta en el resumen de recursos. Los campos deben especificarse en el formato normalizado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> recordsPerPage</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Número de recursos devueltos por la respuesta. El valor predeterminado es 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resultsPage</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Especifica la página de resultados que se devolverá en función del tamaño de página <span class="codeph"> recordsPerPage</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sortBy</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Ordenar por campo de recurso seleccionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sortDirection</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Elección de la dirección de clasificación. De subida es el valor predeterminado. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (searchAssetsByMetadataReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`totalRows`*` | `xsd:int` | No | Número de coincidencias. |
| ` *`assetArray`*` | `types:AssetArray` | No | Matriz de recursos devueltos por la búsqueda. |

## detalles de metadataConditionArray {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

**Estructura del elemento**

`metadataConditionArray` la estructura es la siguiente:

```java
<ns1:items>
   <ns:fieldHandle>field_handle</ns:fieldHandle>
   <ns:op>operator</ns:op>
   <ns:value>comparison_value</ns:value>
</ms1:items>
```

**Valores**

`field_handle` es la clave de búsqueda de metadatos. Puede contener notación de puntos. Los valores posibles incluyen:

* `asset_id` (sin prefijo)
* `name`
* `folder_path`
* `type`
* `file_name`
* `description`
* `comment`
* `user_data`
* `sku`
* `modified_at`
* `modified_by`
* `created_at` (igual que `modified_at` (Fecha en el formulario: 25 de julio de 2014 22:13:45 GMT-0500 (CDT))

* `created_by`

**Operadores permitidos**

El [!DNL operator] define cómo comparar el valor e incluye:

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

El término `comparison_value` es el que se busca.

## Ejemplos {#section-53a12b9c023e4e629eddf5719c955ad4}

Este ejemplo de código realiza una búsqueda con los siguientes criterios de metadatos:

* `name` contiene `1000801`.

* `dc.rights` field es igual a `Per Jessen Schmidt`.

**Solicitar**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
          <xsd:user>user@adobe.com</xsd:user>
          <xsd:password>topSecret</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
      <ns:searchAssetsByMetadataParam>
         <ns:companyHandle>c|656</ns:companyHandle>
         <ns:metadataConditionArray>
            <ns:items>
               <ns:fieldHandle>name</ns:fieldHandle>
               <ns:op>Contains</ns:op>
               <ns:value>1000801</ns:value>
            </ns:items>
            <ns:items>
               <ns:fieldHandle>dc.rights</ns:fieldHandle>
               <ns:op>Equals</ns:op>
               <ns:value>Per Jessen Schmidt</ns:value>
            </ns:items>
         </ns:metadataConditionArray>
         <ns:responseMetadataArray>
            <ns:items>dc.subject</ns:items>
            <ns:items>xmp.CreatorTool</ns:items>
         </ns:responseMetadataArray>
      </ns:searchAssetsByMetadataParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Respuesta**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <searchAssetsByMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <totalRows>1</totalRows>
         <assetSummaryArray>
            <items>
               <assetHandle>a|885289</assetHandle>
               <type>Image</type>
               <name>test9-1000801</name>
               <folder>Extroscope/Test subfolders/</folder>
               <filename>test9-1000801.jpg</filename>
               <created>2009-11-19T07:21:24.252-08:00</created>
               <createUser>pschmidt@adobe.com</createUser>
               <lastModified>2009-11-19T07:21:25.487-08:00</lastModified>
               <lastModifyUser>pschmidt@adobe.com</lastModifyUser>
               <metadataArray>
                  <items>
                     <name>dc.subject</name>
                     <value>[San Fransico, USA</value>
                  </items>
                  <items>
                     <name>xmp.CreatorTool</name>
                     <value>Ver.1.0</value>
                  </items>
               </metadataArray>
            </items>
         </assetSummaryArray>
      </searchAssetsByMetadataReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

