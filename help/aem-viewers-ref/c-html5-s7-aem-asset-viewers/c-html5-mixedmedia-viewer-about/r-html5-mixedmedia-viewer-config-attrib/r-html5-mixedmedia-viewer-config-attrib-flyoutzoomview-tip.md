---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de medios mixtos
role: Developer,Business Practitioner
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 5%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el número de segundos que se muestra el texto de la sugerencia antes de que se oculte. Cuando se establece en <span class="codeph"> -1</span>, el mensaje siempre se muestra, incluso si el usuario activa el menú flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> contar</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el número de veces que se muestra el texto al ver imágenes nuevas en el conjunto. Un valor de <span class="codeph"> -1</span> significa que el texto siempre se muestra cuando se ve una imagen del conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fundido</span></span> </p> </td> 
   <td colname="col2"> Especifica la duración de una animación de fundido que se produce cuando el texto aparece o desaparece. Un valor de <span class="codeph"> 0</span> indica que no hay transición de fundido. </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
