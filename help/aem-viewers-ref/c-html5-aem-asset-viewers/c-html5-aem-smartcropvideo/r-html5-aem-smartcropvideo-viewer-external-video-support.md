---
title: Compatibilidad con vídeo externo
description: 'El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o Adobe Experience Manager: Dynamic Media.'
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
TQID: 'https://experienceleague.adobe.com/nLVjtwe8hj5YpMX6M1GKt1Fx-tZK2Qxe1kdWcK8BQPw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 0%

---

# Compatibilidad con vídeo externo{#external-video-support}

El visor admite la reproducción de vídeo alojado fuera de Dynamic Media Classic o Adobe Experience Manager: Dynamic Media.

Los formatos admitidos para el vídeo externo son MP4 en formato H.264 o manifiesto M3U8 para flujo HLS.

El visor puede trabajar con Dynamic Media Classic o Experience Manager: vídeo de Dynamic Media o con vídeo externo. Si el visualizador comienza con un vídeo de Dynamic Media Classic/Dynamic Media, utilícelo con ese tipo de recurso a partir de ahora, no es posible cargar un vídeo externo en este visualizador mediante [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Y viceversa: si el visor se cargó inicialmente con vídeo externo, debe seguir trabajando con vídeos externos solamente.

Al trabajar con vídeo externo, el visor ignora el valor del modificador playback y detecta el tipo de reproducción de la extensión de vídeo externa. Si la dirección URL del vídeo externo termina con `.M3U8`, el visor está usando la reproducción de HLS; de lo contrario, se usa la reproducción progresiva.
