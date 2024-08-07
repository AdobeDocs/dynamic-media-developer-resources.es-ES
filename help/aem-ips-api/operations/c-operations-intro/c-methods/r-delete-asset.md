---
description: Elimina un recurso.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 10%

---

# deleteAsset{#deleteasset}

Elimina un recurso.

Sintaxis

## Tipos de usuarios autorizados {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y eliminación al recurso.

## Parámetros {#section-0eed164e278b456fbdfb7a50727a0416}

**Entrada (deleteAssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía a la que pertenece la carpeta. |
| assetHandle | `xsd:string` | Sí | El identificador del recurso que se va a eliminar. |

**Salida (deleteAssetParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-d5657289f5234bb0a613dcf691507958}

Este código de ejemplo elimina cualquier tipo de recurso de una compañía específica. Requiere un identificador de recursos, que debe obtener de otra operación.

**Solicitud**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Respuesta**

Ninguno.
