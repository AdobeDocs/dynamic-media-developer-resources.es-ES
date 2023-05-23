---
title: 'Referencia de comando: atributos de configuración'
description: Documentación de atributos de configuración para el visor de giros.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor de giros.

Cualquier comando de configuración se puede establecer en la dirección URL o mediante `setParam()`, o `setParams()`, o ambos, métodos API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden ir precedidos del nombre de clase o el nombre de instancia del componente SDK de visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor que se pasa a `setContainerId()` Método de API. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, `zoomstep` Este comando se documenta de la siguiente manera:

`[SpinView.|<containerId>_spinView].zoomstep`

Lo que significa que puede utilizar este comando de la siguiente manera

* `zoomstep` (sintaxis corta)
* `SpinView.zoomstep` (cualificado con nombre de clase de componente)
* `cont_spinView.zoomstep` (cualificado con ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
