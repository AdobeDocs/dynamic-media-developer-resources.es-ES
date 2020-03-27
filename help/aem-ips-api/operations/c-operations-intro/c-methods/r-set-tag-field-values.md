---
description: Establece los valores del diccionario de etiquetas para un campo de etiqueta existente.
seo-description: Establece los valores del diccionario de etiquetas para un campo de etiqueta existente.
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
topic: Scene7 Image Production System API
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setTagFieldValues{#settagfieldvalues}

Establece los valores del diccionario de etiquetas para un campo de etiqueta existente.

Sintaxis

## Tipos de usuarios autorizados {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-a05cbee4cb4f44198c414a6b14e69156}

**Entrada**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de Compañía. |
| ` *`fieldHandle`*` | `xsd:string` | Sí | Identificador del campo de etiqueta. |
| ` *`valueArray`*` | `types:StringArray` | Sí | Matriz de valores de etiqueta que reemplazan al diccionario existente del campo. Las asociaciones de recursos se mantienen cuando un nuevo valor coincide con un valor existente. |

**Salida (setTagFieldValuesReturn)**

La API de IPS no devuelve una respuesta para esta operación.

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
