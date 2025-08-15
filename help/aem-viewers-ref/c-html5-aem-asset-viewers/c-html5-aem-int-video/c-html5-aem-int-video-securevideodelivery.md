---
title: Entrega de vídeo HTTPS
description: Entrega de vídeo HTTPS
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 68d37b5d-5015-4a98-84b8-8911ace327ed
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Entrega de vídeo HTTPS{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Si el visualizador funciona en la configuración tal como se describe al principio de esta sección, la entrega de vídeo publicado puede producirse en los modos HTTPS (seguro) y HTTP (no seguro). En una configuración predeterminada, el protocolo de entrega de vídeo sigue estrictamente el protocolo de entrega de la página web en la que se incorpora. Sin embargo, es posible forzar la entrega de vídeo HTTPS independientemente del protocolo utilizado al incrustar la página web utilizando el atributo de configuración [VideoPlayer.ssl](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-ssl.md#reference-c28e1b700977493eadab5489458d7771). (La previsualización de vídeo en el modo Autor siempre se entrega de forma segura a través de HTTPS).

Según el método de publicación de [!DNL Dynamic Media] vídeo que utilice en Adobe Experience Manager, el atributo de configuración `VideoPlayer.ssl` se aplica de forma diferente, tal como se muestra en los siguientes ejemplos:

* Si publica un vídeo de [!DNL Dynamic Media] con una dirección URL, anexa `VideoPlayer.ssl` a la dirección URL. Por ejemplo, para forzar la entrega de vídeo seguro, anexe `&VideoPlayer.ssl=on` al final del siguiente ejemplo de URL del visor:

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/InteractiveVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Shoppable_Video_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&interactivedata=content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt&VideoPlayer.contenturl=https://adobedemo62-h.assetsadobe.com/is/content&VideoPlayer.ssl=on
  ```

  Vea también [Vinculación de direcciones URL a su aplicación web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)

* Si publica un vídeo de [!DNL Dynamic Media] con código incrustado, agrega `VideoPlayer.ssl` a la lista de otros parámetros de configuración del visor en el fragmento de código incrustado. Por ejemplo, para forzar la entrega de vídeo HTTPS, anexe `&VideoPlayer.ssl=on` como en el siguiente ejemplo:

  ```html {.line-numbers}
  <style type="text/css"> 
   #s7interactivevideo_div.s7interactivevideoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
  <div id="s7interactivevideo_div"></div> 
  <script type="text/javascript"> 
   var s7interactivevideoviewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId" : "s7interactivevideo_div", 
    "params" : {  
     "VideoPlayer.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/Shoppable_Video_light", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "interactivedata": "content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt", 
     "VideoPlayer.contenturl": "https://adobedemo62-h.assetsadobe.com/is/content", 
     "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
   }) 
   /* // Example of interactive video event for quick view. 
     s7interactivevideoviewer.setHandlers({  
     "quickViewActivate": function(inData) { 
       var sku=inData.sku; //SKU for product ID 
      //To pass other parameter from the hotspot, you must add custom parameter during the hotspot setup as parameterName=value 
      loadQuickView(sku); //Replace this call with your quickview plugin 
      //Please refer to your quickviewer plugin for the quickview call 
      },  
  "initComplete":function() {  
      //--- Attach quickview pop-up to viewer container so pop-up works in fullscreen mode --- 
      var popup = document.getElementById('quickview_div'); // get custom quick view container 
      popup.parentNode.removeChild(popup); // remove it from current DOM 
      var sdkContainerId = s7interactivevideoviewer.getComponent("container").getInnerContainerId(); // get viewer container component 
      var inner_container = document.getElementById(sdkContainerId);  
      inner_container.appendChild(popup); //Attach custom quick view container to viewer 
      }  
     }); 
   */ 
   s7interactivevideoviewer.init(); 
  </script>
  ```

  Ver también [Incrustación del vídeo en una página web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
