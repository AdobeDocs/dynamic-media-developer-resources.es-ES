---
title: zoomMode
description: Establece el tipo de interacción de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
TQID: 'https://experienceleague.adobe.com/Joa1KBx6spGvXsMkjxSCPn-23cICUffLJ9CWOQ-BRwo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 2%

---

# zoomMode{#zoommode}

Establece el tipo de interacción de zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuo </span> habilita el zoom clásico en el que la imagen se amplía gradualmente a medida que hace clic, puntea dos veces o se reduce en la vista principal. Para volver a la vista inicial, aleje o restablezca el estado de zoom. La clase </p> <p> <span class="codeph"> en línea </span> permite el zoom instantáneo, donde la imagen ampliada aparece instantáneamente al pasar el ratón por la vista principal del escritorio o al tocar y mantener presionado un dispositivo táctil. La imagen vuelve automáticamente al estado inicial después de mover el mouse (ratón) desde la vista o de soltar el dedo. En el modo <span class="codeph"> en línea </span>, los conjuntos de imágenes anidados se acoplan y se muestran como miniaturas individuales. La clase <span class="codeph"> activa automáticamente </span> el modo en línea en el escritorio y el modo continuo en los dispositivos táctiles. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
