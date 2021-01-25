---
description: Los catálogos de materiales proporcionan muchos ajustes de configuración de procesamiento de imágenes.
seo-description: Los catálogos de materiales proporcionan muchos ajustes de configuración de procesamiento de imágenes.
seo-title: Catálogos de materiales
solution: Experience Manager
title: Catálogos de materiales
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# Catálogos de materiales{#material-catalogs}

Los catálogos de materiales proporcionan muchos ajustes de configuración de procesamiento de imágenes.

Los catálogos de materiales asignan las identificaciones de viñetas y materiales utilizadas en las solicitudes a las rutas de archivos reales, pueden almacenar todos los metadatos asociados a los materiales y proporcionar contenedores para las plantillas. Rastrean los perfiles ICC y las macros de comandos.

A los catálogos de materiales solo se accede mediante el componente Java de Procesamiento de imágenes (ubicado junto con el Servidor de plataformas). Los archivos de atributos del catálogo deben tener un sufijo [!DNL .ini] y colocarse en la carpeta de catálogo registrada ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). El catálogo de materiales predeterminado ( [!DNL default.ini]) siempre debe estar presente y debe rellenarse con todos los atributos para el correcto funcionamiento del servicio de imágenes.
