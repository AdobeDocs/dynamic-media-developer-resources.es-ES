---
description: La especificación RTF permite valores de color RGB especificados con \colortbl. Cada componente se proporciona por separado con los comandos \red, \green y \blue.
seo-description: La especificación RTF permite valores de color RGB especificados con \colortbl. Cada componente se proporciona por separado con los comandos \red, \green y \blue.
seo-title: Gestión de color
solution: Experience Manager
title: Gestión de color
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 341693d69fc414dacf984d66e2eaeba2418e663b

---


# Gestión de color{#color-handling}

La especificación RTF permite valores de color RGB especificados con `\colortbl`. Cada componente se proporciona por separado con los comandos `\red`, `\green`y `\blue` .

El comando de extensión RTF patentado `\cmykcolortbl` permite especificar colores CMYK, con cada componente de color proporcionado con los comandos `\cyan`, `\magenta`, `\yellow`y `\black` .

Los valores de los componentes de color para `\colortbl` están en el rango de 0 a 255. Los valores de componente para `\cmykcolortbl` están en el rango de 0 a 100.

El comando de extensión RTF `\*\iscolortbl`, admitido por `textPs=`, permite especificar una tabla de colores con valores de color estándar del servicio de imágenes, con compatibilidad completa con RGB, gris, CMYK y alfa. Tiene la siguiente sintaxis:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* uno o varios valores de color IS, separados por &#39;;&#39;

Se puede especificar más de un tipo de tabla de color en la misma cadena `text=` o `textPs=` RTF. Cada tabla de color puede tener un número diferente de entradas. El servicio de imágenes intentará encontrar colores en este orden: `\iscolortbl` before `\cmykcolortbl` (solo si el tipo de píxel de la capa de texto es CMYK) before `\colortbl`. Por `textPs=` ejemplo, los colores se convierten con precisión entre CMYK y RGB si es necesario (por ejemplo, cuando se especifican colores RGB pero se requiere una salida CMYK). Si no se encuentra ningún color para un valor de índice determinado, se utiliza el color predeterminado (negro).

Consulte [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) para ver una descripción de la sintaxis de los valores de color IS.

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` no admite `\*\iscolortbl`. `textPs=` no admite `\cmykcolortbl`.

Las selecciones de color se omiten al procesar las fuentes fotográficas.

## Ejemplo {#section-0f166bb72bd44479be01131077851142}

Permita que se controlen tres colores de texto con variables, mientras se muestra el valor predeterminado de color cuando se abre la cadena RTF en un editor de texto RTF estándar.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
