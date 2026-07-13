---
description: Obtiene las cadenas de búsqueda, palabras clave y otra información acerca de un recurso. La respuesta contiene información adicional sobre el recurso.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
TQID: 'https://experienceleague.adobe.com/5w3SvwJWT7831IVQKCbpy7Tc-zULMfiva8UBuglcX-g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 15%

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

**Solicitud**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Respuesta**

Ninguno.

