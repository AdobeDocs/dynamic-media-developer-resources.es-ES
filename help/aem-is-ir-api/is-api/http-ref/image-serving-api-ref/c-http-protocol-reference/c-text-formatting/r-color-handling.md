---
title: Gestión de color
description: La especificación RTF permite valores de color RGB especificados con &bsol;colortbl. Cada componente se proporciona por separado con los comandos &bsol;red, &bsol;green y &bsol;blue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
TQID: 'https://experienceleague.adobe.com/w5IfFwmdMegueJbDMjwvb5XCPuemRcJ1XTqcJFgdEMQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# Gestión de color{#color-handling}

La especificación RTF permite valores de color RGB especificados con `\colortbl`. Cada componente se proporciona por separado con los comandos `\red`, `\green` y `\blue`.

El comando de extensión RTF propiedad `\cmykcolortbl` permite especificar colores CMYK, con cada componente de color proporcionado con los comandos `\cyan`, `\magenta`, `\yellow` y `\black`.

Los valores de los componentes de color de `\colortbl` están en el intervalo de 0 a 255. Los valores de componente de `\cmykcolortbl` están en el intervalo de 0 a 100.

El comando de extensión RTF `\*\iscolortbl`, admitido por `textPs=`, proporciona una forma de especificar una tabla de colores con valores de color estándar del servicio de imágenes, con compatibilidad total con RGB, gris, CMYK y alfa. Tiene la siguiente sintaxis:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* uno o más valores de color IS, separados con &#39;;&#39;

Se puede especificar más de un tipo de tabla de colores en la misma cadena RTF `text=` o `textPs=`. Cada tabla de colores puede tener un número diferente de entradas. El servicio de imágenes intenta encontrar colores en este orden: `\iscolortbl` antes de `\cmykcolortbl` (solo si el tipo de píxel de la capa de texto es CMYK) antes de `\colortbl`. Solo para `textPs=`, los colores se convierten con precisión entre CMYK y RGB, si es necesario (por ejemplo, cuando se especifican colores RGB pero se requiere la salida CMYK). Si no se encuentra ningún color para un valor de índice determinado, se utiliza el color predeterminado (negro).

Consulte [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) para obtener una descripción de la sintaxis de los valores de color IS.

## Restricciones {#section-c5173e672d854e4aa9656844f7fc4d0e}

El modificador `text=` no admite `\*\iscolortbl`. El modificador `textPs=` no admite `\cmykcolortbl`.

Las selecciones de color se ignoran al procesar Photofonts.

## Ejemplo {#section-0f166bb72bd44479be01131077851142}

Permite controlar tres colores de texto con variables, mientras se sigue mostrando el valor predeterminado de color cuando se abre la cadena RTF en un editor de texto RTF estándar.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
