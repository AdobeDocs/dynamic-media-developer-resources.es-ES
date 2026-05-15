---
title: VideoScrubber.chaptertimepattern
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 93c1d38c-1f45-4794-8084-f520f9caf257
TQID: 'https://experienceleague.adobe.com/Md2edYK3N0jOA-KSqNXq1ttto1-3-tIgcWOkspphIqA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 2%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Atributo de configuración para el visualizador de vídeo interactivo.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Establece el patrón para el tiempo que se muestra en la barra de título de la etiqueta del capítulo, donde <span class="codeph"> h</span> representa horas, <span class="codeph"> m</span> para minutos y <span class="codeph"> s</span> para segundos. </p> <p>El número de letras utilizado para cada unidad de tiempo determina el número de dígitos que se mostrarán para la unidad. Si el número no cabe en los dígitos seleccionados, se muestra el valor equivalente en la unidad siguiente. </p> <p>Por ejemplo, si el tiempo de la película actual es de 67 minutos y 5 segundos, se mostrará un patrón de tiempo de <span class="codeph"> m:ss</span> como 67:05. La misma hora se muestra como 1:07:5 si el patrón de tiempo es <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
chaptertimepattern=h:mm:ss
```
