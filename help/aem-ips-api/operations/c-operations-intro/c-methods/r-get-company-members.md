---
description: Devuelve los usuarios de una compañía especificada por un identificador de compañía.
seo-description: Devuelve los usuarios de una compañía especificada por un identificador de compañía.
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
topic: Scene7 Image Production System API
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# getCompanyMembers{#getcompanymembers}

Devuelve los usuarios de una compañía especificada por un identificador de compañía.

Sintaxis

## Tipos de usuarios autorizados {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-5602e4d6f2214e398e6a804e61f1a088}

**Entrada (getCompanyMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía cuyos miembros desea obtener. |
| ` *`includeInvalid`*` | `xsd:boolean` | Sí | Incluir compañías no válidas. |

**Salida (getCompanyMembersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`miembroArray`*` | `types:CompanyMemberArray` | Sí | Matriz de pertenencias de usuario. |

## Ejemplos {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Este ejemplo de código devuelve todos los miembros de una compañía en una matriz de usuario. La respuesta se ha truncado para la brevedad.

**Solicitar**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**Respuesta**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```

