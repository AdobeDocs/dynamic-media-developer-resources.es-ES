---
description: Actualiza un conjunto de imágenes.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 20%

---

# updateImageSet{#updateimageset}

Actualiza un conjunto de imágenes.

Sintaxis

## Parámetros {#section-3be47dbbce474ce78676b05e163492e3}

**Entrada (updateImageSetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía que contiene el conjunto de imágenes que desea modificar. |
| assetHandle | `xsd:string` | Sí | El controlador del conjunto de imágenes que desea modificar. |
| memberArray | `types:ImageSetMemberUpdateArray` | No | Restablece los miembros del conjunto de imágenes. |
| thumbAssetHandle | `xsd:string` | No | El controlador del recurso que actúa como miniatura para el conjunto de imágenes. |

**Salida (updateImageSetReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| Secuencia |  |  |  |

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
