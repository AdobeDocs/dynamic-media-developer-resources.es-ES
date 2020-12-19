---
description: Obtiene todos los trabajos activos actualmente.
seo-description: Obtiene todos los trabajos activos actualmente.
seo-title: getActiveJobs
solution: Experience Manager
title: getActiveJobs
topic: Scene7 Image Production System API
uuid: 3231d349-b254-4dd0-804d-8beaab116b56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
| ` *`companyHandle`*` | `xsd:string` | No | El identificador de la compañía. |
| ` *`jobHandle`*` | `xsd:string` | No | El identificador del trabajo. |
| ` *`originalName`*` | `xsd:string` | No | Nombre del trabajo original. |

**Salida (getActiveJobsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`jobArray`*` | `xsd:string` | Sí | Matriz de trabajos activos. |

## Ejemplos {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Este ejemplo de código devuelve todos los trabajos activos de una compañía que se ejecuta en IPS. En este caso, la respuesta es inusual porque el coordinador de programación IPS está deshabilitado sin trabajos activos en ejecución. En circunstancias normales, la respuesta devolverá una serie de trabajos activos.

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

