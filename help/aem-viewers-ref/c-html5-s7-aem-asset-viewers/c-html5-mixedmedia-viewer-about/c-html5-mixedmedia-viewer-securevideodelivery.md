---
title: Entrega de vídeo HTTPS
description: Entrega de vídeo HTTPS
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f9651405-ebc6-4b1f-8fb6-031d0b295083
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Entrega de vídeo HTTPS{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Si el visualizador funciona en la configuración tal como se describe al principio de esta sección, la entrega de vídeo publicado puede producirse en los modos HTTPS (seguro) y HTTP (no seguro). En una configuración predeterminada, el protocolo de entrega de vídeo sigue estrictamente el protocolo de entrega de la página web en la que se incorpora. Sin embargo, es posible forzar la entrega de vídeo HTTPS independientemente del protocolo utilizado al incrustar la página web utilizando el atributo de configuración [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (La previsualización de vídeo en el modo Autor siempre se entrega de forma segura a través de HTTPS).

Según el método de publicación de vídeo de Dynamic Media que utilice en Adobe Experience Manager, el atributo de configuración `VideoPlayer.ssl` se aplica de forma diferente, tal como se muestra en el siguiente ejemplo:

* Si publica un vídeo de Dynamic Media con una dirección URL, anexa `VideoPlayer.ssl` a la dirección URL. Por ejemplo, para forzar la entrega de vídeo seguro, anexe `&VideoPlayer.ssl=on` al final del siguiente ejemplo de URL del visor:

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
  ```

  Vea también [(Vinculando direcciones URL a su aplicación web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=es#dynamic)).

* Si publica un vídeo de Dynamic Media con código incrustado, agrega `VideoPlayer.ssl` a la lista de otros parámetros de configuración del visor en el fragmento de código incrustado. Por ejemplo, para forzar la entrega de vídeo HTTPS, anexe `&VideoPlayer.ssl=on` como en el siguiente ejemplo:

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

  Vea también [(Incrustación del vídeo en una página web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=es#dynamic).
