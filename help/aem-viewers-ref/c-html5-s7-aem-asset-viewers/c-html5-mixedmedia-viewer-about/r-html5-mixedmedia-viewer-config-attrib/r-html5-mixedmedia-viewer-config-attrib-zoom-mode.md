---
title: zoomMode
description: Establece el tipo de interacción de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# zoomMode{#zoommode}

Establece el tipo de interacción de zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuo </span> activa el zoom clásico en el que la imagen amplía gradualmente a medida que se hace clic, se pulsa dos veces o se contrae en la vista principal. Para volver a la vista inicial, aleje o restablezca el estado de zoom. La clase </p> <p> <span class="codeph"> en línea </span> activa el zoom instantáneo, en el que la imagen ampliada aparece instantáneamente al pasar el ratón por encima de la vista principal del escritorio o al tocarla y mantenerla en un dispositivo táctil. La imagen vuelve automáticamente al estado inicial después de mover el mouse (ratón) desde la vista o de soltar el dedo. Entrada <span class="codeph"> en línea </span> en este modo, los conjuntos de imágenes anidados se acoplan y se muestran como miniaturas individuales. La clase <span class="codeph"> auto </span> activa el modo inline en el escritorio y el modo continuous en los dispositivos táctiles. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
