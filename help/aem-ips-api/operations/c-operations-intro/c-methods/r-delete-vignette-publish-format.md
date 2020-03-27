---
description: Elimina un formato de publicación de viñeta.
seo-description: Elimina un formato de publicación de viñeta.
seo-title: deleteVignettePublishFormat
solution: Experience Manager
title: deleteVignettePublishFormat
topic: Scene7 Image Production System API
uuid: 3c8148d5-dec6-4ffa-8ab8-2cd70811ada6
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía a la que pertenece la viñeta. |
| ` *`vignetteFormatHandle`*` | `xsd:string` | Sí | Identificador del formato de publicación de la viñeta que se va a eliminar. |

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
