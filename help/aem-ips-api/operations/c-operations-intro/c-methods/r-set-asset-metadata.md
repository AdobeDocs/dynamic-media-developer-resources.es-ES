---
description: Define los valores de metadatos de un recurso. Funciona con una matriz de actualizaciones de metadatos para establecer valores en un lote.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadatos,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---


# setAssetMetadata{#setassetmetadata}

Define los valores de metadatos de un recurso. Funciona con una matriz de actualizaciones de metadatos para establecer valores en un lote.

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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con el recurso que desea actualizar. |
| `*`assetHandle`*` | `xsd:string` | Sí | El identificador del recurso. |
| `*`updateArray`*` | `types:MetadataUpdateArray` | Sí | Actualizaciones en una matriz de actualización de metadatos. |

**Salida (setAssetMetadataReturn)**

La API IPS no devuelve una respuesta para esta operación.

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
