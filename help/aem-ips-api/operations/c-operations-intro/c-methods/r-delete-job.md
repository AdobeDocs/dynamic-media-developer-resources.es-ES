---
description: Elimina un trabajo actual o programado.
seo-description: Elimina un trabajo actual o programado.
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
topic: Scene7 Image Production System API
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía a la que pertenece el trabajo. |
| ` *`jobHandle`*` | `xsd:string` | Sí | Identificador del trabajo que se va a eliminar. |

**Salida**

La API de IPS no devuelve una respuesta para esta operación.

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
