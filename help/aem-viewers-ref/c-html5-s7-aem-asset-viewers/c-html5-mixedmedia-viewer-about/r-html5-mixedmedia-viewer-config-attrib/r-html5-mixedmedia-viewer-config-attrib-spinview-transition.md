---
description: nulo
seo-description: nulo
seo-title: SpinView.transición
solution: Experience Manager
title: SpinView.transición
topic: Dynamic media
uuid: d5cc319a-fb0b-41d3-a118-f00376a127e4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.transición{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`aceleración de tiempo`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tiempo</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos que dura la animación de una sola acción de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> flexibilización</span></span> </p> </td> 
   <td colname="col2"> <p> Crea una ilusión de aceleración o deceleración que hace que la transición parezca más natural. Puede definir la aceleración en una de las siguientes opciones: </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (automático) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (lineal) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (cuadrático) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cúbico) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (en cuarto) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quintic) </li> 
     </ul> </p> <p>El modo automático siempre utiliza transición lineal cuando el zoom elástico está desactivado (predeterminado). De lo contrario, se ajusta a una de las demás funciones de aceleración en función del tiempo de transición. Es decir, cuanto más corto sea el tiempo de transición, más alta será la función de aceleración que se utilizará para acelerar el efecto de aceleración o desaceleración. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
