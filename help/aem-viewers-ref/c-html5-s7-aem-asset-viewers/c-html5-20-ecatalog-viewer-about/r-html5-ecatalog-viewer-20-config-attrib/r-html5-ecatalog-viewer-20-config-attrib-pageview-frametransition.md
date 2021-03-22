---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
uuid: feeb02c0-f3f9-4559-acd9-cad30788b70b
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%

---


# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duración`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva|giro|auto</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto que se aplica al cambiar de marco. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> </span> slideactiva una transición en la que el marco antiguo se desliza de la vista y el nuevo marco se desliza para verse. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> </span> activar activa un efecto de voltear página, cuando un usuario puede arrastrar una de las cuatro esquinas de pliego y realizar un giro de página interactivo. </p> <p>Cuando se utiliza <span class="codeph"> girar</span>, el aspecto del componente se controla con el modificador <span class="codeph"> pageturnstyle</span> y se ignora la clase <span class="codeph"> .s7pagedivider</span> CSS. </p> <p>Nota:  <p><span class="codeph"> </span> Motorola Xoom no admite turnanims. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> </span> establece automáticamente la transición del fotograma de giro en los sistemas de escritorio y la transición de diapositivas en dispositivos táctiles. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración en segundos de un efecto de transición <span class="codeph"> diapositiva</span> o <span class="codeph"> giro</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-4d25a3f483834d2b9586fa70270ce6bd}

Opcional.

## Predeterminado {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Ejemplo {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
