---
description: Los catálogos de imágenes proporcionan muchos ajustes de configuración del servidor, así como fuentes, perfiles ICC, macros de comandos.
seo-description: Los catálogos de imágenes proporcionan muchos ajustes de configuración del servidor, así como fuentes, perfiles ICC, macros de comandos.
seo-title: Catálogos de imágenes
solution: Experience Manager
title: Catálogos de imágenes
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Catálogos de imágenes{#image-catalogs}

Los catálogos de imágenes proporcionan muchos ajustes de configuración del servidor, así como fuentes, perfiles ICC, macros de comandos.

Asignan identificadores de imagen y contenido estático utilizados en solicitudes a rutas de archivo reales, almacenan varios metadatos de imagen, como mapas de imágenes, y proporcionan contenedores para plantillas y conjuntos de imágenes.

Solo Platform Server accede a los catálogos de imágenes, nunca mediante Image Server. Los archivos de atributos del catálogo deben tener un sufijo .ini y colocarse en la carpeta de catálogo de Platform Server ( `PS::CatalogFolder`). Al menos el catálogo de imágenes predeterminado es obligatorio y debe rellenarse con todos los atributos para el correcto funcionamiento de Platform Server.
