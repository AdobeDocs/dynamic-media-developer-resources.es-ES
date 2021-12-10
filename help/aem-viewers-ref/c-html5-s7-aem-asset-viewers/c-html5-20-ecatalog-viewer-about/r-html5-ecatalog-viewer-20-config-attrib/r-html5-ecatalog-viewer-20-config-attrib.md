---
title: 'Referencia de comandos: Atributos de configuración'
description: Documentación de atributos de configuración para el visor de catálogos electrónicos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor de catálogos electrónicos.

Cualquier comando de configuración se puede configurar en la dirección URL o utilizando `setParam()`o `setParams()`, o ambos, métodos de API. También puede especificar cualquier atributo de configuración especificado en el registro de configuración del lado del servidor.

Para algunos comandos de configuración, puede prefijarlos con el nombre de clase o el nombre de instancia del componente correspondiente del SDK de visor. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado a `setContainerId()` método de API. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, `zoomstep` se documenta de la siguiente manera:

`[PageView.|<containerId>_pageView].zoomstep`

Lo que significa que puede utilizar este comando como

* `zoomstep` (sintaxis corta)
* `PageView.zoomstep` (cualificado con nombre de clase de componente)
* `cont_pageView.zoomstep` (cualificado con ID de componente, suponiendo `cont` es el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
