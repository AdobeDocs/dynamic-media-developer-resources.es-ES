---
description: Ajustes de configuración específicos de la empresa.
seo-description: Ajustes de configuración específicos de la empresa.
seo-title: Configuración de la empresa
solution: Experience Manager
title: Configuración de la empresa
uuid: a807d5c1-058d-4313-b4f8-6ee203284003
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 1%

---


# CompanySettings{#companysettings}

Ajustes de configuración específicos de la empresa.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`overwriteMode`*` | `xsd:string` | Determina si se sobrescribirán las imágenes de la carpeta actual con el mismo nombre de imagen base y extensión. |
| `*`keepPublishState`*` | `xsd:boolean` | Especifica si una imagen de reemplazo cargada en IPS debe conservar la configuración &quot;Listo para publicar&quot; existente o si debe ser la especificada por la carga. |
| `*`defaultSourceProfile`*` | `types:Asset` | Especifica el perfil de color de origen predeterminado (Coated FOGRA27 (ISO 126472:2004)) aplicado automáticamente como parte del &quot;Use default Color Behavior&quot; (Comportamiento de color predeterminado) al añadir archivos de imagen CMYK. |
| `*`defaultDisplayProfile`*` | `types:Asset` | Especifica el perfil de color interno predeterminado (U.S. Web Coated (SWOP) v2) aplicado automáticamente como parte del &quot;Usar comportamiento de color predeterminado&quot; al añadir archivos de imagen CMYK. |
| `*`iptcExifMappingXslt`*` | `types:Asset` | La extracción de datos de encabezado de imagen IPTC y EXIF en IPS requiere una conversión de nombres de campo internos a nombres de campo definidos por el usuario para la empresa. Determina una tabla de traducción XSL (el valor predeterminado es &quot;No extraer ningún campo IPTC o EXIF&quot;) para imágenes cargadas. |
| `*`xmpMappingXslt`*` | `types:Asset` | La extracción de XMP datos de encabezado de imagen en IPS requiere una conversión de nombres de campo internos a nombres de campo definidos por el usuario para la empresa. Determina una tabla de traducción XSL (el valor predeterminado es &quot;No extraer ningún campo de XMP&quot;) para las imágenes cargadas. |
| `*`diskSpaceWarningMin`*` | `xsd:int` | Cantidad mínima de espacio libre en disco del directorio de imágenes antes de enviar una advertencia. |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | Determina si se enviarán correos electrónicos antes de que se eliminen automáticamente los elementos colocados en la papelera. |
| `*`javascriptUploadEnabled`*` | `types:Asset` | Determina si se cargarán archivos JavaScript. Se trata de un posible riesgo para la seguridad, por lo que debe utilizarse esta opción con cuidado. |

