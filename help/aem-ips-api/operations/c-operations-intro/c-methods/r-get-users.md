---
description: Obtiene una matriz de usuarios según lo especificado por los identificadores de compañía, grupo y función de usuario. Esta operación permite ordenar los usuarios devueltos y filtrar por carácter.
seo-description: Obtiene una matriz de usuarios según lo especificado por los identificadores de compañía, grupo y función de usuario. Esta operación permite ordenar los usuarios devueltos y filtrar por carácter.
seo-title: getUsers
solution: Experience Manager
title: getUsers
topic: Scene7 Image Production System API
uuid: f16ccd1b-0f00-4d9a-b6e1-6abc3bde1af9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
| ` *`includeInactive`*` | `xsd:boolean` | No | Incluir o excluir usuarios inactivos. Los usuarios administradores que no sean de IPS deben ser miembros activos de al menos una compañía para poder realizar llamadas de API. Se mostrará un error de autorización si el usuario no tiene miembros de compañía activos. |
| ` *`includeInvalid`*` | `xsd:boolean` | No | Permite incluir o excluir usuarios no válidos. |
| ` *`companyHandleArray`*` | `types:HandleArray` | No | Filtre los resultados por compañía. |
| ` *`groupHandleArray`*` | `types:HandleArray` | No | Filtre los resultados por grupo. |
| ` *`userRoleArray`*` | `types:StringArray` | No | Filtre los resultados por función de usuario. |
| ` *`charFilterField`*` | `xsd:string` | No | Filtrar los resultados por el prefijo de cadena del campo (consulte [!DNL Trash State).] |
| ` *`charFilter`*` | `xsd:string` | No | Filtre los resultados por un carácter específico. |
| ` *`sortBy`*` | `xsd:string` | No | Elección de campos de ordenación de usuarios. |
| ` *`recordsPerPage`*` | `xsd:int` | No | Devuelve el número especificado de registros por página. |
| ` *`resultsPage`*` | `xsd:int` | No | Página de resultados. |

**Salida (getUsersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`userArray`*` | `types:UserArray` | Sí | Matriz de usuarios. |

## Ejemplos {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Este ejemplo de código devuelve la matriz de usuarios para varios parámetros opcionales. Las funciones de usuario, los campos de filtro de caracteres de usuario y los campos de ordenación de usuarios se determinan mediante constantes de cadena específicas.

**Solicitar**

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

