---
title: 'Referencia de comandos: Atributos de configuración'
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

# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visualizador de imágenes interactivo.

Cualquier comando de configuración se puede configurar en la dirección URL o utilizando `setParam()`, `setParams()`, o ambos métodos API. Cualquier atributo de configuración también se puede especificar en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden tener el prefijo class name o instance name del componente correspondiente del SDK de visor. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, el comando `zoomstep` está documentado de la siguiente manera:

`[ZoomView.|<containerId>_zoomView].fmt`

Lo que significa que puede utilizar este comando como:

* `fmt` (sintaxis corta)
* `ZoomView.fmt` (cualificado con nombre de clase de componente)
* `cont_zoomView.fmt` (cualificado con ID de componente, suponiendo que  `cont` sea el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores - Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
