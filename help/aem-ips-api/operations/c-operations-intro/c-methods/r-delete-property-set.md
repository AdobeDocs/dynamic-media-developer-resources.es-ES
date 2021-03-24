---
description: Elimina un conjunto de propiedades y todas las propiedades asociadas.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 12%

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
| `*`setHandle`*` | `xsd:string` | Sí | El identificador del conjunto de propiedades que se va a eliminar. |

**Salida (deletePropertySetParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-cf319fc8f86a40ab9cbd838b031973fe}

Este ejemplo de código utiliza el identificador del conjunto como campo en el `deletePropertySetParam` enviado al servidor de servicios web IPS para eliminar el conjunto de propiedades.

**Solicitar**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Respuesta**

Ninguno.
