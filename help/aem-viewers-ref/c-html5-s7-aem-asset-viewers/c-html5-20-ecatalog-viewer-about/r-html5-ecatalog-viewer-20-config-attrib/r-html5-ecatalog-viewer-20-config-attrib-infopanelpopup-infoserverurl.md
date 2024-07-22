---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>La plantilla URL del servidor de información se utiliza para recuperar pares clave/valor para la sustitución de variables en la plantilla de contenido del panel de información. La plantilla especificada generalmente contiene marcadores de posición de macros que se reemplazan por los datos reales antes de que la solicitud se envíe al servidor. </p> <p><span class="codeph"> $1$</span> se ha reemplazado por el valor de rollover que activó la activación de <span class="codeph"> InfoPanelPopup</span>. </p> <p><span class="codeph"> $2$</span> se ha reemplazado por el número de secuencia del fotograma actual en el conjunto de imágenes. </p> <p><span class="codeph"> $3$</span> se ha reemplazado por el primer elemento de ruta especificado en el nombre del conjunto principal del elemento actual. Normalmente corresponde al ID de catálogo. </p> <p><span class="codeph"> $4$</span> se ha reemplazado por el elemento siguiente en la ruta y corresponde al id del recurso. La sintaxis real de la solicitud del servidor de información depende del servidor de información y difiere de un servidor a otro. Por ejemplo, a continuación se muestra una plantilla de solicitud de servidor de información típica de Dynamic Media: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Cuando se configura la ventana emergente del Panel de información, el código del HTML y el código de JavaScript que se pasan al Panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código de HTML y código de JavaScript sean seguros.

## Propiedades {#section-71356e3c13244e62b0582980d9d05328}

Opcional.

## Predeterminado {#section-22e9af803f724434807d34e200eb7518}

Ninguno.

## Ejemplo {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
