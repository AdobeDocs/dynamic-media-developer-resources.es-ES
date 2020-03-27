---
description: nulo
seo-description: nulo
seo-title: Transición de zoomView.frame
solution: Experience Manager
title: Transición de zoomView.frame
topic: Dynamic media
uuid: 28e283ca-51d8-4d6c-9b8a-d16da21f4da1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Transición de zoomView.frame{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`espaciado`*[, *`de duración`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide </span> </p> </td> 
   <td colname="col2"> <p>Especifica el tipo de efecto aplicado al cambio de marco. <span class="codeph"> ninguno </span> significa que no haya transición; el cambio de fotograma se produce instantáneamente. <span class="codeph"> fundido </span> significa transición de fundido cruzado entre marcos antiguos y nuevos. <span class="codeph"> la diapositiva </span> activa la transición en la que se desliza el marco antiguo de la vista y se desliza el nuevo marco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duración </span></span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración (en segundo) del efecto de <span class="codeph"> fundido </span> o <span class="codeph"> de </span> transición de diapositivas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espaciado </span></span> </p> </td> 
   <td colname="col2"> <p>El espaciado entre los marcos adyacentes en <span class="codeph"> la </span> transición de la diapositiva, tiene el rango entre <span class="codeph"> 0 </span> y <span class="codeph"> 1 </span> y es relativo al ancho del componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

Ninguno.

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
