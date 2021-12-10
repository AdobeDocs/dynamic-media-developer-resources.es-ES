---
title: 'Referencia de comandos: Atributos de configuración'
description: Documentación de atributos de configuración para el visor de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor de zoom.

Cualquier comando de configuración se puede configurar en la dirección URL o utilizando `setParam()`o `setParams()`, o ambos, métodos de API. Cualquier atributo de configuración también se puede especificar en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden tener el prefijo class name o instance name del componente correspondiente del SDK de visor. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado a `setContainerId()` método de API. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, `zoomstep` se documenta de la siguiente manera:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Lo que significa que puede utilizar el comando como

* `zoomstep` (sintaxis corta)
* `ZoomView.zoomstep` (cualificado con nombre de clase de componente)
* `cont_zoomView.zoomstep` (cualificado con ID de componente, suponiendo `cont` es el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
