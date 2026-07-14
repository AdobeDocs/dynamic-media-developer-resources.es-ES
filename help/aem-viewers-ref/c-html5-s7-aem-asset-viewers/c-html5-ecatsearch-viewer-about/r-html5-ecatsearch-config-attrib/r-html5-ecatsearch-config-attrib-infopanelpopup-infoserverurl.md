---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
TQID: 'https://experienceleague.adobe.com/en4zktUgJGVG-e0fahRGTxasP3CVxhgfie6d0e3q6r4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

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
>Tenga en cuenta que, al configurar la ventana emergente del Panel de información, el código HTML y el código JavaScript que se pasan al Panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código de HTML y código de JavaScript sean seguros.

## Propiedades {#section-71356e3c13244e62b0582980d9d05328}

Opcional.

## Predeterminado {#section-22e9af803f724434807d34e200eb7518}

Ninguno.

## Ejemplo {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
