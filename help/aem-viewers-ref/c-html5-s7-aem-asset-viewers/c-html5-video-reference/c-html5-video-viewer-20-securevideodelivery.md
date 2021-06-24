---
description: Entrega de vídeo HTTP
solution: Experience Manager
title: Entrega de vídeo HTTP
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Developer,Business Practitioner
exl-id: 33907e22-107b-4345-82bb-cad47cb7a839
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Entrega de vídeo HTTP{#http-video-delivery}

>[!NOTE]
>
>La entrega de vídeo seguro solo se aplica a AEM 6.2 con la instalación de [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) y a AEM 6.1 con la instalación de [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Siempre que el visor funcione en una configuración como se describe al principio de esta sección, la entrega de vídeo publicado puede realizarse tanto en los modos HTTPS (seguro) como HTTP (inseguro). En una configuración predeterminada, el protocolo de entrega de vídeo sigue estrictamente el protocolo de entrega de la página web de incrustación. Sin embargo, es posible forzar el envío de vídeo HTTPS independientemente del protocolo utilizado al incrustar la página web utilizando el atributo de configuración [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) . (Tenga en cuenta que la previsualización de vídeo en modo Autor siempre se entrega de forma segura a través de HTTPS).

Según el método de publicación de vídeo de Dynamic Media que utilice en AEM, el atributo de configuración `VideoPlayer.ssl` se aplica de forma diferente, como se muestra en lo siguiente:

* Si publica un vídeo de Dynamic Media con una dirección URL, anexe `VideoPlayer.ssl` a la dirección URL. Por ejemplo, para forzar el envío seguro de vídeo, añada `&VideoPlayer.ssl=on` al final del siguiente ejemplo de URL de visor:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
   ```

   Consulte también [Vinculación de URL a su aplicación web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Si publica un vídeo de Dynamic Media con código incrustado, añada `VideoPlayer.ssl` a la lista de otros parámetros de configuración del visor en el fragmento de código incrustado. Por ejemplo, para forzar el envío de vídeo HTTPS, añada `&VideoPlayer.ssl=on` como en el siguiente ejemplo:

   ```
   <style type="text/css"> 
    #s7video_div.s7videoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/VideoViewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7videoviewer = new s7viewers.VideoViewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
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

   Consulte también [Incrustación del vídeo en una página web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
