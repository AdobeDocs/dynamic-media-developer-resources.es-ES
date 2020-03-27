---
description: Establece los valores de metadatos de un recurso. Funciona con una matriz de actualizaciones de metadatos para definir valores en un lote.
seo-description: Establece los valores de metadatos de un recurso. Funciona con una matriz de actualizaciones de metadatos para definir valores en un lote.
seo-title: setAssetMetadata
solution: Experience Manager
title: setAssetMetadata
topic: Scene7 Image Production System API
uuid: 17fe8277-a164-4f91-af96-ea43d41bd4f2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetMetadata{#setassetmetadata}

Establece los valores de metadatos de un recurso. Funciona con una matriz de actualizaciones de metadatos para definir valores en un lote.

Sintaxis

## Tipos de usuarios autorizados {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura al recurso.

## Parámetros {#section-bcdcff30905e444388811e897b2824bd}

**Entrada (setAssetMetadataParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con el recurso que desea actualizar. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador del recurso. |
| ` *`updateArray`*` | `types:MetadataUpdateArray` | Sí | Actualizaciones en una matriz de actualizaciones de metadatos. |

**Salida (setAssetMetadataReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-1ab412e7ee1d4d6d8469b0b403598c42}

Este ejemplo de código utiliza una matriz de actualizaciones de metadatos para establecer los metadatos del recurso especificado.

**Solicitar**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**Respuesta**

Ninguno.
