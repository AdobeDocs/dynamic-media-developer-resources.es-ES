---
description: Genera una nueva contraseña.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 18%

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
| `*`contraseña`*` | `xsd:string` | Sí | Una nueva contraseña. |

## Ejemplos {#section-f580fefdccec46fe95359e3aef0ed17f}

Este ejemplo de código genera una contraseña. Es inusual porque la solicitud es simplemente un parámetro sin elementos ni valores adjuntos. IPS devuelve una contraseña segura.

**Solicitar**

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

