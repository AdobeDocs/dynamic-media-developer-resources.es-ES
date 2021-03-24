---
description: Obtiene las cadenas de búsqueda, palabras clave y otra información sobre un recurso. La respuesta contiene información adicional sobre el recurso.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 16%

---


# getSearchStrings{#getsearchstrings}

Obtiene las cadenas de búsqueda, palabras clave y otra información sobre un recurso. La respuesta contiene información adicional sobre el recurso.

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
| `*`companyHandle`*` | `xsd:string` | Sí | Gestionar a la empresa. |
| `*`assetHandle`*` | `xsd:string` | Sí | Gestionar en el recurso. |

**Salida (getSearchStringsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | Sí | Matriz de cadenas de búsqueda de recursos. |

## Ejemplos {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Este ejemplo de código devuelve cadenas de búsqueda específicas del recurso. La respuesta devuelve una matriz vacía.

**Solicitar**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Respuesta**

Ninguno.
