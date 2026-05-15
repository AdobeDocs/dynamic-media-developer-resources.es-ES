---
description: Obtiene una matriz de usuarios según lo especificado por los identificadores de compañía, grupo y función de usuario. Esta operación permite ordenar los usuarios devueltos y filtrar por carácter.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
TQID: 'https://experienceleague.adobe.com/17FQLNVfRg84FeVetVfuTWoLRMf8ugBwXBi2CpmLZfI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 9%

---

# getUsers{#getusers}

Obtiene una matriz de usuarios según lo especificado por los identificadores de compañía, grupo y función de usuario. Esta operación permite ordenar los usuarios devueltos y filtrar por carácter.

## Tipos de usuarios autorizados {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| includeInactive | `xsd:boolean` | No | Incluir o excluir usuarios inactivos. Los usuarios que no son administradores de IPS deben ser miembros activos de al menos una compañía para poder realizar llamadas de API. Se devuelve un error de autorización si el usuario no tiene ninguna pertenencia activa a la compañía. |
| includeInvalid | `xsd:boolean` | No | Permite incluir o excluir usuarios no válidos. |
| companyHandleArray | `types:HandleArray` | No | Filtrar los resultados por empresa. |
| groupHandleArray | `types:HandleArray` | No | Filtrar los resultados por grupo. |
| userRoleArray | `types:StringArray` | No | Filtrar los resultados por función de usuario. |
| charFilterField | `xsd:string` | No | Filtrar los resultados por prefijo de cadena de campo (consulte [!DNL Trash State).] |
| charFilter | `xsd:string` | No | Filtrar los resultados por un carácter específico. |
| sortBy | `xsd:string` | No | Elección de los campos de ordenación del usuario. |
| recordsPerPage | `xsd:int` | No | Devuelve el número especificado de registros por página. |
| resultsPage | `xsd:int` | No | Página de resultados. |

**Salida (getUsersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userArray | `types:UserArray` | Sí | Una matriz de usuarios. |

## Ejemplos {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Este ejemplo de código devuelve la matriz de usuarios para varios parámetros opcionales. Las funciones de usuario, los campos de filtro de caracteres de usuario y los campos de ordenación de usuarios se determinan mediante constantes de cadena específicas.

**Solicitud**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**Respuesta**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```
