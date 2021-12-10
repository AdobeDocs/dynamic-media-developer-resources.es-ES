---
title: Compatibilidad con mapas de imágenes
description: El visor de catálogos electrónicos es compatible con la renderización de iconos de mapas de imágenes sobre la vista principal.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Compatibilidad con mapas de imágenes{#image-map-support}

El visor de catálogos electrónicos es compatible con la renderización de iconos de mapas de imágenes sobre la vista principal.

El aspecto de los iconos de asignación se controla mediante CSS, tal como se describe en [Efecto Mapa de imágenes](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Los mapas de imágenes realizan una de las tres acciones siguientes: redirija a una página web externa, a la activación emergente del panel de información y a los hipervínculos internos.

## Redirigir a una página web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

La variable `href` del mapa de imagen tiene una dirección URL para el recurso externo, ya sea especificado explícitamente o envuelto en una de las funciones de plantilla JavaScript admitidas: `loadProduct()`, `loadProductCW()`y `loadProductPW()`.

El siguiente es un ejemplo de redireccionamiento de URL simple:

`href=http://www.adobe.com`

En este ejemplo, la misma dirección URL se ajusta con la variable `loadProduct()` función:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Cuando agrega el código JavaScript a la variable `HREF` del mapa de imagen, el código se ejecuta en el equipo del cliente. Por lo tanto, asegúrese de que el código JavaScript sea seguro.

## Activación de la ventana emergente del panel de información {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabajar con paneles de información, un mapa de imagen tiene la variable `ROLLOVER_KEY` conjunto de atributos. Además, establezca la variable `href` al mismo tiempo, de lo contrario, el procesamiento externo de la URL interfiere con la activación emergente del panel Información.

Por último, asegúrese de que la configuración del visor incluya los valores adecuados para `InfoPanelPopup.template` y, opcionalmente, `InfoPanelPopup.infoServerUrl` parámetros.

>[!NOTE]
>
>Al configurar la ventana emergente del panel de información, el código de HTML y el código JavaScript que se pasan al panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código de HTML y código JavaScript sean seguros.

## Hipervínculos internos {#section-6afa4fb2fe564c429e0201f019a95849}

Al seleccionar un mapa de imagen, se realiza un intercambio de páginas interno dentro del visualizador. Para usar esa función, se debe configurar una `href` en el mapa de imagen tiene el siguiente formato especial:

` href=target: *`idx`*`

Donde `*`idx`*` es un índice de base cero del diferencial del catálogo.

El siguiente es un ejemplo de `href` para un mapa de imagen que señala a la extensión 3D en el catálogo electrónico:

`href=target:2`
