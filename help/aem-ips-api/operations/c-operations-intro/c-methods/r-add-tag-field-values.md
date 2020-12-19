---
description: Añade nuevos valores de etiqueta en el diccionario de un campo de etiqueta existente.
seo-description: Añade nuevos valores de etiqueta en el diccionario de un campo de etiqueta existente.
seo-title: addTagFieldValues
solution: Experience Manager
title: addTagFieldValues
topic: Scene7 Image Production System API
uuid: 9304f02c-a1df-4477-ab33-f2491c390c92
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# addTagFieldValues{#addtagfieldvalues}

Añade nuevos valores de etiqueta en el diccionario de un campo de etiqueta existente.

Sintaxis

## Tipos de usuarios autorizados {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Entrada (addTagFieldValuesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que contiene el campo de etiqueta. |
| ` *`fieldHandle`*` | `xsd:string` | Sí | Identificador del campo de etiqueta que se va a modificar. |
| ` *`valueArray`*` | `xsd:string` | Sí | Matriz de valores de etiqueta que se agregarán al diccionario existente del campo. |

**Salida (addTagFieldValuesParam)**

La API de IPS no devuelve una respuesta para esta operación.

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
