---
description: El visor de búsqueda de catálogos electrónicos admite la representación de iconos de mapas de imagen sobre la vista principal.
seo-description: El visor de búsqueda de catálogos electrónicos admite la representación de iconos de mapas de imagen sobre la vista principal.
seo-title: Compatibilidad con mapas de imagen
solution: Experience Manager
title: Compatibilidad con mapas de imagen
topic: Dynamic media
uuid: 22ba8168-b384-4eda-a147-ce8172cfed11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Compatibilidad con mapas de imagen{#image-map-support}

El visor de búsqueda de catálogos electrónicos admite la representación de iconos de mapas de imagen sobre la vista principal.

El aspecto de los iconos de mapa se controla mediante CSS, tal como se describe en el efecto [de mapa de](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)imagen.

Los mapas de imagen realizan una de las tres acciones siguientes: redirija a una página web externa, a la activación emergente del panel Información y a los hipervínculos internos.

## Redirigir a una página web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

El `href` atributo del mapa de imagen tiene una dirección URL al recurso externo, especificada explícitamente o encerrada en una de las funciones de plantilla JavaScript admitidas: `loadProduct()`, `loadProductCW()`, y `loadProductPW()`.

A continuación se muestra un ejemplo de redirección de URL sencilla:

`href=http://www.adobe.com`

En este ejemplo, la misma dirección URL se ajusta a la `loadProduct()` función:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Be aware that when you add the JavaScript code into the `HREF` attribute of your image map, the code is run on the client’s computer. Por lo tanto, asegúrese de que el código JavaScript es seguro.

## activación emergente del panel de información {#section-7aa036420af646d1ad8cdc388add0b57}

Para trabajar con paneles de información, un mapa de imagen tiene el `ROLLOVER_KEY` atributo definido. Asimismo, defina el `href` atributo al mismo tiempo; de lo contrario, el procesamiento de la URL externa interfiere con la activación emergente del panel Información.

Por último, asegúrese de que la configuración del visor incluye los valores adecuados para `InfoPanelPopup.template` y, opcionalmente, para los parámetros `InfoPanelPopup.infoServerUrl` .

>[!NOTE]
>
>Tenga en cuenta que, al configurar la ventana emergente del panel de información, el código HTML y el código JavaScript que se pasan al panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código HTML y código JavaScript sean seguros.

## Hipervínculos internos {#section-6afa4fb2fe564c429e0201f019a95849}

Al hacer clic en un mapa de imagen, se realiza un intercambio de páginas internas dentro del visor. Para utilizar esa función, un `href` atributo del mapa de imagen tiene el siguiente formato especial:

` href=target: *`idx`*`

donde ` *`idx`*` es un índice basado en cero del pliego de catálogos.

A continuación se muestra un ejemplo de un `href` atributo para un mapa de imagen que apunta al pliego 3D en el catálogo electrónico:

`href=target:2`
