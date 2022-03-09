---
description: Obtiene todos los trabajos activos actualmente.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 16%

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
| companyHandle | `xsd:string` | No | El identificador de la empresa. |
| jobHandle | `xsd:string` | No | El identificador del trabajo. |
| originalName | `xsd:string` | No | Nombre del trabajo original. |

**Salida (getActiveJobsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| jobArray | `xsd:string` | Sí | Matriz de trabajos activos. |

## Ejemplos {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Este ejemplo de código devuelve todos los trabajos activos de una empresa que se ejecuta en IPS. En este caso, la respuesta es inusual porque el coordinador de programación IPS está deshabilitado sin trabajos activos en ejecución. En circunstancias normales, la respuesta devolverá una serie de trabajos activos.

**Solicitar**

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
