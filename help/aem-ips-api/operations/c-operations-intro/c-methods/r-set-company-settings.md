---
description: Establece varios valores de configuración específicos de la empresa.
seo-description: Establece varios valores de configuración específicos de la empresa.
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
uuid: 5908082f-6743-4444-ba73-757ad4664890
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 11%

---


# setCompanySettings{#setcompanysettings}

Establece varios valores de configuración específicos de la empresa.

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
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`overwriteMode`*` | `xsd:string` | No | Modo de sobrescritura de recursos. |
| `*`keepPublishState`*` | `xsd:boolean` | No | Configúrelo en `true` para preservar el estado de publicación cuando se vuelve a cargar un recurso. |
| `*`defaultSourceProfileHandle`*` | `xsd:string` | No | Recurso IccProfile que se utilizará como perfil de color de origen predeterminado. |
| `*`defaultDisplayProfileHandle`*` | `xsd:string` | No | Recurso IccProfile que se utilizará como perfil de color de visualización predeterminado. |
| `*`iptcExifMappingXsltHandle`*` | `xsd:string` | No | Recurso XSL utilizado para asignar metadatos IPTC y EXIF a campos de metadatos IPS. |
| `*`xmpMappingXsltHandle`*` | `xsd:string` | No | Recurso XSL utilizado para asignar metadatos de XMP a campos de metadatos IPS. |
| `*`diskSpaceWarningMin`*` | `xsd:int` | No | Espacio mínimo en disco libre (en KB) disponible antes de enviar un mensaje de advertencia. |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | No | Configúrelo en `true` para enviar a los administradores de la empresa una notificación cada vez que se vacíen los recursos de la papelera. |

**Salida (setCompanySettingsReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Este ejemplo de código establece la configuración de una empresa.

**Solicitar**

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
