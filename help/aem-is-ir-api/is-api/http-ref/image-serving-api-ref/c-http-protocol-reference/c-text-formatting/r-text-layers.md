---
description: textPs= admite varios modelos de uso diferentes que se describen en esta sección.
seo-description: textPs= admite varios modelos de uso diferentes que se describen en esta sección.
seo-title: Capas de texto
solution: Experience Manager
title: Capas de texto
uuid: 9ccef969-7c54-49ce-b6ff-ae4eabfcf99b
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---


# Capas de texto{#text-layers}

textPs= admite varios modelos de uso diferentes que se describen en esta sección.

>[!NOTE]
>
>Esta sección no se aplica a `text=`.

Las reglas y definiciones comunes son las siguientes:

* Las capas de texto de tamaño automático son capas que no incluyen un comando `size=` o para las que se especifica `size=0,0`.

* El tamaño de capa de las capas de texto autodimensionadas viene determinado por el texto procesado.
* El anclaje de capa predeterminado de capas de texto autodimensionadas generalmente está *no* en el centro de la capa (ver abajo).
* Si se especifica `anchor=` o `origin=` para capas de texto de tamaño automático, la posición de la capa de texto se ve influida por el contenido del texto.

* Cuando se especifica `size=`, se pueden representar partes de glifos de caracteres fuera del rectángulo de la capa.
* `pos=` se puede utilizar en todos los casos para cambiar la posición de una capa de texto.

## Texto específico (tamaño automático) {#section-db99ec98eb114458b2dbc9911a58f74a}

El texto de punto de estilo Photoshop se simula cuando `textPs=` se especifica sin `size=`, `textPath=` o `textFlowPath=`. El tamaño de la capa se determina horizontalmente según la anchura del texto procesado y verticalmente según el interlineado. El texto nunca se ajustará automáticamente.

Si no se especifica `anchor=` ni `origin=`, la primera línea del texto se coloca inmediatamente encima del origen de la capa; los párrafos marcados con `\ql` se colocan a la derecha del origen de la capa, los párrafos que incluyen `\qr` se representan a la izquierda del origen y los párrafos con `\qc` se centran horizontalmente alrededor del origen. Se aplican reglas de posición de capa estándar si se especifica `anchor=` o `origin=`.

Si se especifica `color=`, rellena el cuadro delimitador del texto real representado.

Se ignoran los siguientes comandos RTF: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Cuadro de texto rectangular {#section-1d3ab11df26d4004a1a801546756475d}

Si se especifica `size=` además de `textPs=` (sin `textPath=` y `textFlowPath=`), el texto se limita al rectángulo especificado. La capa se coloca de la forma habitual. Los glifos de caracteres cerca de los bordes del cuadro de texto pueden representarse parcialmente fuera del cuadro de texto.

`color=` rellena la región definida por  `size=`.

Todos los comandos RTF se aplican según lo esperado.

## Cuadro de texto de altura variable {#section-e1233d1c9f8e43218667361dc0c4fd06}

Si especifica `size=` con 0 altura, el cuadro de texto se puede ajustar verticalmente para que quepa todo el contenido. El ancho de la capa se define con el ancho `size=` y el alto de la capa con el alto del texto procesado real. La capa se coloca de la forma habitual. Los glifos de caracteres cerca de los bordes izquierdo y derecho del cuadro de texto pueden procesarse parcialmente fuera del cuadro de texto.

`color=` rellena el rectángulo definido por la anchura especificada con  `size=` y la altura del texto procesado.

Se ignoran los siguientes comandos RTF:

`\vertal*`

## Texto autodimensionado en la ruta {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` conjuntamente con se  `textPs=` puede utilizar para definir una o más regiones en las que se debe fluir el texto. `textFlowXPath=` se puede especificar de forma opcional para excluir el flujo de texto a una o más áreas. Si no se especifica `size=`, la capa de texto resultante es de tamaño automático y el tamaño de la capa viene determinado por el cuadro delimitador del texto procesado.

Si no se especifica `origin=` ni `anchor=`, el anclaje de capa toma como valor predeterminado (0,0) el espacio de coordenadas de píxeles utilizado para definir las rutas, lo que garantiza una posición absoluta independientemente del texto procesado. Si se especifican `anchor=` o `origin=`, la capa se coloca en relación (y se adapta) al cuadro delimitador del contenido real representado.

`color=` rellena el cuadro delimitador del texto real representado.

Se ignoran los siguientes comandos RTF:

`\marg*`

## Texto de tamaño previo en la ruta {#section-ed492a8a54414cd4bde360500cec6968}

Si `size=` se especifica junto con `textFlowPath=`, el tamaño de la capa se determina previamente. (0,0) del espacio de coordenadas de píxeles utilizado para definir la ruta se encuentra en la esquina superior izquierda del rectángulo de la capa.

Las regiones `textFlowPath=` pueden estar situadas fuera del rectángulo de la capa. El texto siempre se mostrará de posición variable y se procesará en todas las regiones de rutas, incluso si el texto se representa fuera del rectángulo de la capa. `extend=0,0,0,0`se puede utilizar para recortar el texto procesado en el rectángulo de capa.

Para la colocación de capas, el rectángulo de capa se basa en el `size=` especificado, independientemente de la cantidad de texto que se represente, aunque parte esté ubicada fuera del rectángulo de capa. Se aplica el posicionamiento de capa estándar.

`color=` rellena el área rectangular definida por  `size=`.

Los siguientes comandos RTF se ignoran para `textFlowPath=`:

`\marg*`

## Autodimensionamiento de texto en la ruta {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` define una o más rutas en las que se  `textPs=` debe representar el texto especificado con. Cuando no se especifica `size=`, la capa de texto resultante es de tamaño automático. El tamaño de la capa viene determinado por el cuadro delimitador del texto procesado.

Si no se especifica `origin=` ni `anchor=`, el anclaje de capa toma como valor predeterminado (0,0) el espacio de coordenadas de píxeles utilizado para definir la ruta de acceso; la posición del texto procesado es fija independientemente de la cantidad de texto procesado. Si se especifican `anchor=` o `origin=`, la capa se coloca en relación (y se adapta) al cuadro delimitador del contenido real representado.

`color=` rellena el cuadro delimitador del texto real representado.

Se ignoran los siguientes comandos RTF:

* `\marg*`
* `\hyph*`
* `\vertal*`

Se ignora cualquier texto después del primer `\par` o `\line`.

## Texto predimensionado en la ruta {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Si `size=` se especifica junto con `textPath=`, el tamaño de la capa se determina previamente. (0,0) del espacio de coordenadas de píxeles utilizado para definir la ruta se encuentra en la esquina superior izquierda del rectángulo de la capa.

Las rutas pueden estar parcialmente o completamente fuera del rectángulo de la capa. El texto siempre se aplicará y procesará a lo largo de toda la ruta, incluso si está fuera del rectángulo de la capa. `extend=0,0,0,0` se puede utilizar para recortar el texto procesado en el rectángulo de capa.

Para la colocación de capas, el rectángulo de capa se basa en el `size=` especificado, aunque parte del texto se represente fuera del rectángulo de capa. Se aplica el posicionamiento de capa estándar.

`color=` rellena el área definida por  `size=`.

Se ignoran los siguientes comandos RTF:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Se ignora cualquier texto después del primer `\par` o `\line`.
