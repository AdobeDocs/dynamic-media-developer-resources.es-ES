---
description: Devuelve una matriz de nombres de ruta de Photoshop para la imagen dada.
seo-description: Devuelve una matriz de nombres de ruta de Photoshop para la imagen dada.
seo-title: getPhotoshopPathNames
solution: Experience Manager
title: getPhotoshopPathNames
topic: Scene7 Image Production System API
uuid: d3f1dea5-393b-498e-963d-37a4e38068a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Controle la compañía que contiene la imagen con la que desea trabajar. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Gestionar el recurso de imagen. |

**Salida (getPhotoshopPathNamesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`pathNameArray`*` | `types:StringArray` | Sí | Matriz de nombres de ruta de Photoshop en una imagen. |

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

