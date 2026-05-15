---
title: hei
description: Ver altura. Especifica la altura de la imagen de respuesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
TQID: 'https://experienceleague.adobe.com/Tpl8zVXQVzs3isa26A3YvnOzs6gqpz3-4L-qDBx-eK0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
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

Los formatos de trama se representan con el tamaño de vista predeterminado (o el valor DefaultPix ). Seleccione **[!UICONTROL Configuración de aplicación]** > **[!UICONTROL Configuración de publicación]** > **[!UICONTROL Servidor de imágenes]** y, a continuación, introduzca los valores de anchura y altura. Los tamaños más pequeños proporcionan un mejor rendimiento. Guarde la configuración y realice una publicación para servicio de imágenes para aplicar un cambio.

Si aplica un comando `scale=1`, se procesará una solicitud de formato de trama con el tamaño especificado en el FXG.

## Predeterminado {#section-76ee3daa77cb468ab310821357cc9404}

Si no se especifican `wid=`, `hei=` o `scale=`, la imagen de respuesta es el tamaño de vista predeterminado especificado en el archivo FXG.

## Ejemplo {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

A menos que se especifique un formato, la imagen se procesará como un archivo SWF. En este caso, la altura y la anchura no tienen significado, ya que SWF suele ampliarse al tamaño de la ventana del explorador. Como resultado, hei y wid solo se aplican a los formatos raster o PDF. Los formatos de trama incluyen:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
