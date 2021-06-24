---
description: Elimina el campo de metadatos de una empresa.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 10%

---

# deleteMetadataField{#deletemetadatafield}

Elimina el campo de metadatos de una empresa.

Sintaxis

## Tipos de usuarios autorizados {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-73f12a30cc4340b6b32dd11effd5195e}

**Entrada (deleteMetadataFieldParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene el campo de metadatos que se va a eliminar. |
| `*`fieldHandle`*` | `xsd:string` | Sí | El identificador del campo de metadatos que se va a eliminar. |

**Salida (deleteMetadataFieldParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Este ejemplo de código elimina el campo de metadatos de una empresa. Utiliza el identificador de empresa y el identificador de metadatos como campos en el `deleteMetadataFieldParam` pasado al servidor de servicios web IPS para realizar esta acción.

**Solicitar**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Respuesta**

None.0
