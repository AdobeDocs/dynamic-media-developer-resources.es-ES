---
description: Elimina un trabajo actual o programado.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
TQID: 'https://experienceleague.adobe.com/rcnHChrY2u5J1-ipPlJ7JilCfbsTHDNDHhqJlLZuWIQ'
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
source-wordcount: 90
ht-degree: 11%

---

# deleteJob{#deletejob}

Elimina un trabajo actual o programado.

Sintaxis

## Tipos de usuarios autorizados {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-000c42bc93744b1a8e777f3ec3c272b0}

**Entrada (deleteJobParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía a la que pertenece el trabajo. |
| jobHandle | `xsd:string` | Sí | El identificador del trabajo que se va a eliminar. |

**Salida**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Este ejemplo de código elimina un trabajo que se está ejecutando o que está programado para ejecutarse en IPS. Requiere un identificador de trabajo, que debe obtener de otra operación.

**Solicitud**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Respuesta**

Ninguno.
