---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación del doble clic/toque para las acciones de giro. Estableciendo en <span class="codeph"> ninguno </span> deshabilita los giros de doble clic o toque. Si se establece en <span class="codeph"> zoom </span>, al hacer clic en la imagen, se gira en un paso de giro; CTRL y clic gira un paso de giro. Estableciendo en <span class="codeph"> restablecer </span> hace que un solo clic en la imagen restablezca el giro al nivel inicial. Para <span class="codeph"> zoomReset </span>, se aplica reset si el factor de giro actual está en el límite especificado o por encima de él; de lo contrario, se aplica spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` En equipos de escritorio; `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
