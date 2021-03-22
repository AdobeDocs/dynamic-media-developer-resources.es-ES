---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 2%

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>La plantilla URL del servidor de información se utiliza para recuperar pares clave/valor para la sustitución de variables en la plantilla de contenido del panel de información. La plantilla especificada generalmente contiene marcadores de posición de macro que se sustituyen por los datos reales antes de que la solicitud se envíe al servidor. </p> <p><span class="codeph"> $1$</span> se reemplaza con el valor de sustitución que activó la  <span class="codeph"> </span> activación de InfoPanelPopupactivation. </p> <p><span class="codeph"> $2$</span> se reemplaza con el número de secuencia del fotograma actual en el conjunto de imágenes. </p> <p><span class="codeph"> $3$</span> se reemplaza con el primer elemento de ruta especificado en el nombre del conjunto principal del elemento actual. Normalmente corresponde al ID de catálogo. </p> <p><span class="codeph"> $4$</span> se reemplaza con el siguiente elemento en la ruta y corresponde al ID del recurso. La sintaxis real de la solicitud del servidor de información depende del servidor de información y difiere de un servidor a otro. Por ejemplo, lo siguiente es una plantilla de solicitud de servidor de información de Dynamic Media típica: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
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

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
