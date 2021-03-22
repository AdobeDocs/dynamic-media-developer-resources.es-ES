---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flotante
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Controla el aspecto del resaltado de la vista principal cuando el flotante está activo. Cuando se establece en <span class="codeph"> 0</span>, el área visible actualmente en la ventana flotante se resalta mediante estilos proporcionados por <span class="codeph"> .s7highlight</span> o <span class="codeph"> .s7cursor</span> nombres de clase CSS (según el valor del modificador <span class="codeph"> highlightMode</span>). Cuando se establece en <span class="codeph"> 1</span> el componente entra en modo "inverso" donde el área visualizada actualmente es completamente transparente (en caso de que <span class="codeph"> modo resaltado</span> esté configurado en <span class="codeph"> resaltado</span>) o tenga estilo con <span class="codeph"> .s7cursor</span> nombre de clase CSS (en caso de que se establezca <span class="codeph"> modo resaltado</span> a <span class="codeph"> cursor</span>), pero el área circundante se rellena con estilos proporcionados por <span class="codeph"> .s7overlay</span> nombre de clase CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
