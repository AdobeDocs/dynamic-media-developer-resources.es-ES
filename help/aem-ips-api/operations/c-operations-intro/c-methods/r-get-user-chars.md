---
description: Obtiene una lista de los caracteres utilizados en un campo concreto.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '180'
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
| `*`charField`*` | `xsd:string` | Sí | Determina el estado de la Papelera que se va a buscar. |
| `*`includeInactive`*` | `xsd:boolean` | Sí | Incluir o excluir usuarios inactivos. Los usuarios administradores que no sean de IPS deben ser miembros activos de al menos una empresa para poder realizar llamadas de API. Se devolverá un error de autorización si el usuario no tiene miembros activos de la empresa. |
| `*`includeInvalid`*` | `xsd:boolean` | No | Incluir o excluir usuarios no válidos. |
| `*`companyHandleArray`*` | `types:HandleArray` | No | Filtre los resultados según la empresa. |
| `*`groupHandleArray`*` | `types:HandleArray` | No | Filtra los resultados según los grupos. |
| `*`userRoleArray`*` | `types:StringArray` | No | Filtra los resultados según la función del usuario. |
| `*`numChars`*` | `xsd:int` | No | Activar >1 carácter. |

**Salida (getUserCharsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`userCharsArray`*` | `types:StringArray` | Sí | Matriz de prefijos de caracteres. |

## Ejemplos {#section-3702f165e8b041139a6144f4a76ca25f}

Este ejemplo de código devuelve:

* Primeros caracteres de los apellidos de los usuarios de una empresa específica.
* Conjunto de grupos.
* Conjunto de funciones de usuario.

La constante de cadena Campos de filtro de caracteres del usuario determina el tipo de caracteres de usuario devueltos.

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
