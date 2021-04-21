---
description: SetIndicator.autohide
solution: Experience Manager
title: SetIndicator.autohide
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 5%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`límite`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> límite</span>]</span> </p> </td> 
   <td colname="col2"> <p> Configura el comportamiento de ocultación automática según el número de páginas y el tamaño del componente en tiempo de ejecución. </p> <p> <span class="codeph"> 0</span> desactiva el ocultamiento automático. </p> <p> <span class="codeph"> 1</span> habilita la ocultación automática. El componente oculta sus puntos si al menos una de las siguientes condiciones se vuelve verdadera: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">la fila con puntos es más ancha que el ancho del componente en tiempo de ejecución, o </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">el número de páginas establecidas para este componente supera el límite configurado por el parámetro <span class="codeph"><span class="varname"> limit</span></span>. </li> 
     </ul> </p> <p> Al establecer <span class="codeph"><span class="varname"> limit</span></span> en <span class="codeph"> -1</span> se deshabilita la segunda condición de ocultación automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
