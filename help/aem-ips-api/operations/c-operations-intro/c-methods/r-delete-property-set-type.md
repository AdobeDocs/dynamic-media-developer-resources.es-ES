---
description: Elimina un tipo de conjunto de propiedades y su conjunto de propiedades y propiedades asociados.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
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
