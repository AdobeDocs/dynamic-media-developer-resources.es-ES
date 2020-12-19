---
description: Utilice esta configuración de servidor para el servicio de catálogo de imágenes.
seo-description: Utilice esta configuración de servidor para el servicio de catálogo de imágenes.
seo-title: Servicio de catálogo de imágenes
solution: Experience Manager
title: Servicio de catálogo de imágenes
topic: Scene7 Image Serving - Image Rendering API
uuid: 601b1c30-7d51-448b-97b5-5ad9cb383975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Servicio de catálogo de imágenes{#image-catalog-service}

Utilice esta configuración de servidor para el servicio de catálogo de imágenes.

## CS::catalog.rootPath - Carpeta del catálogo de imágenes {#section-02d107f157384b18835f884f24fea3aa}

Ubicación de la carpeta del catálogo de imágenes (donde deben encontrarse todos los archivos [!DNL catalog.ini]). Puede ser una ruta absoluta de archivo o una ruta relativa a *[!DNL install_folder]*. El servidor supervisa continuamente esta carpeta y carga o recarga los catálogos cuando se detecta un nuevo archivo de catálogo principal (con [!DNL .ini] sufijo de archivo) o cuando cambia la hora de la última modificación de un archivo de catálogo principal existente.

## CS::catalog.cacheRoot - Carpeta de caché del catálogo {#section-73e499c3a5974f1aa4251e70272ff503}

Carpeta raíz de la caché del sistema de catálogo. Puede configurarse en la misma que una de las carpetas de `PS::cache.rootPaths`. La carpeta debe crearse manualmente antes de cambiar esta configuración.

## CS::catalog.modifiedWaitTime - Retraso de análisis de archivos de catálogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tiempo en msec que el servicio de catálogo espera después de que se cambie un archivo [!DNL catalog.ini] hasta que se carguen los archivos de catálogo secundarios. Este retraso ayuda a garantizar que todos los archivos de catálogo secundarios estén actualizados antes de que el servicio de catálogo intente cargarlos. Valor entero en ms.

## CS::catalog.refreshInterval - Frecuencia de comprobación de archivos de catálogo {#section-517fefc1d8784777a1026abec8630d58}

Frecuencia con la que el servicio de catálogos comprueba si hay cambios en los catálogos de imágenes. Valor entero en ms.
