---
description: Documentación de atributos de configuración para el visor de zoom.
seo-description: Documentación de atributos de configuración para el visor de zoom.
seo-title: 'Referencia de comandos: Atributos de configuración'
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
topic: Dynamic media
uuid: 1bcc879a-12ec-4924-ac05-2e4c1d6e4597
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor de zoom.

Cualquier comando de configuración puede configurarse en la dirección URL o mediante `setParam()`, `setParams()` o ambos métodos de API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden llevar el prefijo nombre de clase o nombre de instancia del componente SDK del visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM de contenedor del visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para dichos comandos. Por ejemplo, el comando `zoomstep` se documenta de la siguiente manera:

`[ZoomView.|<containerId>_zoomView].zoomstep`

lo que significa que puede utilizar este comando como:

* `zoomstep` (sintaxis corta)
* `ZoomView.zoomstep` (calificado con el nombre de clase de componente)
* `cont_zoomView.zoomstep` (calificado con ID de componente, suponiendo que  `cont` es el ID del elemento de contenedor)

Consulte también [Referencia de comandos común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
