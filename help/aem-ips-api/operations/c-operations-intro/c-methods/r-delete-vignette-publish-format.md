---
description: Elimina un formato de publicación de viñeta.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 14%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

Elimina un formato de publicación de viñeta.

## Tipos de usuarios autorizados {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-789625ba29df4b5f880914d4c64f77ce}

**Entrada (deleteVignettePublishFormatParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía a la que pertenece la viñeta. |
| vignetteFormatHandle | `xsd:string` | Sí | El identificador del formato de publicación de viñeta que se va a eliminar. |

**Salida (deleteVignettePublishFormatParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Este ejemplo de código elimina un formato de publicación de viñeta especificado por su identificador.

**Solicitar**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Respuesta**

Ninguno.
