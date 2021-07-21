---
description: Los catálogos de imágenes proporcionan muchos ajustes de configuración del servidor, así como fuentes, perfiles ICC, macros de comandos.
solution: Experience Manager
title: Catálogos de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Catálogos de imágenes{#image-catalogs}

Los catálogos de imágenes proporcionan muchos ajustes de configuración del servidor, así como fuentes, perfiles ICC, macros de comandos.

Asignan identificadores de imagen y contenido estático utilizados en solicitudes a rutas de archivo reales, almacenan varios metadatos de imagen, como mapas de imágenes, y proporcionan contenedores para plantillas y conjuntos de imágenes.

Solo Platform Server accede a los catálogos de imágenes, nunca mediante Image Server. Los archivos de atributos del catálogo deben tener un sufijo .ini y colocarse en la carpeta de catálogo de Platform Server ( `PS::CatalogFolder`). Al menos el catálogo de imágenes predeterminado es obligatorio y debe rellenarse con todos los atributos para el correcto funcionamiento de Platform Server.
