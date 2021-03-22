---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
uuid: 8e78d91e-e4c6-40f1-9421-8da8bc404ee0
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de doble clic o toque para girar acciones. Si se establece en <span class="codeph"> ninguno </span> , se deshabilita el giro al hacer doble clic o tocar. Si se establece en <span class="codeph"> zoom </span> al hacer clic en la imagen, se gira un paso de giro; CTRL+clic despliega un paso de giro. Si se establece <span class="codeph"> restablecer </span> hace que un solo clic en la imagen restablezca el giro al nivel de giro inicial. Para <span class="codeph"> zoomReset </span>, se restablece si el factor de giro actual está en el límite especificado o por encima de él; de lo contrario, se aplica giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` en equipos de escritorio;  `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
