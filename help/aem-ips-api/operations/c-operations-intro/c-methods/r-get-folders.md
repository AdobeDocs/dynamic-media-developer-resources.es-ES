---
description: Devuelve todas las carpetas y subcarpetas, empezando en la ruta de la carpeta. La respuesta getFolders devuelve un máximo de 100 000 carpetas.
seo-description: Devuelve todas las carpetas y subcarpetas, empezando en la ruta de la carpeta. La respuesta getFolders devuelve un máximo de 100 000 carpetas.
seo-title: getFolders
solution: Experience Manager
title: getFolders
uuid: 06e9d745-b711-43e3-8dc6-93da66b981b1
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 7%

---


# getFolders{#getfolders}

Devuelve todas las carpetas y subcarpetas, empezando en la ruta de la carpeta. La respuesta getFolders devuelve un máximo de 100 000 carpetas.

## Objetivo de las carpetas {#section-66e344d5333f42f1b060a0cba25935c3}

Una carpeta permite organizar subcarpetas y recursos. Todos los nombres de carpetas y recursos deben ser únicos. Las carpetas y recursos que comparten el mismo nombre provocarán un conflicto en el área de nombres, incluso si se encuentran en jerarquías de carpetas diferentes.
Sintaxis

## Tipos de usuarios autorizados {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura a la carpeta para devolver datos.

## Parámetros {#section-0c1976503eaa418a9226b51667901176}

**Entrada (getFoldersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa. |
| `*`accessUserHandle`*` | `xsd:string` | No | Utilizado por los administradores para suplantar a un usuario específico. |
| `*`accessGroupHandle`*` | `xsd:string` | No | Filtrar por un grupo específico. |
| `*`folderPath`*` | `xsd:string` | No | La carpeta raíz para recuperar carpetas y todas las subcarpetas en el nivel de hoja. Si se excluye, se utiliza la raíz de la empresa. |
| `*`assetTypeArray`*` | `types:StringArray` | No | Devuelve carpetas que solo contienen tipos de recursos especificados. |
| `*`responseFieldArray`*` | `types:StringArray` | No | Contiene una lista de campos que desea incluir en la respuesta. |
| `*`excludeFieldArray`*` | `types:StringArray` | No | Contiene una lista de campos que desea excluir de la respuesta. |

**Salida (getFoldersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`folderArray`*` | `types:FolderArray` | No | Matriz de carpetas que coinciden con los criterios del filtro. La respuesta está limitada a un máximo de 100 000 carpetas. |
| `*`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## Ejemplos {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Este ejemplo de código devuelve una matriz que contiene todas las carpetas de una empresa junto con información específica sobre cada carpeta.

**Solicitar**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**Respuesta**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```

