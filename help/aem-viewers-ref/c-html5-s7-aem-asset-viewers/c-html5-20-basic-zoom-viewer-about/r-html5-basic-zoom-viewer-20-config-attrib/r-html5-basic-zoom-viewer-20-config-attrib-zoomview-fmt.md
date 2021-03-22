---
description: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
uuid: b118e441-f128-4dfd-a82e-62ec4d1ebf84
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---


# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica el formato de imagen que utiliza el componente para cargar imágenes desde el servidor de imágenes. Si el formato especificado termina con "-alpha", el componente procesa las imágenes como contenido transparente. Para el resto de formatos de imagen, el componente trata las imágenes como opacas. El componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para que sea transparente, establezca la propiedad CSS de color de fondo en transparente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Predeterminado {#section-7564169749ff4a4996049ea1148cb2a5}

`jpeg`

## Ejemplo {#section-96e69b70365f461dae4399e49044ea2f}

`fmt=png-alpha`
