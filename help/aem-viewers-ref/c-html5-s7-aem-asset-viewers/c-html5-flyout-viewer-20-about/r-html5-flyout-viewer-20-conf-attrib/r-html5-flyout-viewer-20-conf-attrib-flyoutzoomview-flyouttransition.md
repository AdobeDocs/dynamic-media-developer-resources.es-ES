---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
uuid: f1a9f2bc-9a13-4980-9241-e835a0aadd2c
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flotante
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|diapositiva|fundir  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto aplicado cuando se muestra u oculta la vista flotante. Con <span class="codeph"> ninguno </span>, la imagen flotante aparece instantáneamente cuando está activada y lista; <span class="codeph"> diapositiva </span> hace que la animación de la diapositiva se reproduzca en dirección de izquierda a derecha; <span class="codeph"> fundido </span> aplica una transición alfa a la imagen flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Número de segundos que tarda la animación del programa en completarse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> El retraso en segundos entre la acción del usuario que inicia la animación del programa y el comienzo mismo de la animación del programa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Número de segundos que tarda la animación oculta en completarse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> El retardo en segundos entre la acción del usuario que inicia la animación de ocultado y el comienzo mismo de la misma animación de ocultado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
