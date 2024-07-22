---
title: dirección
description: Especifica la forma en que se muestran las páginas en la vista principal y en las miniaturas. También especifica la forma en que el usuario interactúa con la interfaz de usuario del visor para cambiar entre marcos del catálogo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7d3df37-3e8b-438f-8b24-035b6982dc14
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 2%

---

# dirección{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|izquierda|derecha </span> </p> </td> 
   <td colname="col2"> <p>Especifica la forma en que se muestran las páginas en la vista principal y en las miniaturas. También especifica la forma en que el usuario interactúa con la interfaz de usuario del visor para cambiar entre marcos del catálogo. </p> <p>Cuando se usa <span class="codeph"> left </span>, establece una alineación a la derecha para la página inicial y a la izquierda para la última página. Vincula subimágenes de página individuales para el orden de procesamiento de izquierda a derecha. También establece la vista principal para utilizar la animación de diapositiva de derecha a izquierda para avanzar el catálogo (en el caso de que <span class="codeph"> PageView.frametransition </span> esté establecida en slide). Por último, las miniaturas se establecen para un orden de relleno de izquierda a derecha. </p> <p>Del mismo modo, cuando se utiliza <span class="codeph"> right </span>, establece una alineación izquierda para la página inicial y una alineación derecha para la última página. Vincula subimágenes de página individuales para el orden de procesamiento de derecha a izquierda. También establece la vista principal para utilizar la animación de diapositiva de izquierda a derecha para avanzar el catálogo (en el caso de que <span class="codeph"> PageView.frametransition </span> esté establecida en slide). Por último, invierte el orden de las miniaturas para que se rellenen en la dirección de derecha a izquierda, de arriba a abajo. </p> <p>Cuando se establece <span class="codeph"> auto </span>, el visor aplica el modo <span class="codeph"> right </span> cuando locale se establece en <span class="codeph"> ja; </span>de lo contrario, utiliza el modo <span class="codeph"> left </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-a66ce10d6c0b449883f654e7e0657e2c}

Opcional.

## Predeterminado {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Ejemplo {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
