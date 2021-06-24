---
description: Documentación de atributos de configuración para el visor flotante
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flotante
role: Developer,Business Practitioner
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor flotante

Puede establecer cualquier comando de configuración en la dirección URL. O bien, puede utilizar `setParam()`, `setParams()` o ambos métodos API. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

A algunos comandos de configuración se les añade el prefijo nombre de clase o nombre de instancia del componente correspondiente del SDK de visor. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, el comando `zoomfactor` se documenta de la siguiente manera:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

El comando se utiliza de la siguiente manera:

* `zoomfactor` (sintaxis corta)
* `FlyoutZoomView.zoomfactor` (cualificado con un nombre de clase de componente)
* `cont_flyout.zoomfactor` (cualificado con el ID de componente, suponiendo que  `cont` sea el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores - Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
