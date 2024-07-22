---
description: textPs= admite varios modelos de uso diferentes descritos en esta sección.
solution: Experience Manager
title: Capas de texto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# Capas de texto{#text-layers}

textPs= admite varios modelos de uso diferentes descritos en esta sección.

>[!NOTE]
>
>Esta sección no se aplica a `text=`.

Las reglas y definiciones comunes son las siguientes:

* Las capas de texto de tamaño personalizado son capas que no incluyen un comando `size=` o para las que se ha especificado `size=0,0`.

* El tamaño de capa de las capas de texto de tamaño personalizado viene determinado por el texto real procesado.
* El anclaje de capa predeterminado de las capas de texto de tamaño personalizado suele ser *no* en el centro de la capa (ver a continuación).
* Si se especifica `anchor=` o `origin=` para las capas de texto de tamaño personalizado, la posición de la capa de texto se verá afectada por el contenido del texto.

* Cuando se especifica `size=`, se pueden representar partes de glifos de caracteres fuera del rectángulo de capa.
* `pos=` se puede usar en todos los casos para cambiar la posición de una capa de texto.

## Texto puntual (ajuste automático) {#section-db99ec98eb114458b2dbc9911a58f74a}

El texto de punto de estilo Photoshop se simula cuando `textPs=` se especifica sin `size=`, `textPath=` o `textFlowPath=`. El tamaño de la capa se determina horizontalmente por la anchura del texto procesado y verticalmente por el interlineado. El texto nunca se ajusta automáticamente.

Si no se especifica ni `anchor=` ni `origin=`, la primera línea del texto se coloca inmediatamente encima del origen de la capa; los párrafos marcados con `\ql` se colocan a la derecha del origen de la capa, los párrafos que incluyen `\qr` se representan a la izquierda del origen y los párrafos con `\qc` se centran horizontalmente alrededor del origen. Se aplican reglas de colocación de capas estándar si se especifican `anchor=` o `origin=`.

Si se especifica `color=`, rellena el cuadro delimitador del texto real representado.

Se omiten los siguientes comandos RTF: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Cuadro de texto rectangular {#section-1d3ab11df26d4004a1a801546756475d}

Si se especifica `size=` además de `textPs=` (sin `textPath=` y `textFlowPath=`), el texto se restringirá al rectángulo especificado. La capa se coloca de la forma habitual. Los glifos de caracteres cerca de los bordes del cuadro de texto pueden representarse parcialmente fuera del cuadro de texto.

`color=` rellena la región definida por `size=`.

Todos los comandos RTF se aplican según lo esperado.

## Cuadro de texto de altura variable {#section-e1233d1c9f8e43218667361dc0c4fd06}

Si se especifica `size=` con 0 alto, el cuadro de texto puede ajustarse verticalmente para ajustarse a todo el contenido. La anchura de la capa se define mediante la anchura de `size=` y la altura de la capa por la altura del texto procesado real. La capa se coloca de la forma habitual. Los glifos de caracteres cerca de los bordes izquierdo y derecho del cuadro de texto pueden representarse parcialmente fuera del cuadro de texto.

`color=` rellena el rectángulo definido por la anchura especificada con `size=` y se representa la altura del texto real.

Los siguientes comandos RTF se omiten:

`\vertal*`

## Texto de tamaño personalizado en ruta {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` junto con `textPs=` se pueden usar para definir una o más regiones en las que el texto debe fluir. `textFlowXPath=` se puede especificar de manera opcional para excluir el texto de fluir a una o más áreas. Si no se especifica `size=`, la capa de texto resultante cambiará de tamaño automáticamente y el tamaño de la capa se determinará mediante el cuadro delimitador del texto que se representa realmente.

Si no se especifica ni `origin=` ni `anchor=`, el anclaje de capa toma el valor predeterminado (0,0) del espacio de coordenadas de píxel utilizado para definir las rutas, lo que garantiza una posición absoluta independientemente del texto procesado. Si se especifican `anchor=` o `origin=`, la capa se coloca en relación con el cuadro delimitador del contenido real representado (y se adapta a él).

`color=` rellena el cuadro delimitador del texto real representado.

Los siguientes comandos RTF se omiten:

`\marg*`

## Texto de tamaño previo en la ruta {#section-ed492a8a54414cd4bde360500cec6968}

Si se especifica `size=` junto con `textFlowPath=`, el tamaño de la capa está predeterminado. (0,0) del espacio de coordenadas de píxel utilizado para definir los trazados se encuentra en la esquina superior izquierda del rectángulo de capa.

Las regiones de `textFlowPath=` pueden estar ubicadas fuera del rectángulo de capa. El texto siempre fluye y se procesa en todas las áreas de trazado, incluso si esto hace que el texto se procese fuera del rectángulo de capa. `extend=0,0,0,0` se puede usar para recortar el texto procesado en el rectángulo de capa.

Para posicionar la capa, el rectángulo de capa se basa en el `size=` especificado, independientemente de la cantidad de texto que se procese realmente, incluso si parte de él se encuentra fuera del rectángulo de capa. Se aplica la posición de capa estándar.

`color=` rellena el área rectangular definida por `size=`.

Los siguientes comandos RTF se omiten para `textFlowPath=`:

`\marg*`

## Texto de tamaño personalizado en ruta {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` define una o más rutas de acceso en las que se debe representar el texto especificado con `textPs=`. Si no se especifica `size=`, la capa de texto resultante cambiará de tamaño automáticamente. El tamaño de la capa está determinado por el cuadro delimitador del texto real representado.

Si no se especifica ni `origin=` ni `anchor=`, el delimitador de capa toma el valor predeterminado (0,0) del espacio de coordenadas de píxel utilizado para definir la ruta; la posición del texto procesado es fija independientemente de la cantidad de texto procesado. Si se especifican `anchor=` o `origin=`, la capa se coloca en relación con el cuadro delimitador del contenido real representado (y se adapta a él).

`color=` rellena el cuadro delimitador del texto real representado.

Los siguientes comandos RTF se omiten:

* `\marg*`
* `\hyph*`
* `\vertal*`

Se ignora cualquier texto posterior a los primeros `\par` o `\line`.

## Texto de tamaño previo en la ruta {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Si se especifica `size=` junto con `textPath=`, el tamaño de la capa está predeterminado. (0,0) del espacio de coordenadas de píxel utilizado para definir los trazados se encuentra en la esquina superior izquierda del rectángulo de capa.

Los trazados pueden estar situados parcial o totalmente fuera del rectángulo de capa. El texto siempre se aplica y se procesa a lo largo de todo el trazado, incluso fuera del rectángulo de capa. `extend=0,0,0,0` se puede usar para recortar el texto procesado en el rectángulo de capa.

Para posicionar la capa, el rectángulo de capa se basa en el `size=` especificado, incluso si parte del texto se procesa fuera del rectángulo de capa. Se aplica la posición de capa estándar.

`color=` rellena el área definida por `size=`.

Los siguientes comandos RTF se omiten:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Se ignora cualquier texto posterior a los primeros `\par` o `\line`.
