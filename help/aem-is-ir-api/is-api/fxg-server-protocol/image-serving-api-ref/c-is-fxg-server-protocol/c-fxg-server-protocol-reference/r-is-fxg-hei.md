---
title: hei
description: Ver altura. Especifica la altura de la imagen de respuesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---

# hei{#hei}

Ver altura. Especifica la altura de la imagen de respuesta.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Altura de la imagen en píxeles (int mayor que 0). </p></td> 
 </tr> 
</table>

Los formatos de trama se representan con el tamaño de vista predeterminado (o el valor DefaultPix ). Seleccione **[!UICONTROL Configuración de aplicación]** > **[!UICONTROL Configuración de Publish]** > **[!UICONTROL Servidor de imágenes]** y, a continuación, introduzca los valores de anchura y altura. Los tamaños más pequeños proporcionan un mejor rendimiento. Guarde la configuración y realice un Publish de servicio de imágenes para aplicar un cambio.

Si aplica un comando `scale=1`, se procesará una solicitud de formato de trama con el tamaño especificado en el FXG.

## Predeterminado {#section-76ee3daa77cb468ab310821357cc9404}

Si no se especifican `wid=`, `hei=` o `scale=`, la imagen de respuesta es el tamaño de vista predeterminado especificado en el archivo FXG.

## Ejemplo {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

A menos que se especifique un formato, la imagen se procesa como un archivo de SWF. En este caso, el alto y el ancho no tienen significado, ya que el SWF suele ampliarse al tamaño de la ventana del explorador. Como resultado, hei y wid solo se aplican a formatos rasterizados o PDF. Los formatos de trama incluyen:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alpha
* PNG-alpha
