---
title: 'Referencia de comando: atributos de configuración'
description: Documentación de atributos de configuración para el visualizador de medios mixtos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aa750941-0a2e-4591-bdff-5e71ecc342aa
TQID: 'https://experienceleague.adobe.com/7s8EFmP3YkVcrk2kMi35mXMrffw1GQQTmXTwvWWGVnc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 0%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visualizador de medios mixtos.

Cualquier comando de configuración se puede establecer en la dirección URL o mediante `setParam()`, `setParams()` o ambos métodos API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden ir precedidos del nombre de clase o del nombre de instancia del componente correspondiente de Viewer SDK. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, el comando `zoomstep` está documentado de la siguiente manera:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Lo que significa que puede utilizar este comando de la siguiente manera

* `zoomstep` (sintaxis corta)
* `ZoomView.zoomstep` (cualificado con nombre de clase de componente)
* `cont_zoomView.zoomstep` (cualificado con ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Vea también [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
