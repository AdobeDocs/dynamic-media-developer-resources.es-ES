---
description: Documentación de atributos de configuración para el visor de vídeo interactivo.
seo-description: Documentación de atributos de configuración para el visor de vídeo interactivo.
seo-title: 'Referencia de comandos: Atributos de configuración'
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
topic: Dynamic media
uuid: eaf7a1a2-b0ec-4df2-926b-5e2c4cd0b3d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor de vídeo interactivo.

Cualquier comando de configuración se puede establecer en URL, usando `setParam()`o `setParams()`, o ambos, métodos API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden llevar el prefijo nombre de clase o nombre de instancia del componente SDK del visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM de contenedor del visor que se pasa al método `setContainerId()` API. La documentación incluye un prefijo opcional para dichos comandos. Por ejemplo, `playback` el comando se documenta de la siguiente manera:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

lo que significa que puede utilizar este comando como:

* `playback` (sintaxis corta)
* `VideoPlayer.playback` (calificado con el nombre de clase de componente)
* `cont_videoPlayer.playback` (calificado con ID de componente, suponiendo `cont` que es el ID del elemento de contenedor)

Consulte también Referencia [de comandos común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
