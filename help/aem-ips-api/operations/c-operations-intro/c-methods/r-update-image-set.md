---
description: Actualiza un conjunto de imágenes.
seo-description: Actualiza un conjunto de imágenes.
seo-title: updateImageSet
solution: Experience Manager
title: updateImageSet
topic: Scene7 Image Production System API
uuid: df118ba3-d86f-4005-928e-76a5a9f899fc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateImageSet{#updateimageset}

Actualiza un conjunto de imágenes.

Sintaxis

## Parámetros {#section-3be47dbbce474ce78676b05e163492e3}

**Input (updateImageSetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que contiene el conjunto de imágenes que desea modificar. |
| ` *`assetHandle`*` | `xsd:string` | Ys | Identificador del conjunto de imágenes que desea modificar. |
| ` *`miembroArray`*` | `types:ImageSetMemberUpdateArray` | No | Restablece los miembros del conjunto de imágenes. |
| ` *`thumbAssetHandle`*` | `xsd:string` | No | Identificador del recurso que actúa como miniatura del conjunto de imágenes. |

**Salida (updateImageSetReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`secuencia`*` |  |  |  |

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

