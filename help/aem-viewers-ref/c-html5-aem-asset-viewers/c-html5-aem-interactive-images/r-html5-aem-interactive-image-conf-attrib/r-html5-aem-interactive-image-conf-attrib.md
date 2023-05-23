---
title: 'Referencia de comando: atributos de configuración'
description: Documentación de atributos de configuración para el visualizador de imágenes interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visualizador de imágenes interactivo.

Cualquier comando de configuración se puede establecer en la dirección URL o mediante `setParam()`, o `setParams()`, o ambos, métodos API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden ir precedidos del nombre de clase o el nombre de instancia del componente SDK de visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor que se pasa a `setContainerId()` Método de API. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, `zoomstep` Este comando se documenta de la siguiente manera:

`[ZoomView.|<containerId>_zoomView].fmt`

Lo que significa que puede utilizar este comando como:

* `fmt` (sintaxis corta)
* `ZoomView.fmt` (cualificado con nombre de clase de componente)
* `cont_zoomView.fmt` (cualificado con ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
