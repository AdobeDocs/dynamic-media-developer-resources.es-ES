---
description: El visor admite la reproducción de vídeo alojado fuera de SPS o AEM Dynamic Media.
seo-description: El visor admite la reproducción de vídeo alojado fuera de SPS o AEM Dynamic Media.
seo-title: Compatibilidad con vídeo externo
solution: Experience Manager
title: Compatibilidad con vídeo externo
topic: Dynamic media
uuid: 2e9f1c54-627f-4462-ae85-8a5ca1d09762
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Compatibilidad con vídeo externo{#external-video-support}

El visor admite la reproducción de vídeo alojado fuera de SPS o AEM Dynamic Media.

Los formatos admitidos para el vídeo externo son MP4 en formato H.264 o M3U8 en flujo HLS.

El visor puede trabajar con vídeo de Dynamic Media Classic o AEM Dynamic Media o con vídeo externo. Si el visor inicio con el vídeo de Dynamic Media Classic/AEM Dynamic Media, debería utilizarse con este tipo de recurso en adelante. No es posible cargar un vídeo externo en este visor con el método [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) y viceversa. Es decir, si el visor se cargó inicialmente con vídeo externo, seguirá funcionando solo con vídeos externos.

Al trabajar con vídeo externo, el visor ignora el valor de cualquier modificador de reproducción y detecta el tipo de reproducción de la extensión de vídeo externa. Si la URL de vídeo externa termina con `.m3u8`, el visor utiliza la reproducción HLS; en caso contrario, se utiliza la reproducción progresiva.
