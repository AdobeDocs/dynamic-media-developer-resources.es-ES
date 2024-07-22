---
title: 'Referencia de comando: atributos de configuración'
description: Documentación de atributos de configuración para el Visor de carrusel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 71c2c973-d711-4d37-b778-381a7ec71527
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el Visor de carrusel.

Cualquier comando de configuración se puede establecer en la dirección URL o mediante `setParam()`, `setParams()` o ambos métodos API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden ir precedidos del nombre de clase o el nombre de instancia del componente SDK de visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, el comando `zoomstep` está documentado de la siguiente manera:

`[ZoomView.|<containerId>_carouselView].fmt`

En este caso, puede utilizar este comando:

* `fmt` (sintaxis corta)
* `CarouselView.fmt` (cualificado con nombre de clase de componente)
* `cont_carouselView.fmt` (cualificado con ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Vea también [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
