---
title: 'Referencia de comandos: Atributos de configuración'
description: Documentación de atributos de configuración para el visor panorámico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor panorámico.

Cualquier comando de configuración se puede configurar en la dirección URL o utilizando `setParam()` y/o `setParams()` Métodos de API. Cualquier atributo de configuración también se puede especificar en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden tener el prefijo class name o instance name del componente SDK HTML5 correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado a `setContainerId()` método de API. La documentación incluirá el prefijo opcional para estos comandos. Por ejemplo, `vrrender` se documenta de la siguiente manera:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Lo que significa que este comando se utiliza de la siguiente manera:

* `vrrender` (sintaxis corta)
* `PanoramicView.vrrender` (cualificado con nombre de clase de componente)
* `cont_panoramicView.vrrender` (cualificado con ID de componente, suponiendo que cont es el ID del elemento contenedor)


Consulte [Referencia de comando común a todos los visores: Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consulte [Referencia de comando común a todos los visualizadores: URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
