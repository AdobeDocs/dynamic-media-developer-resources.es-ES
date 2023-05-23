---
description: textPs= admite varios modelos de uso diferentes descritos en esta sección.
solution: Experience Manager
title: Capas de texto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%

---

# Capas de texto{#text-layers}

textPs= admite varios modelos de uso diferentes descritos en esta sección.

>[!NOTE]
>
>Esta sección no se aplica a `text=`.

Las reglas y definiciones comunes son las siguientes:

* Las capas de texto de tamaño personalizado son capas que no incluyen un `size=` comando o para el que `size=0,0` se ha especificado.

* El tamaño de capa de las capas de texto de tamaño personalizado viene determinado por el texto real procesado.
* El anclaje de capa predeterminado de las capas de texto de tamaño propio suele ser *no* en el centro de la capa (ver abajo).
* If `anchor=` o `origin=` se especifica para capas de texto de tamaño personalizado, la posición de la capa de texto se ve afectada por el contenido del texto.

* Cuándo `size=` se especifica, las partes de los glifos de caracteres se pueden representar fuera del rectángulo de capa.
* `pos=` se puede utilizar en todos los casos para cambiar la posición de una capa de texto.

## Texto puntual (ajuste automático) {#section-db99ec98eb114458b2dbc9911a58f74a}

El texto de punto de estilo Photoshop se simula cuando `textPs=` se especifica sin `size=`, `textPath=`, o `textFlowPath=`. El tamaño de la capa se determina horizontalmente por la anchura del texto procesado y verticalmente por el interlineado. El texto nunca se ajustará automáticamente.

Si ninguno `anchor=` ni `origin=` se especifican, la primera línea del texto se coloca inmediatamente encima del origen de la capa; los párrafos marcados con `\ql` se sitúan a la derecha del origen de la capa, los párrafos que incluyen `\qr` se representan a la izquierda del origen y los párrafos con `\qc` se centran horizontalmente alrededor del origen. Las reglas de colocación de capa estándar se aplican si `anchor=` o `origin=` se han especificado.

If `color=` se especifica, rellena el cuadro delimitador del texto real representado.

Los siguientes comandos RTF se omiten: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Cuadro de texto rectangular {#section-1d3ab11df26d4004a1a801546756475d}

If `size=` se especifica además de `textPs=` (sin `textPath=` y `textFlowPath=`), el texto está restringido al rectángulo especificado. La capa se coloca de la forma habitual. Los glifos de caracteres cerca de los bordes del cuadro de texto pueden representarse parcialmente fuera del cuadro de texto.

`color=` rellena la región definida por `size=`.

Todos los comandos RTF se aplican según lo esperado.

## Cuadro de texto de altura variable {#section-e1233d1c9f8e43218667361dc0c4fd06}

Especificación `size=` con 0 alto permite cambiar el tamaño del cuadro de texto verticalmente para incluir todo el contenido. El ancho de la capa se define mediante el ancho de `size=`y la altura de la capa por la altura del texto procesado real. La capa se coloca de la forma habitual. Los glifos de caracteres cerca de los bordes izquierdo y derecho del cuadro de texto pueden representarse parcialmente fuera del cuadro de texto.

`color=` rellena el rectángulo definido con la anchura especificada con `size=` y la altura del texto real representado.

Los siguientes comandos RTF se omiten:

`\vertal*`

## Texto de tamaño personalizado en ruta {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` junto con `textPs=` se puede utilizar para definir una o más regiones en las que el texto debe fluir. `textFlowXPath=` puede especificarse opcionalmente para excluir el texto de una o más áreas. If `size=` no se ha especificado, la capa de texto resultante es de tamaño propio y el tamaño de la capa viene determinado por el cuadro delimitador del texto que se representa.

Si ninguno `origin=` ni `anchor=` Si se especifican, el anclaje de capa toma el valor predeterminado (0,0) del espacio de coordenadas de píxel utilizado para definir los trazados, lo que garantiza una posición absoluta independientemente del texto procesado. If `anchor=` o `origin=` Cuando se especifican, la capa se coloca en relación (y se adapta) al cuadro delimitador del contenido real representado.

`color=` rellena el cuadro delimitador del texto real representado.

Los siguientes comandos RTF se omiten:

`\marg*`

## Texto de tamaño previo en la ruta {#section-ed492a8a54414cd4bde360500cec6968}

If `size=` se especifica junto con `textFlowPath=`, el tamaño de la capa está predeterminado. (0,0) del espacio de coordenadas de píxel utilizado para definir los trazados se encuentra en la esquina superior izquierda del rectángulo de capa.

El `textFlowPath=` Las regiones pueden estar situadas fuera del rectángulo de capa. El texto siempre tendrá una posición variable y se procesará en todas las áreas de trazado, incluso si esto hace que el texto se procese fuera del rectángulo de capa. `extend=0,0,0,0`se puede utilizar para recortar el texto procesado en el rectángulo de capa.

Para el posicionamiento de capas, el rectángulo de capa se basa en el especificado `size=`, independientemente de la cantidad de texto que se procese realmente, incluso si parte de él se encuentra fuera del rectángulo de capa. Se aplica la posición de capa estándar.

`color=` rellena el área rectangular definida por `size=`.

Los siguientes comandos RTF se omiten para `textFlowPath=`:

`\marg*`

## Texto de tamaño personalizado en ruta {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` define una o más rutas en las que se especifica texto con `textPs=` debería procesarse. Cuándo `size=` no se ha especificado, la capa de texto resultante es de tamaño automático. El tamaño de la capa está determinado por el cuadro delimitador del texto real representado.

Si ninguno `origin=` ni `anchor=` Si se especifican, el anclaje de capa toma el valor predeterminado (0,0) del espacio de coordenadas de píxel utilizado para definir el trazado; la posición del texto procesado se fija independientemente de la cantidad de texto procesado. If `anchor=` o `origin=` Cuando se especifican, la capa se coloca en relación (y se adapta) al cuadro delimitador del contenido real representado.

`color=` rellena el cuadro delimitador del texto real representado.

Los siguientes comandos RTF se omiten:

* `\marg*`
* `\hyph*`
* `\vertal*`

Cualquier texto después del primero `\par` o `\line` se ignora.

## Texto de tamaño previo en la ruta {#section-a3bbbc5187f448b192e53d27e2c53f2f}

If `size=` se especifica junto con `textPath=`, el tamaño de la capa está predeterminado. (0,0) del espacio de coordenadas de píxel utilizado para definir los trazados se encuentra en la esquina superior izquierda del rectángulo de capa.

Los trazados pueden estar situados parcial o totalmente fuera del rectángulo de capa. El texto siempre se aplicará y procesará a lo largo de todo el trazado, incluso fuera del rectángulo de capa. `extend=0,0,0,0` se puede utilizar para recortar el texto procesado en el rectángulo de capa.

Para el posicionamiento de capas, el rectángulo de capa se basa en el especificado `size=`, incluso si parte del texto se procesa fuera del rectángulo de capa. Se aplica la posición de capa estándar.

`color=` rellena el área definida por `size=`.

Los siguientes comandos RTF se omiten:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Cualquier texto después del primero `\par` o `\line` se ignora.
