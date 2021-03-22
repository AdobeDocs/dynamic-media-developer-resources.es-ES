---
description: Devuelve formatos de imagen, como PDF, EPS, SWF, etc.
seo-description: Devuelve formatos de imagen, como PDF, EPS, SWF, etc.
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 16%

---


# getImageFormats{#getimageformats}

Devuelve formatos de imagen, como PDF, EPS, SWF, etc.

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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con los formatos de imagen que desea obtener. |

**Salida (getImageFormatsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`imageFormatArray`*` | `types:ImageFormatArray` | Sí | Matriz de formato de imagen. |

## Ejemplos {#section-73881e12839b4904bf3299b0920bdd0c}

Este ejemplo de código devuelve todos los formatos de imagen para la empresa especificada.

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

