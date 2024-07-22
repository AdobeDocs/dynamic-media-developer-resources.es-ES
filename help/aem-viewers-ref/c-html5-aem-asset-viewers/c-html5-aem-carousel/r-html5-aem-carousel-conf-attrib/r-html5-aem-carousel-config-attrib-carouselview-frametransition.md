---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`duration`*[, *`espaciado`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|fundido|diapositiva </span> </p> </td> 
   <td colname="col2"> <p>Especifica el tipo del efecto aplicado al cambio de fotograma. Por ejemplo, <span class="codeph"> none </span> significa que no hay transición; el cambio de fotograma se produce instantáneamente. Y, </p> <p> <span class="codeph"> fundido </span> significa transición de fundido cruzado entre fotogramas antiguos y nuevos. Finalmente, </p> <p> <span class="codeph"> diapositiva </span> activa la transición en la que el fotograma antiguo se desliza fuera de la vista y el nuevo fotograma se desliza hacia adentro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duración </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración (en segundos) del efecto de transición <span class="codeph"> fundido </span> o <span class="codeph"> diapositiva </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espaciado </span> </span> </p> </td> 
   <td colname="col2"> <p>El espaciado entre los fotogramas adyacentes en la transición de la diapositiva <span class="codeph"> </span> tiene un intervalo de <span class="codeph"> 0 </span> a <span class="codeph"> 1 </span> y es relativo a la anchura del componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

Ninguno.

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
