---
description: Establece varios valores de configuración específicos de la compañía.
seo-description: Establece varios valores de configuración específicos de la compañía.
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
topic: Scene7 Image Production System API
uuid: 5908082f-6743-4444-ba73-757ad4664890
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de compañía. |
| ` *`overwriteMode`*` | `xsd:string` | No | Modo de sobrescritura de recursos. |
| ` *`keepPublishState`*` | `xsd:boolean` | No | Establezca `true` para conservar el estado de publicación cuando se vuelva a cargar un recurso. |
| ` *`defaultSourceProfileHandle`*` | `xsd:string` | No | Recurso IccProfile que se utilizará como perfil de color de origen predeterminado. |
| ` *`defaultDisplayProfileHandle`*` | `xsd:string` | No | Recurso IccProfile que se utilizará como perfil de color de visualización predeterminado. |
| ` *`iptcExifMappingXsltHandle`*` | `xsd:string` | No | Recurso XSL utilizado para asignar metadatos IPTC y EXIF a campos de metadatos IPS. |
| ` *`xmpMappingXsltHandle`*` | `xsd:string` | No | Recurso XSL utilizado para asignar metadatos de XMP a campos de metadatos IPS. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | No | Espacio mínimo disponible en disco (en KB) antes de enviar un mensaje de advertencia. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | No | Establezca `true` para enviar una notificación a los administradores de compañías cada vez que se vacían recursos de la papelera. |

**Salida (setCompanySettingsReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Este ejemplo de código establece la configuración de una compañía.

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
