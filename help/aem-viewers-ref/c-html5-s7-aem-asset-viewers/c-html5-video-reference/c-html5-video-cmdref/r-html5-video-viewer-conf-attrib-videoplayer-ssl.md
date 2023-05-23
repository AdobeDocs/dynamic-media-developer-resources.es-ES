---
title: VideoPlayer.ssl
description: Atributo de configuración para el visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: f7d832f3-e9b1-4161-a572-851e538bb245
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# VideoPlayer.ssl{#videoplayer-ssl}

Atributo de configuración para el visor de vídeo.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|activado</span> </p> </td> 
   <td colname="col2"> <p> Controla si el vídeo se envía a través de una conexión SSL segura (HTTPS) o una conexión no segura (HTTP). </p> <p>Cuando se establece en <span class="codeph"> auto</span> el protocolo de entrega de vídeo se hereda del protocolo de la página web en la que se incorpora. Si la página web se carga a través de HTTPS, el vídeo también se envía a través de HTTPS y a la inversa. Si la página web está en HTTP, el vídeo se envía a través de HTTP. </p> <p>Cuando se establece en <span class="codeph"> el</span>Sin embargo, la entrega de vídeo siempre se produce a través de una conexión segura, independientemente del protocolo de la página web. </p> <p>Solo afecta a la entrega de vídeo publicado y se ignora para la previsualización de vídeo en el modo Autor. </p> </td> 
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

Consulte también [Entrega segura de vídeos](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff).
