---
description: Crea una carpeta.
seo-description: Crea una carpeta.
seo-title: createFolder
solution: Experience Manager
title: createFolder
topic: Scene7 Image Production System API
uuid: e3a4eed3-966d-4435-bfeb-3ead4bf523cd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createFolder{#createfolder}

Crea una carpeta.

>[!NOTE]
>
>La nueva carpeta está subordinada a la carpeta Images, aunque especifique un `/` valor para indicar la raíz de la compañía.

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Control de la compañía |
| ` *`folderPath`*` | `xsd:string` | Sí | Carpeta raíz utilizada para recuperar carpetas y todas las subcarpetas en el nivel de hoja. Si se excluye, se utiliza la raíz de compañía. |

**Salida (createFolderParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Sí | Identificador de la nueva carpeta. |

## Ejemplos {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Este código de muestra crea una carpeta en la raíz de una compañía. La respuesta devuelve el identificador de la carpeta recién creada.

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

