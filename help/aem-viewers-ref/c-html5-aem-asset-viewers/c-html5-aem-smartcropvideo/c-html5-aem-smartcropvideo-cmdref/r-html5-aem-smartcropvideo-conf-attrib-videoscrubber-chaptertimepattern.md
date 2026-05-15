---
title: VideoScrubber.chaptertimepattern
description: Atributo de configuración para el visor de recorte inteligente de vídeos.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5552ed9e-d8fe-4723-a360-405b91e27f8e
TQID: 'https://experienceleague.adobe.com/YecN38lTxR5ErFtAiPztp11CG0Wi91hedFgXv9GIn-A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Atributo de configuración para el visor de recorte inteligente de vídeos.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Establece el patrón para el tiempo que se muestra en la barra de título de la etiqueta del capítulo de vídeo. <span class="codeph"> h</span> es horas, <span class="codeph"> m</span> es minutos y <span class="codeph"> s</span> es segundos. </p> <p>El número de letras utilizado para cada unidad de tiempo determina el número de dígitos que se mostrarán para la unidad. Si el número no cabe en los dígitos seleccionados, se muestra el valor equivalente en la unidad siguiente. </p> <p>Por ejemplo, si el tiempo de la película actual es de 67 minutos y 5 segundos, el patrón de tiempo <span class="codeph"> m:ss</span> se muestra como 67:05. La misma hora se muestra como 1:07:5 si el patrón de tiempo dado es <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```
