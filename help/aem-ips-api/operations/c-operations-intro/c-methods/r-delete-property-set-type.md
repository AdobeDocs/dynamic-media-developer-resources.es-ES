---
description: Elimina un tipo de conjunto de propiedades y su conjunto de propiedades y propiedades asociados.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 11%

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
