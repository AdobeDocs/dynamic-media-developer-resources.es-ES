---
description: Agrega nuevos valores de etiqueta al diccionario de un campo de etiqueta existente.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 13%

---

# addTagFieldValues{#addtagfieldvalues}

Agrega nuevos valores de etiqueta al diccionario de un campo de etiqueta existente.

Sintaxis

## Tipos de usuarios autorizados {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Entrada (addTagFieldValuesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene el campo de etiqueta. |
| `*`fieldHandle`*` | `xsd:string` | Sí | El controlador del campo de etiqueta que se va a modificar. |
| `*`valueArray`*` | `xsd:string` | Sí | Matriz de valores de etiqueta que se agregarán al diccionario existente del campo. |

**Salida (addTagFieldValuesParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-c4049392f1c548f883b8b1f8f167bada}

**Solicitar**

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**Respuesta**

Ninguno.
