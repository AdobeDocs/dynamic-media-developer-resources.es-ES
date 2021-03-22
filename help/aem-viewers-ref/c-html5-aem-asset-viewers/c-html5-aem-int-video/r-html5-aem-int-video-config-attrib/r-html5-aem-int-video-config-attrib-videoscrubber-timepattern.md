---
description: Atributo de configuración para el visualizador de vídeo interactivo.
seo-description: Atributo de configuración para el visualizador de vídeo interactivo.
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
uuid: dc2e7b18-abd7-4b53-a0c4-268ec9cf3cb4
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

Atributo de configuración para el visualizador de vídeo interactivo.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Establece el patrón para el tiempo que se muestra en la burbuja de tiempo, donde <span class="codeph"> h</span> representa horas, <span class="codeph"> m</span> para minutos y <span class="codeph"> s</span> para segundos. </p> <p>El número de letras utilizado para cada unidad de tiempo determina el número de dígitos que se mostrarán para la unidad. Si el número no cabe en los dígitos dados, el valor equivalente se muestra en la unidad siguiente. </p> <p>Por ejemplo, si el tiempo de la película actual es de 67 minutos y 5 segundos, el patrón de tiempo <span class="codeph"> m:ss</span> se muestra como 67:05. La misma hora se muestra como 1:07:5 si el patrón de tiempo es <span class="codeph"> h:mm:s</span>. </p> </td> 
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

