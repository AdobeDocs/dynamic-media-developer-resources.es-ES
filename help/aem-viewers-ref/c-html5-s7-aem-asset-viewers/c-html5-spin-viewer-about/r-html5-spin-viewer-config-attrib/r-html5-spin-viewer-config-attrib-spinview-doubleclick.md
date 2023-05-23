---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación del doble clic/toque para las acciones de giro. Estableciendo en <span class="codeph"> ninguno </span> deshabilita los giros de doble clic o toque. Si se establece en <span class="codeph"> zoom </span>, al hacer clic en la imagen, se gira en un paso de giro; CTRL y clic gira un paso de giro. Estableciendo en <span class="codeph"> restablecer </span> hace que un solo clic en la imagen restablezca el giro al nivel inicial. Para <span class="codeph"> zoomReset </span>, se aplica reset si el factor de giro actual está en el límite especificado o por encima de él; de lo contrario, se aplica spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`reset` en equipos de escritorio; `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
