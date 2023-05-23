---
title: 'Referencia de comando: URL'
description: Documentación de referencia de comandos para el visor de Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Referencia de comando: URL{#command-reference-url}

Documentación de referencia de comandos para el visor de Video360.

Puede establecer cualquier comando de configuración en la dirección URL. O bien, puede utilizar los métodos API `setParam()`, o `setParams()`o ambos para establecer cualquier comando de configuración. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Puede codificar algunos comandos de configuración con el nombre de clase o el nombre de instancia del componente correspondiente del SDK de HTML5 Viewer. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor que se pasa a `setContainerId()` Método de API. La documentación incluye prefijos opcionales para estos comandos. Por ejemplo, `playback` se documenta de la siguiente manera:

```
[Video360Player.|<containerId>_video360Player].playback
```

Lo que significa que este comando se utiliza de la siguiente manera:

* `playback` (sintaxis corta)
* `Video360Player.playback` (cualificado con nombre de clase de componente)
* `cont_video360Player.playback` (cualificado con ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Consulte [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visores: URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
