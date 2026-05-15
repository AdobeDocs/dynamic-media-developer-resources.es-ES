---
title: enredar
description: Ver anchura. Especifica la anchura de la imagen de respuesta (ver imagen).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
TQID: 'https://experienceleague.adobe.com/A1n6WpZEsDWfdLoQZZY-ykX4zXjG86BRXHnVfcpO9yo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 2%

---

# enredar{#wid}

Ver anchura. Especifica la anchura de la imagen de respuesta (ver imagen).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Anchura de la imagen en píxeles (int mayor que 0), </p></td> 
 </tr> 
</table>

## Predeterminado {#section-830bae0b6bac440098444d7cdcb23e2e}

Si no se especifican `wid=`, `hei=` ni `scale=`, la imagen de respuesta será el tamaño de vista predeterminado especificado en el archivo FXG.

Los formatos de trama se representan con el tamaño de vista predeterminado (o el valor DefaultPix ). Haga clic en **[!UICONTROL Configuración de aplicación]** > **[!UICONTROL Configuración de publicación]** > **[!UICONTROL Servidor de imágenes]** y, a continuación, introduzca los valores de anchura y altura. Los tamaños más pequeños proporcionan un mejor rendimiento. Guarde la configuración y realice una publicación para servicio de imágenes para aplicar un cambio.

Si aplica un comando `scale=1`, se procesará una solicitud de formato de trama con el tamaño especificado en el FXG.

## Ejemplo {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

A menos que se especifique un formato, la imagen se procesará como un archivo SWF. En este caso, la altura y la anchura no tienen significado, ya que SWF suele ampliarse al tamaño de la ventana del explorador. Como resultado, `hei` y `wid` solo se aplican a los formatos rasterizado o PDF. Los formatos de trama incluyen:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
