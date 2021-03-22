---
description: El procesador text= coloca el texto en una posición fundamentalmente diferente al procesador textPs= cuando se aplica a capas de tamaño previo (es decir, cuando se especifica size= también).
seo-description: El procesador text= coloca el texto en una posición fundamentalmente diferente al procesador textPs= cuando se aplica a capas de tamaño previo (es decir, cuando se especifica size= también).
seo-title: Colocación de texto
solution: Experience Manager
title: Colocación de texto
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---


# Colocación de texto{#text-positioning}

El procesador text= coloca el texto en una posición fundamentalmente diferente al procesador textPs= cuando se aplica a capas de tamaño previo (es decir, cuando se especifica size= también).

Las capas `text=`y `textPs=` de tamaño automático tienen un aspecto y una posición similares.

`textPs=` alinea la parte superior de la celda de caracteres con la parte superior del cuadro de texto (suponiendo  `\vertalt`), incluso si esto resulta en partes de los glifos de texto procesados que se extienden parcialmente fuera del límite del cuadro de texto. Los glifos procesados de ciertas fuentes también pueden sobresalir ligeramente más allá de los bordes izquierdo y derecho del cuadro de texto. Para las aplicaciones que requieren que todo el texto procesado esté contenido dentro del rectángulo de capa, los comandos RTF `\marg*` o `textFlowPath=` pueden utilizarse para ajustar el área de procesamiento del texto.

Por el contrario, `text=` cambiará el texto procesado según sea necesario y garantizará que todos los glifos procesados encajen completamente dentro del cuadro de texto especificado.

Aunque `text=` puede ser un poco más fácil de usar para aplicaciones simples, `textPs=` ofrece una posición precisa, independiente de las caras de las fuentes y los efectos de texto.

## Ejemplos {#section-1b6bdf2ea34447528188ae4e1430ee71}

Los siguientes ejemplos son para texto de tamaño previo. El comportamiento del texto con tamaño propio es diferente.

** `Text=` siempre proporciona un margen estrecho en la parte superior:**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` representa el texto perfectamente alineado en la parte superior del cuadro de texto, lo que puede resultar en un ligero recorte, incluso para fuentes comunes como Arial:**

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` desplazará automáticamente el texto procesado hacia abajo para evitar el recorte:**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` no moverá texto que contenga partes aumentadas, lo que dará como resultado un recorte significativo si el texto está en la capa 0:**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Un margen de 10 pt (200 twips) en la parte superior procesa este texto sin recorte:**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Los glifos procesados de ciertas fuentes de script pueden extenderse significativamente fuera del cuadro de texto:**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
