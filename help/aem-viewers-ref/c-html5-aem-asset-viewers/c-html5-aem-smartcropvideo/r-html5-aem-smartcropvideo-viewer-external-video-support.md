---
title: Compatibilidad con vídeo externo
description: El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Compatibilidad con vídeo externo{#external-video-support}

El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.

Los formatos admitidos para el vídeo externo son MP4 en formato H.264 o M3U8 en modo HLS.

El visor puede trabajar con Dynamic Media Classic o Experience Manager - vídeo Dynamic Media o con vídeo externo. Si el visor comienza con vídeo de Dynamic Media Classic/Dynamic Media, utilícelo con este tipo de recurso en adelante, no es posible cargar un vídeo externo en este visor utilizando [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Y viceversa: si el visor se cargó inicialmente con vídeo externo, solo debería seguir trabajando con vídeos externos.

Al trabajar con vídeo externo, el visor ignora el valor del modificador de reproducción y detecta el tipo de reproducción de la extensión de vídeo externa. Si la URL de vídeo externa termina con `.M3U8` el visor utiliza la reproducción HLS; de lo contrario, se utiliza la reproducción progresiva.
