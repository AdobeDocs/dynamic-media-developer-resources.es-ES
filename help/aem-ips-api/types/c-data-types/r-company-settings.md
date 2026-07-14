---
description: Ajustes de configuración específicos de la empresa.
solution: Experience Manager
title: ConfiguraciónDeEmpresa
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
TQID: 'https://experienceleague.adobe.com/iGc-AwCFbpkATjLjvSBtx4vsP0-OUDSkH2dFHZ-j2rg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 244
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

Ajustes de configuración específicos de la empresa.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| overwriteMode | `xsd:string` | Determina si se sobrescribirán las imágenes de la carpeta actual con el mismo nombre y extensión de la imagen base. |
| keepPublishState | `xsd:boolean` | Especifica si una imagen de sustitución cargada en IPS debe conservar la configuración existente de &quot;Listo para publicar&quot; o si debe utilizar la configuración especificada en la carga. |
| defaultSourceProfile | `types:Asset` | Especifica el perfil de color de origen predeterminado (Coated FOGRA27 (ISO 126472:2004)) aplicado automáticamente como parte de &quot;Usar comportamiento de color predeterminado&quot; al agregar archivos de imagen CMYK. |
| defaultDisplayProfile | `types:Asset` | Especifica el perfil de color interno predeterminado (U.S. Web Coated (SWOP) v2) aplicado automáticamente como parte de &quot;Usar comportamiento de color predeterminado&quot; al agregar archivos de imagen CMYK. |
| iptcExifMappingXslt | `types:Asset` | La extracción de datos de encabezados de imagen IPTC y EXIF en IPS requiere una conversión de nombres de campo internos a nombres de campo definidos por el usuario para la empresa. Determina una tabla de traducción XSL (el valor predeterminado es &quot;No extraer campos IPTC o EXIF&quot;) para las imágenes cargadas. |
| xmpMappingXslt | `types:Asset` | Para extraer datos de encabezados de imagen de XMP en IPS, es necesario convertir los nombres de campo internos en nombres de campo definidos por el usuario para la empresa. Determina una tabla de traducción XSL (el valor predeterminado es &quot;No extraer campos XMP&quot;) para las imágenes cargadas. |
| diskSpaceWarningMin | `xsd:int` | Cantidad mínima de espacio libre en disco en el directorio de imágenes antes de enviar una advertencia. |
| emailTrashCleanupWarning | `xsd:boolean` | Determina si se enviarán correos electrónicos antes de que los elementos de la papelera se eliminen automáticamente. |
| javascriptUploadEnabled | `types:Asset` | Determina si se cargarán archivos de JavaScript. Esta opción supone un riesgo de seguridad potencial, por lo que debe utilizarse con cuidado. |

