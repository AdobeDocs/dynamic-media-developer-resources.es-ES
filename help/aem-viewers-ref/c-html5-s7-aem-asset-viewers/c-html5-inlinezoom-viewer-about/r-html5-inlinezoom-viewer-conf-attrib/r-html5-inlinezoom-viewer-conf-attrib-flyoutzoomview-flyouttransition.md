---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 3199d4a3-4799-40a2-b0a5-0e1ee4744fbe
TQID: 'https://experienceleague.adobe.com/FOK4Eoi3n-7LWZeJwciRFfkPTTnsrF-v-XI7APHiQIs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`showtime`*[, *`showdelay`*[, *`hidetime`*[, *`hidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ninguno|diapositiva|fundido </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo el efecto aplicado cuando se muestra o se oculta la vista flotante. Con <span class="codeph"> ninguno </span>, la imagen flotante aparece instantáneamente cuando se activa y está lista; con la diapositiva <span class="codeph"> </span>, la animación de diapositiva se reproduce en la dirección de izquierda a derecha; con <span class="codeph">, el fundido </span> aplica una transición alfa a la imagen flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tiempo de muestra </span> </span> </p> </td> 
   <td colname="col2"> <p> Número de segundos necesarios para completar la animación de mostrar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span> </span> </p> </td> 
   <td colname="col2"> <p> Retraso en segundos entre la acción del usuario que inicia la animación de mostrar y el inicio de dicha animación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime </span> </span> </p> </td> 
   <td colname="col2"> <p> Número de segundos que la animación de ocultar tarda en completarse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span> </span> </p> </td> 
   <td colname="col2"> <p> Retraso en segundos entre la acción del usuario que inicia la animación de ocultar y el inicio de dicha animación. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
