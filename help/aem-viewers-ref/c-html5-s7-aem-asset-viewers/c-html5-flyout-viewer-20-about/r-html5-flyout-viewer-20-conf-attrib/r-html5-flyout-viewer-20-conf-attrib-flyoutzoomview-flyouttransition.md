---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: a15723fe-a8be-49c5-bad3-1a1360eeb232
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`hora del espectáculo`*[, *`showdelay`*[, *`esconderse`*[, *`hidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|fade </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo el efecto aplicado cuando se muestra o se oculta la vista flotante. Con <span class="codeph"> ninguno </span>, la imagen flotante aparece instantáneamente cuando se activa y está lista; <span class="codeph"> diapositiva </span> hace que la animación de diapositiva se reproduzca en dirección de izquierda a derecha; <span class="codeph"> atenuación </span> aplica una transición alfa a la imagen flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hora del espectáculo </span> </span> </p> </td> 
   <td colname="col2"> <p> Número de segundos necesarios para completar la animación de mostrar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span> </span> </p> </td> 
   <td colname="col2"> <p> Retraso en segundos entre la acción del usuario que inicia la animación de mostrar y el inicio de dicha animación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> esconderse </span> </span> </p> </td> 
   <td colname="col2"> <p> Número de segundos que la animación de ocultar tarda en completarse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span> </span> </p> </td> 
   <td colname="col2"> <p> Retraso en segundos entre la acción del usuario que inicia la animación de ocultar y el inicio de dicha animación. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
