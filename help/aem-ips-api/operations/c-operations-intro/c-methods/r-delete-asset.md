---
description: Elimina un recurso.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Developer,Administrator
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 12%

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
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa a la que pertenece la carpeta. |
| `*`assetHandle`*` | `xsd:string` | Sí | El identificador del recurso que se va a eliminar. |

**Salida (deleteAssetParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-d5657289f5234bb0a613dcf691507958}

Este código de ejemplo elimina cualquier tipo de recurso de una empresa específica. Requiere un controlador de recursos que debe obtener de otra operación.

**Solicitar**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Respuesta**

Ninguno.
