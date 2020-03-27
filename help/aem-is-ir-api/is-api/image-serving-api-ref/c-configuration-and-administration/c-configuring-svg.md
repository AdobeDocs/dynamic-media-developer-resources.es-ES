---
description: El componente SvgRender es una aplicación Java independiente.
seo-description: El componente SvgRender es una aplicación Java independiente.
seo-title: Configuración de SVG
solution: Experience Manager
title: Configuración de SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: f6e131af-283e-4649-b349-123489c0838d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Configuración de SVG{#configuring-svg}

El componente SvgRender es una aplicación Java independiente.

La configuración de SVG se encuentra en [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml]y [!DNL ServerSupervisorRegistry.xml].

Se utiliza una conexión de socket para comunicarse entre SvgRender y el servidor de imágenes. El número de puerto es 27346. Si es necesario, se puede cambiar configurando `SVGRender.port` en [!DNL svg.conf] y `<SVGTcpPort>` en [!DNL ImageServerRegistry.xml] un nuevo valor.

## Véase también {#section-c085b47d54d44059bdaa67fd5e226e91}

[Configuración de SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
