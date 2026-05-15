---
description: Obtiene todos los trabajos activos actualmente.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
TQID: 'https://experienceleague.adobe.com/YTwzh2h9wVPuURKL5nNFoac2SruwYXDw9oWtd-vzowc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 14%

---

# getActiveJobs{#getactivejobs}

Obtiene todos los trabajos activos actualmente.

Sintaxis

## Tipos de usuarios autorizados {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**Entrada (getActiveJobsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | No | El identificador de la compañía. |
| jobHandle | `xsd:string` | No | El identificador del trabajo. |
| originalName | `xsd:string` | No | Nombre del trabajo original. |

**Salida (getActiveJobsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| jobArray | `xsd:string` | Sí | Matriz de trabajos activos. |

## Ejemplos {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Este ejemplo de código devuelve todos los trabajos activos de una empresa que se ejecuta en IPS. En este caso, la respuesta es inusual porque el coordinador de programación de IPS está deshabilitado y no se están ejecutando trabajos activos. En circunstancias normales, la respuesta devolverá una serie de trabajos activos.

**Solicitud**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**Respuesta**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```
