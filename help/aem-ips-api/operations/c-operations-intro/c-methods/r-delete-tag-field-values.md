---
description: Quita los valores de los campos de etiqueta del diccionario de un campo de etiqueta.
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
TQID: 'https://experienceleague.adobe.com/SRTriQHWMLXJtkGeS-sCDZE3-1bu1TKNkKjxgESYOi4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 11%

---

# deleteTagFieldValues{#deletetagfieldvalues}

Quita los valores de los campos de etiqueta del diccionario de un campo de etiqueta.

## Tipos de usuarios autorizados {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-5db64a6ae238426395bc760b83587260}

**Entrada (deleteTagFieldValuesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía que contiene el campo de etiqueta. |
| fieldHandle | `xsd:string` | Sí | El identificador del campo de etiqueta que se va a modificar. |
| valueArray | `types:StringArray` | Sí | Una matriz de valores de etiqueta que se eliminarán del diccionario del campo. |

**Salida (deleteTagFieldValuesParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-92f9e575a6da491caa09e264b4d6ee55}

**Solicitud**

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

