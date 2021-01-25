---
description: El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo de todos los catálogos de imágenes.
seo-description: El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo de todos los catálogos de imágenes.
seo-title: Catálogo predeterminado
solution: Experience Manager
title: Catálogo predeterminado
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9f0c967e-a2fa-4ef0-bacb-3dcfb06a8027
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# Catálogo predeterminado{#default-catalog}

El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo de todos los catálogos de imágenes.

Si no se encuentra un atributo concreto en un catálogo de imágenes específico, el servidor utiliza el valor correspondiente del catálogo predeterminado. Del mismo modo, el catálogo predeterminado se puede utilizar para proporcionar valores predeterminados para registros de datos de catálogo específicos (imágenes, definiciones de macro, fuentes y perfiles ICC). Si no se encuentra un registro de datos concreto en un catálogo de imágenes específico, el servidor intenta encontrarlo en el catálogo predeterminado. Esto permite que los catálogos de imágenes se llenen poco y simplifica la administración de atributos y datos globales, como plantillas compartidas, macros, fuentes, etc.

Además, el catálogo predeterminado proporciona todos los atributos y registros de datos (macros, fuentes, perfiles ICC, reglas de preprocesamiento de solicitudes) cuando no hay ningún catálogo de imágenes específico involucrado en una operación.

Para el correcto funcionamiento del servidor de plataformas, el archivo de atributos del catálogo predeterminado debe tener el nombre [!DNL default.ini], debe existir siempre en la carpeta del catálogo y debe rellenarse con todos los atributos requeridos, excluyendo `attribute::RootId` y las referencias a los diversos archivos de datos del catálogo, que son todos opcionales.

>[!NOTE]
>
>Todos los archivos de atributos del catálogo excepto [!DNL default.ini] deben contener un valor `attribute::RootId` único. `attribute::RootId` en  [!DNL default.ini] debe estar vacío.

