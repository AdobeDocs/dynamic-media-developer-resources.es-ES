---
description: Devuelve carpetas y subcarpetas en una estructura de árbol jerárquica. La respuesta getFolderTree está limitada a un máximo de 100 000 carpetas
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 9%

---

# getFolderTree{#getfoldertree}

Devuelve carpetas y subcarpetas en una estructura de árbol jerárquica. La respuesta getFolderTree está limitada a un máximo de 100 000 carpetas

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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa. |
| `*`accessUserHandle`*` | `xsd:string` | No | Solo lo utilizan los administradores para suplantar a un usuario específico. |
| `*`accessGroupHandle`*` | `xsd:string` | No | Se utiliza para filtrar por un grupo específico, incluidos aquellos a los que pertenece la empresa. |
| `*`folderPath`*` | `xsd:string` | No | La carpeta raíz para recuperar carpetas y todas las subcarpetas en el nivel de hoja. Si se excluye, se utiliza la raíz de la empresa. |
| `*`profundidad`*` | `xsd:int` | Sí | Un valor de cero obtiene la carpeta de nivel superior. Cualquier otro valor especifica la profundidad que se desciende en el árbol. |
| `*`assetTypeArray`*` | `types:StringArray` | No | Devuelve carpetas que solo contienen tipos de recursos especificados. |
| `*`responseFieldArray`*` | `types:StringArray` | No | Contiene una lista de campos que desea incluir en la respuesta. |
| `*`excludeFieldArray`*` | `types:StringArray` | No | Contiene una lista de campos que desea excluir en la respuesta. |

**Salida (getFolderTreeReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`carpetas`*` | `types:folders` | No | La jerarquía de carpetas en una estructura de árbol. La respuesta está limitada a un máximo de 100 000 carpetas. |
| `*`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## Ejemplos {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

Este ejemplo de código utiliza un control de empresa y un parámetro de profundidad para determinar el nivel de profundidad que debe devolver la respuesta. La respuesta contiene carpetas y matrices de subcarpetas relacionadas. Defina el valor de profundidad en un número menor para buscar más profundamente en el árbol de carpetas.

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
