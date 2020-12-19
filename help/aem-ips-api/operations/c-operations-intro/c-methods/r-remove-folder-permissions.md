---
description: Quita los permisos de la carpeta.
seo-description: Quita los permisos de la carpeta.
seo-title: removeFolderPermissions
solution: Experience Manager
title: removeFolderPermissions
topic: Scene7 Image Production System API
uuid: cd9f7a42-e314-4ec9-abe2-a27581c7cd23
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 16%

---


# removeFolderPermissions{#removefolderpermissions}

Quita los permisos de la carpeta.

Sintaxis

## Tipos de usuarios autorizados {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-7efa68377fd846219b906d354ae64ed3}

**Entrada (removeFolderPermissionsParam)**

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obligatorio </th> 
   <th colname="col4" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Identificador de la compañía con las carpetas con permisos que desea quitar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Gestionar en la carpeta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> <p>Cuando <span class="codeph"> true</span>: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">La eliminación de permisos se propaga a través de todas las operaciones de permisos de carpetas. </li> 
     </ul> </p> <p>Cuando <span class="codeph"> false</span>: 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">La operación solo afecta a la carpeta especificada. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (removeFolderPermissionsReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-04390f0ec7cc460cb5d34d518e33e7a5}

Este ejemplo de código elimina los permisos de una carpeta y sus subcarpetas. Establezca `updateChildren` en `false` si sólo necesita quitar permisos de la carpeta principal.

**Solicitar**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**Respuesta**

Ninguno.
