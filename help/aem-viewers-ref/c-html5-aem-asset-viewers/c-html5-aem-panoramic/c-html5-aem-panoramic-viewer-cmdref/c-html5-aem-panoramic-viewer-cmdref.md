---
title: 'Referencia de comando: atributos de configuración'
description: Documentación de atributos de configuración para el visor panorámico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor panorámico.

Cualquier comando de configuración se puede establecer en la dirección URL o mediante `setParam()` y/o `setParams()` Métodos de API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden ir precedidos del nombre de clase o del nombre de instancia del componente de SDK de HTML5 correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor que se pasa a `setContainerId()` Método de API. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, `vrrender` Este comando se documenta de la siguiente manera:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Lo que significa que este comando se utiliza de la siguiente manera:

* `vrrender` (sintaxis corta)
* `PanoramicView.vrrender` (cualificado con nombre de clase de componente)
* `cont_panoramicView.vrrender` (cualificado con ID de componente, suponiendo que el recuento es el ID del elemento contenedor)


Consulte [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consulte [Referencia de comando común a todos los visores: URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
