---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 4%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numérico|punteado</span> </p> </td> 
   <td colname="col2"> <p> Configura el estilo de representación del indicador determinado. </p> <p>Cuando se establece en <span class="codeph"> </span> punteado, el componente procesa indicadores idénticos para todas las páginas. </p> <p>Cuando se establece en <span class="codeph"> numeric</span>, coloca un número de página basado en 1 dentro de cada elemento indicador. </p> <p>El modo de operación <span class="codeph"> numeric</span> no es compatible con dispositivos con entrada táctil. En su lugar, el componente utiliza <span class="codeph"> dotted</span> en dichos dispositivos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
