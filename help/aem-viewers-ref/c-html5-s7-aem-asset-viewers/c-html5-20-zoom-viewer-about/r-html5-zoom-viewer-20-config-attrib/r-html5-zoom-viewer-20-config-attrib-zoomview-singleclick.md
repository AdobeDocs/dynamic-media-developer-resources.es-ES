---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación del clic/toque en acciones de zoom. Estableciendo en <span class="codeph"> ninguno </span> desactiva el zoom de un solo clic/toque. Si se establece en <span class="codeph"> zoom </span> al hacer clic en la imagen, se amplía un paso de zoom; CTRL y clic reduce un paso de zoom. Estableciendo en <span class="codeph"> restablecer </span> hace que un solo clic en la imagen restablezca el zoom al nivel inicial. Para <span class="codeph"> zoomReset </span>, se aplica reset si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`zoomReset` - En equipos de escritorio; `none` en dispositivos táctiles.

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
