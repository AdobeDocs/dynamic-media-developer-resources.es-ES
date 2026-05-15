---
title: 'Referencia de comando: atributos de configuración'
description: Documentación de atributos de configuración para el visor flotante
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
TQID: 'https://experienceleague.adobe.com/-SDMo-YVHg3J9yAlQWa3kd5oXJZj9IQXJjpsyOrrXpg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 0%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor flotante

Puede establecer cualquier comando de configuración en la dirección URL. O bien, puede usar `setParam()`, `setParams()` o ambos métodos API. También puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración llevan como prefijo el nombre de clase o el nombre de instancia del componente correspondiente de Viewer SDK. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, el comando `zoomfactor` está documentado de la siguiente manera:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

El comando se utiliza de la siguiente manera:

* `zoomfactor` (sintaxis corta)
* `FlyoutZoomView.zoomfactor` (cualificado con un nombre de clase de componente)
* `cont_flyout.zoomfactor` (cualificado con el ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Vea también [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
