---
description: Elimina un mapa de imagen.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
TQID: 'https://experienceleague.adobe.com/6r-EiZLM0tRUpzoTJyTt3rAkyABfNH9DQvDJq-XsqPY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 10%

---

# deleteImageMap{#deleteimagemap}

Elimina un mapa de imagen.

Sintaxis

## Tipos de usuarios autorizados {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura al recurso.

## Parámetros {#section-28de12bab79045a5977c68855e37ae3d}

**Entrada (deleteImageMapParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía que contiene el mapa de imagen que se va a eliminar. |
| imageMapHandle | `xsd:string` | Sí | El controlador del mapa de imagen que se va a eliminar. |

**Salida (deleteImageMapParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Este ejemplo de código elimina un mapa de imagen de una empresa. Debe obtener el identificador del mapa de imagen de otra operación.

**Solicitud**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Respuesta**

Ninguna

