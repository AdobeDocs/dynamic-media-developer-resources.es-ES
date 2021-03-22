---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
uuid: cfb549c2-e0cf-46c3-b5b7-219c8c1bee94
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 5%

---


# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|dotted</span> </p> </td> 
   <td colname="col2"> <p> Configura el estilo de renderización del indicador definido. </p> <p>Cuando se establece en <span class="codeph"> dotted</span> , el componente procesa indicadores idénticos para todas las páginas. </p> <p>Cuando se establece en <span class="codeph"> numérico</span>, coloca un número de página basado en 1 dentro de cada elemento indicador. </p> <p>El modo de operación <span class="codeph"> numérico</span> no es compatible con los dispositivos que pueden introducir datos táctiles. En su lugar, el componente utiliza <span class="codeph"> puntos</span> en dichos dispositivos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
