---
title: createAssetSet
description: Crea un conjunto de recursos genérico con una cadena de definición de conjunto sin procesar para publicarlo en un servidor de imágenes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
TQID: 'https://experienceleague.adobe.com/ZpnD-Kj-3urMziRkX76TiD4cpqkJOyLxP9w2M2V50pM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 297
ht-degree: 6%

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El identificador de la compañía que contiene el conjunto de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El identificador de la carpeta en la que se crea el nuevo conjunto de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nombre </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Nombre del recurso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subtipo </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Un identificador único creado por el cliente para el tipo de conjunto de recursos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Los parámetros de la cadena de definición del conjunto. <p>Estos parámetros deben resolverse en el formato especificado por el visor de destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Controlador del recurso que actúa como miniatura para el nuevo conjunto de imágenes. Si no se especifica, IPS intenta utilizar el primer recurso de imagen al que hace referencia el conjunto. </td> 
  </tr> 
 </tbody> 
</table>

**Funciones de sustitución para setDefinition**

Puede especificar funciones de sustitución en línea que se resuelven durante la búsqueda o publicación del catálogo. Las cadenas de sustitución tienen el formato `${<substitution_func>}`. Las funciones disponibles se describen a continuación.

>[!NOTE]
>
>Los literales de identificador de las listas de parámetros deben estar entre corchetes `([])`. Todo el texto que esté fuera de una cadena de sustitución se copia literalmente en la cadena de salida durante la resolución.

| **Función de sustitución** | **Devuelve** |
|---|---|
| `getFilePath([asset_handle>])` | Ruta del archivo de origen principal del recurso. |
| `getCatalogId([<asset_handle>])` | El ID de catálogo del recurso. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Valores de metadatos para el recurso. |
| `getThumbCatalogId([<asset_handle>])` | El ID de catálogo del recurso (solo para recursos basados en imágenes). El ID de catálogo del recurso de la miniatura asociado (para otros recursos). Si un recurso de miniatura asociado no está disponible, la función devuelve una cadena vacía. |

**Cadena setDefinition de medios de muestra**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

En la búsqueda del catálogo o en el momento de la publicación, este proceso se resuelve en una cadena similar a la siguiente:

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Salida (createAssetSet)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| assetHandle | `xsd:string` | Sí | El identificador del conjunto de recursos. |

## Ejemplos {#section-fed53089de824d67ab96cd9103d384b4}

**Solicitud**

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
