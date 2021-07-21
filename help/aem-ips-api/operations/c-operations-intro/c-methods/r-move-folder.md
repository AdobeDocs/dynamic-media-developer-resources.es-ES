---
description: Mover una carpeta a una nueva ubicación.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 26%

---

# moveFolder{#movefolder}

Mover una carpeta a una nueva ubicación.

Sintaxis

## Tipos de usuarios autorizados {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-473c2e68bcc14a9ea2593bee26e679dd}

**Entrada (moveFolderParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Gestionar a la empresa. |
| `*`folderHandle`*` | `xsd:string` | Sí | Identificador de carpeta. |
| `*`destFolderHandle`*` | `xsd:string` | Sí | Gestionar en la carpeta de destino. |

**Salida (moveFolderReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Sí | Gestionar en la carpeta movida. |

## Ejemplos {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Solicitar**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**Respuesta**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```
