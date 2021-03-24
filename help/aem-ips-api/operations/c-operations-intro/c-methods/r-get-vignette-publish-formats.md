---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 22%

---


# getVignettePublishFormats{#getvignettepublishformats}

Sintaxis

## Tipos de usuarios autorizados {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**Entrada (getVignettePublishFormatsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa. |

**Salida (getVignettePublishFormatsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`vignetteFormatArray`*` | `types:VignettePublishFormatArray` | Sí | Matriz de formatos de publicación de viñetas. |

## Ejemplos {#section-2cc32b27cc6243b7b3e273cc05996226}

Este ejemplo de código devuelve dos formatos de publicación de viñeta asociados a una empresa específica. La información se devuelve en una matriz, que se trunca para su brevedad.

**Solicitar**

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**Respuesta**

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```

