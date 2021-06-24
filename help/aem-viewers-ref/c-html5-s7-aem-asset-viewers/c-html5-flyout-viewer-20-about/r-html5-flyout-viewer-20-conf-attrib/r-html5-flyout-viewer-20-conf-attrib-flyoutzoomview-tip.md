---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flotante
role: Developer,Business Practitioner
exl-id: 122c6406-6fd7-4e45-bff2-11022a3f2cf7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica el número de segundos que se muestra el texto de la sugerencia antes de que se oculte. Cuando se establece en <span class="codeph"> -1</span>, el mensaje siempre se muestra, incluso si el usuario activa el menú flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica el número de veces que se muestra el texto al ver imágenes nuevas en el conjunto. Un valor de <span class="codeph"> -1</span> significa que el texto siempre se muestra cuando se ve una imagen del conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fundido</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración de una animación de fundido que se produce cuando el texto aparece o desaparece. Un valor de <span class="codeph"> 0</span> significa que no hay transición de fundido. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
