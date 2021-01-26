---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic media
uuid: 0d0f2fd8-b3fc-46fd-8720-9c4c51db9646
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>La plantilla URL del servidor de información se utiliza para recuperar pares de clave/valor para la sustitución de variables en la plantilla de contenido del panel de información. La plantilla especificada suele contener marcadores de posición de macro que se reemplazan con los datos reales antes de que la solicitud se envíe al servidor. </p> <p><span class="codeph"> $1$</span> se reemplaza por el valor de rollover que activó  <span class="codeph"> </span> InfoPanelPopupactivation. </p> <p><span class="codeph"> $2$</span> se sustituye por el número de secuencia del fotograma actual en el conjunto de imágenes. </p> <p><span class="codeph"> $3$</span> se sustituye por el primer elemento de ruta especificado en el nombre del conjunto principal del elemento actual. Normalmente corresponde al ID del catálogo. </p> <p><span class="codeph"> $4$</span> se sustituye por el siguiente elemento en la ruta y corresponde al ID del recurso. La sintaxis real de la solicitud del servidor de información depende del servidor de información y difiere de un servidor a otro. Por ejemplo, la siguiente es una plantilla de solicitud típica del servidor de información de Dynamic Media: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tenga en cuenta que, al configurar la ventana emergente del panel de información, el código HTML y el código JavaScript que se pasan al panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código HTML y código JavaScript sean seguros.

## Propiedades {#section-71356e3c13244e62b0582980d9d05328}

Opcional.

## Predeterminado {#section-22e9af803f724434807d34e200eb7518}

Ninguno.

## Ejemplo {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
