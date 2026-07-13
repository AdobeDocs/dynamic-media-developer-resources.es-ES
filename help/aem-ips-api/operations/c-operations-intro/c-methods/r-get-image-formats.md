---
description: Devuelve formatos de imagen, como PDF, EPS, SWF y otros.
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
TQID: 'https://experienceleague.adobe.com/L8HQVUaxUxkNNkZU7f9Edmh4-t6iwys4c106YVEczD8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 74
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

