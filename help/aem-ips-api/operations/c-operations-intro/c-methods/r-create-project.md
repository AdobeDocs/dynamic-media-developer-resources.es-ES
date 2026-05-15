---
description: Crea un nuevo proyecto.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
TQID: 'https://experienceleague.adobe.com/GKNImvhmX1bOepsV0-6QzgZr5jskJQlaqXCMIT5ue5M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 18%

---

# createProject{#createproject}

Crea un nuevo proyecto.

Sintaxis

## Tipos de usuarios autorizados {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-8c741884eb54489bbaad0c444fee80b6}

**Entrada (createProjectParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía asociada con el nuevo proyecto. |
| projectName | `xsd:string` | Sí | Nuevo nombre de proyecto. |

**Salida (createProjectParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| projectHandle | `xsd:string` | Sí | El identificador del nuevo proyecto. |

## Ejemplos {#section-a0cd532b67e346d088fbec141231a0e5}

Este ejemplo de código crea un proyecto denominado `ApiTestProject` en una compañía especificada por su identificador. La respuesta devuelve el identificador del proyecto.

**Solicitud**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```
