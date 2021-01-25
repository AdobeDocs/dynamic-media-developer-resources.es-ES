---
description: Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.
seo-description: Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.
seo-title: Protocolo de servidor FXG
solution: Experience Manager
title: Protocolo de servidor FXG
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 65%

---


# Protocolo de servidor FXG{#fxg-server-protocol}

Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.

Así, un gráfico se puede rotar, ajustar a escala o cambiar de tamaño en relación con un punto de referencia concreto. Los puntos de referencia son `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` y `southeast`. Por ejemplo, si se utiliza el punto de referencia centro, el gráfico se puede rotar 45 grados con respecto a su centro. Esta ilustración muestra dónde están ubicados los puntos de referencia, un gráfico, el gráfico rotado 20 grados con respecto a su punto de referencia `northWest` y el gráfico rotado 20 grados con respecto a su punto de referencia `east`.

![](assets/wp_ref_points.png)

* A. Ubicaciones de puntos de referencia
* B. Un gráfico
* C. Gráfico rotado 20 grados con respecto a su punto de referencia `northWest`
* D. Gráfico rotado 20 grados con respecto a su punto de referencia `east`

La sintaxis es la siguiente:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

El valor predeterminado es none. El valor `inherit` pasa el valor `s7:referencePoint` (siempre que no sea `none`) del principio de la página o del primer nivel de grupo a todos los elementos secundarios. La configuración `none` indica que no existe ningún punto de referencia para el objeto sino que se usa el sistema de coordenadas de FXG.

>[!NOTE]
>
>para utilizar un punto de referencia sin que se produzca ningún desplazamiento en el objeto después de su manipulación, actualice los valores x e y del objeto tras manipularlo.

Si se emplea un valor de `s7:referencePoint`   con grupos (o trazados, elementos de línea u otros elementos sin una definición explícita de anchura y altura), se aplica al cuadro delimitador acumulativo del grupo. Por ejemplo, el punto superior izquierdo del cuadro delimitador de todos los objetos del grupo sirve como punto de referencia `northWest` para el grupo; el punto inferior derecho sirve como punto de referencia `southEast`.

