---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0fcc1f5c-a735-430d-be0c-c00ed08830df
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un solo clic o toque para aplicar zoom a las acciones. Establecer en <span class="codeph"> ninguno </span> deshabilita el zoom de un solo clic/toque. Si está configurado como <span class="codeph"> zoom </span> al hacer clic en la imagen, se amplía un paso de zoom; CTRL+clic reduce un paso de zoom. Establecer en <span class="codeph"> reset </span> hace que un solo clic en la imagen restablezca el zoom al nivel de zoom inicial. Para <span class="codeph"> zoomReset </span>, se aplica el restablecimiento si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica el zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` en equipos de escritorio; `none` en dispositivos táctiles.

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
