---
description: Define el tipo de interacción de zoom.
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Developer,Business Practitioner
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---

# zoomMode{#zoommode}

Define el tipo de interacción de zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuo|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> contínuo  </span> permite el zoom clásico, donde la imagen se amplía gradualmente al hacer clic, tocar dos veces o pellizcar hacia afuera en la vista principal. Debe reducir o restablecer explícitamente el estado del zoom para volver a la vista inicial. </p> <p> <span class="codeph"> en línea  </span> permite el zoom instantáneo, en el que la imagen ampliada aparece instantáneamente al pasar el ratón por encima de la vista principal en el escritorio o al tocar y mantener en un dispositivo táctil; la imagen cambia automáticamente al estado inicial una vez que mueve el ratón de la vista o suelta el dedo. Tenga en cuenta que en el modo <span class="codeph"> en línea </span> los conjuntos de imágenes anidados se acoplan y se muestran como miniaturas individuales. <span class="codeph"> activa automáticamente  </span> el modo en línea en el escritorio y el modo continuo en dispositivos táctiles. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
