---
description: Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.
seo-description: Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.
seo-title: Protocolo de servidor FXG
solution: Experience Manager
title: Protocolo de servidor FXG
topic: Scene7 Image Serving - Image Rendering API
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# Protocolo de servidor FXG{#fxg-server-protocol}

Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.

Así, un gráfico se puede rotar, ajustar a escala o cambiar de tamaño en relación con un punto de referencia concreto. Los puntos de referencia son `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south`y `southeast`. Por ejemplo, si se utiliza el punto de referencia centro, el gráfico se puede rotar 45 grados con respecto a su centro. This illustration shows where the reference points are located, a graphic, the graphic rotated 20 degrees from its `northWest` reference point, and the graphic rotated 20 degrees from its `east` reference point.

![](assets/wp_ref_points.png)

* A. Ubicaciones de puntos de referencia
* B. Un gráfico
* C. The graphic rotated 20 degrees from its `northWest` reference point
* D. The graphic rotated 20 degrees from its `east` reference point

La sintaxis es la siguiente:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

El valor predeterminado es none. El valor `inherit` pasa el valor `s7:referencePoint` (siempre que no sea `none`) del principio de la página o del primer nivel de grupo a todos los elementos secundarios. La configuración `none` indica que no existe ningún punto de referencia para el objeto sino que se usa el sistema de coordenadas de FXG.

>[!NOTE]
>
>para utilizar un punto de referencia sin que se produzca ningún desplazamiento en el objeto después de su manipulación, actualice los valores x e y del objeto tras manipularlo.

Si se emplea un valor de `s7:referencePoint`   con grupos (o trazados, elementos de línea u otros elementos sin una definición explícita de anchura y altura), se aplica al cuadro delimitador acumulativo del grupo. For example, the top-left point of the bounding box of all the objects in the group serves as the `northWest` reference point for the group; the bottom-right point serves as the `southEast` reference point.

