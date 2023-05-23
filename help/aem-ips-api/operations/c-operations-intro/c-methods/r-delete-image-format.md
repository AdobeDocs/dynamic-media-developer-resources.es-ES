---
description: Elimina un formato de imagen. Obtenga el controlador de formato de imagen de saveImageFormat.
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 11%

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
| companyHandle | `xsd:string` | Sí | El identificador de la compañía que contiene el formato de imagen que desea eliminar. |
| imageFormatHandle | `xsd:string` | Sí | El controlador del formato de imagen que desea eliminar. |

**Salida (deleteImageFormatParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Este ejemplo de código elimina un formato de imagen de una empresa. Obtenga el controlador de formato de imagen de otra operación.

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
