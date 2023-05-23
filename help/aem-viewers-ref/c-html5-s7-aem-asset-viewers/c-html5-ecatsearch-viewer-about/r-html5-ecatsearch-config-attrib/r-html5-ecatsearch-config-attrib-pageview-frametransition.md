---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duración`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva|convertir|auto</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto aplicado al cambio de fotograma. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> diapositiva</span> activa una transición en la que el fotograma antiguo se desliza fuera de la vista y el nuevo se desliza hacia la vista. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> dar vuelta</span> activa un efecto de salto de página, cuando un usuario puede arrastrar una de las cuatro esquinas del pliego y realizar un giro de página interactivo. </p> <p>Cuándo <span class="codeph"> dar vuelta</span> se utiliza cuando el aspecto del componente se controla con la variable <span class="codeph"> pageturnstyle</span> y el modificador <span class="codeph"> .s7pagedivider</span> Se omite la clase CSS. </p> <p>Nota:  <p><span class="codeph"> dar vuelta</span> Motorola Xoom no admite la animación de. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> establece la transición de fotogramas de giro en sistemas de escritorio y la transición de diapositivas en dispositivos táctiles. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración en segundos de una <span class="codeph"> diapositiva</span> o <span class="codeph"> dar vuelta</span> efecto de transición. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-4d25a3f483834d2b9586fa70270ce6bd}

Opcional.

## Predeterminado {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Ejemplo {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
