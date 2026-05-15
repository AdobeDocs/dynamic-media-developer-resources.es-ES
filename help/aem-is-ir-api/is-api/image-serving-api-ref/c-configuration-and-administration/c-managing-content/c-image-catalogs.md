---
description: Los catálogos de imágenes proporcionan muchas opciones de configuración del servidor, así como fuentes, perfiles ICC y macros de comandos.
solution: Experience Manager
title: Catálogos de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
TQID: 'https://experienceleague.adobe.com/kfojwk0K5RfRtZdxJmdojqsLirnP6LoXbtFRJ5272lg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# Catálogos de imágenes{#image-catalogs}

Los catálogos de imágenes proporcionan muchas opciones de configuración del servidor, así como fuentes, perfiles ICC y macros de comandos.

Asignan ID de contenido estático y de imagen utilizados en solicitudes a rutas de archivo reales, almacenan varios metadatos de imagen, como mapas de imagen, y proporcionan contenedores para plantillas y conjuntos de imágenes.

Solo el [!DNL Platform Server] tiene acceso a los catálogos de imágenes, nunca el servidor de imágenes. Los archivos de atributos de catálogo deben tener un sufijo .ini y colocarse en la carpeta de catálogo de [!DNL Platform Server] ( `PS::CatalogFolder`). Se requiere al menos el catálogo de imágenes predeterminado, que debe rellenarse con todos los atributos para que el [!DNL Platform Server] funcione correctamente.
