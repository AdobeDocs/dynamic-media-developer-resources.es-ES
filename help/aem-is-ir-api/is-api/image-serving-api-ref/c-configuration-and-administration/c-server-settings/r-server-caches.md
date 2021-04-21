---
description: Utilice esta configuración de servidor para las cachés de servidor.
solution: Experience Manager
title: Cachés de servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# Cachés de servidor{#server-caches}

Utilice esta configuración de servidor para las cachés de servidor.

## PS::cache.rootPaths - Carpetas de datos de caché {#section-f0aa808304d74ecdb0c3644f11906c53}

Las carpetas raíz para la caché de disco de Platform Server. Una o más rutas de archivo absolutas o rutas relativas a *[!DNL install_folder]*, separadas por punto y coma (;). Los datos de la caché de respuestas HTTP se distribuirán uniformemente entre todas las carpetas especificadas. Las cachés para las cachés auxiliares (catálogos de imágenes compiladas y datos de imágenes externas) se ubicarán en la carpeta de caché principal (la primera carpeta de la lista).

## PS::cache.maxSize - Tamaño de caché de datos de respuesta {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

El tamaño máximo de la caché de respuesta HTTP en bytes. Esta configuración limita la cantidad de datos reales que se van a almacenar en caché; no tiene en cuenta la sobrecarga del sistema de archivos. (Consulte [Caché de datos de respuesta](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca)). Si se especifican varias carpetas de datos de caché, los datos de caché se distribuirán de manera uniforme en todas las carpetas. El valor de `cache.maxSize` en [!DNL PlatformServer.conf] está en bytes.

## PS::cache.maxEntries - Entradas máximas de caché de datos de respuesta {#section-5603e327e90542a5b50aeeb27b080410}

Número de entradas asignadas para el índice de caché de respuestas HTTP en memoria.

>[!NOTE]
>
>En Linux, asegúrese de que hay suficientes nodos i asignados para la partición de caché para evitar que se queden sin nodos i.

## IS::TempDirectory - Carpeta de archivos temporales del servidor de imágenes {#section-42ea1e7a68c444878f7245c5bbcb1672}

Ocasionalmente, el servidor de imágenes necesita guardar los datos intermedios en el disco. La ruta puede ser absoluta o relativa a *[!DNL install_folder]*.

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que los permisos de acceso estén establecidos para que Image Server tenga control total de la carpeta.

## SV::temp - Carpeta de archivos temporales del Supervisor del Servidor {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Ocasionalmente, el Supervisor del Servidor necesita guardar los datos intermedios en el disco. La ruta puede ser absoluta o relativa a *[!DNL install_folder]*. El valor predeterminado es [!DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que los permisos de acceso estén establecidos para que el Supervisor del servidor tenga control total de la carpeta.

