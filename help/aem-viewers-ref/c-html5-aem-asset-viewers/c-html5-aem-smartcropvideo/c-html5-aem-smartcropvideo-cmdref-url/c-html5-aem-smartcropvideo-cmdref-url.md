---
title: 'Referencia de comandos: URL'
description: Documentación de referencia de comandos para el visor de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Referencia de comandos: URL{#command-reference-url}

Documentación de referencia de comandos para el visor de vídeo de recorte inteligente.

Puede establecer cualquier comando de configuración en la URL. O bien, puede utilizar los métodos API `setParam()`o `setParams()`, o ambas para configurar cualquier comando de configuración. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Puede prefijar algunos comandos de configuración con el nombre de clase o el nombre de instancia del componente correspondiente del SDK de visor. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado a `setContainerId()` método de API. La documentación incluye prefijos opcionales para estos comandos. Por ejemplo, `playback` está documentado de la siguiente manera:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Lo que significa que este comando se utiliza de la siguiente manera:

* `playback` (sintaxis corta)
* `SmartCropVideoPlayer.playback` (cualificado con nombre de clase de componente)
* `cont_smartCropVideoPlayer.playback` (cualificado con ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Consulte también [Referencia de comando común a todos los visualizadores: URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
