---
description: Elimina un conjunto de propiedades y todas las propiedades asociadas.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
TQID: 'https://experienceleague.adobe.com/1j45J5Kw5P-3ba3WLNy9sTDBC5g4L17bynJQRaU5lAM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 10%

---

# deletePropertySet{#deletepropertyset}

Elimina un conjunto de propiedades y todas las propiedades asociadas.

Sintaxis

## Tipos de usuarios autorizados {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-e5fc868f69494cf6858e03027db09101}

**Entrada (deletePropertySetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| setHandle | `xsd:string` | Sí | El identificador de la propiedad que se va a eliminar. |

**Salida (deletePropertySetParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-cf319fc8f86a40ab9cbd838b031973fe}

Este ejemplo de código utiliza el identificador del conjunto como un campo del `deletePropertySetParam` enviado al servidor de servicios web IPS para eliminar el conjunto de propiedades.

**Solicitud**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Respuesta**

Ninguno.
