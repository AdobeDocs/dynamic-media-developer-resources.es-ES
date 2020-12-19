---
description: nulo
seo-description: nulo
seo-title: ENVÍO de vídeo HTTPS
solution: Experience Manager
title: ENVÍO de vídeo HTTPS
topic: Dynamic media
uuid: 7f8c1fe6-b464-4d80-9ffe-a36081825d49
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# ENVÍO de vídeo HTTPS{#https-video-delivery}

>[!NOTE]
>
>El Envío de vídeo seguro solo se aplica a AEM 6.2 con la instalación de [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) y a AEM 6.1 con la instalación de [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Siempre que el visor funcione en la configuración como se describe al principio de esta sección, el envío de vídeo publicado puede producirse tanto en los modos HTTPS (seguro) como HTTP (no seguro). En una configuración predeterminada, el protocolo de envío de vídeo sigue estrictamente el protocolo de envío de la página web de incrustación. Sin embargo, es posible forzar el envío de vídeo HTTPS sin tener en cuenta el protocolo utilizado al incrustar la página web mediante el atributo de configuración [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (Tenga en cuenta que la previsualización de vídeo en modo Autor siempre se entrega de forma segura a través de HTTPS).

Según el método de publicación de vídeo de Dynamic Media que utilice en AEM, el atributo de configuración `VideoPlayer.ssl` se aplica de forma diferente, tal como se muestra en lo siguiente:

* Si publica un vídeo de Dynamic Media con una URL, anexe `VideoPlayer.ssl` a la URL. Por ejemplo, para forzar el envío de vídeo seguro, añada `&VideoPlayer.ssl=on` al final del siguiente ejemplo de URL de visor:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   Consulte también [(Vinculación de direcciones URL a su Aplicación web](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Si publica un vídeo de Dynamic Media con código incrustado, agregue `VideoPlayer.ssl` a la lista de otros parámetros de configuración del visor en el fragmento de código incrustado. Por ejemplo, para forzar el envío de vídeo HTTPS, anexe `&VideoPlayer.ssl=on` como en el siguiente ejemplo:

   ```
   <style type="text/css"> 
    #s7mixedmedia_div.s7mixedmediaviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
   <div id="s7mixedmedia_div"></div> 
   <script type="text/javascript"> 
    var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
     "containerId" : "s7mixedmedia_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
    }).init(); 
   </script>
   ```

   Consulte también [(Incrustación del video en una página Web](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

