---
description: Elimina un conjunto de propiedades y todas las propiedades asociadas.
seo-description: Elimina un conjunto de propiedades y todas las propiedades asociadas.
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
topic: Dynamic Media Image Production System API
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 11%

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
| `*`setHandle`*` | `xsd:string` | Sí | Identificador del conjunto de propiedades que se va a eliminar. |

**Salida (deletePropertySetParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-cf319fc8f86a40ab9cbd838b031973fe}

Este ejemplo de código utiliza el identificador del conjunto como un campo en el `deletePropertySetParam` enviado al servidor de servicios Web IPS para eliminar el conjunto de propiedades.

**Solicitar**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Respuesta**

Ninguno.
