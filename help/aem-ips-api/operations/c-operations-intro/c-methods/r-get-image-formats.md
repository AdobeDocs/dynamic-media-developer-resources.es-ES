---
description: Devuelve formatos de imagen, como PDF, EPS, SWF y otros.
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 17%

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
| companyHandle | `xsd:string` | Sí | El identificador de la compañía con los formatos de imagen que desea obtener. |

**Salida (getImageFormatsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | Sí | Matriz de formato de imagen. |

## Ejemplos {#section-73881e12839b4904bf3299b0920bdd0c}

Este ejemplo de código devuelve todos los formatos de imagen de la empresa especificada.

**Solicitud**

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
