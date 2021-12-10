---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '126'
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
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> diapositiva</span> activa una transición en la que el marco antiguo se desliza fuera de la vista y el nuevo marco se desliza para verse. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> Turn</span> activa un efecto de voltear página, cuando un usuario puede arrastrar una de las cuatro esquinas de pliego y realizar un cambio de página interactivo. </p> <p>When <span class="codeph"> Turn</span> se utiliza el aspecto del componente se controla con la variable <span class="codeph"> pageturnstyle</span> y <span class="codeph"> .s7pagedivider</span> Se ignora la clase CSS. </p> <p>Nota:  <p><span class="codeph"> Turn</span> la animación no es compatible con Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> establece la transición del fotograma de giro en los sistemas de escritorio y la transición de diapositiva en los dispositivos táctiles. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración en segundos de un <span class="codeph"> diapositiva</span> o <span class="codeph"> Turn</span> efecto de transición. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-4d25a3f483834d2b9586fa70270ce6bd}

Opcional.

## Predeterminado {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Ejemplo {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
