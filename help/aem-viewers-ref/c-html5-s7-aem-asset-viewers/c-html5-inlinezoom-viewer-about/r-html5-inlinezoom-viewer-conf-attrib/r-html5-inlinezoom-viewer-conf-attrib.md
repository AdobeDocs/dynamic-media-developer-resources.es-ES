---
title: 'Referencia de comandos: Atributos de configuración'
description: Documentación de atributos de configuración para el visor flotante
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor flotante

Puede establecer cualquier comando de configuración en la dirección URL. O bien, puede usar `setParam()`, `setParams()`, o ambos métodos API. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

A algunos comandos de configuración se les añade el prefijo nombre de clase o nombre de instancia del componente correspondiente del SDK de visor. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado a `setContainerId()` método de API. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, la variable `zoomfactor` se documenta de la siguiente manera:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

El comando se utiliza de la siguiente manera:

* `zoomfactor` (sintaxis corta)
* `FlyoutZoomView.zoomfactor` (cualificado con un nombre de clase de componente)
* `cont_flyout.zoomfactor` (cualificado con el ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
