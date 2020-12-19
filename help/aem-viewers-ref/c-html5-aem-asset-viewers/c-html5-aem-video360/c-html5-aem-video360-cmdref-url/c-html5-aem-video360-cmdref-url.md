---
description: Documentación de referencia de comandos para el visor de Video360.
seo-description: Documentación de referencia de comandos para el visor de Video360.
seo-title: 'Referencia de comandos: URL'
solution: Experience Manager
title: 'Referencia de comandos: URL'
topic: Dynamic media
uuid: 70c212d7-35ee-408f-abe4-19ba1e4d773d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Referencia de comando - URL{#command-reference-url}

Documentación de referencia de comandos para el visor de Video360.

Puede definir cualquier comando de configuración en la URL. O bien, puede utilizar los métodos de API `setParam()` o `setParams()`, o ambos para establecer cualquier comando de configuración. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Puede añadir un prefijo a algunos comandos de configuración con el nombre de clase o el nombre de instancia del componente correspondiente del SDK del visor HTML5. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM de contenedor del visor pasado al método de API `setContainerId()`. La documentación incluye prefijos opcionales para dichos comandos. Por ejemplo, `playback` se documenta de la siguiente manera:

```
[Video360Player.|<containerId>_video360Player].playback
```

lo que significa que este comando se utiliza de la siguiente manera:

* `playback` (sintaxis corta)
* `Video360Player.playback` (calificado con el nombre de clase de componente)
* `cont_video360Player.playback` (calificado con ID de componente, suponiendo que  `cont` sea el ID del elemento de contenedor)

Consulte [Referencia de comandos común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comandos común a todos los visores: URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
