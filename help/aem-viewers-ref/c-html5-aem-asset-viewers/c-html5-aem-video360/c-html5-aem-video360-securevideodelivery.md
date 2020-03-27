---
description: nulo
seo-description: nulo
seo-title: envío de vídeo HTTPS
solution: Experience Manager
title: envío de vídeo HTTPS
topic: Dynamic media
uuid: 68984ba1-2802-496a-8ad0-ba46b59514ad
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365

---


# envío de vídeo HTTPS{#https-video-delivery}

>[!NOTE]
>
>El Envío de vídeo seguro HTTP solo se aplica a AEM 6.2 con la instalación de [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) y a AEM 6.1 con la instalación de [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Siempre que el visor funcione en la configuración como se describe al principio de esta sección, el envío de vídeo publicado puede producirse tanto en los modos HTTPS (seguro) como HTTP (no seguro). En una configuración predeterminada, el protocolo de envío de vídeo sigue estrictamente el protocolo de envío de la página web de incrustación. Sin embargo, es posible forzar el envío de vídeo HTTPS independientemente del protocolo utilizado al incrustar la página web con el atributo de configuración [Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md) . (Tenga en cuenta que la previsualización de vídeo en modo Autor siempre se entrega de forma segura a través de HTTPS).

Según el método de publicación de vídeo de Dynamic Media que utilice en AEM, el atributo de configuración se aplica de forma diferente, como se muestra en el ejemplo siguiente: `Video360Player.ssl`

* Si publica un vídeo de Dynamic Media con una URL, anexe `Video360Player.ssl` a la URL. Por ejemplo, para forzar el envío de vídeo seguro, añada `&Video360Player.ssl=on` al final del siguiente ejemplo de URL de visor:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   See also [Linking URLs to your Web Application](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Si publica un vídeo de Dynamic Media con código incrustado, añada `Video360Player.ssl` a la lista de otros parámetros de configuración del visor en el fragmento de código incrustado. Por ejemplo, para forzar el envío de vídeo HTTPS, anexe `&Video360Player.ssl=on` como en el siguiente ejemplo:

   ```
   <style type="text/css"> 
    #s7video_div.s7video360viewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7video360viewer = new s7viewers.Video360Viewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "Video360Player.ssl" : "on", 
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

   See also [Embedding the Video on a Web Page](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html)

