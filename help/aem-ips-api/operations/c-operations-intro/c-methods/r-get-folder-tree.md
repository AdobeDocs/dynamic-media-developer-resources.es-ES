---
description: Devuelve carpetas y subcarpetas de una estructura jerárquica de árbol. La respuesta getFolderTree está limitada a un máximo de 100.000 carpetas
seo-description: Devuelve carpetas y subcarpetas de una estructura jerárquica de árbol. La respuesta getFolderTree está limitada a un máximo de 100.000 carpetas
seo-title: getFolderTree
solution: Experience Manager
title: getFolderTree
topic: Dynamic Media Image Production System API
uuid: 93fda0d6-c656-4254-b07b-7a448e164f28
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 8%

---


# getFolderTree{#getfoldertree}

Devuelve carpetas y subcarpetas de una estructura jerárquica de árbol. La respuesta getFolderTree está limitada a un máximo de 100.000 carpetas

Sintaxis

## Tipos de usuarios autorizados {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura a la carpeta para devolver datos.

## Parámetros {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**Entrada (getFolderTreeParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la compañía. |
| `*`accessUserHandle`*` | `xsd:string` | No | Solo lo utilizan los administradores para hacerse pasar por un usuario específico. |
| `*`accessGroupHandle`*` | `xsd:string` | No | Se utiliza para filtrar por un grupo específico, incluidos los grupos a los que pertenece la compañía. |
| `*`folderPath`*` | `xsd:string` | No | La carpeta raíz que se va a recuperar y todas las subcarpetas en el nivel de hoja. Si se excluye, se utiliza la raíz de compañía. |
| `*`profundidad`*` | `xsd:int` | Sí | Un valor de cero obtiene la carpeta de nivel superior. Cualquier otro valor especifica la profundidad que se va a descender en el árbol. |
| `*`assetTypeArray`*` | `types:StringArray` | No | Devuelve carpetas que solo contienen tipos de recursos especificados. |
| `*`responseFieldArray`*` | `types:StringArray` | No | Contiene una lista de campos que desea incluir en la respuesta. |
| `*`excludeFieldArray`*` | `types:StringArray` | No | Contiene una lista de campos que desea excluir en la respuesta. |

**Salida (getFolderTreeReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`carpetas`*` | `types:folders` | No | La jerarquía de carpetas en una estructura de árbol. La respuesta está limitada a un máximo de 100.000 carpetas. |
| `*`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## Ejemplos {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

Este ejemplo de código utiliza un controlador de compañía y un parámetro de profundidad para determinar el nivel de profundidad que debe devolver la respuesta. La respuesta contiene carpetas y matrices de subcarpetas con elementos relacionados. Establezca el valor de profundidad en un número menor para buscar más profundamente en el árbol de carpetas.

**Solicitar**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**Respuesta**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```

