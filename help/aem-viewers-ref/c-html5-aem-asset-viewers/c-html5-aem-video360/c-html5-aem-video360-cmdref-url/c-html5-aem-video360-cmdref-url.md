---
description: Documentación de referencia de comandos para el visualizador de Video360.
solution: Experience Manager
title: 'Referencia de comandos: URL'
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Referencia de comandos: URL{#command-reference-url}

Documentación de referencia de comandos para el visualizador de Video360.

Puede establecer cualquier comando de configuración en la URL. O bien, puede utilizar los métodos API `setParam()`, `setParams()` o ambos para establecer cualquier comando de configuración. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Puede prefijar algunos comandos de configuración con el nombre de clase o el nombre de instancia del componente SDK del visor HTML5 correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye prefijos opcionales para estos comandos. Por ejemplo, `playback` está documentado de la siguiente manera:

```
[Video360Player.|<containerId>_video360Player].playback
```

lo que significa que este comando se utiliza de la siguiente manera:

* `playback` (sintaxis corta)
* `Video360Player.playback` (cualificado con nombre de clase de componente)
* `cont_video360Player.playback` (cualificado con ID de componente, suponiendo que  `cont` sea el ID del elemento contenedor)

Consulte [Referencia de comando común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visualizadores: URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
