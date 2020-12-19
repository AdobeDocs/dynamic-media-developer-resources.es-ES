---
description: Quita los valores de campo de etiqueta del diccionario de un campo de etiqueta.
seo-description: Quita los valores de campo de etiqueta del diccionario de un campo de etiqueta.
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
topic: Scene7 Image Production System API
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
translation-type: tm+mt
source-git-commit: b5eaefb375fbd0d0786619fa6d84b4f6fc17a77f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# deleteTagFieldValues{#deletetagfieldvalues}

Quita los valores de campo de etiqueta del diccionario de un campo de etiqueta.

## Tipos de usuarios autorizados {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-5db64a6ae238426395bc760b83587260}

**Entrada (deleteTagFieldValuesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que contiene el campo de etiqueta. |
| ` *`fieldHandle`*` | `xsd:string` | Sí | Identificador del campo de etiqueta que se va a modificar. |
| ` *`valueArray`*` | `types:StringArray` | Sí | Matriz de valores de etiqueta que se eliminarán del diccionario del campo. |

**Salida (deleteTagFieldValuesParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-92f9e575a6da491caa09e264b4d6ee55}

**Solicitar**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**Respuesta**

Ninguno.
