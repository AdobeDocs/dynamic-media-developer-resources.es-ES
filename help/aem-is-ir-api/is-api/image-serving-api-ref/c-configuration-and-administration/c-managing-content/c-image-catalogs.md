---
description: Los catálogos de imágenes proporcionan muchas opciones de configuración del servidor, así como fuentes, perfiles ICC y macros de comandos.
solution: Experience Manager
title: Catálogos de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Catálogos de imágenes{#image-catalogs}

Los catálogos de imágenes proporcionan muchas opciones de configuración del servidor, así como fuentes, perfiles ICC y macros de comandos.

Asignan ID de contenido estático y de imagen utilizados en solicitudes a rutas de archivo reales, almacenan varios metadatos de imagen, como mapas de imagen, y proporcionan contenedores para plantillas y conjuntos de imágenes.

Solo se puede acceder a los catálogos de imágenes a través de [!DNL Platform Server], nunca por el servidor de imágenes. Los archivos de atributos de catálogo deben tener un sufijo .ini y colocarse en la variable [!DNL Platform Server]Carpeta de catálogo de ( `PS::CatalogFolder`). Se requiere al menos el catálogo de imágenes predeterminado, que debe rellenarse con todos los atributos para el correcto funcionamiento del [!DNL Platform Server].
