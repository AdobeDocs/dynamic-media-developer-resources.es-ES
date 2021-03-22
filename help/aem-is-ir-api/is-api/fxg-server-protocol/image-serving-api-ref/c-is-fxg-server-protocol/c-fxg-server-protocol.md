---
description: Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.
seo-description: Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.
seo-title: Protocolo del servidor FXG
solution: Experience Manager
title: Protocolo del servidor FXG
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 63%

---


# Protocolo del servidor FXG{#fxg-server-protocol}

Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.

Así, un gráfico se puede rotar, ajustar a escala o cambiar de tamaño en relación con un punto de referencia concreto. Los puntos de referencia son `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` y `southeast`. Por ejemplo, si se utiliza el punto de referencia centro, el gráfico se puede rotar 45 grados con respecto a su centro. Esta ilustración muestra dónde se encuentran los puntos de referencia, un gráfico, el gráfico rotado 20 grados desde su punto de referencia `northWest` y el gráfico rotado 20 grados desde su punto de referencia `east`.

![](assets/wp_ref_points.png)

* A. Ubicaciones de los puntos de referencia
* B. Gráfico A
* C. El gráfico rotó 20 grados desde su punto de referencia `northWest`
* D. El gráfico rotó 20 grados desde su punto de referencia `east`

La sintaxis es la siguiente:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

El valor predeterminado es none. El valor `inherit` pasa el valor `s7:referencePoint` (siempre que no sea `none`) del principio de la página o del primer nivel de grupo a todos los elementos secundarios. La configuración `none` indica que no existe ningún punto de referencia para el objeto sino que se usa el sistema de coordenadas de FXG.

>[!NOTE]
>
>para utilizar un punto de referencia sin que se produzca ningún desplazamiento en el objeto después de su manipulación, actualice los valores x e y del objeto tras manipularlo.

Si se emplea un valor de `s7:referencePoint`   con grupos (o trazados, elementos de línea u otros elementos sin una definición explícita de anchura y altura), se aplica al cuadro delimitador acumulativo del grupo. Por ejemplo, el punto superior izquierdo del cuadro delimitador de todos los objetos del grupo sirve como punto de referencia `northWest` para el grupo; el punto inferior derecho sirve como punto de referencia de `southEast`.

