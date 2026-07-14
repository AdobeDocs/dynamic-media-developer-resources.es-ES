---
description: Devuelve una matriz de nombres de rutas Photoshop para la imagen determinada.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
TQID: 'https://experienceleague.adobe.com/BxFBNXpa9ilc4lXeXiuuvCQb9ChImZWt13-pJ3b3osk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 77
ht-degree: 18%

---

# getPhotoshopPathNames{#getphotoshoppathnames}

Devuelve una matriz de nombres de rutas Photoshop para la imagen determinada.

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
| companyHandle | `xsd:string` | Sí | Identificador de la compañía que contiene la imagen con la que desea trabajar. |
| assetHandle | `xsd:string` | Sí | Administre en el recurso de imagen. |

**Salida (getPhotoshopPathNamesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| pathNameArray | `types:StringArray` | Sí | Matriz de nombres de rutas de Photoshop en una imagen. |

## Ejemplos {#section-6d316f14b4184d42af4ca3f717b042dd}

**Solicitud**

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

