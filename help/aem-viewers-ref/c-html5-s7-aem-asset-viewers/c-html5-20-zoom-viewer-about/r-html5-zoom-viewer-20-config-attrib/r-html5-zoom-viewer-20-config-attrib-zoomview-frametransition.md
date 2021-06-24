---
description: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Developer,Business Practitioner
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 5%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *``*[, *`durationspacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|diapositiva  </span> </p> </td> 
   <td colname="col2"> <p>Especifica el tipo del efecto aplicado al cambiar el marco. <span class="codeph"> ninguno  </span> significa transición; el cambio de fotograma se produce instantáneamente. <span class="codeph"> fundido  </span> significa la transición entre fundido antiguo y nuevo. <span class="codeph"> diapositiva  </span> activa la transición en la que el marco antiguo se desliza de la vista y el nuevo marco se desliza. </p> </td> 
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

`frametransition=fade,1`
