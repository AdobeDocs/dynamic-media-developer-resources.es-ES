---
title: createFolder
description: Crea una carpeta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 19%

---

# [!DNL createFolder]{#createfolder}

Crea una carpeta.

>[!NOTE]
>
>La nueva carpeta está subordinada a la carpeta Imágenes , incluso si especifica una `/` para indicar la raíz de la empresa.

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
| companyHandle | `xsd:string` | Sí | Control para la empresa |
| folderPath | `xsd:string` | Sí | La carpeta raíz utilizada para recuperar carpetas y todas las subcarpetas en el nivel de hoja. Si se excluye, se utiliza la raíz de la empresa. |

**Salida (createFolderParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| folderHandle | `xsd:string` | Sí | Gestionar la nueva carpeta. |

## Ejemplos {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Este código de ejemplo crea una carpeta en la raíz de una empresa. La respuesta devuelve el identificador de la carpeta recién creada.

**Solicitar**

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
