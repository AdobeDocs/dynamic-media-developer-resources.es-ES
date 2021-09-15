---
title: Definir indicador
description: El indicador de conjunto es una serie de puntos procesados en la parte inferior del visor. Muestra la posición actual dentro del conjunto.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---

# Definir indicador{#set-indicator}

El indicador de conjunto es una serie de puntos procesados en la parte inferior del visor. Muestra la posición actual dentro del conjunto.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del indicador de conjunto**

El aspecto del contenedor de indicador establecido se controla con el siguiente selector de clase CSS:

```
.s7carouselviewer .s7setindicator
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo en formato hexadecimal del indicador establecido. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El indicador de conjunto admite el selector de atributos de modo, que se puede utilizar para aplicar distintos estilos a los modos de operación numéricos y de puntos. En concreto, `mode="numeric"` corresponde al modo de operación numérico; `mode="dotted"` corresponde al estado de punto predeterminado.

A modo de ejemplo, supongamos que desea configurar un indicador de conjunto con un fondo blanco:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

El aspecto de un punto indicador de conjunto individual se controla con el selector de clase CSS. Se aplica a los elementos tanto en los modos de operación numérica como de puntos.

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del punto indicador definido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del punto indicador definido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p>Margen izquierdo en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p>Margen superior en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right  </span> </p> </td> 
   <td colname="col2"> <p>Margen derecho en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom  </span> </p> </td> 
   <td colname="col2"> <p>Margen inferior en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Radio del borde en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo en formato hexadecimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nombre de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alineación vertical  </span> </p> </td> 
   <td colname="col2"> <p>Alineación vertical del índice del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del texto para el índice del banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Los elementos del indicador de configuración admiten el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a diferentes estados de miniaturas. En concreto, `state="selected"` corresponde al elemento actual del conjunto; `state="unselected"` corresponde al estado del elemento predeterminado.

Por ejemplo, supongamos que desea configurar un indicador de conjunto en modo de puntos para sistemas de escritorio. Desea que se sitúe a 20 píxeles de la parte inferior del visor. Además, desea que los puntos no seleccionados sean negros con un 50% de transparencia, 15 x 15 píxeles con siete esquinas redondeadas de píxeles. Los puntos seleccionados son negros con un 90% de transparencia, 18 x 18 píxeles con nueve píxeles de esquinas redondeadas. El espaciado entre puntos es de cinco píxeles.

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```
