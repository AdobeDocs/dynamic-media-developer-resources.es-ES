---
description: Devuelve los usuarios de una empresa especificada por el identificador de una empresa.
seo-description: Devuelve los usuarios de una empresa especificada por el identificador de una empresa.
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 14%

---


# getCompanyMembers{#getcompanymembers}

Devuelve los usuarios de una empresa especificada por el identificador de una empresa.

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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa cuyos miembros desea obtener. |
| `*`includeInvalid`*` | `xsd:boolean` | Sí | Incluir empresas no válidas. |

**Salida (getCompanyMembersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`memberArray`*` | `types:CompanyMemberArray` | Sí | Matriz de miembros de usuario. |

## Ejemplos {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Este ejemplo de código devuelve todos los miembros de una empresa en una matriz de usuario. La respuesta se ha truncado para su brevedad.

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

