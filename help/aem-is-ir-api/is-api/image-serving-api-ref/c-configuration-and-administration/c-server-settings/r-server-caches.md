---
description: Utilice esta configuración de servidor para cachés de servidor.
solution: Experience Manager
title: Cachés de servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Cachés de servidor{#server-caches}

Utilice esta configuración de servidor para cachés de servidor.

## PS::cache.rootPaths - Carpetas de datos de caché {#section-f0aa808304d74ecdb0c3644f11906c53}

Las carpetas raíz de la caché de disco de [!DNL Platform Server]. Una o varias rutas de acceso o rutas de acceso de archivo absolutas relativas a *[!DNL install_folder]*, separadas por punto y coma (;). Los datos de la caché de respuestas HTTP se distribuyen de forma uniforme en todas las carpetas especificadas. Las cachés para las cachés auxiliares (catálogos de imágenes compiladas y datos de imágenes externas) se encuentran en la carpeta de caché principal (la primera carpeta de la lista).

## PS::cache.maxSize: tamaño del almacenamiento de datos de respuesta {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

Tamaño máximo de la caché de respuestas HTTP en bytes. Esta configuración limita la cantidad de datos reales que se van a almacenar en caché; no tiene en cuenta la sobrecarga del sistema de archivos. (Consulte [Caché de datos de respuesta](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Si se especifican varias carpetas de datos de caché, los datos de la caché se distribuyen de forma uniforme en todas las carpetas. El valor de `cache.maxSize` en [!DNL PlatformServer.conf] se encuentra en bytes.

## PS::cache.maxEntries - Entradas máximas de caché de datos de respuesta {#section-5603e327e90542a5b50aeeb27b080410}

Número de entradas asignadas para el índice de caché de respuestas HTTP en memoria.

>[!NOTE]
>
>En Linux, asegúrese de que haya suficientes nodos i asignados para la partición de caché a fin de evitar quedarse sin nodos i.

## IS::TempDirectory: carpeta de archivos temporales del servidor de imágenes {#section-42ea1e7a68c444878f7245c5bbcb1672}

En ocasiones, el servidor de imágenes necesita guardar datos intermedios en el disco. La ruta puede ser absoluta o relativa a *[!DNL install_folder]*.

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que los permisos de acceso estén configurados de modo que el servidor de imágenes tenga control total sobre la carpeta.

## SV::temp - Carpeta de archivos temporales del Supervisor del servidor {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

El Supervisor de servidor necesita guardar ocasionalmente los datos intermedios en el disco. La ruta puede ser absoluta o relativa a *[!DNL install_folder]*. El valor predeterminado es [!DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que los permisos de acceso estén configurados de modo que el Supervisor del servidor tenga control total de la carpeta.
