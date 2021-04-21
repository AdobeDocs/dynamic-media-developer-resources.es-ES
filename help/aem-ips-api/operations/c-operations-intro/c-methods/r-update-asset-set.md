---
description: Actualiza un conjunto de recursos.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 19%

---


# updateAssetSet{#updateassetset}

Actualiza un conjunto de recursos.

Sintaxis

## Parámetros {#section-d7080ccd97334c94860eb107a3e132b2}

**Entrada (updateAssetSetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene el conjunto de imágenes que desea modificar. |
| `*`assetHandle`*` | `xsd:string` | Sí | El controlador del conjunto de imágenes que desea modificar. |
| `*`setDefinition`*` | `xsd:string` | No | Restaura los miembros del conjunto de imágenes. |
| `*`thumbAssetHandle`*` | `xsd:string` | No | El controlador del recurso que actúa como la miniatura del conjunto de imágenes. |

**Salida (updateAssetSetReturn)**

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

