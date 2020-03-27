---
description: Comprueba los conflictos de ID de IPS comparando los nombres de los recursos con todos los nombres de la Área de nombres del catálogo de servicio de imágenes/procesamiento de imágenes de una compañía.
seo-description: Comprueba los conflictos de ID de IPS comparando los nombres de los recursos con todos los nombres de la Área de nombres del catálogo de servicio de imágenes/procesamiento de imágenes de una compañía.
seo-title: checkAssetNames
solution: Experience Manager
title: checkAssetNames
topic: Scene7 Image Production System API
uuid: 91d073a8-7648-429b-aa5c-c7d595550299
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# checkAssetNames{#checkassetnames}

Comprueba los conflictos de ID de IPS comparando los nombres de los recursos con todos los nombres de la Área de nombres del catálogo de servicio de imágenes/procesamiento de imágenes de una compañía.

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
| ` *`companyHandle`*` | `xsd:string` | No | Identificador de la compañía que contiene al usuario. |
| ` *`assetNamesArray`*` | `types:StringArray` | Sí | Matriz de nombres de recursos para comprobar. |

**Salida (checkAssetNamesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`inUseNameArray`*` | `types:StringArray` | Sí | Matriz de nombres de recursos en uso. |

## Ejemplos {#section-bc5d120d74614a63a425ca3acc337219}

Este código de ejemplo solicita los nombres de los recursos que se utilizan para una compañía específica. La respuesta devuelve una matriz de nombres de recursos que están en uso.

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

