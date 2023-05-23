---
description: Ver altura. Especifica la altura de la imagen de respuesta.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 4%

---

# hei{#hei}

Ver altura. Especifica la altura de la imagen de respuesta.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Alto de la imagen en píxeles (int bueno que 0). </p></td> 
 </tr> 
</table>

Los formatos de trama se representan con el tamaño de vista predeterminado (o el valor DefaultPix ). Clic **[!UICONTROL Ajustes de aplicación]** > **[!UICONTROL Ajustes de publicación]** > **[!UICONTROL Servidor de imágenes]** y, a continuación, introduzca los valores de anchura y altura. Los tamaños más pequeños proporcionan un mejor rendimiento. Debe guardar la configuración y realizar una publicación para servicio de imágenes para aplicar un cambio.

Si aplica una `scale=1` , se procesa una solicitud de formato rasterizado con el tamaño especificado en el FXG.

## Predeterminado {#section-76ee3daa77cb468ab310821357cc9404}

Si ninguno `wid=`, `hei=`, ni `scale=` Si se especifican, la imagen de respuesta es el tamaño de vista predeterminado especificado en el archivo FXG.

## Ejemplo {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

A menos que se especifique un formato, la imagen se procesa como un archivo de SWF. En este caso, el alto y el ancho no tienen significado, ya que el SWF suele ampliarse al tamaño de la ventana del explorador. Como resultado, hei y wid solo se aplican a formatos rasterizados o PDF. Los formatos de trama incluyen:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alpha
* PNG-alpha
