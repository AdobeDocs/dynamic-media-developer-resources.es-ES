---
description: Atributo de configuración para el visor de vídeo interactivo.
seo-description: Atributo de configuración para el visor de vídeo interactivo.
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: dc2e7b18-abd7-4b53-a0c4-268ec9cf3cb4
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

Atributo de configuración para el visor de vídeo interactivo.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Establece el patrón para el tiempo que se muestra en la burbuja de tiempo, donde <span class="codeph"> h</span> representa horas, <span class="codeph"> m</span> durante minutos y <span class="codeph"> s</span> durante segundos. </p> <p>El número de letras utilizado para cada unidad de tiempo determina el número de dígitos que se mostrarán para la unidad. Si el número no puede encajar en los dígitos dados, el valor equivalente se muestra en la unidad siguiente. </p> <p>Por ejemplo, si el tiempo de la película actual es de 67 minutos y 5 segundos, un patrón de tiempo de <span class="codeph"> m:ss</span> se muestra como 67:05. La misma hora se muestra como 1:07:5 si el patrón de tiempo es <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```

