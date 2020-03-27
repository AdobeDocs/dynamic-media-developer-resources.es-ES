---
description: Elimina un tipo de conjunto de propiedades y sus propiedades y conjunto de propiedades asociados.
seo-description: Elimina un tipo de conjunto de propiedades y sus propiedades y conjunto de propiedades asociados.
seo-title: deletePropertySetType
solution: Experience Manager
title: deletePropertySetType
topic: Scene7 Image Production System API
uuid: 7a5232cc-fa3a-4dac-bf88-8b954dd37c87
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deletePropertySetType{#deletepropertysettype}

Elimina un tipo de conjunto de propiedades y sus propiedades y conjunto de propiedades asociados.

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
| ` *`typeHandle`*` | `xsd:string` | Sí | Identificador del tipo de conjunto de propiedades que se va a eliminar. |

**Salida (deletePropertySetTypeParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-85faa2e3411a4e23aa6489037f7ce078}

Este ejemplo de código utiliza el identificador del tipo como campo en el `deletePropertySetTypeParam` enviado al servidor de servicios Web IPS para eliminar el tipo de conjunto de propiedades.

**Solicitar**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Respuesta**

Ninguno.
