---
description: Utilice esta configuración de servidor para el servicio Catálogo de imágenes.
solution: Experience Manager
title: Servicio de catálogo de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
TQID: 'https://experienceleague.adobe.com/Fs2xGD3Dpd8pe5jtto4kPMF0BrJiLNRvdBn8RSPiQjw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 197
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
