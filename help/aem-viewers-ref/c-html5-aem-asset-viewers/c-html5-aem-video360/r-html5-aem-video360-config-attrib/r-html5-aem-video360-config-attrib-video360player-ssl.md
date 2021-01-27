---
description: Atributo de configuración para el visor de Video360.
seo-description: Atributo de configuración para el visor de Video360.
seo-title: Video360Player.ssl
solution: Experience Manager
title: Video360Player.ssl
topic: Dynamic Media
uuid: 00c8295c-cc41-489c-a444-ba9189426a20
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 5%

---


# Video360Player.ssl{#video-player-ssl}

Atributo de configuración para el visor de Video360.

>[!NOTE]
>
>Este atributo de configuración solo se aplica a AEM 6.2 con la instalación de [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) y a AEM 6.1 con la instalación de [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Controla si el vídeo se entrega a través de una conexión SSL segura (HTTPS) o de una conexión no segura (HTTP). </p> <p>Cuando se establece en <span class="codeph"> auto</span>, el protocolo de envío de vídeo se hereda del protocolo de la página web de incrustación. Si la página web se carga a través de HTTPS, el vídeo también se entrega a través de HTTPS y viceversa. Si la página web está en HTTP, el vídeo se envía a través de HTTP. </p> <p>Cuando se establece en <span class="codeph"> en</span>, el envío de vídeo siempre se produce a través de una conexión segura independientemente del protocolo de la página Web. </p> <p>Solo afecta al envío de vídeo publicado y se ignora para la previsualización de vídeo en modo Autor. </p> </td> 
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

Consulte también [Envío de vídeo seguro](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27).
