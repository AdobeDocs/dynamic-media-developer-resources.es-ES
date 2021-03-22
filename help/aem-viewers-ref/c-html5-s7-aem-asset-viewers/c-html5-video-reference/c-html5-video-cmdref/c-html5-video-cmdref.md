---
description: Documentación de atributos de configuración para el visualizador de vídeo.
seo-description: Documentación de atributos de configuración para el visualizador de vídeo.
seo-title: 'Referencia de comandos: Atributos de configuración'
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
uuid: 837cf230-f7dd-4010-a299-c3267d11e200
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visualizador de vídeo.

Puede establecer cualquier comando de configuración en la URL. O bien, puede utilizar los métodos API `setParam()`, `setParams()` o ambos para establecer cualquier comando de configuración. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Puede prefijar algunos comandos de configuración con el nombre de clase o el nombre de instancia del componente correspondiente del SDK de visor. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye prefijos opcionales para estos comandos. Por ejemplo, `playback` está documentado de la siguiente manera:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

lo que significa que este comando se utiliza de la siguiente manera:

* `playback` (sintaxis corta)
* `VideoPlayer.playback` (cualificado con nombre de clase de componente)
* `cont_videoPlayer.playback` (cualificado con ID de componente, suponiendo que  `cont` sea el ID del elemento contenedor)

Consulte [Referencia de comando común a todos los visores - Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consulte [Referencia de comando común a todos los visores: URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
