---
description: Los archivos de viñeta se pueden reemplazar o eliminar mientras el servidor esté activo mediante el comando req=release justo antes de que se sobrescriba el archivo.
seo-description: Los archivos de viñeta se pueden reemplazar o eliminar mientras el servidor esté activo mediante el comando req=release justo antes de que se sobrescriba el archivo.
seo-title: Eliminación o reemplazo de archivos de datos de origen
solution: Experience Manager
title: Eliminación o reemplazo de archivos de datos de origen
topic: Scene7 Image Serving - Image Rendering API
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Eliminando o reemplazando archivos de datos de origen{#deleting-or-replacing-source-data-files}

Los archivos de viñeta se pueden reemplazar o eliminar mientras el servidor esté activo mediante el comando req=release justo antes de que se sobrescriba el archivo.

>[!NOTE]
>
>No se debe reemplazar ni eliminar un archivo de datos mientras el servidor de procesamiento accede a él.

Tenga en cuenta que si elimina o reemplaza un archivo de datos de origen, el servidor de procesamiento solo cerrará el archivo hasta la siguiente solicitud que acceda a esa viñeta. Es posible que sean necesarios varios reintentos si se utiliza mucho un archivo.

El servidor de procesamiento debe detenerse para reemplazar otros archivos de datos.

Las entradas de caché de Platform Server se invalidan automáticamente cuando se reemplazan archivos de material o viñetas. La sustitución de archivos perfil ICC no invalida las memorias caché.

Para evitar las complicaciones de reemplazar archivos, se recomienda asignar un nombre nuevo a un archivo de reemplazo y actualizar las entradas de catálogo correspondientes. Esto permite reemplazar cualquier archivo de datos mientras el servidor está activo y hace que las entradas de caché del servidor se vuelvan obsoletas automáticamente sin ninguna intervención adicional. Este método se puede utilizar para todos los archivos de datos administrados por catálogos de imágenes.
