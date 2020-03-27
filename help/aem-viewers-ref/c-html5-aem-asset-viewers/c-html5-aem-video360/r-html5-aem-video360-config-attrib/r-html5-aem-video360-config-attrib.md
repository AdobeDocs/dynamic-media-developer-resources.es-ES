---
description: Documentación de atributos de configuración para el visor de Video360.
seo-description: Documentación de atributos de configuración para el visor de Video360.
seo-title: 'Referencia de comandos: Atributos de configuración'
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
topic: Dynamic media
uuid: 645bba87-3d84-46e9-97fc-7019c5dd87ca
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor de Video360.

Cualquier comando de configuración se puede establecer en URL, usando `setParam()`o `setParams()`, o ambos, métodos API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden llevar el prefijo nombre de clase o nombre de instancia del componente SDK del visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM de contenedor del visor que se pasa al método `setContainerId()` API. La documentación incluye un prefijo opcional para dichos comandos. Por ejemplo, `playback` el comando se documenta de la siguiente manera:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

lo que significa que puede utilizar este comando como:

* `playback` (sintaxis corta)
* `VideoPlayer.playback` (calificado con el nombre de clase de componente)
* `cont_videoPlayer.playback` (calificado con ID de componente, suponiendo `cont` que es el ID del elemento de contenedor)

Consulte también Referencia [de comandos común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
