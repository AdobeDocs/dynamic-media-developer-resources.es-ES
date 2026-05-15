---
description: Elimina un formato de publicación de viñeta.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
TQID: 'https://experienceleague.adobe.com/e1qIrpGHPuodTx79J1ke-7ULFptiCa6ZoIXyldJvSBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 12%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

Elimina un formato de publicación de viñeta.

## Tipos de usuarios autorizados {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-789625ba29df4b5f880914d4c64f77ce}

**Entrada (deleteVignettePublishFormatParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía a la que pertenece la viñeta. |
| vignetteFormatHandle | `xsd:string` | Sí | El identificador del formato de publicación de viñeta que se va a eliminar. |

**Salida (deleteVignettePublishFormatParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Este ejemplo de código elimina un formato de publicación de viñeta especificado por su identificador.

**Solicitud**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Respuesta**

Ninguno.
