---
description: Establece varios valores de configuración específicos de la compañía.
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
TQID: 'https://experienceleague.adobe.com/df-NUZDApA-q0a-A3oxM6PUQUoVmGy8gqS4HU8lhfvc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 11%

---

# setCompanySettings{#setcompanysettings}

Establece varios valores de configuración específicos de la compañía.

Sintaxis

## Tipos de usuarios autorizados {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-a472da6c57c74a94a179dda081004888}

**Entrada (setCompanySettingsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Manejo de la compañía. |
| overwriteMode | `xsd:string` | No | Modo de sobrescritura de recursos. |
| keepPublishState | `xsd:boolean` | No | Configúrelo en `true` para conservar el estado de publicación cuando se vuelva a cargar un recurso. |
| defaultSourceProfileHandle | `xsd:string` | No | Recurso IccProfile que se utilizará como perfil de color de origen predeterminado. |
| defaultDisplayProfileHandle | `xsd:string` | No | Recurso IccProfile que se utilizará como perfil de color de visualización predeterminado. |
| iptcExifMappingXsltHandle | `xsd:string` | No | Recurso XSL utilizado para asignar metadatos IPTC y EXIF a campos de metadatos IPS. |
| xmpMappingXsltHandle | `xsd:string` | No | Recurso XSL utilizado para asignar metadatos de XMP a campos de metadatos IPS. |
| diskSpaceWarningMin | `xsd:int` | No | Espacio en disco mínimo (en KB) disponible antes de enviar un mensaje de advertencia. |
| emailTrashCleanupWarning | `xsd:boolean` | No | Se establece en `true` para enviar una notificación a los administradores de la empresa cada vez que se eliminen recursos de la papelera. |

**Salida (setCompanySettingsReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Este ejemplo de código establece la configuración de una compañía.

**Solicitud**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**Respuesta**

Ninguno.
