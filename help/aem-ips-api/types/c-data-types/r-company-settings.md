---
description: Configuración específica de compañía.
seo-description: Configuración específica de compañía.
seo-title: CompanySettings
solution: Experience Manager
title: CompanySettings
topic: Scene7 Image Production System API
uuid: a807d5c1-058d-4313-b4f8-6ee203284003
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# CompanySettings{#companysettings}

Configuración específica de compañía.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`overwriteMode`*` | `xsd:string` | Determina si se deben sobrescribir las imágenes en la carpeta actual con el mismo nombre de imagen base y la misma extensión. |
| ` *`keepPublishState`*` | `xsd:boolean` | Especifica si una imagen de sustitución cargada en IPS debe conservar la configuración &quot;Listo para publicar&quot; existente o si debe ser la especificada por la carga. |
| ` *`defaultSourceProfile`*` | `types:Asset` | Especifica el perfil de color de origen predeterminado (Coated FOGRA27 (ISO 126472:2004)) aplicado automáticamente como parte del &quot;Usar comportamiento de color predeterminado&quot; al agregar archivos de imagen CMYK. |
| ` *`defaultDisplayProfile`*` | `types:Asset` | Especifica el perfil de color interno predeterminado (U.S. Web Coated (SWOP) v2) aplicado automáticamente como parte del &quot;Usar comportamiento de color predeterminado&quot; al agregar archivos de imagen CMYK. |
| ` *`iptcExifMappingXslt`*` | `types:Asset` | La extracción de datos de encabezados de imagen IPTC y EXIF en IPS requiere una conversión de nombres de campo internos a nombres de campo definidos por el usuario para la compañía. Determina una tabla de traducción XSL (el valor predeterminado es &quot;No extraer ningún campo IPTC o EXIF&quot;) para las imágenes cargadas. |
| ` *`xmpMappingXslt`*` | `types:Asset` | La extracción de XMP datos de encabezados de imagen en IPS requiere una conversión de nombres de campo internos a nombres de campo definidos por el usuario para la compañía. Determina una tabla de traducción XSL (el valor predeterminado es &quot;No extraer ningún campo de XMP&quot;) para las imágenes cargadas. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | Cantidad mínima de espacio libre en disco del directorio de imágenes antes de enviar una advertencia. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | Determina si se deben enviar correos electrónicos antes de que los elementos colocados en la papelera se eliminen automáticamente. |
| ` *`javascriptUploadEnabled`*` | `types:Asset` | Determina si se cargan archivos JavaScript. Se trata de un riesgo potencial para la seguridad, por lo que debe utilizar esta opción con cuidado. |

