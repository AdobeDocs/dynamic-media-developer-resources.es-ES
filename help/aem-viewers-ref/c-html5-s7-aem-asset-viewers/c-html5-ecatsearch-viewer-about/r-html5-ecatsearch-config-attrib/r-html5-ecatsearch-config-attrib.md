---
description: Documentación de atributos de configuración para eCatalog Viewer.
solution: Experience Manager
title: 'Referencia de comando: atributos de configuración'
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para eCatalog Viewer.

Cualquier comando de configuración se puede establecer en la dirección URL o mediante `setParam()`, o `setParams()`, o ambos, métodos API. También puede especificar cualquier atributo de configuración especificado en el registro de configuración del lado del servidor.

Para algunos comandos de configuración, puede añadirlos como prefijo al nombre de clase o al nombre de instancia del componente SDK de visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor que se pasa a `setContainerId()` Método de API. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, `zoomstep` Este comando se documenta de la siguiente manera:

`[PageView.|<containerId>_pageView].zoomstep`

lo que significa que puede utilizar este comando como:

* `zoomstep` (sintaxis corta)
* `PageView.zoomstep` (cualificado con nombre de clase de componente)
* `cont_pageView.zoomstep` (cualificado con ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
