---
description: Obtiene las cadenas de búsqueda, palabras clave y otra información acerca de un recurso. La respuesta contiene información adicional sobre el recurso.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 17%

---

# getSearchStrings{#getsearchstrings}

Obtiene las cadenas de búsqueda, palabras clave y otra información acerca de un recurso. La respuesta contiene información adicional sobre el recurso.

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
| companyHandle | `xsd:string` | Sí | Gestionar en la empresa. |
| assetHandle | `xsd:string` | Sí | Administre en el recurso. |

**Salida (getSearchStringsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| searchStringArray | `types:SearchStrings` | Sí | Matriz de cadenas de búsqueda de recursos. |

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
