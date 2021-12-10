---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9f52542e-398c-45a2-89ea-95c9aefbde3e
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de doble clic/toque para aplicar zoom a las acciones. Establecer en <span class="codeph"> ninguno </span> deshabilita el zoom de doble clic/toque. Si está configurado como <span class="codeph"> zoom </span> al hacer clic en la imagen, se amplía un paso de zoom; CTRL+clic reduce un paso de zoom. Establecer en <span class="codeph"> reset </span> hace que un solo clic en la imagen restablezca el zoom al nivel de zoom inicial. Para <span class="codeph"> zoomReset </span>, se aplica el restablecimiento si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica el zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`reset` - En equipos de escritorio; `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
