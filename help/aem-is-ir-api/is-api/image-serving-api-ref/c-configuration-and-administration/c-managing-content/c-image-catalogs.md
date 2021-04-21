---
description: Los catálogos de imágenes proporcionan muchos ajustes de configuración del servidor, así como fuentes, perfiles ICC, macros de comandos.
solution: Experience Manager
title: Catálogos de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Catálogos de imágenes{#image-catalogs}

Los catálogos de imágenes proporcionan muchos ajustes de configuración del servidor, así como fuentes, perfiles ICC, macros de comandos.

Asignan identificadores de imagen y contenido estático utilizados en solicitudes a rutas de archivo reales, almacenan varios metadatos de imagen, como mapas de imágenes, y proporcionan contenedores para plantillas y conjuntos de imágenes.

Solo Platform Server accede a los catálogos de imágenes, nunca mediante Image Server. Los archivos de atributos del catálogo deben tener un sufijo .ini y colocarse en la carpeta de catálogo de Platform Server ( `PS::CatalogFolder`). Al menos el catálogo de imágenes predeterminado es obligatorio y debe rellenarse con todos los atributos para el correcto funcionamiento de Platform Server.
