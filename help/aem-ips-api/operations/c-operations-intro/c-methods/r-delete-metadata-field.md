---
description: Elimina el campo de metadatos de una compañía.
seo-description: Elimina el campo de metadatos de una compañía.
seo-title: deleteMetadataField
solution: Experience Manager
title: deleteMetadataField
topic: Scene7 Image Production System API
uuid: 06ec434a-2793-4227-ac93-ae3871c38ab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# deleteMetadataField{#deletemetadatafield}

Elimina el campo de metadatos de una compañía.

Sintaxis

## Tipos de usuarios autorizados {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-73f12a30cc4340b6b32dd11effd5195e}

**Entrada (deleteMetadataFieldParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que contiene el campo de metadatos que se va a eliminar. |
| ` *`fieldHandle`*` | `xsd:string` | Sí | Identificador del campo de metadatos que se va a eliminar. |

**Salida (deleteMetadataFieldParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Este ejemplo de código elimina el campo de metadatos de una compañía. Utiliza el identificador de compañía y el identificador de metadatos como campos del `deleteMetadataFieldParam` pasado al servidor de servicios Web IPS para realizar esta acción.

**Solicitar**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Respuesta**

Ninguno.0
