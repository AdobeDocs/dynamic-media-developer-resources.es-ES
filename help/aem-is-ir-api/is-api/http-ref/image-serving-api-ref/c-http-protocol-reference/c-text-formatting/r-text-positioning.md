---
title: Colocación de texto
description: El procesador text= coloca el texto en una posición fundamentalmente diferente al procesador textPs= cuando se aplica a capas de tamaño previo (es decir, cuando se especifica size= también).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Colocación de texto{#text-positioning}

El procesador `text=` coloca el texto en una posición fundamentalmente diferente al procesador textPs= cuando se aplica a capas de tamaño previo (es decir, cuando también se especifica size= ).

Las capas `text=`y `textPs=` de tamaño automático tienen un aspecto y una posición similares.

El `textPs=` alinea la parte superior de la celda de caracteres con la parte superior del cuadro de texto (suponiendo `\vertalt`), aunque tenga como resultado partes de los glifos de texto procesados que se extienden parcialmente fuera del límite del cuadro de texto. Los glifos procesados de ciertas fuentes también pueden sobresalir ligeramente más allá de los bordes izquierdo y derecho del cuadro de texto. Para las aplicaciones que requieren que todo el texto procesado esté contenido dentro del rectángulo de capa, los comandos RTF `\marg*` o `textFlowPath=` pueden utilizarse para ajustar el área de procesamiento del texto.

Por el contrario, `text=` cambia el texto procesado según sea necesario y garantiza que todos los glifos procesados encajen completamente dentro del cuadro de texto especificado.

Aunque `text=` puede ser un poco más fácil de usar para aplicaciones simples, `textPs=` ofrece una posición precisa, independiente de las caras de las fuentes y los efectos de texto.

## Ejemplos {#section-1b6bdf2ea34447528188ae4e1430ee71}

Los siguientes ejemplos son para texto de tamaño previo. El comportamiento del texto con tamaño propio es diferente.

** `Text=` siempre proporciona un margen estrecho en la parte superior:**

![Ejemplo de posición de texto una imagen](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` representa el texto perfectamente alineado en la parte superior del cuadro de texto, lo que resulta en un ligero recorte, incluso para fuentes comunes como Arial®:**

![Ejemplo de posición de texto dos imágenes](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` desplaza automáticamente el texto representado hacia abajo para evitar el recorte:**

![Imagen de ejemplo de posición de texto de tres imágenes](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` no mueve texto que contenga partes aumentadas, lo que resulta en un recorte significativo si el texto está en la capa 0:**

![Ejemplo de posición del texto cuatro](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Un margen de 10 pt (200 twips) en la parte superior procesa este texto sin recorte:**

![Ejemplo de posición de texto cinco imagen](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Los glifos procesados de ciertas fuentes de script pueden extenderse significativamente fuera del cuadro de texto:**

![Ejemplo de posición de texto seis imágenes](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
