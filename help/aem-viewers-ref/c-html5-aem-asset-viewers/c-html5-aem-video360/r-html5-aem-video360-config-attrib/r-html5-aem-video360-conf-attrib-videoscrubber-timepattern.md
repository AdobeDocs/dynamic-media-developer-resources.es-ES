---
title: VideoScrubber.timepattern
description: Atributo de configuración para el visor de Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f438a06b-6cf4-4bcd-9c4a-ed56f6a9c639
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

Atributo de configuración para el visor de Video360.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Establece el patrón para el tiempo que se muestra en la burbuja de tiempo, donde <span class="codeph"> h</span> es horas, <span class="codeph"> m</span> es minutos, y <span class="codeph"> s</span> es segundos. </p> <p>El número de letras utilizado para cada unidad de tiempo determina el número de dígitos que se mostrarán para la unidad. Si el número no cabe en los dígitos seleccionados, se muestra el valor equivalente en la unidad siguiente. </p> <p>Por ejemplo, si el tiempo de la película actual es de 67 minutos y 5 segundos, el patrón de tiempo <span class="codeph"> m:ss</span> se muestra a las 67:05. El mismo tiempo se muestra como 1:07:5 si el patrón de tiempo dado es <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
