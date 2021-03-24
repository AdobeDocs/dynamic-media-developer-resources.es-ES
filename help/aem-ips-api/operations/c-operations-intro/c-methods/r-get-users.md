---
description: Obtiene una matriz de usuarios según lo especificado por los controladores de empresa, grupo y función de usuario. Esta operación permite ordenar los usuarios devueltos y filtrar por carácter.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 10%

---


# getUsers{#getusers}

Obtiene una matriz de usuarios según lo especificado por los controladores de empresa, grupo y función de usuario. Esta operación permite ordenar los usuarios devueltos y filtrar por carácter.

## Tipos de usuarios autorizados {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`includeInactive`*` | `xsd:boolean` | No | Incluir o excluir usuarios inactivos. Los usuarios administradores que no sean de IPS deben ser miembros activos de al menos una empresa para poder realizar llamadas de API. Se devolverá un error de autorización si el usuario no tiene miembros activos de la empresa. |
| `*`includeInvalid`*` | `xsd:boolean` | No | Permite incluir o excluir usuarios no válidos. |
| `*`companyHandleArray`*` | `types:HandleArray` | No | Filtrar resultados por empresa. |
| `*`groupHandleArray`*` | `types:HandleArray` | No | Filtrar resultados por grupo. |
| `*`userRoleArray`*` | `types:StringArray` | No | Filtre los resultados por función de usuario. |
| `*`charFilterField`*` | `xsd:string` | No | Filtrar los resultados por el prefijo de cadena del campo (consulte [!DNL Trash State).] |
| `*`charFilter`*` | `xsd:string` | No | Filtre los resultados por un carácter específico. |
| `*`sortBy`*` | `xsd:string` | No | Selección de campos de ordenación por el usuario. |
| `*`recordsPerPage`*` | `xsd:int` | No | Devuelve el número especificado de registros por página. |
| `*`resultsPage`*` | `xsd:int` | No | Resultados . |

**Salida (getUsersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | Sí | Una matriz de usuarios. |

## Ejemplos {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Este ejemplo de código devuelve la matriz de usuarios para varios parámetros opcionales. Las funciones de usuario, los campos de filtro de caracteres de usuario y los campos de ordenación de usuario se determinan mediante el uso de constantes de cadena específicas.

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

