---
description: Genera una nueva contraseña.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
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
