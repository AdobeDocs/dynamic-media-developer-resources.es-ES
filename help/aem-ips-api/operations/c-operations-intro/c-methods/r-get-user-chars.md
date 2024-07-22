---
description: Obtiene una lista de los caracteres utilizados en un campo concreto.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 10%

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
| charField | `xsd:string` | Sí | Determina el estado de la papelera que se va a buscar. |
| includeInactive | `xsd:boolean` | Sí | Incluir o excluir usuarios inactivos. Los usuarios que no son administradores de IPS deben ser miembros activos de al menos una compañía para poder realizar llamadas de API. Se devuelve un error de autorización si el usuario no tiene ninguna pertenencia activa a la compañía. |
| includeInvalid | `xsd:boolean` | No | Incluya o excluya usuarios no válidos. |
| companyHandleArray | `types:HandleArray` | No | Filtrar los resultados según la empresa. |
| groupHandleArray | `types:HandleArray` | No | Filtra los resultados según los grupos. |
| userRoleArray | `types:StringArray` | No | Filtra los resultados según la función del usuario. |
| numChars | `xsd:int` | No | Habilite >1 carácter. |

**Salida (getUserCharsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userCharsArray | `types:StringArray` | Sí | Matriz de prefijos de caracteres. |

## Ejemplos {#section-3702f165e8b041139a6144f4a76ca25f}

Este ejemplo de código devuelve:

* Primeros caracteres de los apellidos de los usuarios de una empresa específica.
* Un conjunto de grupos.
* Un conjunto de funciones de usuario.

La constante de cadena Campos del filtro de caracteres de usuario determina el tipo de caracteres de usuario devueltos.

**Solicitud**

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
