---
description: Documentación de referencia de comandos para el visor de vídeo.
seo-description: Documentación de referencia de comandos para el visor de vídeo.
seo-title: 'Referencia de comandos: URL'
solution: Experience Manager
title: 'Referencia de comandos: URL'
topic: Dynamic Media
uuid: 4f9e4a79-6865-4e41-b30b-84ff2c6f6045
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# Referencia de comando - URL{#command-reference-url}

Documentación de referencia de comandos para el visor de vídeo.

Puede definir cualquier comando de configuración en la URL. O bien, puede utilizar los métodos de API `setParam()` o `setParams()`, o ambos para establecer cualquier comando de configuración. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Puede añadir un prefijo a algunos comandos de configuración con el nombre de clase o el nombre de instancia del componente SDK del visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM de contenedor del visor pasado al método de API `setContainerId()`. La documentación incluye prefijos opcionales para dichos comandos. Por ejemplo, `playback` se documenta de la siguiente manera:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

lo que significa que este comando se utiliza de la siguiente manera:

* `playback` (sintaxis corta)
* `VideoPlayer.playback` (calificado con el nombre de clase de componente)
* `cont_videoPlayer.playback` (calificado con ID de componente, suponiendo que  `cont` sea el ID del elemento de contenedor)

Consulte también [Referencia de comandos común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Consulte también [Referencia de comandos común a todos los visores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
