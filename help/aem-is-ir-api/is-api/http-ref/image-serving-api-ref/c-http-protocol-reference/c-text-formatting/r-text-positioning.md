---
title: Posición del texto
description: El procesador text= coloca el texto en una posición fundamentalmente diferente a textPs= renderer cuando se aplica a capas predimensionadas (es decir, cuando size= también se especifica).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Posición del texto{#text-positioning}

El `text=` el procesador coloca el texto de forma fundamentalmente diferente al textPs= renderer cuando se aplica a capas de tamaño previo (es decir, cuando se especifica size= también).

Autonivelado `text=`y `textPs=` las capas tienen un aspecto y una posición similares.

El `textPs=` alinea la parte superior de la celda de caracteres con la parte superior del cuadro de texto (suponiendo que `\vertalt`), incluso si el resultado es que partes de los glifos de texto procesados se extiendan parcialmente fuera del límite del cuadro de texto. Los glifos procesados de ciertas fuentes también pueden sobresalir ligeramente más allá de los bordes izquierdo y derecho del cuadro de texto. Para las aplicaciones que requieren que todo el texto procesado esté contenido dentro del rectángulo de capa, el archivo RTF `\marg*` comandos o `textFlowPath=` se puede utilizar para ajustar el área de procesamiento de texto.

Por el contrario, `text=` cambia el texto procesado según sea necesario y garantiza que todos los glifos procesados se ajusten completamente al cuadro de texto especificado.

While `text=` puede ser ligeramente más fácil de usar para aplicaciones sencillas, `textPs=` ofrece una colocación precisa independientemente de las caras de la fuente y los efectos de texto.

## Ejemplos {#section-1b6bdf2ea34447528188ae4e1430ee71}

Los siguientes ejemplos son para texto con tamaño previo. El comportamiento para el texto de tamaño personalizado es diferente.

** `Text=` siempre proporciona un margen estrecho en la parte superior:**

![Posición del texto, ejemplo, una imagen](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` representa el texto perfectamente alineado con la parte superior del cuadro de texto, lo que da como resultado un ligero recorte, incluso para fuentes comunes como Arial®:**

![Imagen de ejemplo 2 de posición de texto](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` desplaza automáticamente el texto procesado hacia abajo para evitar el recorte:**

![Posición del texto ejemplo tres imágenes](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` no mueve el texto que contiene partes elevadas, lo que produce un recorte significativo si el texto está en la capa 0:**

![Ejemplo de posición de texto para cuatro imágenes](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Un margen de 10 puntos (200 twips) en la parte superior procesa este texto sin recortar:**

![Imagen de ejemplo cinco de posición de texto](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Los glifos procesados de ciertas fuentes de script pueden extenderse significativamente fuera del cuadro de texto:**

![Imagen de ejemplo de posición de texto de seis](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
