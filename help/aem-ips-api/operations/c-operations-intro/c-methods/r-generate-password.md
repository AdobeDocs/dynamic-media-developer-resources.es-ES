---
description: Genera una nueva contraseña.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 16%

---

# generatePassword{#generatepassword}

Genera una nueva contraseña.

Sintaxis

## Tipos de usuarios autorizados {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-d516615c906240819a284786efb19863}

**Entrada (generatePasswordParam)**

Ninguno.

**Salida (generatePasswordParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| contraseña | `xsd:string` | Sí | Una nueva contraseña. |

## Ejemplos {#section-f580fefdccec46fe95359e3aef0ed17f}

Este ejemplo de código genera una contraseña. No es habitual porque la solicitud es simplemente un parámetro sin elementos ni valores incluidos. IPS devuelve una contraseña segura.

**Solicitud**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**Respuesta**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```
