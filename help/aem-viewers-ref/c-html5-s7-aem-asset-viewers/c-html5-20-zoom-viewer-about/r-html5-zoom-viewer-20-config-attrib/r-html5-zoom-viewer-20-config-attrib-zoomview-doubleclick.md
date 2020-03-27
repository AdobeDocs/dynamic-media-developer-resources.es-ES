---
description: nulo
seo-description: nulo
seo-title: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic media
uuid: 8dabc31c-ec7e-4dc0-b528-4f3f43f46721
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de doble al hacer clic o tocar para aplicar zoom a las acciones. Si se establece en <span class="codeph"> none, </span> se deshabilita el zoom de toque o clic en el doble. Si se configura para <span class="codeph"> aplicar zoom al </span> hacer clic en la imagen, se amplía un paso de zoom; CTRL+clic reduce un paso de zoom. La configuración para <span class="codeph"> restablecer </span> hace que un solo clic en la imagen restablezca el nivel de zoom inicial. Para <span class="codeph"> zoomReset </span>, el restablecimiento se aplica si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica el zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`reset` en equipos de escritorio; `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
