---
description: textPs= admite varios modelos de uso diferentes que se describen en esta sección.
seo-description: textPs= admite varios modelos de uso diferentes que se describen en esta sección.
seo-title: Capas de texto
solution: Experience Manager
title: Capas de texto
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ccef969-7c54-49ce-b6ff-ae4eabfcf99b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 0%

---


# Capas de texto{#text-layers}

textPs= admite varios modelos de uso diferentes que se describen en esta sección.

>[!NOTE]
>
>Esta sección no se aplica a `text=`.

Las reglas y definiciones comunes son las siguientes:

* Las capas de texto de tamaño propio son capas que no incluyen un `size=` comando o para las que `size=0,0` se especifica.

* El tamaño de capa de las capas de texto con tamaño propio viene determinado por el texto real procesado.
* El anclaje de capa predeterminado de capas de texto con tamaño propio *no se encuentra* generalmente en el centro de la capa (véase más abajo).
* Si se especifica `anchor=` o `origin=` para capas de texto con tamaño propio, el contenido del texto influye en la posición de la capa de texto.

* Cuando `size=` se especifica, las partes de los glifos de caracteres pueden representarse fuera del rectángulo de la capa.
* `pos=` puede utilizarse en todos los casos para cambiar la posición de una capa de texto.

## Texto de punto (tamaño propio) {#section-db99ec98eb114458b2dbc9911a58f74a}

El texto de punto de estilo Photoshop se simula cuando `textPs=` se especifica sin `size=`, `textPath=`o `textFlowPath=`. El tamaño de la capa se determina horizontalmente según la anchura del texto procesado y verticalmente según el interlineado. El texto nunca se ajustará automáticamente.

Si no `anchor=` se especifica ni `origin=` , la primera línea del texto se coloca inmediatamente encima del origen de la capa; los párrafos marcados con `\ql` se sitúan a la derecha del origen de capas, los párrafos que incluyen `\qr` se procesan a la izquierda del origen y los párrafos con `\qc` centrado horizontalmente alrededor del origen. Si se especifican `anchor=` o `origin=` se especifican reglas de posición de capas estándar.

Si `color=` se especifica, rellena el cuadro delimitador del texto real procesado.

Se omiten los siguientes comandos RTF: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Cuadro de texto rectangular {#section-1d3ab11df26d4004a1a801546756475d}

Si `size=` se especifica además de `textPs=` (sin `textPath=` y `textFlowPath=`), el texto se limita al rectángulo especificado. La capa se coloca de la forma habitual. Los glifos de caracteres cerca de los bordes del cuadro de texto pueden procesarse parcialmente fuera del cuadro de texto.

`color=` rellena la región definida por `size=`.

Todos los comandos RTF se aplican según lo esperado.

## Cuadro de texto Altura variable {#section-e1233d1c9f8e43218667361dc0c4fd06}

Si se especifica `size=` con una altura de 0, el cuadro de texto se puede ajustar verticalmente para dar cabida a todo el contenido. La anchura de la capa se define por la anchura de la capa `size=`y la altura de la capa por la altura del texto procesado real. La capa se coloca de la forma habitual. Los glifos de caracteres cerca de los bordes izquierdo y derecho del cuadro de texto pueden procesarse parcialmente fuera del cuadro de texto.

`color=` rellena el rectángulo definido con la anchura especificada `size=` y la altura del texto real procesado.

Se omiten los siguientes comandos RTF:

`\vertal*`

## Cambiar el tamaño del texto en la ruta {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` conjuntamente con `textPs=` puede utilizarse para definir una o varias regiones en las que debe fluir el texto. `textFlowXPath=` se puede especificar de forma opcional para excluir el flujo de texto a una o varias áreas. Si no `size=` se especifica, la capa de texto resultante se ajusta a sí misma y el tamaño de la capa se determina mediante el cuadro delimitador del texto realmente procesado.

Si no se especifica ninguno `origin=` ni `anchor=` , el anclaje de capa establece de forma predeterminada (0,0) el espacio de coordenadas de píxeles utilizado para definir los trazados, lo que garantiza una posición absoluta independientemente del texto procesado. Si se especifica `anchor=` o `origin=` , la capa se coloca en relación con el cuadro delimitador del contenido real procesado (y se adapta a él).

`color=` rellena el cuadro delimitador del texto real procesado.

Se omiten los siguientes comandos RTF:

`\marg*`

## Texto de tamaño previo en ruta {#section-ed492a8a54414cd4bde360500cec6968}

Si `size=` se especifica junto con `textFlowPath=`, el tamaño de la capa se determina previamente. (0,0) del espacio de coordenadas de píxeles utilizado para definir los trazados se encuentra en la esquina superior izquierda del rectángulo de la capa.

Las `textFlowPath=` regiones pueden estar situadas fuera del rectángulo de la capa. El texto siempre fluye y se procesa en todas las regiones de ruta, incluso si el resultado es que el texto se procesa fuera del rectángulo de la capa. `extend=0,0,0,0`se puede utilizar para recortar el texto procesado en el rectángulo de la capa.

Para la colocación de capas, el rectángulo de capa se basa en el `size=`objeto especificado, independientemente de la cantidad de texto que se procese, incluso si parte de él se encuentra fuera del rectángulo de la capa. Se aplica la posición de capa estándar.

`color=` rellena el área rectangular definida por `size=`.

Los siguientes comandos RTF se omiten para `textFlowPath=`:

`\marg*`

## Cambiar el tamaño del texto en la ruta {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` define una o varias rutas en las que se debe procesar el texto especificado con `textPs=` . Cuando no `size=` se especifica, la capa de texto resultante se ajusta automáticamente. El tamaño de la capa viene determinado por el cuadro delimitador del texto real procesado.

Si no se especifica ninguno `origin=` ni `anchor=` , el anclaje de capa establece de forma predeterminada (0,0) el espacio de coordenadas de píxeles utilizado para definir el trazado; la posición del texto procesado es fija independientemente de la cantidad de texto que se procese. Si se especifica `anchor=` o `origin=` , la capa se coloca en relación con el cuadro delimitador del contenido real procesado (y se adapta a él).

`color=` rellena el cuadro delimitador del texto real procesado.

Se omiten los siguientes comandos RTF:

* `\marg*`
* `\hyph*`
* `\vertal*`

Se ignora todo el texto posterior al primero `\par` o `\line` .

## Texto de tamaño previo en la ruta {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Si `size=` se especifica junto con `textPath=`, el tamaño de la capa se determina previamente. (0,0) del espacio de coordenadas de píxeles utilizado para definir los trazados se encuentra en la esquina superior izquierda del rectángulo de la capa.

Los trazados pueden ubicarse parcial o totalmente fuera del rectángulo de la capa. El texto siempre se aplicará y representará a lo largo de todo el trazado, incluso si está fuera del rectángulo de la capa. `extend=0,0,0,0` se puede utilizar para recortar el texto procesado en el rectángulo de la capa.

Para la colocación de capas, el rectángulo de la capa se basa en el `size=`objeto especificado, aunque parte del texto se procese fuera del rectángulo de la capa. Se aplica la posición de capa estándar.

`color=` rellena el área definida por `size=`.

Se omiten los siguientes comandos RTF:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Se ignora todo el texto posterior al primero `\par` o `\line` .
