---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 2%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Controla la apariencia del resalte de la vista principal cuando el menú flotante está activo. Cuando se establece en <span class="codeph"> 0</span>, el área visible actualmente en la ventana flotante se resalta con los estilos proporcionados por <span class="codeph"> .s7highlight</span> o por <span class="codeph"> .s7cursor</span> nombres de clase CSS (según el valor del modificador <span class="codeph"> highlightmode</span>). Cuando se establece en <span class="codeph">, el componente 1</span> entra en modo "inverso" donde el área visualizada actualmente es totalmente transparente (en el caso de que <span class="codeph"> highlightmode</span> se establezca en <span class="codeph"> highlight</span>) o está diseñado con <span class="codeph"> .s7cursor</span> nombre de clase CSS (en el caso de que <span class="codeph"> highlightmode</span> se establezca en <span class="codeph"> cursor</span>), pero el área adyacente se rellena con los estilos proporcionados por <span class="codeph"> .s7overlay</span> nombre de clase CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
