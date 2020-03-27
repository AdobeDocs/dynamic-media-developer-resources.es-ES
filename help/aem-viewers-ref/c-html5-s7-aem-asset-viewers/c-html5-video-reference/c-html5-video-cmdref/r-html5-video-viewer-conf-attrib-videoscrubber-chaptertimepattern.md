---
description: Atributo de configuración para el visor de vídeo.
seo-description: Atributo de configuración para el visor de vídeo.
seo-title: VideoScrubber.chaptertimepattern
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
topic: Dynamic media
uuid: 75338fa6-83ab-4cb8-babf-e958f97c1b6e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Atributo de configuración para el visor de vídeo.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Establece el patrón para el tiempo que se muestra en la barra de título de la etiqueta de capítulo de vídeo, donde <span class="codeph"> es horas,</span> m <span class="codeph"> es minutos y</span> s <span class="codeph"></span> es segundos. </p> <p>El número de letras utilizado para cada unidad de tiempo determina el número de dígitos que se mostrarán para la unidad. Si el número no puede encajar en los dígitos dados, el valor equivalente se muestra en la unidad siguiente. </p> <p>Por ejemplo, si el tiempo de la película actual es 67 minutos y 5 segundos, el patrón de tiempo <span class="codeph"> m:ss</span> se muestra como 67:05. La misma hora se muestra como 1:07:5 si el patrón de tiempo dado es <span class="codeph"> h:mm:s</span>. </p> </td> 
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

