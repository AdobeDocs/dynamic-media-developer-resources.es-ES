---
title: Compatibilidad con vídeo externo
description: El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Compatibilidad con vídeo externo{#external-video-support}

El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.

Los formatos admitidos para el vídeo externo son MP4 en formato H.264 o manifiesto M3U8 para flujo HLS.

El visor puede trabajar con Dynamic Media Classic o con vídeo Dynamic Media de Experience Manager o con vídeo externo. Si el visualizador comienza con un vídeo de Dynamic Media Classic/Dynamic Media, utilícelo con este tipo de recurso a partir de ahora, no es posible cargar un vídeo externo en este visualizador mediante [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Y viceversa: si el visor se cargó inicialmente con vídeo externo, debe seguir trabajando con vídeos externos solamente.

Al trabajar con vídeo externo, el visor ignora el valor del modificador playback y detecta el tipo de reproducción de la extensión de vídeo externa. Si la dirección URL del vídeo externo termina con `.M3U8` el visor utiliza la reproducción HLS; de lo contrario, se utiliza la reproducción progresiva.
