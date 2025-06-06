---
title: Entrega de vídeo HTTP
description: Entrega de vídeo HTTP
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: b809a11f-3c2d-4abd-b317-fabb36245b1b
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Entrega de vídeo HTTP{#http-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Si el visualizador funciona en la configuración tal como se describe al principio de esta sección, la entrega de vídeo publicado puede producirse en los modos HTTPS (seguro) y HTTP (no seguro). En una configuración predeterminada, el protocolo de entrega de vídeo sigue estrictamente el protocolo de entrega de la página web en la que se incorpora. Sin embargo, es posible forzar la entrega de vídeo HTTPS independientemente del protocolo utilizado al incrustar la página web utilizando el atributo de configuración [SmartCropVideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (La previsualización de vídeo en el modo Autor siempre se entrega de forma segura a través de HTTPS).

Según el método de publicación de vídeo de Dynamic Media que utilice en Adobe Experience Manager, el atributo de configuración `SmartCropVideoPlayer.ssl` se aplica de forma diferente, tal como se muestra en el siguiente ejemplo:

* Si publica un vídeo de Dynamic Media con una dirección URL, anexa `SmartCropVideoPlayer.ssl` a la dirección URL. Por ejemplo, para forzar la entrega de vídeo seguro, anexe `&SmartCropVideoPlayer.ssl=on` al final del siguiente ejemplo de URL del visor:

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/SmartCropVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&SmartCropVideoPlayer.ssl=on
  ```

  Consulte también [Vinculación de direcciones URL a su aplicación web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=es#dynamic).

* Si publica un vídeo de Dynamic Media con código incrustado, agrega `SmartCropVideoPlayer.ssl` a la lista de otros parámetros de configuración del visor en el fragmento de código incrustado. Por ejemplo, para forzar la entrega de vídeo HTTPS, anexe `&SmartCropVideoPlayer.ssl=on` como en el siguiente ejemplo:

  ```
  <style type="text/css"> 
   #s7video_div.s7videoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
  <div id="s7video_div"></div> 
  <script type="text/javascript"> 
   var s7videoviewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId" : "s7video_div", 
    "params" : {  
     "SmartCropVideoPlayer.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/Video", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
     "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
   }).init(); 
  </script>
  ```

  Ver también [Incrustación del vídeo en una página web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=es#dynamic).
