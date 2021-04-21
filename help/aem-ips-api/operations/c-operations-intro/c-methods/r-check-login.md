---
description: Comprueba si un usuario con una empresa específica (identificada por identificador), una dirección de correo electrónico y una contraseña puede iniciar sesión.
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 12%

---


# checkLogin{#checklogin}

Comprueba si un usuario con una empresa específica (identificada por identificador), una dirección de correo electrónico y una contraseña puede iniciar sesión.

>[!NOTE]
>
>Si se omite el control de empresa, este método comprueba el inicio de sesión del usuario predeterminado.

## Tipos de usuarios autorizados {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-1ad4c0b4803b4388aedd655030676cb3}

**Entrada (checkLoginParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | No | El identificador de la empresa que contiene el usuario. |
| `*`correo electrónico`*` | `xsd:string` | Sí | La dirección de correo electrónico del usuario. |
| `*`contraseña`*` | `xsd:string` | Sí | La contraseña del usuario. |

**Salida (checkLoginParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`estado`*` | `xsd:string` | Sí | Estado de inicio de sesión del usuario. |

## Ejemplos {#section-23f90100a9d94bc7b4045634cccd1b98}

Este código de ejemplo utiliza un parámetro de gestión de empresa, una dirección de correo electrónico y una contraseña para determinar si un usuario puede iniciar sesión en IPS. Si el usuario *puede* iniciar sesión, este método devuelve la cadena `ValidLogin`. Si el usuario *no puede* iniciar sesión, este método devuelve la cadena `InvalidLogin`.

**Solicitar**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**Respuesta**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```

