---
description: Documentación de atributos de configuración para el visor flotante
seo-description: Documentación de atributos de configuración para el visor flotante
seo-title: 'Referencia de comandos: Atributos de configuración'
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
topic: Dynamic media
uuid: 0813c334-37b7-43af-b39d-bec66658ad58
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor flotante

Puede definir cualquier comando de configuración en la URL. O bien, puede utilizar `setParam()`, `setParams()` o ambos métodos de API. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración llevan el prefijo nombre de clase o nombre de instancia del componente SDK del visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM de contenedor del visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para dichos comandos. Por ejemplo, el comando `zoomfactor` se documenta de la siguiente manera:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

El comando se utiliza de la siguiente manera:

* `zoomfactor` (sintaxis corta)
* `FlyoutZoomView.zoomfactor` (calificado con un nombre de clase de componente)
* `cont_flyout.zoomfactor` (calificado con el ID del componente, suponiendo que  `cont` sea el ID del elemento de contenedor)

Consulte también [Referencia de comandos común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
