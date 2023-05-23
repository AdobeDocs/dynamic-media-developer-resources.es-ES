---
description: Comprueba los conflictos de ID de IPS comparando los nombres de recursos con todos los nombres del área de nombres del catálogo de servicio de imágenes/procesamiento de imágenes de una empresa.
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 12%

---

# checkAssetNames{#checkassetnames}

Comprueba los conflictos de ID de IPS comparando los nombres de recursos con todos los nombres del área de nombres del catálogo de servicio de imágenes/procesamiento de imágenes de una empresa.

Sintaxis

## Tipos de usuarios autorizados {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parámetros {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Entrada (checkAssetNamesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | No | El identificador de la compañía que contiene al usuario. |
| assetNamesArray | `types:StringArray` | Sí | Matriz de nombres de recursos que se deben comprobar. |

**Salida (checkAssetNamesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | Sí | Matriz de nombres de recursos en uso. |

## Ejemplos {#section-bc5d120d74614a63a425ca3acc337219}

Este código de ejemplo solicita los nombres de recurso en uso para una compañía especificada. La respuesta devuelve una matriz de nombres de recursos que están en uso.

**Solicitar**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**Respuesta**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```
