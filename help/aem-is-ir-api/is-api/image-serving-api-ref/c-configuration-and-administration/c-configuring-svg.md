---
description: El componente SvgRender es una aplicación Java independiente.
solution: Experience Manager
title: Configuración de SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 2%

---


# Configuración de SVG{#configuring-svg}

El componente SvgRender es una aplicación Java independiente.

Los ajustes de configuración de SVG se encuentran en [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] y [!DNL ServerSupervisorRegistry.xml].

Se utiliza una conexión socket para comunicarse entre SvgRender y Image Server. El número de puerto es 27346. Si es necesario, se puede cambiar configurando `SVGRender.port` en [!DNL svg.conf] y `<SVGTcpPort>` en [!DNL ImageServerRegistry.xml] en un nuevo valor.

## Véase también {#section-c085b47d54d44059bdaa67fd5e226e91}

[Configuración de SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
