---
description: Documentación de atributos de configuración para el visor de zoom.
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Developer,Business Practitioner
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor de zoom.

Cualquier comando de configuración se puede configurar en la dirección URL o utilizando `setParam()`, `setParams()`, o ambos métodos API. Cualquier atributo de configuración también se puede especificar en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden tener el prefijo class name o instance name del componente correspondiente del SDK de visor. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, el comando `zoomstep` está documentado de la siguiente manera:

`[ZoomView.|<containerId>_zoomView].zoomstep`

lo que significa que puede utilizar este comando como:

* `zoomstep` (sintaxis corta)
* `ZoomView.zoomstep` (cualificado con nombre de clase de componente)
* `cont_zoomView.zoomstep` (cualificado con ID de componente, suponiendo que  `cont` sea el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores - Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
