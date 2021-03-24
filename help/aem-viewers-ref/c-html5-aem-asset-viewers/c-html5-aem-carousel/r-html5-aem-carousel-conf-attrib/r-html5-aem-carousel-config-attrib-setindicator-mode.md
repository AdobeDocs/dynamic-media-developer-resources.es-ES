---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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
