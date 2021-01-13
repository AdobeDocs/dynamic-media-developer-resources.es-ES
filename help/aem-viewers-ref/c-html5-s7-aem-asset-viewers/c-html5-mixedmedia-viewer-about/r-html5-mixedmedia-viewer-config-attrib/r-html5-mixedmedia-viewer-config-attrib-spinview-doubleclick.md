---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: 8e78d91e-e4c6-40f1-9421-8da8bc404ee0
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de clics/toques de doble para girar acciones. Si se establece en <span class="codeph"> ninguno </span> se deshabilita la opción de tocar o hacer clic en el doble. Si se establece en <span class="codeph"> zoom </span> al hacer clic en la imagen, se gira un paso de giro; CTRL+clic desplaza un paso de giro. Si se establece en <span class="codeph"> reset </span>, se hace un solo clic en la imagen para restablecer el giro al nivel de giro inicial. Para <span class="codeph"> zoomReset </span>, el restablecimiento se aplica si el factor de giro actual está en el límite especificado o por encima de él; de lo contrario, se aplica el giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` en equipos de escritorio;  `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
