---
title: 'Referencia de comando: atributos de configuración'
description: Documentación de atributos de configuración para el visor de Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visor de Video360.

Cualquier comando de configuración se puede establecer en la dirección URL o mediante `setParam()`, `setParams()` o ambos métodos API. También se puede especificar cualquier atributo de configuración en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden ir precedidos del nombre de clase o el nombre de instancia del componente SDK de visor correspondiente. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, el comando `playback` está documentado de la siguiente manera:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

Lo que significa que puede utilizar este comando en lo siguiente:

* `playback` (sintaxis corta)
* `VideoPlayer.playback` (cualificado con nombre de clase de componente)
* `cont_videoPlayer.playback` (cualificado con ID de componente, suponiendo que `cont` es el ID del elemento contenedor)

Vea también [Referencia de comando común a todos los visores: atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
