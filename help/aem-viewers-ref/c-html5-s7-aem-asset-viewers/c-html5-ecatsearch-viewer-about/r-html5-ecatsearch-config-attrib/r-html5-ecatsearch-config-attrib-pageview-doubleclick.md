---
description: nulo
seo-description: nulo
seo-title: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
topic: Dynamic media
uuid: c62302b0-d034-49d4-b5a8-1a77a46fe889
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

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

[!DNL `reset`] en equipos de escritorio; [!DNL `zoomReset`] en dispositivos táctiles.

## Ejemplo {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
