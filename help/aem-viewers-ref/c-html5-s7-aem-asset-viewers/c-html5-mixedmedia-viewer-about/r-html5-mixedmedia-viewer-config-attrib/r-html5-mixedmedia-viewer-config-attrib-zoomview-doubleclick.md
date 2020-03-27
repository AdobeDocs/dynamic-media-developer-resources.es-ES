---
description: nulo
seo-description: nulo
seo-title: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic media
uuid: 2f44dc7f-ebed-4c74-b1ea-0b65655059fe
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

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` en equipos de escritorio; `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
