---
description: Obtiene una lista de los caracteres utilizados en un campo concreto.
seo-description: Obtiene una lista de los caracteres utilizados en un campo concreto.
seo-title: getUserChars
solution: Experience Manager
title: getUserChars
topic: Scene7 Image Production System API
uuid: c9fa7826-5174-4298-99e6-a0627e432567
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 11%

---


# getUserChars{#getuserchars}

Obtiene una lista de los caracteres utilizados en un campo concreto.

Sintaxis

## Tipos de usuarios autorizados {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Entrada (getUserCharsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`charField`*` | `xsd:string` | Sí | Determina el estado de la papelera que se va a buscar. |
| ` *`includeInactive`*` | `xsd:boolean` | Sí | Incluir o excluir usuarios inactivos. Los usuarios administradores que no sean de IPS deben ser miembros activos de al menos una compañía para poder realizar llamadas de API. Se mostrará un error de autorización si el usuario no tiene miembros de compañía activos. |
| ` *`includeInvalid`*` | `xsd:boolean` | No | Incluir o excluir usuarios no válidos. |
| ` *`companyHandleArray`*` | `types:HandleArray` | No | Filtre los resultados según la compañía. |
| ` *`groupHandleArray`*` | `types:HandleArray` | No | Filtros los resultados en función de los grupos. |
| ` *`userRoleArray`*` | `types:StringArray` | No | Resultados de filtros basados en la función de usuario. |
| ` *`numChars`*` | `xsd:int` | No | Activar >1 carácter. |

**Salida (getUserCharsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`userCharsArray`*` | `types:StringArray` | Sí | Matriz de prefijos de caracteres. |

## Ejemplos {#section-3702f165e8b041139a6144f4a76ca25f}

Este ejemplo de código devuelve:

* Primeros caracteres de los apellidos de los usuarios de una compañía específica.
* Conjunto de grupos.
* Conjunto de funciones de usuario.

La constante de cadena Campos de filtro de caracteres de usuario determina el tipo de caracteres de usuario devueltos.

**Solicitar**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**Respuesta**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```

