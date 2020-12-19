---
description: Detiene un trabajo activo.
seo-description: Detiene un trabajo activo.
seo-title: pauseJob
solution: Experience Manager
title: pauseJob
topic: Scene7 Image Production System API
uuid: baad2ad6-46f5-4133-a6d9-8ffadf990a06
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 18%

---


# pauseJob{#pausejob}

Detiene un trabajo activo.

Sintaxis

## Tipos de usuarios autorizados {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-7aedb924cf8b4e05a0dc927636d537a0}

**Entrada (pauseJobParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Manejar a la compañía. |
| ` *`jobHandle`*` | `xsd:string` | Sí | Administre el trabajo que desea pausar. |

**Salida (PauseJobReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-ee4914f9496f4bd88556728a48fb22c1}

Este ejemplo de código pone en pausa un trabajo activo.

**Solicitar**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Respuesta**

Ninguno.
