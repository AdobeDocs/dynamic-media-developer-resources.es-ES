---
description: Establece los valores de metadatos de un recurso. Funciona con una matriz de actualizaciones de metadatos para establecer valores en un lote.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
TQID: 'https://experienceleague.adobe.com/b8E8BK8pyJQiYlR2yNMbYPWcLVNfmAvI5WaOBuaBz1E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 8%

---

# setAssetMetadata{#setassetmetadata}

Establece los valores de metadatos de un recurso. Funciona con una matriz de actualizaciones de metadatos para establecer valores en un lote.

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
| companyHandle | `xsd:string` | Sí | El identificador de la compañía con el recurso que desea actualizar. |
| assetHandle | `xsd:string` | Sí | El identificador del recurso. |
| updateArray | `types:MetadataUpdateArray` | Sí | Actualizaciones en una matriz de actualización de metadatos. |

**Salida (setAssetMetadataReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-1ab412e7ee1d4d6d8469b0b403598c42}

Este ejemplo de código utiliza una matriz de actualizaciones de metadatos para establecer los metadatos del recurso especificado.

**Solicitud**

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

