---
title: createFolder
description: Crea una carpeta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
TQID: 'https://experienceleague.adobe.com/iQNFDdsbxhklGSfUb1pmcNhzIT8kJYc19xFglU7Blc8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 17%

---

# [!DNL createFolder]{#createfolder}

Crea una carpeta.

>[!NOTE]
>
>La nueva carpeta está subordinada a la carpeta Imágenes, aunque especifique un `/` para indicar la raíz de la compañía.

Sintaxis

## Tipos de usuarios autorizados {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura a la carpeta principal.

## Parámetros {#section-c00d8d89cf114886a535056f2a1bf892}

**Entrada (createFolder)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El controlador de la compañía |
| folderPath | `xsd:string` | Sí | La carpeta raíz utilizada para recuperar carpetas y todas las subcarpetas al nivel de hoja. Si se excluye, se utiliza la raíz de la empresa. |

**Salida (createFolderParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| folderHandle | `xsd:string` | Sí | Gestión de la nueva carpeta. |

## Ejemplos {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Este código de ejemplo crea una carpeta en la raíz de una compañía. La respuesta devuelve el identificador de la carpeta recién creada.

**Solicitud**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**Respuesta**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```

