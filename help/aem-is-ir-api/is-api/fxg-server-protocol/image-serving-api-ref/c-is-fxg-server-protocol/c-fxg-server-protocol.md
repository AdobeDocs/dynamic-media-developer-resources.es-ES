---
title: Protocolo de servidor FXG
description: Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
TQID: 'https://experienceleague.adobe.com/DXmhIshiUYoP-BlVe5cJFXbII9sEIdyo5YDkoKP-t0w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 28%

---

# Protocolo de servidor FXG{#fxg-server-protocol}

Para manipular un gráfico, se pueden usar puntos de referencia similares a las direcciones de una brújula.

Así, un gráfico se puede rotar, ajustar a escala o cambiar de tamaño en relación con un punto de referencia concreto. Los puntos de referencia son `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` y `southeast`. Por ejemplo, si utiliza el punto de referencia central, puede girar un gráfico 45° sobre su centro. La siguiente imagen muestra dónde se encuentran los puntos de referencia, un gráfico, el gráfico girado 20° desde su punto de referencia `northWest` y el gráfico girado 20° desde su punto de referencia `east`.

![Imagen de puntos de referencia](assets/wp_ref_points.png)

* A. Ubicaciones de los puntos de referencia
* B. Gráfico
* C. El gráfico giró 20° desde su punto de referencia `northWest`
* D. El gráfico giró 20° desde su punto de referencia `east`

La sintaxis es la siguiente:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

El valor predeterminado es ninguno. El valor `inherit` pasa el valor `s7:referencePoint`, siempre que no sea `none`, desde la parte superior del nivel de página o grupo a todos los elementos secundarios. La configuración `none` significa que no hay ningún punto de referencia para el objeto y que se utiliza el sistema de coordenadas FXG.

>[!NOTE]
>
>para utilizar un punto de referencia sin que se produzca ningún desplazamiento en el objeto después de su manipulación, actualice los valores x e y del objeto tras manipularlo.

Cuando se utiliza un valor de `s7:referencePoint` con grupos (o rutas, elementos de línea o cualquier elemento que no tenga definiciones explícitas de anchura y altura), el valor se aplica al cuadro delimitador acumulado del grupo. Por ejemplo, el punto superior izquierdo del cuadro delimitador de todos los objetos del grupo sirve como punto de referencia `northWest` para el grupo; el punto inferior derecho sirve como punto de referencia `southEast`.
