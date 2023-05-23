---
description: Utilice esta configuración de servidor para el servicio Catálogo de imágenes.
solution: Experience Manager
title: Servicio de catálogo de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# Servicio de catálogo de imágenes{#image-catalog-service}

Utilice esta configuración de servidor para el servicio Catálogo de imágenes.

## CS::catalog.rootPath: carpeta del catálogo de imágenes {#section-02d107f157384b18835f884f24fea3aa}

Ubicación de la carpeta del catálogo de imágenes (donde todas las [!DNL catalog.ini] deben encontrarse los archivos). Puede ser una ruta de archivo absoluta o una ruta relativa al *[!DNL install_folder]*. El servidor supervisa continuamente esta carpeta y carga o vuelve a cargar los catálogos cuando se crea un nuevo archivo de catálogo principal (con [!DNL .ini] se detecta (sufijo de archivo) o cuando ha cambiado la hora de la última modificación de un archivo de catálogo principal existente.

## CS::catalog.cacheRoot: carpeta de caché de catálogo {#section-73e499c3a5974f1aa4251e70272ff503}

Carpeta raíz de la caché del sistema de catálogos. Puede configurarse como una de las carpetas de `PS::cache.rootPaths`. La carpeta debe crearse manualmente antes de cambiar esta configuración.

## CS::catalog.modifyWaitTime: retraso en el análisis del archivo de catálogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tiempo en ms que el servicio de catálogo espera después de un [!DNL catalog.ini] se cambia el archivo hasta que carga los archivos del catálogo secundario. Este retraso ayuda a garantizar que todos los archivos del catálogo secundario estén actualizados antes de que el servicio de catálogo intente cargarlos. Valor entero en ms.

## CS::catalog.refreshInterval: frecuencia de comprobación de archivos de catálogo {#section-517fefc1d8784777a1026abec8630d58}

Frecuencia con la que el servicio de catálogo comprobará si hay cambios en los catálogos de imágenes. Valor entero en ms.
