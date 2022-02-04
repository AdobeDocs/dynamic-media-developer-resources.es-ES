---
title: 'Referencia de comandos: Atributos de configuración'
description: Documentación de atributos de configuración para el visualizador de giros.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visualizador de giros.

Cualquier comando de configuración se puede configurar en la dirección URL o utilizando `setParam()`o `setParams()`, o ambos, métodos de API. Cualquier atributo de configuración también se puede especificar en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden tener el prefijo class name o instance name del componente correspondiente del SDK de visor. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado a `setContainerId()` método de API. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, `zoomstep` se documenta de la siguiente manera:

`[SpinView.|<containerId>_spinView].zoomstep`

Lo que significa que puede utilizar este comando de la siguiente manera

* `zoomstep` (sintaxis corta)
* `SpinView.zoomstep` (cualificado con nombre de clase de componente)
* `cont_spinView.zoomstep` (cualificado con ID de componente, suponiendo `cont` es el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
