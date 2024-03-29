---
title: Protocolo de servidor FXG
description: Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 57%

---

# Protocolo de servidor FXG{#fxg-server-protocol}

Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.

Así, un gráfico se puede rotar, ajustar a escala o cambiar de tamaño en relación con un punto de referencia concreto. Los puntos de referencia son `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south`, y `southeast`. Por ejemplo, si utiliza el punto de referencia central, puede girar un gráfico 45° sobre su centro. La siguiente imagen muestra dónde se encuentran los puntos de referencia, un gráfico, el gráfico girado 20° desde su posición `northWest` punto de referencia y el gráfico girado 20° respecto a su `east` punto de referencia.

![Imagen de puntos de referencia](assets/wp_ref_points.png)

* A. Ubicaciones de los puntos de referencia
* B. Un gráfico
* C. El gráfico giró 20° desde su `northWest` punto de referencia
* D. El gráfico giró 20° desde su `east` punto de referencia

La sintaxis es la siguiente:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

El valor predeterminado es none. El valor `inherit` pasa el valor `s7:referencePoint` (siempre que no sea `none`) del principio de la página o del primer nivel de grupo a todos los elementos secundarios. La configuración `none` indica que no existe ningún punto de referencia para el objeto sino que se usa el sistema de coordenadas de FXG.

>[!NOTE]
>
>para utilizar un punto de referencia sin que se produzca ningún desplazamiento en el objeto después de su manipulación, actualice los valores x e y del objeto tras manipularlo.

Si se emplea un valor de `s7:referencePoint`   con grupos (o trazados, elementos de línea u otros elementos sin una definición explícita de anchura y altura), se aplica al cuadro delimitador acumulativo del grupo. Por ejemplo, el punto superior izquierdo del cuadro delimitador de todos los objetos del grupo sirve como `northWest` punto de referencia para el grupo; el punto inferior derecho sirve como `southEast` punto de referencia.
