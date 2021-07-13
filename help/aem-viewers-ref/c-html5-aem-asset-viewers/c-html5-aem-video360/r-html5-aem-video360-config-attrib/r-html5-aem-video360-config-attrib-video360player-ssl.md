---
description: Atributo de configuración para el visualizador de vídeo360.
solution: Experience Manager
title: Video360Player.ssl
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Developer,User
exl-id: 44efa378-c911-4449-8a10-61212d4392c6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 4%

---

# Video360Player.ssl{#video-player-ssl}

Atributo de configuración para el visualizador de vídeo360.

>[!NOTE]
>
>Este atributo de configuración solo se aplica a AEM 6.2 con la instalación del [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) y a AEM 6.1 con la instalación del [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

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

Consulte también [Entrega segura de vídeo](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27).
