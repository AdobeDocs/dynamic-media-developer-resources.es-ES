---
description: Elimina el campo de metadatos de una empresa.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
TQID: 'https://experienceleague.adobe.com/GnKkb-vTCdD5PwU111sxefzxR7FN74hk3i66c3gcH9I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 9%

---

# deleteMetadataField{#deletemetadatafield}

Elimina el campo de metadatos de una empresa.

Sintaxis

## Tipos de usuarios autorizados {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-73f12a30cc4340b6b32dd11effd5195e}

**Entrada (deleteMetadataFieldParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la empresa que contiene el campo de metadatos que se va a eliminar. |
| fieldHandle | `xsd:string` | Sí | El identificador del campo de metadatos que se va a eliminar. |

**Salida (deleteMetadataFieldParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Este ejemplo de código elimina el campo de metadatos de una empresa. Utiliza el identificador de empresa y el identificador de metadatos como campos del `deleteMetadataFieldParam` pasado al servidor de servicios web IPS para realizar esta acción.

**Solicitud**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Respuesta**

Ninguno.0

