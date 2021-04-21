---
description: dirección
solution: Experience Manager
title: dirección
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---


# dirección{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>Especifica la forma en que se muestran las páginas en la vista principal y en las miniaturas. También especifica la forma en que el usuario interactúa con la interfaz de usuario del visor para cambiar entre marcos de catálogo. </p> <p>Cuando se utiliza <span class="codeph"> izquierda </span>, se establece una alineación derecha para la página inicial y la alineación izquierda para la última página. Vincula subimágenes de página individuales para el orden de procesamiento de izquierda a derecha. También establece la vista principal para utilizar la animación de diapositivas de derecha a izquierda para avanzar en el catálogo (en caso de que <span class="codeph"> PageView.frametransition </span> esté configurada como diapositiva). Por último, las miniaturas se establecen para un orden de relleno de izquierda a derecha. </p> <p>Del mismo modo, cuando se utiliza <span class="codeph"> derecha </span>, se establece una alineación a la izquierda para la página inicial y a la derecha para la última página. Vincula subimágenes de página individuales para el orden de procesamiento de derecha a izquierda. También establece la vista principal para utilizar la animación de diapositivas de izquierda a derecha para avanzar en el catálogo (en caso de que <span class="codeph"> PageView.frametransition </span> esté configurada como diapositiva). Por último, invierte el orden de las miniaturas para que la vista de miniaturas se rellene en dirección derecha a izquierda, de arriba a abajo. </p> <p>Cuando se establece <span class="codeph"> auto </span>, el visor aplica el modo <span class="codeph"> derecho </span> cuando la configuración regional se establece en <span class="codeph"> ja; </span>de lo contrario, utiliza el modo <span class="codeph"> izquierdo </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-a66ce10d6c0b449883f654e7e0657e2c}

Opcional.

## Predeterminado {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Ejemplo {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
