---
description: Documentación de atributos de configuración para el visor de medios mixtos.
seo-description: Documentación de atributos de configuración para el visor de medios mixtos.
seo-title: 'Referencia de comandos: Atributos de configuración'
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
topic: Dynamic media
uuid: c0f09a05-f024-4cf0-a65f-0bfee015f635
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor de medios mixtos.

Cualquier comando de configuración se puede establecer en URL, usando `setParam()`o `setParams()`, o ambos, métodos API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden llevar el prefijo nombre de clase o nombre de instancia del componente SDK del visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM de contenedor del visor que se pasa al método `setContainerId()` API. La documentación incluye un prefijo opcional para dichos comandos. Por ejemplo, `zoomstep` el comando se documenta de la siguiente manera:

`[ZoomView.|<containerId>_zoomView].zoomstep`

lo que significa que puede utilizar este comando como:

* `zoomstep` (sintaxis corta)
* `ZoomView.zoomstep` (calificado con el nombre de clase de componente)
* `cont_zoomView.zoomstep` (calificado con ID de componente, suponiendo `cont` que es el ID del elemento de contenedor)

Consulte también Referencia [de comandos común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
