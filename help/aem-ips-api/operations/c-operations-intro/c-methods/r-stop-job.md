---
description: Detiene un trabajo en curso.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 20%

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
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`jobHandle`*` | `xsd:string` | Sí | Gestione el trabajo que desea detener. |

**Salida (stopJobReturn0**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Solicitar**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Respuesta**

Ninguno.
