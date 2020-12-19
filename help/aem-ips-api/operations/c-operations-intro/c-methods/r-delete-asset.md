---
description: Elimina un recurso.
seo-description: Elimina un recurso.
seo-title: deleteAsset
solution: Experience Manager
title: deleteAsset
topic: Scene7 Image Production System API
uuid: 47f700e0-04bf-4d33-a18a-d938f7e9e326
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '96'
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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía a la que pertenece la carpeta. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador del recurso que se va a eliminar. |

**Salida (deleteAssetParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-d5657289f5234bb0a613dcf691507958}

Este código de muestra elimina cualquier tipo de recurso de una compañía específica. Requiere un identificador de recurso, que debe obtener de otra operación.

**Solicitar**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Respuesta**

Ninguno.
