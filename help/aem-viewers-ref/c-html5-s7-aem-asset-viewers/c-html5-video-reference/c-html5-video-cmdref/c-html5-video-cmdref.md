---
title: 'Referencia de comando: atributos de configuración'
description: Documentación de atributos de configuración para el Visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 5992e5cd-7783-408e-a23f-fdcc3a3d6b69
TQID: 'https://experienceleague.adobe.com/bmQmgsGvn-IjdQEwiTs9F-j7z94hoNtJWhUVkUsh3pU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el Visor de vídeo.

Puede establecer cualquier comando de configuración en la dirección URL. O bien, puede usar los métodos de API `setParam()`, `setParams()` o ambos para establecer cualquier comando de configuración. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración se pueden prefijar con el nombre de clase o el nombre de instancia del componente correspondiente de Viewer SDK. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye prefijos opcionales para estos comandos. Por ejemplo, `playback` está documentado de la siguiente manera:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Lo que significa que este comando se utiliza de la siguiente manera

* `playback` (sintaxis corta)
* `VideoPlayer.playback` (cualificado con nombre de clase de componente)
* `cont_videoPlayer.playback` (cualificado con ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Ver [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Ver [Referencia de comando común a todos los visores: URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
