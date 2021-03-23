---
description: Define los campos de metadatos de fuente.
seo-description: Define los campos de metadatos de fuente.
seo-title: batchSetFontFields
solution: Experience Manager
title: batchSetFontFields
uuid: 0209865e-32b3-4bea-a508-05771a0365e1
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 13%

---


# batchSetFontFields{#batchsetfontfields}

Define los campos de metadatos de fuente.

## Tipos de usuarios autorizados {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-836f5948d00a46e98ccb62f0573e4e68}

**Entrada (batchSetFontFieldsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Gestione a la empresa que contiene las fuentes. |
| `*`updateArray`*` | `types:FontFieldUpdateArray` | Sí | Matriz de actualizaciones de campos de fuente. |

**Salida (batchSetFontFieldsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sí | Número de campos de fuente definidos correctamente. |
| `*`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó establecer campos de fuente. |
| `*`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó establecer campos de fuente. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó aplicar las actualizaciones. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó aplicar las actualizaciones. |

## Ejemplos {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**Solicitar**

```java
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**Respuesta**

```java
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```

