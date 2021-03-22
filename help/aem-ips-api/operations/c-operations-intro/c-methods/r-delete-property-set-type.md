---
description: Elimina un tipo de conjunto de propiedades y su conjunto de propiedades y propiedades asociados.
seo-description: Elimina un tipo de conjunto de propiedades y su conjunto de propiedades y propiedades asociados.
seo-title: deletePropertySetType
solution: Experience Manager
title: deletePropertySetType
uuid: 7a5232cc-fa3a-4dac-bf88-8b954dd37c87
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
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
| `*`typeHandle`*` | `xsd:string` | Sí | El identificador del tipo de conjunto de propiedades que se va a eliminar. |

**Salida (deletePropertySetTypeParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-85faa2e3411a4e23aa6489037f7ce078}

Este ejemplo de código utiliza el identificador del tipo como campo en el `deletePropertySetTypeParam` enviado al servidor de servicios web IPS para eliminar el tipo de conjunto de propiedades.

**Solicitar**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Respuesta**

Ninguno.
