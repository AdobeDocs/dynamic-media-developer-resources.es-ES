---
description: Reinicia un trabajo pausado.
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 16%

---


# resumeJob{#resumejob}

Reinicia un trabajo pausado.

Sintaxis

## Tipos de usuarios autorizados {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**Entrada (resumeJobParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con el trabajo que desea reiniciar. |
| `*`jobHandle`*` | `xsd:string` | Sí | El identificador del trabajo pausado. |

**Salida (resumeJobReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-d0524e031f1f43d89430eade19526162}

Este ejemplo de código reinicia un trabajo pausado.

**Solicitar**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**Respuesta**

Ninguno.
