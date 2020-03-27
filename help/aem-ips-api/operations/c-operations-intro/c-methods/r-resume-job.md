---
description: Reinicia un trabajo pausado.
seo-description: Reinicia un trabajo pausado.
seo-title: resumeJob
solution: Experience Manager
title: resumeJob
topic: Scene7 Image Production System API
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con el trabajo que desea reiniciar. |
| ` *`jobHandle`*` | `xsd:string` | Sí | Identificador del trabajo pausado. |

**Output (resumeJobReturn)**

La API de IPS no devuelve una respuesta para esta operación.

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
