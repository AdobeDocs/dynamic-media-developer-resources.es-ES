---
description: Elimina un formato de imagen. Obtenga el controlador de formato de imagen de saveImageFormat.
seo-description: Elimina un formato de imagen. Obtenga el controlador de formato de imagen de saveImageFormat.
seo-title: deleteImageFormat
solution: Experience Manager
title: deleteImageFormat
topic: Scene7 Image Production System API
uuid: 70dddde9-830b-4267-8ef5-df5241f549e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# deleteImageFormat{#deleteimageformat}

Elimina un formato de imagen. Obtenga el controlador de formato de imagen de saveImageFormat.

Sintaxis

## Tipos de usuarios autorizados {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-462c05d9aad746ee8d2be0656041b693}

**Entrada (deleteImageFormatParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que contiene el formato de imagen que desea eliminar. |
| ` *`imageFormatHandle`*` | `xsd:string` | Sí | Identificador del formato de imagen que desea eliminar. |

**Salida (deleteImageFormatParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Este ejemplo de código elimina un formato de imagen de una compañía. Obtenga el controlador de formato de imagen de otra operación.

**Solicitar**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**Respuesta**

Ninguno.

**Tema relacionado:**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
