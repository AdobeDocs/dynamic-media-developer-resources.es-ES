---
title: wid
description: Ver anchura. Especifica la anchura de la imagen de respuesta (ver imagen).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 4%

---

# wid{#wid}

Ver anchura. Especifica la anchura de la imagen de respuesta (ver imagen).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Anchura de la imagen en píxeles (int mayor que 0), </p></td> 
 </tr> 
</table>

## Predeterminado {#section-830bae0b6bac440098444d7cdcb23e2e}

Si ninguno `wid=`, `hei=`, ni `scale=` Si se especifican, la imagen de respuesta es el tamaño de vista predeterminado especificado en el archivo FXG.

Los formatos de trama se representan con el tamaño de vista predeterminado (o el valor DefaultPix ). Clic **[!UICONTROL Ajustes de aplicación]** > **[!UICONTROL Ajustes de publicación]** > **[!UICONTROL Servidor de imágenes]** y, a continuación, introduzca los valores de anchura y altura. Los tamaños más pequeños proporcionan un mejor rendimiento. Guarde la configuración y realice una publicación para servicio de imágenes para aplicar un cambio.

Si aplica una `scale=1` , se procesa una solicitud de formato rasterizado con el tamaño especificado en el FXG.

## Ejemplo {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

A menos que se especifique un formato, la imagen se procesa como un archivo de SWF. En este caso, el alto y el ancho no tienen significado, ya que el SWF suele ampliarse al tamaño de la ventana del explorador. Como resultado, `hei` y `wid` solo se aplica a los formatos rasterizado o PDF. Los formatos de trama incluyen:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alpha
* PNG-alpha
