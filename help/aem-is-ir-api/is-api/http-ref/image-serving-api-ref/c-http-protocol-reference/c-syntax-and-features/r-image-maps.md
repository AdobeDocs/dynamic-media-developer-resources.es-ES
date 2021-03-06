---
description: IS proporciona mecanismos para simplificar el uso de mapas de imágenes HTML. Los visores basados en JAVA y basados en Flash en IS también incluyen compatibilidad limitada con mapas de imágenes.
solution: Experience Manager
title: Mapas de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Mapas de imágenes{#image-maps}

IS proporciona mecanismos para simplificar el uso de mapas de imágenes HTML. Los visores basados en JAVA y basados en Flash en IS también incluyen compatibilidad limitada con mapas de imágenes.

Los mapas de imagen de origen se proporcionan a IS a través de `catalog::Map` o con la variable `map=` y los mapas procesados se recuperan utilizando la variable `req=map` comando.

Un mapa de imagen consta de uno o más elementos de ÁREA HTML, delimitados correctamente por &#39;&lt;&#39; y &#39;>&#39;. Si se proporciona a través del catálogo::Map, se supone que todos los valores de coordenadas de píxeles están en la resolución de imagen original y en relación con la esquina superior izquierda de la imagen de origen (sin modificar). Cuando se proporciona mediante una `map=` , los valores de coordenadas se asumen como coordenadas de capa, en relación con la esquina superior izquierda de la capa (después `rotate=` y `extend=`).

>[!NOTE]
>
>Las coordenadas % no están permitidas en este momento y pueden procesarse incorrectamente.

IS genera un mapa de imagen compuesto a partir de los mapas de imagen de origen de cada capa constituyente aplicando las transformaciones espaciales (como el escalado y la rotación) a las coordenadas del mapa y, a continuación, montando los mapas de capa procesados en el orden z apropiado (de frente a atrás) y con la posición adecuada.

Los siguientes comandos se consideran para el procesamiento de mapas de imágenes cuando se proporcionan junto con `req=map` (directamente en la solicitud, a través de plantillas de catálogo o en `catalog::Modifier` cadenas):

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

La variable `SHAPE` y `COORDS` atributos de un `AREA` podrá modificarse durante la transformación de un `req=map` solicitud, todos los demás atributos del `AREA` se pasan sin modificación. En la mayoría de los casos, esto implica cambiar la variable `SHAPE` valor de `DEFAULT` a `RECT` (esto también agregaría la variable `COORDS` ), o cambiar el `COORDS` valores.

Cualquiera `AREA` los elementos que pasan a estar vacíos durante el procesamiento se eliminan por completo. Si un mapa está asociado con `layer=comp` está situado detrás de todos los demás mapas. Los datos se devuelven en el formulario de texto uno como o más HTML `AREA` elementos. Una cadena de respuesta vacía indica que no existe ningún mapa de imagen para los objetos especificados.

La transparencia de capa no se tiene en cuenta para el procesamiento de mapas. Una capa totalmente transparente aún puede tener asociado un mapa de imagen. El mapa de una capa parcialmente transparente no se recortará a las regiones transparentes.

## Véase también {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catálogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [Especificación del HTML 4.01](https://www.w3.org/TR/html401/)
