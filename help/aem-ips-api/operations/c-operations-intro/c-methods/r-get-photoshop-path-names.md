---
description: Devuelve una matriz de nombres de ruta de Photoshop para la imagen dada.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 19%

---


# getPhotoshopPathNames{#getphotoshoppathnames}

Devuelve una matriz de nombres de ruta de Photoshop para la imagen dada.

Sintaxis

## Tipos de usuarios autorizados {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-605a4aab23104489a21f7f7f5849801b}

**Entrada (getPhotoshopPathNamesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Gestione a la empresa que contiene la imagen con la que desea trabajar. |
| `*`assetHandle`*` | `xsd:string` | Sí | Gestionar en el recurso de imagen. |

**Salida (getPhotoshopPathNamesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`pathNameArray`*` | `types:StringArray` | Sí | Matriz de nombres de ruta de Photoshop en una imagen. |

## Ejemplos {#section-6d316f14b4184d42af4ca3f717b042dd}

**Solicitar**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**Respuesta**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```

