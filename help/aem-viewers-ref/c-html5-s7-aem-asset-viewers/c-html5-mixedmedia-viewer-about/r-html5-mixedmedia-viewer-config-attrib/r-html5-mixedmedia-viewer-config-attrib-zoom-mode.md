---
description: Define el tipo de interacción de zoom.
seo-description: Define el tipo de interacción de zoom.
seo-title: zoomMode
solution: Experience Manager
title: zoomMode
topic: Dynamic media
uuid: fdbe7ab6-47db-46cf-8a0d-085c66d4b0f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# zoomMode{#zoommode}

Define el tipo de interacción de zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuo|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuas </span> permite aplicar zoom clásico donde la imagen se amplía gradualmente al hacer clic, tocar el doble o pellizcar en la vista principal. Debe reducir o restablecer explícitamente el estado de zoom para volver a la vista inicial. </p> <p> <span class="codeph"> en línea </span> permite el zoom instantáneo, donde la imagen ampliada aparece instantáneamente al pasar el ratón por encima de la vista principal en el equipo de escritorio o al tocar y mantener pulsada la imagen en un dispositivo táctil; la imagen vuelve automáticamente al estado inicial cuando mueve el ratón de la vista o suelta el dedo. Tenga en cuenta que, en <span class="codeph"> modo </span> en línea, los conjuntos de imágenes anidados se acoplan y se muestran como miniaturas individuales. <span class="codeph"> auto </span> activa el modo en línea en el escritorio y el modo continuo en dispositivos táctiles. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
