---
title: Compatibilidad con vídeo externo
description: El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Compatibilidad con vídeo externo{#external-video-support}

El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.

Los formatos admitidos para el vídeo externo son MP4 en formato H.264 o manifiesto M3U8 para flujo HLS.

El visor puede trabajar con Dynamic Media Classic o con vídeo Dynamic Media de Experience Manager o con vídeo externo. Si el visor comienza con un vídeo de Dynamic Media Classic/Dynamic Media, utilícelo con ese tipo de recurso a partir de ahora, no es posible cargar un vídeo externo en este visor mediante el método [`setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Y viceversa: si el visor se cargó inicialmente con vídeo externo, debe seguir trabajando con vídeos externos solamente.

Al trabajar con vídeo externo, el visor ignora el valor del modificador playback y detecta el tipo de reproducción de la extensión de vídeo externa. Si la dirección URL de vídeo externa termina con `.m3u8`, el visor está usando reproducción HLS; de lo contrario, se usa la reproducción progresiva.
