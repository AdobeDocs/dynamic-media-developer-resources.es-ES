---
description: Los catálogos de materiales proporcionan muchos ajustes de configuración de procesamiento de imágenes.
solution: Experience Manager
title: Catálogos de materiales
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# Catálogos de materiales{#material-catalogs}

Los catálogos de materiales proporcionan muchos ajustes de configuración de procesamiento de imágenes.

Los catálogos de materiales asignan viñetas e id de materiales utilizados en solicitudes a rutas de archivos reales, pueden almacenar todos los metadatos asociados con materiales y proporcionar contenedores para plantillas. Rastrean los perfiles ICC y las macros de comandos.

Solo se puede acceder a los catálogos de materiales desde el componente Java de Image Rendering (ubicado junto con Platform Server). Los archivos de atributos del catálogo deben tener un sufijo [!DNL .ini] y colocarse en la carpeta de catálogo registrada ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). El catálogo de materiales predeterminado ( [!DNL default.ini]) siempre debe estar presente y debe rellenarse con todos los atributos para el correcto funcionamiento de Image Serving.
