---
description: Define los valores del diccionario de etiquetas para un campo de etiqueta existente.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 14%

---


# setTagFieldValues{#settagfieldvalues}

Define los valores del diccionario de etiquetas para un campo de etiqueta existente.

Sintaxis

## Tipos de usuarios autorizados {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-a05cbee4cb4f44198c414a6b14e69156}

**Entrada**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`fieldHandle`*` | `xsd:string` | Sí | Identificador de campo de etiqueta. |
| `*`valueArray`*` | `types:StringArray` | Sí | Matriz de valores de etiqueta que reemplazan al diccionario existente del campo. Las asociaciones de recursos se mantienen cuando un nuevo valor coincide con un valor existente. |

**Salida (setTagFieldValuesReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-b11cafd9bed54ab5836c737cc075c918}

**Solicitar**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**Respuesta**

Ninguno.
