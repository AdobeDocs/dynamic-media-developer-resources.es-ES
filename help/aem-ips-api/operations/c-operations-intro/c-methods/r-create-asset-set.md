---
description: Crea un conjunto de recursos genérico con una cadena de definición de conjunto sin procesar que se publicará en un servidor de imágenes.
solution: Experience Manager
title: createAssetSet
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 10%

---


# createAssetSet{#createassetset}

Crea un conjunto de recursos genérico con una cadena de definición de conjunto sin procesar que se publicará en un servidor de imágenes.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El identificador de la empresa que contendrá el conjunto de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El identificador de la carpeta en la que se creará el nuevo conjunto de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Nombre del recurso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Identificador único creado por el cliente para el tipo de conjunto de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Los parámetros de la cadena de definición del conjunto. <p>Deben resolverse en el formato especificado por el visor de destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Control del recurso que actúa como la miniatura del nuevo conjunto de imágenes. Si no se especifica, IPS intenta utilizar el primer recurso de imagen al que hace referencia el conjunto. </td> 
  </tr> 
 </tbody> 
</table>

**Funciones de sustitución para setDefinition**

Puede especificar funciones de sustitución en línea que se resuelvan durante la búsqueda o publicación del catálogo. Las cadenas de sustitución tienen el formato `${<substitution_func>}`. A continuación se enumeran las funciones disponibles.

>[!NOTE]
>
>Los literales de control de las listas de parámetros deben estar entre corchetes `([])`. Todo el texto que está fuera de una cadena de sustitución se copia literalmente en la cadena de salida durante la resolución.

| **Función de sustitución** | **Devuelve** |
|---|---|
| `getFilePath([asset_handle>])` | Ruta del archivo de origen principal del recurso. |
| `getCatalogId([<asset_handle>])` | El ID de catálogo del recurso. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Valores de metadatos del recurso. |
| `getThumbCatalogId([<asset_handle>])` | El ID de catálogo del recurso (solo para recursos basados en imágenes). El ID de catálogo del recurso principal asociado (para otros recursos). Si un recurso de miniatura asociado no está disponible, la función devuelve una cadena vacía. |

**Cadena Media setDefinition de muestra**

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
| `*`assetHandle`*` | `xsd:string` | Sí | El identificador del conjunto de recursos. |

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

