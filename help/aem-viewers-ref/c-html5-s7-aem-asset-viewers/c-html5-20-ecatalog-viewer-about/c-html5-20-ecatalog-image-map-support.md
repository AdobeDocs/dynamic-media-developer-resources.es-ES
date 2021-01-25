---
description: El visor de catálogos electrónicos admite la representación de iconos de mapas de imagen sobre la vista principal.
seo-description: El visor de catálogos electrónicos admite la representación de iconos de mapas de imagen sobre la vista principal.
seo-title: Compatibilidad con mapas de imagen
solution: Experience Manager
title: Compatibilidad con mapas de imagen
topic: Dynamic media
uuid: 69aeda21-909d-45da-bcf5-73ade8c5adda
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Compatibilidad con mapas de imagen{#image-map-support}

El visor de catálogos electrónicos admite la representación de iconos de mapas de imagen sobre la vista principal.

El aspecto de los iconos de mapa se controla mediante CSS, tal como se describe en [Efecto de mapa de imagen](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Los mapas de imagen realizan una de las tres acciones siguientes: redirija a una página web externa, a la activación emergente del panel Información y a los hipervínculos internos.

## Redirigir a una página Web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

El atributo `href` del mapa de imagen tiene una dirección URL al recurso externo, especificada explícitamente o envuelta en una de las funciones de plantilla JavaScript admitidas: `loadProduct()`, `loadProductCW()` y `loadProductPW()`.

A continuación se muestra un ejemplo de redirección de URL sencilla:

`href=http://www.adobe.com`

En este ejemplo, la misma dirección URL se ajusta a la función `loadProduct()`:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Tenga en cuenta que cuando agrega el código JavaScript al atributo `HREF` del mapa de imágenes, el código se ejecuta en el equipo del cliente. Por lo tanto, asegúrese de que el código JavaScript es seguro.

## Activación emergente del panel de información {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabajar con paneles de información, un mapa de imagen tiene el atributo `ROLLOVER_KEY` establecido. Además, configure el atributo `href` al mismo tiempo; de lo contrario, el procesamiento de la URL externa interfiere con la activación emergente del panel Información.

Por último, asegúrese de que la configuración del visor incluye los valores adecuados para los parámetros `InfoPanelPopup.template` y, opcionalmente, `InfoPanelPopup.infoServerUrl`.

>[!NOTE]
>
>Tenga en cuenta que, al configurar la ventana emergente del panel de información, el código HTML y el código JavaScript que se pasan al panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código HTML y código JavaScript sean seguros.

## Hipervínculos internos {#section-6afa4fb2fe564c429e0201f019a95849}

Al hacer clic en un mapa de imagen, se realiza un intercambio de páginas internas dentro del visor. Para utilizar esa función, un atributo `href` del mapa de imagen tiene el siguiente formato especial:

` href=target: *`idx`*`

donde `*`idx`*` es un índice basado en cero del pliego del catálogo.

A continuación se muestra un ejemplo de un atributo `href` para un mapa de imagen que apunta al pliego 3D en el catálogo electrónico:

`href=target:2`
