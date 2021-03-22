---
description: El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o AEM Dynamic Media.
solution: Experience Manager
title: Compatibilidad con vídeo externo
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# Compatibilidad con vídeo externo{#external-video-support}

El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o AEM Dynamic Media.

Los formatos admitidos para el vídeo externo son MP4 en formato H.264 o M3U8 en modo HLS.

El visor puede trabajar con Dynamic Media Classic o AEM vídeo de Dynamic Media o con vídeo externo. Si el visor comienza con vídeo de Dynamic Media Classic/Dynamic Media, utilícelo con este tipo de recurso en adelante, no es posible cargar un vídeo externo en este visor utilizando el método [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) . Y viceversa: si el visor se cargó inicialmente con vídeo externo, solo debería seguir trabajando con vídeos externos.

Al trabajar con vídeo externo, el visor ignora el valor del modificador de reproducción y detecta el tipo de reproducción de la extensión de vídeo externa. Si la URL de vídeo externa termina con .m3u8, el visor utiliza la reproducción HLS; de lo contrario, se utiliza la reproducción progresiva.
