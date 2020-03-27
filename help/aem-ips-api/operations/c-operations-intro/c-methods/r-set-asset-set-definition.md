---
description: Actualiza la definición definida para un conjunto de recursos existente.
seo-description: Actualiza la definición definida para un conjunto de recursos existente.
seo-title: setAssetSetDefinition
solution: Experience Manager
title: setAssetSetDefinition
topic: Scene7 Image Production System API
uuid: 2a2dce5d-7a01-49af-ac8b-33ae0b234ecc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetSetDefinition{#setassetsetdefinition}

Actualiza la definición definida para un conjunto de recursos existente.

Sintaxis

## Tipos de usuarios autorizados {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**Entrada (setAssetDefinitionParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con el conjunto de recursos. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador de conjunto de recursos |
| ` *`setDefinition`*` | `xsd:string` | Sí | Cadena de definición. Véase más abajo. |

**Salida (setAssetSetDefinitionReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Parámetro setDefinition: Acerca de {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**funciones setDefinition**

Especifique `setDefinition` las funciones de sustitución en línea. Se resuelven durante una búsqueda de catálogo o en una publicación. Las cadenas de sustitución tienen el formato `${<substitution_func>}`e incluyen lo siguiente:

>[!NOTE]
>
>Los literales de gestión de las listas de parámetros deben estar entre corchetes `([])`. El texto fuera de una cadena de sustitución se copia en la cadena de salida durante la resolución.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función de sustitución </th> 
   <th colname="col2" class="entry"> Devuelve el valor de </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Ruta del archivo maestro. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> ID del catálogo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([ <span class="varname"> asset_handle </span>],[ <span class="varname"> metadata_field_handle </span>]) </span> </td> 
   <td colname="col2"> Valor de metadatos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> ID del catálogo. Se aplica a recursos basados en imágenes (imagen, Vista ajustada, Vista de capas). <p>Para otros recursos, devuelve el ID de catálogo del recurso de miniatura (si lo hay). Si no hay ningún recurso de miniatura asociado al recurso, la función devuelve una cadena vacía. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplos de setDefinition**

Esta cadena de definición de conjunto de medios:

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

Se resuelve como sigue en tiempo de búsqueda o publicación:

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## Ejemplos {#section-739b42eec3074cafae285ec015a2d088}

**Solicitar**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**Respuesta**

Ninguno.
