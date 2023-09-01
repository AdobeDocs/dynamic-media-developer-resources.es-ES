---
title: Gestión de color
description: La especificación RTF permite valores de color de RGB especificados con &bsol;colortbl. Cada componente se proporciona por separado con los comandos &bsol;red, &bsol;green y &bsol;blue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Gestión de color{#color-handling}

La especificación RTF permite valores de color de RGB especificados con `\colortbl`. Cada componente se proporciona por separado con la variable `\red`, `\green`, y `\blue` comandos.

El comando de extensión RTF propiedad `\cmykcolortbl` permite especificar colores CMYK, con cada componente de color proporcionado con el `\cyan`, `\magenta`, `\yellow`, y `\black` comandos.

Valores de componentes de color para `\colortbl` están en el rango 0-255. Valores de componente para `\cmykcolortbl` están en el rango 0-100.

El comando RTF extension `\*\iscolortbl`, compatible con `textPs=`, proporciona una forma de especificar una tabla de colores con valores de color estándar del servicio de imágenes, con compatibilidad con RGB completos, grises, CMYK y alfa. Tiene la siguiente sintaxis:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* uno o varios valores de color IS, separados con &#39;;&#39;

Se puede especificar más de un tipo de tabla de colores en el mismo `text=` o `textPs=` Cadena RTF. Cada tabla de colores puede tener un número diferente de entradas. El servicio de imágenes intenta encontrar los colores en este orden: `\iscolortbl` antes `\cmykcolortbl` (solo si el tipo de píxel de la capa de texto es CMYK) antes de `\colortbl`. Para `textPs=` Sólo los colores se convierten con precisión entre CMYK y RGB, si es necesario (por ejemplo, cuando se especifican colores de RGB pero se requiere salida CMYK). Si no se encuentra ningún color para un valor de índice determinado, se utiliza el color predeterminado (negro).

Consulte [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) para obtener una descripción de la sintaxis de los valores de color IS.

## Restricciones {#section-c5173e672d854e4aa9656844f7fc4d0e}

El modificador `text=` no admite `\*\iscolortbl`. El modificador `textPs=` no admite `\cmykcolortbl`.

Las selecciones de color se ignoran al procesar Photofonts.

## Ejemplo {#section-0f166bb72bd44479be01131077851142}

Permite controlar tres colores de texto con variables, mientras se sigue mostrando el valor predeterminado de color cuando se abre la cadena RTF en un editor de texto RTF estándar.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
