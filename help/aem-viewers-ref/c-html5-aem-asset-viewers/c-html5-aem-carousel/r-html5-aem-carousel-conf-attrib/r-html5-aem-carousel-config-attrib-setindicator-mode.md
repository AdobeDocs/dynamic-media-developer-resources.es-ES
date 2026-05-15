---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
TQID: 'https://experienceleague.adobe.com/lss5EqVS8ggpyoDlnGlcagfln977-Hw4fcchN5LMGt4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
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
