---
description: dirección
solution: Experience Manager
title: dirección
uuid: 0a30f3b0-64c8-4799-b4f5-fc8996a8b5a4
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---


# dirección{#direction}

[!DNL `direction=auto|left|right`]

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

[!DNL `auto`]

## Ejemplo {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
