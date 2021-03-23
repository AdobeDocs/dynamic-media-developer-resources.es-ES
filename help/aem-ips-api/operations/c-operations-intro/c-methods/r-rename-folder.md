---
description: Cambia el nombre de una carpeta.
seo-description: Cambia el nombre de una carpeta.
seo-title: filenameFolder
solution: Experience Manager
title: filenameFolder
uuid: 7d190a57-1d81-4f41-9205-b8ffdf7330ec
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 19%

---


# filenameFolder{#renamefolder}

Cambia el nombre de una carpeta.

Sintaxis

## Tipos de usuarios autorizados {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura al recurso.

## Parámetros {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**Entrada (cambiar nombre de parámetro de carpeta)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Gestione a la empresa las carpetas a las que desee cambiar el nombre. |
| `*`folderHandle`*` | `xsd:string` | Sí | Gestione en la carpeta . |
| `*`folderName`*` | `xsd:string` | Sí | Nuevo nombre de carpeta. |

**Salida (filenameFolderReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Sí | Gestione en la carpeta con el nombre cambiado. |

## Ejemplos {#section-98bdd2f88d164f488676e90aba1dc864}

Este ejemplo de código cambia el nombre de una carpeta.

**Solicitar**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**Respuesta**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```

