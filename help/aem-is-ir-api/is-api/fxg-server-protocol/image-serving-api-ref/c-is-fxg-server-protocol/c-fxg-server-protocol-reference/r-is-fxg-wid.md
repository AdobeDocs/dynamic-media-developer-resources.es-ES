---
description: Ver anchura. Especifica el ancho de la imagen de respuesta (ver imagen).
seo-description: Ver anchura. Especifica el ancho de la imagen de respuesta (ver imagen).
seo-title: wid
solution: Experience Manager
title: wid
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 4%

---


# wid{#wid}

Ver anchura. Especifica el ancho de la imagen de respuesta (ver imagen).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Anchura de la imagen en píxeles (int bueno a 0), </p></td> 
 </tr> 
</table>

## Predeterminado {#section-830bae0b6bac440098444d7cdcb23e2e}

Si no se especifica `wid=`, `hei=` ni `scale=`, la imagen de respuesta es el tamaño de vista predeterminado especificado en el archivo FXG.

Los formatos de rasterizado se representan con el tamaño de vista predeterminado (o con la configuración DefaultPix). Haga clic en **[!UICONTROL Ajustes de aplicación]** > **[!UICONTROL Ajustes de publicación]** > **[!UICONTROL Servidor de imágenes]** y, a continuación, introduzca los valores de anchura y altura. Los tamaños más pequeños proporcionan un mejor rendimiento. Debe guardar la configuración y realizar una publicación de servicio de imágenes para aplicar un cambio.

Si aplica un comando `scale=1`, se procesa una solicitud de formato de trama con el tamaño especificado en el FXG.

## Ejemplo {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

A menos que se especifique un formato, la imagen se representa como un archivo SWF. En este caso, la altura y la anchura no tienen significado, ya que el SWF normalmente se expande al tamaño de la ventana del explorador. Como resultado, hei y wid solo se aplican a formatos raster o PDF. Los formatos de rasterizado incluyen:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa

