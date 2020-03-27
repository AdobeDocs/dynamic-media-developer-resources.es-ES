---
description: El visor admite la reproducción de vídeo alojado fuera de Scene7 Publishing System o AEM Dynamic Media.
seo-description: El visor admite la reproducción de vídeo alojado fuera de Scene7 Publishing System o AEM Dynamic Media.
seo-title: Compatibilidad con vídeo externo
solution: Experience Manager
title: Compatibilidad con vídeo externo
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Compatibilidad con vídeo externo{#external-video-support}

El visor admite la reproducción de vídeo alojado fuera de Scene7 Publishing System o AEM Dynamic Media.

Los formatos admitidos para el vídeo externo son MP4 en formato H.264 o M3U8 en flujo HLS.

El visor puede trabajar con vídeo de Scene7 o Dynamic Media o con vídeo externo. Si el visor inicio con vídeo de Scene7/Dynamic Media y lo utiliza con este tipo de recurso en adelante, no es posible cargar un vídeo externo en este visor con [ el `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) método . Y viceversa: si el visor se cargó inicialmente con vídeo externo, solo debería seguir trabajando con vídeos externos.

Al trabajar con vídeo externo, el visor ignora el valor del modificador de reproducción y detecta el tipo de reproducción de la extensión de vídeo externa. Si la URL de vídeo externa termina con .m3u8, el visor utiliza la reproducción HLS; de lo contrario, se utiliza la reproducción progresiva.
