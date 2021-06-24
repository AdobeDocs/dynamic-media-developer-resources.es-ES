---
description: Elimina un trabajo actual o programado.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 12%

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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa a la que pertenece el trabajo. |
| `*`jobHandle`*` | `xsd:string` | Sí | El identificador del trabajo que se va a eliminar. |

**Salida**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Este ejemplo de código elimina un trabajo que se está ejecutando o que está programado para ejecutarse en IPS. Requiere un identificador de trabajo, que debe obtener de otra operación.

**Solicitar**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Respuesta**

Ninguno.
