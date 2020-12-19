---
description: Ancho de vista. Especifica el ancho de la imagen de respuesta (imagen de vista).
seo-description: Ancho de vista. Especifica el ancho de la imagen de respuesta (imagen de vista).
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 4%

---


# wid{#wid}

Ancho de vista. Especifica el ancho de la imagen de respuesta (imagen de vista).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Ancho de la imagen en píxeles (int bueno que 0), </p></td> 
 </tr> 
</table>

## Predeterminado {#section-830bae0b6bac440098444d7cdcb23e2e}

Si no se especifica ni `wid=`, `hei=` ni `scale=`, la imagen de respuesta es el tamaño de vista predeterminado especificado en el archivo FXG.

Los formatos de rasterizado se procesan con el Tamaño de Vista predeterminado (o el ajuste DefaultPix). Haga clic en **[!UICONTROL Ajustes de aplicación]** > **[!UICONTROL Ajustes de publicación]** > **[!UICONTROL Servidor de imágenes]** y, a continuación, introduzca los valores de anchura y altura. Los tamaños más pequeños proporcionan un mejor rendimiento. Debe guardar la configuración y realizar una publicación para servicio de imágenes para aplicar un cambio.

Si aplica un comando `scale=1`, se procesa una solicitud de formato rasterizado con el tamaño especificado en FXG.

## Ejemplo {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

A menos que se especifique un formato, la imagen se procesa como archivo SWF. En este caso, la altura y la anchura no tienen significado, ya que el SWF generalmente se expande al tamaño de la ventana del explorador. Como resultado, hei y wid solo se aplican a formatos rasterizados o PDF. Los formatos rasterizados incluyen:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alpha

