---
description: Los catálogos de imágenes proporcionan muchas opciones de configuración de servidor, así como fuentes, perfiles ICC y macros de comandos.
seo-description: Los catálogos de imágenes proporcionan muchas opciones de configuración de servidor, así como fuentes, perfiles ICC y macros de comandos.
seo-title: Catálogos de imágenes
solution: Experience Manager
title: Catálogos de imágenes
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Catálogos de imágenes{#image-catalogs}

Los catálogos de imágenes proporcionan muchas opciones de configuración de servidor, así como fuentes, perfiles ICC y macros de comandos.

Asignan las ID de imagen y de contenido estático utilizadas en las solicitudes a las rutas de archivo reales, almacenan varios metadatos de imagen, como mapas de imagen, y proporcionan contenedores para las plantillas y los conjuntos de imágenes.

A los catálogos de imágenes solo se accede mediante el servidor de plataformas, nunca mediante el servidor de imágenes. Los archivos de atributos del catálogo deben tener un sufijo .ini y colocarse en la carpeta del catálogo de Platform Server ( `PS::CatalogFolder`). Al menos, el catálogo de imágenes predeterminado es obligatorio y debe rellenarse con todos los atributos para el correcto funcionamiento del servidor de plataformas.
