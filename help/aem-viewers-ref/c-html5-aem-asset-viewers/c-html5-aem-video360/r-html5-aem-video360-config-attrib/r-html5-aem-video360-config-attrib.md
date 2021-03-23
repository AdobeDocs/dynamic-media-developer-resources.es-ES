---
description: Documentación de atributos de configuración para el visualizador de Video360.
seo-description: Documentación de atributos de configuración para el visualizador de Video360.
seo-title: 'Referencia de comandos: Atributos de configuración'
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
uuid: 645bba87-3d84-46e9-97fc-7019c5dd87ca
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Documentación de atributos de configuración para el visualizador de Video360.

Cualquier comando de configuración se puede configurar en la dirección URL o utilizando `setParam()`, `setParams()`, o ambos métodos API. Cualquier atributo de configuración también se puede especificar en el registro de configuración del lado del servidor.

Algunos comandos de configuración pueden tener el prefijo class name o instance name del componente correspondiente del SDK de visor. Un nombre de instancia del componente es dinámico y depende del ID del elemento DOM del contenedor de visor pasado al método de API `setContainerId()`. La documentación incluye un prefijo opcional para estos comandos. Por ejemplo, el comando `playback` está documentado de la siguiente manera:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

lo que significa que puede utilizar este comando como:

* `playback` (sintaxis corta)
* `VideoPlayer.playback` (cualificado con nombre de clase de componente)
* `cont_videoPlayer.playback` (cualificado con ID de componente, suponiendo que  `cont` sea el ID del elemento contenedor)

Consulte también [Referencia de comando común a todos los visores - Atributos de configuración](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
