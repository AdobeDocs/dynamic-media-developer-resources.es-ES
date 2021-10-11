---
title: Compatibilidad con vídeo externo
description: El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Compatibilidad con vídeo externo{#external-video-support}

El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o Adobe Experience Manager, Dynamic Media.

Los formatos admitidos para el vídeo externo son MP4 en formato H.264 o M3U8 en modo HLS.

El visor puede trabajar con vídeo de Dynamic Media Classic o Dynamic Media de Experience Manager o con vídeo externo. Si el visor comienza con vídeo de Dynamic Media de Dynamic Media Classic/AEM, debe utilizarse con este tipo de recurso a partir de ahora. No es posible cargar un vídeo externo en este visor utilizando el método [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) y, a la inversa. Es decir, si el visor se cargó inicialmente con vídeo externo, seguirá funcionando solo con vídeos externos.

Al trabajar con vídeo externo, el visor ignora el valor de cualquier modificador de reproducción y detecta el tipo de reproducción de la extensión de vídeo externa. Si la URL de vídeo externa termina con `.m3u8`, el visor utiliza la reproducción HLS; de lo contrario, se utiliza la reproducción progresiva.
