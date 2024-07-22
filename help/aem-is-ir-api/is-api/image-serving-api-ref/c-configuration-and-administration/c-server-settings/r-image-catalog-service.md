---
description: Utilice esta configuración de servidor para el servicio Catálogo de imágenes.
solution: Experience Manager
title: Servicio de catálogo de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Servicio de catálogo de imágenes{#image-catalog-service}

Utilice esta configuración de servidor para el servicio Catálogo de imágenes.

## CS::catalog.rootPath: carpeta del catálogo de imágenes {#section-02d107f157384b18835f884f24fea3aa}

Ubicación de la carpeta del catálogo de imágenes (donde deben estar ubicados los [!DNL catalog.ini] archivos). Puede ser una ruta de acceso absoluta o una ruta de acceso relativa al *[!DNL install_folder]*. El servidor supervisa continuamente esta carpeta y carga o vuelve a cargar los catálogos cuando se detecta un nuevo archivo de catálogo principal (con el sufijo de archivo [!DNL .ini]) o cuando cambia la hora de la última modificación de un archivo de catálogo principal existente.

## CS::catalog.cacheRoot: carpeta de caché de catálogo {#section-73e499c3a5974f1aa4251e70272ff503}

Carpeta raíz de la caché del sistema de catálogos. Puede establecerse en la misma carpeta que una de las carpetas de `PS::cache.rootPaths`. La carpeta debe crearse manualmente antes de cambiar esta configuración.

## CS::catalog.modifyWaitTime: retraso en el análisis del archivo de catálogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tiempo en ms que el servicio de catálogo espera a que se cambie un archivo de [!DNL catalog.ini] hasta que cargue los archivos de catálogo secundarios. Este retraso ayuda a garantizar que todos los archivos del catálogo secundario estén actualizados antes de que el servicio de catálogo intente cargarlos. Valor entero en ms.

## CS::catalog.refreshInterval: frecuencia de comprobación de archivos de catálogo {#section-517fefc1d8784777a1026abec8630d58}

Frecuencia con la que el servicio de catálogo comprueba los cambios en los catálogos de imágenes. Valor entero en ms.
