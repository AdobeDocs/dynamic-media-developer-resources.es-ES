---
description: nulo
seo-description: nulo
seo-title: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
topic: Dynamic media
uuid: ac4fb532-f554-4831-b341-7f8d6ef3a1c0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de doble al hacer clic o tocar para aplicar zoom a las acciones. Si se establece en <span class="codeph"> none, </span> se deshabilita el zoom de toque o clic en el doble. Si se configura para <span class="codeph"> aplicar zoom al </span> hacer clic en la imagen, se amplía un paso de zoom; CTRL+clic reduce un paso de zoom. La configuración para <span class="codeph"> restablecer </span> hace que un solo clic en la imagen restablezca el nivel de zoom inicial. Para <span class="codeph"> zoomReset </span>, el restablecimiento se aplica si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica el zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Opcional.

## Predeterminado {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` en equipos de escritorio; `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
