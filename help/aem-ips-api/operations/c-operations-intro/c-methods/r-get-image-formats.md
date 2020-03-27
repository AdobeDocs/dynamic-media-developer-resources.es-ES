---
description: Devuelve formatos de imagen, como PDF, EPS, SWF y otros.
seo-description: Devuelve formatos de imagen, como PDF, EPS, SWF y otros.
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
topic: Scene7 Image Production System API
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getImageFormats{#getimageformats}

Devuelve formatos de imagen, como PDF, EPS, SWF y otros.

Sintaxis

## Tipos de usuarios autorizados {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-eefa36a70b74498f8727ef61d98cfb63}

**Entrada (getImageFormatsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con los formatos de imagen que desea obtener. |

**Salida (getImageFormatsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`imageFormatArray`*` | `types:ImageFormatArray` | Sí | Matriz de formato de imagen. |

## Ejemplos {#section-73881e12839b4904bf3299b0920bdd0c}

Este ejemplo de código devuelve todos los formatos de imagen para la compañía especificada.

**Solicitar**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**Respuesta**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```

