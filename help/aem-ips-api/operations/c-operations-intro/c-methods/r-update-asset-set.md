---
description: Actualiza un conjunto de recursos.
seo-description: Actualiza un conjunto de recursos.
seo-title: updateAssetSet
solution: Experience Manager
title: updateAssetSet
topic: Scene7 Image Production System API
uuid: e844a395-0ab3-45a7-bcec-8e9e15efc70e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# updateAssetSet{#updateassetset}

Actualiza un conjunto de recursos.

Sintaxis

## Parámetros {#section-d7080ccd97334c94860eb107a3e132b2}

**Input (updateAssetSetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que contiene el conjunto de imágenes que desea modificar. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador del conjunto de imágenes que desea modificar. |
| ` *`setDefinition`*` | `xsd:string` | No | Restablece los miembros del conjunto de imágenes. |
| ` *`thumbAssetHandle`*` | `xsd:string` | No | Identificador del recurso que actúa como miniatura del conjunto de imágenes. |

**Output (updateAssetSetReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
|  |  |  |  |

## Ejemplos {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Solicitar**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**Respuesta**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

