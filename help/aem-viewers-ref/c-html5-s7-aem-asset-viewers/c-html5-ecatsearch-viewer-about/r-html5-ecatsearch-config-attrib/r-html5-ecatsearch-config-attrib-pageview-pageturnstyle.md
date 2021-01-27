---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
topic: Dynamic Media
uuid: 748adb73-bfb6-4fce-aa6a-4216184edabb
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWiddividerColordividerOpacityborderOnOffborderColorfillColor`*`]

Controla el aspecto del componente cuando un [!DNL `PageView.frametransition`] se establece en [!DNL `turn`] o en [!DNL `auto`] en sistemas de escritorio.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> Ancho en píxeles de la sombra del divisor de página que separa las páginas izquierda y derecha del pliego. También controla la anchura de la sombra que se muestra al lado de la página que gira. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> Color de sombra en formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>La opacidad de sombra en el rango de <span class="codeph"> 0</span> a <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> El indicador (ya sea <span class="codeph"> 0</span> o <span class="codeph"> 1</span>) que activa y desactiva el borde alrededor de la página de activación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> Color del borde en formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> Color del relleno sólido del área del componente utilizada durante la animación de giro de página, en formato RRGGBB. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-54c634116cfe4f17813318e07539264c}

Opcional.

## Predeterminado {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## Ejemplos {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
