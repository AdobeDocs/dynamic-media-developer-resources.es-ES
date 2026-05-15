---
title: 'Referencia de comando: atributos de configuración'
description: Documentación de atributos de configuración para el visor panorámico.
solution: Experience Manager
role: Developer,User
autotag-review: '2026-05-13T22:15:11.019Z'
TQID: 'https://experienceleague.adobe.com/-6kskMStr-k7aFwy9GpQE-wjq4iAgwuEqzP2H1BWk2U'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

<!--
feature: Dynamic Media Classic,Viewers,SDK/API
-->

Documentación de atributos de configuración para el visor panorámico.

Cualquier comando de configuración se puede establecer en la dirección URL o mediante `setParam()` o `setParams()` métodos de API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden ir precedidos del nombre de clase o del nombre de instancia del componente SDK de HTML5 correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, el comando `vrrender` está documentado de la siguiente manera:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Lo que significa que este comando se utiliza de la siguiente manera:

* `vrrender` (sintaxis corta)
* `PanoramicView.vrrender` (cualificado con nombre de clase de componente)
* `cont_panoramicView.vrrender` (cualificado con ID de componente, suponiendo que el recuento es el ID del elemento contenedor)


Ver [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Ver [Referencia de comando común a todos los visores: URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
