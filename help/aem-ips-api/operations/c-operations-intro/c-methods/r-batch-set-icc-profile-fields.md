---
description: Establece los campos de metadatos del perfil ICC.
seo-description: Establece los campos de metadatos del perfil ICC.
seo-title: batchSetIccProfileFields
solution: Experience Manager
title: batchSetIccProfileFields
topic: Scene7 Image Production System API
uuid: 163b9b36-85b6-4880-8029-8421b04f4a08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 13%

---


# batchSetIccProfileFields{#batchseticcprofilefields}

Establece los campos de metadatos del perfil ICC.

Sintaxis

## Tipos de usuarios autorizados {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**Entrada (batchSetIccProfileFields)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Gestionar la compañía que contiene los perfiles ICC. |
| ` *`actualizar matriz`*` | `xsd:string` | Sí | Matriz de actualizaciones de perfil ICC. |

**Salida (batchSetIccProfileFields)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sí | Número de campos de perfil ICC establecidos correctamente. |
| ` *`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó establecer los campos de perfil ICC. |
| ` *`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó establecer los campos de perfil ICC. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados a los recursos que generaron advertencias cuando la operación intentó aplicar las actualizaciones. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociada con los recursos que generaron errores cuando la operación intentó aplicar las actualizaciones. |

## Ejemplos {#section-5dc90cfbd9b1411485b44859032f7cb9}

**Solicitar**

```java
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**Respuesta**

```java
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```

