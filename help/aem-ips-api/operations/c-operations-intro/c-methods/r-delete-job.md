---
description: Elimina un trabajo actual o programado.
seo-description: Elimina un trabajo actual o programado.
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 11%

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
