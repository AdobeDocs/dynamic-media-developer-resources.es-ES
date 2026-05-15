---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
TQID: 'https://experienceleague.adobe.com/Pnrb2IBaQgvQL2acyGn7eJuCy1ko0ok42azq9b2y50w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`duration`*[, *`count`*][, *`fade`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el número de segundos que el texto de sugerencia se muestra antes de ocultarse. Cuando se establece en <span class="codeph"> -1</span>, el mensaje siempre se muestra, aunque el usuario active el menú flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> recuento</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el número de veces que se muestra el texto al ver nuevas imágenes del conjunto. Un valor de <span class="codeph"> -1</span> significa que el texto siempre se muestra al ver cualquier imagen del conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fundido</span></span> </p> </td> 
   <td colname="col2"> Especifica la duración de una animación de transición que se produce cuando el texto aparece o desaparece. Un valor de <span class="codeph"> 0</span> indica que no hay transición de transición. </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
