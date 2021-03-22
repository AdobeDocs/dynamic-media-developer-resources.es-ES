---
description: El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo de todos los catálogos de imágenes.
seo-description: El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo de todos los catálogos de imágenes.
seo-title: Catálogo predeterminado
solution: Experience Manager
title: Catálogo predeterminado
uuid: 9f0c967e-a2fa-4ef0-bacb-3dcfb06a8027
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Catálogo predeterminado{#default-catalog}

El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo de todos los catálogos de imágenes.

Si no se encuentra un atributo en particular en un catálogo de imágenes específico, el servidor utiliza el valor correspondiente del catálogo predeterminado en su lugar. Del mismo modo, el catálogo predeterminado se puede utilizar para proporcionar valores predeterminados para registros de datos de catálogo específicos (imágenes, definiciones de macro, fuentes y perfiles ICC). Si no se encuentra un registro de datos concreto en un catálogo de imágenes específico, el servidor intenta encontrarlo en el catálogo predeterminado. Esto permite que los catálogos de imágenes se rellenen escasamente y simplifica la administración de atributos y datos globales, como plantillas compartidas, macros, fuentes, etc.

Además, el catálogo predeterminado proporciona todos los atributos y registros de datos (macros, fuentes, perfiles ICC, reglas de preprocesamiento de solicitudes) cuando no hay ningún catálogo de imágenes específico involucrado en una operación.

Para el correcto funcionamiento del Servidor de plataforma, el archivo de atributos de catálogo para el catálogo predeterminado debe llamarse [!DNL default.ini], siempre debe existir en la carpeta del catálogo y debe rellenarse completamente con todos los atributos requeridos, excluyendo `attribute::RootId` y las referencias a los distintos archivos de datos del catálogo, que son todos opcionales.

>[!NOTE]
>
>Todos los archivos de atributos del catálogo excepto [!DNL default.ini] deben contener un valor único `attribute::RootId`. `attribute::RootId` en  [!DNL default.ini] debe estar vacío.

