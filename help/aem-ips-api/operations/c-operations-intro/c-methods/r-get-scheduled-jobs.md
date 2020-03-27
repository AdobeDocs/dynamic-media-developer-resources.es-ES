---
description: Obtiene los trabajos programados para ejecutarse.
seo-description: Obtiene los trabajos programados para ejecutarse.
seo-title: getScheduledJobs
solution: Experience Manager
title: getScheduledJobs
topic: Scene7 Image Production System API
uuid: 56b0623b-46d7-4d11-8eea-6543ed364b53
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getScheduledJobs{#getscheduledjobs}

Obtiene los trabajos programados para ejecutarse.

Sintaxis

## Tipos de usuarios autorizados {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-2af604ff8282460990b9237158187f8f}

**Entrada (getScheduledJobsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | El identificador de la compañía. |
| ` *`jobHandle`*` | `xsd:string` | No | Identificador de trabajo. |
| ` *`originalName`*` | `xsd:string` | No | El nombre especificado por `submitJob`. |

**Salida (getScheduledJobsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`jobArray`*` | `types:ScheduledJobArray` | Sí | Matriz de trabajos programados. |

## Ejemplos {#section-e79e7da86ba848fd9996aa36de462e6c}

Este ejemplo de código devuelve todos los trabajos programados de una matriz de trabajos. La matriz misma contiene información detallada sobre los trabajos.

**Solicitar**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**Respuesta**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```

