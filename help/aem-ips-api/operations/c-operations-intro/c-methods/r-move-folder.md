---
description: Mueva una carpeta a una nueva ubicación.
seo-description: Mueva una carpeta a una nueva ubicación.
seo-title: moveFolder
solution: Experience Manager
title: moveFolder
topic: Scene7 Image Production System API
uuid: 424858c3-5796-4ae9-b5ad-fd50ddbee702
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveFolder{#movefolder}

Mueva una carpeta a una nueva ubicación.

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Manejar a la compañía. |
| ` *`folderHandle`*` | `xsd:string` | Sí | Identificador de carpeta. |
| ` *`destFolderHandle`*` | `xsd:string` | Sí | Gestionar en la carpeta de destino. |

**Output (moveFolderReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Sí | Gestionar en la carpeta movida. |

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

