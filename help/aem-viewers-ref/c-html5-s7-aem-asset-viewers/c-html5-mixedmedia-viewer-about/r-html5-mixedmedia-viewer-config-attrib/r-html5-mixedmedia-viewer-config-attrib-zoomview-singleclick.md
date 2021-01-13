---
description: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic media
uuid: 3e57e235-7888-4ba2-9c8e-4f568a6caa52
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un solo clic o toque para aplicar zoom a las acciones. Si se establece en <span class="codeph"> ninguno </span> se deshabilita el zoom de un solo clic o toque. Si se establece en <span class="codeph"> zoom </span> al hacer clic en la imagen se amplía un paso de zoom; CTRL+clic reduce un paso de zoom. Si se establece en <span class="codeph"> reset </span>, se hace un solo clic en la imagen para restablecer el zoom al nivel de zoom inicial. Para <span class="codeph"> zoomReset </span>, el restablecimiento se aplica si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica el zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` en equipos de escritorio;  `none` en dispositivos táctiles.

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
