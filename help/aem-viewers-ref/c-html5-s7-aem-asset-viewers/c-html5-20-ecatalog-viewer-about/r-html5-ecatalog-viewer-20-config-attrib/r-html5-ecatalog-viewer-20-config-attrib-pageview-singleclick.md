---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
topic: Dynamic media
uuid: 608700d2-5be4-4b96-b026-b12a3ade68ee
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un solo clic o toque para aplicar zoom a las acciones. Si se establece en <span class="codeph"> ninguno </span> se deshabilita el zoom de un solo clic o toque. Si se establece en <span class="codeph"> zoom </span> al hacer clic en la imagen se amplía un paso de zoom; CTRL+clic reduce un paso de zoom. Si se establece en <span class="codeph"> reset </span>, se hace un solo clic en la imagen para restablecer el zoom al nivel de zoom inicial. Para <span class="codeph"> zoomReset </span>, el restablecimiento se aplica si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica el zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-edcfcd6c0bd24ac093442c56450b3c97}

Opcional.

## Predeterminado {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` en equipos de escritorio;  `none` en dispositivos táctiles.

## Ejemplo {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
