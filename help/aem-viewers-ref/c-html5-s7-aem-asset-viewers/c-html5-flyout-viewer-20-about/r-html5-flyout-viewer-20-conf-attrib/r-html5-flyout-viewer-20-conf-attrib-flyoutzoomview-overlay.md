---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Controla el aspecto del resaltado de la vista principal cuando el flotante está activo. Cuando se establece en <span class="codeph"> 0</span>, el área visible actualmente en la ventana flotante se resalta mediante estilos proporcionados por <span class="codeph">.s7highlight</span> o <span class="codeph"> .s7cursor</span> nombres de clase CSS (según el valor del modificador <span class="codeph"> resaltmode</span>). Cuando se establece en <span class="codeph"> 1</span> el componente entra en modo "inverso" donde el área visualizada actualmente es totalmente transparente (en caso de que <span class="codeph"> modo resaltado</span> se establezca en <span class="codeph"> resaltado</span>) o se le aplique un estilo con <span class="codeph"> .s7cursor</span> nombre de clase CSS (en caso de que <span class="codeph"> modo resaltado</span> esté establecido) en <span class="codeph"> cursor</span>), pero el área circundante se rellena con estilos proporcionados por <span class="codeph"> .s7overlay</span> nombre de clase CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
