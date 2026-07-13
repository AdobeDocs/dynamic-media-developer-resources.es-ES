---
description: Establece los valores del diccionario de etiquetas para un campo de etiqueta existente.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
TQID: 'https://experienceleague.adobe.com/--ArL0CPejqbpJX-G7Z8zdU97WVXXjGfWc74UmOWSV0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 13%

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
| companyHandle | `xsd:string` | Sí | Manejo de la compañía. |
| fieldHandle | `xsd:string` | Sí | Controlador de campo de etiqueta. |
| valueArray | `types:StringArray` | Sí | Matriz de valores de etiqueta que reemplazan el diccionario existente del campo. Las asociaciones de recursos se mantienen cuando un nuevo valor coincide con un valor existente. |

**Salida (setTagFieldValuesReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-b11cafd9bed54ab5836c737cc075c918}

**Solicitud**

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

