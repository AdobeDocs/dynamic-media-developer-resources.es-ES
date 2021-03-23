---
description: Ver altura. Especifica el alto de la imagen de respuesta.
seo-description: Ver altura. Especifica el alto de la imagen de respuesta.
seo-title: hei
solution: Experience Manager
title: hei
uuid: 6f7e580b-6399-4661-b5d9-8044574ba124
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 4%

---


# hei{#hei}

Ver altura. Especifica el alto de la imagen de respuesta.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Altura de la imagen en píxeles (int bueno a 0). </p></td> 
 </tr> 
</table>

Los formatos de rasterizado se representan con el tamaño de vista predeterminado (o con la configuración DefaultPix). Haga clic en **[!UICONTROL Ajustes de aplicación]** > **[!UICONTROL Ajustes de publicación]** > **[!UICONTROL Servidor de imágenes]** y, a continuación, introduzca los valores de anchura y altura. Los tamaños más pequeños proporcionan un mejor rendimiento. Debe guardar la configuración y realizar una publicación de servicio de imágenes para aplicar un cambio.

Si aplica un comando `scale=1`, se procesa una solicitud de formato de trama con el tamaño especificado en el FXG.

## Predeterminado {#section-76ee3daa77cb468ab310821357cc9404}

Si no se especifica `wid=`, `hei=` ni `scale=`, la imagen de respuesta es el tamaño de vista predeterminado especificado en el archivo FXG.

## Ejemplo {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

A menos que se especifique un formato, la imagen se representa como un archivo SWF. En este caso, la altura y la anchura no tienen significado, ya que el SWF normalmente se expande al tamaño de la ventana del explorador. Como resultado, hei y wid solo se aplican a formatos raster o PDF. Los formatos de rasterizado incluyen:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa

