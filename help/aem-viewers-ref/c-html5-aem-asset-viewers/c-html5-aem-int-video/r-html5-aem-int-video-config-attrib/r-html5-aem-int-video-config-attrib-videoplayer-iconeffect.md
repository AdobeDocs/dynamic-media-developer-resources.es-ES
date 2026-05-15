---
title: VideoPlayer.iconeffect
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
TQID: 'https://experienceleague.adobe.com/s2UgvZ7USvFjvZ8NBUKa1MHrRe9HOh-ZE-g7jpNyeeg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 3%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Atributo de configuración para el visualizador de vídeo interactivo.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Activa el IconEffect que se mostrará encima del vídeo cuando este se encuentra en pausa. En algunos dispositivos se utilizan controles nativos. En estos casos, se omite el modificador <span class="codeph"> iconeffect</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> recuento</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el número máximo de veces que IconEffect aparece y vuelve a aparecer. Un valor de <span class="codeph"> -1</span> indica que el icono reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fundido</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la duración en segundos de la animación de mostrar u ocultar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> ocultar automáticamente</span></span> </p> </td> 
   <td colname="col2"> <p> Establece el número de segundos que IconEffect permanece totalmente visible antes de ocultarse automáticamente. Es decir, el tiempo después de que se complete la transición en la animación y antes de que comience la animación de desaparición. Establezca el valor en <span class="codeph"> 0</span> para deshabilitar el comportamiento de ocultar automáticamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
