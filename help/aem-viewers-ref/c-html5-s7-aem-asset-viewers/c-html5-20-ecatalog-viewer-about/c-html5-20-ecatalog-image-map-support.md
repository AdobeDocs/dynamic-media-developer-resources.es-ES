---
title: Compatibilidad con mapas de imagen
description: El visor de catálogos electrónicos admite la representación de iconos de mapa de imagen encima de la vista principal.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Compatibilidad con mapas de imagen{#image-map-support}

El visor de catálogos electrónicos admite la representación de iconos de mapa de imagen encima de la vista principal.

El aspecto de los iconos de mapa se controla mediante CSS como se describe en [Efecto de mapa de imagen](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Los mapas de imagen realizan una de las tres acciones siguientes: redireccionar a una página web externa, activar el panel de información emergente e hipervínculos internos.

## Redirigir a una página web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

El atributo `href` del mapa de imagen tiene una dirección URL del recurso externo, especificada explícitamente o incluida en una de las funciones de plantilla de JavaScript admitidas: `loadProduct()`, `loadProductCW()` y `loadProductPW()`.

El siguiente es un ejemplo de redireccionamiento de URL simple:

`href=http://www.adobe.com`

En este ejemplo, la misma dirección URL está ajustada con la función `loadProduct()`:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Cuando agrega el código JavaScript al atributo `HREF` de su mapa de imagen, el código se ejecuta en el equipo del cliente. Por lo tanto, asegúrese de que el código de JavaScript sea seguro.

## Activación emergente del panel de información {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabajar con paneles de información, un mapa de imagen tiene establecido el atributo `ROLLOVER_KEY`. Además, establezca el atributo `href` al mismo tiempo; de lo contrario, el procesamiento de la URL externa interfiere con la activación de la ventana emergente del panel Información.

Finalmente, asegúrese de que la configuración del visor incluye los valores apropiados para `InfoPanelPopup.template` y, opcionalmente, `InfoPanelPopup.infoServerUrl` parámetros.

>[!NOTE]
>
>Cuando se configura la ventana emergente del Panel de información, el código del HTML y el código de JavaScript que se pasan al Panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código de HTML y código de JavaScript sean seguros.

## Hipervínculos internos {#section-6afa4fb2fe564c429e0201f019a95849}

Al seleccionar un mapa de imagen, se realiza un intercambio de página interno dentro del visor. Para usar esa característica, un atributo `href` del mapa de imagen tiene el siguiente formato especial:

` href=target: *`idx`*`

Donde `*`idx`*` es un índice de base cero del pliego de catálogos.

A continuación se muestra un ejemplo de un atributo `href` para un mapa de imagen que señala a la propagación 3D en el catálogo electrónico:

`href=target:2`
