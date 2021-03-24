---
description: Los archivos de viñeta se pueden reemplazar o eliminar mientras el servidor está activo utilizando el comando req=release justo antes de que se sobrescriba el archivo.
solution: Experience Manager
title: Eliminación o reemplazo de archivos de datos de origen
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Eliminación o reemplazo de archivos de datos de origen{#deleting-or-replacing-source-data-files}

Los archivos de viñeta se pueden reemplazar o eliminar mientras el servidor está activo utilizando el comando req=release justo antes de que se sobrescriba el archivo.

>[!NOTE]
>
>Un archivo de datos no debe reemplazarse ni eliminarse mientras el servidor de procesamiento accede a él.

Tenga en cuenta que eliminar o reemplazar un archivo de datos de origen solo hace que el servidor de procesamiento cierre el archivo hasta la siguiente solicitud que acceda a esa viñeta. Puede que sean necesarios varios reintentos si se utiliza un archivo de forma intensiva.

El servidor de procesamiento debe detenerse para reemplazar otros archivos de datos.

Las entradas de caché de Platform Server se invalidan automáticamente cuando se reemplazan archivos de material o viñetas. Sustituir archivos de perfil ICC no invalida las cachés.

Para evitar las complicaciones de reemplazar archivos, se recomienda dar un nombre nuevo a un archivo de reemplazo y actualizar las entradas de catálogo correspondientes. Esto permite reemplazar cualquier archivo de datos mientras el servidor está activo y hace que las entradas de caché del servidor se vuelvan obsoletas automáticamente sin intervención adicional. Este método se puede utilizar para todos los archivos de datos administrados por catálogos de imágenes.
