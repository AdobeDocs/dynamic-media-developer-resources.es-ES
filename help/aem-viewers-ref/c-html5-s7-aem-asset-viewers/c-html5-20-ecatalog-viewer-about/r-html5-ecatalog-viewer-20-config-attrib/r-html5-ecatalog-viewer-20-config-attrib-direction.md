---
description: dirección
solution: Experience Manager
title: dirección
topic: Dynamic media
uuid: 185824c5-d6f2-4e1b-99ac-726a295ec5f4
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 3%

---


# dirección{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>Especifica la forma en que se muestran las páginas en la vista principal y en las miniaturas. También especifica la forma en que el usuario interactúa con la interfaz de usuario del visor para cambiar entre marcos de catálogo. </p> <p>Cuando se utiliza <span class="codeph"> izquierda </span>, se establece una alineación derecha para la página inicial y la alineación izquierda para la última página. Supone subimágenes de página individuales para el orden de procesamiento de izquierda a derecha. También establece la vista principal para utilizar la animación de diapositivas de derecha a izquierda para avanzar en el catálogo (en caso de que <span class="codeph"> PageView.frametransition </span> esté configurada en slide). Por último, las miniaturas se definen para un orden de relleno de izquierda a derecha. </p> <p>De manera similar, cuando se utiliza <span class="codeph"> derecha </span> se establece una alineación a la izquierda para la página inicial y a la derecha para la última página. Supone subimágenes de página individuales para el orden de procesamiento de derecha a izquierda. También establece la vista principal para utilizar la animación de diapositivas de izquierda a derecha para avanzar en el catálogo (en caso de que la <span class="codeph"> PageView.frametransicion </span> esté configurada en slide). Finalmente, invierte el orden de las miniaturas para que la vista de las miniaturas se rellene en dirección de derecha a izquierda y de arriba abajo. </p> <p>Cuando <span class="codeph"> auto </span> está establecido, el visor aplica el modo <span class="codeph"> derecho </span> cuando la configuración regional está configurada en <span class="codeph"> ja; </span>de lo contrario, utiliza el modo <span class="codeph"> izquierdo </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-a66ce10d6c0b449883f654e7e0657e2c}

Opcional.

## Predeterminado {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Ejemplo {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
