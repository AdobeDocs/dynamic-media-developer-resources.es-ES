---
description: Atributo de configuración para el visualizador de vídeo de medios mixtos.
solution: Experience Manager
title: VideoPlayer.ssl
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Developer,Business Practitioner
exl-id: 5fd3aa39-edb0-4434-aa5f-e511c84cf950
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# VideoPlayer.ssl{#videoplayer-ssl}

Atributo de configuración para el visualizador de vídeo de medios mixtos.

>[!NOTE]
>
>Este atributo de configuración solo se aplica a AEM 6.2 con la instalación del [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) y a AEM 6.1 con la instalación del [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Controla si el vídeo se entrega a través de una conexión SSL segura (HTTPS) o una conexión no segura (HTTP). </p> <p>Cuando se establece en <span class="codeph"> auto</span> , el protocolo de entrega de vídeo se hereda del protocolo de la página web de incrustación. Si la página web se carga a través de HTTPS, el vídeo también se envía a través de HTTPS y viceversa. Si la página web está en HTTP, el vídeo se envía a través de HTTP. </p> <p>Cuando se establece en <span class="codeph"> en</span>, el envío de vídeo siempre se produce a través de una conexión segura independientemente del protocolo de la página web. </p> <p>Solo afecta a la entrega de vídeo publicado y se ignora para la previsualización de vídeo en modo Autor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

Consulte también [Entrega segura de vídeo](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb).
