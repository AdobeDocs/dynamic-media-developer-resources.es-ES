---
description: Establece los campos de metadatos de perfil ICC.
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
TQID: 'https://experienceleague.adobe.com/YmeLGJ9N-W-JOU7oG7utN4d1Q2pV17wtqocdrwYD-lQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 13%

---

# batchSetIccProfileFields{#batchseticcprofilefields}

Establece los campos de metadatos de perfil ICC.

Sintaxis

## Tipos de usuarios autorizados {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**Campos de entrada (batchSetIccProfile)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Administre a la compañía que contiene los perfiles ICC. |
| actualizar matriz | `xsd:string` | Sí | Matriz de actualizaciones de perfiles ICC. |

**Salida (batchSetIccProfileFields)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | `xsd:int` | Sí | El número de campos de perfil ICC definidos correctamente. |
| warningCount | `xsd:int` | Sí | El número de advertencias generadas cuando la operación intentó establecer los campos de perfil ICC. |
| errorCount | `xsd:int` | Sí | El número de errores generados cuando la operación intentó establecer los campos de perfil ICC. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó aplicar las actualizaciones. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó aplicar las actualizaciones. |

## Ejemplos {#section-5dc90cfbd9b1411485b44859032f7cb9}

**Solicitud**

```java {.line-numbers}
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

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```

