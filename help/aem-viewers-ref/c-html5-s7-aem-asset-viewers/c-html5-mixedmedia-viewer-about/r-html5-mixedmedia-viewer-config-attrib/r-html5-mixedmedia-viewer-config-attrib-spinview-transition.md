---
title: SpinView.transition
description: SpinView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`hora`*[, *`relajación`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tiempo</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos que tarda la animación para una única acción de paso de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> relajación</span></span> </p> </td> 
   <td colname="col2"> <p> Crea una ilusión de aceleración o desaceleración que hace que la transición parezca más natural. Puede establecer la aceleración en una de las siguientes opciones: </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (automático) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (lineal) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (cuadrático) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cúbico) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (cuártico) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quíntico) </li> 
     </ul> </p> <p>El modo automático siempre utiliza una transición lineal cuando el zoom elástico está desactivado (predeterminado). De lo contrario, se ajusta a una de las otras funciones de aceleración en función del tiempo de transición. Es decir, cuanto más corto sea el tiempo de transición, mayor será la función de aceleración utilizada para acelerar el efecto de aceleración o desaceleración. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
