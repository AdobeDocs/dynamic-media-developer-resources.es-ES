---
description: Utilice esta configuración de servidor para el servicio de catálogo de imágenes.
seo-description: Utilice esta configuración de servidor para el servicio de catálogo de imágenes.
seo-title: Servicio de catálogo de imágenes
solution: Experience Manager
title: Servicio de catálogo de imágenes
uuid: 601b1c30-7d51-448b-97b5-5ad9cb383975
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Servicio de catálogo de imágenes{#image-catalog-service}

Utilice esta configuración de servidor para el servicio de catálogo de imágenes.

## CS::catalog.rootPath: Carpeta de catálogo de imágenes {#section-02d107f157384b18835f884f24fea3aa}

Ubicación de la carpeta del catálogo de imágenes (donde deben ubicarse todos los archivos [!DNL catalog.ini]). Puede ser una ruta absoluta del archivo o una ruta relativa a *[!DNL install_folder]*. El servidor supervisa continuamente esta carpeta y carga o vuelve a cargar catálogos cuando se detecta un nuevo archivo de catálogo principal (con el sufijo [!DNL .ini]) o cuando ha cambiado la última vez que se modificó un archivo de catálogo principal existente.

## CS::catalog.cacheRoot - Carpeta de caché del catálogo {#section-73e499c3a5974f1aa4251e70272ff503}

La carpeta raíz de la caché del sistema del catálogo. Puede configurarse como una de las carpetas de `PS::cache.rootPaths`. La carpeta debe crearse manualmente antes de cambiar esta configuración.

## CS::catalog.modifyWaitTime - Retraso en el análisis de archivos del catálogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tiempo en msec el servicio de catálogo espera después de cambiar un archivo [!DNL catalog.ini] hasta que carga los archivos de catálogo secundarios. Este retraso ayuda a garantizar que todos los archivos de catálogo secundarios estén actualizados antes de que el servicio de catálogo intente cargarlos. Valor entero en msec.

## CS::catalog.refreshInterval - Frecuencia de comprobación de archivos del catálogo {#section-517fefc1d8784777a1026abec8630d58}

Frecuencia con la que el servicio de catálogo comprobará si hay cambios en los catálogos de imágenes. Valor entero en msec.
