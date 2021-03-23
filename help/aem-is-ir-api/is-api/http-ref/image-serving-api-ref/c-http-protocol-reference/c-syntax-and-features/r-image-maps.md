---
description: IS proporciona mecanismos para simplificar el uso de mapas de imágenes HTML. Los visores basados en JAVA y basados en Flash en IS también incluyen compatibilidad limitada con mapas de imágenes.
seo-description: IS proporciona mecanismos para simplificar el uso de mapas de imágenes HTML. Los visores basados en JAVA y basados en Flash en IS también incluyen compatibilidad limitada con mapas de imágenes.
seo-title: Mapas de imágenes
solution: Experience Manager
title: Mapas de imágenes
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Mapas de imágenes{#image-maps}

IS proporciona mecanismos para simplificar el uso de mapas de imágenes HTML. Los visores basados en JAVA y basados en Flash en IS también incluyen compatibilidad limitada con mapas de imágenes.

Los mapas de imagen de origen se proporcionan a IS mediante `catalog::Map` o con el comando `map=` y los mapas procesados se recuperan mediante el comando `req=map`.

Un mapa de imagen consta de uno o más elementos de AREA HTML, delimitados correctamente por &#39;&lt;&#39; y &#39;>&#39;. Si se proporciona a través del catálogo::Map, se supone que todos los valores de coordenadas de píxeles están en la resolución de imagen original y en relación con la esquina superior izquierda de la imagen de origen (sin modificar). Cuando se proporciona mediante un comando `map=`, se asume que los valores de coordenadas son coordenadas de capa, en relación con la esquina superior izquierda de la capa (después de `rotate=` y `extend=`).

>[!NOTE]
>
>Las coordenadas % no están permitidas en este momento y pueden procesarse incorrectamente.

IS genera un mapa de imagen compuesto a partir de los mapas de imagen de origen de cada capa constituyente aplicando las transformaciones espaciales (como el escalado y la rotación) a las coordenadas del mapa y, a continuación, montando los mapas de capa procesados en el orden z apropiado (de frente a atrás) y con la posición adecuada.

Los siguientes comandos se consideran para el procesamiento de mapas de imágenes cuando se proporcionan junto con `req=map` (ya sea directamente en la solicitud, a través de plantillas de catálogo o en cadenas `catalog::Modifier` ):

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

Todos los demás comandos se ignoran de forma efectiva.

Los atributos `SHAPE` y `COORDS` de una `AREA` se pueden modificar durante el procesamiento de una solicitud `req=map`, y todos los demás atributos del elemento `AREA` se pasan sin modificación. En la mayoría de los casos esto implica cambiar el valor `SHAPE` de `DEFAULT` a `RECT` (esto también agregaría el atributo `COORDS`) o cambiar los valores `COORDS`.

Cualquier elemento `AREA` que quede vacío durante el procesamiento se eliminará por completo. Si un mapa está asociado con `layer=comp` se coloca detrás de todos los demás mapas. Los datos se devuelven en el formulario de texto uno como o más elementos HTML `AREA`. Una cadena de respuesta vacía indica que no existe ningún mapa de imagen para los objetos especificados.

La transparencia de capa no se tiene en cuenta para el procesamiento de mapas. Una capa totalmente transparente aún puede tener asociado un mapa de imagen. El mapa de una capa parcialmente transparente no se recortará a las regiones transparentes.

## Véase también {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), especificación  [HTML 4.01](http://www.w3.org/TR/html401/)
