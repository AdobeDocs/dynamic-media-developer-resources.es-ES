---
description: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de medios mixtos
role: Developer,User
exl-id: 0c79b3e2-ac5a-43c3-ac52-8240e7ed3cc1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Establece el patrón para el tiempo que se muestra en la barra de control, donde <span class="codeph"> h</span> es horas, <span class="codeph"> m</span> es minutos y <span class="codeph"> s</span> es segundos. </p> <p>El número de letras utilizado para cada unidad de tiempo determina el número de dígitos que se mostrarán para la unidad. Si el número no cabe en los dígitos dados, el valor equivalente se muestra en la unidad siguiente. </p> <p>Por ejemplo, si el tiempo de la película actual es de 67 minutos y 5 segundos, el patrón de tiempo <span class="codeph"> m:ss</span> se muestra como 67:05. La misma hora se muestra como 1:07:5 si el patrón de tiempo dado es <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
