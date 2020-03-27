---
description: Crea un conjunto de recursos genérico con una cadena de definición de conjunto sin procesar para publicarlo en un servidor de imágenes.
seo-description: Crea un conjunto de recursos genérico con una cadena de definición de conjunto sin procesar para publicarlo en un servidor de imágenes.
seo-title: createAssetSet
solution: Experience Manager
title: createAssetSet
topic: Scene7 Image Production System API
uuid: 1e86bd37-511c-4c12-abfd-075053b86f78
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# createAssetSet{#createassetset}

Crea un conjunto de recursos genérico con una cadena de definición de conjunto sin procesar para publicarlo en un servidor de imágenes.

Sintaxis

## Tipos de usuarios autorizados {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-3580b586296e42a5b21426085b1bb72d}

**Entrada (createAssetSet)**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Identificador de la compañía que contendrá el conjunto de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Identificador de la carpeta en la que se creará el nuevo conjunto de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Nombre del recurso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Identificador único creado por el cliente para el tipo de conjunto de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Parámetros de la cadena de definición establecida. <p>Deben resolverse en el formato especificado por el visor de destinatario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Control del recurso que actúa como miniatura para el nuevo conjunto de imágenes. Si no se especifica, IPS intenta utilizar el primer recurso de imagen al que hace referencia el conjunto. </td> 
  </tr> 
 </tbody> 
</table>

**Funciones de sustitución para setDefinition**

Puede especificar las funciones de sustitución en línea que se resuelven durante la búsqueda o publicación del catálogo. Las cadenas de sustitución tienen el formato `${<substitution_func>}`. A continuación se enumeran las funciones disponibles.

>[!NOTE]
>
>Los literales de control de las listas de parámetros deben estar entre corchetes `([])`. Todo el texto que está fuera de una cadena de sustitución se copia literalmente en la cadena de salida durante la resolución.

| **Función de sustitución** | **Devuelve** |
|---|---|
| `getFilePath([asset_handle>])` | Ruta del archivo maestro del recurso. |
| `getCatalogId([<asset_handle>])` | El ID de catálogo del recurso. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Valores de metadatos del recurso. |
| `getThumbCatalogId([<asset_handle>])` | El ID de catálogo del recurso (solo para recursos basados en imágenes). El ID de catálogo del recurso de miniatura asociado (para otros recursos). Si un recurso de miniatura asociado no está disponible, la función devuelve una cadena vacía. |

**Cadena de definición de conjunto de medios de muestra**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

En el momento de la búsqueda o publicación del catálogo, esto se resuelve en una cadena similar a la siguiente:

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Salida (createAssetSet)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador del conjunto de recursos. |

## Ejemplos {#section-fed53089de824d67ab96cd9103d384b4}

**Solicitar**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**Respuesta**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```

