---
description: El visor de búsqueda en el catálogo electrónico admite la renderización de iconos de mapa de imagen encima de la vista principal.
solution: Experience Manager
title: Compatibilidad con mapas de imágenes
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Compatibilidad con mapas de imágenes{#image-map-support}

El visor de búsqueda en el catálogo electrónico admite la renderización de iconos de mapa de imagen encima de la vista principal.

El aspecto de los iconos de mapa se controla mediante CSS, tal como se describe en [Image map effect](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Los mapas de imágenes realizan una de las tres acciones siguientes: redirija a una página web externa, a la activación emergente del panel de información y a los hipervínculos internos.

## Redirigir a una página web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

El atributo `href` del mapa de imagen tiene una dirección URL para el recurso externo, ya sea especificada explícitamente o envuelta en una de las funciones de plantilla JavaScript admitidas: `loadProduct()`, `loadProductCW()` y `loadProductPW()`.

El siguiente es un ejemplo de redireccionamiento de URL simple:

`href=http://www.adobe.com`

En este ejemplo, la misma dirección URL se ajusta con la función `loadProduct()` :

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Tenga en cuenta que cuando agrega el código JavaScript al atributo `HREF` del mapa de imagen, el código se ejecuta en el equipo del cliente. Por lo tanto, asegúrese de que el código JavaScript sea seguro.

## Activación de la ventana emergente del panel de información {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabajar con paneles de información, un mapa de imagen tiene el atributo `ROLLOVER_KEY` establecido. Además, establezca el atributo `href` al mismo tiempo; de lo contrario, el procesamiento externo de la URL interfiere con la activación del panel emergente Información.

Por último, asegúrese de que la configuración del visor incluya los valores adecuados para los parámetros `InfoPanelPopup.template` y, opcionalmente, `InfoPanelPopup.infoServerUrl`.

>[!NOTE]
>
>Tenga en cuenta que, al configurar la ventana emergente del panel de información, el código HTML y el código JavaScript que se pasan al panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código HTML y código JavaScript sean seguros.

## Hipervínculos internos {#section-6afa4fb2fe564c429e0201f019a95849}

Al hacer clic en un mapa de imagen, se realiza un intercambio de páginas interno dentro del visualizador. Para utilizar esa función, un atributo `href` en el mapa de imágenes tiene el siguiente formato especial:

` href=target: *`idx`*`

donde `*`idx`*` es un índice de base cero del diferencial del catálogo.

El siguiente es un ejemplo de atributo `href` para un mapa de imagen que señala a la extensión 3D en el catálogo electrónico:

`href=target:2`
