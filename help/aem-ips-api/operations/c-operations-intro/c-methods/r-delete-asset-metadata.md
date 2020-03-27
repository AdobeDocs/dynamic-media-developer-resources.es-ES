---
description: Elimina los valores de metadatos de un recurso. Funciona con una matriz de eliminación de metadatos para definir valores en un lote.
seo-description: Elimina los valores de metadatos de un recurso. Funciona con una matriz de eliminación de metadatos para definir valores en un lote.
seo-title: deleteAssetMetadata
solution: Experience Manager
title: deleteAssetMetadata
topic: Scene7 Image Production System API
uuid: 2dc783c6-23da-4a94-8780-3c4ec88ff3f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteAssetMetadata{#deleteassetmetadata}

Elimina los valores de metadatos de un recurso. Funciona con una matriz de eliminación de metadatos para definir valores en un lote.

Sintaxis

## Tipos de usuarios autorizados {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y eliminación al recurso.

## Parámetros {#section-0eed164e278b456fbdfb7a50727a0416}

**Entrada (deleteAssetMetadataParam)**

<table id="table_A4438E2FE5F245E5B73F46CD887BE70F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>companyHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Identificador de la compañía a la que pertenece la carpeta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>assetHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Identificador del recurso que se va a eliminar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>metadataDelete </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Metadatos que se van a eliminar del recurso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>deleteArray </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:MetadataDeleteArray</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Matriz de metadatos para eliminar del recurso. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (deleteAssetMetadataParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-d5657289f5234bb0a613dcf691507958}

MetadataDelete

```java
    <complexType name="MetadataDelete">
        <sequence>
            <element name="fieldHandle" type="xsd:string"/>
        </sequence>
    </complexType>
```

Llamada de ejemplo

```java
<ac:Request id="deleteAssetMetadata">
 <deleteAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
  <companyHandle>c|101</companyHandle>
  <assetHandle>a|202</assetHandle>
  <deleteArray>
   <items>
    <fieldHandle>m|2919|ASSET|UntypedUDFField1395788289789</fieldHandle>
   </items>
  </deleteArray>
 </deleteAssetMetadataParam>
</ac:Request>
```

