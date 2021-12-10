---
title: PageView.doubleclick
description: PageView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de doble clic/toque para aplicar zoom a las acciones. Establecer en <span class="codeph"> ninguno </span> deshabilita el zoom de doble clic/toque. Si está configurado como <span class="codeph"> zoom </span> al hacer clic en la imagen, se amplía un paso de zoom; CTRL+clic reduce un paso de zoom. Establecer en <span class="codeph"> reset </span> hace que un solo clic en la imagen restablezca el zoom al nivel de zoom inicial. Para <span class="codeph"> zoomReset </span>, se aplica el restablecimiento si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica el zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Opcional.

## Predeterminado {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` en equipos de escritorio; `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
