---
description: Devuelve las coordenadas del cuadrilateral que rodea la ruta de Photoshop con nombre.
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 18%

---


# getPhotoshopPath{#getphotoshoppath}

Devuelve las coordenadas del cuadrilateral que rodea la ruta de Photoshop con nombre.

Sintaxis

## Tipos de usuarios autorizados {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Parámetros {#section-ebffe496284c4ced9f329f78127be199}

**Entrada (getPhotoshopPathParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Gestione a la empresa con la imagen con la que desee trabajar. |
| `*`assetHandle`*` | `xsd:string` | Sí | Gestionar en el recurso de imagen. |
| `*`pathName`*` | `xsd:string` | Sí | Nombre de la ruta de Photoshop que desea devolver. |

**Salida (getPhotoshopPathReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`PerspectivaQuad`*` | `types:PerspectiveQuad` | Sí | Devuelve las coordenadas de la imagen en función de la ruta. Consulte [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204). |

## Ejemplos {#section-1f0461cbdc184c8d8925336d5279db47}

**Solicitar**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**Respuesta**

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)

