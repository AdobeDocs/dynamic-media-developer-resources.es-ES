---
description: El visor de búsqueda en el catálogo electrónico admite la representación de iconos de mapa de imagen encima de la vista principal.
solution: Experience Manager
title: Compatibilidad con mapas de imagen
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Compatibilidad con mapas de imagen{#image-map-support}

El visor de búsqueda en el catálogo electrónico admite la representación de iconos de mapa de imagen encima de la vista principal.

El aspecto de los iconos de mapa se controla mediante CSS como se describe en [Efecto de mapa de imagen](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Los mapas de imagen realizan una de las tres acciones siguientes: redireccionar a una página web externa, activar el panel de información emergente e hipervínculos internos.

## Redirigir a una página web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

El `href` El atributo del mapa de imagen tiene una dirección URL del recurso externo, especificada explícitamente o ajustada a una de las funciones de plantilla JavaScript admitidas: `loadProduct()`, `loadProductCW()`, y `loadProductPW()`.

El siguiente es un ejemplo de redireccionamiento de URL simple:

`href=http://www.adobe.com`

En este ejemplo, la misma dirección URL se incluye con el `loadProduct()` función:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Tenga en cuenta que cuando agregue el código JavaScript a la variable `HREF` del mapa de imagen, el código se ejecuta en el equipo del cliente. Por lo tanto, asegúrese de que el código JavaScript sea seguro.

## Activación emergente del panel de información {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabajar con paneles de información, un mapa de imagen tiene el `ROLLOVER_KEY` conjunto de atributos. Además, configure el `href` al mismo tiempo, de lo contrario el procesamiento de URL externo interfiere con la activación emergente del panel Información.

Por último, asegúrese de que la configuración del visor incluye los valores adecuados para `InfoPanelPopup.template` y, opcionalmente, `InfoPanelPopup.infoServerUrl` parámetros.

>[!NOTE]
>
>Tenga en cuenta que, al configurar el elemento emergente del Panel de información, el código de HTML y el código JavaScript que se pasan al Panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código de HTML y código JavaScript sean seguros.

## Hipervínculos internos {#section-6afa4fb2fe564c429e0201f019a95849}

Al hacer clic en un mapa de imagen, se realiza un intercambio de página interno dentro del visor. Para utilizar esa función, puede `href` el atributo en el mapa de imagen tiene el siguiente formato especial:

` href=target: *`idx`*`

donde `*`idx`*` es un índice de base cero del pliego de catálogos.

El siguiente es un ejemplo de un `href` para un mapa de imagen que apunta a la propagación 3D en el catálogo electrónico:

`href=target:2`
