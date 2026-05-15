---
description: Detiene un trabajo en curso.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
TQID: 'https://experienceleague.adobe.com/L72oxdH9gFQcXgjbWznsuVGV0-UCQXLShJm-DvbZd8Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 54
ht-degree: 18%

---

# stopJob{#stopjob}

Detiene un trabajo en curso.

Sintaxis

## Tipos de usuarios autorizados {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-2b64f074e37c4c38849994f3bc65342a}

**Entrada (stopJobParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Manejo de la compañía. |
| jobHandle | `xsd:string` | Sí | Gestione el trabajo que desea detener. |

**Salida (stopJobReturn0**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Solicitud**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Respuesta**

Ninguno.
