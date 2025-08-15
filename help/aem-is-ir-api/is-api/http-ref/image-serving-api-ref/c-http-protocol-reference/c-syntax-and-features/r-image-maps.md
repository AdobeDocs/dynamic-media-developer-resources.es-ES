---
description: IS proporciona mecanismos para simplificar el uso de los mapas de imagen de HTML. Los visores basados en JAVA y Flash de IS también admiten de forma limitada los mapas de imágenes.
solution: Experience Manager
title: Mapas de imagen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Mapas de imagen{#image-maps}

IS proporciona mecanismos para simplificar el uso de los mapas de imagen de HTML. Los visores basados en JAVA y Flash de IS también admiten de forma limitada los mapas de imágenes.

Los mapas de imágenes de Source se proporcionan a IS mediante `catalog::Map` o con el comando `map=`, y los mapas procesados se recuperan mediante el comando `req=map`.

Un mapa de imagen consta de uno o más elementos HTML AREA, delimitados correctamente con &#39;&lt;&#39; y &#39;>&#39;. Si se proporciona a través de catalog::Map, se asume que todos los valores de coordenadas de píxel están en la resolución de imagen original y en relación con la esquina superior izquierda de la imagen de origen (sin modificar). Cuando se proporciona mediante un comando `map=`, se supone que los valores de coordenadas son coordenadas de capa, en relación con la esquina superior izquierda de la capa (después de `rotate=` y `extend=`).

>[!NOTE]
>
>Las coordenadas % no están permitidas en este momento y pueden procesarse incorrectamente.

IS genera un mapa de imagen compuesto a partir de los mapas de imagen de origen de cada capa constituyente aplicando las transformaciones espaciales (como el escalado y la rotación) a las coordenadas del mapa y, a continuación, montando los mapas de capa procesados en el orden z adecuado (de delante hacia atrás) y con la posición adecuada.

Los siguientes comandos se tienen en cuenta para el procesamiento de mapas de imágenes cuando se proporcionan junto con `req=map` (ya sea directamente en la solicitud, mediante plantillas de catálogo o en cadenas de `catalog::Modifier`):

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

Los atributos `SHAPE` y `COORDS` de un(a) `AREA` se pueden modificar durante el procesamiento de una solicitud `req=map`; todos los demás atributos del elemento `AREA` se pasan sin modificación. En la mayoría de los casos, esto implica cambiar el valor `SHAPE` de `DEFAULT` a `RECT` (esto también agregaría el atributo `COORDS`) o cambiar los valores `COORDS`.

Cualquier elemento `AREA` que se vacíe durante el procesamiento se eliminará por completo. Si un mapa está asociado con `layer=comp`, se coloca detrás de todos los demás mapas. Los datos se devuelven en texto a partir de uno o más elementos de HTML `AREA`. Una cadena de respuesta vacía indica que no existe ningún mapa de imagen para los objetos especificados.

La transparencia de capa no se tiene en cuenta para el procesamiento de mapas. Una capa totalmente transparente puede seguir teniendo asociado un mapa de imagen. El mapa de una capa parcialmente transparente no se recorta a las regiones transparentes.

## Véase también {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catálogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [Especificación de HTML 4.01](https://www.w3.org/TR/html401/)
