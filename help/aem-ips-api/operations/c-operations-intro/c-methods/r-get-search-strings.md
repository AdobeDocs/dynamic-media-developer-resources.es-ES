---
description: Obtiene las cadenas de búsqueda, las palabras clave y otra información sobre un recurso. La respuesta contiene información adicional sobre el recurso.
seo-description: Obtiene las cadenas de búsqueda, las palabras clave y otra información sobre un recurso. La respuesta contiene información adicional sobre el recurso.
seo-title: getSearchStrings
solution: Experience Manager
title: getSearchStrings
topic: Dynamic Media Image Production System API
uuid: 9d588d6b-c79c-4531-a2e8-8467254a7985
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 14%

---


# getSearchStrings{#getsearchstrings}

Obtiene las cadenas de búsqueda, las palabras clave y otra información sobre un recurso. La respuesta contiene información adicional sobre el recurso.

Sintaxis

## Tipos de usuarios autorizados {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-c1efda4bb15349a68b276bafee8c18fd}

**Entrada (getSearchStringsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Manejar a la compañía. |
| `*`assetHandle`*` | `xsd:string` | Sí | Gestionar en el recurso. |

**Salida (getSearchStringsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | Sí | Matriz de cadenas de búsqueda de recursos. |

## Ejemplos {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Este ejemplo de código devuelve cadenas de búsqueda específicas de recursos. La respuesta devuelve una matriz vacía.

**Solicitar**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Respuesta**

Ninguno.
