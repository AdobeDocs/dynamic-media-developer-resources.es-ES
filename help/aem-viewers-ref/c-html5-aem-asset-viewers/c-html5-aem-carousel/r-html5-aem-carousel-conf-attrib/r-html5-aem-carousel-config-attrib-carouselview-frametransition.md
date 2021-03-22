---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
uuid: 9539ede1-08fb-4bfc-8a5a-870c7d84de7f
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`durationspacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|diapositiva  </span> </p> </td> 
   <td colname="col2"> <p>Especifica el tipo del efecto aplicado al cambiar el marco. <span class="codeph"> ninguno  </span> representa ninguna transición; el cambio de fotograma se produce instantáneamente. </p> <p> <span class="codeph"> fundido  </span> significa la transición entre fundido antiguo y nuevo. </p> <p> <span class="codeph"> diapositiva  </span> activa la transición en la que el marco antiguo se desliza de la vista y el nuevo marco se desliza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration  </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración (en segundo) del efecto de transición <span class="codeph"> fundido </span> o <span class="codeph"> diapositiva </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espaciado  </span> </span> </p> </td> 
   <td colname="col2"> <p>El espaciado entre marcos adyacentes en la transición <span class="codeph"> diapositiva </span>, tiene el rango entre <span class="codeph"> 0 </span> y <span class="codeph"> 1 </span> y es relativo al ancho del componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

Ninguno.

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
