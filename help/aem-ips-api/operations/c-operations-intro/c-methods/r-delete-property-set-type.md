---
description: Elimina un tipo de conjunto de propiedades y su conjunto de propiedades y propiedades asociados.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
TQID: 'https://experienceleague.adobe.com/MslFY4FLpUm0zZRKTL6ZK4-seRyEMbF55r1LRToIFQY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 9%

---

# deletePropertySetType{#deletepropertysettype}

Elimina un tipo de conjunto de propiedades y su conjunto de propiedades y propiedades asociados.

Sintaxis

## Tipos de usuarios autorizados {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-1c8973f5d35f44b4a6a483a41609e455}

**Entrada (deletePropertySetTypeParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| typeHandle | `xsd:string` | Sí | El identificador del tipo de conjunto de propiedades que se va a eliminar. |

**Salida (deletePropertySetTypeParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-85faa2e3411a4e23aa6489037f7ce078}

Este ejemplo de código utiliza el identificador del tipo como un campo del `deletePropertySetTypeParam` enviado al servidor de servicios web IPS para eliminar el tipo de conjunto de propiedades.

**Solicitud**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Respuesta**

Ninguno.
