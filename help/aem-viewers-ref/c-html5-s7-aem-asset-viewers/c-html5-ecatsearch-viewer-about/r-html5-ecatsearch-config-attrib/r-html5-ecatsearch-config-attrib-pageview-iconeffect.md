---
description: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
uuid: c8d63ad9-6867-4b90-a113-6a75e394f706
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 4%

---


# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Habilita el <span class="codeph"> iconeffect</span> para que se muestre en la parte superior de la imagen cuando esta se encuentra en estado de restablecimiento y sugiere una acción disponible para interactuar con la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> contar</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el número máximo de veces que el <span class="codeph"> iconeffect</span> aparece y vuelve a aparecer. Un valor de <span class="codeph"> -1</span> indica que el icono siempre vuelve a aparecer indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fundido</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración de la animación de mostrar u ocultar, en segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Establece el número de segundos que el <span class="codeph"> iconeffect</span> permanece totalmente visible antes de que se oculte automáticamente. Es decir, el tiempo después de completar la animación de fundido pero antes de que comience la animación de fundido-out. Un valor de <span class="codeph"> 0</span> deshabilita el comportamiento de ocultación automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Opcional.

## Predeterminado {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## Ejemplo {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]
