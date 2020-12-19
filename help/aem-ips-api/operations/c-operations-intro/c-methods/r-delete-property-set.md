---
description: Elimina un conjunto de propiedades y todas las propiedades asociadas.
seo-description: Elimina un conjunto de propiedades y todas las propiedades asociadas.
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
topic: Scene7 Image Production System API
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
| ` *`setHandle`*` | `xsd:string` | Sí | Identificador del conjunto de propiedades que se va a eliminar. |

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
