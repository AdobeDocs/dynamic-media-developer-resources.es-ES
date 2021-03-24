---
description: Pone en pausa un trabajo activo.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---


# pauseJob{#pausejob}

Pone en pausa un trabajo activo.

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
| `*`companyHandle`*` | `xsd:string` | Sí | Gestionar a la empresa. |
| `*`jobHandle`*` | `xsd:string` | Sí | Gestione el trabajo que desea pausar. |

**Salida (PauseJobReturn)**

La API IPS no devuelve una respuesta para esta operación.

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
