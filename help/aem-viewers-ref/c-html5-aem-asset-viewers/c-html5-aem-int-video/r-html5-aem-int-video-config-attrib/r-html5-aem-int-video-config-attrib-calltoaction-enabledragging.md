---
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
title: CallToAction.enabledragging
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---


# CallToAction.enabledragging{#calltoaction-enabledragging}

Atributo de configuración para el visualizador de vídeo interactivo.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Activa o desactiva la capacidad de un usuario para desplazarse por las miniaturas con un ratón o mediante gestos táctiles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Está en el rango <span class="codeph"> 0-1 </span> y es un valor porcentual para el movimiento en la dirección incorrecta de la velocidad real. </p> <p>Si se establece en <span class="codeph"> 1 </span> se mueve con el ratón. </p> <p>Si se establece en <span class="codeph"> 0 </span> no le permite moverse en la dirección incorrecta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

