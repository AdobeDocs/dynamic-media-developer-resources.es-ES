---
description: nulo
seo-description: nulo
seo-title: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
topic: Dynamic media
uuid: b08b605e-5ffc-42cc-931d-d67750a8dca8
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un solo clic o toque para aplicar zoom a las acciones. Si se establece en <span class="codeph"> none, </span> se deshabilita el zoom de un solo clic o toque. Si se configura para <span class="codeph"> aplicar zoom al </span> hacer clic en la imagen, se amplía un paso de zoom; CTRL+clic reduce un paso de zoom. La configuración para <span class="codeph"> restablecer </span> hace que un solo clic en la imagen restablezca el nivel de zoom inicial. Para <span class="codeph"> zoomReset </span>, el restablecimiento se aplica si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica el zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-edcfcd6c0bd24ac093442c56450b3c97}

Opcional.

## Predeterminado {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] en equipos de escritorio; [!DNL `none`] en dispositivos táctiles.

## Ejemplo {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]