---
title: PageView.singleclick
description: PageView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un solo clic o toque para aplicar zoom a las acciones. Establecer en <span class="codeph"> ninguno </span> deshabilita el zoom de un solo clic/toque. Si está configurado como <span class="codeph"> zoom </span> al hacer clic en la imagen, se amplía un paso de zoom; CTRL+clic reduce un paso de zoom. Establecer en <span class="codeph"> reset </span> hace que un solo clic en la imagen restablezca el zoom al nivel de zoom inicial. Para <span class="codeph"> zoomReset </span>, se aplica el restablecimiento si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica el zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-edcfcd6c0bd24ac093442c56450b3c97}

Opcional.

## Predeterminado {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` en equipos de escritorio; `none` en dispositivos táctiles.

## Ejemplo {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
