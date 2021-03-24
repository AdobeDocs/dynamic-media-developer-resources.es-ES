---
description: Elimina un formato de publicación de viñeta.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 13%

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
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa a la que pertenece la viñeta. |
| `*`viñetaFormatoControlador`*` | `xsd:string` | Sí | Identificador del formato de publicación de la viñeta que se va a eliminar. |

**Salida (deleteVignettePublishFormatParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Este ejemplo de código elimina un formato de publicación de viñeta especificado por su controlador.

**Solicitar**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Respuesta**

Ninguno.
