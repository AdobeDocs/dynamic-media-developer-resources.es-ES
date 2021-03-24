---
description: Elimina los valores de los campos de etiqueta del diccionario de un campo de etiqueta.
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 12%

---


# deleteTagFieldValues{#deletetagfieldvalues}

Elimina los valores de los campos de etiqueta del diccionario de un campo de etiqueta.

## Tipos de usuarios autorizados {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-5db64a6ae238426395bc760b83587260}

**Entrada (deleteTagFieldValuesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene el campo de etiqueta. |
| `*`fieldHandle`*` | `xsd:string` | Sí | El controlador del campo de etiqueta que se va a modificar. |
| `*`valueArray`*` | `types:StringArray` | Sí | Matriz de valores de etiqueta que se eliminarán del diccionario del campo. |

**Salida (deleteTagFieldValuesParam)**

La API IPS no devuelve una respuesta para esta operación.

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
