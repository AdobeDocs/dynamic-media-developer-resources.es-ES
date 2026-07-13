---
description: Los archivos de viñeta se pueden reemplazar o eliminar mientras el servidor está activo mediante el comando req=release justo antes de que se sobrescriba el archivo.
solution: Experience Manager
title: Eliminar o reemplazar archivos de datos de origen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
TQID: 'https://experienceleague.adobe.com/clXDwtsKfD4WkpgNvoJoXG19WvFkcOhdjtTGmoArpv4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 207
ht-degree: 0%

---

# Eliminar o reemplazar archivos de datos de origen{#deleting-or-replacing-source-data-files}

Los archivos de viñeta se pueden reemplazar o eliminar mientras el servidor está activo mediante el comando req=release justo antes de que se sobrescriba el archivo.

>[!NOTE]
>
>Un archivo de datos no debe reemplazarse ni eliminarse mientras el servidor de procesamiento esté accediendo a él.

Tenga en cuenta que eliminar o reemplazar un archivo de datos de origen solo hace que el servidor de procesamiento cierre el archivo hasta la siguiente solicitud que acceda a esa viñeta. Pueden ser necesarios varios reintentos si un archivo se utiliza con frecuencia.

El servidor de procesamiento debe detenerse para reemplazar otros archivos de datos.

[!DNL Platform Server] entradas de caché se invalidan automáticamente cuando se reemplazan archivos de material o viñetas. La sustitución de archivos de perfil ICC no invalida las cachés.

Para evitar las complicaciones derivadas de reemplazar archivos, se recomienda dar un nuevo nombre al archivo de reemplazo y actualizar las entradas de catálogo correspondientes. Esto permite reemplazar cualquier archivo de datos mientras el servidor esté activo y hace que las entradas de la caché del servidor queden obsoletas automáticamente sin ninguna intervención adicional. Este método se puede utilizar para todos los archivos de datos administrados por catálogos de imágenes.

