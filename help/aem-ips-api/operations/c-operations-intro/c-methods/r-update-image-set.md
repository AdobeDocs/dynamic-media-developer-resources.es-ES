---
description: Actualiza un conjunto de imágenes.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,Conjuntos de imágenes
role: Developer,Administrator
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 18%

---

# updateImageSet{#updateimageset}

Actualiza un conjunto de imágenes.

Sintaxis

## Parámetros {#section-3be47dbbce474ce78676b05e163492e3}

**Entrada (updateImageSetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene el conjunto de imágenes que desea modificar. |
| `*`assetHandle`*` | `xsd:string` | Ys | El controlador del conjunto de imágenes que desea modificar. |
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | No | Restaura los miembros del conjunto de imágenes. |
| `*`thumbAssetHandle`*` | `xsd:string` | No | El controlador del recurso que actúa como la miniatura del conjunto de imágenes. |

**Salida (updateImageSetReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`Secuencia`*` |  |  |  |

## Ejemplos {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Solicitar**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**Respuesta**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```
